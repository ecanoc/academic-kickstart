+++
# A Demo section created with the Blank widget.
# Any elements can be added in the body: https://sourcethemes.com/academic/docs/writing-markdown-latex/
# Add more sections by duplicating this file and customizing to your requirements.

widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 15  # Order that this section will appear.
share = false
profile = false
date = "2019-06-23"


title = "Viewer"
subtitle = ""

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "1"

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "white"
  
  # Background gradient.
  #gradient_start = "DarkGreen"
  # gradient_end = "ForestGreen"
  
  # Background image.
  # image = "image.jpg"  # Name of image in `static/img/`.
  # image_darken = 0.6  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.

  # Text color (true=light or false=dark).
  # text_color_light = true

[design.spacing]
  # Customize the section spacing. Order is top, right, bottom, left.
  padding = ["20px", "0", "20px", "0"]

[advanced]
 # Custom CSS. 
 css_style = "midiplayer"
 
 # CSS class.
 css_class = ""

+++
<div class="panel-body">
    <button onclick="renderMei()" class="dropbtn">Render</button>
    <select id="country">
			<option value="None">-- Select --</option>
			<option value="ID001"selected>me.mei</option>
			<option value="ID002">test.mei</option>
			<option value="ID003">Track 3</option>
		</select>
    <button onclick="play_midi()" class="dropbtn">Play</button>
    <div style="height: 30px;">
            <div id="player" style="z-index: 20; position: absolute; display: none;"></div>
    </div>
    <div id="svg_output" class="panel" style="min-height: 800px;"/>
</div>

<script src="https://www.verovio.org/javascript/develop/verovio-toolkit.js" type="text/javascript" ></script>
<script src="https://code.jquery.com/jquery-3.1.1.min.js" type="text/javascript" ></script>
<link rel="stylesheet" href="css/midiplayer.css" />

<script type="text/javascript">
      var vrvToolkit = new verovio.toolkit();
      var zoom = 60;
      var pageheight = 2000;
      var pagewidth = 500;
      var file = "me.mei";
      var ids = [];
      var isPlaying = false;

      function setOptions() {
                //////////////////////////////////////////////////////////////
                /* Adjust the height and width according to the window size */
                //////////////////////////////////////////////////////////////
                pageHeight = $(document).height() * 100 / zoom ;
                pageWidth = $(window).width() * 75 / zoom ;
                options = {
                            pageHeight: pageHeight,
                            pageWidth: pageWidth,
                            scale: zoom,
                            adjustPageHeight: true
                        };
                vrvToolkit.setOptions(options);
            }

      ////////////////////////////////////
      /* Load the file using a HTTP GET */
      ////////////////////////////////////
      function loadData(data) {
                setOptions();
                vrvToolkit.loadData(data);
                page = 1;
                loadPage();
                
            }
      function loadPage(){
                svg = vrvToolkit.renderToSVG(page, {});
                $("#svg_output").html(svg);
                
                $(".note").click(function() {
                    var id = $(this).attr("id");
                    var time = vrvToolkit.getTimeForElement(id);
                    $("#midi-player").midiPlayer.seek(time);
                });
      }

      function renderMei(){
                var e = document.getElementById("country");
				        file = e.options[e.selectedIndex].text;
                fetch(file)
                    .then(function(response) {
                    return response.text();
                })
                .then(function(text) {
                    loadData(text);
                 });
      }

      function play_midi() {
                if (isPlaying == false) {
                    var base64midi = vrvToolkit.renderToMIDI();
                    var song = 'data:audio/midi;base64,' + base64midi;
                    $("#player").show();
                    $("#player").midiPlayer.play(song);
                    isPlaying = true;
                }
      }

      var midiUpdate = function(time) {
                
                var vrvTime = Math.max(0, time - 400);
                var elementsattime = vrvToolkit.getElementsAtTime(vrvTime);
                if (elementsattime.page > 0) {
                    if (elementsattime.page != page) {
                        page = elementsattime.page;
                        loadPage();
                    }
                    if ((elementsattime.notes.length > 0) && (ids != elementsattime.notes)) {
                        ids.forEach(function(noteid) {
                            if ($.inArray(noteid, elementsattime.notes) == -1) {
                                $("#" + noteid).attr("fill", "#000").attr("stroke", "#000");
                            }
                        });
                        ids = elementsattime.notes;
                        ids.forEach(function(noteid) {
                            if ($.inArray(noteid, elementsattime.notes) != -1) {
                                $("#" + noteid).attr("fill", "#c00").attr("stroke", "#c00");;
                            }
                        });
                    }
                }
      }

      var midiStop = function() {
                ids.forEach(function(noteid) {
                    $("#" + noteid).attr("fill", "#000").attr("stroke", "#000");
                });
                $("#player").hide();
                isPlaying = false;
      }

      $(document).ready(function() {
              $("#player").midiPlayer({
                            color: "#c00",
                            onUpdate: midiUpdate,
                            onStop: midiStop,
                            width: 250
                        });

      renderMei();       
      });
     
      
</script>



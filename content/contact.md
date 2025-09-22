---
# Leave the homepage title empty to use the site title
title: ""
share: False
cms_exclude: true
reading_time: False
show_date: false
#backlinks: false
pager: false
---

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact Us</title>
  <script src="https://www.google.com/recaptcha/api.js" async defer></script>
  <style>
    .contact-form {
      max-width: 600px;
      margin: 2rem auto;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 4px 6px 4px rgba(0, 0, 0, 0.1);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
    }
    .form-group {
      margin-bottom: 1.5rem;
    }
    .form-control {
      display: block;
      width: 100%;
      padding: 0.75rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      font-size: 1rem;
    }
    .submit-btn {
      display: inline-block;
      padding: 0.75rem 1.5rem;
      background-color: #4a90e2;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1rem;
      transition: background-color 0.3s ease;
    }
    .submit-btn:hover {
      background-color: #3578ca;
    }
    .g-recaptcha {
      margin-bottom: 1.5rem;
    }
  </style>
</head>
<body>
  <div class="contact-form">
    <h2>Contact Me</h2>
    <form action="https://api.staticforms.xyz/submit" method="POST">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" class="form-control" required>
      </div>  
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" class="form-control" required>
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" name="message" class="form-control" rows="5" required></textarea>
      </div>
      <div class="g-recaptcha" data-sitekey=6Ldm67wrAAAAAAKrnS6kiXIE57s7gKDSHnn4bKaV></div>
      <!-- Hidden fields -->
      <input type="hidden" name="apiKey" value=sf_7kjdg409lik2756e994290lm>
      <input type="hidden" name="subject" value="New Contact Form Submission">
      <input type="hidden" name="replyTo" value="@">
      <input type="hidden" name="redirectTo" value="https://yoursite.com/thank-you">
      <button type="submit" class="submit-btn">Send Message</button>
    </form>
  </div>
</body>
</html>
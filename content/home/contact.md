---
# An instance of the Contact widget.
# Documentation: https://sourcethemes.com/academic/docs/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  #form:
    #provider: netlify
    #netlify:
      # Enable CAPTCHA challenge to reduce spam?
     # captcha: true

design:
  columns: '2'
---

<form name="contact" netlify>
  <!-- Honeypot field for spam prevention -->
  <input type="hidden" name="bot-field" />

  <p>
    <label>Name <input type="text" name="name" required /></label>
  </p>
  <p>
    <label>Email <input type="email" name="email" required /></label>
  </p>
  <p>
    <label>Message <textarea name="message" rows="4" required></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

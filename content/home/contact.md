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

<form name="contact" netlify style="max-width: 900px; margin: auto; padding: 20px; border: 1px solid #ccc; border-radius: 8px; background-color: #f9f9f9;">
  <h2 style="text-align: center;">Contact Us</h2>
  
  <p>
    <label style="font-weight: bold;">Name:</label>
    <input type="text" name="name" required style="width: 100%; padding: 10px; margin: 5px 0; border-radius: 4px; border: 1px solid #ccc;" />
  </p>
  
  <p>
    <label style="font-weight: bold;">Email:</label>
    <input type="email" name="email" required style="width: 100%; padding: 10px; margin: 5px 0; border-radius: 4px; border: 1px solid #ccc;" />
  </p>
  
  <p>
    <label style="font-weight: bold;">Message:</label>
    <textarea name="message" rows="8" required style="width: 100%; padding: 10px; margin: 5px 0; border-radius: 4px; border: 1px solid #ccc;"></textarea>
  </p>
  
  <p style="text-align: center;">
    <button type="submit" style="background-color: #007bff; color: white; padding: 10px 20px; border: none; border-radius: 4px; cursor: pointer;">Send</button>
  </p>
</form>


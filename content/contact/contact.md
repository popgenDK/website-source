---
# An instance of the Contact widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 10

title: Contact
subtitle:

content:
  # Contact (edit or remove options as required)

  email: albrecht@binf.ku.dk
  phone: 35330246
  address:
    street: Ole Maaløes Vej 5, København N
    city: Copenhagen
    postcode: '2200'
    country: Denmark
    country_code: DK
  coordinates:
    latitude: '55.699760237390045'
    longitude: '12.556951373014032'
  directions: Enter Building 2 and take the stairs to Office 2.2.23 on Floor 2 (US 3rd floor)
  office_hours:
    - 'Monday 10:00 to 13:00'
    - 'Wednesday 09:00 to 10:00'
  appointment_url: 'https://calendly.com'
  #contact_links:
  #  - icon: comments
  #    icon_pack: fas
  #    name: Discuss on Forum
  #    link: 'https://discourse.gohugo.io'

  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

design:
  columns: '1'
---

Please tell us who you are. At least you are not a robot :D

---
title: Support
permalink: /support/
layout: splash
header:
  overlay_image: "/assets/images/bluebackground2.png"
class: wide
defaults:
  # _pages
  - scope:
      path: ""
      type: pages
    values:
      author_profile: true

feature_row:
  - image_path: /assets/images/ticketicon2.png
    alt: "placeholder image 1"
    title: Help us improve!
    excerpt: "Something not right? Drop us a ticket and we'll take a look!"
    url: "https://github.com/archesproject/arches/issues"
    btn_label: "File ticket"
    btn_class: "btn--inverse"
  - image_path: /assets/images/forumicon2.png
    alt: "placeholder image 2"
    title: "Visit our forum!"
    excerpt: "Join our Arches community and check out the user forum below."
    url: "https://groups.google.com/d/forum/archesproject?hl=en"
    btn_label: "Go to forum"
    btn_class: "btn--inverse"
  - image_path: /assets/images/contacticon.png
    title: "Get in contact!"
    excerpt: "Have a question? Want to make a suggestion? We would love to hear from you!."
    url: "http://localhost:4000/modeler/"
    btn_label: "Contact us"
    btn_class: "btn--inverse"

---
# Find the support you need here!

{% include feature_row %}

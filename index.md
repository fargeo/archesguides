---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: splash
header:
  overlay_image: "/assets/images/bluebackground2.png"

  excerpt: "This post should display a **header with an overlay image**, if the theme supports it."

feature_row:
    - image_path: /assets/images/modeler.jpg
      alt: "placeholder image 1"
      title: "User Guide"
      excerpt: "Explore our user guide for basic Arches set-up and customization instructions."
      url: "http://localhost:4000/user/"
      btn_label: "Go to guide"
      btn_class: "btn--info"
    - image_path: /assets/images/admin.jpg
      alt: "placeholder image 2"
      title: "Admin Guide"
      excerpt: "Check out our admin guide and learn about available Arches administrative functions."
      url: "http://localhost:4000/admin/"
      btn_label: "Go to guide"
      btn_class: "btn--info"
    - image_path: /assets/images/user.jpg
      title: "Data Modeler Guide"
      excerpt: "Unlock Arches potential with our modeler’s guide to complex data modeling capabilities."
      url: "http://localhost:4000/modeler/"
      btn_label: "Go to guide"
      btn_class: "btn--info"
---
# Check out our guides below
### No matter what kind of Arches user you are, we have a guide for you!


{% include feature_row %}

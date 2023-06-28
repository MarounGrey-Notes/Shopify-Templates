## Two column section with the custom background image
###### (Dawn Theme)

![alt text](https://github.com/MarounGrey-Notes/Shopify-Templates/blob/main/images/Screenshot%202023-06-27%20215819.png?raw=true)

```

<div class="two-col-section-bg" style="background-image: url({{ section.settings.background_image | img_url: 'master' }});">
  <div class="page-width section-{{ section.id }}-padding isolate"> 
    <div class="two-column-wrapper">
  
      <div class="column custom-section-column-left">

          <!-- Some Code Here  -->

      </div>
      
      <div class="column custom-section-column-right">

          <!-- Some Code Here  -->

      </div>

    </div>
  </div>
</div>


{% schema %}
  {
    "name": "Two Col Bg",
    "settings": [
      {
        "type": "image_picker",
        "id": "background_image",
        "label": "Select background image"
      }
    ],
    "presets": [
    {
      "name": "Two Col BG"
    }
  ]
  }
{% endschema %}


{% stylesheet %}
  .custom-contact-bg {
    background-size: cover;
    background-position: center;
    background-repeat: no repeat;
  }
  .two-column-wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .column {
    width: 48%;
  }

{% endstylesheet %}

```

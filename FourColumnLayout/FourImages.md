## Four Images in a Row

![alt text](https://github.com/MarounGrey-Notes/Shopify-Templates/blob/main/images/Screenshot%202023-06-28%20232218.png?raw=true)

```

  <div style="background-color: {{ section.settings.background_color }};">
    <div class="page-width section-{{ section.id }}-padding isolate">
      <div class="text-center">{{ section.settings.header }}</div>
  
      <div class="four-column-wrapper">
        <div class="column custom-section-column-first">
          <a href="{{ section.settings.image_link_1 }}">
            <img class="image-preview" src="{{ section.settings.image_1 | img_url: 'master' }}">
          </a>
        </div>
  
        <div class="column custom-section-column-second">
          <a href="{{ section.settings.image_link_2 }}">
            <img class="image-preview" src="{{ section.settings.image_2 | img_url: 'master' }}">
          </a>
        </div>
  
        <div class="column custom-section-column-third">
          <a href="{{ section.settings.image_link_3 }}">
            <img class="image-preview" src="{{ section.settings.image_3 | img_url: 'master' }}">
          </a>
        </div>
  
        <div class="column custom-section-column-third">
          <a href="{{ section.settings.image_link_4 }}">
            <img class="image-preview" src="{{ section.settings.image_4 | img_url: 'master' }}">
          </a>
        </div>
      </div>
    </div>
  </div>
  
  
  {% schema %}
  {
    "name": "Four Images Grid",
    "settings": [
      {
        "type": "color",
        "id": "background_color",
        "label": "Select background color"
      },
      {
        "type": "html",
        "id": "header",
        "label": "HTML",
        "default": "<h2>Custom content</h2><p>Use this advanced section to build your own layouts or to add custom HTML, Liquid, or scripts.</p>"
      },
      {
        "type": "image_picker",
        "id": "image_1",
        "label": "Image 1"
      },
      {
        "type": "url",
        "id": "image_link_1",
        "label": "Image 1 Link"
      },
      {
        "type": "image_picker",
        "id": "image_2",
        "label": "Image 2"
      },
       {
        "type": "url",
        "id": "image_link_2",
        "label": "Image 2 Link"
      },
      {
        "type": "image_picker",
        "id": "image_3",
        "label": "Image 3"
      },
       {
        "type": "url",
        "id": "image_link_3",
        "label": "Image 3 Link"
      },
      {
        "type": "image_picker",
        "id": "image_4",
        "label": "Image 4"
      },
       {
        "type": "url",
        "id": "image_link_4",
        "label": "Image 4 Link"
      }
  
    ],
    "presets": [
    {
      "name": "Four Images Grid"
    }
  ]
  }
  {% endschema %}
  
  
  {% stylesheet %}
      .four-column-wrapper {
        padding: 40px 0 80px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
      }
  
    .custom-section-column-first,
    .custom-section-column-second,
    .custom-section-column-third {
      flex-basis: 25%; /* Adjust the width as per your preference */
    }
  
    .column {
      padding: 15px;
      border-radius: 15px;
    }
  
    /* Media Query for Mobile */
    @media (max-width: 767px) {
      .custom-section-column-first,
      .custom-section-column-second,
      .custom-section-column-third {
        flex-basis: 100%;
      }
      .video-preview {
        margin: auto;
      }
    }
  {% endstylesheet %}
  
  {% javascript %}
  {% endjavascript %}

```

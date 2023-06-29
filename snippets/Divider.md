# Header, divider and paragraph
![alt text](https://github.com/MarounGrey-Notes/Shopify-Templates/assets/62679040/d54e9a8c-962c-4a4c-b203-d66f19e010f1)
```
<h2>{{ section.settings.heading_text }}</h2>
{% if section.settings.enable_divider %}
  <div style="text-align: center;">
    <hr class="divider" style="border-top: 3px solid #1299C5; width: 50%;">
  </div>
{% endif %}
<p>{{ section.settings.paragraph_text }}</p>


{% schema %}
{
  "name": "Divider",
  "settings": [
     {
      "type": "text",
      "id": "heading_text",
      "label": "Heading Text",
      "default": "Hello, World!"
    },
    {
      "type": "checkbox",
      "id": "enable_divider",
      "label": "Enable Divider",
      "default": true
    },
    {
      "type": "text",
      "id": "paragraph_text",
      "label": "Paragraph Text",
      "default": "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    }
  ],
  "presets": [
    {
      "name": "Custom Column Image Left"
    }
  ]
}
{% endschema %}


{% stylesheet %}

  .divider {
    display: block;
    margin: 0;
    padding: 0;
  }

{% endstylesheet %}
```

# Category Cards

![alt text](https://github.com/MarounGrey-Notes/Shopify-Templates/blob/main/images/Screenshot%202023-06-28%20233730.png?raw=true)

```
<div style="margin: 50px 0;">
  <h2 class="cards-heading">{{ section.settings.category_header }}</h2>
  <div class="page-width section-{{ section.id }}-padding isolate">
    <div class="card-container">

      <a href="{{ section.settings.card1_link }}" style="text-decoration: none;">
        <div class="card">
            <img src="{{ section.settings.card1_image | img_url: 'master'  }}" alt="{{ section.settings.card1.alt }}" width="58" height="58" style="margin: auto;">
            <h3>{{ section.settings.card1_title }}</h3>

        </div>
      </a>

      <a href="{{ section.settings.card2_link }}" style="text-decoration: none;">
        <div class="card">
            <img src="{{ section.settings.card2_image | img_url: 'master'  }}" alt="{{ section.settings.card2.alt }}" width="58" height="58" style="margin: auto;">
            <h3>{{ section.settings.card2_title }}</h3>
        </div>
      </a>

      <a href="{{ section.settings.card3_link }}" style="text-decoration: none;">
        <div class="card">
            <img src="{{ section.settings.card3_image | img_url: 'master'  }}" alt="{{ section.settings.card3.alt }}" width="58" height="58" style="margin: auto;">
            <h3>{{ section.settings.card3_title }}</h3>

        </div>
      </a>
          
    </div>
  </div>
</div>

{% schema %}
{
  "name": "Category Cards Section",
  "settings": [
    {
      "type": "text",
      "label": "Header",
      "id": "category_header"
    },
    {
      "type": "image_picker",
      "label": "Card 1 Image",
      "id": "card1_image"
    },
    {
      "type": "text",
      "label": "Card 1 Title",
      "id": "card1_title"
    },
    {
      "type": "url",
      "label": "Card 1 Link",
      "id": "card1_link"
    },
    {
      "type": "image_picker",
      "label": "Card 2 Image",
      "id": "card2_image"
    },
    {
      "type": "text",
      "label": "Card 2 Title",
      "id": "card2_title"
    },
    {
      "type": "url",
      "label": "Card 2 Link",
      "id": "card2_link"
    },
    {
      "type": "image_picker",
      "label": "Card 3 Image",
      "id": "card3_image"
    },
    {
      "type": "text",
      "label": "Card 3 Title",
      "id": "card3_title"
    },
    {
      "type": "url",
      "label": "Card 3 Link",
      "id": "card3_link"
    }
  ],
  "presets": [
    {
      "name": "Category Cards Section"
    }
  ]
}
{% endschema %}

{% stylesheet %}
.cards-heading {
  text-align: center;
}

.card-container {
  display: flex;
  justify-content: center;
}

.card {
  border: 2px solid #dddddd;
  padding: 20px;
  border-radius: 20px;
  margin: 10px;
  text-align: center;
}

.card:hover {
  background-color: #f4f4f4;
}

.card img {
  max-width: 100%;
}

@media (max-width: 989px) {
  .card-container {
    display: block;
    margin: auto;
  }

  .card {
    margin: 40px;
  }
}
{% endstylesheet %}

{% javascript %}
{% endjavascript %}
```

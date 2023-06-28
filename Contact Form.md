# Contact Form


### Liquid
```
<div class="contact-form">
  <h2>{{ section.settings.form_header }}</h2>
  
  <form action="/contact" method="post" id="contactForm" class="contact-form__form">
    <div class="contact-form__row">
      <div class="contact-form__field">
        <label for="firstName">First Name</label>
        <input class="contact-form__input" type="text" name="firstName" id="firstName" required placeholder="Enter Name">
      </div>
      <div class="contact-form__field">
        <label for="lastName">Last Name</label>
        <input class="contact-form__input" type="text" name="lastName" id="lastName" required placeholder="Enter Last Name">
      </div>
    </div>
    <div class="contact-form__field">
      <label for="email">Email</label>
      <input class="contact-form__input" type="email" name="email" id="email" required placeholder="Email here.">
    </div>
    <div class="contact-form__field">
      <label for="message">Message</label>
      <textarea class="contact-form__input" name="message" id="message" required placeholder="Type Message here.."></textarea>
    </div>
    <div class="contact-form__field">
      <button type="submit" class="contact-form__submit" style="background-color: {{ section.settings.button_color }};">Send Message</button>
    </div>
  </form>
</div>


{% schema %}
{
  "name": "Custom contact form",
  "settings": [
    {
      "type": "text",
      "id": "form_header",
      "label": "Contact Form Header",
      "default": "Fill Out The Form"
    },
    {
      "type": "color",
      "id": "button_color",
      "label": "Button Color",
      "default": "#1299C5"
    }
  ],
  "presets": [
  {
    "name": "Custom Contact Form"
  }
  ]
}
{% endschema %}


{% stylesheet %}

  .contact-form {
    background-color: #FFFFFF;
    padding: 3rem;
    margin: 5rem 0;
    border-radius: 20px;
    text-align: center;
  }
  .contact-form__row {
    display: flex;
    justify-content: space-between;
  }
  .contact-form__field {
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
  }
  .contact-form__field label {
    text-align: left;
    margin-bottom: 5px;
  }
  .contact-form__field input,
  .contact-form__field textarea {
    font-size: 16px;
  }
  .contact-form__input {
    padding: 15px;
    border-radius: 20px;
    border: 1px solid #d9d9d9;
    background-color: #f4f4f478;
    font-style: italic;
    font-family: 'Helvetica';
  }
  .contact-form__input:focus-visible {
    outline-offset: 0.1rem;
    box-shadow: none;
  }
  .contact-form__submit {
    color: white;
    border-radius: 20px;
    padding: 15px;
    margin-top: 1rem;
    border: none;
    text-decoration: none;
  }
@media (min-width: 1146px) {
  .contact-form__field {
    width: 100%;
    margin: 10px;
  }
}
@media (max-width: 1145px) {
    .contact-form__row {
        display: block;
    }
}

{% endstylesheet %}

```

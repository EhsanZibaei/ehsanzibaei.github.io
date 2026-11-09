---
layout: page
title: Contact
permalink: /contact/
---
<div class="contact-page">
  <header class="contact-intro">
    <p class="contact-eyebrow">Get in touch</p>
    <h1>Let’s talk about what you’re building.</h1>
    <p>
      Have a question about robotics, control systems, sensor fusion, or applied AI?
      Share a little about your project and I’ll get back to you.
    </p>
  </header>

  <form class="contact-form" action="https://formspree.io/f/myzegyoe" method="POST">
    <div class="contact-field">
      <label for="name">Name</label>
      <input type="text" id="name" name="name" autocomplete="name" required placeholder="Your name">
    </div>

    <div class="contact-field">
      <label for="email">Email</label>
      <input type="email" id="email" name="_replyto" autocomplete="email" required placeholder="you@example.com">
    </div>

    <div class="contact-field">
      <label for="message">How can I help?</label>
      <textarea id="message" name="message" required placeholder="Tell me a little about your project or question."></textarea>
    </div>

    <input type="text" name="_gotcha" tabindex="-1" autocomplete="off" hidden>

    <button type="submit">Send message <span aria-hidden="true">&rarr;</span></button>
    <p class="contact-form-note">This form is processed by Formspree.</p>
  </form>
</div>

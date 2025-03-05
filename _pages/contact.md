---
layout: page
title: Contact
permalink: /contact/
---

# Contact Me

You can reach me through the form below.


<form action="https://formspree.io/f/myzegyoe" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="_replyto" required>
    <input type="text" name="_gotcha" style="display:none">

    <label for="message">Message:</label>
    <textarea id="message" name="message" required></textarea>

    <button onclick="gtag('event', 'click', {'event_category': 'Button', 'event_label': 'Contact Form'});">
    Send
    </button>
</form>

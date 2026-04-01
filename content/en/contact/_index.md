---
title: Contact Us
linkTitle: Contact
menu: {main: {weight: 40}}
---

{{% blocks/cover title="Contact Us" height="auto" %}}

We're here to help you on your journey.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

Get in touch with us to book an appointment or learn more about our services.

{{% /blocks/lead %}}

{{% blocks/section type="row" color="white" %}}

## Location

Dr Salam Jibrel Medical Center
Kingdom of Bahrain

## Phone

- [+973 1725 5095](tel:+97317255095)
- [+973 1770 1747](tel:+97317701747)
- [+973 3928 8794](tel:+97339288794)

## WhatsApp

[+973 3727 2771](https://wa.me/97337272771)

## Working Hours

- Saturday - Thursday: 8:00 AM - 8:00 PM
- Friday: Closed

{{% /blocks/section %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">Send Us a Message</h2>

<form name="contact" method="POST" action="{{ "contact/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="contact" />

  <div class="mb-3">
    <label for="name" class="form-label fw-bold">Full Name *</label>
    <input type="text" class="form-control" id="name" name="name" required>
  </div>

  <div class="mb-3">
    <label for="email" class="form-label fw-bold">Email Address *</label>
    <input type="email" class="form-control" id="email" name="email" required>
  </div>

  <div class="mb-3">
    <label for="phone" class="form-label fw-bold">Phone Number</label>
    <input type="tel" class="form-control" id="phone" name="phone">
  </div>

  <div class="mb-3">
    <label for="subject" class="form-label fw-bold">Subject *</label>
    <select class="form-select" id="subject" name="subject" required>
      <option value="" disabled selected>Select a subject</option>
      <option value="Book an Appointment">Book an Appointment</option>
      <option value="General Inquiry">General Inquiry</option>
      <option value="Insurance Question">Insurance Question</option>
      <option value="Services Information">Services Information</option>
      <option value="Other">Other</option>
    </select>
  </div>

  <div class="mb-3">
    <label for="message" class="form-label fw-bold">Message *</label>
    <textarea class="form-control" id="message" name="message" rows="5" placeholder="How can we help you?" required></textarea>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">Send Message</button>
  </div>
</form>

</div>

{{% /blocks/section %}}

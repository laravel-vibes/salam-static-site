---
title: Happy Clients
linkTitle: Happy Clients
---

{{% blocks/cover title="Share Your Experience" height="auto" %}}

We'd love to hear about your positive experience with us.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

Your kind words mean the world to our team. If you've had a positive experience at Dr Salam Jibrel Medical Center, please take a moment to share your feedback. It inspires us to keep doing our best.

{{% /blocks/lead %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">Share Your Feedback</h2>

<form name="happy-clients" method="POST" action="{{ "happy-clients/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="happy-clients" />

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
    <label for="service" class="form-label fw-bold">Service Received</label>
    <select class="form-select" id="service" name="service">
      <option value="" disabled selected>Select a service</option>
      <option value="IVF Treatment">IVF Treatment</option>
      <option value="Consultation">Consultation</option>
      <option value="Laboratory">Laboratory</option>
      <option value="Ultrasound">Ultrasound</option>
      <option value="General Care">General Care</option>
      <option value="Other">Other</option>
    </select>
  </div>

  <div class="mb-3">
    <label class="form-label fw-bold">How would you rate your experience? *</label>
    <input type="hidden" id="rating" name="rating" required>
    <div class="star-rating d-flex gap-1" style="direction: ltr;">
      <span class="star" data-value="1">&#9733;</span>
      <span class="star" data-value="2">&#9733;</span>
      <span class="star" data-value="3">&#9733;</span>
      <span class="star" data-value="4">&#9733;</span>
      <span class="star" data-value="5">&#9733;</span>
    </div>
    <div class="form-text" id="rating-text"></div>
  </div>

  <div class="mb-3">
    <label for="feedback" class="form-label fw-bold">Your Feedback *</label>
    <textarea class="form-control" id="feedback" name="feedback" rows="6" placeholder="Tell us about your experience and what made it special..." required></textarea>
  </div>

  <div class="mb-3">
    <label for="recommend" class="form-label fw-bold">Would you recommend us to others? *</label>
    <select class="form-select" id="recommend" name="recommend" required>
      <option value="" disabled selected>Select</option>
      <option value="Yes, definitely">Yes, definitely</option>
      <option value="Yes, probably">Yes, probably</option>
      <option value="Not sure">Not sure</option>
    </select>
  </div>

  <div class="mb-3 form-check">
    <input type="checkbox" class="form-check-input" id="consent" name="consent" value="yes">
    <label class="form-check-label" for="consent">I agree to have my feedback shared publicly on the website (first name only)</label>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">Submit Feedback</button>
  </div>
</form>

</div>

<style>
.star-rating .star {
  font-size: 2.2rem;
  color: #ccc;
  cursor: pointer;
  transition: color 0.15s ease, transform 0.15s ease;
}
.star-rating .star:hover,
.star-rating .star.hovered {
  color: #f5c518;
  transform: scale(1.15);
}
.star-rating .star.selected {
  color: #f5c518;
}
</style>

<script>
(function() {
  var stars = document.querySelectorAll('.star-rating .star');
  var input = document.getElementById('rating');
  var text = document.getElementById('rating-text');
  var labels = {1:'Poor', 2:'Fair', 3:'Good', 4:'Very Good', 5:'Excellent'};

  stars.forEach(function(star) {
    star.addEventListener('click', function() {
      var val = this.getAttribute('data-value');
      input.value = val + ' Stars - ' + labels[val];
      stars.forEach(function(s) {
        s.classList.toggle('selected', s.getAttribute('data-value') <= val);
      });
      text.textContent = labels[val];
    });
    star.addEventListener('mouseenter', function() {
      var val = this.getAttribute('data-value');
      stars.forEach(function(s) {
        s.classList.toggle('hovered', s.getAttribute('data-value') <= val);
      });
    });
    star.addEventListener('mouseleave', function() {
      stars.forEach(function(s) { s.classList.remove('hovered'); });
    });
  });
})();
</script>

{{% /blocks/section %}}

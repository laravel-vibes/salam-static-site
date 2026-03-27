---
title: Complaints
linkTitle: Complaints
---

{{% blocks/cover title="Submit a Complaint" height="auto" %}}

Your feedback helps us improve our services.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

We take all complaints seriously and are committed to resolving any issues you may have experienced. Please fill out the form below and our team will review your complaint promptly.

{{% /blocks/lead %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">Complaint Form</h2>

<form name="complaints" method="POST" action="{{ "complaints/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="complaints" />

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
    <label for="date-of-visit" class="form-label fw-bold">Date of Visit</label>
    <input type="date" class="form-control" id="date-of-visit" name="date-of-visit">
  </div>

  <div class="mb-3">
    <label for="department" class="form-label fw-bold">Department *</label>
    <select class="form-select" id="department" name="department" required>
      <option value="" disabled selected>Select a department</option>
      <option value="Reception">Reception</option>
      <option value="Consultation">Consultation</option>
      <option value="Laboratory">Laboratory</option>
      <option value="Nursing">Nursing</option>
      <option value="Billing">Billing</option>
      <option value="Other">Other</option>
    </select>
  </div>

  <div class="mb-3">
    <label for="complaint" class="form-label fw-bold">Details of Your Complaint *</label>
    <textarea class="form-control" id="complaint" name="complaint" rows="6" placeholder="Please describe your experience and what went wrong..." required></textarea>
  </div>

  <div class="mb-3">
    <label for="resolution" class="form-label fw-bold">Desired Resolution</label>
    <textarea class="form-control" id="resolution" name="resolution" rows="3" placeholder="How would you like us to resolve this issue?"></textarea>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">Submit Complaint</button>
  </div>
</form>

</div>

{{% /blocks/section %}}

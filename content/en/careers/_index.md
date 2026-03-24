---
title: Careers
linkTitle: Careers
menu: {main: {weight: 37}}
---

{{% blocks/cover title="Join Our Team" height="auto" %}}

Build your career with Dr Salam Jibrel Medical Center.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

We're always looking for talented and passionate professionals to join our team. If you're dedicated to providing exceptional patient care, we'd love to hear from you.

{{% /blocks/lead %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">Apply Now</h2>

<form name="careers" method="POST" action="/careers/thank-you/" data-netlify="true" enctype="multipart/form-data">
  <input type="hidden" name="form-name" value="careers" />

  <div class="mb-3">
    <label for="name" class="form-label fw-bold">Full Name *</label>
    <input type="text" class="form-control" id="name" name="name" required>
  </div>

  <div class="mb-3">
    <label for="email" class="form-label fw-bold">Email Address *</label>
    <input type="email" class="form-control" id="email" name="email" required>
  </div>

  <div class="mb-3">
    <label for="phone" class="form-label fw-bold">Phone Number *</label>
    <input type="tel" class="form-control" id="phone" name="phone" required>
  </div>

  <div class="mb-3">
    <label for="position" class="form-label fw-bold">Position Applied For *</label>
    <select class="form-select" id="position" name="position" required>
      <option value="" disabled selected>Select a position</option>
      <option value="Doctor">Doctor</option>
      <option value="Nurse">Nurse</option>
      <option value="Lab Technician">Lab Technician</option>
      <option value="Receptionist">Receptionist</option>
      <option value="Administrative">Administrative</option>
      <option value="Other">Other</option>
    </select>
  </div>

  <div class="mb-3">
    <label for="experience" class="form-label fw-bold">Years of Experience</label>
    <input type="number" class="form-control" id="experience" name="experience" min="0" max="50">
  </div>

  <div class="mb-3">
    <label for="message" class="form-label fw-bold">Cover Letter / Message</label>
    <textarea class="form-control" id="message" name="message" rows="5" placeholder="Tell us about yourself and why you'd like to join our team..."></textarea>
  </div>

  <div class="mb-4">
    <label for="resume" class="form-label fw-bold">Upload CV / Resume *</label>
    <input type="file" class="form-control" id="resume" name="resume" accept=".pdf,.doc,.docx" required>
    <div class="form-text">Accepted formats: PDF, DOC, DOCX (max 8 MB)</div>
  </div>

  <div class="mb-3">
    <label for="documents" class="form-label fw-bold">Additional Documents</label>
    <input type="file" class="form-control" id="documents" name="documents" accept=".pdf,.doc,.docx,.jpg,.png">
    <div class="form-text">Certificates, licenses, or other supporting documents (max 8 MB total)</div>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">Submit Application</button>
  </div>
</form>

</div>

{{% /blocks/section %}}

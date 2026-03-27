---
title: الشكاوى
linkTitle: الشكاوى
---

{{% blocks/cover title="تقديم شكوى" height="auto" %}}

ملاحظاتك تساعدنا على تحسين خدماتنا.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

نتعامل مع جميع الشكاوى بجدية ونلتزم بحل أي مشكلات قد تكون واجهتها. يرجى ملء النموذج أدناه وسيقوم فريقنا بمراجعة شكواك على الفور.

{{% /blocks/lead %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">نموذج الشكوى</h2>

<form name="complaints-ar" method="POST" action="{{ "complaints/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="complaints-ar" />

  <div class="mb-3">
    <label for="name" class="form-label fw-bold">الاسم الكامل *</label>
    <input type="text" class="form-control" id="name" name="name" required>
  </div>

  <div class="mb-3">
    <label for="email" class="form-label fw-bold">البريد الإلكتروني *</label>
    <input type="email" class="form-control" id="email" name="email" required>
  </div>

  <div class="mb-3">
    <label for="phone" class="form-label fw-bold">رقم الهاتف</label>
    <input type="tel" class="form-control" id="phone" name="phone">
  </div>

  <div class="mb-3">
    <label for="date-of-visit" class="form-label fw-bold">تاريخ الزيارة</label>
    <input type="date" class="form-control" id="date-of-visit" name="date-of-visit">
  </div>

  <div class="mb-3">
    <label for="department" class="form-label fw-bold">القسم *</label>
    <select class="form-select" id="department" name="department" required>
      <option value="" disabled selected>اختر القسم</option>
      <option value="الاستقبال">الاستقبال</option>
      <option value="الاستشارات">الاستشارات</option>
      <option value="المختبر">المختبر</option>
      <option value="التمريض">التمريض</option>
      <option value="المحاسبة">المحاسبة</option>
      <option value="أخرى">أخرى</option>
    </select>
  </div>

  <div class="mb-3">
    <label for="complaint" class="form-label fw-bold">تفاصيل الشكوى *</label>
    <textarea class="form-control" id="complaint" name="complaint" rows="6" placeholder="يرجى وصف تجربتك وما حدث..." required></textarea>
  </div>

  <div class="mb-3">
    <label for="resolution" class="form-label fw-bold">الحل المطلوب</label>
    <textarea class="form-control" id="resolution" name="resolution" rows="3" placeholder="كيف تود منا حل هذه المشكلة؟"></textarea>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">إرسال الشكوى</button>
  </div>
</form>

</div>

{{% /blocks/section %}}

---
title: اتصل بنا
linkTitle: اتصل بنا
menu: {main: {weight: 40}}
---

{{% blocks/cover title="اتصل بنا" height="auto" %}}

نحن هنا لمساعدتكم في رحلتكم.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

تواصلوا معنا لحجز موعد أو لمعرفة المزيد عن خدماتنا.

{{% /blocks/lead %}}

{{% blocks/section type="row" color="white" %}}

## الموقع

مركز د. سلام جبريل الطبي
مملكة البحرين

## الهاتف

- [٠٩٥ ٥٢٥ ١٧ ٩٧٣+](tel:+97317255095)
- [٧٤٧ ٧٠١ ١٧ ٩٧٣+](tel:+97317701747)
- [٧٩٤ ٢٨٨ ٣٩ ٩٧٣+](tel:+97339288794)

## واتساب

[٧٧١ ٢٧٢ ٣٧ ٩٧٣+](https://wa.me/97337272771)

## ساعات العمل

- السبت - الخميس: ٨:٠٠ صباحاً - ٨:٠٠ مساءً
- الجمعة: مغلق

{{% /blocks/section %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">أرسل لنا رسالة</h2>

<form name="contact-ar" method="POST" action="{{ "contact/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="contact-ar" />

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
    <label for="subject" class="form-label fw-bold">الموضوع *</label>
    <select class="form-select" id="subject" name="subject" required>
      <option value="" disabled selected>اختر الموضوع</option>
      <option value="حجز موعد">حجز موعد</option>
      <option value="استفسار عام">استفسار عام</option>
      <option value="سؤال عن التأمين">سؤال عن التأمين</option>
      <option value="معلومات عن الخدمات">معلومات عن الخدمات</option>
      <option value="أخرى">أخرى</option>
    </select>
  </div>

  <div class="mb-3">
    <label for="message" class="form-label fw-bold">الرسالة *</label>
    <textarea class="form-control" id="message" name="message" rows="5" placeholder="كيف يمكننا مساعدتك؟" required></textarea>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">إرسال الرسالة</button>
  </div>
</form>

</div>

{{% /blocks/section %}}

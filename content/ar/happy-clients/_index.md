---
title: عملاء سعداء
linkTitle: عملاء سعداء
---

{{% blocks/cover title="شاركنا تجربتك" height="auto" %}}

نود أن نسمع عن تجربتك الإيجابية معنا.
{.display-6}

{{% /blocks/cover %}}

{{% blocks/lead color="white" %}}

كلماتكم الطيبة تعني الكثير لفريقنا. إذا كانت لديك تجربة إيجابية في مركز الدكتور سلام جبريل الطبي، يرجى تخصيص لحظة لمشاركة ملاحظاتك. إنها تلهمنا لمواصلة تقديم أفضل ما لدينا.

{{% /blocks/lead %}}

{{% blocks/section color="light" %}}

<div class="mx-auto" style="max-width: 700px;">

<h2 class="text-center mb-4">شاركنا رأيك</h2>

<form name="happy-clients-ar" method="POST" action="{{ "happy-clients/thank-you/" | relLangURL }}" data-netlify="true">
  <input type="hidden" name="form-name" value="happy-clients-ar" />

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
    <label for="service" class="form-label fw-bold">الخدمة المقدمة</label>
    <select class="form-select" id="service" name="service">
      <option value="" disabled selected>اختر الخدمة</option>
      <option value="علاج أطفال الأنابيب">علاج أطفال الأنابيب</option>
      <option value="استشارة">استشارة</option>
      <option value="مختبر">مختبر</option>
      <option value="أشعة صوتية">أشعة صوتية</option>
      <option value="رعاية عامة">رعاية عامة</option>
      <option value="أخرى">أخرى</option>
    </select>
  </div>

  <div class="mb-3">
    <label class="form-label fw-bold">كيف تقيّم تجربتك؟ *</label>
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
    <label for="feedback" class="form-label fw-bold">ملاحظاتك *</label>
    <textarea class="form-control" id="feedback" name="feedback" rows="6" placeholder="أخبرنا عن تجربتك وما الذي جعلها مميزة..." required></textarea>
  </div>

  <div class="mb-3">
    <label for="recommend" class="form-label fw-bold">هل تنصح الآخرين بنا؟ *</label>
    <select class="form-select" id="recommend" name="recommend" required>
      <option value="" disabled selected>اختر</option>
      <option value="نعم، بالتأكيد">نعم، بالتأكيد</option>
      <option value="نعم، على الأرجح">نعم، على الأرجح</option>
      <option value="غير متأكد">غير متأكد</option>
    </select>
  </div>

  <div class="mb-3 form-check">
    <input type="checkbox" class="form-check-input" id="consent" name="consent" value="yes">
    <label class="form-check-label" for="consent">أوافق على مشاركة ملاحظاتي علنياً على الموقع (الاسم الأول فقط)</label>
  </div>

  <div class="text-center mt-4">
    <button type="submit" class="btn btn-primary btn-lg px-5">إرسال الملاحظات</button>
  </div>
</form>

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
  var labels = {1:'ضعيف', 2:'مقبول', 3:'جيد', 4:'جيد جداً', 5:'ممتاز'};

  stars.forEach(function(star) {
    star.addEventListener('click', function() {
      var val = this.getAttribute('data-value');
      input.value = val + ' نجوم - ' + labels[val];
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

</div>

{{% /blocks/section %}}

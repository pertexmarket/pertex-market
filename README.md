<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عرض خاص: شاحن سيارة 4 في 1 + حامل هاتف ذكي</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap');
  
  :root {
    --bg-dark: #0f172a;
    --card-bg: #1e293b;
    --accent-gold: #f59e0b;
    --gold-hover: #d97706;
    --text-light: #f8fafc;
    --text-muted: #94a3b8;
  }

  * { margin:0; padding:0; box-sizing:border-box; }
  body { font-family: 'Cairo', sans-serif; background: var(--bg-dark); color: var(--text-light); overflow-x: hidden; }

  .hero { text-align: center; padding: 40px 16px 20px; background: linear-gradient(180deg, #020617 0%, var(--bg-dark) 100%); border-bottom: 2px solid rgba(245, 158, 11, 0.2); }
  .badge { background: rgba(245, 158, 11, 0.15); color: var(--accent-gold); padding: 6px 16px; border-radius: 20px; font-size: 13px; font-weight: 700; display: inline-block; margin-bottom: 12px; border: 1px solid var(--accent-gold); }
  .hero h1 { font-size: clamp(22px, 5vw, 36px); font-weight: 900; line-height: 1.3; margin-bottom: 10px; color: var(--text-light); }
  .hero p { font-size: 15px; color: var(--text-muted); max-width: 500px; margin: 0 auto 15px; }
  .price-tag { font-size: 28px; font-weight: 900; color: var(--accent-gold); text-shadow: 0 2px 10px rgba(245,158,11,0.3); margin-top: 10px; }

  .gallery-section { padding: 30px 16px; max-width: 900px; margin: 0 auto; }
  .section-title { text-align: center; font-size: 20px; font-weight: 700; margin-bottom: 20px; color: var(--accent-gold); }
  .grid-gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 16px; }
  
  .img-card { background: var(--card-bg); border-radius: 16px; padding: 12px; border: 1px solid rgba(255,255,255,0.05); text-align: center; transition: 0.3s; }
  .img-card:hover { transform: translateY(-4px); border-color: var(--accent-gold); }
  .img-wrapper { width: 100%; height: 240px; border-radius: 12px; overflow: hidden; background: #000; margin-bottom: 10px; display:flex; align-items:center; justify-content:center; color:#64748b; font-size:13px; }
  .img-wrapper img { width: 100%; height: 100%; object-fit: cover; }
  .img-card p { font-size: 14px; font-weight: 700; color: var(--text-light); }

  .features { background: var(--card-bg); margin: 20px 16px; padding: 24px; border-radius: 18px; max-width: 700px; margin: 20px auto; border: 1px solid rgba(255,255,255,0.08); }
  .features h3 { font-size: 18px; color: var(--accent-gold); margin-bottom: 12px; }
  .features ul { list-style: none; }
  .features li { padding: 8px 0; font-size: 14px; color: var(--text-light); display: flex; align-items: center; gap: 8px; border-bottom: 1px solid rgba(255,255,255,0.05); }
  .features li:last-child { border-bottom: none; }

  .order-container { max-width: 550px; margin: 30px auto 50px; padding: 0 16px; }
  .order-card { background: #ffffff; color: #0f172a; padding: 28px 20px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
  .order-card h3 { text-align: center; font-size: 20px; font-weight: 900; margin-bottom: 20px; color: #0f172a; }

  .form-group { margin-bottom: 14px; }
  .form-group label { display: block; font-size: 13px; font-weight: 700; margin-bottom: 6px; color: #334155; }
  .form-group input, .form-group select { width: 100%; padding: 12px 14px; border-radius: 10px; border: 1.5px solid #cbd5e1; font-family: 'Cairo', sans-serif; font-size: 14px; outline: none; transition: 0.2s; background: #f8fafc; }
  .form-group input:focus, .form-group select:focus { border-color: var(--accent-gold); background: #fff; }

  .delivery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 14px; }
  .delivery-btn { border: 2px solid #cbd5e1; border-radius: 12px; padding: 12px; text-align: center; cursor: pointer; transition: 0.2s; background: #f8fafc; }
  .delivery-btn.active { border-color: var(--accent-gold); background: rgba(245, 158, 11, 0.1); }
  .delivery-btn.disabled-opt { opacity: 0.4; cursor: not-allowed; pointer-events: none; }
  .delivery-btn .d-title { font-size: 12px; font-weight: 700; }
  .delivery-btn .d-price { font-size: 14px; font-weight: 900; color: #d97706; margin-top: 2px; }

  .qty-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 18px; }
  .qty-btn { position: relative; border: 2px solid #cbd5e1; border-radius: 12px; padding: 14px 10px; text-align: center; cursor: pointer; transition: 0.2s; background: #f8fafc; }
  .qty-btn.active { border-color: var(--accent-gold); background: rgba(245, 158, 11, 0.1); box-shadow: 0 4px 14px rgba(245,158,11,0.2); }
  .qty-btn .q-title { font-size: 13px; font-weight: 700; color: #1e293b; }
  .qty-btn .q-price { font-size: 17px; font-weight: 900; color: #d97706; margin-top: 4px; }
  .qty-btn .q-old { font-size: 12px; color: #94a3b8; text-decoration: line-through; margin-inline-start: 4px; }
  .qty-btn .q-badge { position: absolute; top: -10px; right: 50%; transform: translateX(50%); background: #dc2626; color: #fff; font-size: 10px; font-weight: 900; padding: 3px 10px; border-radius: 10px; white-space: nowrap; }

  .summary { background: #f1f5f9; padding: 16px; border-radius: 12px; margin: 18px 0; border: 1px dashed #cbd5e1; }
  .summary-row { display: flex; justify-content: space-between; font-size: 14px; padding: 4px 0; color: #475569; }
  .summary-row.total { font-size: 18px; font-weight: 900; color: #0f172a; border-top: 1px solid #cbd5e1; padding-top: 8px; margin-top: 6px; }
  .summary-row.total span:last-child { color: #d97706; }

  .btn-submit { display: block; width: 100%; padding: 16px; border-radius: 12px; font-family: 'Cairo', sans-serif; font-size: 18px; font-weight: 900; border: none; background: linear-gradient(135deg, var(--accent-gold), var(--gold-hover)); color: #ffffff; cursor: pointer; transition: 0.2s; box-shadow: 0 6px 20px rgba(245,158,11,0.3); }
  .btn-submit:hover:not(:disabled) { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(245,158,11,0.5); }
  .btn-submit:disabled { opacity: 0.5; cursor: not-allowed; }

  .faq-section { margin-top: 25px; border-top: 2px dashed #e2e8f0; padding-top: 20px; }
  .faq-title { font-size: 16px; font-weight: 900; color: #0f172a; text-align: center; margin-bottom: 14px; display: flex; align-items: center; justify-content: center; gap: 6px; }
  .faq-item { background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 12px; padding: 12px 16px; margin-bottom: 10px; }
  .faq-question { font-size: 13px; font-weight: 700; color: #1e293b; margin-bottom: 4px; display: flex; align-items: center; gap: 6px; }
  .faq-answer { font-size: 13px; font-weight: 600; color: #059669; padding-right: 20px; }
</style>
</head>
<body>

<div class="hero">
  <span class="badge">🔥 العرض الأكثر طلباً لاكسسوارات السيارات</span>
  <h1>بوكس السيارة المتكامل (4 في 1) 🚗</h1>
  <p>شاحن سريع متعدد المنافذ + حامل هاتف ذكي وثابت لقيادة آمنة ومريحة</p>
  <div class="price-tag">2990 دج <span style="font-size:14px; color:var(--text-muted); text-decoration:line-through;">3900 دج</span></div>
</div>

<div class="gallery-section">
  <div class="section-title">📷 صور المنتجات في البوكس</div>
  <div class="grid-gallery">
    <div class="img-card">
      <div class="img-wrapper">صورة المنتج 1</div>
      <p>⚡ شاحن السيارة السريع 4 في 1</p>
    </div>
    <div class="img-card">
      <div class="img-wrapper">صورة المنتج 2</div>
      <p>🔌 منافذ متعددة وكوابل مدمجة</p>
    </div>
    <div class="img-card">
      <div class="img-wrapper">صورة المنتج 3</div>
      <p>📱 حامل الهاتف العالي الثبات</p>
    </div>
  </div>
</div>

<div class="features">
  <h3>مميزات البوكس:</h3>
  <ul>
    <li>✅ <strong>شاحن 4 في 1:</strong> كوابل سريعة ومنافذ شحن متعددة لشحن أكثر من هاتف في وقت واحد.</li>
    <li>✅ <strong>حامل هاتف ذكي:</strong> تثبيت قوي ومقاوم لاهتزازات الطريق مع دوران 360 درجة.</li>
    <li>✅ <strong>تصميم فاخر:</strong> متوافق مع جميع أنواع السيارات ولا يأخذ مساحة كبيرة.</li>
    <li>✅ <strong>ضمان الجودة:</strong> حماية جهازك من التيار الزائد والحرارة.</li>
  </ul>
</div>

<div class="order-container">
  <div class="order-card">
    <h3>🛒 اطلب البوكس الآن والدفع عند الاستلام</h3>
    
    <div class="form-group">
      <label>الاسم واللقب</label>
      <input type="text" id="fullname" placeholder="أدخل اسمك الكامل">
    </div>

    <div class="form-group">
      <label>رقم الهاتف</label>
      <input type="tel" id="phone" placeholder="06XXXXXXXX">
    </div>

    <div class="form-group">
      <label>الولاية</label>
      <select id="wilaya" onchange="updateDelivery()">
        <option value="">— اختر الولاية —</option>
      </select>
    </div>

    <label style="font-size:13px; font-weight:700; margin-bottom:6px; display:block; color:#334155;">اختر العرض</label>
    <div class="qty-grid">
      <div class="qty-btn active" id="btn-qty1" onclick="setQty(1)">
        <div class="q-title">📦 قطعة واحدة</div>
        <div class="q-price">2990 دج</div>
      </div>
      <div class="qty-btn" id="btn-qty2" onclick="setQty(2)">
        <span class="q-badge">وفّر 1530 دج</span>
        <div class="q-title">📦📦 قطعتين</div>
        <div class="q-price">5450 دج <span class="q-old">5980 دج</span></div>
      </div>
    </div>

    <label style="font-size:13px; font-weight:700; margin-bottom:6px; display:block; color:#334155;">نوع التوصيل</label>
    <div class="delivery-grid">
      <div class="delivery-btn" id="btn-home" onclick="setDelivery('home')">
        <div class="d-title">🏠 للمنزل</div>
        <div class="d-price" id="p-home">—</div>
      </div>
      <div class="delivery-btn" id="btn-office" onclick="setDelivery('office')">
        <div class="d-title">🏢 للمكتب</div>
        <div class="d-price" id="p-office">—</div>
      </div>
    </div>

    <div class="form-group">
      <label>البلدية / العنوان</label>
      <input type="text" id="address" placeholder="اسم البلدية أو العنوان">
    </div>

    <div class="summary">
      <div class="summary-row"><span>سعر البوكس:</span><span id="sum-box">2990 دج</span></div>
      <div class="summary-row"><span>سعر التوصيل:</span><span id="sum-del">—</span></div>
      <div class="summary-row total"><span>المجموع الكلي:</span><span id="sum-total">—</span></div>
    </div>

    <button class="btn-submit" id="submit-btn" onclick="sendOrder()" disabled>تأكيد الطلب الآن</button>

    <div class="faq-section">
      <div class="faq-title">❓ أسئلة شائعة</div>
      
      <div class="faq-item">
        <div class="faq-question">💳 طريقة الدفع؟</div>
        <div class="faq-answer">الدفع يد بيد عند استلام طلبيتك وإعادة معاينتها.</div>
      </div>

      <div class="faq-item">
        <div class="faq-question">🚚 مدة التوصيل؟</div>
        <div class="faq-answer">التوصيل سريع من يومين إلى ثلاثة أيام كأقصى حد.</div>
      </div>
    </div>

  </div>
</div>

<script>
var TELEGRAM_TOKEN = "8984328868:AAEjxhYfk_Iw6PhnSEIrsTZ3zCd_7zZHiLA"; 
var TELEGRAM_CHAT_ID = "8765345419"; 

var QTY_PRICES = { 1: 2990, 2: 5450 };
var currentQty = 1;
var BOX_PRICE = QTY_PRICES[currentQty];

var RATES = {
  "01 - Adrar": [1500, 750],
  "02 - Chlef": [900, 450],
  "03 - Laghouat": [1000, 500],
  "04 - Oum El Bouaghi": [750, 450],
  "05 - Batna": [450, 300],
  "06 - Bejaia": [800, 450],
  "07 - Biskra": [750, 450],
  "08 - Bechar": [1000, 500],
  "09 - Blida": [700, 450],
  "10 - Bouira": [900, 450],
  "11 - Tamanrasset": [1700, 800],
  "12 - Tebessa": [900, 450],
  "13 - Tlemcen": [950, 450],
  "14 - Tiaret": [950, 450],
  "15 - Tizi Ouzou": [700, 450],
  "16 - Alger": [700, 450],
  "17 - Djelfa": [1050, 600],
  "18 - Jijel": [800, 450],
  "19 - Setif": [700, 450],
  "20 - Saida": [900, 500],
  "21 - Skikda": [750, 450],
  "22 - Sidi Bel Abbes": [800, 450],
  "23 - Annaba": [750, 450],
  "24 - Guelma": [750, 450],
  "25 - Constantine": [700, 450],
  "26 - Medea": [800, 450],
  "27 - Mostaganem": [800, 450],
  "28 - Msila": [800, 450],
  "29 - Mascara": [800, 450],
  "30 - Ouargla": [900, 450],
  "31 - Oran": [800, 450],
  "32 - El Bayadh": [1150, 600],
  "33 - Illizi": [1700, 750],
  "34 - Bordj Bou Arreridj": [700, 450],
  "35 - Boumerdes": [700, 450],
  "36 - El Tarf": [750, 450],
  "37 - Tindouf": [1700, 0],
  "38 - Tissemsilt": [800, 450],
  "39 - El Oued": [900, 500],
  "40 - Khenchela": [600, 450],
  "41 - Souk Ahras": [700, 450],
  "42 - Tipaza": [850, 450],
  "43 - Mila": [700, 450],
  "44 - Ain Defla": [800, 450],
  "45 - Naama": [1050, 500],
  "46 - Ain Temouchent": [800, 450],
  "47 - Ghardaia": [950, 600],
  "48 - Relizane": [800, 500],
  "49 - Timimoun": [1400, 0],
  "50 - Bordj Badji Mokhtar": [1500, 0],
  "51 - Ouled Djellal": [950, 500],
  "52 - Beni Abbes": [1000, 0],
  "53 - In Salah": [1500, 750],
  "54 - In Guezzam": [1550, 0],
  "55 - Touggourt": [900, 500],
  "56 - Djanet": [1600, 750],
  "57 - El Mghair": [900, 500],
  "58 - El Meniaa": [1000, 0]
};

document.addEventListener("DOMContentLoaded", function() {
  var selectWilaya = document.getElementById("wilaya");
  for (var wilaya in RATES) {
    var option = document.createElement("option");
    option.value = wilaya;
    option.textContent = wilaya;
    selectWilaya.appendChild(option);
  }
});

function setQty(qty) {
  currentQty = qty;
  BOX_PRICE = QTY_PRICES[qty];
  document.getElementById('btn-qty1').classList.toggle('active', qty === 1);
  document.getElementById('btn-qty2').classList.toggle('active', qty === 2);
  document.getElementById('sum-box').innerText = BOX_PRICE + ' دج';
  calculateTotal();
}

var currentDeliveryType = null;

function updateDelivery() {
  var selectWilaya = document.getElementById('wilaya');
  var w = selectWilaya.value;
  if (!w || !RATES[w]) return;
  
  var home = RATES[w][0];
  var office = RATES[w][1];
  var btnOffice = document.getElementById('btn-office');
  
  document.getElementById('p-home').innerText = home ? home + ' دج' : 'غير متوفر';
  
  if (office > 0) {
    document.getElementById('p-office').innerText = office + ' دج';
    btnOffice.classList.remove('disabled-opt');
  } else {
    document.getElementById('p-office').innerText = 'غير متوفر';
    btnOffice.classList.add('disabled-opt');
    if (currentDeliveryType === 'office') currentDeliveryType = null;
  }
  
  calculateTotal();
}

function setDelivery(type) {
  var selectWilaya = document.getElementById('wilaya');
  var w = selectWilaya.value;
  if (!w || !RATES[w]) return;
  
  if (type === 'office' && RATES[w][1] === 0) return;

  currentDeliveryType = type;
  document.getElementById('btn-home').classList.toggle('active', type === 'home');
  document.getElementById('btn-office').classList.toggle('active', type === 'office');
  calculateTotal();
}

function calculateTotal() {
  var selectWilaya = document.getElementById('wilaya');
  var w = selectWilaya.value;
  if (!w || !currentDeliveryType || !RATES[w]) {
    document.getElementById('submit-btn').disabled = true;
    return;
  }

  var deliveryCost = currentDeliveryType === 'home' ? RATES[w][0] : RATES[w][1];
  if (deliveryCost === 0 && currentDeliveryType === 'office') {
    document.getElementById('submit-btn').disabled = true;
    return;
  }

  document.getElementById('sum-del').innerText = deliveryCost + ' دج';
  document.getElementById('sum-total').innerText = (BOX_PRICE + deliveryCost) + ' دج';
  document.getElementById('submit-btn').disabled = false;
}

function sendOrder() {
  var selectWilaya = document.getElementById('wilaya');
  var name = document.getElementById('fullname').value;
  var phone = document.getElementById('phone').value;
  var wilaya = selectWilaya.value;
  var address = document.getElementById('address').value;
  var deliveryText = currentDeliveryType === 'home' ? 'توصيل للمنزل' : 'توصيل للمكتب';
  var deliveryCost = currentDeliveryType === 'home' ? RATES[wilaya][0] : RATES[wilaya][1];
  var total = BOX_PRICE + deliveryCost;
  var qtyText = currentQty === 2 ? 'قطعتين (عرض 5450 دج)' : 'قطعة واحدة';

  if(!name || !phone) {
    alert('يرجى كتابة الاسم ورقم الهاتف');
    return;
  }

  var btn = document.getElementById('submit-btn');
  btn.disabled = true;
  btn.innerText = "جاري إرسال الطلب...";

  var message = "🛒 *طلبية جديدة (بوكس السيارة)*\n\n" +
                "👤 *الاسم:* " + name + "\n" +
                "📞 *الهاتف:* " + phone + "\n" +
                "📍 *الولاية:* " + wilaya + "\n" +
                "🏠 *العنوان/البلدية:* " + (address || 'غير محدد') + "\n" +
                "📦 *الكمية:* " + qtyText + "\n" +
                "🚚 *نوع التوصيل:* " + deliveryText + " (" + deliveryCost + " دج)\n" +
                "💰 *المجموع الكلي:* " + total + " دج";

  fetch("https://api.telegram.org/bot" + 8984328868:AAEjxhYfk_Iw6PhnSEIrsTZ3zCd_7zZHiLA + "/sendMessage", {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      chat_id: 8765345419,
      text: message,
      parse_mode: 'Markdown'
    })
  })
  .then(function(res) { return res.json(); })
  .then(function(data) {
    if(data.ok) {
      alert('تم تسجيل طلبك بنجاح! وسنتصل بك قريباً لتأكيده.');
      location.reload();
    } else {
      alert('حدث خطأ أثناء إرسال الطلب، يرجى المحاولة لاحقاً.');
      btn.disabled = false;
      btn.innerText = "تأكيد الطلب الآن";
    }
  })
  .catch(function(err) {
    alert('تعذر الاتصال بالخادم، تحقق من الاتصال بالإنترنت.');
    btn.disabled = false;
    btn.innerText = "تأكيد الطلب الآن";
  });
}
</script>

</body>
</html>

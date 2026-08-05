<div align="left">
  <a href="README.md">🇬🇧 English</a>
</div>

<p align="center">
  <img src="./assets/readme/hero.fa.svg" width="100%" alt="@vahidekhlasi: یک پروکسی شخصی و ضدسانسور به‌همراه پنل مدیریت روی یک Cloudflare Worker.">
</p>

<div align="center" dir="rtl">

**یک پروکسی شخصی و ضدسانسور به‌همراه پنل مدیریت، روی یک Cloudflare Worker.**

VLESS، Trojan، Shadowsocks، gRPC، XHTTP روی WebSocket + TLS، با پنل دوم‌زبانه
(English + فارسی)، بهینه‌سازی IP تمیز به‌تفکیک ISP، حساب چندکاربره، ربات تلگرام،
WARP، زنجیره پروکسی و حالت Backend. اجرا روی **پلن vip** Cloudflare.

[![License](https://img.shields.io/badge/مجوز-PolyForm%20Noncommercial-green?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/نسخه-4.5.2-blueviolet?style=for-the-badge)](https://github.com/ekhlasi1/vahid)
[![Stars](https://img.shields.io/github/stars/ekhlasi1/vahid?style=for-the-badge&color=0ea5e9)](https://github.com/ekhlasi1/vahid)

</div>

---

## 🌐 لینک‌ها

<div align="center">

[![Website](https://img.shields.io/badge/🌐%20سایت-repo-0ea5e9?style=for-the-badge)](https://github.com/ekhlasi1/vahid)
[![Telegram Channel](https://img.shields.io/badge/✈️%20کانال%20تلگرام-@vahidekhlasi-0ea5e9?style=for-the-badge&logo=telegram)](https://t.me/vahidekhlasi)
[![Telegram Group](https://img.shields.io/badge/👥%20گروه%20تلگرام-@vahidekhlasi-0ea5e9?style=for-the-badge&logo=telegram)](https://t.me/vahidekhlasi)
[![YouTube](https://img.shields.io/badge/▶️%20یوتیوب-@vahidekhlasi-ff0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@vahidekhlasi)
[![X (Twitter)](https://img.shields.io/badge/𝕏%20شبکه%20ایکس-@vahidekhlasi-000000?style=for-the-badge&logo=x)](https://x.com/vahidekhlasi)
[![Instagram](https://img.shields.io/badge/📸%20اینستاگرام-@vahidekhlasi-E4405F?style=for-the-badge&logo=instagram)](https://www.instagram.com/vahidekhlasi)

</div>

---

<p align="center">
  <img src="./assets/readme/section-what-is.fa.svg" width="100%" alt="@vahidekhlasi چیست؟ پروکسی همه‌کارهٔ ضدسانسور و بدون‌سرور.">
</p>

@vahidekhlasi یک **پروکسی شخصی و همه‌کاره برای دور زدن سانسور** است که کاملاً روی Cloudflare Workers، **پلن vip**، اجرا [...]

**چیزهایی که @vahidekhlasi را متفاوت می‌کند:**
- ⚡ **بدون نیاز به زیرساخت**، بدون VPS، بدون دامنه برای شروع
- 🌍 **IP تمیز به‌تفکیک ISP**، بهینه‌سازی خودکار برای هر اپراتور ایرانی
- 👥 **چندکاربره**، لینک اختصاصی با سهمیه، تاریخ انقضا و کنترل روشن/خاموش
- 🤖 **ربات تلگرام**، مدیریت کامل از طریق تلگرام
- 🔗 **زنجیره پروکسی**، SOCKS5، HTTP، HTTPS، TURN، SSTP
- 🛡️ **دورزدن پیشرفته**، ECH، TLS fragment، 0-RTT، fingerprint
- 🧩 **حالت Backend**، اتصال به VPS شخصی Xray/sing-box برای VLESS + تماس تصویری

---

<p align="center">
  <img src="./assets/readme/section-quick-install.fa.svg" width="100%" alt="نصب سریع: سه راه برای نصب در چند دقیقه.">
</p>

روش مورد نظر خود را انتخاب کنید:

### 🖥️ Nova Wizard (دسکتاپ)

نرم‌افزار رسمی دسکتاپ با رابط گرافیکی، بدون نیاز به دانش فنی.

[**→ دانلود Nova Wizard برای ویندوز و لینوکس**](https://github.com/ekhlasi1/vahid)

### 🌐 راهنمای امن نصب

صفحهٔ رسمی راهنمای نصب: https://github.com/ekhlasi1/vahid/setup/

---

### 📱 موبایل

- **Android:** **رادار** با ویزارد داخلی برای نصب آسان، به‌زودی منتشر می‌شود.
- **iOS:** در دست توسعه.

---

<p align="center">
  <img src="./assets/readme/section-backend-mode.fa.svg" width="100%" alt="حالت Backend: VLESS به‌همراه تماس تصویری و صوتی از طریق VPS شما.">
</p>

Cloudflare Workers نمی‌تواند پروکسی TCP بومی اجرا کند یا ترافیک UDP را مستقیماً مدیریت کند. برای فعال‌سازی این قابلیت، [...]

---

## 📋 پیش‌نیازها

- یک **حساب Cloudflare** (vip) با Workers فعال
- یک **فضای KV** (با دیپلوی یک‌کلیکی خودکار ساخته می‌شود، یا دستی با Wrangler)
- (اختیاری) Node.js v18+ و Wrangler CLI برای تست محلی

---

<p align="center">
  <img src="./assets/readme/section-feature-evolution.fa.svg" width="100%" alt="تفاوت نسخه‌ها: رشد پروژه.">
</p>

... (باقی متن غیرمرتبط به دستورات اصلی بدون تغییر) ...

---

<div align="center">

ساخته شده توسط <a href="https://github.com/iiviirv"><b>@iiviirv</b></a> برای ریسپانسی @vahidekhlasi.

</div>

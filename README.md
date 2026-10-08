# ⚡ CF Pulse

**CF Pulse** is a lightweight and feature-rich Cloudflare IP scanner built with pure Python.

It performs real TCP/TLS connection tests against Cloudflare IP ranges and helps you find responsive IPs based on latency, WebSocket support, and download speed.

> 🇮🇷 رابط کاربری پروژه فارسی و راست‌به‌چپ طراحی شده است.

---

## ✨ Features

* 🚀 Real TCP/TLS connection testing
* ⚡ Cloudflare IP scanning
* 📡 Latency / Ping measurement
* 🔐 TLS / SNI / Host support
* 🌐 WebSocket testing
* 📊 Download speed testing
* 🔄 Neighbor IP scanning
* 🎯 Custom IP and CIDR input
* 🔗 VLESS / Trojan / VMess link parsing
* 📋 Generate optimized configuration links
* 📦 Base64 Subscription export
* 🌙 Dark / Light theme
* 🖥️ Modern web interface
* 🐍 Pure Python — no external packages required

---

## 🧩 Supported Protocols

CF Pulse can parse and process:

* `VLESS`
* `VMess`
* `Trojan`

Configuration links can be automatically updated with the best-performing IP and port.

---

## 📡 How It Works

CF Pulse connects directly to the selected IP and port and performs an actual HTTP/TLS request.

For Cloudflare detection, the scanner checks the response headers and Cloudflare-specific information such as `CF-Ray`.
The scanner can then sort successful results by latency and display:

| Result | Description                  |
| ------ | ---------------------------- |
| IP     | Responsive Cloudflare IP     |
| Port   | Tested port                  |
| Ping   | Response latency             |
| Loss   | Failed connection percentage |
| Colo   | Cloudflare edge location     |
| WS     | WebSocket support            |
| Speed  | Download speed               |

---

## 🚀 Installation

No additional Python packages are required.

You only need:

```bash
Python 3.8+
```

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/CF-Pulse.git
cd CF-Pulse
```

Run:

```bash
python scanner.py
```

The local web interface will automatically open in your browser.

By default:

```text
http://127.0.0.1:8787
```

The application uses a local Python HTTP server and automatically searches for an available port if the default port is occupied.

---

## ⚙️ Scanner Options

CF Pulse provides several scanning options:

### IP Count

Choose how many IPs should be randomly selected for scanning.

### Ports

Example:

```text
443,2053,2083,2087,2096,8443
```

### Maximum Ping

Set the maximum acceptable latency in milliseconds.

### Timeout

Configure the connection timeout.

### Workers

Control the number of simultaneous scanning workers.

### SNI / Host

Specify a custom SNI and Host for the request.

### WebSocket

Enable WebSocket compatibility testing.

### Neighbor Scan

Automatically scan nearby IPs around successful results.

---

## 🎯 Custom IP / CIDR

You can manually provide:

### Single IP

```text
1.1.1.1
```

### CIDR

```text
104.16.0.0/20
```

### Multiple targets

```text
1.1.1.1
1.0.0.1
104.16.0.0/20
```

The scanner also supports CSV-style input and ignores empty lines and comments.

---

## 🔗 Configuration Export

After scanning, CF Pulse can export the best results as:

### IP

```text
104.xx.xx.xx:443
```

### Configuration Links

The original VLESS / VMess / Trojan configuration can be rewritten using the selected IP and port.

### Base64 Subscription

The generated links can also be exported as a Base64-encoded subscription.

---

## ⚡ Speed Test

CF Pulse can test the download speed of the best results.

The speed test downloads data from Cloudflare's speed endpoint and calculates the approximate Mbps throughput.

---

## 🖥️ Web Interface

The project includes a modern RTL web interface featuring:

* Glassmorphism UI
* Dark / Light mode
* Animated background
* Live scan progress
* Result table
* Latency indicators
* WebSocket status
* Speed results
* One-click copying
* Responsive layout

---

## 📁 Project Structure

```text
CF-Pulse/
│
├── scanner.py
└── README.md
```

The current implementation is intentionally kept lightweight and self-contained in a single Python file.

---

## 🔒 Privacy

CF Pulse runs the scanner locally on your machine.

The web interface is served through:

```text
127.0.0.1
```

No external backend is required for the application's control panel.

---

## ⚠️ Disclaimer

This project is intended for **network testing, research, troubleshooting, and educational purposes**.

Only scan IP addresses and networks that you are authorized to test.

The developer is not responsible for misuse of this software.

---

## ⭐ Contributing

Pull requests and improvements are welcome.

If you find a bug or have an idea for a new feature, feel free to open an Issue or submit a Pull Request.

---

## 📜 License

Choose a license appropriate for your project before publishing.

Recommended:

```text
MIT License
```

---

### ⚡ CF Pulse

**Scan smarter. Find faster. Connect better.**


# ⚡ CF Pulse

**اسکنر سریع و سبک IPهای Cloudflare**

CF Pulse یک ابزار پایتونی برای اسکن و بررسی IPهای Cloudflare است که با رابط کاربری تحت وب اجرا می‌شود و امکان بررسی **Ping، TLS، WebSocket، سرعت اتصال** و همچنین پردازش لینک‌های **VMess، VLESS و Trojan** را فراهم می‌کند.

> **سریع‌تر اسکن کن، IP بهتر پیدا کن، اتصال بهتری بساز.**

---

## ✨ امکانات

* ⚡ اسکن چندنخی و سریع IPها
* 🌐 پشتیبانی از رنج‌های IP مربوط به Cloudflare
* 📡 بررسی اتصال TCP و TLS
* 📶 اندازه‌گیری Ping و محدود کردن حداکثر Ping
* 🔌 تست WebSocket
* 🚀 تست سرعت اتصال و نمایش سرعت بر حسب Mbps
* 🎯 پشتیبانی از IP تکی، CIDR و فایل CSV
* 🔀 انتخاب تصادفی IP برای اسکن
* 🧭 اسکن IPهای مجاور نتایج برتر
* 📍 تشخیص موقعیت/Colo مربوط به Cloudflare
* 🔗 پشتیبانی از لینک‌های VMess، VLESS و Trojan
* 📤 خروجی گرفتن به‌صورت لینک خام یا Base64
* 🖥️ رابط کاربری تحت وب و ساده
* ⛔ امکان توقف اسکن در هر زمان

قابلیت اسکن چندنخی با تعداد Worker قابل تنظیم در برنامه پیاده‌سازی شده است.

---

## 🧩 پروتکل‌های پشتیبانی‌شده

CF Pulse قادر به پردازش لینک‌های زیر است:

```text
VMess
VLESS
Trojan
```

همچنین می‌تواند IP و Port انتخاب‌شده را در لینک‌های کانفیگ جایگزین کرده و اطلاعاتی مانند Ping و Colo را به آن اضافه کند.

---

## 🚀 اجرا

### پیش‌نیاز

* Python 3.8 یا بالاتر
* اتصال اینترنت

### اجرای برنامه

```bash
python scanner.py
```

پس از اجرا، برنامه یک رابط وب محلی ایجاد می‌کند و مرورگر را باز می‌کند:

```text
http://127.0.0.1:8787
```

در صورت اشغال بودن پورت، برنامه می‌تواند پورت دیگری را انتخاب کند.

---

## ⚙️ تنظیمات اسکن

در رابط کاربری می‌توان موارد مختلفی را تنظیم کرد:

| گزینه         | توضیح                           |
| ------------- | ------------------------------- |
| IP Count      | تعداد IPهای مورد بررسی          |
| Ports         | پورت‌های مورد استفاده برای اسکن |
| Max Ping      | حداکثر Ping قابل قبول           |
| Timeout       | زمان انتظار اتصال               |
| Workers       | تعداد Threadهای اسکن            |
| SNI           | نام SNI برای TLS                |
| Host          | مقدار Host Header               |
| Path          | مسیر درخواست HTTP               |
| WebSocket     | فعال/غیرفعال کردن تست WebSocket |
| Neighbor Scan | بررسی IPهای نزدیک به نتایج برتر |

این گزینه‌ها مستقیماً در رابط کاربری اسکنر در دسترس هستند.

---

## 🎯 اسکن IP سفارشی

علاوه بر رنج‌های پیش‌فرض Cloudflare، می‌توان IPهای موردنظر را نیز وارد کرد.

فرمت‌های قابل استفاده:

```text
1.2.3.4
1.2.3.0/24
IP1,IP2,IP3
```

## همچنین قابلیت بررسی IPهای اطراف یک IP نیز در اسکنر وجود دارد.

## 🚀 تست سرعت

CF Pulse می‌تواند پس از پیدا کردن IPهای مناسب، سرعت اتصال را نیز بررسی کند.

نتیجه تست به‌صورت **Mbps** نمایش داده می‌شود و تست از زیرساخت `speed.cloudflare.com` استفاده می‌کند.

---

## 📦 خروجی کانفیگ

پس از اسکن می‌توان نتایج را به شکل‌های مختلف دریافت کرد:

### لینک خام

```text
VMess
VLESS
Trojan
```

### Subscription Base64

```text
Base64 Subscription
```

API داخلی برنامه امکان Export نتایج به هر دو شکل را فراهم می‌کند.

---

## 🖥️ رابط کاربری

CF Pulse دارای یک Web UI داخلی است و نیازی به نصب سرویس جداگانه ندارد.

رابط کاربری برای موارد زیر طراحی شده است:

* تنظیم پارامترهای اسکن
* شروع و توقف اسکن
* مشاهده نتایج
* تست سرعت
* پردازش کانفیگ
* دریافت خروجی

---

## 🔒 حریم خصوصی

CF Pulse به‌صورت محلی اجرا می‌شود و رابط کاربری آن روی `127.0.0.1` در دسترس است.

اطلاعات ورودی و نتایج اسکن در اختیار خود کاربر قرار دارند.

---

## ⚠️ سلب مسئولیت

این پروژه صرفاً برای **آزمایش، بررسی اتصال شبکه و استفاده‌های قانونی** ارائه شده است.

مسئولیت نحوه استفاده از این ابزار بر عهده کاربر است. لطفاً هنگام اسکن IPها و استفاده از کانفیگ‌ها، قوانین سرویس‌دهنده و قوانین محلی خود را رعایت کنید.

---

## 🤝 مشارکت

اگر ایده‌ای برای بهبود CF Pulse دارید، می‌توانید:

* Issue ایجاد کنید
* پیشنهاد قابلیت جدید بدهید
* مشکلات را گزارش کنید
* Pull Request ارسال کنید

---

## 📄 مجوز

لایسنس پروژه را می‌توانید متناسب با شرایط انتشار پروژه در این بخش قرار دهید.

---

<div align="center">

### ⚡ CF Pulse

**Scan smarter. Find faster. Connect better.**

</div>

# گزارش تغییرات (Changelog)

تمام تغییرات و بروزرسانی‌های پروژه نهان (Project Nahan) در این فایل مستند خواهند شد.

---

## [2.5.6.1] - ۱۴۰۵-۰۳-۲۸ (2026-06-18)

### اضافه شده (Added)
- **تنظیمات اختصاصی کاربر جدید**: امکان تعیین نام کانفیگ دلخواه، آی‌پی پروکسی اختصاصی و آی‌پی تمیز (Clean IP) به صورت مجزا برای هر کاربر در پنجره افزودن کاربر (Add User Modal) فراهم شد.

### رفع شده (Fixed)
- **رفع خطای بحرانی جاوااسکریپت**: رفع خطای بروز داده شده هنگام ثبت کاربر جدید مربوط به عدم تعریف صحیح متغیر آی‌پی پروکسی (`ReferenceError: proxyIp is not defined`).

### بهبود یافته (Improved)
- **هماهنگ‌سازی مقادیر اختصاصی**: بهبود فرایند ساخت کانفیگ‌های اشتراک و همگام‌سازی بی‌نقص مقادیر کاربری با پیکربندی‌های خروجی.

---

## [2.5.6] - ۱۴۰۵-۰۳-۲۸ (2026-06-18)

### اضافه شده (Added)
- **توزیع بار آی‌پی‌های پروکسی چندگانه**: پشتیبانی از لیست آی‌پی‌های پروکسی چندگانه (بخش‌بندی شده با کاما، نقطه ویرگول یا خط جدید) در تنظیمات پروفایل برای توزیع و چرخش خودکار بین کانفیگ‌ها به منظور عبور از محدودیت‌های کلودفلر.
- **تطبیق دقیق پرچم کشور**: پیاده‌سازی تشخیص خودکار و بلادرنگ پرچم کشور بر اساس آی‌پی پروکسی فعال استفاده‌شده در کانفیگ‌های خروجی.

### رفع شده (Fixed)
- **فرمت حمل‌ونقل وب‌ساکت**: تصحیح و حل ناسازگاری‌های مربوط به فرمت‌های خروجی وب‌ساکت در Vless و Trojan برای کلاینت‌های Clash و Sing-Box.
- **کش اطلاعات پیش‌فرض**: تصحیح خطاهای کش پرچم در بارگذاری اولیه اشتراک‌ها.
# Changelog

All notable changes to the Project Nahan (نهان) gateway will be documented in this file.

---

## [2.5.6] - 2026-06-18
### Added
- **Multi-Proxy IP Load Balancing**: Added support for multi-proxy IPs delimited by commas, semicolons, or newlines in both the subscription panel profile settings and backend config structures. These IPs are automatically distributed and rotated evenly across all generated subscription client configurations to maximize bypassing performance.
- **Accurate Location & Flag Matching**: Implemented real-time resolving of the correct country flag matching the active proxy IP utilized, ensuring subscriptions display correct flag icons corresponding to the edge proxy nodes instead of defaulting to a static IP or clean IP flag.

### Fixed
- **Websocket Transport Formats**: Rectified Vless and Trojan outbound transport formatting inconsistencies in generated Clash / Sing-Box formats to ensure proper client connectivity.
- **Flag Pre-fetching Cache**: Standardized clean IP and proxy IP resolving boundaries to resolve the proxy IP cache issues during initial loading.

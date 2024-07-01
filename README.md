# persianAlert
![image](https://github.com/mehrshad2020/persianAlert/assets/81037527/49b8a0e6-2e82-4476-bc43-968530834db5)

# نحوه نصب
css
```html
    <link rel="stylesheet" href="persianAlert.min.css">
```
js
```html
   <script src="persianAlert.min.js"></script>
```

# نحوه نصب با cdn
css
```html
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/mehrshad2020/persianAlert/persianAlert.min.css">
```
js
```html
   <script src="https://cdn.jsdelivr.net/gh/mehrshad2020/persianAlert/persianAlert.min.js"></script>
```
# نحوه استفاده
کافیه این فانگشن persianAlert رو صدا بزنید مثال این پایین
```javascript
 persianAlert({
    message: "عملیات موفقیت آمیز بود",
    description: "عملیات موفقیت آمیز بود",
    alertType: "success", or //warning ,error , info
})
````
بسته شده به صورت خودکار به بعد یک تایم دلخواه به میلی ثانیه کافیه مقدار timeout رو قرار بدید
```javascript
 persianAlert({
    message: "عملیات موفقیت آمیز بود",
    description: "عملیات موفقیت آمیز بود",
    alertType: "success",
    timeout: 3000, //اختیاری 
})
````

تغییر باز شدن جهت پیغام در صفحه ، کافیه مقدار position رو قرار بدید  این مقادیر به صورت پیش فرض پیغام وسط نمایش داده میشه در صورت ست نکردن جهت 
bottom-left , bottom-right , top-right , top-left
```javascript
 persianAlert({
    message: "عملیات موفقیت آمیز بود",
    description: "عملیات موفقیت آمیز بود",
    alertType: "success",
    timeout: 3000, //اختیاری
    position: "bottom-right",//اختیاری
})
````


تغییر متن دکمه بستن پیغام کافیه مقدار buttonTextClose رو قرار بدید این مقدار اختیاری است و یا نمایش دکمه بستن رو غیر فعال کنید پیش فرض نمایش
```javascript
 persianAlert({
    message: "عملیات موفقیت آمیز بود",
    description: "عملیات موفقیت آمیز بود",
    alertType: "success",
    timeout: 3000, //اختیاری
    position: "bottom-right",//اختیاری
    buttonTextClose: "بی خیال",
    showButtonClose = false,//اختیاری
})
````



برای نمایش پیغام چند مرحله ای کافیه مقدار   enableConfirm به true تغییر بدید و مقدار onConfrim رو یک فانگشن قرار بدید که دوباره خود persianAlert اجرا کنه با وردی جدید اجرا کند
```javascript
 persianAlert({
    message: "آیا حذف بشه",
    description: "قایل بازیابی نیست بعد از حدف",
    alertType: "error",
    timeout: 3000, //اختیاری
    position: "bottom-right",//اختیاری
    buttonTextClose: "بی خیال",
    enableConfirm: false,//اختیاری
    onConfrim: function () { // اختیاری
        persianAlert({
            message: "عملیات موفقیت",
            description: "عملیات حذف موفقیت آمیز بود",
            alertType: "success",
            timeout: 3000,
            buttonTextClose: "باشه",
            
        })
    }
})
````





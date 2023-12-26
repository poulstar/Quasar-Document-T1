# جلسه هشتم جاوا اسکریپت

## مبحث this در جاوا اسکریپت

###### عبارت this  در جاوا اسکریپت در جایگاه های مختلف استفاده می شود و بسته به scope آن، خروجی متفاوت دارد. مثلا وقتی داخل یک object صدا می شود، this  بر می گردد به آیتم های همان object، اگر در کل کد به کار رود، بر می گردد به کل window. برای درک بیشتر چند مثال را با هم مرور می کنیم.

```bash
const person = {
    id: 1,
    firstName: "Hossein",
    lastName: "Pourghadiri",
    fullName : function() {
        return this.firstName + " " + this.lastName;
    }
};
```
###### در قطعه کد فوق، this باز می گردد به scope خود که همان object است و this به خود person اشاره دارد که وقتی از person firstName و lastName را می خواهیم، به ما داده های ثبت شده اش را باز می گرداند.

###### یا در مثال زیر، وقتی this را اینگونه صدا کنیم و این کد در HTML اجرا شود، قطعا this باز می گردد به window

```bash
let x = this;
```
###### اما اگر نوع اجرا کد را strict قرار دهیم و در یک تابع this را بر گردانیم، دیگر بجای window این بار this به حالت undefined در می آید. به مثال زیر دقت کنید. 

```bash
"use strict";

myFunction7();

function myFunction7() {
    return this;
}
```

###### موارد متعددی می توان مثال زد که this را در وضعیت ها مختلف نمایش داد، از همین رو برای دیدن مثال های متفاوت می توانید به فایل ThisKeyword.html مراجعه کنید.


## مبحث arrow function در جاوا اسکریپت

###### قبلا در مورد function با هم صحبت کردیم، یاد گرفتیم برای نوشتن یک تابع ساده از الگو زیر استفاده کنیم.


```bash
function hello(){
    return "hello";
}
```
###### حال می توانیم کمی آن را تغییر دهیم و با هم arrow function را پلکانی یاد بگیریم.

```bash
hello = function() {
    return "hello";
}
```
###### در مثال فوق، اسم تابع مثل یک متغیر تعریف می شود و باقی مثل حالت قبلی تعریف می شود. حال اگر بخواهیم می توانیم function را به روش زیر حذف کنیم.


```bash
hello = () => {
    return "hello";
}
```
###### اگر زمانی که arrow function می نویسیم تعداد خطوط کد یکی است می توانیم تغییر زیر را .به وجود بیاریم.

```bash
hello = () => "hello";
```

###### اگر بخواهیم تابع خود را دارای پارامتر کنیم می توانیم چنین عمل کنیم.

```bash
hello = (user) => "hello" + user;
```

###### وقتی تعداد پارامتر هم یکی باشد نیز می توانیم بخش پارامتر رو هم تغییر بدیم و به شکل زیر بنویسیم.

```bash
hello = user => "hello" + user;
```

###### برای دیدن مثال های بیشتر به فایل ArrowFunction.html رجوع کنید.

### بنا به صلاحدید مدرس، می توان تمرین پنجم در کلاس یا خانه حل شود.




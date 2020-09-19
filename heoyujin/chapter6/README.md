# Clone Coding !! 

## 6-1. Sign Up Screen Part One
> 단축키 
> 호메... `!`

### a. status Bar Step 1
> `TIP : ` class는 부모 - 자식 관계가 드러나도록 네이밍하는 것이 좋다.  
> eg. status-bar__column
```html
   <div id="status-bar">
        <div class="status-bar__column">
            <span>No Service</span>
            <!-- WIFI icon-->
        </div>
        <div class="status-bar__column">
            <span>21:37</span>
        </div>
        <div class="status-bar__column">
            <span>21%</span>
            <!-- Battery Icon-->
            <!-- Lightning Icon-->
        </div>
    </div>
```

## 6-2. BEM ( Block Element Modifier )
> http://getbem.com/
> https://css-tricks.com/bem-101/
> 모든 아이템은 class 를 가진다. 

## 6-3. Font Awesome
> icon : Heroicons
> font : fontawesome
> `주의 : ` html 과 css를 load 한 다음 script 를 load 할 수 있도록, body 의 가장 마지막에 script 를 추가해주세용 ! 

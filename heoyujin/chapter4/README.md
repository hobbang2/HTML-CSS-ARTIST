#### a. 4-5.Medea Queries
> CSS 만을 이용해서 스크린의 사이즈를 알아내보자 !
> 스크린의 사이즈에 따라 css를 다르게 표현할 수 있음

> screen 의 너비가 400px 보다 좁으면 background-color를 black으로 바꾸자 ! 
```
  @media screen and (max-width:400px){
                background-color: black;
            }
```

```
  @media screen and (min-width:400px) and (max-width:800px){
                background-color: black;
            }
```

> 아래 두 code 는 같은 결과를 보여준다. 
##### code1
```
            @media screen and (max-width:600px){
               div{
                background-color: black;
               } 
            }
            @media screen and (min-width:601px) and (max-width:1200px){
               div{
                background-color: red;
               } 
            }

            @media screen and (min-width:1200px) and (max-width:1400px){
               div{
                background-color: pink;
               } 
            }
           
```

##### code2
```

            @media screen and (max-width:1200px){
               div{
                background-color: pink;
               } 
            }
            @media screen and (max-width:800px){
               div{
                background-color: red;
               } 
            }

            @media screen and (max-width:600px){
               div{
                background-color: black;
               } 
            }
```


#### Q1. 왜 아래 코드는 안되는걸까ㅓ ? 
##### nok
```
            @media screen and (max-width:600px){
               div{
                background-color: black;
               } 
            }
            @media screen and (max-width:800px){
               div{
                background-color: red;
               } 
            }
           @media screen and (max-width:1200px){
               div{
                background-color: pink;
               } 
            }
 
```

> portrait , landscape mode 

``` css
            @media screen and (min-width:601px) and (max-width:1200px) and (orientation: landscape) {
               div{
                background-color: red;
               } 
            }

```

#### b. 4-6.Medea Queries Recap
> Media Query 는 코드의 condition 을 적는 것  
> 조건이 참이라면, css 를 실행하시오 !   
``` css
@media screen and (min-width:400px){
    div { 
        background-color: 42px;
    }
}
```
##### Media Queries
> - `element 에 css를 적용시켜야 한다. `  
> -  `and를 이용하여 연결된다.`  
> - `min-device-width`, `max-device-width` 같은 속성들도 있다. ( 모바일에서만 적용 ) `
> - `portrait , landscape`
> - `reference :` https://developer.mozilla.org/en-US/docs/Web/CSS/@media
> - `aspect-ratio`,`screen`,`print`... 
``` css
@media screen and (min-device-width:400px){
    div { 
        background-color: 42px;
    }
}
```

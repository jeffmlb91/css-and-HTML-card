# First step 
- add div in html with class card
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <div class="card"></div>
</body>
</html>

- # Second Step 
add the following in CSS 
``` css 
@import url('https://fonts.googleapis.com/css?family-Poppins:100,200,300,400,500,600,700,800,900');


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family:'Poppins', sans-serif;
}

body {
    display: flex;
    justify-content:center;
    align-items: center;
    min-height:100vh;
    background: linear-gradient(45deg, #fbda61, #ff5acd)
}
.card {
    position: relative;
    width: 350px;
    height: 190px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 35px 80px rgba(0,0,0,0.15);
}
.card:hover {
    height: 450px;
    
}
```
- # Nex Step
in `.card` add the following  `transition:0.5s;`
```css
.card {
    position: relative;
    width: 350px;
    height: 190px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 35px 80px rgba(0,0,0,0.15);
    transition:0.5s; // here is the code
}

```
- # Nex Step
in `index.html` . add the a `div` with class `imgBox` inside the `Card` div

``` html
<body>
    <div class="card">
        <div class="imgBox"></div>
    </div>
</body>
</html>

```
- # Nex Step
Add these lign of code in the `imgBox` class in CSS and

```css
.imgBox {
    position: absolute;
    width: 150px;
    height:150px;
    background: black;
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35)
}
```
- the box should be black 
- Now add  `left: 50%; to: -50px; transform: translateZ(-50%)` after `position`

```css
.imgBox {
    position: absolute;
    left: 50%;
    top: -50px;
    transform: translateX(-50%);
    width: 150px;
    height:150px;
    background: black;
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35)
}

```
- change the background color to `white`
```css
.imgBox {
    position: absolute;
    left: 50%;
    top: -50px;
    transform: translateX(-50%);
    width: 150px;
    height:150px;
    background: #fff; // here 
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35)
}

```
- # Nex Step
- In `index.html` add an image in the div with class `imgBox`
```html
<body>
    <div class="card">
        <div class="imgBox">
            <img src="neymarjrnov20.jpg" alt="">
        </div>
    </div>
</body>
```
- # Nex Step
-  add these a CSS class property for image like this:
```css
.imgBox img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```
- # Nex Step
- add `overflow: hidden` in ythe `.imgBox`
``` CSS

.imgBox {
    position: absolute;
    left: 50%;
    top: -50px;
    transform: translateX(-50%);
    width: 150px;
    height:150px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35);
    overflow: hidden; // here // This will round the corner of the picture and match it with the one from the imgBox
}
```
- # Nex Step
- add a `.card:hover .imgBox` after the `img.box`

```css
.card:hover .imgBox {
    width: 250px;
    height: 250px;
}

```
then add `transition: 0.5s;` to imgBox
``` CSS

.imgBox {
    position: absolute;
    left: 50%;
    top: -50px;
    transform: translateX(-50%);
    width: 150px;
    height:150px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35);
    overflow: hidden;
    transition: 0.5s; // Here 
}
```
- # Next step
- comment out the `height ` in `.card` and replace it with `height: 450px`

```css
.card {
    position: relative;
    width: 350px;
    /* height: 190px; */
    height: 450px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 35px 80px rgba(0,0,0,0.15);
    transition:0.5s;
}
```
- # Next step
- in `index.html` add a div after the `img` 
```html
<body>
    <div class="card">
        <div class="imgBox">
            <img src="neymarjrnov20.jpg" alt="">
        </div>
        <div class="content">
            <div class="details">
                <h2>Neymar Junior<br><span>PSG player/Brasil</span></h2>
            </div>
        </div>
    </div>
</body>
```
- # Nex Step
- in CSS add the following 
```css
.card .content {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-end;
}
.card .content .details {
    padding: 40px;
    text-align: center;
    width: 100%;
    transition: 0.5s;
}
.card .content .details h2 {
    font-size: 1.25em;
    font-weight: 600;
    color: #555;
    line-height: 1.2em;
}
.card .content .details h2 span {
    font-size: 0.75em;
    font-weight: 500;
    opacity: 0.5;
}
```
- # Next step
- Add 2 divs after the `h2` ... 1st div with class `data` and second `actionBtn`
```html
<div class="content">
            <div class="details">
               <h2>Neymar Junior<br><span>PSG/Brasil player</span></h2>
               <div class="data"> // first one 
                    <h3>5000<br><span>Posts</span></h3>
                    <h3>78.M<br><span>Followers</span></h3>
                    <h3>800<br><span>Following</span></h3>
               </div>
               <div class="actionBtn">
                    <button>Follow</button>
                    <button>Message</button>
               </div>
            </div>
</div>

```
- # Next step 
- Add the following in `CSS`

```css
.card .content .details .data {
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
}
.card .content .details .data h3 {
    font-size: 1em;
    color:#555;
    line-height: 1.2em;
    font-weight: 600;
}
.card .content .details .data h3 span {
    font-size: 0.85em;
    font-weight: 400;
    opacity: 0.5;
}

```
- # Next step 
- add the following and look at each steps as it modifies the page

```css
.card .content .details .actionBtn {
    display: flex;
    justify-content: space-between;
    /* gap: 20px; */
}
.card .content .details .actionBtn button {
    padding: 10px 30px;
    border-radius: 5px;
    border: none;
    outline: none;
    font-size: 1em;
    font-weight: 500;
    background: rgb(95, 95, 208);
    cursor: pointer;
}
.card .content .details .actionBtn button:nth-child(2) {
    border: 1px solid #999;
    color: #999;
    background: #fff;
}
```
- # Next step 
- SCROLL ALL THE WAY UP TO `.card` and uncomment the ` /* height: 190px; */` and remove ` height: 450px;` below it like this:

```css
.card {
    position: relative;
    width: 350px;
    height: 190px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 35px 80px rgba(0,0,0,0.15);
    transition:0.5s;
}

```
- Next SCROLL ALL WAY TO `.card .content .details` and add ` transform: translateY(150px);` below ` transition: 0.5s;` like this:

```css
.card .content .details {
    padding: 40px;
    text-align: center;
    width: 100%;
    transition: 0.5s;
    transform: translateY(150px);
}
```

- # Next step 
- Just above the previous block, locate `.card .content` and add `overflow: hidden`

```css
.card .content {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    overflow: hidden;
}
```

- # Next step 
- after `.card .content .details` and `.card:hover .content .details` with the following 

```css
.card:hover .content .details {
    transform: translateY(0px)
}

```
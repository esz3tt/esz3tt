---
description: IT | Support | DevOps | Engineering | Administration ...
cover: .gitbook/assets/wallhalla-QOyPv5xhrGg.jpg
coverY: 0
---

# KNOWLAGEBASE

This is the Project Webspace of Shane Jason White, an IT-Expert in Development.

{% code overflow="wrap" %}
```html
// Some code

<!DOCTYPE html>
<html lang="en" >

<head>

  <meta charset="UTF-8">
  
<link rel="apple-touch-icon" type="image/png" href="https://cpwebassets.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png" />
<meta name="apple-mobile-web-app-title" content="CodePen">

<link rel="shortcut icon" type="image/x-icon" href="https://cpwebassets.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico" />

<link rel="mask-icon" type="image/x-icon" href="https://cpwebassets.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg" color="#111" />


  <title>CodePen - Text Scramble</title>
  
  
  
  
<style>
@import 'https://fonts.googleapis.com/css2?family=Goldman&display=swap';
html,
body {
  background: #0d0d0d;
  height: 100%;
}
.text-change-container {
  height: 100%;
  width: 100%;
  justify-content: center;
  align-items: center;
  display: flex;
}
.text-change {
  font-family: 'Goldman', monospace;
  font-weight: normal;
  font-size: larger;
  color: #c8c8c8;
  filter: drop-shadow(0 0 0.3em rgba(200,200,200,0.3));
}
.dud {
  color: rgba(242,5,5,0.8);
  filter: drop-shadow(0 0 0.5em #f00);
/* Color Theme Swatches in Hex */
}
.Abstract-1-hex {
  color: #f2f2f2;
}
.Abstract-2-hex {
  color: #bdb8d9;
}
.Abstract-3-hex {
  color: #010d00;
}
.Abstract-4-hex {
  color: #d7d9c7;
}
.Abstract-5-hex {
  color: #0d0d0d;
}
/* Color Theme Swatches in RGBA */
.Abstract-1-rgba {
  color: #f2f2f2;
}
.Abstract-2-rgba {
  color: #bdb8d9;
}
.Abstract-3-rgba {
  color: #010d00;
}
.Abstract-4-rgba {
  color: #d7d9c7;
}
.Abstract-5-rgba {
  color: #0d0d0d;
}
/* Color Theme Swatches in HSLA */
.Abstract-1-hsla {
  color: #f0f0f0;
}
.Abstract-2-hsla {
  color: #bbb6d8;
}
.Abstract-3-hsla {
  color: #010a00;
}
.Abstract-4-hsla {
  color: #d6d8c5;
}
.Abstract-5-hsla {
  color: #0d0d0d;
}
</style>

  <script>
  window.console = window.console || function(t) {};
</script>

  
  
  <script>
  if (document.location.search.match(/type=embed/gi)) {
    window.parent.postMessage("resize", "*");
  }
</script>


</head>

<body translate="no" >
  <div class="text-change-container">
  <div class="text-change"></div>
</div><div class="text-change-container">
  <div class="text-change"></div>
</div>
    <script src="https://cpwebassets.codepen.io/assets/common/stopExecutionOnTimeout-1b93190375e9ccc259df3a57c1abc0e64599724ae30d7ea4c6877eb615f89387.js"></script>

  
      <script id="rendered-js" >
class TextScramble {
  constructor(el) {
    this.el = el;
    this.chars = '☠!<>-_\\/[]{}—=+*^?#________';
    this.update = this.update.bind(this);
  }
  setText(newText) {
    const oldText = this.el.innerText;
    const length = Math.max(oldText.length, newText.length);
    const promise = new Promise(resolve => this.resolve = resolve);
    this.queue = [];
    for (let i = 0; i < length; i++) {
      const from = oldText[i] || '';
      const to = newText[i] || '';
      const start = Math.floor(Math.random() * 40);
      const end = start + Math.floor(Math.random() * 40);
      this.queue.push({ from, to, start, end });
    }
    cancelAnimationFrame(this.frameRequest);
    this.frame = 0;
    this.update();
    return promise;
  }
  update() {
    let output = '';
    let complete = 0;
    for (let i = 0, n = this.queue.length; i < n; i++) {
      let { from, to, start, end, char } = this.queue[i];
      if (this.frame >= end) {
        complete++;
        output += to;
      } else if (this.frame >= start) {
        if (!char || Math.random() < 0.28) {
          char = this.randomChar();
          this.queue[i].char = char;
        }
        output += `<span class="dud">${char}</span>`;
      } else {
        output += from;
      }
    }
    this.el.innerHTML = output;
    if (complete === this.queue.length) {
      this.resolve();
    } else {
      this.frameRequest = requestAnimationFrame(this.update);
      this.frame++;
    }
  }
  randomChar() {
    return this.chars[Math.floor(Math.random() * this.chars.length)];
  }}


const phrases = [
'Shane White',
'cqrCyber / cc',
'tools\ related to Cyber',
'Security',
'&',
'Computer / Science',
'&',
'Ethical Hacking \ { * }',
'an initiative to help secure the Cyber',
'https://godiam.sharepoint.com',
'entwicklerprogramm@pm.me',
'',
'',
''];



const el = document.querySelector('.text-change');
const fx = new TextScramble(el);

let counter = 0;
const next = () => {
  fx.setText(phrases[counter]).then(() => {
    setTimeout(next, 2000);
  });
  counter = (counter + 1) % phrases.length;
};


next();
//# sourceURL=pen.js
    </script>

  

</body>

</html>
 

```
{% endcode %}

|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
| - | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   | \<!DOCTYPE html>                                                                                                                                                                                                                                                                                                                    |
|   | \<html lang="en" >                                                                                                                                                                                                                                                                                                                  |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<head>                                                                                                                                                                                                                                                                                                                             |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<meta charset="UTF-8">                                                                                                                                                                                                                                                                                                             |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   | \<link rel="apple-touch-icon" type="image/png" href="[https://cpwebassets.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png](https://cpwebassets.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png)" /> |
|   | \<meta name="apple-mobile-web-app-title" content="CodePen">                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<link rel="shortcut icon" type="image/x-icon" href="[https://cpwebassets.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico](https://cpwebassets.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico)" />                   |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<link rel="mask-icon" type="image/x-icon" href="[https://cpwebassets.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg](https://cpwebassets.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg)" color="#111" />        |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<title>CodePen - Text Scramble\</title>                                                                                                                                                                                                                                                                                            |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   | \<style>                                                                                                                                                                                                                                                                                                                            |
|   | @import 'https://fonts.googleapis.com/css2?family=Goldman\&display=swap';                                                                                                                                                                                                                                                           |
|   | html,                                                                                                                                                                                                                                                                                                                               |
|   | body {                                                                                                                                                                                                                                                                                                                              |
|   | background: #0d0d0d;                                                                                                                                                                                                                                                                                                                |
|   | height: 100%;                                                                                                                                                                                                                                                                                                                       |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .text-change-container {                                                                                                                                                                                                                                                                                                            |
|   | height: 100%;                                                                                                                                                                                                                                                                                                                       |
|   | width: 100%;                                                                                                                                                                                                                                                                                                                        |
|   | justify-content: center;                                                                                                                                                                                                                                                                                                            |
|   | align-items: center;                                                                                                                                                                                                                                                                                                                |
|   | display: flex;                                                                                                                                                                                                                                                                                                                      |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .text-change {                                                                                                                                                                                                                                                                                                                      |
|   | font-family: 'Goldman', monospace;                                                                                                                                                                                                                                                                                                  |
|   | font-weight: normal;                                                                                                                                                                                                                                                                                                                |
|   | font-size: larger;                                                                                                                                                                                                                                                                                                                  |
|   | color: #c8c8c8;                                                                                                                                                                                                                                                                                                                     |
|   | filter: drop-shadow(0 0 0.3em rgba(200,200,200,0.3));                                                                                                                                                                                                                                                                               |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .dud {                                                                                                                                                                                                                                                                                                                              |
|   | color: rgba(242,5,5,0.8);                                                                                                                                                                                                                                                                                                           |
|   | filter: drop-shadow(0 0 0.5em #f00);                                                                                                                                                                                                                                                                                                |
|   | /\* Color Theme Swatches in Hex \*/                                                                                                                                                                                                                                                                                                 |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-1-hex {                                                                                                                                                                                                                                                                                                                   |
|   | color: #f2f2f2;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-2-hex {                                                                                                                                                                                                                                                                                                                   |
|   | color: #bdb8d9;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-3-hex {                                                                                                                                                                                                                                                                                                                   |
|   | color: #010d00;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-4-hex {                                                                                                                                                                                                                                                                                                                   |
|   | color: #d7d9c7;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-5-hex {                                                                                                                                                                                                                                                                                                                   |
|   | color: #0d0d0d;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | /\* Color Theme Swatches in RGBA \*/                                                                                                                                                                                                                                                                                                |
|   | .Abstract-1-rgba {                                                                                                                                                                                                                                                                                                                  |
|   | color: #f2f2f2;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-2-rgba {                                                                                                                                                                                                                                                                                                                  |
|   | color: #bdb8d9;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-3-rgba {                                                                                                                                                                                                                                                                                                                  |
|   | color: #010d00;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-4-rgba {                                                                                                                                                                                                                                                                                                                  |
|   | color: #d7d9c7;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-5-rgba {                                                                                                                                                                                                                                                                                                                  |
|   | color: #0d0d0d;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | /\* Color Theme Swatches in HSLA \*/                                                                                                                                                                                                                                                                                                |
|   | .Abstract-1-hsla {                                                                                                                                                                                                                                                                                                                  |
|   | color: #f0f0f0;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-2-hsla {                                                                                                                                                                                                                                                                                                                  |
|   | color: #bbb6d8;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-3-hsla {                                                                                                                                                                                                                                                                                                                  |
|   | color: #010a00;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-4-hsla {                                                                                                                                                                                                                                                                                                                  |
|   | color: #d6d8c5;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | .Abstract-5-hsla {                                                                                                                                                                                                                                                                                                                  |
|   | color: #0d0d0d;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | \</style>                                                                                                                                                                                                                                                                                                                           |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<script>                                                                                                                                                                                                                                                                                                                           |
|   | window.console = window.console \|\| function(t) {};                                                                                                                                                                                                                                                                                |
|   | \</script>                                                                                                                                                                                                                                                                                                                          |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   | \<script>                                                                                                                                                                                                                                                                                                                           |
|   | if (document.location.search.match(/type=embed/gi)) {                                                                                                                                                                                                                                                                               |
|   | window.parent.postMessage("resize", "\*");                                                                                                                                                                                                                                                                                          |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | \</script>                                                                                                                                                                                                                                                                                                                          |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \</head>                                                                                                                                                                                                                                                                                                                            |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \<body translate="no" >                                                                                                                                                                                                                                                                                                             |
|   | \<div class="text-change-container">                                                                                                                                                                                                                                                                                                |
|   | \<div class="text-change">\</div>                                                                                                                                                                                                                                                                                                   |
|   | \</div>\<div class="text-change-container">                                                                                                                                                                                                                                                                                         |
|   | \<div class="text-change">\</div>                                                                                                                                                                                                                                                                                                   |
|   | \</div>                                                                                                                                                                                                                                                                                                                             |
|   | \<script src="[https://cpwebassets.codepen.io/assets/common/stopExecutionOnTimeout-1b93190375e9ccc259df3a57c1abc0e64599724ae30d7ea4c6877eb615f89387.js](https://cpwebassets.codepen.io/assets/common/stopExecutionOnTimeout-1b93190375e9ccc259df3a57c1abc0e64599724ae30d7ea4c6877eb615f89387.js)">\</script>                        |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   | \<script id="rendered-js" >                                                                                                                                                                                                                                                                                                         |
|   | class TextScramble {                                                                                                                                                                                                                                                                                                                |
|   | constructor(el) {                                                                                                                                                                                                                                                                                                                   |
|   | this.el = el;                                                                                                                                                                                                                                                                                                                       |
|   | this.chars = '☠!<>-\_\\\\/\[]{}—=+\*^?#\_\_\_\_\_\_\_\_';                                                                                                                                                                                                                                                                           |
|   | this.update = this.update.bind(this);                                                                                                                                                                                                                                                                                               |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | setText(newText) {                                                                                                                                                                                                                                                                                                                  |
|   | const oldText = this.el.innerText;                                                                                                                                                                                                                                                                                                  |
|   | const length = Math.max(oldText.length, newText.length);                                                                                                                                                                                                                                                                            |
|   | const promise = new Promise(resolve => this.resolve = resolve);                                                                                                                                                                                                                                                                     |
|   | this.queue = \[];                                                                                                                                                                                                                                                                                                                   |
|   | for (let i = 0; i < length; i++) {                                                                                                                                                                                                                                                                                                  |
|   | const from = oldText\[i] \|\| '';                                                                                                                                                                                                                                                                                                   |
|   | const to = newText\[i] \|\| '';                                                                                                                                                                                                                                                                                                     |
|   | const start = Math.floor(Math.random() \* 40);                                                                                                                                                                                                                                                                                      |
|   | const end = start + Math.floor(Math.random() \* 40);                                                                                                                                                                                                                                                                                |
|   | this.queue.push({ from, to, start, end });                                                                                                                                                                                                                                                                                          |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | cancelAnimationFrame(this.frameRequest);                                                                                                                                                                                                                                                                                            |
|   | this.frame = 0;                                                                                                                                                                                                                                                                                                                     |
|   | this.update();                                                                                                                                                                                                                                                                                                                      |
|   | return promise;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | update() {                                                                                                                                                                                                                                                                                                                          |
|   | let output = '';                                                                                                                                                                                                                                                                                                                    |
|   | let complete = 0;                                                                                                                                                                                                                                                                                                                   |
|   | for (let i = 0, n = this.queue.length; i < n; i++) {                                                                                                                                                                                                                                                                                |
|   | let { from, to, start, end, char } = this.queue\[i];                                                                                                                                                                                                                                                                                |
|   | if (this.frame >= end) {                                                                                                                                                                                                                                                                                                            |
|   | complete++;                                                                                                                                                                                                                                                                                                                         |
|   | output += to;                                                                                                                                                                                                                                                                                                                       |
|   | } else if (this.frame >= start) {                                                                                                                                                                                                                                                                                                   |
|   | if (!char \|\| Math.random() < 0.28) {                                                                                                                                                                                                                                                                                              |
|   | char = this.randomChar();                                                                                                                                                                                                                                                                                                           |
|   | this.queue\[i].char = char;                                                                                                                                                                                                                                                                                                         |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | output += \`\<span class="dud">${char}\</span>\`;                                                                                                                                                                                                                                                                                   |
|   | } else {                                                                                                                                                                                                                                                                                                                            |
|   | output += from;                                                                                                                                                                                                                                                                                                                     |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | this.el.innerHTML = output;                                                                                                                                                                                                                                                                                                         |
|   | if (complete === this.queue.length) {                                                                                                                                                                                                                                                                                               |
|   | this.resolve();                                                                                                                                                                                                                                                                                                                     |
|   | } else {                                                                                                                                                                                                                                                                                                                            |
|   | this.frameRequest = requestAnimationFrame(this.update);                                                                                                                                                                                                                                                                             |
|   | this.frame++;                                                                                                                                                                                                                                                                                                                       |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | }                                                                                                                                                                                                                                                                                                                                   |
|   | randomChar() {                                                                                                                                                                                                                                                                                                                      |
|   | return this.chars\[Math.floor(Math.random() \* this.chars.length)];                                                                                                                                                                                                                                                                 |
|   | \}}                                                                                                                                                                                                                                                                                                                                 |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | const phrases = \[                                                                                                                                                                                                                                                                                                                  |
|   | 'Shane White',                                                                                                                                                                                                                                                                                                                      |
|   | 'cqrCyber / cc',                                                                                                                                                                                                                                                                                                                    |
|   | 'tools\ related to Cyber',                                                                                                                                                                                                                                                                                                          |
|   | 'Security',                                                                                                                                                                                                                                                                                                                         |
|   | '&',                                                                                                                                                                                                                                                                                                                                |
|   | 'Computer / Science',                                                                                                                                                                                                                                                                                                               |
|   | '&',                                                                                                                                                                                                                                                                                                                                |
|   | 'Ethical Hacking \ { \* }',                                                                                                                                                                                                                                                                                                         |
|   | 'an initiative to help secure the Cyber',                                                                                                                                                                                                                                                                                           |
|   | 'https://godiam.sharepoint.com',                                                                                                                                                                                                                                                                                                    |
|   | 'entwicklerprogramm@pm.me',                                                                                                                                                                                                                                                                                                         |
|   | '',                                                                                                                                                                                                                                                                                                                                 |
|   | '',                                                                                                                                                                                                                                                                                                                                 |
|   | ''];                                                                                                                                                                                                                                                                                                                                |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | const el = document.querySelector('.text-change');                                                                                                                                                                                                                                                                                  |
|   | const fx = new TextScramble(el);                                                                                                                                                                                                                                                                                                    |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | let counter = 0;                                                                                                                                                                                                                                                                                                                    |
|   | const next = () => {                                                                                                                                                                                                                                                                                                                |
|   | fx.setText(phrases\[counter]).then(() => {                                                                                                                                                                                                                                                                                          |
|   | setTimeout(next, 2000);                                                                                                                                                                                                                                                                                                             |
|   | });                                                                                                                                                                                                                                                                                                                                 |
|   | counter = (counter + 1) % phrases.length;                                                                                                                                                                                                                                                                                           |
|   | };                                                                                                                                                                                                                                                                                                                                  |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | next();                                                                                                                                                                                                                                                                                                                             |
|   | //# sourceURL=pen.js                                                                                                                                                                                                                                                                                                                |
|   | \</script>                                                                                                                                                                                                                                                                                                                          |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \</body>                                                                                                                                                                                                                                                                                                                            |
|   | <p><br></p>                                                                                                                                                                                                                                                                                                                         |
|   | \</html>                                                                                                                                                                                                                                                                                                                            |
|   |                                                                                                                                                                                                                                                                                                                                     |
|   |                                                                                                                                                                                                                                                                                                                                     |

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://codepen.io/esz3tt/pen/GRxYWdK" %}

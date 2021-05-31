# Vadim Bezymyannyi
#### [GitHub](https://github.com/Vadosdavos), [Telegramm](https://t.me/inemidavos), [E-mail](bezbvap@gmail.com)
---
I'am 27 years old. I have C&I Engineer degree, but I want to change my speciality. So I started to learn web-technologies, in particular HTML, CSS and JavaScript. Studying is easy for me, I like to solve problems and get results. I appreciate honesty and kindness in people. I want to work remotely and travel.

##### My technology stack: 
* HTML5
* CSS3
* JavaScript
* Bootstrap 
* Git/GitHub

###### My works: 

1. Header for online-zoo:

```
<header class="page-header">
      <div class="container">
        <h1 class="visualy-hidden">Online Zoo</h1>
        <a class="logo" href="index.html"><img src="images/logo-light.svg" alt="Logo" width="59" height="42" /></a>
        <nav>
          <ul class="header-nav">
            <li class="nav-item active"><a>About</a></li>
            <li class="nav-item"><a href="live-broadcast-panda.html">Zoos</a></li>
            <li class="nav-item"><a href="map.html">Map</a></li>
            <li class="nav-item"><a href="#contact-form">Contact Us</a></li>
            <li class="nav-item"><a href="https://www.figma.com/file/HKt5Nlx0jghQtJp6jW9q8F/zooApp">Design</a></li>
          </ul>
        </nav>
        <div class="theme-btn-container">
          <input id="theme" type="checkbox" class="theme-check" />
          <label for="theme" class="theme-btn"></label>
        </div>
      </div>
    </header>
```
2. JavaScript for online-piano:

```
function playAudio(src) {
  const audio = new Audio();
  audio.src = src;
  audio.currentTime = 0;
  audio.play();
}
piano.addEventListener('mousedown', function (evt) {
  if (evt.target.classList.contains('piano-key')) {
    isMousedown = true;
    let note = evt.target.dataset.note;
    let src = `assets/audio/${note}.mp3`;
    playAudio(src);
    pianoKeys.forEach((el) => {
      if (el.classList.contains('piano-key-active')) {
        el.classList.remove('piano-key-active');
      }
    });
    evt.target.classList.add('piano-key-active');
  }
});
window.addEventListener('mouseup', function (evt) {
  isMousedown = false;
  pianoKeys.forEach((el) => {
    if (el.classList.contains('piano-key-active')) {
      el.classList.remove('piano-key-active');
    }
  });
});
window.addEventListener('mouseover', function (evt) {
  if (evt.target.classList.contains('piano-key') && isMousedown) {
    let note = evt.target.dataset.note;
    let src = `assets/audio/${note}.mp3`;
    playAudio(src);
    evt.target.classList.add('piano-key-active');
  }
});
window.addEventListener('mouseout', function (evt) {
  if (evt.target.classList.contains('piano-key') && isMousedown) {
    evt.target.classList.remove('piano-key-active');
  }
});
window.addEventListener('keydown', function (evt) {
  if (evt.repeat) {
    return;
  }
  let letter = evt.code.charAt(evt.code.length - 1);
  for (let pianoKey of pianoKeys) {
    if (letter === pianoKey.dataset.letter) {
      let note = pianoKey.dataset.note;
      let src = `assets/audio/${note}.mp3`;
      playAudio(src);
      pianoKey.classList.add('piano-key-active');
    }
  }
  window.addEventListener('keyup', function (evt) {
    pianoKeys.forEach((el) => {
      if (el.classList.contains('piano-key-active')) {
        el.classList.remove('piano-key-active');
      }
    });
  });
});

buttonsContainer.addEventListener('click', function (evt) {
  if (evt.target.classList.contains('btn')) {
    buttons.forEach((bt) => {
      if (bt.classList.contains('btn-active')) {
        bt.classList.remove('btn-active');
      }
    });
    evt.target.classList.add('btn-active');
    if (evt.target.classList.contains('btn-letters')) {
      pianoKeys.forEach((el) => {
        el.classList.add('piano-key-letter');
      });
    } else {
      pianoKeys.forEach((el) => {
        el.classList.remove('piano-key-letter');
      });
    }
  }
});
```

##### Education: 

* Kaliningrad State Technical University 2010-2015. Master degree of Automation of technological processes and production
* [CS50](https://cs50.harvard.edu/) online-course (https://github.com/Vadosdavos/cs50)
* html training at [HTML Academy](https://htmlacademy.ru/)

##### Language skills:
* Russian: Native
* English: Pre-Intermediate

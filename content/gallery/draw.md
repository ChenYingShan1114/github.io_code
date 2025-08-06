---
title: "My art works"
date: 2025-04-30
draft: false
---

<style>

body  {
    background-image: url("/self/img/gallery/draw/background.jpg");
    background-repeat: no-repeat;
    background-color: #a3a3a3;
    background-position: fixed; /* Center the image */
    background-size: cover;
}

.gallery-container {
  position: relative;
  width: 100%;
  height: 800px;
  margin: 0 auto;
}

.center-images {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  gap: 20px;
  z-index: 10;
}

.center-images img {
  width: 250px;
  height: 350px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
}

.sticker {
  position: absolute;
  width: 150px;
  height: auto;
  transition: transform 0.3s ease;
  cursor: pointer;
}

.sticker:hover {
  transform: scale(1.1) rotate(5deg);
}

.sticker img {
  width: 100%;
  height: auto;
}

/* Random positions for stickers - no overlap, avoiding center */

.sticker:nth-child(2) { top: 18%; left: 18%; } /*doll*/
.sticker:nth-child(3) { top: 6%; left: 68%; } /*penguin*/
.sticker:nth-child(4) { top: 7%; left: 35%; } /*dragon*/
.sticker:nth-child(5) { top: 35%; left: 5%; } /*stitch*/
.sticker:nth-child(6) { top: 8%; left: 6%; } /*sunfish*/
.sticker:nth-child(7) { top: 37%; left: 78%; } /*giraffe*/
.sticker:nth-child(8) { top: 41%; left: 88%; } /*santa*/
.sticker:nth-child(9) { top: 72%; left: 25%; } /*frog*/
.sticker:nth-child(10) { top: 68%; left: 13%; } /*pikachu*/
.sticker:nth-child(11) { top: 75%; left: 42%; } /*elephant*/
.sticker:nth-child(12) { top: 78%; left: 58%; } /*car*/
.sticker:nth-child(13) { top: 15%; left: 85%; } /*octopus*/
.sticker:nth-child(14) { top: 12%; left: 50%; } /*101dog*/
.sticker:nth-child(15) { top: 70%; left: 78%; } /*walle*/
.sticker:nth-child(16) { top: 85%; left: 20%; } 
/*.sticker:nth-child(26) { top: 88%; left: 38%; }
.sticker:nth-child(27) { top: 82%; left: 55%; }
.sticker:nth-child(28) { top: 85%; left: 72%; }
.sticker:nth-child(29) { top: 92%; left: 12%; }
.sticker:nth-child(30) { top: 95%; left: 82%; } */

.flip-card {
  background-color: transparent;
  width: 250px;
  height: 350px;
  perspective: 1000px;
  display: inline-block;
}
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  transition: transform 0.6s cubic-bezier(.4,2,.6,1);
  transform-style: preserve-3d;
}
.flip-card.flipped .flip-card-inner {
  transform: rotateY(180deg);
}
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
  font-size: 2rem;
  font-family: monospace;
}
.flip-card-front {
  background: #fff;
}
.flip-card-back {
  background: #222;
  color: #fff;
  transform: rotateY(180deg);
  width: 250px; /* match image width */
  height: 350px; /* match image height */
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  font-family: monospace;
  padding: 24px; /* <-- Add this line for margin inside the box */
  box-sizing: border-box; /* Ensures padding doesn't overflow */
  font-size: 12px;
}

</style>

<div class="gallery-container">
  <!-- Center images -->
  <div class="center-images">
    <div class="flip-card" id="flipSeries01">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <img src="/self/img/gallery/draw/series01.png"/>
        </div>
        <div class="flip-card-back">
          One day, I dove into the crystal-clear waters and discovered a mysterious jade stone — perfectly shaped like my homeland, Taiwan.
        </div>
      </div>
    </div>
    <div class="flip-card" id="flipSeries02">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <img src="/self/img/gallery/draw/series02.png"/>
        </div>
        <div class="flip-card-back">
          Intrigued by its beauty, I gently picked it up and vowed to care for it like a treasured companion. From that moment on, we journeyed together — across lands and seas — sharing breathtaking views and tasting delicious foods from around the world.
        </div>
      </div>
    </div>
    <div class="flip-card" id="flipSeries03">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <img src="/self/img/gallery/draw/series03.png"/>
        </div>
        <div class="flip-card-back">
          Now, we've climbed to the mountain’s edge to gaze upon the most stunning cityscape around Taipei 101. But adventures take energy, and we’re in need of something special — sweet, juicy fruits from Taiwan, of course! 🍍🍌 <br>
          Will you help us find them hidden in the scene? But beware… some areas are enchanted. Don’t touch the magic! ✨
        </div>
      </div>
    </div>
  </div>

  <!-- Sticker images positioned around -->
  <div class="sticker" id="toggleSticker01"><img src="/self/img/gallery/draw/doll.png"/></div>
  <div class="sticker" id="toggleSticker02"><img src="/self/img/gallery/draw/penguin.png"/></div>
  <div class="sticker" id="toggleSticker03"><img src="/self/img/gallery/draw/dragon.png"/></div>
  <div class="sticker" id="toggleSticker04"><img src="/self/img/gallery/draw/stitch.png"/></div>
  <div class="sticker" id="toggleSticker05"><img src="/self/img/gallery/draw/sunfish.png"/></div>
  <div class="sticker" id="toggleSticker06"><img src="/self/img/gallery/draw/giraffe.png"/></div>
  <div class="sticker" id="toggleSticker07"><img src="/self/img/gallery/draw/santa.png"/></div>
  <div class="sticker" id="toggleSticker08"><img src="/self/img/gallery/draw/frog.png"/></div>
  <div class="sticker" id="toggleSticker09"><img src="/self/img/gallery/draw/pikachu.png"/></div>
  <div class="sticker" id="toggleSticker10"><img src="/self/img/gallery/draw/elephant.png"/></div>
  <div class="sticker" id="toggleSticker11"><img src="/self/img/gallery/draw/car.png"/></div>
  <div class="sticker" id="toggleSticker12"><img src="/self/img/gallery/draw/octopus.png"/></div>
  <div class="sticker" id="toggleSticker13"><img src="/self/img/gallery/draw/101dog.png"/></div>
  <div class="sticker" id="toggleLottery"><img src="/self/img/gallery/draw/wallE.png"/></div>
</div>

<div id="magicOverlay" style="display:none; position:fixed; top:0; left:0; width:100vw; height:100vh; background:rgba(0,0,0,0.8); z-index:9999; justify-content:center; align-items:center;">
  <span id="magicText" style="color:white; font-size:2rem; font-family:monospace;"></span>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  // Generic toggle function
  function createToggle(elementId, originalSrc, toggleSrc) {
    const element = document.getElementById(elementId);
    const img = element.querySelector('img');
    let isOriginal = false;
    
    element.addEventListener('click', function() {
      if (isOriginal) {
        img.src = toggleSrc;
        isOriginal = false;
      } else {
        img.src = originalSrc;
        isOriginal = true;
      }
    });
  }

  // Create toggles for each sticker
  createToggle('toggleSticker01', '/self/img/gallery/draw/fruit01.png', '/self/img/gallery/draw/doll.png');
  createToggle('toggleSticker02', '/self/img/gallery/draw/fruit02.png', '/self/img/gallery/draw/penguin.png');
  createToggle('toggleSticker03', '/self/img/gallery/draw/fruit03.png', '/self/img/gallery/draw/dragon.png');
  createToggle('toggleSticker04', '/self/img/gallery/draw/fruit04.png', '/self/img/gallery/draw/stitch.png');
  createToggle('toggleSticker05', '/self/img/gallery/draw/fruit05.png', '/self/img/gallery/draw/sunfish.png');
  createToggle('toggleSticker06', '/self/img/gallery/draw/fruit06.png', '/self/img/gallery/draw/giraffe.png');
  createToggle('toggleSticker07', '/self/img/gallery/draw/fruit07.png', '/self/img/gallery/draw/santa.png');
  createToggle('toggleSticker08', '/self/img/gallery/draw/fruit08.png', '/self/img/gallery/draw/frog.png');
  createToggle('toggleSticker09', '/self/img/gallery/draw/fruit09.png', '/self/img/gallery/draw/pikachu.png');
  createToggle('toggleSticker10', '/self/img/gallery/draw/fruit10.png', '/self/img/gallery/draw/elephant.png');
  createToggle('toggleSticker11', '/self/img/gallery/draw/fruit11.png', '/self/img/gallery/draw/car.png');
  createToggle('toggleSticker12', '/self/img/gallery/draw/fruit12.png', '/self/img/gallery/draw/octopus.png');
  createToggle('toggleSticker13', '/self/img/gallery/draw/fruit13.png', '/self/img/gallery/draw/101dog.png');

  // WallE sticker click redirects to project page
  const wallESticker = document.getElementById('toggleLottery');
  if (wallESticker) {
    wallESticker.addEventListener('click', function() {
      // Show overlay
      var overlay = document.getElementById('magicOverlay');
      var textElem = document.getElementById('magicText');
      var message = 'the magic from 2D to 3D......';
      overlay.style.display = 'flex';
      textElem.textContent = '';
      let i = 0;

      // Typewriter effect
      function typeWriter() {
        if (i < message.length) {
          textElem.textContent += message.charAt(i);
          i++;
          setTimeout(typeWriter, 60);
        } else {
          // After a pause, redirect
          setTimeout(function() {
            window.location.href = '/projects/projects_animation/walle/';
          }, 1200);
        }
      }
      typeWriter();
    });
  }

  // Always hide the overlay and clear the message on page load
  var overlay = document.getElementById('magicOverlay');
  var textElem = document.getElementById('magicText');
  if (overlay && textElem) {
    overlay.style.display = 'none';
    textElem.textContent = '';
  }
});

window.addEventListener('pageshow', function() {
  var overlay = document.getElementById('magicOverlay');
  var textElem = document.getElementById('magicText');
  if (overlay && textElem) {
    overlay.style.display = 'none';
    textElem.textContent = '';
  }
});

function addFlipToggle(cardId) {
  const card = document.getElementById(cardId);
  if (card) {
    card.addEventListener('click', function() {
      card.classList.toggle('flipped');
    });
  }
}
addFlipToggle('flipSeries01');
addFlipToggle('flipSeries02');
addFlipToggle('flipSeries03');
</script>
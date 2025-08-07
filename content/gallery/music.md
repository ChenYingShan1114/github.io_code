---
title: "My Music Life"
date: 2019-06-30
draft: false
not_show_date: true
---

<style>
.gallery-container {
  position: relative;
  width: 100%;
  display: flex;
  align-items: flex-start;
  height: 890px;
  background-color: white; /* For browsers that do not support gradients */
  background-image: linear-gradient(to bottom right, black, white);
}


.block {
  display: flex;
  flex-direction: column;
  /* align-items: center; ← remove to allow left alignment */
  margin-left: 50px;
}

.music-table {
  color: white;
  background: rgba(0, 0, 0, 0);
  width: 550px;
  margin: 20px 0 24px 10px; /* 200px down, 10px right */
  border-collapse: collapse;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

.music-table th, .music-table td {
  padding: 8px 12px;
}

.video-vertical {
  flex: 0 0 auto;
  margin: 12px 0px 24px 120px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.2);
  overflow: hidden;
  background: #111;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 560px;
  width: 315px;
}

.video-vertical iframe {
  display: block;
  width: 315px;
  height: 560px;
  border: none;
  border-radius: 16px;
}

.sticker {
  margin: 0px 0px 0px -120px;
  width: 70px;
}
</style>

<div class="gallery-container">
  <div class="block">
    <table class="music-table">
      <tr>
        <th>Instrument</th>
        <th>Start to End</th>
        <th>Years Played</th>
        <th>Music Genre</th>
      </tr>
      <tr>
        <td align="center">Violin</td>
        <td align="center">5 to 16</td>
        <td align="center">12</td>
        <td align="center">Classical Music</td>
      </tr>
      <tr>
        <td align="center">Piano</td>
        <td align="center">6 to 15</td>
        <td align="center">10</td>
        <td align="center">Classical Music</td>
      </tr>
      <tr>
        <td align="center">Percussion</td>
        <td align="center">16 to 18</td>
        <td align="center">3</td>
        <td align="center">Popular Music with Wind Band</td>
      </tr>
      <tr>
        <td align="center">Guitar</td>
        <td align="center">18 till now (self-learned)</td>
        <td align="center"></td>
        <td align="center">Play Popular Music and Sing by Myself</td>
      </tr>
    </table>
    <div class="video-vertical">
      <iframe width="315" height="560" src="https://www.youtube.com/embed/ywocoA_z8Wg?si=-APK_xexGwPtssbf"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </div>
  </div>
  <div class="sticker" id="violinSticker">
    <img src="/self/img/gallery/draw/violin.png" />
  </div>
</div>
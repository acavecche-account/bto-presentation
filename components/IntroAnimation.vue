<template>
<div id="intro-anim" style="position:fixed;inset:0;background:#000;z-index:100;overflow:hidden;">
  <!-- EARTH -->
  <div id="earth-wrap" style="position:absolute;inset:0;display:flex;align-items:center;justify-content:center;transition:transform 2s ease-in, opacity 0.5s ease;">
    <div id="globe" style="width:380px;height:380px;border-radius:50%;background:radial-gradient(circle at 35% 35%, #1a3a5c, #0a0a0a);border:1px solid #1e3a5c;box-shadow:0 0 80px #0a2a4a, inset 0 0 60px #0a1a2a;animation:spin 12s linear infinite;position:relative;">
      <div style="position:absolute;top:22%;left:18%;width:28%;height:22%;background:#0d2a1a;border-radius:40% 60% 50% 40%;opacity:0.7;"></div>
      <div style="position:absolute;top:30%;left:52%;width:20%;height:26%;background:#0d2a1a;border-radius:50%;opacity:0.7;"></div>
      <div style="position:absolute;top:50%;left:30%;width:16%;height:18%;background:#0d2a1a;border-radius:50%;opacity:0.6;"></div>
      <div style="position:absolute;top:18%;left:58%;width:24%;height:18%;background:#0d2a1a;border-radius:60% 40%;opacity:0.7;"></div>
    </div>
  </div>
  <!-- ZOOM FLASH -->
  <div id="flash" style="position:absolute;inset:0;background:#fff;opacity:0;pointer-events:none;"></div>
  <!-- ROOM SCENE -->
  <div id="room" style="position:absolute;inset:0;opacity:0;display:flex;align-items:flex-end;justify-content:center;padding-bottom:0;transition:opacity 0.8s ease;">
    <div style="position:absolute;inset:0;background:linear-gradient(180deg,#0a0a0f 0%,#0f0f1a 60%,#1a1a2a 100%);"></div>
    <div style="position:relative;z-index:2;width:600px;margin-bottom:0;">
      <div style="background:#1a1208;height:18px;border-radius:4px 4px 0 0;box-shadow:0 -2px 20px rgba(0,0,0,0.8);"></div>
      <div id="laptop" style="position:absolute;bottom:18px;left:50%;transform:translateX(-50%) scale(0.6);transition:transform 1.2s cubic-bezier(0.16,1,0.3,1), opacity 0.5s ease;opacity:0;">
        <div style="width:300px;background:#111;border-radius:8px 8px 0 0;border:2px solid #333;padding:4px;box-shadow:0 0 40px rgba(100,150,255,0.15);">
          <div id="screen" style="width:100%;aspect-ratio:16/9;background:#050510;border-radius:4px;overflow:hidden;display:flex;align-items:center;justify-content:center;position:relative;">
            <div style="position:absolute;inset:0;background:radial-gradient(circle,rgba(80,120,255,0.08),transparent 70%);"></div>
            <video id="intro-video" autoplay muted loop playsinline style="width:100%;height:100%;object-fit:cover;opacity:0;transition:opacity 0.5s ease;" :src="videoSrc"></video>
            <div id="screen-placeholder" style="position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;">
              <div style="font-size:1.5rem;">▶</div>
              <div style="font-size:0.6rem;color:#555;letter-spacing:0.1em;text-transform:uppercase;">drop intro-clip.mp4 in /assets</div>
            </div>
          </div>
        </div>
        <div style="width:300px;height:6px;background:#222;border-radius:0 0 2px 2px;border:2px solid #333;border-top:none;"></div>
        <div style="width:320px;margin-left:-10px;height:12px;background:#1a1a1a;border-radius:0 0 8px 8px;border:2px solid #333;border-top:none;"></div>
      </div>
      <div style="position:absolute;bottom:0;left:50%;transform:translateX(-50%);width:200px;height:30px;background:rgba(80,120,255,0.06);filter:blur(20px);border-radius:50%;"></div>
    </div>
  </div>
  <!-- SKIP -->
  <div @click="skipIntro" style="position:absolute;bottom:2rem;right:2rem;font-size:0.7rem;color:#444;letter-spacing:0.1em;text-transform:uppercase;cursor:pointer;z-index:200;">skip →</div>
</div>
</template>

<script setup>
import { onMounted } from 'vue'

const videoSrc = '/assets/intro-clip.mp4'

function skipIntro() {
  const anim = document.getElementById('intro-anim')
  if (!anim) return
  anim.style.transition = 'opacity 0.4s'
  anim.style.opacity = '0'
  setTimeout(() => { anim.style.display = 'none' }, 400)
}

onMounted(() => {
  const anim = document.getElementById('intro-anim')
  const earthWrap = document.getElementById('earth-wrap')
  const flash = document.getElementById('flash')
  const room = document.getElementById('room')
  const laptop = document.getElementById('laptop')
  const video = document.getElementById('intro-video')
  const placeholder = document.getElementById('screen-placeholder')
  if (!anim) return
  setTimeout(() => {
    if (earthWrap) { earthWrap.style.transform = 'scale(12)'; earthWrap.style.opacity = '0' }
  }, 2000)
  setTimeout(() => {
    if (flash) { flash.style.transition = 'opacity 0.15s'; flash.style.opacity = '0.6'; setTimeout(() => { flash.style.opacity = '0' }, 150) }
  }, 2800)
  setTimeout(() => { if (room) room.style.opacity = '1' }, 2900)
  setTimeout(() => {
    if (laptop) { laptop.style.opacity = '1'; laptop.style.transform = 'translateX(-50%) scale(1)' }
  }, 3400)
  setTimeout(() => {
    if (video && video.readyState >= 2 && placeholder) { placeholder.style.opacity = '0'; video.style.opacity = '1' }
  }, 4200)
  setTimeout(() => {
    anim.style.transition = 'opacity 0.8s'
    anim.style.opacity = '0'
    setTimeout(() => { anim.style.display = 'none' }, 800)
  }, 7000)
})
</script>

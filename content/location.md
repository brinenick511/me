---
title: "Location"
date: 2024-05-08
hidemeta: true
description: "Address and location for the School of Computer Science, Wuhan University."

---

---

#### Address

School of Computer Science, Wuhan University  
Room 702  
Wuhan 430072  
Hubei, China

---

#### Location

<div class="location-map">
  <div class="location-map-switch" role="group" aria-label="Map provider">
    <button type="button" data-map-provider="google" aria-pressed="true">Google Maps</button>
    <button type="button" data-map-provider="amap" aria-pressed="false">高德地图</button>
  </div>
  <button class="location-map-poster" type="button" aria-label="Load interactive map">
    <img src="/me/location-map-preview.webp" width="2280" height="1428"
      alt="Map preview around the School of Computer Science, Wuhan University"
      loading="lazy" decoding="async">
    <span class="location-map-load">Load interactive map</span>
  </button>
  <iframe
    id="location-map-frame"
    title="Interactive map showing the School of Computer Science, Wuhan University"
    data-google="https://www.google.com/maps?q=Xiaomi-Wuhan%20University%20Artificial%20Intelligent%20Union%20Laboratory&amp;z=17&amp;hl=en&amp;output=embed"
    data-amap="https://www.amap.com/ssr/embed/place?name=%E6%AD%A6%E6%B1%89%E5%A4%A7%E5%AD%A6%E8%AE%A1%E7%AE%97%E6%9C%BA%E5%AD%A6%E9%99%A2&amp;lng=114.357486&amp;lat=30.538507&amp;address=%E6%B9%96%E5%8C%97%E7%9C%81%E6%AD%A6%E6%B1%89%E5%B8%82%E6%AD%A6%E6%98%8C%E5%8C%BA%E7%8F%9E%E7%8F%88%E5%B1%B1%E8%A1%97%E9%81%93%E6%80%9D%E6%BA%90%E8%B7%AF&amp;zoom=16&amp;source=poi_detail&amp;platform=pc"
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"
    allowfullscreen hidden></iframe>
  <noscript>
    <p class="location-map-fallback">
      <a href="https://www.google.com/maps/search/?api=1&amp;query=Xiaomi-Wuhan%20University%20Artificial%20Intelligent%20Union%20Laboratory">Open in Google Maps</a>
      ·
      <a href="https://uri.amap.com/marker?position=114.357486,30.538507&amp;name=%E6%AD%A6%E6%B1%89%E5%A4%A7%E5%AD%A6%E8%AE%A1%E7%AE%97%E6%9C%BA%E5%AD%A6%E9%99%A2">Open in Amap</a>
    </p>
  </noscript>
  <p class="location-map-links">
    <a href="https://www.google.com/maps/search/?api=1&amp;query=Xiaomi-Wuhan%20University%20Artificial%20Intelligent%20Union%20Laboratory" target="_blank" rel="noopener noreferrer">Open in Google Maps</a>
    <span aria-hidden="true">·</span>
    <a href="https://uri.amap.com/marker?position=114.357486,30.538507&amp;name=%E6%AD%A6%E6%B1%89%E5%A4%A7%E5%AD%A6%E8%AE%A1%E7%AE%97%E6%9C%BA%E5%AD%A6%E9%99%A2" target="_blank" rel="noopener noreferrer">Open in Amap</a>
  </p>
</div>

<script>
(() => {
  const wrap = document.querySelector('.location-map');
  if (!wrap) return;
  const frame = wrap.querySelector('iframe');
  const poster = wrap.querySelector('.location-map-poster');
  const buttons = [...wrap.querySelectorAll('[data-map-provider]')];
  const urls = { google: frame.dataset.google, amap: frame.dataset.amap };
  let current = 'google';
  let loaded = false;
  let warmed = false;

  const load = (provider) => {
    if (!urls[provider]) return;
    current = provider;
    frame.src = urls[provider];
    frame.hidden = false;
    poster.hidden = true;
    loaded = true;
    buttons.forEach((button) => {
      button.setAttribute('aria-pressed', String(button.dataset.mapProvider === provider));
    });
  };

  const select = (provider, loadNow = false) => {
    if (!urls[provider]) return;
    current = provider;
    buttons.forEach((button) => {
      button.setAttribute('aria-pressed', String(button.dataset.mapProvider === provider));
    });
    if (loadNow || loaded) load(provider);
  };

  const warm = () => {
    if (warmed) return;
    warmed = true;
    const link = document.createElement('link');
    link.rel = 'preconnect';
    link.href = new URL(urls[current]).origin;
    link.crossOrigin = '';
    document.head.appendChild(link);
  };

  let initial = 'google';
  try {
    const timeZone = Intl.DateTimeFormat().resolvedOptions().timeZone || '';
    const languages = navigator.languages || [];
    const language = languages[0] || navigator.language || '';
    const chinaTimeZone = /^Asia\/(Shanghai|Chongqing|Urumqi|Harbin)$/i.test(timeZone);
    const chineseLanguage = languages.some((item) => /^zh/i.test(item)) || /^zh/i.test(language);
    if (chinaTimeZone && chineseLanguage) {
      initial = 'amap';
    }
  } catch (error) {
    // Keep the Google default when locale detection is unavailable.
  }
  select(initial);

  poster.addEventListener('click', () => load(current));
  poster.addEventListener('pointerenter', warm, { once: true });
  poster.addEventListener('focus', warm, { once: true });

  buttons.forEach((button) => {
    button.addEventListener('click', () => select(button.dataset.mapProvider, true));
    button.addEventListener('pointerenter', warm, { once: true });
  });
})();
</script>

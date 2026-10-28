---
layout: home
permalink: /
title: "About me"
excerpt: "PhD candidate in Economics at IIT Roorkee, working on health economics, household economics and microeconometrics."
tagline: "Who Bears the Cost of Economic Growth?"
lede: "Doctoral candidate in Economics at AHEAD Lab, IIT Roorkee"
redirect_from:
  - /about/
  - /about.html
---

<section id="about">
  <h2>About</h2>
  <div class="cards">
    <div class="card"><h3>Research focus</h3><p>My current work studies health state dependence in decision making, especially in the context of occupational health risks.</p></div>
    <div class="card"><h3>Background</h3><p>Research Assistant at ISID, Delhi, with internships at ZIGRAM Data Technologies and RIS, Delhi. MSc in Economics from IIT Roorkee; BSc in Mathematics from Dr. Bhimrao Ambedkar University, Agra.</p></div>
    <div class="card"><h3>Methods</h3><p>Microeconometrics and text-as-data approaches, such as structural topic modeling of parliamentary records.</p></div>
  </div>

  <p class="sub">Presented at</p>
  <ul class="chips">
    <li>Indiana University (ISSI’22)</li>
    <li>IIM Ahmedabad (IMRC’25)</li>
    <li>IGIDR Mumbai (CoRE’25)</li>
    <li>MIDS Chennai (DC’25)</li>
    <li>NIT Goa (TAES’25)</li>
    <li>VVGNLI Noida</li>
    <li>SANEM Dhaka (SAEC’23, ’25)</li>
  </ul>

  <p class="sub">Accepted for presentation</p>
  <ul class="chips">
    <li class="up">University of Vienna (COMPTEXT 2025)</li>
    <li class="up">University of Iceland (NHESG’26)</li>
    <li class="up">University of Tasmania (AHES’26)</li>
    <li class="up">Paññāsāstra University of Cambodia (SAERD’26)</li>
  </ul>

  <p class="sub">Map</p>
  <p style="font-size:0.9em; margin:0 0 8px;">
    <span style="color:#1a5fb4;">●</span> Presented &nbsp;
    <span style="color:#e66100;">●</span> Accepted for presentation
  </p>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.css">
  <div id="conf-map" style="height:480px; width:100%; border-radius:8px; position:relative; z-index:0;"></div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.js"></script>
  <script>
  window.addEventListener('load', function () {
    var el = document.getElementById('conf-map');
    if (typeof L === 'undefined') { el.innerHTML = '<p style="padding:1em">Map could not be loaded.</p>'; return; }
    const map = L.map('conf-map').setView([25, 40], 2);
    L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 18,
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);
    const presented = [
      ["Indiana University (ISSI'22)", 39.1682, -86.5230],
      ["IIM Ahmedabad (IMRC'25)", 23.0347, 72.5339],
      ["IGIDR Mumbai (CoRE'25)", 19.1675, 72.8797],
      ["MIDS Chennai (DC'25)", 13.0078, 80.2548],
      ["NIT Goa (TAES'25)", 15.4015, 73.9792],
      ["VVGNLI Noida", 28.5868, 77.3477],
      ["SANEM Dhaka (SAEC'23, '25)", 23.7964, 90.4154]
    ];
    const accepted = [
      ["University of Vienna (COMPTEXT 2025)", 48.2132, 16.3599],
      ["University of Iceland (NHESG'26)", 64.1395, -21.9506],
      ["University of Tasmania (AHES'26)", -42.9026, 147.3273],
      ["Paññāsāstra University of Cambodia (SAERD'26)", 11.5730, 104.8904]
    ];
    presented.forEach(([n, lat, lng]) =>
      L.circleMarker([lat, lng], {radius: 8, color: '#1a5fb4', fillOpacity: 0.85})
        .addTo(map).bindPopup('<b>' + n + '</b><br>Presented'));
    accepted.forEach(([n, lat, lng]) =>
      L.circleMarker([lat, lng], {radius: 8, color: '#e66100', fillOpacity: 0.85})
        .addTo(map).bindPopup('<b>' + n + '</b><br>Accepted for presentation'));
  });
  </script>
</section>

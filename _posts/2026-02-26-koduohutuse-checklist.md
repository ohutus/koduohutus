---
layout: post
title: "Koduohutuse checklist"
---

# Koduohutuse checklist

<ul id="checklist">
  <li><input type="checkbox" id="punkt1">Tulekustuti olemas ja töökorras</li>
  <li><input type="checkbox" id="punkt2">Suitsuandurid paigaldatud ja kontrollitud</li>
  <li><input type="checkbox" id="punkt3">Gaasiandurid paigaldatud</li>
  <li><input type="checkbox" id="punkt4">Esmaabikomplekt kättesaadav</li>
  <li><input type="checkbox" id="punkt5">Elektrijuhtmed korras, vigastusi pole</li>
  <li><input type="checkbox" id="punkt6">Uksed ja lukud turvalised</li>
  <li><input type="checkbox" id="punkt7">Akende turvalukud paigaldatud</li>
  <li><input type="checkbox" id="punkt8">Libisemisvastased mattid vannitoas</li>
  <li><input type="checkbox" id="punkt9">Valgustus pimedates kohtades</li>
  <li><input type="checkbox" id="punkt10">Tulekustuti ja suitsuandurite hoolduskuupäevad üle vaadatud</li>
</ul>

<button onclick="kuvaTulemus()">Näita tulemusi</button>

<script>
function kuvaTulemus() {
  const checklist = document.querySelectorAll('#checklist input[type="checkbox"]');
  let kontrollitud = [];
  checklist.forEach((item, index) => {
    if (item.checked) kontrollitud.push(`Punkt ${index + 1}: ${item.nextSibling.textContent.trim()}`);
  });

  if (kontrollitud.length === 0) {
    alert("Ühtki punkti ei ole veel kontrollitud!");
  } else {
    alert("Kontrollitud punktid:\n" + kontrollitud.join("\n"));
  }
}
</script>
<!DOCTYPE html>
<html lang="et">
<head>
<meta charset="UTF-8">
<title>Värviriba</title>
<style>
  body {
    margin: 0;
    background: #111;
  }

  .color-bar {
    width: 100%;
    height: 12px; /* natuke suurem riba */
  }
</style>
</head>
<body>

<div class="color-bar" id="bar"></div>

<script>
  const bar = document.getElementById("bar");
  let hue = 0;

  setInterval(() => {
    hue = (hue + 1) % 360;
    bar.style.backgroundColor = `hsl(${hue}, 100%, 50%)`;
  }, 60);
</script>

</body>
</html>


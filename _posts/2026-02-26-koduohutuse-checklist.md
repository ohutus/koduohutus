---
layout: post
title: "Koduohutuse checklist"
---

<!DOCTYPE html>
<html lang="et">
<head>
  <meta charset="UTF-8">
  <title>Koduohutuse Checklist</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; }
    h1 { color: #2c3e50; }
    ul { list-style: none; padding: 0; }
    li { margin: 10px 0; }
    input[type="checkbox"] { transform: scale(1.2); margin-right: 10px; }
  </style>
</head>
<body>

<h1>Koduohutuse Checklist</h1>
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

</body>
</html>

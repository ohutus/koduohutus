---
layout: post
title: "Koduohutuse checklist"
---

// Koduohutuse checklist
const koduohutusChecklist = [
  { id: 1, teema: "Tulekustuti", kontrollitud: false },
  { id: 2, teema: "Suitsuandurid", kontrollitud: false },
  { id: 3, teema: "Gaasiandurid", kontrollitud: false },
  { id: 4, teema: "Esmaabikomplekt", kontrollitud: false },
  { id: 5, teema: "Elektrijuhtmete kontroll", kontrollitud: false },
  { id: 6, teema: "Uksed ja lukud", kontrollitud: false },
  { id: 7, teema: "Akende turvalukk", kontrollitud: false },
  { id: 8, teema: "Libisemisvastased mattid vannitoas", kontrollitud: false },
  { id: 9, teema: "Valgustus pimedates kohtades", kontrollitud: false },
  { id: 10, teema: "Tulekustuti ja suitsuandurite kuupäevad", kontrollitud: false }
];

// Funktsioon kontrolli märkimiseks
function märgiKontrollitud(id) {
  const item = koduohutusChecklist.find(i => i.id === id);
  if (item) {
    item.kontrollitud = true;
    console.log(`${item.teema} on märgitud kontrollituks.`);
  } else {
    console.log("Sellist punkti ei leitud.");
  }
}

// Funktsioon kontrolltabeli kuvamiseks
function kuvaChecklist() {
  console.log("=== Koduohutuse Checklist ===");
  koduohutusChecklist.forEach(item => {
    const staatus = item.kontrollitud ? "[✓]" : "[ ]";
    console.log(`${staatus} ${item.teema}`);
  });
}

// Näide kasutamisest
kuvaChecklist();      // Näitab kogu checklisti
märgiKontrollitud(2); // Märgib suitsuandurid kontrollituks
kuvaChecklist();      // Kuvab uuendatud checklisti


---
layout: post
title: "Suvaline fakt liiklusohutuse kohta"
---

<b id="fakt">Enamik raskeid õnnetusi juhtub tuttaval teel</b>

<button id="teinefakt">Veel</button>

<script>const faktid = [
  "Enamik raskeid õnnetusi juhtub tuttaval teel",
  "Turvavöö vähendab surma riski eest kokkupõrkes ligi 45–50%",
  "Turvapadi avaneb umbes 20–40 millisekundiga.",
  "Ilma turvavööta võib turvapadi hoopis vigastusi suurendada.",
  "Pimedas helkurita jalakäiat on lähituledega märgatav umbes 30 meetri pealt. Helkuriga võib nähtavus ulatuda 150 meetrini või rohkem",
  "Telefon roolis pikendab reaktsiooniaega rohkem kui kerge joove",
  "Kiiruse väike tõus = suur riskitõus. Kui kiirus kasvab 50 km/h pealt 60 km/h-ni, suureneb jalakäija surma risk mitmekordselt, kui kokkupõrge toimub.",
  ];
  document.querySelector("#teinefakt").addEventListener("click", () => {document.querySelector("#fakt").innerHTML = faktid[Math.floor(Math.random() * faktid.length)]})
</script>

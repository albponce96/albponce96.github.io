---
title: "Consultoría"
url: "/consultancy/"
summary: "Experiencia en consultoría"
---

He desarrollado consultorías especializadas en mecanismos financieros para la
conservación, valoración económica de servicios ecosistémicos, sistemas de
monitoreo (MRV) e investigación de mercados.

<div class="research-controls" id="consultancy-controls">
<input id="consultancy-search" type="search" placeholder="🔍 Buscar por institución, rol o tema…" autocomplete="off" aria-label="Buscar consultorías">
<div class="research-topics">
<button type="button" class="kw kw-chip kw--all active" data-kw="all">Todas</button>
<button type="button" class="kw kw-chip kw--fin" data-kw="mecanismos-financieros">Mecanismos financieros</button>
<button type="button" class="kw kw-chip kw--merese" data-kw="merese">MERESE</button>
<button type="button" class="kw kw-chip kw--cons" data-kw="conservacion">Conservación</button>
<button type="button" class="kw kw-chip kw--areas" data-kw="areas-protegidas">Áreas protegidas</button>
<button type="button" class="kw kw-chip kw--mrv" data-kw="mrv">MRV</button>
<button type="button" class="kw kw-chip kw--val" data-kw="valoracion-economica">Valoración económica</button>
<button type="button" class="kw kw-chip kw--merc" data-kw="investigacion-mercados">Investigación de mercados</button>
<button type="button" class="kw kw-chip kw--gob" data-kw="gobernanza">Gobernanza</button>
<button type="button" class="kw kw-chip kw--estr" data-kw="estrategia">Estrategia</button>
</div>
</div>

<p class="research-count" id="consultancy-count"></p>

<div class="cons-grid" id="consultancies">
<div class="cons-card" data-kw="mecanismos-financieros merese conservacion areas-protegidas">
<div class="cons-head"><span class="cons-org">Profonanpe</span><span class="cons-date">jul – set 2026</span></div>
<div class="cons-role">Consultor de Proyecto</div>
<p class="cons-desc">Desarrollo de una hoja de ruta para la implementación de Mecanismos de Retribución por Servicios Ecosistémicos en las ACR Champará-Coyllorccocha (Áncash) y Selva Verde-Santo Domingo (Puno).</p>
<div class="cons-tags"><span class="kw kw--fin" data-kw="mecanismos-financieros">Mecanismos financieros</span><span class="kw kw--merese" data-kw="merese">MERESE</span><span class="kw kw--cons" data-kw="conservacion">Conservación</span><span class="kw kw--areas" data-kw="areas-protegidas">Áreas protegidas</span></div>
</div>
<div class="cons-card" data-kw="merese valoracion-economica mrv conservacion">
<div class="cons-head"><span class="cons-org">Pronaturaleza</span><span class="cons-date">dic 2025 – may 2026</span></div>
<div class="cons-role">Consultor de Proyecto</div>
<p class="cons-desc">Lideré el diagnóstico socioeconómico, la valoración económica y la estrategia de financiamiento de servicios ecosistémicos; diseñé el modelo de gobernanza y formulé el sistema de Monitoreo, Reporte y Verificación (MRV), con su teoría de cambio y matriz de indicadores.</p>
<div class="cons-tags"><span class="kw kw--merese" data-kw="merese">MERESE</span><span class="kw kw--val" data-kw="valoracion-economica">Valoración económica</span><span class="kw kw--mrv" data-kw="mrv">MRV</span><span class="kw kw--cons" data-kw="conservacion">Conservación</span></div>
</div>
<div class="cons-card" data-kw="investigacion-mercados estrategia">
<div class="cons-head"><span class="cons-org">Advantage LATAM Insights</span><span class="cons-date">oct – dic 2025</span></div>
<div class="cons-role">Consultor en Investigación de Mercados</div>
<p class="cons-desc"><strong>Competitividad y estrategia de mercados.</strong> Elaboré recomendaciones estratégicas para una agencia gubernamental de Corea del Sur, basadas en un análisis de competitividad, segmentación y <em>drivers</em> de mercado en Reino Unido y Alemania.</p>
<div class="cons-tags"><span class="kw kw--merc" data-kw="investigacion-mercados">Investigación de mercados</span><span class="kw kw--estr" data-kw="estrategia">Estrategia</span></div>
</div>
<div class="cons-card" data-kw="gobernanza areas-protegidas conservacion">
<div class="cons-head"><span class="cons-org">Graglia Consulting Group</span><span class="cons-date">set – dic 2022</span></div>
<div class="cons-role">Analista Técnico</div>
<p class="cons-desc"><strong>Gobernanza participativa en las ANP PN Río Abiseo y RC Amarakaeri.</strong> Diseñé propuestas técnicas para fortalecer la gobernanza y la gestión participativa en dos áreas protegidas de la Amazonía peruana, articulando instrumentos de gestión y estrategias comerciales en coordinación con la UICN.</p>
<div class="cons-tags"><span class="kw kw--gob" data-kw="gobernanza">Gobernanza</span><span class="kw kw--areas" data-kw="areas-protegidas">Áreas protegidas</span><span class="kw kw--cons" data-kw="conservacion">Conservación</span></div>
</div>
</div>

<p class="research-empty" id="consultancy-empty" hidden>No se encontraron consultorías con esos criterios. <a href="#" id="consultancy-reset">Ver todas →</a></p>

<script>
(function () {
  var search = document.getElementById('consultancy-search');
  var chips = document.querySelectorAll('#consultancy-controls .kw-chip');
  var cards = document.querySelectorAll('#consultancies .cons-card');
  var countEl = document.getElementById('consultancy-count');
  var emptyEl = document.getElementById('consultancy-empty');
  var resetLink = document.getElementById('consultancy-reset');
  var total = cards.length;
  var activeKw = 'all';

  function setActiveChip(kw) {
    for (var i = 0; i < chips.length; i++) {
      chips[i].classList.toggle('active', chips[i].getAttribute('data-kw') === kw);
    }
  }

  function apply() {
    var q = (search && search.value ? search.value : '').trim().toLowerCase();
    var visible = 0;
    cards.forEach(function (card) {
      var kws = (card.getAttribute('data-kw') || '').split(' ');
      var okKw = activeKw === 'all' || kws.indexOf(activeKw) !== -1;
      var okText = !q || card.textContent.toLowerCase().indexOf(q) !== -1;
      var show = okKw && okText;
      card.style.display = show ? '' : 'none';
      if (show) visible++;
    });
    countEl.textContent = (visible === total)
      ? total + ' consultorías'
      : visible + ' de ' + total + ' consultorías';
    emptyEl.hidden = visible !== 0;
  }

  function filterByKw(kw) {
    activeKw = kw;
    setActiveChip(kw);
    apply();
  }

  for (var i = 0; i < chips.length; i++) {
    (function (chip) {
      chip.addEventListener('click', function () { filterByKw(chip.getAttribute('data-kw')); });
    })(chips[i]);
  }

  document.querySelectorAll('#consultancies .cons-tags .kw').forEach(function (tag) {
    tag.style.cursor = 'pointer';
    tag.addEventListener('click', function () {
      filterByKw(tag.getAttribute('data-kw'));
      var anchor = document.getElementById('consultancy-controls');
      if (anchor && anchor.scrollIntoView) anchor.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });

  if (search) search.addEventListener('input', apply);
  if (resetLink) resetLink.addEventListener('click', function (e) {
    e.preventDefault();
    if (search) search.value = '';
    filterByKw('all');
  });

  apply();
})();
</script>

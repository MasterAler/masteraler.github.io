---
layout: default
title: Portfolio
active_page: portfolio
---

<style>
/* ── Portfolio terminal log ── */
#pf {
  --green:  #b5e853;
  --cyan:   #63c0f5;
  --orange: #f0a500;
  --dim:    #555;
  --dimmer: #333;
  --text:   #ccc;
  --bg-hl:  rgba(181, 232, 83, 0.04);
  --border-hl: #b5e853;
}

.pf-cmd {
  font-size: 15px;
  margin-bottom: 4px;
  opacity: 0;
  animation: pf-in 0.35s ease 0.1s forwards;
}
.pf-cmd .u  { color: var(--green); }
.pf-cmd .sep { color: #666; }
.pf-cmd .p  { color: var(--cyan); }
.pf-cmd .dl { color: #666; margin: 0 4px; }
.pf-cmd .c  { color: #ddd; }

.pf-hint {
  color: var(--dimmer);
  font-size: 12px;
  margin: 6px 0 22px;
  opacity: 0;
  animation: pf-in 0.35s ease 0.3s forwards;
}

/* ── entries ── */
.pf-entry {
  border-left: 2px solid transparent;
  padding: 7px 2px 7px 14px;
  cursor: pointer;
  margin-bottom: 1px;
  transition: border-color 0.15s, background 0.15s;
  opacity: 0;
  animation: pf-in 0.4s ease forwards;
}
.pf-entry:hover { background: var(--bg-hl); border-left-color: var(--dimmer); }
.pf-entry.open  { background: var(--bg-hl); border-left-color: var(--border-hl); }

.pf-entry:nth-child(1)  { animation-delay: 0.35s; }
.pf-entry:nth-child(2)  { animation-delay: 0.47s; }
.pf-entry:nth-child(3)  { animation-delay: 0.59s; }
.pf-entry:nth-child(4)  { animation-delay: 0.71s; }
.pf-entry:nth-child(5)  { animation-delay: 0.83s; }
.pf-entry:nth-child(6)  { animation-delay: 0.95s; }
.pf-entry:nth-child(7)  { animation-delay: 1.07s; }
.pf-entry:nth-child(8)  { animation-delay: 1.19s; }
.pf-entry:nth-child(9)  { animation-delay: 1.31s; }
.pf-entry:nth-child(10) { animation-delay: 1.43s; }
.pf-entry:nth-child(11) { animation-delay: 1.55s; }
.pf-entry:nth-child(12) { animation-delay: 1.67s; }

.pf-row {
  display: flex;
  flex-wrap: wrap;
  align-items: baseline;
  gap: 10px;
  font-size: 15px;
  line-height: 1.5;
}
.pf-hash { color: var(--orange); font-size: 13px; flex-shrink: 0; }
.pf-msg  { color: #ddd; flex: 1; min-width: 180px; }
.pf-msg em { color: var(--green); font-style: normal; font-weight: 600; }
.pf-date { color: var(--dim); font-size: 13px; flex-shrink: 0; }

/* ── expanded detail ── */
.pf-detail {
  display: none;
  margin-top: 10px;
  padding-top: 12px;
  border-top: 1px dashed rgba(99, 192, 245, 0.15);
}
.pf-detail.show {
  display: block;
  animation: pf-fade 0.2s ease;
}

.pf-dhdr {
  color: var(--dim);
  font-size: 12px;
  margin-bottom: 10px;
  line-height: 1.7;
}
.pf-dhdr .full-hash { color: var(--orange); }

.pf-desc {
  color: #b0b0b0;
  font-size: 14px;
  line-height: 1.85;
  white-space: pre-line;
  margin-bottom: 12px;
}

.pf-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-bottom: 10px;
}
.pf-tag {
  border: 1px solid rgba(181, 232, 83, 0.3);
  background: rgba(181, 232, 83, 0.06);
  color: var(--green);
  padding: 1px 9px;
  font-size: 11px;
  border-radius: 2px;
  letter-spacing: 0.04em;
}

.pf-link {
  display: inline-block;
  color: var(--cyan);
  font-size: 13px;
  text-decoration: none;
  opacity: 0.85;
}
.pf-link::before { content: '↗ '; }
.pf-link:hover { color: var(--green); opacity: 1; }

/* ── footer ── */
.pf-footer {
  margin-top: 32px;
  padding-top: 14px;
  border-top: 1px dashed rgba(181, 232, 83, 0.18);
  font-size: 13px;
  color: var(--dim);
  opacity: 0;
  animation: pf-in 0.4s ease 1.7s forwards;
}
.pf-footer a { color: var(--cyan); text-decoration: none; }
.pf-footer a:hover { color: var(--green); }

@keyframes pf-in {
  from { opacity: 0; transform: translateX(-7px); }
  to   { opacity: 1; transform: none; }
}
@keyframes pf-fade {
  from { opacity: 0; }
  to   { opacity: 1; }
}
</style>

<div id="pf">

<div class="pf-cmd">
  <span class="u">masteraler</span><span class="sep">@</span><span class="u">home</span><span class="sep">:</span><span class="p">~/side-projects</span><span class="dl">$</span><span class="c"> git log --oneline .</span>
</div>

<div class="pf-hint"># click any commit to expand</div>

<div id="pf-log">

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">a3f2c89</span>
      <span class="pf-msg"><em>ivl-display</em>: embedded display client for ICU ventilator (ARM)</span>
      <span class="pf-date">2024-11</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">a3f2c894b1e72d91cc0f3a8b5d4e6f2a9c1b0e37</span><br>
Date:   Nov 2024</div>
      <div class="pf-desc">Intensive Care Unit ventilator — embedded display module (freelance).

Thick client running on ARM hardware for medical ventilators
and anesthesia machines. Display interface, system control,
calculation subsystems, and clinical decision support — the screen
you actually see when you turn the device on.

Low-level board-to-board protocol work over serial, plus debugging
of the computational components. Built with a 3-person freelance
team alongside the manufacturer's in-house engineers.</div>
      <div class="pf-tags">
        <span class="pf-tag">C++</span>
        <span class="pf-tag">Qt / QML</span>
        <span class="pf-tag">Boost</span>
        <span class="pf-tag">ARM / Embedded</span>
        <span class="pf-tag">Serial Protocol</span>
        <span class="pf-tag">Medical</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">c5e8b41</span>
      <span class="pf-msg"><em>etl-probator</em>: control software for high-voltage circuit probation lab</span>
      <span class="pf-date">2023-10</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">c5e8b41a4d3f7e92b6c0a5d8f1e3b9c4a7d2f5e6</span><br>
Date:   Oct 2023</div>
      <div class="pf-desc">ETL Probator — onboard control software for an Energoskan
high-voltage circuit probation laboratory ("On-board computer laboratory").

Qt Widgets GUI speaking Modbus RTU over serial to the lab's hardware
controller: drives configurable test schemes with per-scheme I/O bit
patterns, polls indication blocks (voltage, current, GND / work-GND,
door interlocks, emergency button), and runs auto / manual command
modes with full event logging.

Each probation scheme ships with its own schematic and operator hints
loaded from disk, so adding a new test is a config + image drop-in.</div>
      <div class="pf-tags">
        <span class="pf-tag">C++</span>
        <span class="pf-tag">Qt Widgets</span>
        <span class="pf-tag">Modbus RTU</span>
        <span class="pf-tag">Serial</span>
        <span class="pf-tag">Industrial</span>
        <span class="pf-tag">High Voltage</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">7b91d4e</span>
      <span class="pf-msg"><em>ovida</em>: video coaching platform backend</span>
      <span class="pf-date">2022-09</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">7b91d4e2a6c83f410b9d5e71c2a8f3b4e9d1c6f2</span><br>
Date:   Sep 2022</div>
      <div class="pf-desc">Ovida — backend for a professional video coaching platform.

Year-long build supporting video calls, personal dashboards,
and post-session analysis: dual-stream synchronized recording,
speech-to-text transcription with highlight detection (open questions,
significant pauses, verbal patterns), and video-stream analysis
of facial expressions and eye movements.

Python microservices over Kafka, FastAPI endpoints, S3 storage,
NLP pipelines on top. International team across frontend, data
science, and DevOps.</div>
      <div class="pf-tags">
        <span class="pf-tag">Python</span>
        <span class="pf-tag">FastAPI</span>
        <span class="pf-tag">Kafka</span>
        <span class="pf-tag">Docker</span>
        <span class="pf-tag">Kubernetes</span>
        <span class="pf-tag">NLP / S3</span>
      </div>
      <a class="pf-link" href="https://ovida.io/" target="_blank" rel="noopener">ovida.io</a>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">e2a7d51</span>
      <span class="pf-msg"><em>stock-optimizer</em>: trader-assistance portfolio constructor</span>
      <span class="pf-date">2021-03</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">e2a7d514c98a3f6b0d1e8c5b2f9a4d7e3b6c0a85</span><br>
Date:   Mar 2021</div>
      <div class="pf-desc">Stock Optimizer — Streamlit app for equity portfolio construction.

Four optimization strategies — minimum correlation, expected-return
maximization, Sharpe ratio, and equal weights — expressed as
quadratic and linear programs over cvxopt / OSQP solvers.

Filtering by RSI, region, and sector; per-stock whitelist and
blacklist with hard-pinned weights; resulting allocation visualised
as Plotly breakdowns by sector and region.</div>
      <div class="pf-tags">
        <span class="pf-tag">Python</span>
        <span class="pf-tag">Streamlit</span>
        <span class="pf-tag">cvxopt / OSQP</span>
        <span class="pf-tag">Pandas / NumPy</span>
        <span class="pf-tag">Quant Finance</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">4b9c8f3</span>
      <span class="pf-msg"><em>penenza</em>: web scraper for penenza.ru financial marketplace</span>
      <span class="pf-date">2019-04</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">4b9c8f37e5a2d106f4b8c1e9d3a7b5c2f0e8d4a6</span><br>
Date:   Apr 2019</div>
      <div class="pf-desc">penenza — Python 3 module automating data retrieval from
the penenza.ru tender / financial marketplace.

Lightweight scraper package built on BeautifulSoup and Requests,
packaged with setuptools and covered by nose tests.</div>
      <div class="pf-tags">
        <span class="pf-tag">Python 3</span>
        <span class="pf-tag">BeautifulSoup</span>
        <span class="pf-tag">Requests</span>
        <span class="pf-tag">Web Scraping</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">3f7a1c0</span>
      <span class="pf-msg"><em>dark-and-light</em>: corporate website</span>
      <span class="pf-date">2017-09</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">3f7a1c048d9e2b5a6c1f4e7d3b0a8c2e5f9d1b4a</span><br>
Date:   Sep 2017</div>
      <div class="pf-desc">Dark & Light — site + identity for a wholesale petroleum
products company.

Logo and corporate identity (business cards, brochures), WordPress
site build, and a set of branded signs cut on a plotter — full
design pass from print to web.</div>
      <div class="pf-tags">
        <span class="pf-tag">WordPress</span>
        <span class="pf-tag">Web</span>
        <span class="pf-tag">Logo / Identity</span>
        <span class="pf-tag">Print Design</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">6f3e1d8</span>
      <span class="pf-msg"><em>isan-calculator</em>: web-scheduled scientific calculation service</span>
      <span class="pf-date">2015-10</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">6f3e1d82a4c7b9e0d5f2c8a1b3e6d4f0a9c2e7b5</span><br>
Date:   Oct 2015</div>
      <div class="pf-desc">ISAN Calculator — web service for queued 2D PGI scientific computations.

PHP frontend lets researchers upload configs and schedule jobs;
a Linux daemon (CentOS) puts them on a ZMQ queue and dispatches
to an extensible Python task runner. Reports are generated on
completion and delivered by email.</div>
      <div class="pf-tags">
        <span class="pf-tag">PHP</span>
        <span class="pf-tag">Python</span>
        <span class="pf-tag">ZMQ</span>
        <span class="pf-tag">Linux Daemon</span>
        <span class="pf-tag">Task Queue</span>
        <span class="pf-tag">Scientific</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">9e4d3b7</span>
      <span class="pf-msg"><em>spectrtool</em>: signal spectrum processing utility</span>
      <span class="pf-date">2013-06</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">9e4d3b71f2a6c8d4e0b3f5a7c2d9e1b4f6a3c8e2</span><br>
Date:   Jun 2013</div>
      <div class="pf-desc">SpectrTool — desktop utility for spectral data analysis and processing.

Visualization and processing of signal spectra; supports common
spectrum formats. Built for technical and scientific use cases.</div>
      <div class="pf-tags">
        <span class="pf-tag">Delphi</span>
        <span class="pf-tag">Signal Processing</span>
        <span class="pf-tag">Scientific</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">2c8f1a6</span>
      <span class="pf-msg"><em>shoecurve-editor</em>: CAD viewer for shoe last models</span>
      <span class="pf-date">2012-07</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">2c8f1a673d4b9e21f5c7a3d8b2e4f6a1c9d3e5b7</span><br>
Date:   Jul 2012</div>
      <div class="pf-desc">ShoeCurve Editor — desktop CAD module for shoe last models.

Standalone viewer for 3D shoe lasts with arbitrary cross-section
and projection output, rotate/move controls, format conversion,
plus a handful of minor editing tools.</div>
      <div class="pf-tags">
        <span class="pf-tag">C#</span>
        <span class="pf-tag">WPF</span>
        <span class="pf-tag">.NET</span>
        <span class="pf-tag">CAD</span>
        <span class="pf-tag">3D Viewer</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">d6b2e9a</span>
      <span class="pf-msg"><em>vizitka-editor</em>: in-browser business card editor (Java applet)</span>
      <span class="pf-date">—</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">d6b2e9a4f1c7d3e8b0a5c2f4e9d1b6c8a3f7e2d0</span></div>
      <div class="pf-desc">Business Cards Editor — embedded Java Swing applet for sketching
business cards in the browser.

Users draw from scratch or edit existing templates; the template
library is decoupled from the code and loaded from an XML config,
so new layouts drop in without a rebuild. </div>
      <div class="pf-tags">
        <span class="pf-tag">Java</span>
        <span class="pf-tag">Swing</span>
        <span class="pf-tag">Applet</span>
        <span class="pf-tag">XML Templates</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">8e5c4d1</span>
      <span class="pf-msg"><em>amateur-forum</em>: community discussion platform</span>
      <span class="pf-date">—</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">8e5c4d13a7f2b9e6c0d4a1f8b3e7c5d2a9f0b6e4</span></div>
      <div class="pf-desc">CoverDuck — web-based community discussion board.

Threaded discussion platform with user accounts,
moderation tooling, and topic categorization.</div>
      <div class="pf-tags">
        <span class="pf-tag">Web</span>
        <span class="pf-tag">PHP</span>
        <span class="pf-tag">MySQL</span>
        <span class="pf-tag">phpBB</span>
      </div>
    </div>
  </div>

  <div class="pf-entry" onclick="pfToggle(this)">
    <div class="pf-row">
      <span class="pf-hash">5a1f8c2</span>
      <span class="pf-msg"><em>magic-lottery</em>: event roulette application</span>
      <span class="pf-date">—</span>
    </div>
    <div class="pf-detail">
      <div class="pf-dhdr">commit <span class="full-hash">5a1f8c27e3d4b9c1a6f2e8d0c5b7a3e9f1d4c6b8</span></div>
      <div class="pf-desc">Magic Lottery Roulette — animated draw application for live events.

Randomized prize draw mechanics with a spinning roulette wheel UI.
Designed for on-screen display during corporate or public events.</div>
      <div class="pf-tags">
        <span class="pf-tag">Delphi</span>
        <span class="pf-tag">Animation</span>
        <span class="pf-tag">Desktop</span>
      </div>
    </div>
  </div>

</div>

<div class="pf-footer">
  12 commits · full portfolio at <a href="https://freelance.ru/portfolio/user/MasterAler" target="_blank" rel="noopener">freelance.ru/MasterAler ↗</a>
</div>

</div>

<script>
function pfToggle(el) {
  var detail = el.querySelector('.pf-detail');
  var wasOpen = el.classList.contains('open');
  document.querySelectorAll('#pf-log .pf-entry.open').forEach(function(e) {
    e.classList.remove('open');
    e.querySelector('.pf-detail').classList.remove('show');
  });
  if (!wasOpen) {
    el.classList.add('open');
    detail.classList.add('show');
  }
}
</script>

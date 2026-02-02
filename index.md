---
layout: default
title: Dashboard
---

<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-label">Total Portfolio Value</span>
    <span class="stat-value" id="total-value">Loading...</span>
  </div>

  <div class="stat-card">
    <span class="stat-label">Total Cost Basis</span>
    <span class="stat-value" id="total-cost">Loading...</span>
  </div>

  <div class="stat-card">
    <span class="stat-label">Unrealized Gain/Loss</span>
    <span class="stat-value" id="total-gain">Loading...</span>
  </div>

  <div class="stat-card">
    <span class="stat-label">Portfolio IRR</span>
    <span class="stat-value" id="portfolio-irr">Loading...</span>
  </div>
</div>

<div class="card" style="margin-bottom: 1.5rem;">
  <h2 class="card-title">Gains Summary</h2>
  <div class="gains-summary">
    <div class="gains-summary-item">
      <span class="gains-summary-label">Realized Gains</span>
      <span class="gains-summary-value" id="realized-gain">Loading...</span>
    </div>
    <div class="gains-summary-item">
      <span class="gains-summary-label">Unrealized Gains</span>
      <span class="gains-summary-value" id="unrealized-gain">Loading...</span>
    </div>
    <div class="gains-summary-item">
      <span class="gains-summary-label">Total Gains</span>
      <span class="gains-summary-value" id="total-gain-all">Loading...</span>
    </div>
  </div>
</div>

<div class="charts-grid">
  <div class="card">
    <h2 class="card-title">Top Gainers</h2>
    <div id="top-gainers" class="loading">Loading...</div>
  </div>

  <div class="card">
    <h2 class="card-title">Smallest Gains</h2>
    <div id="top-losers" class="loading">Loading...</div>
  </div>
</div>

<div class="card">
  <h2 class="card-title">Category Breakdown</h2>
  <div id="category-breakdown" class="loading">Loading...</div>
</div>

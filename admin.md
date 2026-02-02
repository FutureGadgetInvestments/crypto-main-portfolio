---
layout: default
title: Admin
description: Manage your portfolio data
---

<header class="page-header">
  <h1 class="page-title">Admin</h1>
  <p class="page-description">Manage your portfolio data and view instructions</p>
</header>

<div class="stats-grid">
  <a href="https://docs.google.com/spreadsheets/d/1ixld4bbNNXkF3b9kaXjoIZ5Aq6bV2m_HXL70A_cZ40M/edit?usp=sharing" target="_blank" class="stat-card admin-link">
    <span class="stat-label">Edit Data</span>
    <span class="stat-value" style="font-size: 1.25rem;">Open Google Sheets</span>
    <small style="color: var(--color-gray-500);">Add, edit, or remove positions</small>
  </a>

  <a href="https://docs.google.com/spreadsheets/d/e/2PACX-1vQdW4--3KMPl6vSJGFY4BdzNxJgbZFMPnfGYSqS7AEox19YzmYQGo5wvKHupYOS1vTO2J6F6oksqzry/pubhtml" target="_blank" class="stat-card admin-link">
    <span class="stat-label">View Only</span>
    <span class="stat-value" style="font-size: 1.25rem;">Published Sheet</span>
    <small style="color: var(--color-gray-500);">Share this link with others</small>
  </a>
</div>

<div class="card" style="margin-bottom: 1.5rem;">
  <h2 class="card-title">Opening a New Position</h2>
  <p style="color: var(--color-gray-600); margin-bottom: 1rem;">When you open a new position, update <strong>2 sheets</strong>:</p>

  <div class="admin-section">
    <h3 style="font-size: 1rem; margin-bottom: 0.5rem;">1. Holdings Sheet</h3>
    <p style="color: var(--color-gray-600); font-size: 0.875rem;">Add a new row with:</p>
    <ul style="color: var(--color-gray-600); font-size: 0.875rem; margin-left: 1.5rem;">
      <li><strong>id</strong> - Unique identifier (lowercase, hyphenated) e.g. <code>yousd-base</code></li>
      <li><strong>name</strong> - Display name e.g. <code>yoUSD</code></li>
      <li><strong>category</strong> - Position category e.g. <code>PENDLE</code></li>
      <li><strong>network</strong> - Blockchain network e.g. <code>Base</code></li>
      <li><strong>date_acquired</strong> - Date opened (MM/DD/YYYY)</li>
      <li><strong>cost_basis</strong> - Amount deposited (number only)</li>
      <li><strong>current_value</strong> - Current value (update periodically)</li>
      <li><strong>last_checked_date</strong> - When you last updated current_value</li>
      <li><strong>status</strong> - Set to <code>open</code></li>
      <li><strong>notes</strong> - Any relevant notes e.g. expiry date</li>
    </ul>
  </div>

  <div class="admin-section" style="margin-top: 1rem;">
    <h3 style="font-size: 1rem; margin-bottom: 0.5rem;">2. Transactions Sheet</h3>
    <p style="color: var(--color-gray-600); font-size: 0.875rem;">Add a <strong>Deposit</strong> entry:</p>
    <ul style="color: var(--color-gray-600); font-size: 0.875rem; margin-left: 1.5rem;">
      <li><strong>date</strong> - Date of deposit (MM/DD/YYYY)</li>
      <li><strong>amount</strong> - Negative number (money going out) e.g. <code>-2500</code></li>
      <li><strong>type</strong> - <code>Deposit</code></li>
      <li><strong>notes</strong> - Description of the deposit</li>
    </ul>
  </div>
</div>

<div class="card" style="margin-bottom: 1.5rem;">
  <h2 class="card-title">Closing a Position (Selling)</h2>
  <p style="color: var(--color-gray-600); margin-bottom: 1rem;">When you close/sell a position, update <strong>3 sheets</strong>:</p>

  <div class="admin-section">
    <h3 style="font-size: 1rem; margin-bottom: 0.5rem;">1. Holdings Sheet</h3>
    <p style="color: var(--color-gray-600); font-size: 0.875rem;">Find the position row and change:</p>
    <ul style="color: var(--color-gray-600); font-size: 0.875rem; margin-left: 1.5rem;">
      <li><strong>status</strong> - Change from <code>open</code> to <code>closed</code></li>
      <li><strong>current_value</strong> - Update to final value (optional)</li>
      <li><strong>last_checked_date</strong> - Update to sale date</li>
    </ul>
  </div>

  <div class="admin-section" style="margin-top: 1rem;">
    <h3 style="font-size: 1rem; margin-bottom: 0.5rem;">2. Sales Sheet</h3>
    <p style="color: var(--color-gray-600); font-size: 0.875rem;">Add a new row with:</p>
    <ul style="color: var(--color-gray-600); font-size: 0.875rem; margin-left: 1.5rem;">
      <li><strong>id</strong> - Identifier for this sale e.g. <code>yousd-base-sale-1</code></li>
      <li><strong>date</strong> - Date of sale (MM/DD/YYYY)</li>
      <li><strong>cost_basis</strong> - Original cost basis</li>
      <li><strong>sale_price</strong> - Amount received from sale</li>
      <li><strong>notes</strong> - Any relevant notes</li>
    </ul>
  </div>

  <div class="admin-section" style="margin-top: 1rem;">
    <h3 style="font-size: 1rem; margin-bottom: 0.5rem;">3. Transactions Sheet</h3>
    <p style="color: var(--color-gray-600); font-size: 0.875rem;">Add a <strong>Withdrawal</strong> entry:</p>
    <ul style="color: var(--color-gray-600); font-size: 0.875rem; margin-left: 1.5rem;">
      <li><strong>date</strong> - Date of sale (MM/DD/YYYY)</li>
      <li><strong>amount</strong> - Positive number (money coming in) e.g. <code>2600</code></li>
      <li><strong>type</strong> - <code>Withdrawal</code></li>
      <li><strong>notes</strong> - Description of the withdrawal</li>
    </ul>
  </div>
</div>

<div class="card">
  <h2 class="card-title">Why All Three Updates Matter</h2>
  <div style="color: var(--color-gray-600); line-height: 1.7;">
    <ul style="margin-left: 1.5rem;">
      <li><strong>Holdings</strong> - Tracks what you hold/held and maintains historical record</li>
      <li><strong>Sales</strong> - Calculates realized gains (sale_price - cost_basis)</li>
      <li><strong>Transactions</strong> - Powers IRR calculation (tracks all cash flowing in and out)</li>
    </ul>
    <p style="margin-top: 1rem;">
      <strong>Important:</strong> If you skip the Withdrawal transaction when selling, your IRR will be incorrect
      because it won't know money came back to you.
    </p>
  </div>
</div>

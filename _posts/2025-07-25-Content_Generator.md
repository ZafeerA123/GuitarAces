---
layout: post
title: Video Script UI 💡
description: Interactive UI for Generating Scripts
type: post
comments: false
permalink: Generator
categories: [Final Project]
---


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GuitarAces Content Generator</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>

<style>
  /* Base styles with deep purple music theme */
  * {
    box-sizing: border-box;
  }
  
  body {
    margin: 0;
    padding: 0;
    font-family: 'Inter', sans-serif;
    color: #fff;
    overflow-x: hidden;
    min-height: 100vh;
  }
  
  /* Dynamic gradient background with music wave animation */
  .page-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, #1a0b3d, #2d1b69, #4c2a85);
    z-index: -3;
  }
  
  /* Animated sound wave overlay */
  .wave-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: 
      radial-gradient(ellipse at 80% 10%, rgba(147, 51, 234, 0.15), transparent 50%),
      radial-gradient(ellipse at 20% 90%, rgba(168, 85, 247, 0.2), transparent 50%),
      radial-gradient(ellipse at 50% 50%, rgba(196, 181, 253, 0.1), transparent 60%);
    animation: waveFlow 15s infinite alternate;
    z-index: -2;
  }
  
  @keyframes waveFlow {
    0% { 
      background-position: 0% 0%, 100% 100%, 50% 50%;
      transform: rotate(0deg) scale(1);
    }
    50% {
      background-position: 50% 50%, 50% 50%, 25% 75%;
      transform: rotate(1deg) scale(1.02);
    }
    100% { 
      background-position: 100% 100%, 0% 0%, 75% 25%;
      transform: rotate(-1deg) scale(0.98);
    }
  }
  
  /* Main container */
  .main-container {
    position: relative;
    padding: 60px 20px;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    z-index: 1;
  }
  
  /* Floating music notes */
  .music-notes {
    position: fixed;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
  }
  
  .music-note {
    position: absolute;
    color: rgba(147, 51, 234, 0.4);
    font-size: 24px;
    animation: musicFloat 8s infinite ease-in-out;
  }
  
  @keyframes musicFloat {
    0%, 100% { 
      transform: translateY(0px) rotate(0deg) scale(1);
      opacity: 0.4;
    }
    25% {
      transform: translateY(-40px) rotate(5deg) scale(1.1);
      opacity: 0.6;
    }
    50% { 
      transform: translateY(-80px) rotate(-3deg) scale(0.9);
      opacity: 0.8;
    }
    75% {
      transform: translateY(-40px) rotate(7deg) scale(1.05);
      opacity: 0.5;
    }
  }
  
  .music-note:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
  .music-note:nth-child(2) { top: 40%; left: 85%; animation-delay: 2s; font-size: 32px; }
  .music-note:nth-child(3) { top: 70%; left: 15%; animation-delay: 4s; font-size: 20px; }
  .music-note:nth-child(4) { top: 15%; left: 70%; animation-delay: 1s; font-size: 28px; }
  .music-note:nth-child(5) { top: 80%; left: 80%; animation-delay: 3s; }
  .music-note:nth-child(6) { top: 35%; left: 5%; animation-delay: 5s; font-size: 26px; }
  
  /* Title styling */
  h1 {
    font-size: 3.5rem;
    font-weight: 800;
    margin-bottom: 40px;
    text-align: center;
    background: linear-gradient(135deg, #c4b5fd, #a855f7, #7c3aed, #6d28d9);
    background-size: 300% auto;
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: gradientShift 4s linear infinite, fadeInUp 1s ease-out both;
    line-height: 1.1;
    text-shadow: 0 0 30px rgba(168, 85, 247, 0.5);
  }
  
  @keyframes gradientShift {
    0% { background-position: 0% center; }
    100% { background-position: 300% center; }
  }
  
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  /* Glass card styling */
  .glass-card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border-radius: 24px;
    overflow: hidden;
    box-shadow: 
      0 20px 40px rgba(0, 0, 0, 0.3), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.1),
      0 0 0 1px rgba(147, 51, 234, 0.2);
    padding: 40px;
    width: 100%;
    max-width: 500px;
    text-align: center;
    transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    position: relative;
    animation: cardFloat 8s infinite ease-in-out, fadeInUp 1s ease-out 0.3s both;
    margin-bottom: 40px;
  }
  
  @keyframes cardFloat {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    25% { transform: translateY(-10px) rotate(0.5deg); }
    50% { transform: translateY(-5px) rotate(0deg); }
    75% { transform: translateY(-15px) rotate(-0.5deg); }
  }
  
  .glass-card:hover {
    transform: translateY(-10px) scale(1.02);
    background: rgba(255, 255, 255, 0.08);
    box-shadow: 
      0 30px 60px rgba(0, 0, 0, 0.4), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.12),
      0 0 40px rgba(147, 51, 234, 0.3);
  }
  
  /* Input styling */
  input {
    width: 100%;
    padding: 16px 20px;
    margin-bottom: 24px;
    font-size: 1.1rem;
    border-radius: 16px;
    border: 2px solid rgba(147, 51, 234, 0.3);
    background: rgba(255, 255, 255, 0.08);
    color: #fff;
    outline: none;
    transition: all 0.4s ease;
    backdrop-filter: blur(10px);
    font-family: 'Inter', sans-serif;
  }
  
  input::placeholder {
    color: rgba(255, 255, 255, 0.6);
  }
  
  input:focus {
    border-color: #a855f7;
    background: rgba(255, 255, 255, 0.12);
    box-shadow: 0 0 20px rgba(168, 85, 247, 0.3);
    transform: scale(1.02);
  }
  
  /* Button styling */
  .submit-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    width: 100%;
    padding: 16px 32px;
    border-radius: 16px;
    font-weight: 700;
    font-size: 1.1rem;
    border: none;
    background: linear-gradient(135deg, #a855f7, #7c3aed, #6d28d9);
    color: #fff;
    cursor: pointer;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    position: relative;
    overflow: hidden;
    box-shadow: 0 8px 32px rgba(168, 85, 247, 0.4);
    animation: buttonGlow 3s infinite alternate;
    font-family: 'Inter', sans-serif;
  }
  
  @keyframes buttonGlow {
    0% { 
      box-shadow: 0 8px 32px rgba(168, 85, 247, 0.4), 0 0 20px rgba(168, 85, 247, 0.2);
    }
    100% { 
      box-shadow: 0 12px 40px rgba(168, 85, 247, 0.6), 0 0 30px rgba(168, 85, 247, 0.4);
    }
  }
  
  .submit-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: all 0.6s ease;
    z-index: 1;
  }
  
  .submit-btn:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0 16px 48px rgba(168, 85, 247, 0.6);
  }
  
  .submit-btn:hover::before {
    left: 100%;
  }
  
  .submit-btn:active {
    transform: translateY(-2px) scale(1.02);
  }
  
  .submit-btn:disabled {
    opacity: 0.7;
    cursor: not-allowed;
    transform: none;
  }
  
  /* Loader styling */
  .loader {
    border: 3px solid rgba(255, 255, 255, 0.3);
    border-top: 3px solid #fff;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    animation: spin 1s linear infinite;
    display: inline-block;
    margin-left: 8px;
  }
  
  @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }
  
  /* Result card styling */
  .card-result {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border-radius: 24px;
    box-shadow: 
      0 20px 40px rgba(0, 0, 0, 0.3), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.1),
      0 0 0 1px rgba(147, 51, 234, 0.2);
    padding: 40px;
    width: 100%;
    max-width: 600px;
    margin: 20px 0;
    animation: fadeInUp 0.8s ease-out both;
    position: relative;
  }
  
  .card-result h2 {
    color: #c4b5fd;
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 20px;
    text-shadow: 0 2px 8px rgba(147, 51, 234, 0.5);
  }
  
  .card-result p {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.6;
    margin-bottom: 16px;
    font-size: 1.1rem;
  }
  
  .card-result a {
    color: #00ffe7;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    background: linear-gradient(135deg, rgba(0, 255, 231, 0.1), rgba(0, 212, 255, 0.1));
    padding: 8px 16px;
    border-radius: 12px;
    display: inline-block;
    margin-top: 10px;
  }
  
  .card-result a:hover {
    color: #fff;
    background: linear-gradient(135deg, #00ffe7, #00d4ff);
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(0, 255, 231, 0.3);
  }
  
  /* Trending section */
  .trending-section {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border-radius: 24px;
    box-shadow: 
      0 20px 40px rgba(0, 0, 0, 0.3), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.1),
      0 0 0 1px rgba(147, 51, 234, 0.2);
    padding: 40px;
    width: 100%;
    max-width: 700px;
    animation: fadeInUp 1s ease-out 0.5s both;
    position: relative;
  }
  
  .trending-section h2 {
    color: #c4b5fd;
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 30px;
    text-shadow: 0 2px 8px rgba(147, 51, 234, 0.5);
    text-align: center;
  }
  
  /* Tooltip styling */
  .tooltip {
    position: relative;
    display: inline-block;
    cursor: help;
  }
  
  .tooltip .tooltiptext {
    visibility: hidden;
    width: 280px;
    background: rgba(0, 0, 0, 0.9);
    color: #fff;
    text-align: left;
    border-radius: 12px;
    padding: 12px 16px;
    position: absolute;
    z-index: 1000;
    bottom: 125%;
    left: 50%;
    transform: translateX(-50%);
    opacity: 0;
    transition: opacity 0.3s ease;
    font-size: 0.95rem;
    line-height: 1.4;
    backdrop-filter: blur(20px);
    border: 1px solid rgba(147, 51, 234, 0.3);
  }
  
  .tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
  }
  
  /* Trending list styling */
  #trendingList {
    padding: 0;
    margin: 0;
  }
  
  #trendingList li {
    list-style: none;
    margin-bottom: 20px;
    background: rgba(255, 255, 255, 0.08);
    border: 1px solid rgba(147, 51, 234, 0.2);
    border-radius: 16px;
    padding: 20px;
    backdrop-filter: blur(10px);
    transition: all 0.4s ease;
    position: relative;
    overflow: hidden;
  }
  
  #trendingList li::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(147, 51, 234, 0.1), transparent);
    transition: all 0.8s ease;
  }
  
  #trendingList li:hover {
    background: rgba(255, 255, 255, 0.12);
    transform: translateY(-5px) scale(1.02);
    border-color: rgba(147, 51, 234, 0.4);
    box-shadow: 0 10px 30px rgba(147, 51, 234, 0.2);
  }
  
  #trendingList li:hover::before {
    left: 100%;
  }
  
  #trendingList a {
    color: #00ffe7;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    display: block;
  }
  
  #trendingList a:hover {
    color: #fff;
  }
  
  #trendingList a span {
    color: rgba(255, 255, 255, 0.8);
    font-weight: 400;
    font-size: 0.95rem;
  }
  
  /* Music particles */
  .music-particles {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: -1;
  }
  
  .music-particle {
    position: absolute;
    background: linear-gradient(45deg, #a855f7, #c4b5fd);
    border-radius: 50%;
    opacity: 0.4;
    animation: particleFloat 10s ease-in-out infinite;
  }
  
  @keyframes particleFloat {
    0%, 100% { 
      transform: translateY(0px) translateX(0px) scale(1);
      opacity: 0.4;
    }
    33% { 
      transform: translateY(-80px) translateX(40px) scale(1.2);
      opacity: 0.7;
    }
    66% { 
      transform: translateY(-40px) translateX(-60px) scale(0.8);
      opacity: 0.5;
    }
  }
  
  .music-particle:nth-child(1) { width: 6px; height: 6px; top: 20%; left: 10%; animation-delay: 0s; animation-duration: 12s; }
  .music-particle:nth-child(2) { width: 8px; height: 8px; top: 35%; left: 85%; animation-delay: 2s; animation-duration: 10s; }
  .music-particle:nth-child(3) { width: 5px; height: 5px; top: 60%; left: 15%; animation-delay: 4s; animation-duration: 14s; }
  .music-particle:nth-child(4) { width: 10px; height: 10px; top: 75%; left: 80%; animation-delay: 1s; animation-duration: 9s; }
  .music-particle:nth-child(5) { width: 7px; height: 7px; top: 45%; left: 5%; animation-delay: 6s; animation-duration: 11s; }
  .music-particle:nth-child(6) { width: 9px; height: 9px; top: 15%; left: 70%; animation-delay: 3s; animation-duration: 13s; }
  .music-particle:nth-child(7) { width: 6px; height: 6px; top: 85%; left: 25%; animation-delay: 5s; animation-duration: 8s; }
  .music-particle:nth-child(8) { width: 11px; height: 11px; top: 50%; left: 90%; animation-delay: 7s; animation-duration: 15s; }
  
  /* Responsive adjustments */
  @media (max-width: 768px) {
    h1 {
      font-size: 2.5rem;
    }
    
    .glass-card, .card-result, .trending-section {
      padding: 30px 25px;
      margin: 20px 10px;
    }
    
    .main-container {
      padding: 40px 15px;
    }
    
    .tooltip .tooltiptext {
      width: 240px;
    }
  }
  
  @media (max-width: 480px) {
    h1 {
      font-size: 2rem;
    }
    
    .glass-card, .card-result, .trending-section {
      padding: 25px 20px;
    }
  }
</style>

<!-- Page Background with Music Wave Animations -->
<div class="page-background"></div>
<div class="wave-overlay"></div>

<!-- Floating Music Notes -->
<div class="music-notes">
  <div class="music-note">♪</div>
  <div class="music-note">♫</div>
  <div class="music-note">♪</div>
  <div class="music-note">♬</div>
  <div class="music-note">♫</div>
  <div class="music-note">♪</div>
</div>

<!-- Music Particles -->
<div class="music-particles">
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
  <div class="music-particle"></div>
</div>

<div class="main-container">
  <h1>🎬 Guitar Aces Content Generator</h1>
  
  <div class="glass-card">
    <input type="text" id="keywordInput" placeholder="Enter a potential video topic" />
    <button class="submit-btn" id="generateBtn" onclick="submitKeyword()">
      🎸 Generate Script
    </button>
  </div>
  
  <div id="scriptsContainer"></div>
  
  <div class="trending-section" id="trendingSection">
    <h2 class="tooltip">🔥 Trending Today
      <span class="tooltiptext">Feeling stuck? These are trending TikToks — refresh the page for a new batch!</span>
    </h2>
    <ul id="trendingList"></ul>
  </div>
</div>

<script>
  const sheetURL = "https://opensheet.vercel.app/15jwGTstUvwavtcD44ZNMk6RDOs2y7zcn3hHFvvw691M/Sheet1";
  const webhookURL = "https://hook.us2.make.com/nqoi4abb8zblgrchy7y9vosnqhrs1pes";

  function clean(str) {
    return str?.toLowerCase().replace(/^['"`""'']+|['"`""'']+$/g, '').replace(/\s+/g, ' ').replace(/[\u200B-\u200D\uFEFF]/g, '').trim();
  }

  async function submitKeyword() {
    const inputEl = document.getElementById("keywordInput");
    const btnEl = document.getElementById("generateBtn");
    const keyword = clean(inputEl.value);
    const container = document.getElementById("scriptsContainer");

    if (!keyword) return alert("Please enter a keyword.");

    // Show loading state
    btnEl.disabled = true;
    btnEl.innerHTML = `🎵 Generating <span class="loader"></span>`;

    // Send to webhook
    await fetch(webhookURL, {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ keyword })
    });

    // Estimate new row number
    let estimatedRow = "a new row";
    try {
      const res = await fetch(sheetURL);
      const data = await res.json();
      estimatedRow = `Row ${data.length + 1}`;
    } catch (err) {
      console.warn("Unable to fetch sheet data.");
    }

    // Show result
    container.innerHTML = `
      <div class="card-result">
        <h2>✅ Request Sent</h2>
        <p>Your script is being generated with AI magic!</p>
        <p><strong>Check:</strong> ${estimatedRow}</p>
        <a href="https://docs.google.com/spreadsheets/d/15jwGTstUvwavtcD44ZNMk6RDOs2y7zcn3hHFvvw691M/edit#gid=0" target="_blank">
          📄 View Script on Google Sheets
        </a>
      </div>
    `;

    // Reset button after 2s
    setTimeout(() => {
      btnEl.disabled = false;
      btnEl.innerHTML = "🎸 Generate Script";
      inputEl.value = "";
    }, 2000);
  }

  // Webhook URL that returns the latest TikTok trends as JSON
  const trendsWebhook = "https://hook.us2.make.com/qlnuuhstm25oxmlft55qgyhlfd7m5t45";

  async function loadTrendingVideos() {
    const list = document.getElementById("trendingList");
    list.innerHTML = "<li style='text-align: center; color: rgba(255,255,255,0.7);'>🎵 Loading trending TikToks...</li>";

    try {
      const res = await fetch(trendsWebhook);
      const json = await res.json();
      const trends = json.trends || [];

      if (trends.length === 0) {
        list.innerHTML = "<li style='text-align: center; color: rgba(255,255,255,0.7);'>🎭 No trending videos right now.</li>";
        return;
      }

      list.innerHTML = trends.slice(0, 5).map(t => `
        <li>
          <a href="${t.webVideoUrl}" target="_blank" rel="noopener noreferrer">
            🎥 ${t.text}<br>
            <span>❤️ ${Number(t.diggCount || 0).toLocaleString()} likes</span>
          </a>
        </li>
      `).join("");

    } catch (err) {
      list.innerHTML = "<li style='text-align: center; color: rgba(255,255,255,0.7);'>🎸 Unable to load trends right now.</li>";
      console.error("Error fetching trends:", err);
    }
  }

  // Run on page load
  loadTrendingVideos();
  
  // Allow Enter key to submit
  document.getElementById('keywordInput').addEventListener('keypress', function(e) {
    if (e.key === 'Enter') {
      submitKeyword();
    }
  });
</script>

</body>
</html>







---
layout: base
title: GuitarAces Marketing Solutions
description: Empowering TheGuitarAces with Digital Marketing Strategy
comments: true
hide: true
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GuitarAces - Social Media Marketing Solutions</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>

<style>
  /* Base styles with deep purple marketing theme */
  body {
    margin: 0;
    padding: 0;
    font-family: 'Inter', sans-serif;
    color: #fff;
    overflow-x: hidden;
  }
  
  /* Dynamic gradient background with marketing wave animation */
  .page-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, #1a0b3d, #2d1b69, #4c2a85);
    z-index: -3;
  }
  
  /* Animated social media wave overlay */
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
  
  .hero-container {
    position: relative;
    padding: 60px 20px;
    overflow: hidden;
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
  
  /* Floating social media icons */
  .social-icons {
    position: absolute;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
  }
  
  .social-icon {
    position: absolute;
    color: rgba(147, 51, 234, 0.4);
    font-size: 24px;
    animation: socialFloat 8s infinite ease-in-out;
  }
  
  @keyframes socialFloat {
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
  
  .social-icon:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
  .social-icon:nth-child(2) { top: 40%; left: 85%; animation-delay: 2s; font-size: 32px; }
  .social-icon:nth-child(3) { top: 70%; left: 15%; animation-delay: 4s; font-size: 20px; }
  .social-icon:nth-child(4) { top: 15%; left: 70%; animation-delay: 1s; font-size: 28px; }
  .social-icon:nth-child(5) { top: 80%; left: 80%; animation-delay: 3s; }
  .social-icon:nth-child(6) { top: 35%; left: 5%; animation-delay: 5s; font-size: 26px; }
  
  /* Pulsing marketing rings */
  .marketing-ring {
    position: absolute;
    border: 2px solid rgba(147, 51, 234, 0.3);
    border-radius: 50%;
    animation: marketingPulse 4s infinite;
  }
  
  @keyframes marketingPulse {
    0% {
      transform: scale(0.8);
      opacity: 0.8;
    }
    50% {
      transform: scale(1.2);
      opacity: 0.4;
    }
    100% {
      transform: scale(1.8);
      opacity: 0;
    }
  }
  
  .marketing-ring-1 {
    top: 30%;
    right: 20%;
    width: 120px;
    height: 120px;
    animation-delay: 0s;
  }
  
  .marketing-ring-2 {
    bottom: 25%;
    left: 15%;
    width: 180px;
    height: 180px;
    animation-delay: 2s;
  }
  
  /* Hero section */
  .hero-section {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 60px;
    position: relative;
    z-index: 1;
  }
  
  .hero-content {
    flex: 1;
    min-width: 300px;
  }
  
  .hero-title {
    font-size: 4rem;
    font-weight: 800;
    margin-bottom: 24px;
    background: linear-gradient(135deg, #c4b5fd, #a855f7, #7c3aed, #6d28d9);
    background-size: 300% auto;
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: gradientShift 4s linear infinite;
    line-height: 1.1;
    text-shadow: 0 0 30px rgba(168, 85, 247, 0.5);
  }
  
  @keyframes gradientShift {
    0% { background-position: 0% center; }
    100% { background-position: 300% center; }
  }
  
  .hero-subtitle {
    font-size: 1.3rem;
    margin-bottom: 30px;
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.6;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
    animation: fadeInUp 1s ease-out 0.5s both;
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
  
  .button-container {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    animation: fadeInUp 1s ease-out 0.8s both;
  }
  
  .button {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 16px 32px;
    border-radius: 50px;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    position: relative;
    overflow: hidden;
    font-size: 1.1rem;
  }
  
  .button::before {
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
  
  .primary-button {
    background: linear-gradient(135deg, #a855f7, #7c3aed, #6d28d9);
    color: #fff;
    box-shadow: 0 8px 32px rgba(168, 85, 247, 0.4);
    animation: buttonGlow 3s infinite alternate;
  }
  
  @keyframes buttonGlow {
    0% { 
      box-shadow: 0 8px 32px rgba(168, 85, 247, 0.4), 0 0 20px rgba(168, 85, 247, 0.2);
    }
    100% { 
      box-shadow: 0 12px 40px rgba(168, 85, 247, 0.6), 0 0 30px rgba(168, 85, 247, 0.4);
    }
  }
  
  .primary-button:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0 16px 48px rgba(168, 85, 247, 0.6);
  }
  
  .primary-button:hover::before {
    left: 100%;
  }
  
  .secondary-button {
    background: rgba(255, 255, 255, 0.1);
    color: #c4b5fd;
    border: 2px solid rgba(196, 181, 253, 0.3);
    backdrop-filter: blur(10px);
  }
  
  .secondary-button:hover {
    transform: translateY(-5px) scale(1.05);
    background: rgba(255, 255, 255, 0.2);
    border-color: rgba(196, 181, 253, 0.6);
    box-shadow: 0 16px 32px rgba(0, 0, 0, 0.2);
  }
  
  /* Demo section */
  .demo-section {
    flex: 1;
    min-width: 400px;
    position: relative;
    animation: fadeInUp 1s ease-out 1s both;
  }
  
  .demo-glow {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 120%;
    height: 120%;
    border-radius: 30px;
    filter: blur(50px);
    background: radial-gradient(circle, rgba(147, 51, 234, 0.3), rgba(168, 85, 247, 0.2), transparent 70%);
    z-index: 0;
    animation: demoGlow 6s infinite alternate;
  }
  
  @keyframes demoGlow {
    0% { 
      transform: translate(-50%, -50%) scale(0.9);
      opacity: 0.6;
    }
    100% { 
      transform: translate(-50%, -50%) scale(1.1);
      opacity: 0.9;
    }
  }
  
  .demo-window {
    position: relative;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border-radius: 24px;
    overflow: hidden;
    box-shadow: 
      0 20px 40px rgba(0, 0, 0, 0.3), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.1),
      0 0 0 1px rgba(147, 51, 234, 0.2);
    z-index: 1;
    animation: windowFloat 8s infinite ease-in-out;
  }
  
  @keyframes windowFloat {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    25% { transform: translateY(-10px) rotate(0.5deg); }
    50% { transform: translateY(-5px) rotate(0deg); }
    75% { transform: translateY(-15px) rotate(-0.5deg); }
  }
  
  .window-header {
    background: rgba(255, 255, 255, 0.08);
    padding: 20px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .window-controls {
    display: flex;
    gap: 10px;
  }
  
  .window-circle {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    animation: controlBreathe 4s infinite alternate;
  }
  
  @keyframes controlBreathe {
    0% { transform: scale(1); opacity: 0.8; }
    100% { transform: scale(1.1); opacity: 1; }
  }
  
  .window-circle.red { background-color: #ff6b6b; }
  .window-circle.yellow { background-color: #ffd93d; }
  .window-circle.green { background-color: #6bcf7f; }
  
  .app-title {
    flex: 1;
    text-align: center;
    font-size: 16px;
    font-weight: 600;
    color: rgba(255, 255, 255, 0.9);
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }
  
  .window-content {
    padding: 30px;
  }
  
  .window-title {
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 25px;
    color: #c4b5fd;
    text-shadow: 0 2px 8px rgba(147, 51, 234, 0.5);
    text-align: center;
  }
  
  .marketing-stats {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin-bottom: 30px;
  }
  
  .stat-item {
    background: rgba(255, 255, 255, 0.06);
    border: 1px solid rgba(147, 51, 234, 0.2);
    border-radius: 16px;
    padding: 20px;
    text-align: center;
    transition: all 0.4s ease;
    backdrop-filter: blur(10px);
    position: relative;
    overflow: hidden;
  }
  
  .stat-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(147, 51, 234, 0.1), transparent);
    transition: all 0.8s ease;
  }
  
  .stat-item:hover {
    background: rgba(255, 255, 255, 0.1);
    transform: translateY(-5px) scale(1.02);
    border-color: rgba(147, 51, 234, 0.4);
    box-shadow: 0 10px 30px rgba(147, 51, 234, 0.2);
  }
  
  .stat-item:hover::before {
    left: 100%;
  }
  
  .stat-label {
    font-weight: 600;
    color: #a855f7;
    margin-bottom: 8px;
    font-size: 0.95rem;
  }
  
  .stat-value {
    color: rgba(255, 255, 255, 0.9);
    font-size: 1.1rem;
    font-weight: 500;
  }
  
  .action-button {
    position: relative;
    display: block;
    width: 100%;
    padding: 16px;
    text-align: center;
    background: linear-gradient(135deg, #7c3aed, #6d28d9, #5b21b6);
    color: #fff;
    border-radius: 16px;
    text-decoration: none;
    font-weight: 700;
    font-size: 1.1rem;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    box-shadow: 0 8px 24px rgba(124, 58, 237, 0.4);
    overflow: hidden;
  }
  
  .action-button::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: all 0.6s ease;
  }
  
  .action-button:hover {
    transform: translateY(-3px) scale(1.02);
    box-shadow: 0 12px 32px rgba(124, 58, 237, 0.6);
  }
  
  .action-button:hover::before {
    left: 100%;
  }
  
  .marketing-icon {
    position: absolute;
    bottom: -15px;
    right: -15px;
    width: 45px;
    height: 45px;
    background: linear-gradient(135deg, #1f2937, #111827);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 
      0 8px 16px rgba(0, 0, 0, 0.4),
      inset 0 0 0 2px rgba(147, 51, 234, 0.3);
    z-index: 2;
    animation: iconPulse 3s infinite alternate;
  }
  
  @keyframes iconPulse {
    0% { 
      transform: scale(1);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4), inset 0 0 0 2px rgba(147, 51, 234, 0.3);
    }
    100% { 
      transform: scale(1.1);
      box-shadow: 0 12px 24px rgba(0, 0, 0, 0.5), inset 0 0 0 2px rgba(147, 51, 234, 0.6);
    }
  }
  
  /* Features section */
  .features-section {
    position: relative;
    padding: 120px 20px;
    overflow: hidden;
  }
  
  .features-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(30, 15, 62, 0.9), rgba(45, 27, 105, 0.9));
    z-index: 0;
  }
  
  .features-content {
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }
  
  .section-header {
    text-align: center;
    max-width: 800px;
    margin: 0 auto 80px;
  }
  
  .section-title {
    font-size: 3rem;
    font-weight: 800;
    margin-bottom: 24px;
    background: linear-gradient(135deg, #c4b5fd, #a855f7, #7c3aed);
    background-size: 200% auto;
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: gradientShift 4s linear infinite;
  }
  
  .section-description {
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.7;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }
  
  /* Feature cards with staggered layout */
  .features-container {
    max-width: 1000px;
    margin: 60px auto 0;
    display: flex;
    flex-direction: column;
  }
  
  .top-features {
    display: flex;
    justify-content: space-between;
    gap: 40px;
    margin-bottom: 120px;
  }
  
  .bottom-feature {
    max-width: 550px;
    margin: 0 auto;
  }
  
  .feature-card {
    background: rgba(255, 255, 255, 0.04);
    backdrop-filter: blur(20px);
    border-radius: 24px;
    overflow: hidden;
    box-shadow: 
      0 20px 40px rgba(0, 0, 0, 0.3), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.08);
    padding: 50px;
    transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    flex: 1;
    position: relative;
    animation: cardFloat 8s infinite ease-in-out;
  }
  
  @keyframes cardFloat {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    25% { transform: translateY(-15px) rotate(0.8deg); }
    50% { transform: translateY(-8px) rotate(0deg); }
    75% { transform: translateY(-20px) rotate(-0.8deg); }
  }
  
  .feature-card:nth-child(1) { animation-delay: 0s; }
  .feature-card:nth-child(2) { animation-delay: 2s; }
  .bottom-feature .feature-card { animation-delay: 4s; }
  
  /* Gradient border effect */
  .feature-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: 24px;
    padding: 2px;
    background: linear-gradient(135deg, 
      rgba(147, 51, 234, 0.6), 
      rgba(168, 85, 247, 0.3), 
      transparent, 
      rgba(147, 51, 234, 0.2)
    );
    -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: xor;
    mask-composite: exclude;
    opacity: 0.6;
    transition: opacity 0.6s ease;
  }
  
  .feature-card:hover {
    transform: translateY(-20px) scale(1.03);
    background: rgba(255, 255, 255, 0.08);
    box-shadow: 
      0 30px 60px rgba(0, 0, 0, 0.4), 
      inset 0 0 0 1px rgba(255, 255, 255, 0.12),
      0 0 40px rgba(147, 51, 234, 0.3);
  }
  
  .feature-card:hover::before {
    opacity: 1;
  }
  
  .feature-icon {
    width: 90px;
    height: 90px;
    margin: 0 auto 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, rgba(147, 51, 234, 0.2), rgba(168, 85, 247, 0.1));
    border-radius: 24px;
    font-size: 32px;
    position: relative;
    box-shadow: 
      0 12px 24px rgba(0, 0, 0, 0.2),
      inset 0 0 0 1px rgba(255, 255, 255, 0.08);
    animation: iconFloat 6s infinite ease-in-out;
  }
  
  @keyframes iconFloat {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-10px) rotate(5deg); }
  }
  
  .feature-icon::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 24px;
    padding: 2px;
    background: linear-gradient(135deg, rgba(147, 51, 234, 0.8), rgba(168, 85, 247, 0.2));
    -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: xor;
    mask-composite: exclude;
  }
  
  .feature-title {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 24px;
    color: #c4b5fd;
    text-align: center;
    text-shadow: 0 4px 8px rgba(147, 51, 234, 0.3);
  }
  
  .feature-description {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.7;
    text-align: center;
    font-size: 1.15rem;
  }
  
  /* CTA section with enhanced visuals */
  .cta-section {
    position: relative;
    padding: 120px 20px;
    text-align: center;
    overflow: hidden;
  }
  
  .cta-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(45, 27, 105, 0.95), rgba(55, 35, 135, 0.95));
    z-index: 0;
  }
  
  .cta-ripple {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 800px;
    height: 800px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(147, 51, 234, 0.08) 0%, transparent 70%);
    animation: ctaRipple 8s infinite;
    z-index: 0;
  }
  
  @keyframes ctaRipple {
    0% {
      transform: translate(-50%, -50%) scale(0.8);
      opacity: 0.8;
    }
    50% {
      transform: translate(-50%, -50%) scale(1.2);
      opacity: 0.4;
    }
    100% {
      transform: translate(-50%, -50%) scale(1.6);
      opacity: 0;
    }
  }
  
  .cta-content {
    max-width: 800px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }
  
  .cta-title {
    font-size: 3rem;
    font-weight: 800;
    margin-bottom: 24px;
    color: #fff;
    text-shadow: 0 4px 16px rgba(147, 51, 234, 0.5);
  }
  
  .cta-description {
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 0.9);
    margin: 0 auto 40px;
    line-height: 1.7;
    max-width: 600px;
    text-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
  }
  
  .cta-buttons {
    display: flex;
    justify-content: center;
    gap: 24px;
    flex-wrap: wrap;
  }
  
  /* Responsive adjustments */
  @media (max-width: 768px) {
    .hero-title {
      font-size: 2.8rem;
    }
    
    .section-title, .cta-title {
      font-size: 2.2rem;
    }
    
    .top-features {
      flex-direction: column;
      margin-bottom: 60px;
    }
    
    .feature-title {
      font-size: 1.6rem;
    }
    
    .demo-section {
      min-width: 300px;
    }
  }
  
  /* Particle system for marketing visualization */
  .marketing-particles {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: -1;
  }
  
  .marketing-particle {
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
  
  /* Generate particle positions */
  .marketing-particle:nth-child(1) { width: 6px; height: 6px; top: 20%; left: 10%; animation-delay: 0s; animation-duration: 12s; }
  .marketing-particle:nth-child(2) { width: 8px; height: 8px; top: 35%; left: 85%; animation-delay: 2s; animation-duration: 10s; }
  .marketing-particle:nth-child(3) { width: 5px; height: 5px; top: 60%; left: 15%; animation-delay: 4s; animation-duration: 14s; }
  .marketing-particle:nth-child(4) { width: 10px; height: 10px; top: 75%; left: 80%; animation-delay: 1s; animation-duration: 9s; }
  .marketing-particle:nth-child(5) { width: 7px; height: 7px; top: 45%; left: 5%; animation-delay: 6s; animation-duration: 11s; }
  .marketing-particle:nth-child(6) { width: 9px; height: 9px; top: 15%; left: 70%; animation-delay: 3s; animation-duration: 13s; }
  .marketing-particle:nth-child(7) { width: 6px; height: 6px; top: 85%; left: 25%; animation-delay: 5s; animation-duration: 8s; }
  .marketing-particle:nth-child(8) { width: 11px; height: 11px; top: 50%; left: 90%; animation-delay: 7s; animation-duration: 15s; }
</style>

<!-- Page Background with Marketing Wave Animations -->
<div class="page-background"></div>
<div class="wave-overlay"></div>

<!-- Marketing Particles -->
<div class="marketing-particles">
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
  <div class="marketing-particle"></div>
</div>

<!-- Hero Section -->
<div class="hero-container">
  <!-- Floating Social Media Icons -->
  <div class="social-icons">
    <div class="social-icon">📱</div>
    <div class="social-icon">📊</div>
    <div class="social-icon">📧</div>
    <div class="social-icon">📹</div>
    <div class="social-icon">📈</div>
    <div class="social-icon">💡</div>
  </div>
  
  <!-- Marketing Rings -->
  <div class="marketing-ring marketing-ring-1"></div>
  <div class="marketing-ring marketing-ring-2"></div>
  
  <div class="hero-section">
    <div class="hero-content">
      <h1 class="hero-title">TheGuitarAces: Social Media Marketing</h1>
      <p class="hero-subtitle">Take TheGuitarAces from relying on word-of-mouth to growing online with easy-to-use social media plans, simple video tools, and automated posting.</p>
      <div class="button-container">
        <a href="#demo" class="button primary-button">
          <span>🚀</span>
          Boost Your Exposure
        </a>
        <a href="#features" class="button secondary-button">
          <span>📊</span>
          View Solutions
        </a>
      </div>
    </div>
    
    <div class="demo-section">
      <div class="demo-glow"></div>
      <div class="demo-window">
        <div class="window-header">
          <div class="window-controls">
            <div class="window-circle red"></div>
            <div class="window-circle yellow"></div>
            <div class="window-circle green"></div>
          </div>
          <div class="app-title">TheGuitarAces Marketing Dashboard</div>
        </div>
        <div class="window-content">
          <h3 class="window-title">Marketing Analytics</h3>
          <div class="marketing-stats">
            <div class="stat-item">
              <div class="stat-label">Social Media Reach</div>
              <div class="stat-value" data-target="15000">0</div>
            </div>
            <div class="stat-item">
              <div class="stat-label">Video Views</div>
              <div class="stat-value" data-target="8500">0</div>
            </div>
            <div class="stat-item">
              <div class="stat-label">Email Open Rate</div>
              <div class="stat-value" data-target="68">0%</div>
            </div>
            <div class="stat-item">
              <div class="stat-label">New Customers</div>
              <div class="stat-value" data-target="24">+0</div>
            </div>
          </div>
          <div style="position: relative;">
            <a href="#demo" class="action-button">
              Generate Your Marketing Content
              <div class="marketing-icon">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="#a855f7">
                  <path d="M16 6l2.29 2.29-4.88 4.88-4-4L2 16.59 3.41 18l6-6 4 4 6.3-6.29L22 12V6z"/>
                </svg>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- Features Section -->
<div class="features-section" id="features">
  <div class="features-bg"></div>
  
  <div class="features-content">
    <div class="section-header">
      <h2 class="section-title">Complete Marketing Ecosystem for TheGuitarAces</h2>
      <p class="section-description">Our comprehensive solution addresses TheGuitarAces' marketing challenges with multiple digital strategies to increase exposure and attract new customers.</p>
    </div>
    
    <!-- Feature Cards with Enhanced Layout -->
    <div class="features-container">
      <!-- Top row with two cards side by side -->
      <div class="top-features">
        <div class="feature-card">
          <div class="feature-icon">
            <svg width="40" height="40" viewBox="0 0 24 24" fill="#a855f7">
              <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm-5 14H4v-4h11v4zm0-5H4V9h11v4zm2 5h-2v-4h2v4zm0-5h-2V9h2v4z"/>
            </svg>
          </div>
          <h3 class="feature-title">Email Marketing Tools</h3>
          <p class="feature-description">Professional email templates and automated campaigns to nurture leads and keep TheGuitarAces top-of-mind with potential students and existing customers.</p>
        </div>
        
        <div class="feature-card">
          <div class="feature-icon">
            <svg width="40" height="40" viewBox="0 0 24 24" fill="#a855f7">
              <path d="M17 10.5V7c0-.55-.45-1-1-1H4c-.55 0-1 .45-1 1v10c0 .55.45 1 1 1h12c.55 0 1-.45 1-1v-3.5l4 4v-11l-4 4z"/>
            </svg>
          </div>
          <h3 class="feature-title">Video Content Generator</h3>
          <p class="feature-description">AI-powered social media video idea generator that creates engaging content concepts tailored for guitar education and music learning audiences.</p>
        </div>
      </div>

      <!-- Bottom row with one centered card -->
      <div class="bottom-feature">
        <div class="feature-card">
          <div class="feature-icon">
            <svg width="40" height="40" viewBox="0 0 24 24" fill="#a855f7">
              <path d="M19 3h-4.18C14.4 1.84 13.3 1 12 1c-1.3 0-2.4.84-2.82 2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 0c.55 0 1 .45 1 1s-.45 1-1 1-1-.45-1-1 .45-1 1-1zm2 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/>
            </svg>
          </div>
          <h3 class="feature-title">Smart Scheduling Calendar</h3>
          <p class="feature-description">Intelligent video scheduling system with optimized upload times to maximize views, engagement, and interactions across all social media platforms for TheGuitarAces.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- CTA Section -->
<div class="cta-section" id="demo">
  <div class="cta-bg"></div>
  <div class="cta-ripple"></div>
  
  <div class="cta-content">
    <h2 class="cta-title">Ready to Transform TheGuitarAces Marketing?</h2>
    <p class="cta-description">Advanced digital solutions designed to increase exposure for TheGuitarAces.</p>
    <div class="cta-buttons">
      <a href="{{site.baseurl}}/Generator" class="button primary-button">
        <span>🎯</span>
        Start Marketing Campaign
      </a>
      <a href="#demo" class="button primary-button">
        <span>📊</span>
        View Analytics Demo
      </a>
    </div>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  // Animated counter for marketing statistics
  const statValues = document.querySelectorAll('.stat-value');
  
  function animateCounter(element) {
    const target = parseInt(element.getAttribute('data-target'));
    const increment = target / 200;
    let current = 0;
    
    const timer = setInterval(() => {
      current += increment;
      if (current >= target) {
        current = target;
        clearInterval(timer);
      }
      
      if (element.textContent.includes('%')) {
        element.textContent = Math.floor(current) + '%';
      } else if (element.textContent.includes('+')) {
        element.textContent = '+' + Math.floor(current);
      } else {
        element.textContent = Math.floor(current).toLocaleString();
      }
    }, 20);
  }
  
  // Intersection Observer for counter animation
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const statValue = entry.target.querySelector('.stat-value');
        if (statValue && !statValue.classList.contains('animated')) {
          statValue.classList.add('animated');
          animateCounter(statValue);
        }
      }
    });
  }, { threshold: 0.5 });
  
  // Observe stat items
  document.querySelectorAll('.stat-item').forEach(item => {
    observer.observe(item);
  });
  
  // Smooth scrolling for anchor links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        });
      }
    });
  });
});
</script>

<script src="https://utteranc.es/client.js"
        repo="ZafeerA123/GuitarAces"
        issue-term="title"
        label="blogpost-comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>

</body>
</html>



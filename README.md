<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ACCOUNT INFORMATION — Aivan Junrel Sarte</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

  :root {
    --gold: #D4AF37;
    --dark-gold: #B8941F;
    --platinum: #E5E4E2;
    --deep-blue: #0A1628;
    --accent-blue: #1E3A8A;
    --silver: #C0C0C0;
    --text-dark: #1a1a1a;
    --text-light: #ffffff;
    --shadow: rgba(0, 0, 0, 0.25);
  }

  body {
    font-family: 'Inter', system-ui, -apple-system, sans-serif;
    background: radial-gradient(circle at 30% 20%, #1e293b 0%, #0f172a 50%, #020617 100%);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    margin: 0;
  }

  .vip-card {
    width: 380px;
    height: 240px;
    background: linear-gradient(135deg, var(--deep-blue) 0%, #1e3a8a 50%, var(--deep-blue) 100%);
    border-radius: 16px;
    position: relative;
    overflow: hidden;
    box-shadow: 
      0 8px 32px rgba(0, 0, 0, 0.4),
      0 4px 16px rgba(212, 175, 55, 0.2),
      inset 0 1px 0 rgba(255, 255, 255, 0.1);
    border: 2px solid var(--gold);
    transform: perspective(1000px) rotateX(2deg) rotateY(-2deg);
    transition: all 0.3s ease;
    animation: glowPulse 4s ease-in-out infinite;
  }

  .vip-card:hover {
    transform: perspective(1000px) rotateX(0deg) rotateY(0deg) scale(1.02);
    box-shadow: 
      0 12px 48px rgba(0, 0, 0, 0.5),
      0 6px 24px rgba(212, 175, 55, 0.3),
      inset 0 1px 0 rgba(255, 255, 255, 0.15);
  }

  /* Holographic effect overlay */
  .vip-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(
      45deg,
      transparent 30%,
      rgba(255, 255, 255, 0.1) 50%,
      transparent 70%
    );
    pointer-events: none;
    animation: shimmer 3s infinite;
  }

  @keyframes shimmer {
    0% { transform: translateX(-100%) translateY(-100%); }
    100% { transform: translateX(100%) translateY(100%); }
  }

  /* Typing animation keyframes */
  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }

  @keyframes blink-cursor {
    from, to { border-color: transparent; }
    50% { border-color: var(--gold); }
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes slideInRight {
    from {
      opacity: 0;
      transform: translateX(30px);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }

  @keyframes scaleIn {
    from {
      opacity: 0;
      transform: scale(0.8);
    }
    to {
      opacity: 1;
      transform: scale(1);
    }
  }

  @keyframes glowPulse {
    0%, 100% {
      box-shadow: 
        0 8px 32px rgba(0, 0, 0, 0.4),
        0 4px 16px rgba(212, 175, 55, 0.2),
        inset 0 1px 0 rgba(255, 255, 255, 0.1);
    }
    50% {
      box-shadow: 
        0 12px 40px rgba(0, 0, 0, 0.5),
        0 6px 24px rgba(212, 175, 55, 0.4),
        inset 0 1px 0 rgba(255, 255, 255, 0.15);
    }
  }

  @keyframes typingMicrotext {
    from { width: 0; }
    to { width: 100%; }
  }

  /* Security pattern background */
  .security-pattern {
    position: absolute;
    top: 0;
    right: 0;
    width: 200px;
    height: 200px;
    background: repeating-linear-gradient(
      45deg,
      transparent,
      transparent 2px,
      rgba(212, 175, 55, 0.05) 2px,
      rgba(212, 175, 55, 0.05) 4px
    );
    border-radius: 50%;
    opacity: 0.3;
  }

  .vip-header {
    position: absolute;
    top: 16px;
    left: 20px;
    right: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .vip-logo {
    font-size: 18px;
    font-weight: 800;
    color: var(--gold);
    text-shadow: 0 1px 2px rgba(0, 0, 0, 0.5);
    letter-spacing: 2px;
    opacity: 0;
    animation: slideInRight 0.8s ease-out 0.5s forwards;
  }

  .card-number {
    font-family: 'Courier New', monospace;
    font-size: 10px;
    color: var(--platinum);
    font-weight: 600;
    letter-spacing: 1px;
    opacity: 0;
    animation: fadeInUp 0.6s ease-out 1s forwards;
  }

  .member-info {
    position: absolute;
    bottom: 60px;
    left: 140px;
    right: 20px;
  }

  .member-name {
    font-size: 16px;
    font-weight: 700;
    color: var(--text-light);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    line-height: 1.2;
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.7);
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--gold);
    width: 0;
    animation: 
      typing 2s steps(20, end) 1.5s forwards,
      blink-cursor 0.75s step-end 1.5s infinite;
  }

  .member-details {
    margin-top: 8px;
    font-size: 9px;
    color: var(--platinum);
    line-height: 1.4;
    font-weight: 500;
    opacity: 0;
    animat
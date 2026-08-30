# Buka-aja-dulu

<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Surat 💌</title>

<style>
* {
    box-sizing: border-box;
}

html, body {
    margin: 0;
    width: 100%;
    height: 100%;
    font-family: Arial, sans-serif;
}

body {
    overflow: hidden;
    background: linear-gradient(135deg, #ffdce7, #f7b8c9);
}

/* =========================
   DEKORASI BACKGROUND
========================= */

.decor {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
}

.decor span {
    position: absolute;
    font-size: 35px;
    opacity: .55;
    animation: float 4s ease-in-out infinite;
}

.d1 { top: 8%; left: 8%; }
.d2 { top: 16%; right: 10%; animation-delay: .7s; }
.d3 { bottom: 18%; left: 8%; animation-delay: 1.2s; }
.d4 { bottom: 10%; right: 8%; animation-delay: 1.8s; }
.d5 { top: 45%; left: 4%; font-size: 25px; animation-delay: .4s; }
.d6 { top: 55%; right: 4%; font-size: 25px; animation-delay: 1.5s; }

@keyframes float {
    0%, 100% {
        transform: translateY(0) rotate(0);
    }

    50% {
        transform: translateY(-12px) rotate(6deg);
    }
}

/* =========================
   HALAMAN AWAL
========================= */

.home {
    position: relative;
    width: 100%;
    height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;
}

.home-box {
    text-align: center;
    z-index: 5;
    padding: 30px;
}

.home-box .emoji {
    font-size: 90px;
    animation: bounce 2s ease-in-out infinite;
}

@keyframes bounce {
    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

.home h1 {
    color: #864354;
    font-size: 34px;
    margin: 15px 0 8px;
}

.home p {
    color: #864354;
    font-size: 17px;
    margin-bottom: 25px;
}

.open-btn {
    border: none;
    padding: 15px 30px;
    border-radius: 30px;

    background: #d9687e;
    color: white;

    font-size: 17px;
    font-weight: bold;

    cursor: pointer;

    box-shadow: 0 8px 20px rgba(120,50,70,.2);

    transition: .2s;
}

.open-btn:active {
    transform: scale(.94);
}

/* =========================
   SURAT
========================= */

.letter-screen {
    position: fixed;
    inset: 0;

    display: none;

    justify-content: center;
    align-items: center;

    padding: 20px;

    background: rgba(247,184,201,.96);

    z-index: 20;
}

.letter-screen.show {
    display:

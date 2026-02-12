<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grupo Privado - ConteÃºdo Exclusivo +18</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(to bottom, #0f0f0f, #3d1a1a, #0f0f0f);
            color: white;
            overflow-x: hidden;
        }

        .bg-effects {
            position: fixed;
            inset: 0;
            pointer-events: none;
            overflow: hidden;
            z-index: 0;
        }

        .bg-effects::before {
            content: '';
            position: absolute;
            top: 0;
            left: 25%;
            width: 384px;
            height: 384px;
            background: rgba(220, 38, 38, 0.2);
            border-radius: 50%;
            filter: blur(128px);
            animation: pulse 4s ease-in-out infinite;
        }

        .bg-effects::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 25%;
            width: 384px;
            height: 384px;
            background: rgba(236, 72, 153, 0.2);
            border-radius: 50%;
            filter: blur(128px);
            animation: pulse 4s ease-in-out 1s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 40;
            transition: all 0.3s ease;
            background: transparent;
        }

        header.scrolled {
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(220, 38, 38, 0.2);
        }

        .header-content {
            max-width: 1280px;
            margin: 0 auto;
            padding: 1rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(to bottom right, #dc2626, #ec4899);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: pulse 2s ease-in-out infinite;
        }

        .logo-text h1 {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(to right, #f87171, #fb7185, #f87171);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo-text p {
            font-size: 0.75rem;
            color: rgba(249, 115, 147, 0.8);
        }

        .header-btn {
            display: none;
            align-items: center;
            gap: 0.5rem;
            background: linear-gradient(to right, #dc2626, #ec4899);
            color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 9999px;
            font-weight: 600;
            font-size: 0.875rem;
            text-decoration: none;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 10px 15px -3px rgba(220, 38, 38, 0.25);
        }

        .header-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 25px -5px rgba(220, 38, 38, 0.4);
        }

        @media (min-width: 768px) {
            .header-btn {
                display: flex;
            }
        }

        /* Age Verification Modal */
        .age-modal {
            position: fixed;
            inset: 0;
            z-index: 100;
            background: linear-gradient(to bottom right, #7c2d12, #581c87, #000);
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem;
        }

        .age-modal.hidden {
            display: none;
        }

        .age-modal-content {
            max-width: 448px;
            width: 100%;
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(220, 38, 38, 0.3);
            border-radius: 1.5rem;
            padding: 2rem;
            text-align: center;
            animation: fadeIn 0.3s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        .age-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 1.5rem;
            background: linear-gradient(to bottom right, #dc2626, #ec4899);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: pulse 2s ease-in-out infinite;
            font-size: 2.5rem;
        }

        .age-modal h2 {
            font-size: 1.875rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .age-modal p {
            color: rgba(249, 115, 147, 0.9);
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .age-buttons {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
            margin-bottom: 1.5rem;
        }

        .btn-confirm {
            background: linear-gradient(to right, #dc2626, #ec4899);
            color: white;
            font-weight: bold;
            padding: 1rem;
            border-radius: 0.75rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            transform: scale(1);
        }

        .btn-confirm:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 25px -5px rgba(220, 38, 38, 0.4);
        }

        .btn-decline {
            background: rgba(255, 255, 255, 0.1);
            color: rgba(209, 213, 219, 0.8);
            font-weight: 500;
            padding: 0.75rem;
            border-radius: 0.75rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .btn-decline:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .age-disclaimer {
            font-size: 0.75rem;
            color: rgba(107, 114, 128, 0.8);
        }

        /* Hero Section */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding-top: 5rem;
            padding-bottom: 4rem;
            z-index: 10;
        }

        .hero-content {
            max-width: 1280px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 10;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(220, 38, 38, 0.1);
            border: 1px solid rgba(220, 38, 38, 0.3);
            border-radius: 9999px;
            padding: 0.5rem 1rem;
            margin-bottom: 1.5rem;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }

        .hero-badge span {
            color: rgba(248, 113, 113, 0.9);
            font-size: 0.875rem;
            font-weight: 500;
        }

        .hero h2 {
            font-size: clamp(2.5rem, 10vw, 5rem);
            font-weight: bold;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            background: linear-gradient(to right, #f87171, #fb7185, #f87171);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: clamp(1rem, 3vw, 1.5rem);
            color: rgba(249, 115, 147, 0.9);
            max-width: 48rem;
            margin: 0 auto 2rem;
            font-weight: 300;
            line-height: 1.6;
        }

        .hero-cta {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            margin-bottom: 3rem;
        }

        .btn-primary {
            position: relative;
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            background: linear-gradient(to right, #dc2626, #ec4899, #dc2626);
            color: white;
            font-weight: bold;
            font-size: 1.125rem;
            padding: 1rem 2rem;
            border-radius: 9999px;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            transform: scale(1);
            box-shadow: 0 20px 25px -5px rgba(220, 38, 38, 0.4);
            overflow: hidden;
            text-decoration: none;
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            inset: 0;
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(-100%);
            transition: transform 0.7s ease;
        }

        .btn-primary:hover::before {
            transform: translateX(100%);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 25px 50px -12px rgba(220, 38, 38, 0.5);
        }

        .btn-primary span {
            position: relative;
            z-index: 1;
        }

        .hero-stats {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            font-size: 0.875rem;
            color: rgba(249, 115, 147, 0.7);
        }

        .stat {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        /* Gallery Section */
        .gallery {
            position: relative;
            padding: 5rem 1rem;
            z-index: 10;
        }

        .gallery-header {
            max-width: 1280px;
            margin: 0 auto 4rem;
            text-align: center;
        }

        .gallery-header h3 {
            font-size: clamp(1.875rem, 5vw, 3rem);
            font-weight: bold;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #fb7185, #f87171);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .gallery-header p {
            color: rgba(249, 115, 147, 0.8);
            font-size: 1.125rem;
            max-width: 42rem;
            margin: 0 auto;
        }

        .gallery-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .gallery-item {
            position: relative;
            cursor: pointer;
            transform: scale(1);
            transition: all 0.5s ease;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-image {
            position: relative;
            aspect-ratio: 3/4;
            border-radius: 1rem;
            overflow: hidden;
            background: linear-gradient(to bottom right, rgba(127, 29, 29, 0.5), rgba(126, 39, 80, 0.5));
            border: 1px solid rgba(220, 38, 38, 0.2);
            box-shadow: 0 20px 25px -5px rgba(127, 29, 29, 0.2);
        }

        .gallery-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.7s ease;
        }

        .gallery-item:hover .gallery-image img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.2), transparent);
            opacity: 0.6;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 0.8;
        }

        .gallery-badge {
            position: absolute;
            top: 1rem;
            left: 1rem;
            background: linear-gradient(to right, #dc2626, #ec4899);
            color: white;
            font-size: 0.75rem;
            font-weight: bold;
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            display: flex;
            align-items: center;
            gap: 0.25rem;
        }

        .gallery-content {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 1.5rem;
            transform: translateY(0.5rem);
            transition: transform 0.3s ease;
        }

        .gallery-item:hover .gallery-content {
            transform: translateY(0);
        }

        .gallery-content h4 {
            font-size: 1.25rem;
            font-weight: bold;
            color: white;
            margin-bottom: 0.25rem;
        }

        .gallery-content p {
            color: rgba(249, 115, 147, 0.9);
            font-size: 0.875rem;
            font-style: italic;
            margin-bottom: 0.5rem;
        }

        .gallery-more {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: rgba(248, 113, 113, 0.9);
            font-size: 0.875rem;
            font-weight: 500;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .gallery-more {
            opacity: 1;
        }

        /* CTA Section */
        .cta {
            position: relative;
            padding: 6rem 1rem;
            overflow: hidden;
            z-index: 10;
        }

        .cta::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(to right, rgba(127, 29, 29, 0.5), rgba(126, 39, 80, 0.5), rgba(127, 29, 29, 0.5));
        }

        .cta-content {
            max-width: 48rem;
            margin: 0 auto;
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(220, 38, 38, 0.2);
            border-radius: 1.875rem;
            padding: 2rem 2rem;
            text-align: center;
            position: relative;
            z-index: 1;
            box-shadow: 0 20px 25px -5px rgba(127, 29, 29, 0.2);
        }

        .cta-icon {
            width: 64px;
            height: 64px;
            margin: 0 auto 1.5rem;
            background: linear-gradient(to bottom right, #dc2626, #ec4899);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: pulse 2s ease-in-out infinite;
            font-size: 2rem;
        }

        .cta h3 {
            font-size: clamp(1.875rem, 5vw, 3rem);
            font-weight: bold;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #f87171, #fb7185, #f87171);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .cta p {
            color: rgba(249, 115, 147, 0.9);
            font-size: 1.125rem;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .cta-button {
            position: relative;
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            background: linear-gradient(to right, #dc2626, #ec4899, #dc2626);
            color: white;
            font-weight: bold;
            font-size: 1.25rem;
            padding: 1.25rem 2.5rem;
            border-radius: 9999px;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 25px 50px -12px rgba(220, 38, 38, 0.5);
            overflow: hidden;
            text-decoration: none;
            animation: pulse 2s ease-in-out infinite;
        }

        .cta-button::before {
            content: '';
            position: absolute;
            inset: 0;
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(-100%);
            transition: transform 0.7s ease;
        }

        .cta-button:hover::before {
            transform: translateX(100%);
        }

        .cta-button:hover {
            transform: scale(1.05);
            box-shadow: 0 25px 50px -12px rgba(220, 38, 38, 0.6);
        }

        .cta-button span {
            position: relative;
            z-index: 1;
        }

        .cta-disclaimer {
            margin-top: 1.5rem;
            font-size: 0.875rem;
            color: rgba(249, 115, 147, 0.6);
        }

        /* Features */
        .features {
            position: relative;
            padding: 5rem 1rem;
            background: rgba(0, 0, 0, 0.2);
            z-index: 10;
        }

        .features-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            text-align: center;
            padding: 1.5rem;
            border-radius: 1.5rem;
            background: linear-gradient(to bottom right, rgba(127, 29, 29, 0.3), rgba(126, 39, 80, 0.3));
            border: 1px solid rgba(220, 38, 38, 0.1);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            border-color: rgba(220, 38, 38, 0.3);
        }

        .feature-icon {
            width: 56px;
            height: 56px;
            margin: 0 auto 1rem;
            background: linear-gradient(to bottom right, rgba(220, 38, 38, 0.2), rgba(236, 72, 153, 0.2));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.75rem;
            transition: transform 0.3s ease;
        }

        .feature-card:hover .feature-icon {
            transform: scale(1.1);
        }

        .feature-card h4 {
            font-size: 1.25rem;
            font-weight: bold;
            color: white;
            margin-bottom: 0.5rem;
        }

        .feature-card p {
            color: rgba(249, 115, 147, 0.7);
        }

        /* Modal */
        .modal {
            position: fixed;
            inset: 0;
            z-index: 50;
            background: rgba(0, 0, 0, 0.95);
            backdrop-filter: blur(4px);
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem;
            animation: fadeIn 0.3s ease-out;
        }

        .modal.hidden {
            display: none;
        }

        .modal-content {
            position: relative;
            width: 100%;
            max-width: 80rem;
            background: linear-gradient(to bottom right, #1f2937, #000);
            border: 1px solid rgba(220, 38, 38, 0.3);
            border-radius: 1.875rem;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(127, 29, 29, 0.5);
        }

        .modal-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            z-index: 20;
            width: 40px;
            height: 40px;
            background: rgba(0, 0, 0, 0.5);
            border: none;
            border-radius: 50%;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            font-size: 1.5rem;
        }

        .modal-close:hover {
            background: rgba(220, 38, 38, 0.5);
            transform: rotate(90deg);
        }

        .modal-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0;
        }

        @media (min-width: 768px) {
            .modal-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        .modal-image {
            position: relative;
            height: 384px;
            background: #000;
        }

        @media (min-width: 768px) {
            .modal-image {
                height: 600px;
            }
        }

        .modal-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .modal-nav {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 48px;
            height: 48px;
            background: rgba(0, 0, 0, 0.5);
            border: none;
            border-radius: 50%;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            font-size: 1.5rem;
        }

        .modal-nav:hover {
            background: rgba(220, 38, 38, 0.5);
        }

        .modal-nav.prev {
            left: 1rem;
        }

        .modal-nav.next {
            right: 1rem;
        }

        .modal-counter {
            position: absolute;
            bottom: 1rem;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px);
            padding: 0.5rem 1rem;
            border-radius: 9999px;
            font-size: 0.875rem;
            color: white;
        }

        .modal-content-side {
            padding: 2rem 3rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        @media (max-width: 768px) {
            .modal-content-side {
                padding: 2rem;
            }
        }

        .modal-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(220, 38, 38, 0.1);
            border: 1px solid rgba(220, 38, 38, 0.3);
            border-radius: 9999px;
            padding: 0.25rem 0.75rem;
            width: fit-content;
            margin-bottom: 1rem;
        }

        .modal-badge span {
            color: rgba(248, 113, 113, 0.9);
            font-size: 0.75rem;
            font-weight: bold;
        }

        .modal h2 {
            font-size: clamp(1.875rem, 5vw, 3rem);
            font-weight: bold;
            margin-bottom: 0.5rem;
            background: linear-gradient(to right, #f87171, #fb7185);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .modal-tagline {
            color: rgba(249, 115, 147, 0.9);
            font-size: 1.125rem;
            font-style: italic;
            margin-bottom: 1rem;
        }

        .modal-description {
            color: rgba(209, 213, 219, 0.9);
            font-size: 1.125rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }

        .modal-highlights {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
            margin-bottom: 2rem;
        }

        .highlight {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            color: rgba(249, 115, 147, 0.9);
        }

        .highlight-icon {
            font-size: 1.25rem;
            color: rgba(220, 38, 38, 0.9);
            flex-shrink: 0;
        }

        /* Footer */
        footer {
            border-top: 1px solid rgba(220, 38, 38, 0.1);
            background: rgba(0, 0, 0, 0.4);
            padding: 3rem 1rem;
            text-align: center;
            position: relative;
            z-index: 10;
        }

        .footer-logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .footer-logo span {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(to right, #f87171, #fb7185);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        footer p {
            color: rgba(249, 115, 147, 0.6);
            font-size: 0.875rem;
            margin-bottom: 0.5rem;
        }

        /* Mobile CTA */
        .mobile-cta {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(to top, #000, rgba(0, 0, 0, 0.95), transparent);
            padding: 1rem;
            z-index: 30;
        }

        @media (min-width: 768px) {
            .mobile-cta {
                display: none;
            }
        }

        .mobile-cta a {
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            background: linear-gradient(to right, #dc2626, #ec4899);
            color: white;
            font-weight: bold;
            padding: 1rem;
            border-radius: 9999px;
            text-decoration: none;
            box-shadow: 0 10px 15px -3px rgba(220, 38, 38, 0.25);
            animation: pulse 2s ease-in-out infinite;
        }

        @media (max-width: 768px) {
            body {
                padding-bottom: 80px;
            }
        }
    </style>
</head>
<body>
    <div class="bg-effects"></div>

    <!-- Header -->
    <header id="header">
        <div class="header-content">
            <div class="logo">
                <div class="logo-icon">ðŸ”¥</div>
                <div class="logo-text">
                    <h1>Grupo Privado</h1>
                    <p>ConteÃºdo Exclusivo +18</p>
                </div>
            </div>
            <a href="https://t.me/+Xj4Rvh71WsxhMGJh" target="_blank" class="header-btn">
                ðŸ’¬ Entrar Agora ðŸ”¥
            </a>
        </div>
    </header>

    <!-- Age Verification Modal -->
    <div class="age-modal" id="ageModal">
        <div class="age-modal-content">
            <div class="age-icon">ðŸ”ž</div>
            <h2>ConteÃºdo Adulto</h2>
            <p>Este site contÃ©m material sexualmente explÃ­cito destinado apenas a adultos. VocÃª deve ter 18 anos ou mais para continuar.</p>
            <div class="age-buttons">
                <button class="btn-confirm" onclick="allowAccess()">Sim, tenho 18+ anos ðŸ”¥</button>
                <button class="btn-decline" onclick="denyAccess()">NÃ£o, sair do site</button>
            </div>
            <p class="age-disclaimer">Ao entrar, vocÃª concorda com nossos termos de uso e confirma ser maior de idade.</p>
        </div>
    </div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="hero-badge">
                <span>âœ¨ +18 ConteÃºdo Exclusivo</span>
            </div>
            <h2>Quer Ser Feliz?</h2>
            <p>Acesse meus conteÃºdos mais quentes e exclusivos. <strong style="color: rgba(248, 113, 113, 0.9);">Sem censura, sem limites.</strong></p>
            <div class="hero-cta">
                <a href="https://t.me/+Xj4Rvh71WsxhMGJh" target="_blank" class="btn-primary">
                    <span>â¤ï¸</span>
                    <span>ðŸ”¥ Acessa Aqui Safadinho ðŸ”¥</span>
                    <span>âœ¨</span>
                </a>
            </div>
            <div class="hero-stats">
                <div class="stat">
                    <span>ðŸ‘ï¸</span>
                    <span>+50k VisualizaÃ§Ãµes</span>
                </div>
                <div class="stat">
                    <span>ðŸ”’</span>
                    <span>100% Privado</span>
                </div>
                <div class="stat">
                    <span>ðŸ”¥</span>
                    <span>ConteÃºdo DiÃ¡rio</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery">
        <div class="gallery-header">
            <h3>Preview Exclusivo</h3>
            <p>Clique nas imagens para ver mais detalhes. <strong style="color: rgba(248, 113, 113, 0.9);">O conteÃºdo completo estÃ¡ no grupo privado.</strong></p>
        </div>
        <div class="gallery-grid">
            <div class="gallery-item" onclick="openModal(0)">
                <div class="gallery-image">
                    <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/FFpPshJIkJZnzISl.png" alt="Fasano Ipanema">
                    <div class="gallery-overlay"></div>
                    <div class="gallery-badge">
                        <span>ðŸ”’ EXCLUSIVO</span>
                    </div>
                    <div class="gallery-content">
                        <h4>Fasano Ipanema</h4>
                        <p>"Onde o luxo encontra a tentaÃ§Ã£o"</p>
                        <div class="gallery-more">
                            <span>ðŸ‘ï¸</span>
                            <span>Ver mais</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="gallery-item" onclick="openModal(1)">
                <div class="gallery-image">
                    <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/FXZoSMLGhheuflrr.png" alt="Joatinga Paradise">
                    <div class="gallery-overlay"></div>
                    <div class="gallery-badge">
                        <span>ðŸ”’ EXCLUSIVO</span>
                    </div>
                    <div class="gallery-content">
                        <h4>Joatinga Paradise</h4>
                        <p>"PrÃ³ximo demais para ser real"</p>
                        <div class="gallery-more">
                            <span>ðŸ‘ï¸</span>
                            <span>Ver mais</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="gallery-item" onclick="openModal(2)">
                <div class="gallery-image">
                    <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/uzfGmDsKfcRJHVYX.png" alt="Copacabana Palace">
                    <div class="gallery-overlay"></div>
                    <div class="gallery-badge">
                        <span>ðŸ”’ EXCLUSIVO</span>
                    </div>
                    <div class="gallery-content">
                        <h4>Copacabana Palace</h4>
                        <p>"ElegÃ¢ncia que provoca"</p>
                        <div class="gallery-more">
                            <span>ðŸ‘ï¸</span>
                            <span>Ver mais</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="cta-content">
            <div class="cta-icon">â¤ï¸</div>
            <h3>Vem Ser Feliz Comigo</h3>
            <p>NÃ£o perca tempo. O conteÃºdo mais quente e exclusivo te espera do outro lado. <strong style="color: rgba(248, 113, 113, 0.9);">Clique agora e venha se divertir.</strong></p>
            <a href="https://t.me/+Xj4Rvh71WsxhMGJh" target="_blank" class="cta-button">
                <span>ðŸ’¬</span>
                <span>ðŸ”¥ Acessa Aqui Safadinho ðŸ”¥</span>
            </a>
            <p class="cta-disclaimer">ðŸ”ž ConteÃºdo +18 | Acesso Imediato | 100% AnÃ´nimo</p>
        </div>
    </section>

    <!-- Features -->
    <section class="features">
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">ðŸ”’</div>
                <h4>Privacidade Total</h4>
                <p>Seus dados 100% protegidos e anÃ´nimos</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">ðŸ”¥</div>
                <h4>ConteÃºdo Quente</h4>
                <p>Fotos e vÃ­deos sem censura todos os dias</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">ðŸ’¬</div>
                <h4>Chat Direto</h4>
                <p>Converse diretamente comigo no privado</p>
            </div>
        </div>
    </section>

    <!-- Modal -->
    <div class="modal hidden" id="modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">âœ•</button>
            <div class="modal-grid">
                <div class="modal-image">
                    <img id="modalImage" src="" alt="">
                    <button class="modal-nav prev" onclick="prevImage()">â€¹</button>
                    <button class="modal-nav next" onclick="nextImage()">â€º</button>
                    <div class="modal-counter">
                        <span id="imageCounter">1</span> / 3
                    </div>
                </div>
                <div class="modal-content-side">
                    <div class="modal-badge">
                        <span>ðŸ”’ CONTEÃšDO EXCLUSIVO</span>
                    </div>
                    <h2 id="modalTitle">TÃ­tulo</h2>
                    <p class="modal-tagline" id="modalTagline">Tagline</p>
                    <p class="modal-description" id="modalDescription">DescriÃ§Ã£o</p>
                    <div class="modal-highlights">
                        <div class="highlight" id="highlight1">
                            <span class="highlight-icon">ðŸ”¥</span>
                            <span>Highlight 1</span>
                        </div>
                        <div class="highlight" id="highlight2">
                            <span class="highlight-icon">ðŸ”¥</span>
                            <span>Highlight 2</span>
                        </div>
                        <div class="highlight" id="highlight3">
                            <span class="highlight-icon">ðŸ”¥</span>
                            <span>Highlight 3</span>
                        </div>
                    </div>
                    <a href="https://t.me/+Xj4Rvh71WsxhMGJh" target="_blank" class="cta-button">
                        <span>â¤ï¸</span>
                        <span>ðŸ”¥ Quero Ver Tudo ðŸ”¥</span>
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Mobile CTA -->
    <div class="mobile-cta">
        <a href="https://t.me/+Xj4Rvh71WsxhMGJh" target="_blank">
            <span>ðŸ’¬</span>
            <span>ðŸ”¥ Acessa Aqui Safadinho ðŸ”¥</span>
        </a>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-logo">
            <span>ðŸ”¥</span>
            <span>Grupo Privado</span>
        </div>
        <p>ðŸ”ž ConteÃºdo destinado a maiores de 18 anos</p>
        <p>Â© 2026 Todos os direitos reservados. Acesse o conteÃºdo exclusivo via Telegram.</p>
    </footer>

    <script>
        const galleryData = [
            {
                title: "Fasano Ipanema",
                tagline: "Onde o luxo encontra a tentaÃ§Ã£o",
                description: "Mergulhe em uma experiÃªncia visual que desperta todos os sentidos. Cada imagem Ã© uma celebraÃ§Ã£o da sensualidade e do prazer, capturada em momentos Ãºnicos de pura tentaÃ§Ã£o. Um refÃºgio onde seus desejos mais secretos ganham vida.",
                image: "https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/FFpPshJIkJZnzISl.png",
                highlights: ["ConteÃºdo sem censura", "Acesso imediato", "AtualizaÃ§Ãµes diÃ¡rias"]
            },
            {
                title: "Joatinga Paradise",
                tagline: "PrÃ³ximo demais para ser real",
                description: "Escape para um mundo de intimidade absoluta onde a frontalidade encontra a arte. Momentos capturados com intensidade, onde vocÃª pode se entregar completamente ao prazer da observaÃ§Ã£o. Um lugar onde fantasias se tornam visuais.",
                image: "https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/FXZoSMLGhheuflrr.png",
                highlights: ["ConteÃºdo +18 garantido", "Chat privado disponÃ­vel", "Material inÃ©dito"]
            },
            {
                title: "Copacabana Palace",
                tagline: "ElegÃ¢ncia que provoca",
                description: "A sofisticaÃ§Ã£o da seduÃ§Ã£o em sua forma mais pura. Cada detalhe pensado para provocar, cada imagem criada para seduzir. Viva a experiÃªncia que transcende o comum e entrega o extraordinÃ¡rio do prazer visual.",
                image: "https://files.manuscdn.com/user_upload_by_module/session_file/310519663134978826/uzfGmDsKfcRJHVYX.png",
                highlights: ["Ensaios profissionais", "Qualidade 4K", "ConteÃºdo VIP"]
            }
        ];

        let currentModalIndex = 0;

        function allowAccess() {
            document.getElementById('ageModal').classList.add('hidden');
            localStorage.setItem('ageVerified', 'true');
        }

        function denyAccess() {
            window.location.href = 'https://www.google.com';
        }

        function openModal(index) {
            currentModalIndex = index;
            const data = galleryData[index];
            document.getElementById('modalImage').src = data.image;
            document.getElementById('modalTitle').textContent = data.title;
            document.getElementById('modalTagline').textContent = `"${data.tagline}"`;
            document.getElementById('modalDescription').textContent = data.description;
            document.getElementById('highlight1').innerHTML = `<span class="highlight-icon">ðŸ”¥</span><span>${data.highlights[0]}</span>`;
            document.getElementById('highlight2').innerHTML = `<span class="highlight-icon">ðŸ”¥</span><span>${data.highlights[1]}</span>`;
            document.getElementById('highlight3').innerHTML = `<span class="highlight-icon">ðŸ”¥</span><span>${data.highlights[2]}</span>`;
            document.getElementById('imageCounter').textContent = index + 1;
            document.getElementById('modal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
        }

        function nextImage() {
            currentModalIndex = (currentModalIndex + 1) % galleryData.length;
            const data = galleryData[currentModalIndex];
            document.getElementById('modalImage').src = data.image;
            document.getElementById('imageCounter').textContent = currentModalIndex + 1;
        }

        function prevImage() {
            currentModalIndex = (currentModalIndex - 1 + galleryData.length) % galleryData.length;
            const data = galleryData[currentModalIndex];
            document.getElementById('modalImage').src = data.image;
            document.getElementById('imageCounter').textContent = currentModalIndex + 1;
        }

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Check age verification on load
        window.addEventListener('load', () => {
            if (localStorage.getItem('ageVerified') === 'true') {
                document.getElementById('ageModal').classList.add('hidden');
            }
        });

        // Close modal on background click
        document.getElementById('modal').addEventListener('click', (e) => {
            if (e.target.id === 'modal') {
                closeModal();
            }
        });
    </script>
</body>
</html>

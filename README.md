<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kim Chang-woo | Data Analyst</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,400;500;600;700&family=Noto+Sans+KR:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* CSS Variables - MiniMax Design System */
        :root {
            --colors-canvas: #ffffff;
            --colors-surface: #f9f9fa;
            --colors-primary: #000000;
            --colors-on-primary: #ffffff;
            --colors-ink: #000000;
            --colors-charcoal: #333333;
            --colors-steel: #666666;
            --colors-muted: #999999;
            --colors-hairline: #e5e5e5;
            
            /* Vibrant Product Colors */
            --colors-brand-coral: linear-gradient(135deg, #ff5757, #ff8e53);
            --colors-brand-magenta: linear-gradient(135deg, #e00078, #ff4da6);
            --colors-brand-blue: linear-gradient(135deg, #0044ff, #0099ff);
            
            /* Typography */
            --font-family: 'DM Sans', 'Noto Sans KR', sans-serif;
            
            /* Spacing */
            --spacing-xs: 8px;
            --spacing-sm: 12px;
            --spacing-md: 16px;
            --spacing-xl: 24px;
            --spacing-xxl: 32px;
            --spacing-section: 64px;
            --spacing-hero: 96px;
            
            /* Radius */
            --rounded-full: 9999px;
            --rounded-xl: 16px;
            --rounded-hero: 32px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        body {
            background-color: var(--colors-canvas);
            color: var(--colors-ink);
            font-family: var(--font-family);
            line-height: 1.5;
        }

        /* Container */
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 32px;
        }

        /* Top Navigation */
        .top-nav {
            position: sticky;
            top: 0;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(8px);
            border-bottom: 1px solid var(--colors-hairline);
            height: 64px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            z-index: 100;
            padding: 0 32px;
        }

        .nav-logo {
            font-size: 20px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 11px 24px;
            border-radius: var(--rounded-full);
            font-size: 14px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: opacity 0.2s;
        }

        .btn:hover { opacity: 0.8; }

        .btn-primary {
            background-color: var(--colors-primary);
            color: var(--colors-on-primary);
            border: none;
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--colors-ink);
            border: 1px solid var(--colors-ink);
        }

        /* Badges */
        .badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: var(--rounded-full);
            font-size: 13px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .badge-coral { background: #ff5757; color: #fff; }
        .badge-blue { background: #e6f0ff; color: #0044ff; }

        /* Typography System */
        .hero-display {
            font-size: 80px;
            font-weight: 600;
            line-height: 1.10;
            letter-spacing: -2px;
            margin-bottom: var(--spacing-xl);
        }

        .display-lg {
            font-size: 56px;
            font-weight: 600;
            line-height: 1.10;
            letter-spacing: -1.5px;
            margin-bottom: var(--spacing-md);
        }

        .heading-lg {
            font-size: 40px;
            font-weight: 600;
            line-height: 1.20;
            letter-spacing: -1px;
            margin-bottom: var(--spacing-md);
        }

        .subtitle {
            font-size: 18px;
            font-weight: 500;
            line-height: 1.50;
            color: var(--colors-steel);
        }

        /* Hero Section */
        .hero-section {
            padding-top: var(--spacing-hero);
            padding-bottom: var(--spacing-hero);
            text-align: center;
        }

        .hero-actions {
            display: flex;
            gap: 16px;
            justify-content: center;
            margin-top: 40px;
        }

        /* White Info Cards */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 32px;
            margin-bottom: var(--spacing-hero);
        }

        .card-white {
            background-color: var(--colors-canvas);
            border: 1px solid var(--colors-hairline);
            border-radius: var(--rounded-xl);
            padding: var(--spacing-xxl);
        }

        .card-white h3 {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 16px;
        }
        
        .card-white p, .card-white li {
            color: var(--colors-charcoal);
            margin-bottom: 8px;
            font-size: 16px;
        }

        .card-white ul {
            list-style-position: inside;
        }

        /* Vibrant Product Matrix */
        .product-section {
            padding: var(--spacing-section) 0 var(--spacing-hero);
        }

        .matrix-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 32px;
        }

        .product-card {
            border-radius: var(--rounded-hero);
            padding: 40px 32px;
            color: var(--colors-on-primary);
            display: flex;
            flex-direction: column;
            min-height: 420px;
        }

        .product-coral { background: var(--colors-brand-coral); }
        .product-magenta { background: var(--colors-brand-magenta); }
        .product-blue { background: var(--colors-brand-blue); }

        .product-card .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: auto;
        }

        .product-card h3 {
            font-size: 40px;
            font-weight: 600;
            line-height: 1.1;
            letter-spacing: -1px;
            margin-top: 24px;
        }

        .product-card p {
            font-size: 16px;
            opacity: 0.9;
            margin-top: 16px;
            line-height: 1.5;
        }

        .insight-box {
            background: rgba(255, 255, 255, 0.15);
            border-radius: var(--rounded-xl);
            padding: 16px;
            margin-top: 24px;
            font-size: 14px;
            backdrop-filter: blur(4px);
        }

        /* Footer */
        .footer {
            background-color: var(--colors-primary);
            color: var(--colors-on-primary);
            padding: var(--spacing-section) 32px;
            text-align: center;
        }
        
        .footer p { color: var(--colors-muted); font-size: 14px; }
    </style>
</head>
<body>

    <nav class="top-nav">
        <div class="nav-logo">Kim Chang-woo.</div>
        <div>
            <a href="mailto:kcw3875@gmail.com" class="btn btn-primary">Contact Me</a>
        </div>
    </nav>

    <div class="container">
        <header class="hero-section">
            <span class="badge badge-blue" style="margin-bottom: 24px;">Data Analyst</span>
            <h1 class="hero-display">Logic Meets<br>Data Infrastructure.</h1>
            <p class="subtitle">산업경영공학의 프로세스 최적화 관점으로 비즈니스 인텔리전스를 구축합니다.</p>
            
            <div class="hero-actions">
                <a href="#projects" class="btn btn-primary">View Models & Projects</a>
                <a href="#" class="btn btn-secondary">Download Resume</a>
            </div>
        </header>

        <section class="info-grid">
            <div class="card-white">
                <h3>System Identity</h3>
                <p><strong>Name</strong> : 김창우 (Kim Chang-woo)</p>
                <p><strong>Major</strong> : 산업경영공학과 (Industrial Management Engineering)</p>
                <p><strong>Role</strong> : Data Analyst</p>
                <p><strong>Contact</strong> : kcw3875@gmail.com</p>
            </div>
            <div class="card-white">
                <h3>Technical Specifications</h3>
                <ul>
                    <li><strong>ADsP</strong> (데이터 분석 준전문가)</li>
                    <li><strong>Six Sigma Green Belt</strong> (프로세스 개선 및 품질 관리)</li>
                    <li><strong>컴퓨터활용능력 2급</strong> (데이터 스프레드시트 관리)</li>
                    <li><strong>Data Stack</strong> : Python, Pandas, Scikit-learn, OpenAI API</li>
                </ul>
            </div>
        </section>

        <section id="projects" class="product-section">
            <h2 class="heading-lg" style="text-align: center;">Full-Stack Project Matrix</h2>
            <p class="subtitle" style="text-align: center; margin-bottom: 64px;">세 가지 고유의 데이터 프로덕트 라인업</p>
            
            <div class="matrix-grid">
                <div class="product-card product-coral">
                    <div class="card-header">
                        <span class="badge badge-coral" style="background:#fff; color:#ff5757;">PUBLIC DATA</span>
                        <span>26.04</span>
                    </div>
                    <h3>Urban<br>Parking 1.0</h3>
                    <p><strong>주차 구역 최적화 분석</strong><br>양천구 및 서초구의 주정차 단속 데이터를 활용하여 주차장 최적 입지를 탐색하고, 히트맵 기반 시각화 파이프라인을 구축했습니다.</p>
                    <div class="insight-box">
                        <strong>Insight:</strong> 데이터 분석이 단순 수치 산출을 넘어 실제 공간 정책 제안으로 이어지기 위한 현실적 변수 제어의 중요성을 체감했습니다.
                    </div>
                </div>

                <div class="product-card product-magenta">
                    <div class="card-header">
                        <span class="badge" style="background:#fff; color:#e00078;">DEEP LEARNING</span>
                        <span>26.04</span>
                    </div>
                    <h3>Super<br>Conductor 2.0</h3>
                    <p><strong>초전도체 특성 예측 모델링</strong><br>머신러닝 및 딥러닝 회귀 모델의 Baseline을 직접 구축하고, 다양한 하이퍼파라미터 튜닝을 통해 모델 간 성능을 비교 및 개선했습니다.</p>
                    <div class="insight-box">
                        <strong>Insight:</strong> 모델의 아키텍처 복잡도보다, 목적에 맞는 데이터 전처리(Preprocessing) 논리가 성능 향상에 더 결정적인 영향을 미침을 확인했습니다.
                    </div>
                </div>

                <div class="product-card product-blue">
                    <div class="card-header">
                        <span class="badge" style="background:#fff; color:#0044ff;">AI AGENT</span>
                        <span>26.05</span>
                    </div>
                    <h3>AIVLE<br>Assistant 3.0</h3>
                    <p><strong>업무 자동화 개인비서 구축</strong><br>조장으로서 팀 프로젝트를 리드하며, OpenAI API의 LLM과 구글 캘린더 연동을 통해 자연어로 구동되는 지능형 일정 관리 시스템을 개발했습니다.</p>
                    <div class="insight-box">
                        <strong>Insight:</strong> 외부 API 통합을 통한 SaaS형 서비스 확장 구조를 설계하며, 인프라 구축에 대한 기술적 자신감을 얻었습니다.
                    </div>
                </div>
            </div>
        </section>
    </div>

    <footer class="footer">
        <h2 style="font-size: 24px; font-weight: 600; margin-bottom: 8px;">Kim Chang-woo</h2>
        <p>intelligence with data engineering</p>
    </footer>

</body>
</html>

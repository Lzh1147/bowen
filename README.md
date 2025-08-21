<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>广州博文知识产权代理有限公司 - 专业医学科研服务平台</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #0066cc;
            --secondary-color: #004499;
            --accent-color: #00a8ff;
            --text-dark: #333;
            --text-light: #666;
            --bg-light: #f8f9fa;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Microsoft YaHei', sans-serif;
            color: var(--text-dark);
            line-height: 1.6;
        }

        /* 导航栏样式 */
        .navbar {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .navbar-brand {
            font-weight: bold;
            color: var(--primary-color) !important;
            font-size: 1.5rem;
        }

        .nav-link {
            color: var(--text-dark) !important;
            font-weight: 500;
            margin: 0 10px;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-link:hover {
            color: var(--primary-color) !important;
        }

        .nav-link.external-link {
            color: var(--accent-color) !important;
        }

        .nav-link.external-link::after {
            content: '↗';
            font-size: 0.8em;
            margin-left: 3px;
        }

        /* 英雄区域 */
        .hero-section {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 100px 0;
            position: relative;
            overflow: hidden;
        }

        .hero-section::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.3; }
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero-title {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 20px;
            animation: fadeInUp 0.8s ease;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            animation: fadeInUp 0.8s ease 0.2s both;
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

        .badge-trusted {
            background-color: rgba(255,255,255,0.2);
            padding: 10px 20px;
            border-radius: 30px;
            display: inline-block;
            animation: fadeInUp 0.8s ease 0.4s both;
        }

        /* 业务范围卡片 */
        .service-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            height: 100%;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
            transform: translateX(-100%);
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .service-card:hover::before {
            transform: translateX(0);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .service-number {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 2rem;
            font-weight: bold;
            color: var(--accent-color);
            opacity: 0.3;
        }

        /* 优势部分 */
        .advantage-section {
            background-color: var(--bg-light);
            padding: 80px 0;
        }

        .advantage-item {
            background: white;
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 20px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        .advantage-item:hover {
            transform: translateX(10px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .advantage-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        /* 服务详情 */
        .service-detail {
            padding: 80px 0;
        }

        .service-detail-card {
            background: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            margin-bottom: 40px;
        }

        .feature-list {
            list-style: none;
            padding: 0;
        }

        .feature-list li {
            padding: 10px 0;
            padding-left: 30px;
            position: relative;
        }

        .feature-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }

        /* IF趋势图表格样式 */
        .if-trend-container {
            background: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            margin-top: 30px;
        }

        .if-trend-title {
            text-align: center;
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--text-dark);
            margin-bottom: 10px;
        }

        .if-trend-subtitle {
            text-align: center;
            color: var(--text-light);
            font-size: 1rem;
            margin-bottom: 30px;
        }

        .if-trend-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 14px;
        }

        .if-trend-table th {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 15px 10px;
            text-align: center;
            font-weight: 600;
            border: none;
        }

        .if-trend-table th:first-child {
            border-top-left-radius: 10px;
            text-align: left;
            padding-left: 20px;
        }

        .if-trend-table th:last-child {
            border-top-right-radius: 10px;
        }

        .if-trend-table td {
            padding: 12px 10px;
            text-align: center;
            border-bottom: 1px solid #f0f0f0;
        }

        .if-trend-table td:first-child {
            text-align: left;
            padding-left: 20px;
            font-weight: 500;
            color: var(--text-dark);
        }

        .if-trend-table tr:hover {
            background-color: #f8f9fa;
        }

        .if-trend-table tr:last-child td {
            border-bottom: none;
        }

        .if-value {
            font-weight: 600;
            padding: 4px 8px;
            border-radius: 4px;
            display: inline-block;
            min-width: 45px;
        }

        .if-high {
            background-color: #e8f5e9;
            color: #2e7d32;
        }

        .if-medium {
            background-color: #fff3e0;
            color: #ef6c00;
        }

        .if-low {
            background-color: #ffebee;
            color: #c62828;
        }

        .trend-arrow {
            font-size: 12px;
            margin-left: 3px;
        }

        .trend-up {
            color: #2e7d32;
        }

        .trend-down {
            color: #c62828;
        }

        .trend-stable {
            color: #ef6c00;
        }

        .journal-category {
            display: inline-block;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 500;
            margin-left: 10px;
        }

        .category-q1 {
            background-color: #e8f5e9;
            color: #2e7d32;
        }

        .category-q2 {
            background-color: #e3f2fd;
            color: #1565c0;
        }

        .category-q3 {
            background-color: #fff3e0;
            color: #ef6c00;
        }

        .category-q4 {
            background-color: #ffebee;
            color: #c62828;
        }

        .table-legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 13px;
            color: #666;
        }

        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 3px;
        }

        /* 页脚 */
        footer {
            background-color: var(--secondary-color);
            color: white;
            padding: 50px 0 30px;
        }

        .footer-widget h5 {
            margin-bottom: 20px;
            font-weight: bold;
        }

        .footer-widget ul {
            list-style: none;
            padding: 0;
        }

        .footer-widget ul li {
            margin-bottom: 10px;
        }

        .footer-widget ul li a {
            color: rgba(255,255,255,0.8);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-widget ul li a:hover {
            color: white;
        }

        .footer-widget ul li a.external-link {
            color: var(--accent-color);
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2rem;
            }
            .hero-subtitle {
                font-size: 1.2rem;
            }
            .if-trend-table {
                font-size: 12px;
            }
            .if-trend-table th,
            .if-trend-table td {
                padding: 8px 5px;
            }
            .if-trend-table td:first-child {
                padding-left: 10px;
            }
            .journal-category {
                display: block;
                margin-left: 0;
                margin-top: 3px;
            }
        }

        /* 动画效果 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* 表格动画 */
        .table-row {
            opacity: 0;
            transform: translateX(-20px);
            transition: all 0.5s ease;
        }

        .table-row.visible {
            opacity: 1;
            transform: translateX(0);
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar navbar-expand-lg navbar-light fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="bi bi-hospital"></i> 广州博文
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#home">首页</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">公司简介</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#services">业务范围</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#advantages">我们的优势</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">联系我们</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link external-link" href="http://www.yixuekeyanfudao.cn" target="_blank">辅导资源</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- 英雄区域 -->
    <section id="home" class="hero-section">
        <div class="container">
            <div class="hero-content">
                <h1 class="hero-title">专业医学科研服务平台</h1>
                <p class="hero-subtitle">广州博文知识产权代理有限公司 - 老品牌 值得信赖</p>
                <div class="badge-trusted">
                    <i class="bi bi-shield-check"></i> 2024年合并升级 | 医学科研服务专家
                </div>
            </div>
        </div>
    </section>

    <!-- 公司简介 -->
    <section id="about" class="py-5">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 fade-in">
                    <h2 class="mb-4">公司简介</h2>
                    <p class="lead">广州博文知识产权代理有限公司位于广州市番禺区东荟创新园，于2024年合并广州博文信息咨询有限公司和广州博医汇生物科技有限公司。</p>
                    <p>作为国内较早从事医学科研服务品牌之一，我们专门为医学工作者提供优质的科研服务。科研团队由来自全国知名医学院硕博导师和研究员组成，拥有强大的科研理论与实践经验。</p>
                    <p>我们为医务人员提供医学专利申请、医学期刊出版、医学著作出版、课题立项、科普发表等咨询辅助服务。清楚当前各医学工作者所面临的困境和挑战，致力做最专业的医学科研发展平台，为广大医护人员提供优质的服务体验。</p>
                </div>
                <div class="col-lg-6 fade-in">
                    <img src="https://picsum.photos/seed/medical-research/600/400.jpg" alt="医学科研" class="img-fluid rounded shadow">
                </div>
            </div>
        </div>
    </section>

    <!-- 业务范围 -->
    <section id="services" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">业务范围</h2>
            <div class="row g-4">
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="service-card">
                        <span class="service-number">1</span>
                        <div class="service-icon">
                            <i class="bi bi-journal-medical"></i>
                        </div>
                        <h4>国内外期刊发表</h4>
                        <p>提供北大核心、科技核心、SCI等国内外期刊发表服务，确保文章真实可查</p>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="service-card">
                        <span class="service-number">2</span>
                        <div class="service-icon">
                            <i class="bi bi-clipboard-data"></i>
                        </div>
                        <h4>医学课题申请立项</h4>
                        <p>携手资深专家，提供专业课题申报服务，提高立项成功率</p>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="service-card">
                        <span class="service-number">3</span>
                        <div class="service-icon">
                            <i class="bi bi-book"></i>
                        </div>
                        <h4>著作出书</h4>
                        <p>与多家权威出版社合作，提供独著、主编、副主编等多种出书方式</p>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="service-card">
                        <span class="service-number">4</span>
                        <div class="service-icon">
                            <i class="bi bi-shield-lock"></i>
                        </div>
                        <h4>专利申请代理</h4>
                        <p>专业代理发明专利、实用新型专利，开通优先审核通道</p>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="service-card">
                        <span class="service-number">5</span>
                        <div class="service-icon">
                            <i class="bi bi-megaphone"></i>
                        </div>
                        <h4>科普作品</h4>
                        <p>医学杂志、正规报刊、公众号科普发表，覆盖多种传播渠道</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 我们的优势 -->
    <section id="advantages" class="advantage-section">
        <div class="container">
            <h2 class="text-center mb-5">我们的优势</h2>
            <div class="row">
                <div class="col-md-6 fade-in">
                    <div class="advantage-item">
                        <div class="d-flex align-items-start">
                            <div class="advantage-icon">
                                <i class="bi bi-newspaper"></i>
                            </div>
                            <div>
                                <h4>医学核心期刊合作</h4>
                                <p>明确了解期刊收稿刊期及要求，确保合作周期稳妥</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 fade-in">
                    <div class="advantage-item">
                        <div class="d-flex align-items-start">
                            <div class="advantage-icon">
                                <i class="bi bi-building"></i>
                            </div>
                            <div>
                                <h4>著作出版社合作</h4>
                                <p>多家权威出版社直接签约合作，确保出版顺利</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 fade-in">
                    <div class="advantage-item">
                        <div class="d-flex align-items-start">
                            <div class="advantage-icon">
                                <i class="bi bi-lightning"></i>
                            </div>
                            <div>
                                <h4>知识产权局优先审查</h4>
                                <p>优先审查通道，百分百授权</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 fade-in">
                    <div class="advantage-item">
                        <div class="d-flex align-items-start">
                            <div class="advantage-icon">
                                <i class="bi bi-graph-up"></i>
                            </div>
                            <div>
                                <h4>SCI独立评测系统</h4>
                                <p>全行业唯一有独立评测期刊稳定性系统，时刻精准了解期刊动态</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- SCI期刊IF趋势图表格 -->
            <div class="row mt-5">
                <div class="col-12 fade-in">
                    <div class="if-trend-container">
                        <h3 class="if-trend-title">SCI期刊近年IF趋势图</h3>
                        <p class="if-trend-subtitle">精选医学领域SCI期刊影响因子变化趋势分析（2019-2023）</p>
                        
                        <div class="table-responsive">
                            <table class="if-trend-table">
                                <thead>
                                    <tr>
                                        <th>期刊名称</th>
                                        <th>2019 IF</th>
                                        <th>2020 IF</th>
                                        <th>2021 IF</th>
                                        <th>2022 IF</th>
                                        <th>2023 IF</th>
                                        <th>趋势</th>
                                        <th>分区</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr class="table-row">
                                        <td>
                                            Nature Medicine
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">53.44</span></td>
                                        <td><span class="if-value if-high">67.54</span></td>
                                        <td><span class="if-value if-high">87.24</span></td>
                                        <td><span class="if-value if-high">82.90</span></td>
                                        <td><span class="if-value if-high">58.70</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            New England Journal of Medicine
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">74.69</span></td>
                                        <td><span class="if-value if-high">91.25</span></td>
                                        <td><span class="if-value if-high">176.08</span></td>
                                        <td><span class="if-value if-high">158.50</span></td>
                                        <td><span class="if-value if-high">96.20</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            The Lancet
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">60.39</span></td>
                                        <td><span class="if-value if-high">79.32</span></td>
                                        <td><span class="if-value if-high">202.73</span></td>
                                        <td><span class="if-value if-high">168.90</span></td>
                                        <td><span class="if-value if-high">98.40</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            JAMA
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">45.54</span></td>
                                        <td><span class="if-value if-high">56.27</span></td>
                                        <td><span class="if-value if-high">157.34</span></td>
                                        <td><span class="if-value if-high">120.70</span></td>
                                        <td><span class="if-value if-high">63.10</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            BMJ
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">30.22</span></td>
                                        <td><span class="if-value if-high">39.89</span></td>
                                        <td><span class="if-value if-high">93.33</span></td>
                                        <td><span class="if-value if-high">105.70</span></td>
                                        <td><span class="if-value if-high">93.60</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Cell
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">36.22</span></td>
                                        <td><span class="if-value if-high">41.58</span></td>
                                        <td><span class="if-value if-high">66.85</span></td>
                                        <td><span class="if-value if-high">59.90</span></td>
                                        <td><span class="if-value if-high">45.50</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Cancer Cell
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">26.02</span></td>
                                        <td><span class="if-value if-high">31.74</span></td>
                                        <td><span class="if-value if-high">50.17</span></td>
                                        <td><span class="if-value if-high">38.80</span></td>
                                        <td><span class="if-value if-high">48.80</span></td>
                                        <td><span class="trend-arrow trend-up">↑</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Nature Reviews Cancer
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">53.03</span></td>
                                        <td><span class="if-value if-high">60.72</span></td>
                                        <td><span class="if-value if-high">69.80</span></td>
                                        <td><span class="if-value if-high">78.40</span></td>
                                        <td><span class="if-value if-high">78.50</span></td>
                                        <td><span class="trend-arrow trend-stable">→</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Journal of Clinical Oncology
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">28.24</span></td>
                                        <td><span class="if-value if-high">32.96</span></td>
                                        <td><span class="if-value if-high">44.54</span></td>
                                        <td><span class="if-value if-high">42.10</span></td>
                                        <td><span class="if-value if-medium">42.10</span></td>
                                        <td><span class="trend-arrow trend-stable">→</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Annals of Internal Medicine
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">21.32</span></td>
                                        <td><span class="if-value if-high">25.39</span></td>
                                        <td><span class="if-value if-high">51.60</span></td>
                                        <td><span class="if-value if-medium">39.20</span></td>
                                        <td><span class="if-value if-medium">39.20</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Gut
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-high">17.94</span></td>
                                        <td><span class="if-value if-high">19.82</span></td>
                                        <td><span class="if-value if-medium">23.06</span></td>
                                        <td><span class="if-value if-medium">24.50</span></td>
                                        <td><span class="if-value if-medium">24.50</span></td>
                                        <td><span class="trend-arrow trend-stable">→</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Hepatology
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-medium">14.97</span></td>
                                        <td><span class="if-value if-medium">17.43</span></td>
                                        <td><span class="if-value if-medium">17.30</span></td>
                                        <td><span class="if-value if-medium">13.50</span></td>
                                        <td><span class="if-value if-medium">13.50</span></td>
                                        <td><span class="trend-arrow trend-down">↓</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Journal of Hepatology
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-medium">12.49</span></td>
                                        <td><span class="if-value if-medium">15.84</span></td>
                                        <td><span class="if-value if-medium">19.94</span></td>
                                        <td><span class="if-value if-medium">25.70</span></td>
                                        <td><span class="if-value if-medium">25.70</span></td>
                                        <td><span class="trend-arrow trend-up">↑</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            Circulation
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-medium">18.88</span></td>
                                        <td><span class="if-value if-medium">23.60</span></td>
                                        <td><span class="if-value if-medium">30.84</span></td>
                                        <td><span class="if-value if-medium">37.80</span></td>
                                        <td><span class="if-value if-medium">37.80</span></td>
                                        <td><span class="trend-arrow trend-up">↑</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                    <tr class="table-row">
                                        <td>
                                            European Heart Journal
                                            <span class="journal-category category-q1">Q1</span>
                                        </td>
                                        <td><span class="if-value if-medium">16.62</span></td>
                                        <td><span class="if-value if-medium">22.67</span></td>
                                        <td><span class="if-value if-medium">35.85</span></td>
                                        <td><span class="if-value if-medium">39.30</span></td>
                                        <td><span class="if-value if-medium">39.30</span></td>
                                        <td><span class="trend-arrow trend-up">↑</span></td>
                                        <td><span class="if-value if-high">Q1</span></td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>

                        <!-- 图例说明 -->
                        <div class="table-legend">
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #e8f5e9;"></div>
                                <span>高IF (>20)</span>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #fff3e0;"></div>
                                <span>中等IF (10-20)</span>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #ffebee;"></div>
                                <span>低IF (<10)</span>
                            </div>
                            <div class="legend-item">
                                <i class="bi bi-arrow-up" style="color: #2e7d32;"></i>
                                <span>上升趋势</span>
                            </div>
                            <div class="legend-item">
                                <i class="bi bi-arrow-down" style="color: #c62828;"></i>
                                <span>下降趋势</span>
                            </div>
                            <div class="legend-item">
                                <i class="bi bi-arrow-right" style="color: #ef6c00;"></i>
                                <span>稳定趋势</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 服务详情 -->
    <section class="service-detail">
        <div class="container">
            <h2 class="text-center mb-5">服务详情</h2>
            
            <!-- 国内核心期刊发表服务 -->
            <div class="service-detail-card fade-in">
                <h3><i class="bi bi-journal-text"></i> 国内核心期刊发表服务</h3>
                <div class="row mt-4">
                    <div class="col-md-6">
                        <h5>服务特点</h5>
                        <ul class="feature-list">
                            <li>北大核心、CSCD、科技核心写作+发表</li>
                            <li>量身定制，临床稿件按单位常见病例统计分析</li>
                            <li>涉及实验全部真实实验，大部分期刊已开通加急通道</li>
                            <li>直接对接社内编辑团队，全程系统投稿</li>
                            <li>完整投稿记录，确保真实可查，出刊时效保证</li>
                        </ul>
                    </div>
                    <div class="col-md-6">
                        <h5>收稿要求</h5>
                        <div class="mb-3">
                            <strong>北大核心：</strong>对文章的新颖度及作者单位的科研能力有较高的要求，需要三甲以及有课题支撑，重复率要求5%左右，正常刊期需要提前两年准备。
                        </div>
                        <div>
                            <strong>科技核心：</strong>对文章的新颖度及作者单位的科研能力也有一定要求，重复率要求10%以内，正常刊期需要提前两年准备。
                        </div>
                    </div>
                </div>
            </div>

            <!-- 课题基金申报立项服务 -->
            <div class="service-detail-card fade-in">
                <h3><i class="bi bi-clipboard2-pulse"></i> 课题基金申报立项服务</h3>
                <div class="row mt-4">
                    <div class="col-md-4">
                        <div class="text-center">
                            <div class="advantage-icon mx-auto mb-3">
                                <i class="bi bi-person-badge"></i>
                            </div>
                            <h5>专业对口专家定制</h5>
                            <p>熟悉当前热议，丰富的临床及基础实验经验</p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="text-center">
                            <div class="advantage-icon mx-auto mb-3">
                                <i class="bi bi-gear"></i>
                            </div>
                            <h5>细节化优质体验</h5>
                            <p>10年以上基金评审经验专家一对一高效服务</p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="text-center">
                            <div class="advantage-icon mx-auto mb-3">
                                <i class="bi bi-file-earmark-check"></i>
                            </div>
                            <h5>交付整套方案</h5>
                            <p>确保方案可行性，最大化提高立项几率</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 著作出书合作与协调 -->
            <div class="service-detail-card fade-in">
                <h3><i class="bi bi-book-half"></i> 著作出书合作与协调</h3>
                <div class="row mt-4">
                    <div class="col-md-3">
                        <div class="text-center">
                            <h4>独著出书</h4>
                            <p>作者可独自承包，或全部作者指定安排，周期快</p>
                        </div>
                    </div>
                    <div class="col-md-3">
                        <div class="text-center">
                            <h4>主编拼书</h4>
                            <p>同专业作者拼书，负责章节可调整，从第一主编到第六主编不等</p>
                        </div>
                    </div>
                    <div class="col-md-3">
                        <div class="text-center">
                            <h4>副主编</h4>
                            <p>负责字符可按要求增加，周期短</p>
                        </div>
                    </div>
                    <div class="col-md-3">
                        <div class="text-center">
                            <h4>编委</h4>
                            <p>多书可选，性价比高，ISBN/CIP齐全</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">联系我们</h2>
            <div class="row">
                <div class="col-md-4 text-center fade-in">
                    <div class="advantage-icon mx-auto mb-3">
                        <i class="bi bi-geo-alt"></i>
                    </div>
                    <h5>公司地址</h5>
                    <p>广州市番禺区东荟创新园</p>
                </div>
                <div class="col-md-4 text-center fade-in">
                    <div class="advantage-icon mx-auto mb-3">
                        <i class="bi bi-telephone"></i>
                    </div>
                    <h5>联系电话</h5>
                    <p>400-XXX-XXXX</p>
                </div>
                <div class="col-md-4 text-center fade-in">
                    <div class="advantage-icon mx-auto mb-3">
                        <i class="bi bi-envelope"></i>
                    </div>
                    <h5>电子邮箱</h5>
                    <p>info@bowen-ip.com</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h5>关于我们</h5>
                        <p>广州博文知识产权代理有限公司是国内较早从事医学科研服务品牌之一，致力于为广大医护人员提供优质的科研服务。</p>
                        <div class="mt-3">
                            <span class="badge bg-secondary me-2">安全靠谱</span>
                            <span class="badge bg-secondary me-2">正规机构</span>
                            <span class="badge bg-secondary me-2">实力雄厚</span>
                            <span class="badge bg-secondary">价格合理</span>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h5>快速链接</h5>
                        <ul>
                            <li><a href="#home">首页</a></li>
                            <li><a href="#about">公司简介</a></li>
                            <li><a href="#services">业务范围</a></li>
                            <li><a href="#advantages">我们的优势</a></li>
                            <li><a href="#contact">联系我们</a></li>
                            <li><a href="http://www.yixuekeyanfudao.cn" target="_blank" class="external-link">辅导资源</a></li>
                        </ul>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h5>服务承诺</h5>
                        <ul>
                            <li>成果转换 - 提高医学科研成果转换</li>
                            <li>安全 - 恪守职业道德底线</li>
                            <li>目标 - 打造全国最专业的中国医学科研平台</li>
                            <li>渠道优势 - 一手代理，实惠靠谱</li>
                        </ul>
                    </div>
                </div>
            </div>
            <hr class="my-4" style="border-color: rgba(255,255,255,0.2);">
            <div class="text-center">
                <p>&copy; 2024 广州博文知识产权代理有限公司. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // 滚动动画
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // 表格行动画
        const tableRows = document.querySelectorAll('.table-row');
        const tableObserver = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.classList.add('visible');
                    }, index * 100);
                    tableObserver.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });

        tableRows.forEach(row => {
            tableObserver.observe(row);
        });

        // 导航栏滚动效果
        window.addEventListener('scroll', () => {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.padding = '10px 0';
                navbar.style.boxShadow = '0 2px 20px rgba(0,0,0,0.1)';
            } else {
                navbar.style.padding = '15px 0';
                navbar.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
            }
        });

        // 平滑滚动
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
    </script>
</body>
</html>

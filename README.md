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
            content: '?';
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }

        /* 统计图表 */
        .chart-container {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            height: 400px;
            position: relative;
        }

        .bar {
            position: absolute;
            bottom: 50px;
            width: 60px;
            background: linear-gradient(to top, var(--primary-color), var(--accent-color));
            border-radius: 5px 5px 0 0;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .bar:hover {
            opacity: 0.8;
            transform: scaleY(1.05);
        }

        .bar-1 { left: 50px; height: 108px; }
        .bar-2 { left: 130px; height: 128px; }
        .bar-3 { left: 210px; height: 32px; }
        .bar-4 { left: 290px; height: 24px; }
        .bar-5 { left: 370px; height: 76px; }
        .bar-6 { left: 450px; height: 96px; }
        .bar-7 { left: 530px; height: 100px; }
        .bar-8 { left: 610px; height: 112px; }

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
            .bar {
                width: 40px;
            }
            .bar-1 { left: 20px; }
            .bar-2 { left: 70px; }
            .bar-3 { left: 120px; }
            .bar-4 { left: 170px; }
            .bar-5 { left: 220px; }
            .bar-6 { left: 270px; }
            .bar-7 { left: 320px; }
            .bar-8 { left: 370px; }
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

            <!-- 统计图表 -->
            <div class="row mt-5">
                <div class="col-12 fade-in">
                    <h3 class="text-center mb-4">期刊稳定性评测数据</h3>
                    <div class="chart-container">
                        <div class="bar bar-1" title="2.7"></div>
                        <div class="bar bar-2" title="3.2"></div>
                        <div class="bar bar-3" title="0.8"></div>
                        <div class="bar bar-4" title="0.6"></div>
                        <div class="bar bar-5" title="1.9"></div>
                        <div class="bar bar-6" title="2.4"></div>
                        <div class="bar bar-7" title="2.5"></div>
                        <div class="bar bar-8" title="2.8"></div>
                        <div style="position: absolute; bottom: 20px; left: 0; right: 0; text-align: center; color: #666;">
                            投稿增长比、国人占比、影响因子变化、自引率等动态因素
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

        // 图表悬停效果
        document.querySelectorAll('.bar').forEach(bar => {
            bar.addEventListener('mouseenter', function() {
                const value = this.getAttribute('title');
                this.style.position = 'relative';
                this.innerHTML = `<span style="position: absolute; top: -25px; left: 50%; transform: translateX(-50%); background: #333; color: white; padding: 2px 8px; border-radius: 3px; font-size: 12px;">${value}</span>`;
            });
            
            bar.addEventListener('mouseleave', function() {
                this.innerHTML = '';
            });
        });
    </script>
</body>
</html>

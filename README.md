<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>计算科学研究实验室 - 学术网站</title>
    <!-- 引入Tailwind CSS用于快速构建样式 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入Font Awesome图标库 -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- 自定义配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // 学术风格配色：深蓝为主色，灰色系为辅助色
                        primary: '#0F4C81',    // 深蓝 - 专业、稳重
                        secondary: '#4A6FA5',  // 浅蓝 - 辅助色
                        neutral: '#F5F7FA',    // 浅灰 - 背景色
                        dark: '#2C3E50',       // 深灰 - 文本色
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-balance {
                text-wrap: balance;
            }
            .section-padding {
                padding: clamp(2rem, 5vw, 4rem) 0;
            }
        }
        
        /* 基础样式 */
        body {
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            color: #2C3E50;
            line-height: 1.6;
        }
        
        /* 学术卡片悬停效果 */
        .academic-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .academic-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-neutral">
    <!-- 导航栏 -->
    <header class="bg-white shadow-sm sticky top-0 z-50">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4">
                <!-- 网站Logo/名称 -->
                <a href="#" class="flex items-center space-x-2">
                    <i class="fa fa-flask text-primary text-2xl"></i>
                    <span class="text-xl font-semibold text-dark">计算科学研究实验室</span>
                </a>
                
                <!-- 桌面端导航 -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#home" class="text-dark hover:text-primary transition-colors font-medium">首页</a>
                    <a href="#research" class="text-dark hover:text-primary transition-colors font-medium">研究方向</a>
                    <a href="#publications" class="text-dark hover:text-primary transition-colors font-medium">发表论文</a>
                    <a href="#team" class="text-dark hover:text-primary transition-colors font-medium">研究团队</a>
                    <a href="#contact" class="text-dark hover:text-primary transition-colors font-medium">联系我们</a>
                </nav>
                
                <!-- 移动端菜单按钮 -->
                <button id="menuBtn" class="md:hidden text-dark text-xl">
                    <i class="fa fa-bars"></i>
                </button>
            </div>
            
            <!-- 移动端导航菜单 -->
            <div id="mobileMenu" class="md:hidden hidden pb-4">
                <nav class="flex flex-col space-y-4">
                    <a href="#home" class="text-dark hover:text-primary transition-colors font-medium">首页</a>
                    <a href="#research" class="text-dark hover:text-primary transition-colors font-medium">研究方向</a>
                    <a href="#publications" class="text-dark hover:text-primary transition-colors font-medium">发表论文</a>
                    <a href="#team" class="text-dark hover:text-primary transition-colors font-medium">研究团队</a>
                    <a href="#contact" class="text-dark hover:text-primary transition-colors font-medium">联系我们</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section id="home" class="bg-primary text-white py-16 md:py-24">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="max-w-3xl mx-auto text-center">
                <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-6">推进计算科学的前沿研究</h1>
                <p class="text-lg md:text-xl opacity-90 mb-8 text-balance">
                    我们致力于高性能计算、人工智能算法和数据科学领域的基础与应用研究，
                    为解决复杂科学问题提供创新的计算方法和技术方案。
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#research" class="bg-white text-primary px-6 py-3 rounded-md font-medium hover:bg-opacity-90 transition-colors">
                        探索研究方向
                    </a>
                    <a href="#contact" class="bg-transparent border border-white px-6 py-3 rounded-md font-medium hover:bg-white hover:bg-opacity-10 transition-colors">
                        合作与咨询
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 研究方向 -->
    <section id="research" class="section-padding bg-white">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-2xl md:text-3xl font-bold text-dark mb-4">研究方向</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-gray-600">
                    我们的研究聚焦于计算科学的核心领域，结合理论创新与实际应用，解决关键科学问题
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 研究方向1 -->
                <div class="academic-card bg-neutral p-6 rounded-lg shadow-sm">
                    <div class="text-primary text-3xl mb-4">
                        <i class="fa fa-superpowers"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-dark">高性能计算</h3>
                    <p class="text-gray-600">
                        研究大规模并行计算架构、数值算法优化和高性能计算应用，提升科学计算的效率和规模。
                    </p>
                </div>
                
                <!-- 研究方向2 -->
                <div class="academic-card bg-neutral p-6 rounded-lg shadow-sm">
                    <div class="text-primary text-3xl mb-4">
                        <i class="fa fa-brain"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-dark">人工智能算法</h3>
                    <p class="text-gray-600">
                        开发适用于科学计算的机器学习和深度学习算法，解决复杂的非线性问题和数据驱动的科学发现。
                    </p>
                </div>
                
                <!-- 研究方向3 -->
                <div class="academic-card bg-neutral p-6 rounded-lg shadow-sm">
                    <div class="text-primary text-3xl mb-4">
                        <i class="fa fa-database"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-dark">数据科学</h3>
                    <p class="text-gray-600">
                        研究大规模科学数据的管理、分析和可视化方法，挖掘数据中的科学规律和知识。
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- 发表论文 -->
    <section id="publications" class="section-padding bg-neutral">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-2xl md:text-3xl font-bold text-dark mb-4">发表论文</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-gray-600">
                    我们的研究成果发表在国际顶级学术期刊和会议上，推动相关领域的学术发展
                </p>
            </div>
            
            <div class="space-y-6 max-w-4xl mx-auto">
                <!-- 论文1 -->
                <div class="academic-card bg-white p-6 rounded-lg shadow-sm">
                    <div class="flex flex-col md:flex-row md:items-center justify-between mb-3">
                        <h3 class="text-lg font-semibold text-dark">
                            基于深度学习的大规模流体模拟加速方法
                        </h3>
                        <span class="text-sm text-primary font-medium bg-primary/10 px-3 py-1 rounded-full inline-block mt-2 md:mt-0">
                            Nature Computing, 2025
                        </span>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Zhang, L., Wang, H., & Li, J. (2025). 提出了一种新型深度学习框架，将流体模拟的计算效率提升了两个数量级。
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-file-pdf-o mr-2"></i> PDF
                        </a>
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-link mr-2"></i> 原文链接
                        </a>
                    </div>
                </div>
                
                <!-- 论文2 -->
                <div class="academic-card bg-white p-6 rounded-lg shadow-sm">
                    <div class="flex flex-col md:flex-row md:items-center justify-between mb-3">
                        <h3 class="text-lg font-semibold text-dark">
                            异构计算架构下的并行数值算法优化研究
                        </h3>
                        <span class="text-sm text-primary font-medium bg-primary/10 px-3 py-1 rounded-full inline-block mt-2 md:mt-0">
                            IEEE TPDS, 2024
                        </span>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Wang, H., Zhang, L., & Chen, Y. (2024). 针对GPU-CPU异构架构设计了自适应并行算法，显著提升了科学计算的性能。
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-file-pdf-o mr-2"></i> PDF
                        </a>
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-link mr-2"></i> 原文链接
                        </a>
                    </div>
                </div>
                
                <!-- 论文3 -->
                <div class="academic-card bg-white p-6 rounded-lg shadow-sm">
                    <div class="flex flex-col md:flex-row md:items-center justify-between mb-3">
                        <h3 class="text-lg font-semibold text-dark">
                            大数据驱动的科学发现：方法与应用
                        </h3>
                        <span class="text-sm text-primary font-medium bg-primary/10 px-3 py-1 rounded-full inline-block mt-2 md:mt-0">
                            Science Data, 2024
                        </span>
                    </div>
                    <p class="text-gray-600 mb-4">
                        Li, J., Wang, H., & Zhang, L. (2024). 提出了面向科学数据的特征提取和知识发现方法，应用于多个学科领域。
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-file-pdf-o mr-2"></i> PDF
                        </a>
                        <a href="#" class="text-primary hover:text-primary/80 flex items-center">
                            <i class="fa fa-link mr-2"></i> 原文链接
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-8">
                <a href="#" class="inline-block text-primary hover:text-primary/80 font-medium">
                    查看更多论文 <i class="fa fa-arrow-right ml-1"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- 研究团队 -->
    <section id="team" class="section-padding bg-white">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-2xl md:text-3xl font-bold text-dark mb-4">研究团队</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-gray-600">
                    我们拥有一支由资深教授、青年研究员和优秀博士生组成的研究团队
                </p>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- 团队成员1 -->
                <div class="academic-card text-center">
                    <div class="bg-neutral rounded-full w-40 h-40 mx-auto mb-4 flex items-center justify-center">
                        <i class="fa fa-user text-6xl text-primary/70"></i>
                    </div>
                    <h3 class="text-lg font-semibold text-dark mb-1">张明教授</h3>
                    <p class="text-primary mb-3">团队负责人 / 博导</p>
                    <p class="text-gray-600 text-sm mb-4">
                        研究方向：高性能计算、并行算法
                    </p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-envelope"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-google"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-researchgate"></i></a>
                    </div>
                </div>
                
                <!-- 团队成员2 -->
                <div class="academic-card text-center">
                    <div class="bg-neutral rounded-full w-40 h-40 mx-auto mb-4 flex items-center justify-center">
                        <i class="fa fa-user text-6xl text-primary/70"></i>
                    </div>
                    <h3 class="text-lg font-semibold text-dark mb-1">李华 副教授</h3>
                    <p class="text-primary mb-3">青年研究员</p>
                    <p class="text-gray-600 text-sm mb-4">
                        研究方向：人工智能、机器学习
                    </p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-envelope"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-google"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-researchgate"></i></a>
                    </div>
                </div>
                
                <!-- 团队成员3 -->
                <div class="academic-card text-center">
                    <div class="bg-neutral rounded-full w-40 h-40 mx-auto mb-4 flex items-center justify-center">
                        <i class="fa fa-user text-6xl text-primary/70"></i>
                    </div>
                    <h3 class="text-lg font-semibold text-dark mb-1">王强 博士</h3>
                    <p class="text-primary mb-3">博士后</p>
                    <p class="text-gray-600 text-sm mb-4">
                        研究方向：数据科学、数值模拟
                    </p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-envelope"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-google"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-researchgate"></i></a>
                    </div>
                </div>
                
                <!-- 团队成员4 -->
                <div class="academic-card text-center">
                    <div class="bg-neutral rounded-full w-40 h-40 mx-auto mb-4 flex items-center justify-center">
                        <i class="fa fa-user text-6xl text-primary/70"></i>
                    </div>
                    <h3 class="text-lg font-semibold text-dark mb-1">赵晓 同学</h3>
                    <p class="text-primary mb-3">博士研究生</p>
                    <p class="text-gray-600 text-sm mb-4">
                        研究方向：深度学习、科学计算
                    </p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-envelope"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-google"></i></a>
                        <a href="#" class="text-gray-500 hover:text-primary"><i class="fa fa-github"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact" class="section-padding bg-neutral">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-2xl md:text-3xl font-bold text-dark mb-4">联系我们</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-gray-600">
                    如果您对我们的研究感兴趣，或者希望开展合作研究，请通过以下方式联系我们
                </p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <!-- 联系信息 -->
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h3 class="text-xl font-semibold text-dark mb-6">联系方式</h3>
                    
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="text-primary text-xl mt-1 mr-4">
                                <i class="fa fa-map-marker"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-dark">地址</h4>
                                <p class="text-gray-600">北京市海淀区中关村南大街5号 计算科学大楼 508室</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="text-primary text-xl mt-1 mr-4">
                                <i class="fa fa-envelope"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-dark">邮箱</h4>
                                <p class="text-gray-600">research@computelab.edu.cn</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="text-primary text-xl mt-1 mr-4">
                                <i class="fa fa-phone"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-dark">电话</h4>
                                <p class="text-gray-600">+86 (10) 8888-7777</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="text-primary text-xl mt-1 mr-4">
                                <i class="fa fa-clock-o"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-dark">工作时间</h4>
                                <p class="text-gray-600">周一至周五: 9:00 - 17:30</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-8">
                        <h4 class="font-medium text-dark mb-3">关注我们</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="w-10 h-10 rounded-full bg-primary text-white flex items-center justify-center hover:bg-primary/90 transition-colors">
                                <i class="fa fa-weixin"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-primary text-white flex items-center justify-center hover:bg-primary/90 transition-colors">
                                <i class="fa fa-weibo"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-primary text-white flex items-center justify-center hover:bg-primary/90 transition-colors">
                                <i class="fa fa-github"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-primary text-white flex items-center justify-center hover:bg-primary/90 transition-colors">
                                <i class="fa fa-google"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 联系表单 -->
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <h3 class="text-xl font-semibold text-dark mb-6">发送消息</h3>
                    
                    <form>
                        <div class="mb-4">
                            <label for="name" class="block text-gray-700 font-medium mb-2">姓名</label>
                            <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary" placeholder="请输入您的姓名">
                        </div>
                        
                        <div class="mb-4">
                            <label for="email" class="block text-gray-700 font-medium mb-2">邮箱</label>
                            <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary" placeholder="请输入您的邮箱地址">
                        </div>
                        
                        <div class="mb-4">
                            <label for="subject" class="block text-gray-700 font-medium mb-2">主题</label>
                            <input type="text" id="subject" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary" placeholder="请输入消息主题">
                        </div>
                        
                        <div class="mb-6">
                            <label for="message" class="block text-gray-700 font-medium mb-2">消息内容</label>
                            <textarea id="message" rows="4" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary" placeholder="请输入您的消息内容"></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-primary text-white py-3 rounded-md font-medium hover:bg-primary/90 transition-colors">
                            发送消息
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <i class="fa fa-flask text-primary text-2xl"></i>
                        <span class="text-xl font-semibold">计算科学研究实验室</span>
                    </div>
                    <p class="text-gray-400 mb-4">
                        致力于推进计算科学的前沿研究与应用
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-weixin"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-weibo"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-github"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-google"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">快速链接</h4>
                    <ul class="space-y-2">
                        <li><a href="#home" class="text-gray-400 hover:text-white transition-colors">首页</a></li>
                        <li><a href="#research" class="text-gray-400 hover:text-white transition-colors">研究方向</a></li>
                        <li><a href="#publications" class="text-gray-400 hover:text-white transition-colors">发表论文</a></li>
                        <li><a href="#team" class="text-gray-400 hover:text-white transition-colors">研究团队</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition-colors">联系我们</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">相关资源</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">研究数据</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">代码仓库</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">学术合作</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">招生信息</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">资助项目</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">联系信息</h4>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fa fa-map-marker text-primary mt-1 mr-2"></i>
                            <span class="text-gray-400">北京市海淀区中关村南大街5号</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fa fa-envelope text-primary mt-1 mr-2"></i>
                            <span class="text-gray-400">research@computelab.edu.cn</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fa fa-phone text-primary mt-1 mr-2"></i>
                            <span class="text-gray-400">+86 (10) 8888-7777</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-10 pt-6 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm">© 2025 计算科学研究实验室. 保留所有权利.</p>
                <div class="mt-4 md:mt-0">
                    <a href="#" class="text-gray-400 hover:text-white text-sm mr-4 transition-colors">隐私政策</a>
                    <a href="#" class="text-gray-400 hover:text-white text-sm transition-colors">使用条款</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // 移动端菜单切换
        document.getElementById('menuBtn').addEventListener('click', function() {
            const mobileMenu = document.getElementById('mobileMenu');
            mobileMenu.classList.toggle('hidden');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                // 关闭移动端菜单
                document.getElementById('mobileMenu').classList.add('hidden');
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80, // 偏移量，避免被导航栏遮挡
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.classList.add('shadow-md');
                header.classList.remove('shadow-sm');
            } else {
                header.classList.remove('shadow-md');
                header.classList.add('shadow-sm');
            }
        });
        
        // 表单提交处理
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('消息发送成功！我们将尽快回复您。');
            this.reset();
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>全国硕士研究生招生考试初试成绩查询系统</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
            background-color: #f5f5f5;
        }
        .chsi-blue {
            background-color: #12519A;
        }
        .text-chsi-blue {
            color: #12519A;
        }
        .nav-item:hover {
            color: #ff9900;
        }
        .tab-active {
            background-color: #0c4284;
            color: white;
        }
        .tab-inactive {
            background-color: #9cb1ce;
            color: #333;
        }
        /* 模拟图2页面的轻微背景纹理 */
        .result-bg {
            background-color: #f0f2f5;
            background-image: radial-gradient(#d1d5db 1px, transparent 1px);
            background-size: 20px 20px;
        }
        /* 表格线样式 */
        .score-table th, .score-table td {
            border-bottom: 1px dashed #ccc;
        }
        .score-table tr:last-child td {
            border-bottom: none;
        }
        /* 顶部横幅装饰 */
        .banner-bg {
            background: linear-gradient(135deg, #2196F3 0%, #1976D2 100%);
            position: relative;
        }
        .banner-dots {
            position: absolute;
            left: 10%;
            top: 50%;
            transform: translateY(-50%);
            width: 40px;
            height: 60px;
            background-image: radial-gradient(white 2px, transparent 2px);
            background-size: 10px 10px;
            opacity: 0.3;
        }
        /* 网格边框处理 */
        .grid-wrapper {
            border-left: 1px solid #e5e7eb;
            border-top: 1px solid #e5e7eb;
        }
        .grid-item {
            border-right: 1px solid #e5e7eb;
            border-bottom: 1px solid #e5e7eb;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col text-gray-800">

    <header class="bg-white border-b border-gray-200 hidden md:block">
        <div class="max-w-[1200px] mx-auto px-4 flex justify-between items-center h-10 text-xs text-gray-500">
            <div class="flex space-x-4">
                <a class="hover:text-blue-600 cursor-pointer">学信网</a>
                <a class="hover:text-blue-600 cursor-pointer">阳光高考</a>
                <a class="hover:text-blue-600 cursor-pointer">研招网</a>
                <a class="hover:text-blue-600 cursor-pointer">学职平台</a>
            </div>
            <div class="flex space-x-4">
                <a class="hover:text-blue-600 cursor-pointer">登录</a>
                <span class="text-gray-300">|</span>
                <a class="hover:text-blue-600 cursor-pointer">注册</a>
                <span class="text-gray-300">|</span>
                <a class="hover:text-blue-600 cursor-pointer">帮助中心</a>
            </div>
        </div>
    </header>

    <div id="step1-select" class="flex-grow w-full bg-white">
        <div class="banner-bg w-full py-12 text-center text-white">
            <div class="banner-dots hidden md:block"></div>
            <h1 class="text-[32px] font-bold tracking-wider mb-4">2026年部分考生初试成绩查询</h1>
            <p class="text-sm opacity-90 tracking-wide">本系统所有数据均为招生单位提供，招生单位对查询结果负责解释。</p>
        </div>

        <div class="max-w-[1200px] mx-auto px-4 py-8">
            <div class="bg-[#fafafa] p-6 border border-gray-100 flex flex-wrap gap-x-6 gap-y-4 text-[14px] text-gray-600 leading-loose">
                <span class="cursor-pointer hover:text-blue-600">北京</span>
                <span class="cursor-pointer hover:text-blue-600">天津</span>
                <span class="cursor-pointer hover:text-blue-600">河北</span>
                <span class="cursor-pointer hover:text-blue-600">山西</span>
                <span class="cursor-pointer hover:text-blue-600">内蒙古</span>
                <span class="cursor-pointer hover:text-blue-600">辽宁</span>
                <span class="cursor-pointer hover:text-blue-600">吉林</span>
                <span class="cursor-pointer hover:text-blue-600">黑龙江</span>
                <span class="cursor-pointer hover:text-blue-600">上海</span>
                <span class="cursor-pointer hover:text-blue-600">江苏</span>
                <span class="cursor-pointer hover:text-blue-600">浙江</span>
                <span class="cursor-pointer hover:text-blue-600">安徽</span>
                <span class="cursor-pointer hover:text-blue-600">福建</span>
                <span class="cursor-pointer hover:text-blue-600">江西</span>
                <span class="cursor-pointer hover:text-blue-600">山东</span>
                <span class="bg-[#1890ff] text-white px-2 py-0.5 rounded cursor-pointer">河南</span>
                <span class="cursor-pointer hover:text-blue-600">湖北</span>
                <span class="cursor-pointer hover:text-blue-600">湖南</span>
                <span class="cursor-pointer hover:text-blue-600">广东</span>
                <span class="cursor-pointer hover:text-blue-600">广西</span>
                <span class="cursor-pointer hover:text-blue-600">海南</span>
                <span class="cursor-pointer hover:text-blue-600">重庆</span>
                <span class="cursor-pointer hover:text-blue-600">四川</span>
                <span class="cursor-pointer hover:text-blue-600">贵州</span>
                <span class="cursor-pointer hover:text-blue-600">云南</span>
                <span class="cursor-pointer hover:text-blue-600">西藏</span>
                <span class="cursor-pointer hover:text-blue-600">陕西</span>
                <span class="cursor-pointer hover:text-blue-600">甘肃</span>
                <span class="cursor-pointer hover:text-blue-600">青海</span>
                <span class="cursor-pointer hover:text-blue-600">宁夏</span>
                <span class="cursor-pointer hover:text-blue-600">新疆</span>
            </div>

            <div class="mt-6 border border-gray-200 bg-white">
                <div class="p-4 border-b border-gray-200 text-lg font-bold">
                    <span class="text-[#1890ff]">河南</span> <span class="text-gray-700">成绩查询</span>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 text-[14px] text-black grid-wrapper">
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10078)华北水利水电大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10459)郑州大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10460)河南理工大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10462)郑州轻工业大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10463)河南工业大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10464)河南科技大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10465)中原工学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10466)河南农业大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10467)河南科技学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10471)河南中医药大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10472)河南医药大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10475)河南大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition" onclick="goToStep2()">(10476)河南师范大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10477)信阳师范大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10479)安阳师范学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10481)南阳师范学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10482)洛阳师范学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10484)河南财经政法大学</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10485)郑州航空工业管理学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(10919)平顶山学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(11765)河南城建学院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(82606)中钢集团洛阳耐火材料研究院</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(82708)机械科学研究总院(郑州机械研究所)</div>
                    <div class="p-5 grid-item hover:text-[#1890ff] cursor-pointer transition">(82907)中国航空研究院(014中心)</div>
                </div>
            </div>
        </div>
    </div>

    <div id="step2-form" class="hidden flex-grow bg-white shadow-sm pb-16">
        <div class="max-w-[1200px] mx-auto">
            <div class="text-sm text-gray-500 px-4 py-3 border-b border-gray-200">
                位置：首页 > 研究生教育 > 招生信息 > 成绩查询
            </div>
            
            <div class="flex border-b-4 border-[#0c4284] bg-gray-100 pl-4">
                <div class="px-8 py-3 tab-inactive cursor-pointer font-medium mt-2 rounded-t-sm">考试大纲</div>
                <div class="px-8 py-3 tab-active cursor-pointer font-medium mt-2 ml-1 rounded-t-sm">成绩查询</div>
            </div>

            <div class="mt-16 max-w-2xl mx-auto px-4">
                <h1 class="text-2xl font-bold text-center mb-10 tracking-widest text-gray-800">硕士研究生初试成绩查询</h1>
                
                <form onsubmit="goToStep3(event)" class="space-y-6">
                    <div class="flex items-center justify-center">
                        <label class="w-24 text-right pr-4 text-gray-600 text-sm">姓名：</label>
                        <input type="text" id="studentName" required class="border border-gray-300 px-3 py-1.5 w-72 focus:outline-none focus:border-blue-500 transition shadow-sm">
                    </div>
                    
                    <div class="flex items-center justify-center">
                        <label class="w-24 text-right pr-4 text-gray-600 text-sm">考生编号：</label>
                        <input type="text" id="studentId" required class="border border-gray-300 px-3 py-1.5 w-72 focus:outline-none focus:border-blue-500 transition shadow-sm">
                    </div>

                    <div class="flex justify-center space-x-6 pt-6">
                        <button type="submit" class="bg-[#0c4284] text-white px-8 py-1.5 text-sm cursor-pointer hover:bg-blue-800 transition">查询</button>
                        <button type="reset" class="bg-[#0c4284] text-white px-8 py-1.5 text-sm cursor-pointer hover:bg-blue-800 transition">重置</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <div id="step3-result" class="hidden flex-grow justify-center items-start pt-10 pb-20 result-bg">
        <div class="w-full max-w-4xl bg-white shadow-lg p-12 border border-gray-200 relative min-h-[500px]">
            
            <h3 class="text-lg font-bold mb-8 text-gray-800">初试科目及成绩：</h3>
            
            <table class="w-full score-table mb-12 text-gray-700 text-[15px]">
                <thead>
                    <tr>
                        <th class="text-left font-normal py-4 px-12 w-2/3">科目代码及名称</th>
                        <th class="text-center font-normal py-4 w-1/3">成绩</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="py-5 px-12">[101] 思想政治理论</td>
                        <td class="text-center">78</td>
                    </tr>
                    <tr>
                        <td class="py-5 px-12">[204] 英语（二）</td>
                        <td class="text-center">79</td>
                    </tr>
                    <tr>
                        <td class="py-5 px-12">[333] 教育综合</td>
                        <td class="text-center">132</td>
                    </tr>
                    <tr>
                        <td class="py-5 px-12">[860] 心理健康教育</td>
                        <td class="text-center">137</td>
                    </tr>
                    <tr>
                        <td class="py-5 px-12">总分</td>
                        <td class="text-center">426</td>
                    </tr>
                </tbody>
            </table>

            <div class="mt-16 flex flex-col items-center">
                <div id="qrcode" class="border-[3px] border-white shadow-sm p-1 bg-white min-w-[90px] min-h-[90px] flex items-center justify-center">
                    </div>
                <div class="text-[10px] text-gray-400 mt-1">扫码核实成绩信息</div>
            </div>
            
        </div>
        
        <div class="absolute top-6 right-6">
            <button onclick="goBack()" class="px-4 py-2 border border-gray-300 rounded text-sm bg-white text-gray-600 hover:bg-gray-100 transition cursor-pointer shadow-sm">
                返回重新查询
            </button>
        </div>
    </div>

    <footer class="bg-gray-800 text-gray-400 py-8 mt-auto text-sm text-center border-t-4 border-blue-600">
        <div class="max-w-6xl mx-auto px-4 space-y-2">
            <p>主办单位：教育部学生服务与素质发展中心（原全国高等学校学生信息咨询与就业指导中心）</p>
            <p>Copyright © 2003-2026 学信网 All Rights Reserved</p>
            <p class="mt-4"><a class="hover:text-white transition cursor-pointer">京ICP备19004913号-1</a></p>
        </div>
    </footer>

    <script>
        const step1 = document.getElementById('step1-select');
        const step2 = document.getElementById('step2-form');
        const step3 = document.getElementById('step3-result');

        // 进入第二步
        function goToStep2() {
            step1.classList.add('hidden');
            step2.classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // 提交表单进入第三步并生成真实二维码
        function goToStep3(event) {
            event.preventDefault(); 
            
            const name = document.getElementById('studentName').value;
            const id = document.getElementById('studentId').value;
            
            // 组装扫码后显示的文字信息
            const qrText = `【研招网初试成绩核实】\n姓名：${name}\n考生编号：${id}\n总分：426\n[101]思想政治理论：78\n[204]英语（二）：79\n[333]教育综合：132\n[860]心理健康教育：137`;

            // 使用稳定可靠的 QuickChart QR API 接口，完全脱离本地 JS 库依赖，避免了未定义及溢出错误
            const qrUrl = `https://quickchart.io/qr?text=${encodeURIComponent(qrText)}&size=90&margin=0`;
            
            const qrContainer = document.getElementById('qrcode');
            qrContainer.innerHTML = '<span class="text-xs text-gray-300">加载中..</span>'; // 过渡效果
            
            // 创建并插入图片
            const img = new Image();
            img.onload = function() {
                qrContainer.innerHTML = '';
                qrContainer.appendChild(img);
            };
            img.src = qrUrl;
            img.width = 90;
            img.height = 90;
            img.alt = "扫码核查";

            // 切换页面显示
            step2.classList.add('hidden');
            step3.classList.remove('hidden');
            step3.classList.add('flex'); // 保持flex布局剧中
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        
        // 返回操作
        function goBack() {
            document.getElementById('studentName').value = '';
            document.getElementById('studentId').value = '';
            step3.classList.add('hidden');
            step3.classList.remove('flex');
            step1.classList.remove('hidden'); // 这里改为返回到最开始的省份界面，更符合逻辑
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    </script>
</body>
</html>

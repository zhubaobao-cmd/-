<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>低升糖(GI)水果红绿灯表 | 控糖减肥必看</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f0f8f0;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .container {
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            padding: 30px;
            margin-top: 20px;
        }
        
        header {
            text-align: center;
            padding-bottom: 25px;
            border-bottom: 2px solid #eaeaea;
            margin-bottom: 30px;
        }
        
        h1 {
            color: #27ae60;
            font-size: 2.5rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        h1 i {
            color: #ff6b6b;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        .gi-explanation {
            background: linear-gradient(135deg, #e3f2fd 0%, #f3e5f5 100%);
            border-left: 5px solid #3498db;
            padding: 20px;
            border-radius: 8px;
            margin: 25px 0;
        }
        
        .gi-explanation h3 {
            color: #2980b9;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .gi-explanation p {
            margin-bottom: 10px;
        }
        
        .gi-scale {
            display: flex;
            justify-content: space-between;
            margin: 30px 0;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .gi-level {
            flex: 1;
            min-width: 200px;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            color: white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .gi-level:hover {
            transform: translateY(-5px);
        }
        
        .gi-level.green {
            background: linear-gradient(135deg, #27ae60 0%, #2ecc71 100%);
        }
        
        .gi-level.yellow {
            background: linear-gradient(135deg, #f39c12 0%, #f1c40f 100%);
        }
        
        .gi-level.red {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
        }
        
        .gi-level i {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .gi-value {
            font-size: 2.2rem;
            font-weight: bold;
            margin: 10px 0;
        }
        
        .tabs {
            display: flex;
            margin-bottom: 30px;
            border-bottom: 2px solid #eaeaea;
            flex-wrap: wrap;
        }
        
        .tab {
            padding: 15px 30px;
            background-color: #f1f2f6;
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            color: #7f8c8d;
            transition: all 0.3s;
            border-radius: 8px 8px 0 0;
            margin-right: 5px;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tab.active {
            background-color: white;
            color: #2c3e50;
            border-bottom: 3px solid;
            position: relative;
            top: 2px;
        }
        
        .tab.green.active {
            border-bottom-color: #27ae60;
        }
        
        .tab.yellow.active {
            border-bottom-color: #f39c12;
        }
        
        .tab.red.active {
            border-bottom-color: #e74c3c;
        }
        
        .tab:hover:not(.active) {
            background-color: #e4e5e9;
        }
        
        .table-container {
            overflow-x: auto;
            margin-bottom: 40px;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        
        th {
            color: white;
            padding: 18px 15px;
            text-align: left;
            font-weight: 600;
            position: sticky;
            top: 0;
        }
        
        .green th {
            background-color: #27ae60;
        }
        
        .yellow th {
            background-color: #f39c12;
        }
        
        .red th {
            background-color: #e74c3c;
        }
        
        td {
            padding: 18px 15px;
            border-bottom: 1px solid #eaeaea;
        }
        
        tr:hover {
            background-color: #f9f9f9;
        }
        
        .fruit-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            margin-right: 10px;
            font-size: 1.2rem;
            color: white;
        }
        
        .green .fruit-icon {
            background-color: #27ae60;
        }
        
        .yellow .fruit-icon {
            background-color: #f39c12;
        }
        
        .red .fruit-icon {
            background-color: #e74c3c;
        }
        
        .gi-badge {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 0.9rem;
        }
        
        .green .gi-badge {
            background-color: #d5f4e6;
            color: #27ae60;
        }
        
        .yellow .gi-badge {
            background-color: #fef9e7;
            color: #f39c12;
        }
        
        .red .gi-badge {
            background-color: #fadbd8;
            color: #e74c3c;
        }
        
        .warning-note {
            background-color: #fff8e1;
            border-left: 5px solid #f1c40f;
            padding: 15px;
            border-radius: 8px;
            margin: 10px 0;
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .warning-note i {
            color: #f39c12;
            margin-top: 3px;
        }
        
        .tips-section {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 25px;
            margin-top: 40px;
        }
        
        .tips-section h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .tip-card {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .tip-card:hover {
            transform: translateY(-5px);
        }
        
        .tip-card i {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: #27ae60;
        }
        
        .tip-card h4 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #eaeaea;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            .container {
                padding: 20px 15px;
            }
            
            h1 {
                font-size: 1.8rem;
                flex-direction: column;
                gap: 10px;
            }
            
            .gi-scale {
                flex-direction: column;
            }
            
            .tab {
                padding: 12px 20px;
                font-size: 1rem;
            }
            
            th, td {
                padding: 12px 8px;
                font-size: 0.9rem;
            }
            
            .tips-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fas fa-apple-alt"></i> 低升糖(GI)水果红绿灯表 🚦</h1>
            <p class="subtitle">控糖、减肥必看指南 | 科学选择水果，健康管理血糖</p>
        </header>
        
        <div class="gi-explanation">
            <h3><i class="fas fa-chart-line"></i> 什么是GI值（升糖指数）？</h3>
            <p><strong>GI值（升糖指数）</strong>是衡量食物引起血糖升高程度的指标。食物GI值越高，食用后血糖上升越快。</p>
            <p>选择低GI水果有助于：稳定血糖、减少胰岛素分泌、增强饱腹感、控制体重。</p>
        </div>
        
        <div class="gi-scale">
            <div class="gi-level green">
                <i class="fas fa-check-circle"></i>
                <h3>绿灯区</h3>
                <div class="gi-value">GI &lt; 55</div>
                <p>放心适量吃，血糖波动小</p>
                <p>减脂首选</p>
            </div>
            
            <div class="gi-level yellow">
                <i class="fas fa-exclamation-triangle"></i>
                <h3>黄灯区</h3>
                <div class="gi-value">GI 55-70</div>
                <p>控制食量吃</p>
                <p>避免饭后立即食用</p>
            </div>
            
            <div class="gi-level red">
                <i class="fas fa-times-circle"></i>
                <h3>红灯区</h3>
                <div class="gi-value">GI &gt; 70</div>
                <p>尽量少吃或避免</p>
                <p>升糖速度快</p>
            </div>
        </div>
        
        <div class="tabs">
            <button class="tab green active" onclick="showTable('green')">
                <i class="fas fa-traffic-light"></i> 🟢 绿灯区 (低GI)
            </button>
            <button class="tab yellow" onclick="showTable('yellow')">
                <i class="fas fa-traffic-light"></i> 🟡 黄灯区 (中GI)
            </button>
            <button class="tab red" onclick="showTable('red')">
                <i class="fas fa-traffic-light"></i> 🔴 红灯区 (高GI)
            </button>
        </div>
        
        <div class="table-container">
            <table id="green-table" class="green">
                <thead>
                    <tr>
                        <th width="25%">水果</th>
                        <th width="15%">GI值 (参考)</th>
                        <th width="60%">推荐理由与食用建议</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>樱桃 (车厘子)</strong>
                        </td>
                        <td><span class="gi-badge">22</span></td>
                        <td>水果界的"低GI之王"，富含花青素，抗氧化能力强，对心血管有益。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>李子/黑布林</strong>
                        </td>
                        <td><span class="gi-badge">24</span></td>
                        <td>纤维丰富，有助于肠道健康，但注意别吃太酸的伤胃。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>柚子</strong>
                        </td>
                        <td><span class="gi-badge">25</span></td>
                        <td>饱腹感强，含糖量低，非常适合加餐。柚子皮中的柚皮苷也有益健康。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-apple-alt"></i>
                            </div>
                            <strong>苹果</strong>
                        </td>
                        <td><span class="gi-badge">36</span></td>
                        <td>平价之王，带皮吃纤维更多。"一天一苹果，医生远离我"。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>梨</strong>
                        </td>
                        <td><span class="gi-badge">36</span></td>
                        <td>水分足，GI低，有润肺止咳功效，但梨皮纤维丰富，建议洗净带皮吃。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>草莓</strong>
                        </td>
                        <td><span class="gi-badge">40</span></td>
                        <td>低糖低卡，维生素C含量高，抗氧化，是理想的减肥水果。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>番石榴 (芭乐)</strong>
                        </td>
                        <td><span class="gi-badge">41</span></td>
                        <td>膳食纤维极高，控糖神器，维生素C含量是橙子的2倍以上。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>橙子/橘子</strong>
                        </td>
                        <td><span class="gi-badge">43</span></td>
                        <td>富含维生素C，最好直接吃果肉，<strong>不要榨汁</strong>，以免摄入过多糖分且损失纤维。</td>
                    </tr>
                </tbody>
            </table>
            
            <table id="yellow-table" class="yellow" style="display:none;">
                <thead>
                    <tr>
                        <th width="25%">水果</th>
                        <th width="15%">GI值 (参考)</th>
                        <th width="60%">注意事项</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>香蕉 (熟)</strong>
                        </td>
                        <td><span class="gi-badge">52-60</span></td>
                        <td>越熟的香蕉升糖越快，生香蕉GI较低。香蕉富含钾，适合运动后补充能量。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>芒果</strong>
                        </td>
                        <td><span class="gi-badge">55</span></td>
                        <td>糖分较高，一次半个为宜。芒果富含维生素A，有益眼睛健康。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>猕猴桃</strong>
                        </td>
                        <td><span class="gi-badge">52</span></td>
                        <td>虽然GI不算高，但部分品种糖分高，适量吃。富含维生素C和膳食纤维。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>葡萄</strong>
                        </td>
                        <td><span class="gi-badge">50-59</span></td>
                        <td>皮里含有益成分(如白藜芦醇)，但糖分吸收快，建议一次一小串，约10-15颗。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>菠萝</strong>
                        </td>
                        <td><span class="gi-badge">66</span></td>
                        <td>接近高GI，且含有蛋白酶，少吃。食用后可用淡盐水漱口减少对口腔的刺激。</td>
                    </tr>
                </tbody>
            </table>
            
            <table id="red-table" class="red" style="display:none;">
                <thead>
                    <tr>
                        <th width="25%">水果</th>
                        <th width="15%">GI值 (参考)</th>
                        <th width="60%">为什么危险</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>西瓜</strong>
                        </td>
                        <td><span class="gi-badge">72</span></td>
                        <td>主要是水和糖，极其容易吃过量（因为不饱腹）。建议一次一小块，约200克。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>荔枝</strong>
                        </td>
                        <td><span class="gi-badge">72</span></td>
                        <td>"一颗荔枝三把火"，果糖含量极高，容易导致上火和血糖快速升高。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>龙眼 (桂圆)</strong>
                        </td>
                        <td><span class="gi-badge">80+</span></td>
                        <td>鲜果和干果糖分都极高，干龙眼热量更高，不建议糖尿病患者食用。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>红枣 (干)</strong>
                        </td>
                        <td><span class="gi-badge">100+</span></td>
                        <td><strong>升糖炸弹</strong>，干红枣基本等同于吃糖，即使是鲜枣也要严格控制量。</td>
                    </tr>
                    <tr>
                        <td>
                            <div class="fruit-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <strong>榴莲</strong>
                        </td>
                        <td><span class="gi-badge">-</span></td>
                        <td>虽然GI波动大，但<strong>热量和脂肪极高</strong>，减肥杀手。一小块榴莲≈一碗饭的热量。</td>
                    </tr>
                </tbody>
            </table>
        </div>
        
        <div class="warning-note">
            <i class="fas fa-exclamation-triangle"></i>
            <div>
                <strong>重要提示：</strong> GI值仅反映食物中碳水化合物的"质"，未考虑实际摄入的"量"。血糖负荷(GL) = GI × 实际摄入的碳水化合物量 ÷ 100，更能反映食物对血糖的实际影响。即使是低GI水果，过量食用也会导致血糖升高。
            </div>
        </div>
        
        <div class="tips-section">
            <h3><i class="fas fa-lightbulb"></i> 健康吃水果的黄金法则</h3>
            <div class="tips-grid">
                <div class="tip-card">
                    <i class="fas fa-clock"></i>
                    <h4>选对时间</h4>
                    <p>水果最好在两餐之间吃（如上午10点或下午3点），避免饭后立即吃水果，以免血糖叠加升高。</p>
                </div>
                <div class="tip-card">
                    <i class="fas fa-balance-scale"></i>
                    <h4>控制分量</h4>
                    <p>每天水果摄入量控制在200-350克，大约相当于一个中等大小的苹果或一小碗草莓。</p>
                </div>
                <div class="tip-card">
                    <i class="fas fa-utensils"></i>
                    <h4>完整食用</h4>
                    <p>尽量吃完整水果而不是榨汁，因为榨汁会破坏纤维，使糖分吸收更快，升糖指数更高。</p>
                </div>
                <div class="tip-card">
                    <i class="fas fa-leaf"></i>
                    <h4>多样化选择</h4>
                    <p>不同颜色水果含有不同营养素，可轮换选择，以获得全面的维生素和抗氧化剂。</p>
                </div>
                <div class="tip-card">
                    <i class="fas fa-user-md"></i>
                    <h4>个体化原则</h4>
                    <p>糖尿病患者或血糖异常者应在医生或营养师指导下选择水果，并监测血糖反应。</p>
                </div>
                <div class="tip-card">
                    <i class="fas fa-heartbeat"></i>
                    <h4>关注整体饮食</h4>
                    <p>水果只是健康饮食的一部分，应搭配全谷物、优质蛋白和健康脂肪，形成均衡膳食。</p>
                </div>
            </div>
        </div>
        
        <footer>
            <p>数据来源：国际血糖指数数据库及营养学研究 | 设计：健康饮食科普</p>
            <p>© 2023 低升糖(GI)水果红绿灯表 | 本表格仅供参考，具体饮食建议请咨询专业医生或营养师</p>
            <p style="margin-top: 10px;"><i class="fas fa-info-circle"></i> GI值可能因水果品种、成熟度和测试方法不同而有差异</p>
        </footer>
    </div>

    <script>
        function showTable(tableType) {
            // 隐藏所有表格
            document.getElementById('green-table').style.display = 'none';
            document.getElementById('yellow-table').style.display = 'none';
            document.getElementById('red-table').style.display = 'none';
            
            // 移除所有tab的active类
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // 显示选中的表格
            if (tableType === 'green') {
                document.getElementById('green-table').style.display = 'table';
                document.querySelectorAll('.tab')[0].classList.add('active');
            } else if (tableType === 'yellow') {
                document.getElementById('yellow-table').style.display = 'table';
                document.querySelectorAll('.tab')[1].classList.add('active');
            } else {
                document.getElementById('red-table').style.display = 'table';
                document.querySelectorAll('.tab')[2].classList.add('active');
            }
        }
        
        // 表格行悬停效果增强
        document.addEventListener('DOMContentLoaded', function() {
            const rows = document.querySelectorAll('tbody tr');
            rows.forEach(row => {
                row.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.01)';
                    this.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
                    this.style.transition = 'all 0.3s ease';
                });
                
                row.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1)';
                    this.style.boxShadow = 'none';
                });
            });
            
            // 初始显示绿灯区
            showTable('green');
        });
    </script>
</body>
</html>

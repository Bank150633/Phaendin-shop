<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ร้านผ่อนสบาย - ของกินเล่น & ของใช้ในบ้าน</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        header {
            background: linear-gradient(135deg, #ff6b6b, #ff8e53);
            color: white;
            text-align: center;
            padding: 40px 20px;
        }
        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        .container {
            max-width: 1000px;
            margin: 30px auto;
            padding: 0 20px;
        }
        .section-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 1.8rem;
            color: #2c3e50;
        }
        /* Calculator Area */
        .calculator-box {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            margin-bottom: 40px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .form-group select, .form-group input {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }
        .result-box {
            background: #fff5f5;
            padding: 20px;
            border-radius: 8px;
            border-left: 5px solid #ff6b6b;
            margin-top: 20px;
            display: none;
        }
        /* Product Grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }
        .product-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        .product-card:hover {
            transform: translateY(-5px);
        }
        .product-info {
            padding: 20px;
        }
        .product-tag {
            background: #ffe3e3;
            color: #ff6b6b;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            display: inline-block;
            margin-bottom: 10px;
        }
        .product-name {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .product-price {
            font-size: 1.1rem;
            color: #ff6b6b;
            font-weight: bold;
            margin-bottom: 15px;
        }
        .btn {
            display: block;
            width: 100%;
            background: #2ecc71;
            color: white;
            text-align: center;
            padding: 12px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            transition: background 0.2s;
        }
        .btn:hover {
            background: #27ae60;
        }
        footer {
            text-align: center;
            padding: 40px;
            background: #2c3e50;
            color: white;
            margin-top: 50px;
        }
    </style>
</head>
<body>

    <header>
        <h1>ร้านผ่อนสบายใจ Shop</h1>
        <p>ศูนย์รวมของกินเล่น & ของใช้ในบ้านระบบผ่อนเอง อนุมัติไว ได้ของจริง</p>
    </header>

    <div class="container">
        
        <!-- ส่วนคำนวณเงินผ่อน -->
        <div class="calculator-box">
            <h2 style="margin-bottom: 20px; color: #ff6b6b;">🧮 เครื่องคำนวณยอดผ่อนชำระ</h2>
            <div class="form-group">
                <label>เลือกสินค้าที่ต้องการผ่อน:</label>
                <select id="productSelect" onchange="calculatePlan()">
                    <option value="0">-- กรุณาเลือกสินค้า --</option>
                    <option value="600">เซ็ตน้ำพริกหมูกระจกยักษ์ (600 บาท)</option>
                    <option value="1200">เซ็ตขนมปี๊บแบ่งขาย 20 ถุง (1,200 บาท)</option>
                    <option value="800">ชั้นวางของและกล่องจัดระเบียบมินิมอล (800 บาท)</option>
                    <option value="1500">หม้อทอดไร้น้ำมันพร้อมอุปกรณ์ครัว (1,500 บาท)</option>
                </select>
            </div>
            <div class="form-group">
                <label>เลือกจำนวนงวดที่ต้องการผ่อน:</label>
                <select id="monthsSelect" onchange="calculatePlan()">
                    <option value="2">2 งวด (จ่ายทุก 2 สัปดาห์)</option>
                    <option value="4">4 งวด (จ่ายรายเดือน)</option>
                </select>
            </div>
            
            <div class="result-box" id="resultBox">
                <p id="depositText" style="font-weight: bold; color: #2c3e50;"></p>
                <p id="installmentText" style="color: #555; margin-top: 5px;"></p>
                <p style="font-size: 0.9rem; color: #e74c3c; margin-top: 10px;">*ระบบผ่อนหมดส่งของ หรือ วางเงินดาวน์ตามเงื่อนไขร้านค้า</p>
            </div>
        </div>

        <!-- รายการสินค้า -->
        <h2 class="section-title">📦 สินค้าพร้อมผ่อนวันนี้</h2>
        <div class="product-grid">
            
            <!-- ชิ้นที่ 1 -->
            <div class="product-card">
                <div class="product-info">
                    <span class="product-tag">ของกินเล่น</span>
                    <div class="product-name">เซ็ตน้ำพริกหมูกระจกยักษ์ คละรสได้</div>
                    <div class="product-price">ราคาผ่อนรวม: 600.-</div>
                    <p style="font-size: 0.9rem; color: #7f8c8d; margin-bottom: 15px;">สำหรับตุนเสบียง ผ่อนสบายๆ เริ่มต้นหลักร้อย</p>
                    <a href="https://line.me" class="btn" target="_blank">📲 ทักแชทขอผ่อนชิ้นนี้</a>
                </div>
            </div>

            <!-- ชิ้นที่ 2 -->
            <div class="product-card">
                <div class="product-info">
                    <span class="product-tag">ของกินเล่น</span>
                    <div class="product-name">เซ็ตขนมปี๊บ มินิบราวนี่อบกรอบ 20 ถุง</div>
                    <div class="product-price">ราคาผ่อนรวม: 1,200.-</div>
                    <p style="font-size: 0.9rem; color: #7f8c8d; margin-bottom: 15px;">รับไปกินหรือไปแบ่งขายต่อเพื่อสร้างรายได้</p>
                    <a href="https://line.me" class="btn" target="_blank">📲 ทักแชทขอผ่อนชิ้นนี้</a>
                </div>
            </div>

            <!-- ชิ้นที่ 3 -->
            <div class="product-card">
                <div class="product-info">
                    <span class="product-tag">ของใช้ในบ้าน</span>
                    <div class="product-name">ชั้นวางของและกล่องจัดระเบียบมินิมอล</div>
                    <div class="product-price">ราคาผ่อนรวม: 800.-</div>
                    <p style="font-size: 0.9rem; color: #7f8c8d; margin-bottom: 15px;">ชุดช่วยจัดบ้านให้เป็นระเบียบสไตล์เกาหลี</p>
                    <a href="https://line.me" class="btn" target="_blank">📲 ทักแชทขอผ่อนชิ้นนี้</a>
                </div>
            </div>

        </div>
    </div>

    <footer>
        <p>© 2026 ร้านผ่อนสบายใจ - งบ 5,000 สร้างอาชีพออนไลน์</p>
        <p style="font-size: 0.8rem; margin-top: 10px; color: #bdc3c7;">ปลอดภัย มั่นใจ ได้ของชัวร์</p>
    </footer>

    <script>
        function calculatePlan() {
            var price = parseFloat(document.getElementById("productSelect").value);
            var months = parseInt(document.getElementById("monthsSelect").value);
            var resultBox = document.getElementById("resultBox");
            
            if (price === 0) {
                resultBox.style.display = "none";
                return;
            }
            
            // คำนวณเงินดาวน์ 30% เพื่อความปลอดภัยของทุนคุณ
            var deposit = price * 0.3;
            var remaining = price - deposit;
            var perMonth = remaining / months;
            
            document.getElementById("depositText").innerHTML = "💰 เงินดาวน์ก้อนแรก (30%): " + deposit.toFixed(0) + " บาท (ส่งของทันที)";
            document.getElementById("installmentText").innerHTML = "📅 ผ่อนต่ออีก " + months + " งวด งวดละ: " + perMonth.toFixed(0) + " บาท";
            
            resultBox.style.display = "block";
        }
    </script>
</body>
</html>

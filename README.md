<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phaendin | Dark Premium Edition</title>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        /* 🎨 1. ปรับโทนสีให้เข้มขึ้น (Dark Mode) */
        :root { 
            --gold: #b8860b; 
            --gold-light: #1e1b13; 
            --dark-bg: #121212; 
            --card-bg: #1c1c1c;
            --text-main: #e0e0e0;
            --text-muted: #888;
            --sale: #ff4757; 
        }

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; margin: 0; padding: 0; }
        a { text-decoration: none; color: inherit; }
        body { font-family: 'Kanit', sans-serif; background: var(--dark-bg); color: var(--text-main); line-height: 1.5; }

        header { background: #000; color: var(--gold); text-align: center; padding: 30px 0; border-bottom: 2px solid var(--gold); }
        header h1 { font-size: 28px; letter-spacing: 6px; font-weight: 600; text-transform: uppercase; }

        /* 🌟 สินค้าแนะนำ (เน้นจากคอลัมน์ G) */
        .rec-section { background: var(--gold-light); padding: 25px 0; border-bottom: 1px solid #332b1a; }
        .section-label { color: var(--gold); font-size: 15px; font-weight: 600; padding: 0 15px 15px; text-transform: uppercase; letter-spacing: 1px; }
        .rec-slider { display: flex; gap: 20px; overflow-x: auto; padding: 0 15px 15px; scroll-snap-type: x mandatory; }
        .rec-slider::-webkit-scrollbar { display: none; }
        
        .rec-card { min-width: 80vw; max-width: 320px; background: var(--card-bg); border: 1px solid #444; border-radius: 12px; overflow: hidden; scroll-snap-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }

        /* 🖼️ 2. ปรับ Gallery รูปภาพให้ดูเล็กลงและพอดี */
        .img-gallery { display: flex; overflow-x: auto; scroll-snap-type: x mandatory; aspect-ratio: 4/3; position: relative; background: #000; }
        .img-gallery::-webkit-scrollbar { display: none; }
        .img-gallery img { min-width: 100%; object-fit: cover; scroll-snap-align: center; opacity: 0.9; transition: 0.3s; }
        .img-gallery img:hover { opacity: 1; }
        
        .img-dots { position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%); display: flex; gap: 5px; }
        .dot { width: 5px; height: 5px; background: rgba(255,255,255,0.3); border-radius: 50%; }

        .rec-info { padding: 18px; }
        .rec-tag { font-size: 11px; background: var(--gold); color: #000; padding: 2px 12px; border-radius: 4px; margin-bottom: 10px; display: inline-block; font-weight: 600; }
        .rec-title { font-size: 16px; font-weight: 500; height: 48px; overflow: hidden; margin-bottom: 15px; color: #fff; }
        .rec-price-row { display: flex; justify-content: space-between; align-items: center; border-top: 1px solid #333; padding-top: 15px; }
        .rec-price { font-size: 24px; font-weight: 600; color: var(--gold); }
        .rec-btn { background: var(--gold); color: #000; padding: 8px 20px; border-radius: 6px; font-size: 14px; font-weight: 600; transition: 0.2s; }
        .rec-btn:active { transform: scale(0.95); opacity: 0.8; }

        /* ค้นหาและหมวดหมู่ */
        .sticky-tools { position: sticky; top: 0; z-index: 100; background: rgba(18,18,18,0.95); backdrop-filter: blur(10px); border-bottom: 1px solid #333; padding: 12px 0; }
        .search-box { padding: 0 15px 12px; }
        #searchInput { width: 100%; padding: 12px 15px; border-radius: 10px; border: 1px solid #333; background: #252525; color: #fff; font-family: 'Kanit'; font-size: 14px; }
        #searchInput:focus { outline: none; border-color: var(--gold); }
        
        .cat-bar { display: flex; gap: 8px; padding: 0 15px 5px; overflow-x: auto; }
        .cat-bar::-webkit-scrollbar { display: none; }
        .cat-btn { background: #252525; border: 1px solid #333; padding: 7px 18px; border-radius: 20px; font-size: 13px; white-space: nowrap; color: var(--text-muted); font-family: 'Kanit'; transition: 0.3s; }
        .cat-btn.active { background: var(--gold); color: #000; border-color: var(--gold); font-weight: 500; }

        /* 📦 Grid สินค้าทั่วไป */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; padding: 15px; }
        .card { background: var(--card-bg); border-radius: 10px; border: 1px solid #2a2a2a; overflow: hidden; display: flex; flex-direction: column; }
        .card .img-gallery { aspect-ratio: 1/1; } /* รูปใน Grid เป็นจตุรัสให้ดูเล็ก */
        .card-info { padding: 12px; flex-grow: 1; }
        .card-title { font-size: 13px; height: 38px; overflow: hidden; margin-bottom: 10px; color: #ccc; font-weight: 300; }
        .card-price { color: var(--gold); font-weight: 600; font-size: 18px; margin-bottom: 10px; }
        .btn-buy { display: block; background: transparent; color: var(--gold); text-align: center; padding: 8px; border-radius: 6px; border: 1px solid var(--gold); font-size: 12px; font-weight: 500; }

        footer { background: #000; border-top: 1px solid var(--gold); padding: 50px 20px; text-align: center; margin-top: 40px; }
        #loading { text-align: center; padding: 100px; color: var(--gold); font-size: 18px; letter-spacing: 2px; }
    </style>
</head>
<body>

<header><h1>PHAENDIN</h1></header>

<div id="rec-area" class="rec-section">
    <div class="section-label">🔥 สินค้าแนะนำพิเศษ</div>
    <div class="rec-slider" id="rec-list"></div>
</div>

<div class="sticky-tools">
    <div class="search-box"><input type="text" id="searchInput" placeholder="ค้นหาอุปกรณ์แต่งรถ..." onkeyup="render()"></div>
    <div class="cat-bar" id="cat-list"><button class="cat-btn active" onclick="setCat('all', this)">ทั้งหมด</button></div>
</div>

<div id="loading">LOADING...</div>
<div class="grid" id="main-list"></div>

<footer>
    <h2 style="color:var(--gold); margin-bottom:10px; letter-spacing:3px;">PHAENDIN</h2>
    <p style="color:#555; font-size:11px; text-transform:uppercase;">Premium Automotive Accessories</p>
</footer>

<script>
    const SHEET_URL = 'https://docs.google.com/spreadsheets/d/14bgucoSdLmBEd3HeMGAmhb4bSwQ0JplYRvOWGbJsp2Y/gviz/tq?tqx=out:csv';
    let db = [];
    let currentCat = 'all';

    async function fetchData() {
        try {
            const res = await fetch(SHEET_URL);
            const text = await res.text();
            const rows = text.split(/\r?\n/).slice(1);
            let cats = new Set();

            db = rows.map(r => {
                const c = r.split(/,(?=(?:(?:[^"]*"){2})*[^"]*$)/).map(v => v.replace(/^"|"$/g, '').trim());
                if(c.length >= 6 && c[5]) cats.add(c[5]);
                return (c.length >= 4 && c[0] !== "") ? c : null;
            }).filter(x => x);

            const catList = document.getElementById('cat-list');
            Array.from(cats).sort().forEach(c => {
                const btn = document.createElement('button');
                btn.className = 'cat-btn'; btn.innerText = c;
                btn.onclick = (e) => setCat(c, e.target);
                catList.appendChild(btn);
            });

            document.getElementById('loading').style.display = 'none';
            render();
        } catch (e) { document.getElementById('loading').innerText = 'ERROR LOADING DATA'; }
    }

    function createGallery(imgString) {
        if (!imgString) return '';
        const imgs = imgString.split(',');
        let html = `<div class="img-gallery">`;
        imgs.forEach(url => {
            html += `<img src="${url.trim()}" loading="lazy" onerror="this.src='https://via.placeholder.com/400x400/1c1c1c/b8860b?text=Phaendin'">`;
        });
        html += `<div class="img-dots">` + imgs.map(() => `<div class="dot"></div>`).join('') + `</div>`;
        html += `</div>`;
        return html;
    }

    function setCat(cat, btn) {
        currentCat = cat;
        document.querySelectorAll('.cat-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        render();
    }

    function render() {
        const search = document.getElementById('searchInput').value.toLowerCase();
        
        // 4. กรองสินค้าแนะนำจากคอลัมน์ G (Index ที่ 6)
        // ถ้าคอลัมน์ G มีคำว่า "แนะนำ", "1", หรือ "yes" จะถูกนำมาโชว์ที่ Slider
        const recommendedItems = db.filter(p => 
            p[6] && (p[6].includes("แนะนำ") || p[6].includes("Recommend") || p[6] === "1")
        );

        document.getElementById('rec-list').innerHTML = recommendedItems.map(p => `
            <div class="rec-card">
                ${createGallery(p[1])}
                <div class="rec-info">
                    <span class="rec-tag">SELECTED: ${p[6]}</span>
                    <div class="rec-title">${p[0]}</div>
                    <div class="rec-price-row">
                        <span class="rec-price">฿${p[2]}</span>
                        <a href="${p[3]}" target="_blank" class="rec-btn">สั่งซื้อ</a>
                    </div>
                </div>
            </div>`).join('');

        // ซ่อนส่วนแนะนำถ้ามีการค้นหา หรือเลือกหมวดหมู่ เพื่อให้แสดงผลลัพธ์ชัดเจน
        if (currentCat !== 'all' || search !== "") {
            document.getElementById('rec-area').style.display = "none";
        } else {
            document.getElementById('rec-area').style.display = recommendedItems.length > 0 ? "block" : "none";
        }

        const filtered = db.filter(p => (currentCat === 'all' || p[5] === currentCat) && p[0].toLowerCase().includes(search));
        
        // กรองเอาสินค้าที่โชว์ด้านบนออกไปจากลิสต์ข้างล่างถ้าอยากให้ไม่ซ้ำ (Optional)
        const gridItems = (currentCat === 'all' && search === "") 
            ? filtered.filter(p => !recommendedItems.includes(p)) 
            : filtered;

        drawGrid(gridItems);
    }

    function drawGrid(items) {
        const list = document.getElementById('main-list');
        if (items.length === 0) {
            list.innerHTML = `<div style="grid-column: 1/3; text-align:center; padding:50px; color:#555;">ไม่พบสินค้าที่คุณค้นหา</div>`;
            return;
        }
        list.innerHTML = items.map(p => `
            <div class="card">
                ${createGallery(p[1])}
                <div class="card-info">
                    <div class="card-title">${p[0]}</div>
                    <div class="card-price">฿${p[2]}</div>
                    <a href="${p[3]}" target="_blank" class="btn-buy">สั่งซื้อ</a>
                </div>
            </div>`).join('');
    }
    fetchData();
</script>
</body>
</html>

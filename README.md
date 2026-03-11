<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>AIJIA 爱家 | 硬核工艺 · 爱筑家园</title>
    <style>
        :root {
            --soft-gold: #e5c9a4;
            --dy-red: #fe2c55;
            --bg-dark: #000000;
            --card-gray: #111111;
            --border-white: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: "PingFang SC", sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg-dark); color: #fff; line-height: 1.6; overflow-x: hidden; padding-bottom: 100px; }

        header { position: fixed; top: 0; width: 100%; height: 70px; display: flex; justify-content: space-between; align-items: center; padding: 0 5%; z-index: 1000; background: rgba(0,0,0,0.8); backdrop-filter: blur(20px); border-bottom: 1px solid var(--border-white); }
        .logo { font-size: 22px; font-weight: 900; letter-spacing: 4px; }
        .logo span { color: var(--soft-gold); font-weight: 300; }

        /* --- Hero --- */
        .hero { height: 70vh; display: flex; flex-direction: column; justify-content: center; padding: 0 8%; background: radial-gradient(circle at 80% 20%, #222 0%, #000 100%); }
        .hero h1 { font-size: clamp(65px, 18vw, 130px); font-weight: 900; line-height: 0.9; margin-bottom: 10px; }
        .metal-text { background: linear-gradient(165deg, #fff 10%, #999 40%, #fff 50%, #888 70%, #fff 100%); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: shine 6s linear infinite; }
        .hero h2 { font-size: clamp(35px, 10vw, 60px); color: var(--soft-gold); font-weight: 300; letter-spacing: 10px; }
        @keyframes shine { to { background-position: 200% center; } }

        /* --- 通用标题 --- */
        .sec-header { padding: 80px 8% 40px; }
        .sec-header p { color: var(--soft-gold); font-size: 12px; letter-spacing: 4px; text-transform: uppercase; margin-bottom: 10px; }
        .sec-header h3 { font-size: 28px; font-weight: 800; }

        /* --- 材质PK --- */
        .pk-scroll { display: flex; overflow-x: auto; padding: 0 8% 40px; gap: 20px; scrollbar-width: none; }
        .pk-scroll::-webkit-scrollbar { display: none; }
        .pk-item { min-width: 280px; background: var(--card-gray); padding: 30px; border: 1px solid var(--border-white); }
        .pk-item.win { border-color: var(--soft-gold); position: relative; }
        .pk-item.win::after { content: "RECOMMEND"; position: absolute; top: 15px; right: 15px; font-size: 10px; color: var(--soft-gold); border: 1px solid var(--soft-gold); padding: 2px 6px; }
        .pk-item h4 { font-size: 20px; margin-bottom: 15px; }
        .pk-item ul { list-style: none; font-size: 13px; color: #888; }
        .pk-item ul li { margin-bottom: 8px; display: flex; align-items: center; }
        .pk-item ul li::before { content: "✕"; color: #ff4d4f; margin-right: 8px; }
        .pk-item.win ul li::before { content: "✓"; color: var(--soft-gold); }

        /* --- 表格对比 --- */
        .compare-table { margin: 0 8% 40px; border: 1px solid var(--border-white); font-size: 13px; }
        .table-row { display: grid; grid-template-columns: 1fr 1.5fr 1.5fr; border-bottom: 1px solid var(--border-white); }
        .table-cell { padding: 15px 10px; text-align: center; display: flex; align-items: center; justify-content: center; }
        .t-head { background: #1a1a1a; color: var(--soft-gold); font-weight: 800; }
        .t-aijia { background: rgba(229, 201, 164, 0.05); font-weight: 700; }

        /* --- 工艺 --- */
        .process-grid { display: grid; grid-template-columns: 1fr; gap: 20px; padding: 0 8% 80px; }
        .process-card { background: #0a0a0a; border-left: 3px solid var(--soft-gold); padding: 25px; }
        .process-card h5 { color: var(--soft-gold); font-size: 18px; margin-bottom: 10px; }
        .process-card p { font-size: 14px; color: #999; }

        /* --- 颜色 --- */
        .color-palette { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; padding: 0 5% 80px; }
        @media (min-width: 768px) { .color-palette { grid-template-columns: repeat(7, 1fr); } }
        .color-item { background: var(--card-gray); padding: 20px 5px; text-align: center; border: 1px solid var(--border-white); }
        .swatch { width: 45px; height: 45px; border-radius: 50%; margin: 0 auto 10px; border: 1.5px solid rgba(255,255,255,0.2); }
        .color-item span { font-size: 11px; color: #999; display: block; }

        /* --- 按钮与方案 --- */
        .install-section { padding: 0 8% 100px; display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .install-card { background: #0a0a0a; border: 1px solid var(--border-white); padding: 50px 30px; border-radius: 4px; text-align: center; }
        .install-card.premium { border-color: var(--soft-gold); background: rgba(229, 201, 164, 0.05); }
        .btn { display: block; width: 100%; padding: 16px; border-radius: 4px; text-decoration: none; font-weight: 800; margin-bottom: 10px; border: none; cursor: pointer; }
        .btn-white { background: #fff; color: #000; }
        .btn-outline { border: 1px solid var(--soft-gold); color: var(--soft-gold); background: transparent; }
        .btn-gold { background: var(--soft-gold); color: #000; }

        /* --- 弹窗与底部菜单 --- */
        .modal { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.9); z-index: 3000; padding: 10% 8%; }
        .modal-body { background: #111; padding: 40px 30px; border: 1px solid var(--soft-gold); border-radius: 8px; position: relative; }
        .dock { position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%); width: 92%; max-width: 450px; background: #fff; height: 74px; border-radius: 40px; display: flex; align-items: center; padding: 6px; z-index: 2000; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        .dock-item { flex: 1; text-align: center; text-decoration: none; color: #000; font-size: 10px; font-weight: 900; display: flex; flex-direction: column; }
        .dock-main { background: #000; color: #fff; border-radius: 35px; height: 100%; justify-content: center; }
        
        /* 表单输入样式 */
        .form-input { width: 100%; background: #222; border: 1px solid #333; padding: 15px; margin-bottom: 15px; color: #fff; border-radius: 4px; outline: none; }
        .form-input:focus { border-color: var(--soft-gold); }
    </style>
</head>
<body>

    <header>
        <div class="logo">AIJIA <span>爱家铝业</span></div>
        <div style="font-size: 9px; color: #555; letter-spacing: 2px;">PREMIUM QUALITY</div>
    </header>

    <section class="hero">
        <h1 class="metal-text">硬核工艺</h1>
        <h2>爱筑家园</h2>
    </section>

    <div class="sec-header">
        <p>Why Aluminum?</p >
        <h3>不同材质踢脚线对比</h3>
    </div>
    <div class="pk-scroll">
        <div class="pk-item"><h4>实木/木塑</h4><ul><li>受潮易发霉鼓包</li><li>含有甲醛释放风险</li><li>易生虫，不耐撞击</li></ul></div>
        <div class="pk-item"><h4>PVC材质</h4><ul><li>廉价感强，易老化</li><li>接缝明显，易变色</li><li>安装稳定性差</li></ul></div>
        <div class="pk-item win"><h4>航空铝合金</h4><ul><li>永久不霉、不锈、防火</li><li>0甲醛环保材质</li><li>莫氏硬度高，防撞耐用</li></ul></div>
    </div>

    <div class="sec-header">
        <p>Craftsmanship</p >
        <h3>爱家核心工艺</h3>
    </div>
    <section class="process-grid">
        <div class="process-card"><h5>纳米级喷砂工艺</h5><p>形成细腻哑光磨砂质感，触感如丝绸，不留指纹。</p ></div>
        <div class="process-card"><h5>深层阳极氧化</h5><p>50年不退色、不被腐蚀，色泽质感极佳。</p ></div>
    </section>

    <div class="sec-header">
        <p>Installation</p >
        <h3>安装方案选择</h3>
    </div>
    <section class="install-section">
        <div class="install-card">
            <h4>自行安装</h4>
            <p>适合已有装修工人，提供全套教学视频。</p >
            <a href=" " class="btn btn-white">观看安装视频</a >
            <button onclick="openModal('textTutorial')" class="btn btn-outline">文字教学手册</button>
        </div>
        <div class="install-card premium">
            <h4>预约师傅安装</h4>
            <p>全国300+城市上门，测量、安装、售后一站式包办。</p >
            <button onclick="openModal('bookingModal')" class="btn btn-gold">在线提交预约申请</button>
        </div>
    </section>

    <div id="bookingModal" class="modal">
        <div class="modal-body">
            <span style="position:absolute;top:15px;right:20px;font-size:24px;color:#666;" onclick="closeModal('bookingModal')">×</span>
            <h4 style="color:var(--soft-gold);margin-bottom:20px;">预约上门测量服务</h4>
            
            <form action="https://formspree.io/f/mgonagql" method="POST" id="my-form">
                <input type="text" name="客户姓名" class="form-input" placeholder="您的姓名" required>
                <input type="tel" name="联系电话" class="form-input" placeholder="联系电话" required>
                <input type="text" name="所在城市" class="form-input" placeholder="所在城市" required>
                <input type="text" name="预估面积" class="form-input" placeholder="预估面积(如80平)">
                <button type="submit" id="submit-btn" class="btn btn-gold" style="width:100%;font-weight:900;">立即提交申请</button>
                <p id="my-form-status" style="margin-top:15px; font-size:13px; text-align:center;"></p >
            </form>
        </div>
    </div>

    <div id="textTutorial" class="modal">
        <div class="modal-body">
            <span style="position:absolute;top:15px;right:20px;font-size:24px;color:#666;" onclick="closeModal('textTutorial')">×</span>
            <h4 style="color:var(--soft-gold);margin-bottom:20px;">文字安装指南</h4>
            <div style="font-size:14px;color:#ccc;line-height:1.8;text-align:left;">
                1. 墙面清理：确保墙脚平整干燥。<br>
                2. 卡扣安装：每隔40cm固定底座。<br>
                3. 裁切对拼：转角处建议45度斜切。<br>
                4. 扣合面板：将面板插入底座按压锁死。
            </div>
        </div>
    </div>

    <div class="dock">
        <a href="snssdk1128://user/profile/29509811695" class="dock-item" style="color:var(--dy-red)">
            <span>🎵</span>抖音主页
        </a >
        <a href="tel:18919521681" class="dock-item dock-main">
            <span>📞</span>呼叫经理
        </a >
        <a href="javascript:void(0);" onclick="copyWX()" class="dock-item">
            <span>💬</span>微信咨询
        </a >
    </div>

    <script>
        function openModal(id) { document.getElementById(id).style.display = 'block'; }
        function closeModal(id) { document.getElementById(id).style.display = 'none'; }
        
        // 复制微信逻辑
        function copyWX() {
            const input = document.createElement('input');
            input.setAttribute('value', 'wxid_wg8u93oruyik22');
            document.body.appendChild(input);
            input.select();
            document.execCommand('copy');
            document.body.removeChild(input);
            alert('微信号已复制，请去微信添加');
            window.location.href = "weixin://";
        }

        // Formspree 提交逻辑优化
        var form = document.getElementById("my-form");
        async function handleSubmit(event) {
          event.preventDefault();
          var status = document.getElementById("my-form-status");
          var data = new FormData(event.target);
          fetch(event.target.action, {
            method: form.method,
            body: data,
            headers: { 'Accept': 'application/json' }
          }).then(response => {
            if (response.ok) {
              status.innerHTML = "✅ 提交成功！经理将尽快回电。";
              form.reset();
              setTimeout(() => closeModal('bookingModal'), 2000);
            } else {
              response.json().then(data => {
                if (Object.hasOwn(data, 'errors')) {
                  status.innerHTML = data["errors"].map(error => error["message"]).join(", ");
                } else {
                  status.innerHTML = "❌ 提交失败，请直接电话联系。";
                }
              })
            }
          }).catch(error => {
            status.innerHTML = "❌ 网络错误，请检查网络。";
          });
        }
        form.addEventListener("submit", handleSubmit)
    </script>
</body>
</html>

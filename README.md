<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>AIJIA 爱家 | 硬核工艺 · 爱筑家园</title>
    <style>
        :root { --soft-gold: #e5c9a4; --bg-dark: #000000; --card-gray: #111111; }
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: "PingFang SC", sans-serif; }
        body { background: var(--bg-dark); color: #fff; line-height: 1.6; padding-bottom: 100px; }
        
        /* 导航与视觉 */
        header { position: fixed; top: 0; width: 100%; height: 60px; display: flex; justify-content: space-between; align-items: center; padding: 0 5%; z-index: 1000; background: rgba(0,0,0,0.8); backdrop-filter: blur(10px); border-bottom: 1px solid rgba(255,255,255,0.1); }
        .logo { font-size: 20px; font-weight: 900; }
        .logo span { color: var(--soft-gold); }
        .hero { height: 50vh; display: flex; flex-direction: column; justify-content: center; padding: 0 8%; background: linear-gradient(to bottom, #222, #000); }
        .hero h1 { font-size: 50px; font-weight: 900; background: linear-gradient(to right, #fff, var(--soft-gold)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }

        /* 内容板块 */
        .section { padding: 40px 8%; }
        .section h3 { color: var(--soft-gold); font-size: 24px; margin-bottom: 20px; border-left: 4px solid var(--soft-gold); padding-left: 15px; }
        .card { background: var(--card-gray); padding: 20px; border-radius: 8px; margin-bottom: 20px; border: 1px solid rgba(255,255,255,0.05); }

        /* 核心：表单样式 */
        .form-group { margin-bottom: 15px; }
        .form-label { display: block; font-size: 14px; color: var(--soft-gold); margin-bottom: 8px; }
        .form-input { width: 100%; background: #222; border: 1px solid #333; padding: 15px; color: #fff; border-radius: 4px; font-size: 16px; }
        .form-input:focus { border-color: var(--soft-gold); outline: none; }
        .submit-btn { width: 100%; background: var(--soft-gold); color: #000; border: none; padding: 16px; font-size: 18px; font-weight: 900; border-radius: 4px; cursor: pointer; margin-top: 10px; }

        /* 底部导航 */
        .dock { position: fixed; bottom: 20px; left: 5%; width: 90%; background: #fff; border-radius: 40px; height: 60px; display: flex; align-items: center; z-index: 2000; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        .dock-item { flex: 1; text-align: center; text-decoration: none; color: #000; font-size: 12px; font-weight: 700; }
        .dock-main { background: #000; color: #fff; border-radius: 30px; height: 50px; line-height: 50px; margin: 0 5px; }
    </style>
</head>
<body>

    <header>
        <div class="logo">AIJIA <span>爱家铝业</span></div>
    </header>

    <section class="hero">
        <h1>硬核工艺</h1>
        <p style="color:var(--soft-gold); letter-spacing:5px;">爱筑家园 · 铝享生活</p >
    </section>

    <section class="section" id="booking">
        <h3>预约上门测量</h3>
        <div class="card">
            <form action="https://formspree.io/f/mgonagql" method="POST">
                <div class="form-group">
                    <label class="form-label">您的姓名</label>
                    <input type="text" name="客户姓名" class="form-input" placeholder="请输入姓名" required>
                </div>
                <div class="form-group">
                    <label class="form-label">联系电话</label>
                    <input type="tel" name="联系电话" class="form-input" placeholder="请输入手机号" required>
                </div>
                <div class="form-group">
                    <label class="form-label">所在城市</label>
                    <input type="text" name="所在城市" class="form-input" placeholder="例如：兰州" required>
                </div>
                <div class="form-group">
                    <label class="form-label">需求备注</label>
                    <textarea name="留言内容" class="form-input" rows="3" placeholder="例如：大概100平，需要奶油白"></textarea>
                </div>
                <input type="hidden" name="_subject" value="【新预约】来自爱家铝业官网">
                
                <button type="submit" class="submit-btn">立即提交预约</button>
            </form>
        </div>
    </section>

    <section class="section">
        <h3>核心优势</h3>
        <div class="card"><h4>航空原铝</h4><p>6063-T5级别，硬度高，防撞不变形。</p ></div>
        <div class="card"><h4>0甲醛</h4><p>金属材质，不含胶水，装完即刻入住。</p ></div>
    </section>

    <div class="dock">
        <a href=" " class="dock-item">电话咨询</a >
        <a href="#booking" class="dock-item dock-main">在线预约</a >
        <a href="javascript:alert('已复制微信号：wxid_wg8u93oruyik22')" class="dock-item">微信联系</a >
    </div>

</body>
</html>

<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KAIZEN STORE - مسابقات فري فاير الرسمية</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, sans-serif; }
        body { background-color: #0f172a; color: #f8fafc; display: flex; justify-content: center; align-items: center; min-height: 100vh; padding: 15px; }
        .container { background-color: #1e293b; padding: 25px; border-radius: 16px; box-shadow: 0 10px 25px rgba(0,0,0,0.5); width: 100%; max-width: 450px; border: 1px solid #334155; text-align: center; }
        
        /* بروفايل اليوتيوبر */
        .creator-box { display: flex; align-items: center; background: #0f172a; padding: 12px; border-radius: 12px; margin-bottom: 20px; border: 1px solid #475569; }
        .creator-img { width: 60px; height: 60px; border-radius: 50%; object-fit: cover; border: 2px solid #38bdf8; margin-left: 12px; }
        .creator-info { text-align: right; }
        .creator-info h3 { color: #38bdf8; font-size: 16px; margin-bottom: 2px; }
        .creator-info p { color: #94a3b8; font-size: 12px; }

        h1 { color: #facc15; margin-bottom: 10px; font-size: 22px; text-shadow: 0 2px 4px rgba(0,0,0,0.3); }
        
        /* صور الديكور */
        .game-banner { width: 100%; border-radius: 10px; margin: 15px 0; border: 1px solid #475569; max-height: 180px; object-fit: cover; }

        /* صندوق الجوائز */
        .prizes-grid { display: flex; gap: 10px; margin: 15px 0; }
        .prize-card { flex: 1; background: rgba(56, 189, 248, 0.08); border: 1px solid #38bdf8; padding: 12px; border-radius: 10px; text-align: center; }
        .prize-card h4 { color: #38bdf8; font-size: 15px; margin-bottom: 5px; }
        .prize-card span { color: #cbd5e1; font-size: 13px; font-weight: bold; }

        p.desc { color: #94a3b8; font-size: 13px; line-height: 1.5; margin-bottom: 20px; }
        
        .btn { width: 100%; padding: 14px; background: linear-gradient(135deg, #0ea5e9, #2563eb); border: none; border-radius: 8px; color: white; font-size: 16px; font-weight: bold; cursor: pointer; transition: 0.3s; margin-top: 10px; box-shadow: 0 4px 12px rgba(14, 165, 233, 0.4); }
        .btn:hover { opacity: 0.9; transform: translateY(-2px); }
        
        .input-group { margin-bottom: 15px; text-align: right; }
        .input-group label { display: block; margin-bottom: 5px; font-size: 13px; color: #cbd5e1; }
        .input-group input { width: 100%; padding: 12px; border-radius: 8px; border: 1px solid #475569; background-color: #0f172a; color: #fff; font-size: 15px; outline: none; }
        .input-group input:focus { border-color: #38bdf8; }
        
        .hidden { display: none; }
        .support-note { background: #334155; padding: 10px; border-radius: 6px; font-size: 12px; color: #e2e8f0; margin-bottom: 15px; }
    </style>
</head>
<body>

    <div class="container">
        <!-- معلومات صاحب الموقع (اليوتيوبر كايزن) -->
        <div class="creator-box">
            <img src="8165.png" alt="يوسف محمد - كايزن" class="creator-img">
            <div class="creator-info">
                <h3>اليوتيوبر كايزن</h3>
                <p>صحب الموقع: يوسف محمد | KAIZEN STORE</p>
            </div>
        </div>

        <!-- قسم تفاصيل المسابقة -->
        <div id="contest-info">
            <h1>🔥 مسابقات KAIZEN STORE الكبرى 🔥</h1>
            
            <!-- صورة من داخل لعبة فري فاير -->
            <img src="9293.png" alt="Free Fire KAIZEN" class="game-banner">

            <div class="prizes-grid">
                <div class="prize-card">
                    <h4>💎 الجائزة الأولى</h4>
                    <span>100 جوهرة</span>
                </div>
                <div class="prize-card">
                    <h4>📦 الجائزة الثانية</h4>
                    <span>بويا باس (Booyah Pass)</span>
                </div>
            </div>

            <p class="desc">علشان نقدر نستمر في توزيع الهدايا والجواهر، ساهم في دعمنا بمشاهدة إعلان بسيط وهتتحول فوراً لصفحة تسجيل بياناتك في السحب!</p>
            
            <button class="btn" onclick="openAdAndJoin()">📺 دعم الموقع والانضمام للسحب</button>
        </div>

        <!-- قسم تسجيل البيانات (يظهر بعد التفاعل مع الإعلان) -->
        <div id="register-form" class="hidden">
            <h1>📝 تسجيل بيانات السحب</h1>
            <div class="support-note">تسلم يا بطل على دعمك للقناة والموقع! اكتب بياناتك بدقة عشان ندخلك في السحب على الجواهر أو البويا باس.</div>
            
            <div class="input-group">
                <label>اسمك الثنائي</label>
                <input type="text" id="playerName" placeholder="اكتب اسمك هنا">
            </div>
            <div class="input-group">
                <label>آيدي فري فاير (Free Fire ID)</label>
                <input type="text" id="playerGameId" placeholder="اكتب الآيدي الخاص بك (الأرقام)">
            </div>
            
            <button class="btn" onclick="submitData()" style="background: linear-gradient(135deg, #10b981, #059669); box-shadow: 0 4px 12px rgba(16, 185, 129, 0.4);">تأكيد المشاركة نهائياً 🚀</button>
        </div>

        <!-- رسالة النجاح -->
        <div id="success-msg" class="hidden">
            <h1 style="color: #10b981; font-size: 24px;">🎉 تم تسجيلك بنجاح يا بطل!</h1>
            <p style="color: #fff; margin-top: 15px; font-size: 14px; line-height: 1.6;">تم حفظ بياناتك في قائمة السحب. تابع قناة اليوتيوب وإعلانات متجر كايزن عشان تشوف اسم الفائز قريب جداً!</p>
        </div>
    </div>

    <script>
        function openAdAndJoin() {
            // رابط الإعلان (يمكنك تعديله لاحقاً برابط شركة الإعلانات أو الرابط المختصر الخاص بك)
            window.open("https://www.google.com", "_blank");
            
            // إظهار فورم إدخال الآيدي والاسم بعد مشاهدة الإعلان
            document.getElementById('contest-info').classList.add('hidden');
            document.getElementById('register-form').classList.remove('hidden');
        }

        function submitData() {
            let name = document.getElementById('playerName').value.trim();
            let gameId = document.getElementById('playerGameId').value.trim();

            if (name === "" || gameId === "") {
                alert("يا صاحبي، لازم تكتب اسمك والآيدي بتاع اللعبة الأول!");
                return;
            }

            // إخفاء الفورم وإظهار رسالة النجاح
            document.getElementById('register-form').classList.add('hidden');
            document.getElementById('success-msg').classList.remove('hidden');
        }
    </script>
</body>
</html>

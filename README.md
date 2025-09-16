<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title style="font-family: 'Vazirmatn', 'Tahoma', sans-serif;">دوره جامع پایتون — از صفر تا شیءگرا</title>

  <!-- بارگذاری فونت Vazirmatn از CDN -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn@v33.003/Vazirmatn-font-face.css">

  <!-- بارگذاری فونت Poppins برای عناوین -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&display=swap" rel="stylesheet">

  <style>
    * {
      box-sizing: border-box;
    }
    body {
      background-color: #121212;
      margin: 0;
      padding: 2rem 1rem;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
      color: #dcdcdc;
    }
    .section-card {
      background: linear-gradient(145deg, rgb(61, 61, 87), rgb(49, 49, 70));
      border-radius: 15px;
      padding: 2rem;
      margin: 0 auto 2.5rem;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
      width: 100%;
      max-width: min(1200px, 95vw);
    }
    .section-card h1 {
      width: 100%;
      text-align: center;
      color: #ffffff;
      font-size: 2.8rem;
      margin-bottom: 0;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
      letter-spacing: 1px;
    }
    .section-card h2 {
      text-align: center;
      color: #ffffff;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
      letter-spacing: 1px;
    }
    .container {
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
      align-items: center;
    }
    .card {
      background: linear-gradient(145deg, #24243e, #1e1e3a);
      border-radius: 12px;
      padding: 1.5rem;
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.4);
      border-inline-start: 4px solid transparent;
      width: min(1000px, 90vw);
      margin: 0 auto 1.25rem;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
    }
    .container > .card:last-child {
      margin-bottom: 2rem;
    }
    .card h3 {
      color: #ffffff;
      font-size: 1.3rem;
      margin-bottom: 0.75rem;
      font-weight: bold;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
    }
    p, li {
      color: #dcdcdc;
      font-size: 0.95rem;
      line-height: 1.5;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
    }
    p {
      margin-bottom: 0.75rem;
    }
    ul, ol {
      padding-right: 1.25rem;
      margin-bottom: 0.75rem;
    }
    li {
      margin-bottom: 0.5rem;
    }
    blockquote {
      border-right: 3px solid #66bb6a;
      padding-right: 1rem;
      margin-right: 0;
      color: #f0f0f0;
      font-style: italic;
      text-align: right;
    }
    .note {
      background-color: #fdd835;
      color: #000;
      padding: 1rem;
      border-radius: 6px;
      margin-top: 1.25rem;
      font-style: italic;
      font-size: 0.95rem;
      font-family: 'Vazirmatn', 'Tahoma', sans-serif;
      width: min(1000px, 90vw);
      margin: 1.25rem auto 0;
    }
    .card.green { border-inline-start-color: #66bb6a; }
    .card.blue { border-inline-start-color: #29b6f6; }
    .card.orange { border-inline-start-color: #ffa726; }
    .card.purple { border-inline-start-color: #ba68c8; }
    .card.red { border-inline-start-color: #ef5350; }
    .toc-card ul {
      list-style-type: none;
      padding-right: 0;
    }
    .toc-card a {
      color: #29b6f6;
      text-decoration: none;
    }
        /* اصلاح نمایش جداول در حالت RTL */
        table {
          width: 100%;
          border-collapse: collapse;
          margin: 1.5rem auto;
          direction: rtl;
        }
        th, td {
          padding: 0.75rem;
          text-align: right;
          border: 1px solid #444;
        }
        th {
          background-color: #2a2a4a;
          color: white;
        }
        tr:nth-child(even) {
          background-color: #1e1e30;
        }
        code {
          background: #2d2d3d;
          padding: 0.2rem 0.4rem;
          border-radius: 4px;
          font-family: 'Courier New', monospace;
          color: #f0f0f0;
        }
        pre {
          background: #1e1e2e;
          padding: 1rem;
          border-radius: 8px;
          overflow-x: auto;
          direction: ltr;
          text-align: left;

    @media (max-width: 768px) {
    .section-card {
      padding: 1.25rem;
      max-width: 95vw;
    }

    .card {
      width: 100%;
      padding: 1rem;
    }

    .note {
      width: 100%;
    }

    h1 {
      font-size: 2rem;
    }

    .section-card h2 {
      font-size: 1.4rem;
    }

    .card h3 {
      font-size: 1.2rem;
    }

    p, li {
      font-size: 0.9rem;
    }
  }

  @media (max-width: 480px) {
    h1 {
      font-size: 1.8rem;
    }

    .section-card h2 {
      font-size: 1.2rem;
    }

    .card {
      padding: 0.75rem;
    }

    .note {
      padding: 0.75rem;
    }

    p, li {
      font-size: 0.85rem;
    }
  }
    }
  </style>
</head>
<body>

  <div class="section-card">
    <h1>🐍 دوره جامع پایتون — از صفر تا شیءگرا 🚀</h1>
    <h2>یک دوره‌ی پروژه‌محور و گام‌به‌گام با استفاده از Jupyter Notebook</h2>
    <div class="container">
      <!-- هدف دوره -->
      <div class="card blue">
        <h3>🎯 هدف دوره</h3>
        <ul>
          <li><strong>شروع سریع و اصولی</strong> — از نصب ابزارها تا اولین خط کد</li>
          <li><strong>یادگیری هسته‌ی زبان</strong> — داده‌ها، عملگرها، ساختار کد و کنترل جریان</li>
          <li><strong>توابع و الگوهای متداول</strong> — لامبدا، آرگومان‌های پویا، مستندسازی</li>
          <li><strong>کار با فایل‌ها</strong> — خواندن/نوشتن فایل‌های متنی و باینری با مثال‌های واقعی</li>
          <li><strong>برنامه‌نویسی شیءگرا (OOP)</strong> — کلاس، ارث‌بری، چندریختی، متدهای ویژه</li>
          <li><strong>تمرین‌های کاربردی</strong> — برای تثبیت مفاهیم و آماده‌سازی برای بازار کار</li>
        </ul>
      </div>
      <!-- پیش‌نیازها -->
      <div class="card orange">
        <h3>🧰 پیش‌نیازها</h3>
        <ul>
          <li><strong>دانش اولیه کامپیوتر</strong> — نیازی به تجربه برنامه‌نویسی نیست!</li>
          <li><strong>نصب VS Code یا JupyterLab</strong> — <a href="https://code.visualstudio.com/" target="_blank">دانلود VS Code</a></li>
          <li><strong>نصب پایتون 3.10+</strong> — پیشنهاد: استفاده از <strong>Conda</strong></li>
        </ul>
        <h4>🔧 راه‌اندازی محیط با Conda</h4>
        <pre><code>conda create -n py-course python=3.11 -y
conda activate py-course
pip install jupyter</code></pre>
        <h4>▶️ اجرای نوت‌بوک‌ها</h4>
        <p>در VS Code: افزونه‌های <strong>Python</strong> و <strong>Jupyter</strong> را نصب کنید و فایل‌های <code>.ipynb</code> را مستقیماً باز کنید.</p>
      </div>
      <!-- ساختار پوشه‌ها -->
      <div class="card green">
        <h3>📁 ساختار پوشه‌ها</h3>
        <table>
          <tr>
            <th></th>
            <th>عنوان فصل</th>
            <th>توضیح</th>
          </tr>
          <tr><td>📖</td><td><a href="./01%20introduction/">01 introduction</a></td><td>مقدمه و معرفی پایتون</td></tr>
          <tr><td>⚙️</td><td><a href="./02%20Python%20Setup/">02 Python Setup</a></td><td>نصب و راه‌اندازی</td></tr>
          <tr><td>🔢</td><td><a href="./03%20Data%20Type/">03 Data Type</a></td><td>انواع داده</td></tr>
          <tr><td>🧱</td><td><a href="./04%20Code%20Structure/">04 Code Structure</a></td><td>ساختار کد</td></tr>
          <tr><td>🔄</td><td><a href="./05%20Control%20Structure/">05 Control Structure</a></td><td>ساختارهای کنترلی</td></tr>
          <tr><td>🧩</td><td><a href="./06%20Functions/">06 Functions</a></td><td>توابع</td></tr>
          <tr><td>📂</td><td><a href="./07%20File%20Handling/">07 File Handling</a></td><td>مدیریت فایل‌ها</td></tr>
          <tr><td>🧠</td><td><a href="./08%20OOP/">08 OOP</a></td><td>شیءگرایی</td></tr>
          <tr><td>🛠️</td><td><a href="./09%20Projects/">09 Projects</a></td><td>پروژه‌های عملی</td></tr>
        </table>
      </div>
      <!-- روش مطالعه -->
      <div class="card purple">
        <h3>📚 روش پیشنهادی مطالعه</h3>
        <ol>
          <li>پوشه‌ها را <strong>به ترتیب</strong> دنبال کنید.</li>
          <li>هر نوت‌بوک را <strong>اجرا کنید</strong> و کدها را <strong>تغییر دهید</strong>.</li>
          <li>تمرین‌های پایان هر فصل را <strong>انجام دهید</strong> و خروجی را تحلیل کنید.</li>
          <li>از <strong>VS Code</strong> استفاده کنید و Kernel را روی <code>py-course</code> تنظیم کنید.</li>
        </ol>
      </div>
      <!-- نکات تکمیلی -->
      <div class="card red">
        <h3>💡 نکات تکمیلی</h3>
        <ul>
          <li>همیشه نسخه پایتون و فعال بودن محیط Conda را چک کنید.</li>
          <li>اگر نوت‌بوک اجرا نشد، Kernel را از بالای صفحه تغییر دهید.</li>
          <li>برای رفع اشکال، ابتدا <code>pip list</code> و <code>python --version</code> را چک کنید.</li>
        </ul>
      </div>
      <!-- مشارکت -->
      <div class="card blue">
        <h3>🤝 مشارکت و پشتیبانی</h3>
        <p>✨ اگر پیشنهادی دارید یا با اشکالی مواجه شدید:</p>
        <ul>
          <li>➡️ یک <a href="https://github.com/yourusername/python-course/issues" target="_blank">Issue</a> ثبت کنید</li>
          <li>➡️ یا مستقیماً در نوت‌بوک‌ها یادداشت بگذارید!</li>
        </ul>
        <p>⭐ اگر از این دوره استفاده کردید، لطفاً <strong>ستاره (Star)</strong> بزنید!</p>
      </div>
      <!-- مجوز -->
      <div class="card green">
        <h3>📜 مجوز</h3>
        <p>این پروژه تحت مجوز <a href="./LICENSE">MIT</a> منتشر شده است.</p>
        <p>آزادانه استفاده، کپی و اصلاح کنید — فقط نام منبع را ذکر کنید 🙏</p>
      </div>
    </div>
  </div>

</body>
</html>
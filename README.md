<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ডাক্তার অ্যাপয়েন্টমেন্ট</title>
  <style>
    body{
      font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: linear-gradient(135deg,#0f2027,#203a43,#2c5364);
      color:#fff;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .card{
      background:#111827;
      width:100%;
      max-width:420px;
      padding:24px;
      border-radius:16px;
      box-shadow:0 20px 40px rgba(0,0,0,.4);
    }
    h1{
      font-size:22px;
      margin-bottom:16px;
      text-align:center;
    }
    label{
      display:block;
      margin-top:12px;
      font-size:14px;
      opacity:.9;
    }
    input, select, button{
      width:100%;
      margin-top:6px;
      padding:10px;
      border-radius:10px;
      border:none;
      outline:none;
      font-size:14px;
    }
    input, select{
      background:#1f2933;
      color:#fff;
    }
    button{
      margin-top:18px;
      background:#22c55e;
      color:#022c22;
      font-weight:600;
      cursor:pointer;
    }
    button:hover{
      background:#16a34a;
    }
    .note{
      margin-top:14px;
      font-size:12px;
      text-align:center;
      opacity:.7;
    }
    .success{
      display:none;
      margin-top:16px;
      background:#064e3b;
      padding:12px;
      border-radius:10px;
      text-align:center;
      font-size:14px;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>ডাক্তার অ্যাপয়েন্টমেন্ট</h1>

    <label>রোগীর নাম</label>
    <input type="text" id="name" placeholder="আপনার নাম লিখুন" />

    <label>মোবাইল নাম্বার</label>
    <input type="tel" id="phone" placeholder="01XXXXXXXXX" />

    <label>ডাক্তার নির্বাচন করুন</label>
    <select id="doctor">
      <option>ডা. আহমেদ (মেডিসিন)</option>
      <option>ডা. রাহিম (কার্ডিওলজি)</option>
      <option>ডা. সুমি (গাইনি)</option>
    </select>

    <label>তারিখ</label>
    <input type="date" id="date" />

    <label>সময়</label>
    <select id="time">
      <option>সকাল ১০টা</option>
      <option>দুপুর ১২টা</option>
      <option>বিকাল ৪টা</option>
      <option>রাত ৮টা</option>
    </select>

    <button onclick="book()">অ্যাপয়েন্টমেন্ট নিন</button>

    <div class="success" id="success">✅ আপনার অ্যাপয়েন্টমেন্ট রিকোয়েস্ট পাঠানো হয়েছে</div>

    <div class="note">ডেমো ওয়েবসাইট — ব্যাকএন্ড / পেমেন্ট যুক্ত নয়</div>
  </div>

  <script>
    function book(){
      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const date = document.getElementById('date').value;

      if(!name || !phone || !date){
        alert('সব তথ্য পূরণ করুন');
        return;
      }
      document.getElementById('success').style.display='block';
    }
  </script>
</body>
</html>
# doctors-appoyenment

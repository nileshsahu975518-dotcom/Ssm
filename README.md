<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LinkBio Pro</title>
  <style>
    :root{--bg:#0b1220;--card:#111827;--pri:#22c55e;--txt:#e5e7eb;--mut:#9ca3af}
    *{box-sizing:border-box} body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto;background:linear-gradient(180deg,#020617,#0b1220);color:var(--txt)}
    .wrap{max-width:420px;margin:auto;padding:14px}
    .card{background:rgba(17,24,39,.9);border:1px solid #1f2937;border-radius:16px;box-shadow:0 10px 30px rgba(0,0,0,.35);padding:16px;margin-bottom:14px}
    .brand{display:flex;align-items:center;gap:10px}
    .logo{width:44px;height:44px;border-radius:12px;background:#22c55e;display:grid;place-items:center;color:#022c22;font-weight:900}
    h1{font-size:20px;margin:6px 0} h2{font-size:16px;margin:8px 0}
    .btn{width:100%;padding:14px;border-radius:14px;border:0;background:linear-gradient(135deg,#22c55e,#16a34a);color:#022c22;font-weight:800;margin-top:10px}
    .btn.alt{background:#1f2937;color:#e5e7eb;border:1px solid #374151}
    .link{display:block;text-decoration:none;color:#e5e7eb;padding:14px;border-radius:14px;border:1px solid #1f2937;background:#0b1220;margin-top:10px}
    input,select{width:100%;padding:12px;border-radius:12px;border:1px solid #1f2937;background:#020617;color:#e5e7eb;margin-top:8px}
    .tabs{display:flex;gap:8px} .tab{flex:1;text-align:center;padding:10px;border-radius:12px;border:1px solid #1f2937;background:#020617}
    .tab.active{background:#1f2937}
    .mut{color:var(--mut);font-size:12px}
    .hide{display:none}
    .nav{position:sticky;bottom:0;background:#020617;border-top:1px solid #1f2937;display:flex}
    .nav a{flex:1;text-align:center;padding:12px;color:#9ca3af;text-decoration:none}
    .nav a.active{color:#22c55e}
  </style>
</head>
<body>
  <div class="wrap">
    <!-- LINK IN BIO -->
    <div id="bio" class="card">
      <div class="brand"><div class="logo">LP</div><div><h1>LinkBio Pro</h1><div class="mut">Mobile-first • App-like</div></div></div>
      <a class="link" href="#" onclick="show('login')">Login / Register</a>
      <a class="link" href="#" onclick="show('user')">User Panel </a>
      <a class="link" href="#" onclick="show('admin')">Admin Panel </a>
      <a class="link" href="#" onclick="show('pay')">Add Funds (UPI)</a>
    </div><!-- AUTH -->
<div id="login" class="card hide">
  <div class="tabs"><div id="tlog" class="tab active" onclick="tab('log')">Login</div><div id="treg" class="tab" onclick="tab('reg')">Register</div></div>
  <div id="log"><input placeholder="Email"/><input placeholder="Password" type="password"/><button class="btn" onclick="demo()">Login</button></div>
  <div id="reg" class="hide"><input placeholder="Name"/><input placeholder="Email"/><input placeholder="Password" type="password"/><button class="btn" onclick="demo()">Create Account</button></div>
  <button class="btn alt" onclick="show('bio')">Back</button>
</div>

<!-- USER PANEL -->
<div id="user" class="card hide">
  <h2>User Panel</h2>
  <div class="mut">Balance</div><h1>₹0.00</h1>
  <select><option>Instagram Followers</option><option>Instagram Likes</option></select>
  <input placeholder="Profile / Post URL"/>
  <input placeholder="Quantity"/>
  <button class="btn" onclick="demo()">Place Order</button>
  <button class="btn alt" onclick="show('bio')">Back</button>
</div>

<!-- ADMIN PANEL -->
<div id="admin" class="card hide">
  <h2>Admin Panel</h2>
  <input placeholder="Service Name"/>
  <input placeholder="Rate"/>
  <button class="btn" onclick="demo()">Add Service</button>
  <button class="btn alt" onclick="show('bio')">Back</button>
</div>

<!-- PAYMENT -->
<div id="pay" class="card hide">
  <h2>Add Funds (UPI)</h2>
  <div class="mut">UPI ID</div><h1>neelesh-lucky@fam</h1>
  <a class="btn" href="upi://pay?pa=neelesh-lucky@fam&pn=LinkBio%20Pro&cu=INR">Pay via UPI App</a>
  <div class="mut">Razorpay integration scaffold (keys required)</div>
  <button class="btn alt" onclick="show('bio')">Back</button>
</div>

  </div>  <script>
    function show(id){['bio','login','user','admin','pay'].forEach(x=>document.getElementById(x).classList.add('hide'));document.getElementById(id).classList.remove('hide')}
    function tab(t){document.getElementById('log').classList.toggle('hide',t!=='log');document.getElementById('reg').classList.toggle('hide',t!=='reg');document.getElementById('tlog').classList.toggle('active',t==='log');document.getElementById('treg').classList.toggle('active',t==='reg')}
    function demo(){}
  </script></body>
</html>upi://pay?pa=neelesh-lucky@fam

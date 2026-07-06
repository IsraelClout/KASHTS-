<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kwabeng Anglican Senior High Tech School</title>
<style>
:root{
  /* Colors pulled directly from your crest */
  --kass-purple-dark:#3a1e5c;
  --kass-purple:#5d3a8a;
  --kass-purple-light:#7a5aa8;
  --kass-lavender:#a78bfa;
  --kass-silver:#e5e7eb;
  --text:#ffffff;
}
*{box-sizing:border-box;margin:0;padding:0;font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif}
body{
  background: linear-gradient(180deg, var(--kass-purple-dark) 0%, var(--kass-purple) 50%, var(--kass-purple-dark) 100%);
  color:var(--text);
  min-height:100vh;
  background-attachment: fixed; /* keeps background consistent */
}
.container{max-width:1200px;margin:0 auto;padding:0 20px}
img{max-width:100%;display:block;border-radius:12px}

/* ===== CONSTANT DASHBOARD HEADER ===== */
header{
  position:sticky;top:0;z-index:1000;
  background:rgba(58,30,92,.92);
  backdrop-filter:blur(16px);
  border-bottom:3px solid var(--kass-lavender);
  box-shadow: 0 4px 20px rgba(0,0,0,.3);
}
.nav{max-width:1200px;margin:0 auto;padding:14px 20px;display:flex;justify-content:space-between;align-items:center;gap:16px;flex-wrap:wrap}
.logo{display:flex;align-items:center;gap:14px;font-weight:800;font-size:1.1rem;color:var(--kass-silver)}
.logo img{height:55px;width:55px;border-radius:10px;background:white;padding:4px;border:2px solid var(--kass-lavender)}
.logo span small{display:block;font-size:.7rem;font-weight:500;opacity:.8}
.tabs{display:flex;gap:8px;flex-wrap:wrap}
.tab-btn{background:transparent;border:1px solid transparent;color:var(--text);padding:10px 18px;border-radius:10px;font-weight:700;cursor:pointer;transition:.2s;font-size:.95rem}
.tab-btn:hover{background:rgba(167,139,250,.2)}
.tab-btn.active{background:var(--kass-lavender);color:var(--kass-purple-dark)}

/* ===== PAGES ===== */
.page{display:none;padding:80px 0;min-height:calc(100vh - 140px);animation:fade .4s}
.page.active{display:block}
@keyframes fade{from{opacity:0;transform:translateY(10px)}}
h1{font-size:clamp(2.4rem,5vw,3.8rem);font-weight:800;line-height:1.1;margin-bottom:20px;text-align:center}
h1 span{color:var(--kass-lavender)}
h2{font-size:2.2rem;color:var(--kass-lavender);margin-bottom:20px;text-align:center}
p.lead{font-size:1.15rem;max-width:750px;opacity:.9;margin:0 auto 30px;text-align:center}
.btn{background:var(--kass-lavender);color:var(--kass-purple-dark);padding:14px 28px;border-radius:12px;font-weight:800;text-decoration:none;display:inline-block;border:none;cursor:pointer;transition:.3s}
.btn:hover{transform:translateY(-3px);box-shadow:0 10px 30px rgba(167,139,250,.5)}
.btn-outline{background:transparent;border:2px solid var(--kass-silver);color:var(--kass-silver)}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:24px;margin-top:30px}
.card{
  background:rgba(93,58,138,.4);
  border:1px solid rgba(167,139,250,.3);
  backdrop-filter:blur(10px);
  padding:24px;border-radius:18px;
  transition:.3s
}
.card:hover{border-color:var(--kass-lavender);transform:translateY(-5px)}
.card h3{color:var(--kass-lavender);margin-bottom:10px}

/* ===== GALLERY PAGE ===== */
.gallery-controls{display:flex;justify-content:center;gap:10px;margin-bottom:30px;flex-wrap:wrap}
.filter-btn{padding:8px 16px;border-radius:20px;background:rgba(167,139,250,.15);border:1px solid rgba(167,139,250,.3);color:var(--text);cursor:pointer;font-weight:600}
.filter-btn.active{background:var(--kass-lavender);color:var(--kass-purple-dark)}
.gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:18px}
.gallery-item{position:relative;overflow:hidden;border-radius:14px;border:2px solid rgba(167,139,250,.2);cursor:pointer;transition:.3s}
.gallery-item:hover{transform:translateY(-5px);border-color:var(--kass-lavender)}
.gallery-item img{height:240px;width:100%;object-fit:cover}
.gallery-caption{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(transparent,rgba(58,30,92,.9));padding:12px;font-size:.9rem;font-weight:600}

/* ===== LIGHTBOX ===== */
.lightbox{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,.9);z-index:2000;place-items:center}
.lightbox.active{display:grid}
.lightbox img{max-width:90%;max-height:85%;border-radius:16px;border:3px solid var(--kass-lavender)}
.lightbox-close{position:absolute;top:20px;right:30px;font-size:40px;color:white;cursor:pointer}

/* ===== FORM ===== */
form{display:grid;gap:14px;max-width:600px;margin:0 auto}
input,textarea,select{width:100%;padding:14px;border-radius:10px;border:1px solid rgba(167,139,250,.3);background:rgba(93,58,138,.4);color:var(--text);font-size:1rem}
input:focus{outline:2px solid var(--kass-lavender)}

footer{text-align:center;padding:25px;background:var(--kass-purple-dark);font-size:.9rem;opacity:.8;border-top:2px solid var(--kass-lavender)}
.motto{text-align:center;font-style:italic;color:var(--kass-lavender);font-weight:700;font-size:1.1rem;margin-top:10px}
@media(max-width:800px){.tabs{width:100%;justify-content:center}}
</style>
</head>
<body>

<!-- ===== CONSTANT DASHBOARD ===== -->
<header>
  <div class="nav">
    <div class="logo">
      <img src=" Screenshot_20260701-223509 (1).png" alt="KASS Crest">
      <span>KWABENG ANGLICAN SHS TECH<br><small>BODY • SOUL • MIND</small></span>
    </div>
    <div class="tabs">
      <button class="tab-btn active" onclick="showPage('home')">Home</button>
      <button class="tab-btn" onclick="showPage('about')">About</button>
      <button class="tab-btn" onclick="showPage('gallery')">Gallery</button>
      <button class="tab-btn" onclick="showPage('academics')">Academics</button>
      <button class="tab-btn" onclick="showPage('admission')">Admission</button>
      <button class="tab-btn" onclick="showPage('contact')">Contact</button>
    </div>
  </div>
</header>

<main class="container">

  <!-- ===== PAGE 1: HOME ===== -->
  <section id="home" class="page active">
    <div style="text-align:center;padding-top:40px">
      <h1>Welcome to <span>Kwabeng Anglican SHS Tech</span></h1>
      <p class="lead">Established 1983. Training leaders in Body, Soul, and Mind for service to God and country.</p>
      <div style="display:flex;gap:16px;justify-content:center;flex-wrap:wrap">
        <button class="btn" onclick="showPage('admission')">Apply Now</button>
        <button class="btn btn-outline" onclick="showPage('gallery')">View Gallery</button>
      </div>
      
      <div class="grid" style="margin-top:60px">
        <div class="card"><h3>Est. 1983</h3><p>Over 40 years of academic and Moral excellence</p></div>
        <div class="card"><h3>8 Programs</h3><p>Science, Agriculture, Arts, Technical, Business, Home Economics</p></div>
         <div class="card"><h3>School Category</h3><p> B </p></div>
        <div class="card"><h3>Boarding & Day</h3><p>Mixed gender school in Kwabeng, Eastern Region</p></div>
      </div>
      <p class="motto">"BODY • SOUL • MIND"</p>
    </div>
  </section>

  <!-- ===== PAGE 2: ABOUT ===== -->
  <section id="about" class="page">
    <h2>About KASHTS</h2>
    <p class="lead">Kwabeng Anglican Senior High Tech School is committed to holistic education rooted in Anglican values.</p>
    <div class="grid">
      <div class="card"><h3>Our Mission</h3><p>To provide quality Discipline, Religious values and Academic excellence that develops the whole person - Body, Soul, and Mind.</p></div>
      <div class="card"><h3>Our Vision</h3><p>To be a center of excellence producing disciplined, skilled, and God-fearing leaders.</p></div>
      <h3>Our Crest</h3>
       <img src=" Screenshot_20260701-223509 (1).png" alt="KASS Crest"> 
    </div>
  </section>

  <!-- ===== PAGE 3: GALLERY ===== -->
  <section id="gallery" class="page">
    <h2>KASHTS Gallery</h2>
    <p class="lead">Life at Kwabeng Anglican SHS Tech</p>
    
    <div class="gallery-controls">
      <button class="filter-btn active" onclick="filterGallery('all')">All</button>
      <button class="filter-btn" onclick="filterGallery('students')">Students</button>
      <button class="filter-btn" onclick="filterGallery('campus')">Campus</button>
      <button class="filter-btn" onclick="filterGallery('events')">Events</button>
    </div>

    <div class="gallery-grid">
      <div class="gallery-item" data-cat="students"><img src="Screenshot_20260704-195516 (1).png" alt="Classroom"><div class="gallery-caption">School Choir</div></div>
      <div class="gallery-item" data-cat="students"><img src="Screenshot_20260704-195715 (2).png" alt="Classroom"><div class="gallery-caption">School Bus</div></div>
      <div class="gallery-item" data-cat="students"><img src="Screenshot_20260704-195411 (1).png" alt="Classroom"><div class="gallery-caption">Students</div></div>
      <div class="gallery-item" data-cat="campus"><img src=" IMG-20260701-WA0000 (1).jpg" alt="Building"><div class="gallery-caption">Main School Block</div></div>
      <div class="gallery-item" data-cat="events"><img src="a7c6943c444a4489aeefcff4011c1a7f (1).jpg" alt="Head"><div class="gallery-caption">Headmistrees</div></div>
            <div class="gallery-item" data-cat="students"><img src="Screenshot_20260704-195417 (1).png" alt="Classroom"><div class="gallery-caption">School Church Cloth</div></div>
            <div class="gallery-item" data-cat="students"><img src="IMG-20260701-WA0001.jpg" alt="Classroom"><div class="gallery-caption">School Staffs</div></div>
      <div class="gallery-item" data-cat="students"><img src="pm_1782230655824_cmp.jpg" alt="Graduation"><div class="gallery-caption">Students</div></div>
       <div class="gallery-item" data-cat="students"><img src="Screenshot_20260630-191542 (1) (1).png " alt="Graduation"><div class="gallery-caption">Campus</div></div>
         <div class="gallery-item" data-cat="students"><img src=" IMG-20260630-WA0074.jpg" alt="Classroom"><div class="gallery-caption">School Life</div></div>
     <div class="gallery-item" data-cat="campus"><img src="Screenshot_20260704-195531 (1) (1).png" alt="Chapel"><div class="gallery-caption">School Chaplincy Head</div></div>
            <div class="gallery-item" data-cat="students"><img src="Screenshot_20260704-195453 (1).png " alt="Graduation"><div class="gallery-caption">KASHTS Media</div></div>
           <div class="gallery-item" data-cat="students"><img src="3aef985b34f86af65d83ccaa92600097.png" alt="Classroom"><div class="gallery-caption">School Choir</div></div>
      <div class="gallery-item" data-cat="students"><img src=" e31f114854f6dcf9b8068e99a3be0b0c.png" alt="Classroom"><div class="gallery-caption">Holy Spirit Mood</div></div>
    <div class="gallery-item" data-cat="events"><img src="Screenshot_20260704-195506 (1).png" alt="Cultural"><div class="gallery-caption">Anniversiry Day</div></div>
 <div class="gallery-item" data-cat="students"><img src=" IMG-20260630-WA0035.jpg" alt="Classroom"><div class="gallery-caption">School Entrance</div></div>
       <div class="gallery-item" data-cat="students"><img src=" 8a771873e0d660229a15c97394bd5c1b.png" alt="Classroom"><div class="gallery-caption">Sunday Service</div></div>
  <div class="gallery-item" data-cat="students"><img src="IMG-20260630-WA0065.jpg" alt="Classroom"><div class="gallery-caption">Technical class</div></div>
        <div class="gallery-item" data-cat="students"><img src=" 9cbf0f3108b4a66c48b7b6f00722e1eb.png" alt="Classroom"><div class="gallery-caption">Asist Head Domestic</div></div>
    <div class="gallery-item" data-cat="students"><img src=" pm_1782230651856_cmp.jpg" alt="Classroom"><div class="gallery-caption">School Church Wear</div></div>
     <div class="gallery-item" data-cat="students"><img src=" Screenshot_20260705-010931 (1).png" alt="Classroom"><div class="gallery-caption">ICT Lab</div></div>
      <div class="gallery-item" data-cat="students"><img src=" Screenshot_20260705-010908 (1).png" alt="Classroom"><div class="gallery-caption">Science Block</div></div>
       <div class="gallery-item" data-cat="students"><img src=" Screenshot_20260705-010740 (1).png" alt="Classroom"><div class="gallery-caption">Dormatory</div></div>
        <div class="gallery-item" data-cat="students"><img src=" Screenshot_20260705-010901 (1).png" alt="Classroom"><div class="gallery-caption">School Cardet</div></div>
        <div class="gallery-item" data-cat="students"><img src="IMG-20260703-WA0001.jpg" alt="Classroom"><div class="gallery-caption">School Uniform</div></div>
          <div class="gallery-item" data-cat="students"><img src=" Screenshot_20260705-010854 (1).png" alt="Classroom"><div class="gallery-caption">Classroom</div></div>
          <div class="gallery-item" data-cat="students"><img src="IMG-20260630-WA0075.jpg" alt="Classroom"><div class="gallery-caption">Past Students</div></div>
    </div>
  </section>

  <!-- ===== PAGE 4: ACADEMICS ===== -->
  <section id="academics" class="page">
    <h2>Academic & Technical Programs</h2>
    <p class="lead">Choose your path to excellence</p>
    <div class="grid">
      <div class="card"><h3>General Arts</h3><p>Economics, Literature, Government, History, Information Communication & Technology, Elective Math, Geography, CRS, French, Twi, General Knowledge In Arts</p></div>
      <div class="card"><h3>General Science</h3><p>Physics, Chemistry, Biology, Elective Math, Information Communication & Technology</p></div>
       <div class="card"><h3> Agriculture Science</h3><p>Physics, Chemistry, Fishery, Crops, General Agriculture, Elective Math, Animal Husborndery</p></div>
      <div class="card"><h3>Technical</h3><p>Applied Electricity & Electronics ,   Building Contruction, Elective Math, Physics, Technical Drawing</p></div>
      <div class="card"><h3>Visual Arts</h3><p>Graphic Design, Picture Making, General Knowledge In Arts, Ceramics, Jewellery, Portery, Textiles</p></div>
      <div class="card"><h3>Home Economics</h3><p>Food & Nutrition, Clothing, Management In Living, Economics, General Knowledge In Arts </p></div>
      <div class="card"><h3>Business</h3><p>Accounting, Costing, Economics, Business Management</p></div>
    </div>
  </section>

  <!-- ===== PAGE 5: ADMISSION ===== -->
  <section id="admission" class="page">
    <h2>Admissions 2026/2027</h2>
    <p class="lead">Join the KASHTS Family. Body Soul Mind.</p>
    
    <div class="grid" style="margin-bottom:40px">
      <div class="card"><h3>Requirements</h3><p>BECE Certificate, Placement Slip, Birth Certificate, 4 Passport Pictures</p></div>
      <div class="card"><h3>Cut-off Point</h3><p>Check GES Placement. Both Boarding and Day available.</p></div>
    </div>

    <form onsubmit="alert('Application received! KASS will contact you shortly.');return false;">
      <input type="text" placeholder="Student Full Name" required>
      <input type="tel" placeholder="Parent/Guardian WhatsApp Number" required>
      <select required>
        <option value="">Select Program</option>
        <option>General Science</option>
        <option>General Arts</option>
        <option>Agriculture Science</option>
        <option>Technical</option>
        <option>Visual Arts</option>
        <option>Home Economics</option>
        <option>Business</option>
      </select>
      <textarea placeholder="Any Questions?" rows="4"></textarea>
      <button class="btn" type="submit">Submit Application</button>
    </form>
  </section>

  <!-- ===== PAGE 6: CONTACT ===== -->
  <section id="contact" class="page">
    <h2>Contact KASHTS</h2>
    <p class="lead">We’d love to hear from you</p>
    <div class="grid">
      <div class="card"><h3>Address</h3><p>Kwabeng, Eastern Region, Ghana<br>P.O. Box 03, Akyem-Kwabeng</p></div>
      <div class="card"><h3>Phone</h3><p>024 480 0137 | 020 555 2735</p></div>
      <div class="card"><h3>Connect To KASHTS: </h3><p>KASHTS Media on TicTok</p></div>
    </div>
  </section>

</main>

<!-- ===== LIGHTBOX FOR GALLERY ===== -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="">
</div>

<footer>© 2026 Kwabeng Anglican Senior High Tech School | BODY • SOUL • MIND | Est. 1983</footer>

<script>
// ===== PAGE SWITCHING =====
function showPage(id){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  event.target.classList.add('active');
  window.scrollTo({top:0, behavior:'smooth'});
}

// ===== GALLERY FILTER =====
function filterGallery(cat){
  document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('active'));
  event.target.classList.add('active');
  document.querySelectorAll('.gallery-item').forEach(item=>{
    if(cat==='all' || item.dataset.cat===cat) item.style.display='block';
    else item.style.display='none';
  })
}

// ===== GALLERY LIGHTBOX =====
document.querySelectorAll('.gallery-item img').forEach(img=>{
  img.onclick = (e) => {
    e.stopPropagation();
    document.getElementById('lightbox-img').src = img.src;
    document.getElementById('lightbox').classList.add('active');
  }
})
function closeLightbox(){
  document.getElementById('lightbox').classList.remove('active');
}
</script>
</body>
</html>

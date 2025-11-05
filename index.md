<link rel="stylesheet" href="assets/css/style.css">

# QA Chronicles — Kelina Cowell

Monthly, light-hearted illustrated posts that distil real QA lessons from my portfolio projects. All artwork is my own.

---

## Issue 1 — <em>If it doesn’t function, nothing else matters.</em>

<div class="flipbook" id="issue1">
  <button class="fb-btn prev" aria-label="Previous page">←</button>
  <img class="fb-page" src="" alt="">
  <button class="fb-btn next" aria-label="Next page">→</button>
  <div class="fb-meta"><span class="fb-count">1</span>/<span class="fb-total">1</span></div>
</div>

<script>
(function () {
  const pages = [
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-1.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-2.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-3.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-4.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-5.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-6.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-7.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-8.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-9.png.png",
    "{{ site.baseurl }}/assets/images/chronicles/issue-01/page-10.png.png"
  ];
  const root = document.getElementById('issue1');
  const img = root.querySelector('.fb-page');
  const count = root.querySelector('.fb-count');
  const totalEl = root.querySelector('.fb-total'); let i=0;
  function show(n){ i=(n+pages.length)%pages.length; img.classList.add('flip');
    img.src=pages[i]; img.alt='Issue 1 page '+(i+1);
    count.textContent=(i+1); totalEl.textContent=pages.length;
    setTimeout(()=>img.classList.remove('flip'),220); }
  root.querySelector('.prev').onclick=()=>show(i-1);
  root.querySelector('.next').onclick=()=>show(i+1);
  document.onkeydown=(e)=>{ if(e.key==='ArrowRight')show(i+1); if(e.key==='ArrowLeft')show(i-1); };
  let sx=0; img.addEventListener('touchstart',e=>sx=e.changedTouches[0].clientX,{passive:true});
  img.addEventListener('touchend',e=>{const dx=e.changedTouches[0].clientX-sx; if(Math.abs(dx)>30){dx<0?show(i+1):show(i-1)}},{passive:true});
  img.addEventListener('load',()=>{[ (i+1)%pages.length, (i-1+pages.length)%pages.length ].forEach(n=>{const a=new Image(); a.src=pages[n];});});
  show(0);
})();
</script>

- **Summary:** A playful look at how keyboard ↔ controller context can get lost around Pause/Join-In/Resume, and the quick repros I use to catch it early.
- **Based on:** <em>Battletoads — Functional Testing (input parity)</em>
- **Case study:** Wants Receipts? [⬅ Go to my Battletoads QA project](https://kelinacowell.github.io/Manual-QA-Portfolio-Kelina-Cowell/projects/battletoads/)
- **LinkedIn post:** (add the URL here when published)

[⬅ Back to Homepage](https://kelinacowellqa.github.io)

<p>
  <a class="cta-btn" href="https://kelinacowellqa.github.io">⬅ Back to Portfolio Hub</a>
</p>

  <a class="cta-btn" href="https://kelinacowellqa.github.io">⬅ Back to Portfolio Hub</a>
</p>


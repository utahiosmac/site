This is our 12th group survey. Our Slack group now has 971 members. Our group is primarily focused on iOS or Mac developers in the Utah area. 113 people responded to the survey.

**AUTHOR**: Jacob Bullock 

**PUBLISHED**: September 2025

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>2025 Summer – iOS & Mac Developers Survey (Utah)</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.3/dist/chart.umd.min.js"></script>
  <style>
    :root {
      --bg: #ffffff;
      --card: #ffffff;
      --ink: #111827; /* gray-900 */
      --muted: #6b7280; /* gray-500 */
      --grid: #e5e7eb;  /* gray-200 */
      --border: #e5e7eb;
    }
    * { box-sizing: border-box; }
    body { margin:0; font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji"; background:var(--bg); color:var(--ink); line-height:1.45; }
    header { padding: 36px 20px 8px; text-align: center; }
    h1 { font-weight: 800; margin: 0 0 6px; font-size: clamp(24px,4vw,36px); }
    .sub { color: var(--muted); font-weight: 500; }
    .note { max-width: 900px; margin: 0 auto 10px; padding: 0 20px; color: var(--muted); text-align: center; font-size: 14px; }
    main { max-width: 1100px; margin: 16px auto 48px; padding: 0 20px; display: grid; grid-template-columns: 1fr; gap: 18px; }
    .card { background: var(--card); border: 1px solid var(--border); border-radius: 14px; padding: 14px 14px 10px; box-shadow: 0 1px 2px rgba(0,0,0,0.04); }
    .card h2 { font-size: 16px; margin: 0 0 8px; font-weight: 700; color: var(--ink); }
    .legend { display: flex; flex-wrap: wrap; gap: 10px 14px; margin: 8px 4px 6px; padding: 0; list-style: none; }
    .legend li { display: flex; align-items: center; gap: 6px; font-size: 13px; color: var(--ink); cursor: pointer; }
    .legend .swatch { width: 10px; height: 10px; border-radius: 2px; border: 1px solid rgba(0,0,0,0.15); }
  </style>
</head>
<body>
  <!-- <header>
    <h1>2025 Summer – iOS & Mac Developers Survey (Utah)</h1>
    <div class="sub">113 responses</div>
  </header> -->
  <p class="note">Multi-select answers are split on commas / semicolons / slashes and counted individually.</p>
  <main id="grid"></main>
  <footer class="note">Generated from the attached Excel responses (first = timestamp, last = open feedback excluded).</footer>

  <script>
    const CHART_DATA = {"What type of development do you do professionally?": {"iOS": 100, "Android": 31, "Web": 23, "macOS": 18, "Frameworks or SDKs": 15, "watchOS": 4, "Backend": 3, "tvOS": 3, "Embedded": 1, "I work on a digital forensics product that is not specifically \"iOS\" but is definitely iOS-adjacent": 1, "Python": 1, "Web backend": 1}, "How old are you?": {"30-39": 54, "40-49": 35, "26-29": 10, "50-59": 7, "18-25": 5, "60+": 2}, "How do you primarily code your apps?": {"Swift": 83, "React Native": 9, "Flutter": 6, "Objective-C": 3, "Python": 3, "C#": 2, "Typescript": 2, "Angular": 1, "Elixir": 1, "Java": 1, "Kotlin": 1, "Multiple of languages depending on the work": 1, "React": 1, "Swift and moving to RN =": 1, "TypeScript": 1, "Unity": 1, "Web": 1}, "My education includes": {"Bachelors degree in Computer Science or other tech related field": 63, "Code bootcamp (e.g. Dev Mountain)": 20, "Bachelors degree in a non tech related field": 15, "Masters Degree in Computer Science or other tech related field": 15, "Some college": 14, "Masters Degree in a non tech related field": 5, "mostly self taught with books and tutorials": 5, "No formal education": 5, "course).": 1, "Doctorate in a non tech related field": 1, "my iOS skills are entirely self taught (never took a mobile-focused class": 1, "Projects and self pursuits": 1, "While I have a CS degree": 1}, "How long have you been programming professionally?": {"10-14 years": 39, "15+ years": 36, "7-9 years": 21, "3-6 years": 12, "1 -2 years": 4}, "Your Location (County)": {"Utah County": 56, "Salt Lake County": 24, "Not in Utah": 20, "Davis County": 6, "Weber": 6, "Other Utah County": 5, "I would rather not say": 1}, "How many days per week are you required to be in the office?": {"fully remote": 75, "No in-office requirement": 75, "3 days": 14, "1 day": 9, "2 days": 5, "5 days": 5, "4 days": 2}, "What is your current level?": {"Senior": 57, "Staff": 23, "Principal": 19, "Mid": 9, "Junior": 3}, "If you work full time for someone else, what is your annual base salary? (Please write the whole number. For instance if you make thirty thousand, please write 30000.  Please DO NOT write 30k, 30, thirty thousand, etc.)": {"160000.0": 6, "170000.0": 5, "180000.0": 4, "210000.0": 4, "250000.0": 4, "140000.0": 3, "165000.0": 3, "175000.0": 3, "185000.0": 3, "200000.0": 3, "205000.0": 3, "100000.0": 2, "125000.0": 2, "135000.0": 2, "190000.0": 2, "191000.0": 2, "196000.0": 2, "220000.0": 2, "260000.0": 2, "1.0": 1, "105000.0": 1, "117504.0": 1, "118000.0": 1, "123000.0": 1, "136500.0": 1, "145000.0": 1, "150000.0": 1, "155300.0": 1, "157500.0": 1, "163000.0": 1, "172000.0": 1, "173000.0": 1, "174900.0": 1, "175500.0": 1, "175543.42": 1, "176000.0": 1, "178500.0": 1, "179300.0": 1, "185400.0": 1, "189000.0": 1, "196560.0": 1, "201000.0": 1, "211000.0": 1, "215000.0": 1, "218000.0": 1, "230000.0": 1, "245000.0": 1, "247000.0": 1, "255000.0": 1, "309000.0": 1, "35360.0": 1, "75000.0": 1, "80000.0": 1, "83000.0": 1}, "If you work full time for someone else, what is your total annual compensation (salary+bonus+) (Please write the whole number. For instance if your total compensation is thirty thousand, please write 30000.  Please DO NOT write 30k, 30, thirty thousand, etc.)": {"180000.0": 5, "210000.0": 5, "160000.0": 4, "165000.0": 4, "250000.0": 4, "125000.0": 3, "200000.0": 3, "220000.0": 3, "260000.0": 3, "140000.0": 2, "193000.0": 2, "195000.0": 2, "215000.0": 2, "230000.0": 2, "1.0": 1, "105000.0": 1, "117504.0": 1, "120000.0": 1, "123000.0": 1, "136500.0": 1, "148000.0": 1, "150000.0": 1, "151000.0": 1, "152000.0": 1, "155000.0": 1, "155250.0": 1, "170000.0": 1, "173000.0": 1, "175543.42": 1, "182000.0": 1, "185000.0": 1, "186360.0": 1, "189000.0": 1, "190000.0": 1, "196000.0": 1, "196350.0": 1, "201250.0": 1, "205000.0": 1, "207900.0": 1, "211000.0": 1, "212000.0": 1, "218000.0": 1, "225000.0": 1, "227000.0": 1, "231150.0": 1, "245000.0": 1, "265000.0": 1, "275000.0": 1, "283455.0": 1, "293000.0": 1, "300000.0": 1, "350000.0": 1, "35360.0": 1, "357500.0": 1, "415000.0": 1, "484000.0": 1, "590000.0": 1, "600000.0": 1, "670000.0": 1, "75000.0": 1, "750000.0": 1, "83000.0": 1}, "If you work for a company, how big is the mobile development team. (Specifically how many developers are there)": {"3-5 developers": 31, "Just me": 15, "20-49": 13, "2 developers": 12, "6-10 developers": 11, "11-19": 9, "1000+": 6, "100-499": 4, "50-99": 3, "500-999": 2}, "How much Paid Time Off do you receive at your company per year": {"Unlimited": 51, "21+ days": 20, "11-15 days": 11, "16-20 days": 10, "Only unpaid time off": 9, "6-10 days": 2}, "Does your company hire and support / mentor Junior Developers": {"No": 49, "we do not hire junior developers": 49, "but there is room for improvement": 28, "We hire junior developers and we do support them": 28, "We hire junior developers and do a great job helping them level up": 22, "but don't support them": 3, "We hire junior developers": 3}, "Do you know there is a #jobs channel in the utah slack channel and a spreadsheet for members to post current positions?": {"Yes": 106, "No": 5}, "Which AI Tools do you use in your day to day at work?": {"Chat GPT": 66, "Claude": 55, "Cursor": 43, "Gemini": 19, "Copilot": 4, "Alex Sidebar": 3, "GitHub Copilot": 3, "Alex Side Bar": 1, "Claude Code": 1, "Conductor": 1, "copilot": 1, "Firebender": 1, "Github copilot": 1, "Github Copilot": 1, "GitHub CoPilot": 1, "Grok": 1, "I use Duck.ai (powered by Chat GPT I think) occasionally": 1, "My own tools": 1, "VSCode": 1, "Warp": 1, "XcodeAI": 1}, "Does your company allow the use of AI tools?": {"Yes": 106, "No": 3}, "What percent of your code is written with the help of AI?": {"less than 25%": 64, "0.5": 29, "0.75": 6, "All Vibes (100%)": 2}, "Do you do contract app development?": {"No": 63, "on the side": 38, "Sometimes": 38, "full time": 11, "Yes": 11}, "What is your (or your employer's) hourly rate for contract app development?\t(e.g. 25)": {"150.0": 7, "125.0": 5, "75.0": 5, "100.0": 4, "200.0": 4, "120.0": 2, "175.0": 2, "250.0": 2, "30.0": 2, "45.0": 2, "60.0": 2, "0.0": 1, "1.0": 1, "105.0": 1, "110.0": 1, "117.0": 1, "130.0": 1, "165.0": 1, "210.0": 1, "29.0": 1, "50.0": 1, "65.0": 1, "80.0": 1, "85.0": 1}, "How many hours per week do you typically spend on contract work? (e.g. 40)": {"0.0": 14, "5.0": 7, "10.0": 6, "1.0": 5, "15.0": 3, "20.0": 3, "4.0": 3, "40.0": 3, "30.0": 2, "50.0": 2, "2.0": 1, "35.0": 1, "39.0": 1, "45.0": 1, "6.0": 1}, "As a contractor, what type of roles do you typically have?": {"Solo Developer on the whole project": 41, "Staff Augmentation or Individual Contributor": 18, "Architect": 12, "Project Lead": 12, "Tech lead": 11, "I don't do contract work": 1, "My own projects": 1}};

    const grid = document.getElementById('grid');
    const NUM_RE = /^-?\d+(?:\.\d+)?$/;

    function palette(n) {
      const base = ['#2563eb','#16a34a','#f59e0b','#ef4444','#7c3aed','#0ea5e9','#22c55e','#f97316','#e11d48','#a855f7','#14b8a6','#84cc16'];
      const arr = []; for (let i=0;i<n;i++) arr.push(base[i%base.length]); return arr;
    }
    function isNumericLabels(labels) { return labels.length>0 && labels.every(l => NUM_RE.test(String(l).trim())); }

    function binByStep(map, step) {
      const entries = Object.entries(map).map(([k,v])=>[Number(k), v]).filter(([n])=>!Number.isNaN(n)).sort((a,b)=>a[0]-b[0]);
      if (entries.length === 0) return map;
      const values = entries.map(e=>e[0]);
      const counts = entries.map(e=>e[1]);
      const min = Math.min(...values), max = Math.max(...values);
      const start = Math.floor(min/step)*step;
      const end   = Math.ceil(max/step)*step;
      const bins = Math.max(1, Math.ceil((end - start)/step));
      const labels = []; const tallies = Array(bins).fill(0);
      for (let i=0;i<bins;i++) { const s = start + i*step; const e = s + step; labels.push(step>=1000 ? `${Math.round(s/1000)}–${Math.round(e/1000)}k` : `${s}–${e}`); }
      for (let i=0;i<values.length;i++) { let idx = Math.floor((values[i] - start)/step); if (idx<0) idx=0; if (idx>=bins) idx=bins-1; tallies[idx] += counts[i]; }
      const out = {}; labels.forEach((l,i)=> out[l]=tallies[i]); return out;
    }

    function binStepForTitle(title) {
      const t = (title||'').toLowerCase();
      if (t.includes('hours per week')) return 5;
      if (t.includes('hourly rate')) return 20;
      if (t.includes('total annual compensation') || t.includes('annual base salary')) return 20000;
      return 0;
    }

    function buildPieLegend(chart, container) {
      container.innerHTML='';
      const ds = chart.data.datasets[0];
      const colors = ds.backgroundColor || [];
      const total = (ds.data||[]).reduce((a,b)=>a+b,0)||1;
      chart.data.labels.forEach((label, i) => {
        const li = document.createElement('li');
        const sw = document.createElement('span'); sw.className='swatch'; sw.style.backgroundColor = colors[i] || '#999'; li.appendChild(sw);
        const v = ds.data[i] || 0; const pct = Math.round(v/total*100);
        li.appendChild(document.createTextNode(` ${label} — ${v} (${pct}%)`));
        li.onclick = () => { const meta = chart.getDatasetMeta(0); const el = meta.data[i]; el.hidden = !el.hidden; chart.update(); };
        container.appendChild(li);
      });
    }

    function makeCard(title, map) {
      let localMap = Object.assign({}, map);
      const rawLabels = Object.keys(localMap);
      const step = binStepForTitle(title);
      if (step > 0 && isNumericLabels(rawLabels)) { localMap = binByStep(localMap, step); }

      const labels = Object.keys(localMap);
      const values = Object.values(localMap);
      const total = values.reduce((a,b)=>a+b,0);

      const card = document.createElement('section'); card.className='card';
      const h2 = document.createElement('h2'); h2.textContent = title; card.appendChild(h2);

      if (labels.length === 0 || total === 0) {
        const p = document.createElement('p'); p.className='sub'; p.textContent='No responses for this question';
        card.appendChild(p); grid.appendChild(card); return;
      }

      const numeric = isNumericLabels(labels);
      const many = labels.length > 10 || numeric;
      const type = (!numeric && labels.length <= 6) ? 'pie' : 'bar';

      const labelsWithCounts = type==='bar' ? labels.map((l,i)=> `${l} (${values[i]})`) : labels;

      const canvas = document.createElement('canvas'); canvas.style.display='block'; card.appendChild(canvas);
      grid.appendChild(card);

      const fixedHeight = Math.max(260, Math.min(36 * labelsWithCounts.length + 104, 560));
      canvas.height = type==='pie' ? 360 : fixedHeight; canvas.style.height = canvas.height + 'px';
      canvas.width = Math.max(360, Math.floor(card.clientWidth - 32));

      const colors = palette(labels.length);
      const cfg = {
        type: type,
        data: type==='pie'
          ? { labels, datasets:[{ data: values, backgroundColor: colors, borderColor: '#fff', borderWidth: 1 }] }
          : { labels: labelsWithCounts, datasets:[{ label:'Responses', data: values, backgroundColor: colors.map(c=>c+'cc') }] },
        options: {
          responsive:false, maintainAspectRatio:false, animation:false,
          indexAxis: (type==='bar' && many) ? 'y' : 'x',
          plugins: {
            legend: { display: false },   // disable default legend for all
            tooltip: { enabled:true }
          },
          scales: type==='pie' ? {} : {
            x: { ticks: { color:'#111827', precision:0 }, grid: { color:'var(--grid)' }, beginAtZero: true },
            y: { ticks: { color:'#111827', autoSkip:false }, grid: { color:'var(--grid)' } }
          }
        }
      };

      const chart = new Chart(canvas.getContext('2d'), cfg);

      if (type==='pie') {
        const legend = document.createElement('ul'); legend.className='legend'; card.appendChild(legend);
        buildPieLegend(chart, legend);
      }
    }

    for (const [q, map] of Object.entries(CHART_DATA)) { makeCard(q, map); }
  </script>
</body>
</html>

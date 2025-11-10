---
survey: true
---
# Summer 2025 Developer Survey

This is our twelfth group survey. Our Slack group now has 971 members. Our group is primarily focused on iOS or Mac developers in the Utah area. 113 people responded to the survey.

**AUTHOR**: Jacob Bullock 

**PUBLISHED**: November 2025

  <script>
    const CHART_DATA = { "What type of development do you do professionally?": { "iOS": 101, "macOS": 18, "watchOS": 4, "tvOS": 3, "Frameworks or SDKs": 15, "Android": 31, "Web": 23, "Backend/Python": 5, "Embedded": 1 }, "How old are you?": { "18-25": 5, "26-29": 10, "30-39": 54, "40-49": 35, "50-59": 7, "60+": 2 }, "How do you primarily code your apps?": { "Swift": 84, "React Native": 9, "Flutter": 6, "Objective-C": 3, "Python": 3, "C#": 2, "Typescript": 2, "Angular": 1, "Elixir": 1, "Java": 1, "Kotlin": 1, "Depends on the work": 1, "React": 1, "TypeScript": 1, "Unity": 1, "Web": 1 }, "My education includes": { "No formal education (self-taught, etc)": 12, "Code bootcamp (e.g. Dev Mountain)": 20, "Some college": 14, "Bachelors degree in Computer Science or other tech related field": 63, "Bachelors degree in a non tech related field": 15, "Masters Degree in Computer Science or other tech related field": 15, "Masters Degree in a non tech related field": 5, "Doctorate in a non tech related field": 1 }, "How long have you been programming professionally?": { "1-2 years": 4, "3-6 years": 12, "7-9 years": 21, "10-14 years": 39, "15+ years": 36 }, "Your Location (County)": { "Utah County": 56, "Salt Lake County": 24, "Not in Utah": 20, "Davis County": 6, "Weber": 6, "Other Utah County": 5, "I would rather not say": 1 }, "How many days per week are you required to be in the office?": { "Fully remote": 75, "No in-office requirement": 75, "1 day": 9, "2 days": 5, "3 days": 14, "4 days": 2, "5 days": 5 }, "What is your current level?": { "Junior": 3, "Mid": 9, "Senior": 57, "Staff": 23, "Principal": 19 }, "If you work full time for someone else, what is your annual base salary?": { "$0-$49,999": 1, "$50,000-$74,999": 0, "$75,000-$99,999": 3, "$100,000-$124,999": 6, "$125,000-$149,999": 9, "$150,000-$174,999": 21, "$175,000-$199,999": 24, "$200,000-$224,999": 16, "$225,000-$249,999": 3, "$250,000-$274,999": 7, "$275,000-$299,999": 0, "$300,000-$324,999": 1 }, "If you work full time for someone else, what is your total annual compensation (salary+bonus+etc)?": { "$0-$49,999": 2, "$50,000-$99,999": 2, "$100,000-$149,999": 11, "$150,000-$199,999": 32, "$200,000-$249,999": 25, "$250,000-$299,999": 11, "$300,000-$349,999": 1, "$350,000-$399,999": 2, "$400,000-$449,999": 1, "$450,000-$499,999": 1, "$500,000-$549,999": 0, "$550,000-$599,999": 1, "$600,000-$649,999": 1, "$650,000-$699,999": 1, "$700,000-$749,999": 0, "$750,000-$799,999": 1 }, "If you work for a company, how big is the mobile development team?": { "Just me": 15, "2": 12, "3-5": 31, "6-10": 11, "11-19": 9, "20-49": 13, "50-99": 3, "100-499": 4, "500-999": 2, "1000+": 6 }, "How much Paid Time Off do you receive at your company per year": { "Only unpaid time off": 9, "6-10 days": 2, "11-15 days": 11, "16-20 days": 10, "21+ days": 20, "Unlimited": 51 }, "Does your company hire and support / mentor Junior Developers": { "No, we do not hire junior developers": 49, "We hire junior developers, but don't support them": 3, "We hire junior developers, and we do support them, but there is room for improvement": 28, "We hire junior developers, and do a great job helping them level up": 22 }, "Do you know there is a #jobs channel in the Utah slack and a spreadsheet for members to post current positions?": { "Yes": 106, "No": 5 }, "Which AI Tools do you use in your day to day at work?": { "Chat GPT": 66, "Claude": 56, "Cursor": 43, "Gemini": 19, "Github Copilot": 11, "Alex Sidebar": 4, "Conductor": 1, "Firebender": 1, "Grok": 1, "Duck.ai": 1, "VSCode": 1, "Warp": 1, "XcodeAI": 1, "Custom (my own)": 1 }, "Does your company allow the use of AI tools?": { "Yes": 106, "No": 3 }, "What percent of your code is written with the help of AI?": { "less than 25%": 64, "50%": 29, "75%": 6, "100% (All Vibes)": 2 }, "Do you do contract app development?": { "No": 63, "Sometimes (on the side)": 38, "Yes (full time)": 11 }, "What is your (or your employer's) hourly rate for contract app development?": { "$0-$24": 2, "$25-$49": 5, "$50-$74": 4, "$75-$99": 7, "$100-$124": 9, "$125-$149": 6, "$150-$174": 8, "$175-$199": 2, "$200-$224": 5, "$225-$249": 0, "$250-$274": 2, "$275-$299": 0 }, "How many hours per week do you typically spend on contract work? (e.g. 40)": { "None": 14, "1-9": 18, "10-19": 9, "20-29": 3, "30-39": 4, "40-49": 4, "50+": 2 }, "As a contractor, what type of roles do you typically have?": { "I don't do contract work": 2, "Solo Developer on the whole project": 41, "Staff Augmentation or Individual Contributor": 18, "Project/Tech Lead": 23, "Architect": 12}};

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

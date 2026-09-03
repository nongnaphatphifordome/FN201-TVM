<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>เครื่องคำนวณมูลค่าเงินตามเวลา</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Thai:wght@400;500;600;700&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #F5F1E7;
    --paper: #FFFEFB;
    --ink: #1E2A22;
    --ink-soft: #5B6B5F;
    --primary: #0B3D2E;
    --primary-light: #1A5C43;
    --accent: #B08A2E;
    --line: #D9D2BE;
    --danger: #9C3B2E;
    --danger-bg: #F6E9E4;
  }
  *{ box-sizing: border-box; }
  html, body{
    margin:0; padding:0;
    background: var(--bg);
    color: var(--ink);
    font-family: 'Noto Sans Thai', sans-serif;
    -webkit-font-smoothing: antialiased;
  }
  body{
    display:flex;
    justify-content:center;
    padding: 28px 14px 60px;
  }
  .sheet{
    width:100%;
    max-width: 460px;
  }
  .masthead{
    padding: 6px 4px 22px;
    border-bottom: 2px solid var(--primary);
    margin-bottom: 22px;
    position:relative;
  }
  .masthead .kicker{
    font-family:'IBM Plex Mono', monospace;
    font-size: 12px;
    letter-spacing: 0.08em;
    color: var(--accent);
    margin-bottom: 6px;
  }
  .masthead h1{
    font-size: 26px;
    line-height:1.25;
    margin:0;
    color: var(--primary);
    font-weight:700;
  }
  .masthead p{
    margin: 8px 0 0;
    font-size: 13.5px;
    color: var(--ink-soft);
    line-height:1.6;
  }

  .panel{
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 4px;
    padding: 22px 20px 20px;
    margin-bottom: 18px;
  }

  .toggle-row{
    display:flex;
    flex-wrap: wrap;
    align-items:center;
    justify-content:space-between;
    gap: 8px;
    margin-bottom: 20px;
    padding-bottom: 18px;
    border-bottom: 1px dashed var(--line);
  }
  .toggle-row .label{
    font-size: 13px;
    color: var(--ink-soft);
    flex: 1 1 140px;
  }
  .toggle{
    display:flex;
    flex-wrap: wrap;
    background: var(--bg);
    border: 1px solid var(--line);
    border-radius: 100px;
    padding: 3px;
    gap: 2px;
  }
  .toggle button{
    border:none;
    background: transparent;
    font-family:'Noto Sans Thai', sans-serif;
    font-size: 12px;
    font-weight:600;
    padding: 7px 10px;
    border-radius: 100px;
    color: var(--ink-soft);
    cursor:pointer;
    transition: background 0.18s ease, color 0.18s ease;
    white-space: nowrap;
  }
  .toggle button.active{
    background: var(--primary);
    color: #fff;
  }

  .field{
    display:flex;
    align-items:flex-end;
    justify-content:space-between;
    gap: 12px;
    padding: 13px 0;
    border-bottom: 1px solid var(--line);
  }
  .field:last-child{ border-bottom:none; padding-bottom:2px; }
  .field .fmeta{
    flex: 0 0 auto;
  }
  .field .fmeta .abbr{
    font-family:'IBM Plex Mono', monospace;
    font-size: 13px;
    font-weight:600;
    color: var(--primary);
  }
  .field .fmeta .thname{
    font-size: 12px;
    color: var(--ink-soft);
    margin-top: 2px;
  }
  .field .finput{
    flex: 1 1 auto;
    display:flex;
    align-items:center;
    gap: 6px;
  }
  .field input{
    width: 100%;
    border: none;
    border-bottom: 1px solid transparent;
    background: transparent;
    text-align: right;
    font-family:'IBM Plex Mono', monospace;
    font-size: 16.5px;
    font-weight:600;
    color: var(--ink);
    padding: 4px 2px 6px;
    outline:none;
    min-width: 0;
  }
  .field input::placeholder{
    color: #B9C0B4;
    font-weight:500;
  }
  .field input:focus{
    border-bottom: 1px solid var(--primary);
  }
  .field .unit{
    font-size: 13px;
    color: var(--ink-soft);
    flex: 0 0 auto;
  }
  .field.solved .abbr{ color: var(--accent); }
  .field.solved input{ color: var(--accent); }

  .actions{
    display:flex;
    gap: 10px;
    margin-top: 20px;
  }
  .btn{
    flex:1;
    border:none;
    border-radius: 4px;
    padding: 13px 10px;
    font-family:'Noto Sans Thai', sans-serif;
    font-size: 14.5px;
    font-weight:700;
    cursor:pointer;
    transition: opacity 0.15s ease, transform 0.05s ease;
  }
  .btn:active{ transform: scale(0.98); }
  .btn-primary{ background: var(--primary); color:#fff; }
  .btn-primary:hover{ background: var(--primary-light); }
  .btn-ghost{ background: transparent; color: var(--ink-soft); border: 1px solid var(--line); }
  .btn-ghost:hover{ background: var(--bg); }

  .hint{
    font-size: 12px;
    color: var(--ink-soft);
    margin-top: 12px;
    line-height:1.6;
  }

  .message{
    display:none;
    background: var(--danger-bg);
    color: var(--danger);
    border: 1px solid #E5C6BC;
    border-radius: 4px;
    padding: 12px 14px;
    font-size: 13px;
    margin-bottom: 18px;
    line-height:1.6;
  }
  .message.show{ display:block; }

  .result{
    background: var(--primary);
    color: #fff;
    border-radius: 4px;
    padding: 22px 20px;
    display:none;
    opacity:0;
    transform: translateY(6px);
    transition: opacity 0.32s ease, transform 0.32s ease;
  }
  .result.show{ display:block; opacity:1; transform:translateY(0); }
  .result .rlabel{
    font-family:'IBM Plex Mono', monospace;
    font-size: 12px;
    letter-spacing: 0.06em;
    color: #CFE0D6;
    margin-bottom: 8px;
  }
  .result .rvalue{
    font-family:'IBM Plex Mono', monospace;
    font-size: 30px;
    font-weight:600;
    word-break: break-all;
  }
  .result .rsub{
    font-size: 12.5px;
    color: #CFE0D6;
    margin-top: 10px;
    line-height:1.6;
  }

  footer{
    text-align:center;
    font-size: 11.5px;
    color: var(--ink-soft);
    margin-top: 22px;
  }
</style>
</head>
<body>
<div class="sheet">

  <div class="masthead">
    <div class="kicker">TIME VALUE OF MONEY</div>
    <h1>เครื่องคำนวณมูลค่าเงินตามเวลา</h1>
    <p>กรอกข้อมูล 4 ใน 5 ช่อง แล้วเว้นว่างช่องที่ต้องการหาคำตอบไว้ 1 ช่อง จากนั้นกดคำนวณ</p>
  </div>

  <div class="panel">
    <div class="toggle-row">
      <div class="label">รูปแบบการจ่ายเงินงวด</div>
      <div class="toggle">
        <button id="btnOrdinary" class="active" onclick="setType(0)">จ่ายปลายงวด</button>
        <button id="btnDue" onclick="setType(1)">จ่ายต้นงวด</button>
      </div>
    </div>

    <div class="toggle-row">
      <div class="label">ความถี่ของงวด (N)</div>
      <div class="toggle">
        <button id="btnUnitMonth" class="active" onclick="setPeriodUnit('month')">รายเดือน</button>
        <button id="btnUnitQuarter" onclick="setPeriodUnit('quarter')">รายไตรมาส</button>
        <button id="btnUnitYear" onclick="setPeriodUnit('year')">รายปี</button>
      </div>
    </div>

    <div class="toggle-row" id="rateUnitRow">
      <div class="label">อัตราดอกเบี้ย (i) ที่กรอก/ต้องการหา</div>
      <div class="toggle">
        <button id="btnRatePeriod" class="active" onclick="setRateUnit('period')">ต่องวด</button>
        <button id="btnRateAnnual" onclick="setRateUnit('annual')">ต่อปี (Nominal)</button>
      </div>
    </div>

    <div class="field" id="row-PV">
      <div class="fmeta">
        <div class="abbr">PV</div>
        <div class="thname">มูลค่าปัจจุบัน</div>
      </div>
      <div class="finput">
        <span class="unit">฿</span>
        <input type="text" inputmode="decimal" id="in-PV" placeholder="0.00">
      </div>
    </div>

    <div class="field" id="row-FV">
      <div class="fmeta">
        <div class="abbr">FV</div>
        <div class="thname">มูลค่าอนาคต</div>
      </div>
      <div class="finput">
        <span class="unit">฿</span>
        <input type="text" inputmode="decimal" id="in-FV" placeholder="0.00">
      </div>
    </div>

    <div class="field" id="row-PMT">
      <div class="fmeta">
        <div class="abbr">PMT</div>
        <div class="thname">เงินงวด</div>
      </div>
      <div class="finput">
        <span class="unit">฿</span>
        <input type="text" inputmode="decimal" id="in-PMT" placeholder="0.00">
      </div>
    </div>

    <div class="field" id="row-i">
      <div class="fmeta">
        <div class="abbr">i</div>
        <div class="thname" id="i-label">อัตราดอกเบี้ยต่องวด (ต่อเดือน)</div>
      </div>
      <div class="finput">
        <input type="text" inputmode="decimal" id="in-i" placeholder="0.00">
        <span class="unit">%</span>
      </div>
    </div>

    <div class="field" id="row-N">
      <div class="fmeta">
        <div class="abbr">N</div>
        <div class="thname">จำนวนงวด</div>
      </div>
      <div class="finput">
        <input type="text" inputmode="decimal" id="in-N" placeholder="0">
        <span class="unit" id="n-unit">เดือน</span>
      </div>
    </div>

    <div class="actions">
      <button class="btn btn-ghost" onclick="clearAll()">ล้างข้อมูล</button>
      <button class="btn btn-primary" onclick="calculate()">คำนวณ</button>
    </div>

    <div class="hint">หมายเหตุ: ใส่เครื่องหมายลบหน้าตัวเลขสำหรับเงินที่จ่ายออก (เช่น เงินลงทุน) และปล่อยเป็นค่าบวกสำหรับเงินที่ได้รับ เพื่อให้สมการคำนวณถูกต้องตามหลักการเงิน · ถ้าเลือก "ต่อปี (Nominal)" ระบบจะแปลงเป็นอัตราต่องวดให้อัตโนมัติก่อนคำนวณ แล้วแปลงกลับเป็นรายปีตอนแสดงผล</div>
  </div>

  <div class="message" id="errorBox"></div>

  <div class="result" id="resultBox">
    <div class="rlabel" id="resultLabel">ผลลัพธ์</div>
    <div class="rvalue" id="resultValue">0.00</div>
    <div class="rsub" id="resultSub"></div>
  </div>

  <footer>คำนวณตามสมการมูลค่าเงินตามเวลามาตรฐาน (5 ตัวแปร)</footer>
</div>

<script>
let pmtType = 0; // 0 = ordinary (ปลายงวด), 1 = due (ต้นงวด)
let periodUnit = 'month'; // 'month' รายเดือน | 'quarter' รายไตรมาส | 'year' รายปี → กำหนดว่า 1 งวด เท่ากับอะไร
let rateUnit = 'period';  // 'period' = อัตราต่องวด (ตรงกับ periodUnit), 'annual' = อัตราต่อปี (nominal, แปลงหาร/คูณด้วยจำนวนงวดต่อปี)
const fields = ['PV','FV','PMT','i','N'];
const thNames = { PV:'มูลค่าปัจจุบัน (PV)', FV:'มูลค่าอนาคต (FV)', PMT:'เงินงวด (PMT)', i:'อัตราดอกเบี้ย (i)', N:'จำนวนงวด (N)' };
const unitTh = { month: 'เดือน', quarter: 'ไตรมาส', year: 'ปี' };

function periodsPerYear(){
  if (periodUnit === 'month') return 12;
  if (periodUnit === 'quarter') return 4;
  return 1;
}

function setType(t){
  pmtType = t;
  document.getElementById('btnOrdinary').classList.toggle('active', t===0);
  document.getElementById('btnDue').classList.toggle('active', t===1);
}

function setPeriodUnit(u){
  periodUnit = u;
  document.getElementById('btnUnitMonth').classList.toggle('active', u==='month');
  document.getElementById('btnUnitQuarter').classList.toggle('active', u==='quarter');
  document.getElementById('btnUnitYear').classList.toggle('active', u==='year');
  document.getElementById('n-unit').textContent = unitTh[u];

  const rateUnitRow = document.getElementById('rateUnitRow');
  if (u === 'year'){
    // 1 งวด = 1 ปีอยู่แล้ว จึงไม่มีความหมายที่จะเลือก "ต่อปี" แยกต่างหาก
    rateUnit = 'period';
    document.getElementById('btnRatePeriod').classList.add('active');
    document.getElementById('btnRateAnnual').classList.remove('active');
    rateUnitRow.style.opacity = '0.45';
    rateUnitRow.style.pointerEvents = 'none';
  } else {
    rateUnitRow.style.opacity = '1';
    rateUnitRow.style.pointerEvents = 'auto';
  }
  updateRateLabel();
}

function setRateUnit(u){
  if (periodUnit === 'year') return; // ไม่เปิดใช้งานเมื่อเลือกงวดเป็นรายปี
  rateUnit = u;
  document.getElementById('btnRatePeriod').classList.toggle('active', u==='period');
  document.getElementById('btnRateAnnual').classList.toggle('active', u==='annual');
  updateRateLabel();
}

function updateRateLabel(){
  const label = document.getElementById('i-label');
  if (rateUnit === 'annual'){
    label.textContent = 'อัตราดอกเบี้ยต่อปี (Nominal)';
  } else {
    label.textContent = 'อัตราดอกเบี้ยต่องวด (ต่อ' + unitTh[periodUnit] + ')';
  }
}

function showError(msg){
  const box = document.getElementById('errorBox');
  box.textContent = msg;
  box.classList.add('show');
  document.getElementById('resultBox').classList.remove('show');
}
function hideError(){
  document.getElementById('errorBox').classList.remove('show');
}
function clearSolvedHighlight(){
  fields.forEach(f => document.getElementById('row-'+f).classList.remove('solved'));
}

function clearAll(){
  fields.forEach(f => document.getElementById('in-'+f).value = '');
  hideError();
  document.getElementById('resultBox').classList.remove('show');
  clearSolvedHighlight();
}

function formatNumber(num, decimals){
  if (!isFinite(num)) return '—';
  const rounded = Number(num.toFixed(decimals));
  const parts = rounded.toFixed(decimals).split('.');
  parts[0] = parts[0].replace(/\B(?=(\d{3})+(?!\d))/g, ',');
  return parts.join('.');
}

function parseVal(id){
  const raw = document.getElementById('in-'+id).value.trim();
  if (raw === '') return null;
  const num = Number(raw.replace(/,/g,''));
  return isNaN(num) ? undefined : num;
}

// FVIFA(i, N) = ((1+i)^N - 1) / i, with i as decimal rate
function fvifa(i, N){
  if (Math.abs(i) < 1e-12) return N;
  return (Math.pow(1+i, N) - 1) / i;
}

function solveFV(PV, PMT, i, N, type){
  const x = Math.pow(1+i, N);
  return -(PV*x) - PMT*(1+i*type)*fvifa(i, N);
}
function solvePV(FV, PMT, i, N, type){
  const x = Math.pow(1+i, N);
  return ( -FV - PMT*(1+i*type)*fvifa(i, N) ) / x;
}
function solvePMT(PV, FV, i, N, type){
  const x = Math.pow(1+i, N);
  const denom = (1+i*type) * fvifa(i, N);
  if (Math.abs(denom) < 1e-12) throw new Error('ไม่สามารถหาค่า PMT ได้จากข้อมูลที่กรอก (อาจเป็นเพราะ i และ N เป็น 0 พร้อมกัน)');
  return ( -FV - PV*x ) / denom;
}
function solveN(PV, FV, PMT, i, type){
  if (Math.abs(i) < 1e-12){
    if (PMT === 0) throw new Error('ไม่สามารถหาค่า N ได้ เนื่องจากไม่มีดอกเบี้ยและไม่มีเงินงวด');
    return -(PV+FV)/PMT;
  }
  const k = PMT*(1+i*type)/i;
  const numerator = k - FV;
  const denominator = PV + k;
  if (Math.abs(denominator) < 1e-12) throw new Error('ไม่สามารถหาค่า N ได้จากข้อมูลที่กรอก');
  const ratio = numerator/denominator;
  if (ratio <= 0) throw new Error('ไม่พบคำตอบของ N ที่เป็นจริงจากข้อมูลที่กรอก โปรดตรวจสอบเครื่องหมายบวก/ลบของตัวเลข');
  const n = Math.log(ratio) / Math.log(1+i);
  if (n <= 0) throw new Error('ค่า N ที่คำนวณได้ไม่ถูกต้อง โปรดตรวจสอบข้อมูลที่กรอก');
  return n;
}
function solveI(PV, FV, PMT, N, type){
  function f(iVal){
    if (Math.abs(iVal) < 1e-12) return PV + PMT*N + FV;
    const x = Math.pow(1+iVal, N);
    return PV*x + PMT*(1+iVal*type)*fvifa(iVal, N) + FV;
  }
  const starts = [0.01, 0.05, 0.1, -0.05, 0.2, -0.2];
  for (let s = 0; s < starts.length; s++){
    let i0 = starts[s];
    let i1 = i0 + 0.01;
    let f0 = f(i0), f1 = f(i1);
    let converged = false;
    for (let iter = 0; iter < 200; iter++){
      if (Math.abs(f1-f0) < 1e-14) break;
      let i2 = i1 - f1*(i1-i0)/(f1-f0);
      if (!isFinite(i2) || i2 <= -1) break;
      i0 = i1; f0 = f1;
      i1 = i2; f1 = f(i1);
      if (Math.abs(f1) < 1e-8){ converged = true; break; }
    }
    if (converged && isFinite(i1) && i1 > -1){
      return i1;
    }
  }
  throw new Error('ไม่พบคำตอบของอัตราดอกเบี้ย (i) โปรดตรวจสอบเครื่องหมายบวก/ลบและค่าตัวแปรอื่น');
}

function calculate(){
  hideError();
  clearSolvedHighlight();

  const raw = {};
  let invalidField = null;
  fields.forEach(f => {
    const v = parseVal(f);
    if (v === undefined) invalidField = f;
    raw[f] = v;
  });

  if (invalidField){
    showError('ข้อมูลในช่อง ' + thNames[invalidField] + ' ไม่ใช่ตัวเลข กรุณาตรวจสอบอีกครั้ง');
    return;
  }

  const blanks = fields.filter(f => raw[f] === null);

  if (blanks.length === 0){
    showError('กรุณาเว้นว่างไว้ 1 ช่อง ซึ่งเป็นช่องที่ต้องการให้คำนวณหาคำตอบ');
    return;
  }
  if (blanks.length > 1){
    showError('กรุณากรอกข้อมูลให้ครบ 4 ใน 5 ช่อง (เว้นว่างได้เพียง 1 ช่องเท่านั้น)');
    return;
  }

  const target = blanks[0];
  const PV = raw.PV, FV = raw.FV, PMT = raw.PMT, N = raw.N;
  const ppy = periodsPerYear();

  // แปลงอัตราดอกเบี้ยที่กรอก (อาจเป็น "ต่อปี") ให้เป็นอัตราต่องวดก่อนนำไปคำนวณเสมอ
  let iDecimalPerPeriod = null;
  if (raw.i !== null){
    iDecimalPerPeriod = (rateUnit === 'annual') ? (raw.i/100) / ppy : raw.i/100;
  }

  try{
    let result;
    let resultDisplay;
    let subLines = [];

    if (target === 'FV'){
      result = solveFV(PV, PMT, iDecimalPerPeriod, N, pmtType);
      resultDisplay = '฿ ' + formatNumber(result, 2);
    } else if (target === 'PV'){
      result = solvePV(FV, PMT, iDecimalPerPeriod, N, pmtType);
      resultDisplay = '฿ ' + formatNumber(result, 2);
    } else if (target === 'PMT'){
      result = solvePMT(PV, FV, iDecimalPerPeriod, N, pmtType);
      resultDisplay = '฿ ' + formatNumber(result, 2);
    } else if (target === 'N'){
      result = solveN(PV, FV, PMT, iDecimalPerPeriod, pmtType);
      resultDisplay = formatNumber(result, 2) + ' ' + unitTh[periodUnit];
    } else if (target === 'i'){
      const iPerPeriod = solveI(PV, FV, PMT, N, pmtType);
      if (rateUnit === 'annual'){
        result = iPerPeriod * ppy * 100;
        resultDisplay = formatNumber(result, 4) + ' % ต่อปี (Nominal)';
      } else {
        result = iPerPeriod * 100;
        resultDisplay = formatNumber(result, 4) + ' % ต่องวด';
      }
      // แสดงรายละเอียดเพิ่ม: อัตราต่องวด และอัตราที่แท้จริงต่อปี (EAR) เมื่อคิดดอกเบี้ยมากกว่า 1 ครั้งต่อปี
      if (ppy > 1){
        subLines.push('เทียบเท่าอัตราต่อ' + unitTh[periodUnit] + ': ' + formatNumber(iPerPeriod*100, 4) + ' %');
        const ear = (Math.pow(1+iPerPeriod, ppy) - 1) * 100;
        subLines.push('อัตราดอกเบี้ยที่แท้จริงต่อปี (EAR): ' + formatNumber(ear, 4) + ' %');
      }
    }

    document.getElementById('in-'+target).value = formatNumber(result, target === 'i' ? 4 : 2);
    document.getElementById('row-'+target).classList.add('solved');

    document.getElementById('resultLabel').textContent = 'ผลลัพธ์ · ' + thNames[target];
    document.getElementById('resultValue').textContent = resultDisplay;

    const baseLine = 'รูปแบบการจ่ายเงินงวด: ' + (pmtType === 1 ? 'จ่ายต้นงวด' : 'จ่ายปลายงวด') +
      ' · ความถี่ของงวด: ราย' + unitTh[periodUnit];
    document.getElementById('resultSub').innerHTML = [baseLine].concat(subLines).join('<br>');
    document.getElementById('resultBox').classList.add('show');
  } catch(e){
    showError(e.message || 'ไม่สามารถคำนวณได้ กรุณาตรวจสอบข้อมูลที่กรอก');
  }
}
</script>
</body>
</html>

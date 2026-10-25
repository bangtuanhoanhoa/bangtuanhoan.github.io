# phamdinhbao2005.github.io
<!DOCTYPE html>
<html lang="vi"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Bảng tuần hoàn các nguyên tố hóa học</title>
<style>
:root{--bg:#f6f7f9;--fg:#15202b;--mut:#5d6b7a;--card:#fff;--line:#d5dbe2;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#10151b;--fg:#e8edf2;--mut:#9aa8b6;--card:#19212a;--line:#2d3844}}
:root[data-theme="dark"]{--bg:#10151b;--fg:#e8edf2;--mut:#9aa8b6;--card:#19212a;--line:#2d3844}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--fg);font-family:"Be Vietnam Pro","Segoe UI",system-ui,sans-serif;padding:16px}
h1{font-size:1.4rem;margin:0 0 4px}
p.sub{margin:0 0 12px;color:var(--mut);font-size:.9rem}
.legend{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:12px}
.chip{border:1px solid hsl(var(--h) 60% 50%/.7);background:hsl(var(--h) 70% 50%/.18);color:var(--fg);border-radius:999px;padding:4px 10px;font:inherit;font-size:.78rem;cursor:pointer}
.chip.on{background:hsl(var(--h) 70% 50%/.55);font-weight:600}
.gh{grid-row:1;grid-column:var(--c);border:1px solid var(--line);background:var(--card);color:var(--fg);border-radius:5px;font:inherit;padding:3px 1px;cursor:pointer;display:flex;flex-direction:column;align-items:center;line-height:1.25;min-width:0}
.gh b{font-size:.8rem}.gh i{font-size:.58rem;color:var(--mut);font-style:normal}.gh u{font-size:.58rem;text-decoration:none;text-align:center;line-height:1.2}
.gh.on{border-color:var(--fg);outline:2px solid var(--fg)}
.gi{display:none;border:1px solid hsl(var(--h) 60% 50%/.7);background:hsl(var(--h) 70% 50%/.15);border-radius:8px;padding:8px 12px;margin-bottom:12px;font-size:.88rem;line-height:1.5}
.wrap{overflow-x:auto;padding-bottom:6px}
.tbl{display:grid;grid-template-columns:repeat(18,minmax(56px,1fr));grid-template-rows:auto repeat(7,auto) 12px auto auto;gap:3px;min-width:1050px}
.el{grid-row:var(--r);grid-column:var(--c);aspect-ratio:1/1.08;border:1px solid hsl(var(--h) 60% 50%/.7);background:hsl(var(--h) 70% 50%/.2);color:var(--fg);border-radius:5px;padding:2px 3px;font:inherit;cursor:pointer;display:flex;flex-direction:column;align-items:center;justify-content:center;line-height:1.1;min-width:0}
.el:hover,.el:focus-visible{background:hsl(var(--h) 70% 50%/.5);outline:2px solid var(--fg);outline-offset:1px;z-index:1}
.el small{font-size:.58rem;color:var(--mut);align-self:flex-start}
.el b{font-size:1.05rem}
.el span{font-size:.5rem;max-width:100%;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.el.dim{opacity:.18}
.ph{grid-row:var(--r);grid-column:3;border:1px dashed hsl(var(--h) 60% 50%/.7);border-radius:5px;font-size:.6rem;display:flex;align-items:center;justify-content:center;color:var(--mut)}
#ov{position:fixed;inset:0;background:rgba(0,0,0,.55);display:none;align-items:center;justify-content:center;padding:12px;z-index:9}
#ov.show{display:flex}
.dlg{background:var(--card);border-radius:14px;max-width:580px;width:100%;max-height:92vh;overflow:auto;padding:18px;border:1px solid var(--line)}
.top{display:flex;gap:14px;align-items:center}
.big{width:104px;height:104px;flex:none;border-radius:10px;border:2px solid hsl(var(--h) 60% 50%);background:hsl(var(--h) 70% 50%/.25);display:flex;flex-direction:column;align-items:center;justify-content:center}
.big small{align-self:flex-start;margin:4px 0 0 8px;color:var(--mut)}
.big b{font-size:2.6rem;line-height:1}
.top h2{margin:0;font-size:1.6rem}
.top div p{margin:2px 0;color:var(--mut);font-size:.9rem}
.bohr{display:block;margin:12px auto;max-width:100%}
.info{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.info div{background:var(--bg);border-radius:8px;padding:8px 10px}
.info div.w{grid-column:1/-1}
.info dt{font-size:.72rem;color:var(--mut)}
.info dd{margin:2px 0 0;font-size:.95rem;font-weight:600}
.nav{display:flex;justify-content:space-between;gap:8px;margin-top:14px}
.nav button{font:inherit;padding:8px 14px;border-radius:8px;border:1px solid var(--line);background:var(--bg);color:var(--fg);cursor:pointer}
.nav button:hover{border-color:var(--fg)}
</style></head><body>
<h1>Bảng tuần hoàn các nguyên tố hóa học</h1>
<p class="sub">Bấm vào một ô để xem thông tin chi tiết. Bấm số nhóm (1–18) ở hàng trên cùng hoặc tên loại nguyên tố để xem cấu hình chung.</p>
<div class="legend" id="lg"></div>
<div class="gi" id="gi"></div>
<div class="wrap"><div class="tbl" id="t"></div></div>
<div id="ov" role="dialog" aria-modal="true"><div class="dlg" id="dl"></div></div>
<script>
const RAW="H,Hiđro,1.008,14,20,2.2;He,Heli,4.0026,,4,;Li,Liti,6.94,454,1615,0.98;Be,Beri,9.0122,1560,2742,1.57;B,Bo,10.81,2349,4200,2.04;C,Cacbon,12.011,3800,4300,2.55;N,Nitơ,14.007,63,77,3.04;O,Oxi,15.999,54,90,3.44;F,Flo,18.998,53,85,3.98;Ne,Neon,20.18,25,27,;Na,Natri,22.99,371,1156,0.93;Mg,Magie,24.305,923,1363,1.31;Al,Nhôm,26.982,933,2792,1.61;Si,Silic,28.085,1687,3538,1.9;P,Photpho,30.974,317,554,2.19;S,Lưu huỳnh,32.06,388,718,2.58;Cl,Clo,35.45,172,239,3.16;Ar,Argon,39.95,84,87,;K,Kali,39.098,337,1032,0.82;Ca,Canxi,40.078,1115,1757,1;Sc,Scandi,44.956,1814,3109,1.36;Ti,Titan,47.867,1941,3560,1.54;V,Vanadi,50.942,2183,3680,1.63;Cr,Crom,51.996,2180,2944,1.66;Mn,Mangan,54.938,1519,2334,1.55;Fe,Sắt,55.845,1811,3134,1.83;Co,Coban,58.933,1768,3200,1.88;Ni,Niken,58.693,1728,3186,1.91;Cu,Đồng,63.546,1358,2835,1.9;Zn,Kẽm,65.38,693,1180,1.65;Ga,Gali,69.723,303,2673,1.81;Ge,Germani,72.63,1211,3106,2.01;As,Asen,74.922,1090,887,2.18;Se,Selen,78.971,494,958,2.55;Br,Brom,79.904,266,332,2.96;Kr,Krypton,83.798,116,120,3;Rb,Rubidi,85.468,312,961,0.82;Sr,Stronti,87.62,1050,1655,0.95;Y,Ytri,88.906,1799,3609,1.22;Zr,Zirconi,91.224,2128,4682,1.33;Nb,Niobi,92.906,2750,5017,1.6;Mo,Molipden,95.95,2896,4912,2.16;Tc,Tecneti,98,2430,4538,1.9;Ru,Ruteni,101.07,2607,4423,2.2;Rh,Rodi,102.91,2237,3968,2.28;Pd,Paladi,106.42,1828,3236,2.2;Ag,Bạc,107.87,1235,2435,1.93;Cd,Cadmi,112.41,594,1040,1.69;In,Indi,114.82,430,2345,1.78;Sn,Thiếc,118.71,505,2875,1.96;Sb,Antimon,121.76,904,1860,2.05;Te,Telu,127.6,723,1261,2.1;I,Iot,126.9,387,457,2.66;Xe,Xenon,131.29,161,165,2.6;Cs,Xesi,132.91,301,944,0.79;Ba,Bari,137.33,1000,2170,0.89;La,Lantan,138.91,1193,3737,1.1;Ce,Xeri,140.12,1068,3716,1.12;Pr,Praseodim,140.91,1208,3793,1.13;Nd,Neodim,144.24,1297,3347,1.14;Pm,Prometi,145,1315,3273,;Sm,Samari,150.36,1345,2067,1.17;Eu,Europi,151.96,1099,1802,;Gd,Gadolini,157.25,1585,3546,1.2;Tb,Terbi,158.93,1629,3503,;Dy,Dysprosi,162.5,1680,2840,1.22;Ho,Honmi,164.93,1734,2993,1.23;Er,Erbi,167.26,1802,3141,1.24;Tm,Tuli,168.93,1818,2223,1.25;Yb,Ytecbi,173.05,1097,1469,;Lu,Luteti,174.97,1925,3675,1.27;Hf,Hafni,178.49,2506,4876,1.3;Ta,Tantan,180.95,3290,5731,1.5;W,Vonfram,183.84,3695,5828,2.36;Re,Reni,186.21,3459,5869,1.9;Os,Osmi,190.23,3306,5285,2.2;Ir,Iridi,192.22,2719,4701,2.2;Pt,Platin,195.08,2041,4098,2.28;Au,Vàng,196.97,1337,3129,2.54;Hg,Thủy ngân,200.59,234,630,2;Tl,Tali,204.38,577,1746,1.62;Pb,Chì,207.2,601,2022,2.33;Bi,Bismut,208.98,544,1837,2.02;Po,Poloni,209,527,1235,2;At,Astatin,210,575,610,2.2;Rn,Radon,222,202,211,;Fr,Franxi,223,300,950,0.7;Ra,Radi,226,973,2010,0.9;Ac,Actini,227,1323,3471,1.1;Th,Thori,232.04,2115,5061,1.3;Pa,Protactini,231.04,1841,4300,1.5;U,Urani,238.03,1405,4404,1.38;Np,Neptuni,237,910,4175,1.36;Pu,Plutoni,244,912,3505,1.28;Am,Americi,243,1449,2880,1.13;Cm,Curi,247,1613,3383,1.28;Bk,Berkeli,247,1259,,;Cf,Californi,251,1173,,;Es,Einsteini,252,1133,,;Fm,Fermi,257,1800,,;Md,Mendelevi,258,1100,,;No,Nobeli,259,1100,,;Lr,Lorenxi,266,1900,,;Rf,Rutherfordi,267,,,;Db,Dubni,268,,,;Sg,Seaborgi,269,,,;Bh,Bohri,270,,,;Hs,Hassi,277,,,;Mt,Meitneri,278,,,;Ds,Darmstadti,281,,,;Rg,Roentgeni,282,,,;Cn,Copernixi,285,,,;Nh,Nihoni,286,,,;Fl,Flerovi,289,,,;Mc,Moscovi,290,,,;Lv,Livermori,293,,,;Ts,Tennessin,294,,,;Og,Oganesson,294,,,";
const E=RAW.split(";").map((s,i)=>{const a=s.split(",");return{z:i+1,s:a[0],n:a[1],m:a[2],mp:a[3]?+a[3]:null,bp:a[4]?+a[4]:null,en:a[5]?+a[5]:null}});
const EN="Hydrogen,Helium,Lithium,Beryllium,Boron,Carbon,Nitrogen,Oxygen,Fluorine,Neon,Sodium,Magnesium,Aluminium,Silicon,Phosphorus,Sulfur,Chlorine,Argon,Potassium,Calcium,Scandium,Titanium,Vanadium,Chromium,Manganese,Iron,Cobalt,Nickel,Copper,Zinc,Gallium,Germanium,Arsenic,Selenium,Bromine,Krypton,Rubidium,Strontium,Yttrium,Zirconium,Niobium,Molybdenum,Technetium,Ruthenium,Rhodium,Palladium,Silver,Cadmium,Indium,Tin,Antimony,Tellurium,Iodine,Xenon,Caesium,Barium,Lanthanum,Cerium,Praseodymium,Neodymium,Promethium,Samarium,Europium,Gadolinium,Terbium,Dysprosium,Holmium,Erbium,Thulium,Ytterbium,Lutetium,Hafnium,Tantalum,Tungsten,Rhenium,Osmium,Iridium,Platinum,Gold,Mercury,Thallium,Lead,Bismuth,Polonium,Astatine,Radon,Francium,Radium,Actinium,Thorium,Protactinium,Uranium,Neptunium,Plutonium,Americium,Curium,Berkelium,Californium,Einsteinium,Fermium,Mendelevium,Nobelium,Lawrencium,Rutherfordium,Dubnium,Seaborgium,Bohrium,Hassium,Meitnerium,Darmstadtium,Roentgenium,Copernicium,Nihonium,Flerovium,Moscovium,Livermorium,Tennessine,Oganesson".split(",");
E.forEach((e,i)=>{e.v=e.n;e.n=EN[i]});
const CATS={alk:["Kim loại kiềm",0],ale:["Kim loại kiềm thổ",28],lan:["Lantanit",52],act:["Actinit",345],tra:["Kim loại chuyển tiếp",215],pst:["Kim loại yếu",180],mtl:["Á kim",95],non:["Phi kim",140],hal:["Halogen",265],nob:["Khí hiếm",295]};
const GEN={alk:["ns¹","Nhóm IA (nhóm 1, trừ H): 1 electron ở phân lớp s ngoài cùng, dễ nhường 1 electron tạo ion M⁺."],ale:["ns²","Nhóm IIA (nhóm 2): 2 electron ở phân lớp s ngoài cùng, dễ nhường 2 electron tạo ion M²⁺."],tra:["(n−1)d¹⁻¹⁰ ns¹⁻²","Nguyên tố d (nhóm B): electron cuối cùng điền vào phân lớp d bên trong, có nhiều số oxi hóa. Một số ngoại lệ như Cr (3d⁵4s¹), Cu (3d¹⁰4s¹)."],pst:["ns² np¹⁻⁴","Electron ngoài cùng ở phân lớp np (Al, Ga, In, Tl: np¹; Sn, Pb: np²; Bi: np³; Po: np⁴). Từ chu kỳ 4 trở đi có thêm (n−1)d¹⁰ đã bão hòa."],mtl:["ns² np¹⁻⁴","B: 2s²2p¹; Si, Ge: np²; As, Sb: np³; Te: np⁴. Tính chất trung gian giữa kim loại và phi kim."],non:["ns² np²⁻⁵ (H: 1s¹)","Gồm H, C, N, O, P, S, Se. Có xu hướng nhận hoặc góp chung electron để đạt cấu hình bền."],hal:["ns² np⁵","Nhóm VIIA (nhóm 17): 7 electron ngoài cùng, dễ nhận 1 electron tạo ion X⁻."],nob:["ns² np⁶ (He: 1s²)","Nhóm VIIIA (nhóm 18): lớp ngoài cùng bão hòa 8 electron (He: 2 electron), rất trơ về mặt hóa học."],lan:["4f¹⁻¹⁴ 5d⁰⁻¹ 6s²","Nguyên tố f chu kỳ 6: electron cuối cùng điền vào phân lớp 4f, lớp ngoài cùng thường là 6s²."],act:["5f¹⁻¹⁴ 6d⁰⁻² 7s²","Nguyên tố f chu kỳ 7: electron cuối cùng điền vào phân lớp 5f, lớp ngoài cùng thường là 7s². Đều là nguyên tố phóng xạ."]};
function gi(k){const el=document.getElementById("gi");el.style.display=k?"block":"none";if(!k)return;el.style.setProperty("--h",CATS[k][1]);el.innerHTML=`<b>${CATS[k][0]}</b> – cấu hình electron lớp ngoài cùng chung: <b>${GEN[k][0]}</b><br>${GEN[k][1]}`}
const L=(a)=>a.reduce((o,k)=>(o[k]=1,o),{});
const sets={nob:L([2,10,18,36,54,86,118]),alk:L([3,11,19,37,55,87]),ale:L([4,12,20,38,56,88]),mtl:L([5,14,32,33,51,52]),non:L([1,6,7,8,15,16,34]),hal:L([9,17,35,53,85,117]),pst:L([13,31,49,50,81,82,83,84,113,114,115,116])};
function cat(z){for(const k in sets)if(sets[k][z])return k;if(z>=57&&z<=71)return"lan";if(z>=89&&z<=103)return"act";return"tra"}
function pos(z){
 if(z<=2)return[1,z==1?1:18];if(z<=10)return[2,z<=4?z-2:z+8];if(z<=18)return[3,z<=12?z-10:z];
 if(z<=36)return[4,z-18];if(z<=54)return[5,z-36];
 if(z<=56)return[6,z-54];if(z<=71)return[9,z-54];if(z<=86)return[6,z-68];
 if(z<=88)return[7,z-86];if(z<=103)return[10,z-86];return[7,z-100]}
const ORD=[["1s",2],["2s",2],["2p",6],["3s",2],["3p",6],["4s",2],["3d",10],["4p",6],["5s",2],["4d",10],["5p",6],["6s",2],["4f",14],["5d",10],["6p",6],["7s",2],["5f",14],["6d",10],["7p",6]];
const EX={24:{"4s":1,"3d":5},29:{"4s":1,"3d":10},41:{"5s":1,"4d":4},42:{"5s":1,"4d":5},44:{"5s":1,"4d":7},45:{"5s":1,"4d":8},46:{"5s":0,"4d":10},47:{"5s":1,"4d":10},57:{"4f":0,"5d":1},58:{"4f":1,"5d":1},64:{"4f":7,"5d":1},78:{"6s":1,"5d":9},79:{"6s":1,"5d":10},89:{"5f":0,"6d":1},90:{"5f":0,"6d":2},91:{"5f":2,"6d":1},92:{"5f":3,"6d":1},93:{"5f":4,"6d":1},96:{"5f":7,"6d":1},103:{"6d":0,"7p":1}};
function cfg(z){let r=z;const c=ORD.map(([k,m])=>{const e=Math.min(m,r);r-=e;return[k,e]});
 const ex=EX[z];if(ex)c.forEach(x=>{if(ex[x[0]]!==undefined)x[1]=ex[x[0]]});return c.filter(x=>x[1]>0)}
const SUP="⁰¹²³⁴⁵⁶⁷⁸⁹";const sup=n=>String(n).split("").map(d=>SUP[d]).join("");
const fmt=c=>c.map(x=>x[0]+sup(x[1])).join(" ");
const CORE=[[86,14,"Rn"],[54,10,"Xe"],[36,7,"Kr"],[18,4,"Ar"],[10,2,"Ne"],[2,0,"He"]];
function short(z){const k=CORE.find(c=>c[0]<z);if(!k)return fmt(cfg(z));const full=cfg(z),done=ORD.slice(0,k[1]+1).map(x=>x[0]);return"["+k[2]+"] "+fmt(full.filter(x=>!done.includes(x[0])))}
function shells(z){const s=[];cfg(z).forEach(([k,e])=>{const n=+k[0];s[n-1]=(s[n-1]||0)+e});return s.map(x=>x||0)}
function block(z,c){return c=="lan"||c=="act"?"f":c=="tra"?"d":(c=="alk"||c=="ale"||z<=2)?"s":"p"}
function state(e){if(e.mp!=null&&e.mp>298)return"Rắn";if(e.bp!=null)return e.bp>298?"Lỏng":"Khí";return e.mp!=null?"Rắn":"Chưa rõ"}
const T=document.getElementById("t"),LG=document.getElementById("lg");let filt=null,cur=0;
E.forEach(e=>{const k=cat(e.z),[r,c]=pos(e.z),b=document.createElement("button");b.className="el";b.dataset.k=k;
 b.dataset.g=r<=7?c:0;b.style.cssText=`--r:${r+1};--c:${c};--h:${CATS[k][1]}`;
 b.innerHTML=`<small>${e.z}</small><b>${e.s}</b><span>${e.n}</span>`;b.setAttribute("aria-label",e.n);b.title=e.n;b.onclick=()=>open(e.z);T.appendChild(b)});
[[7,"57–71","lan"],[8,"89–103","act"]].forEach(([r,t,k])=>{const d=document.createElement("div");d.className="ph";d.style.cssText=`--r:${r};--h:${CATS[k][1]}`;d.textContent=t;T.appendChild(d)});
Object.keys(CATS).forEach(k=>{const b=document.createElement("button");b.className="chip";b.style.setProperty("--h",CATS[k][1]);b.textContent=CATS[k][0];
 b.onclick=()=>{filt=filt==k?null:k;gi(filt);fg=0;document.querySelectorAll(".gh").forEach(x=>x.classList.remove("on"));document.querySelectorAll(".chip").forEach(x=>x.classList.toggle("on",x==b&&filt));document.querySelectorAll(".el").forEach(x=>x.classList.toggle("dim",!!filt&&x.dataset.k!=filt))};LG.appendChild(b)});
const GRP=["IA|Kim loại kiềm|ns¹|ns¹|H là phi kim nhưng cũng có cấu hình 1s¹","IIA|Kim loại kiềm thổ|ns²|ns²|Be, Mg, Ca, Sr, Ba, Ra","IIIB|Nhóm scandi|(n−1)d¹ ns²|d¹s²|Sc, Y và La/Ac hoặc Lu/Lr tùy cách xếp","IVB|Nhóm titan|(n−1)d² ns²|d²s²|Ti, Zr, Hf, Rf","VB|Nhóm vanadi|(n−1)d³ ns²|d³s²|V, Nb, Ta, Db; Nb ngoại lệ 4d⁴ 5s¹","VIB|Nhóm crom|(n−1)d⁴ ns²|d⁴s²|Cr, Mo, W, Sg; Cr và Mo ngoại lệ (n−1)d⁵ ns¹ (bán bão hòa)","VIIB|Nhóm mangan|(n−1)d⁵ ns²|d⁵s²|Mn, Tc, Re, Bh","VIIIB|Nhóm sắt|(n−1)d⁶ ns²|d⁶s²|Fe, Ru, Os, Hs; Ru ngoại lệ 4d⁷ 5s¹","VIIIB|Nhóm coban|(n−1)d⁷ ns²|d⁷s²|Co, Rh, Ir, Mt; Rh ngoại lệ 4d⁸ 5s¹","VIIIB|Nhóm niken|(n−1)d⁸ ns²|d⁸s²|Ni, Pd, Pt, Ds; Pd ngoại lệ 4d¹⁰, Pt ngoại lệ 5d⁹ 6s¹","IB|Nhóm đồng|(n−1)d¹⁰ ns¹|d¹⁰s¹|Cu, Ag, Au, Rg (phân lớp d bão hòa)","IIB|Nhóm kẽm|(n−1)d¹⁰ ns²|d¹⁰s²|Zn, Cd, Hg, Cn","IIIA|Nhóm bo|ns² np¹|np¹|B, Al, Ga, In, Tl, Nh","IVA|Nhóm cacbon|ns² np²|np²|C, Si, Ge, Sn, Pb, Fl","VA|Nhóm nitơ|ns² np³|np³|N, P, As, Sb, Bi, Mc","VIA|Nhóm oxi (chalcogen)|ns² np⁴|np⁴|O, S, Se, Te, Po, Lv","VIIA|Halogen|ns² np⁵|np⁵|F, Cl, Br, I, At, Ts; dễ nhận 1 electron tạo ion X⁻","VIIIA|Khí hiếm|ns² np⁶|np⁶|He là ngoại lệ (1s²); lớp ngoài cùng bão hòa nên rất trơ"].map(s=>s.split("|"));
let fg=0;
GRP.forEach((a,i)=>{const g=i+1,b=document.createElement("button");b.className="gh";b.style.setProperty("--c",g);b.title="Nhóm "+g+" – "+a[1];b.innerHTML=`<b>${g}</b><i>${a[0]}</i><u>${a[2].replace(" ","<br>")}</u>`;b.onclick=()=>showGroup(g);T.appendChild(b)});
function showGroup(g){fg=fg==g?0:g;filt=null;document.querySelectorAll(".chip").forEach(x=>x.classList.remove("on"));document.querySelectorAll(".gh").forEach((x,i)=>x.classList.toggle("on",fg==i+1));document.querySelectorAll(".el").forEach(x=>x.classList.toggle("dim",!!fg&&+x.dataset.g!=fg));const el=document.getElementById("gi");el.style.display=fg?"block":"none";if(!fg)return;const a=GRP[fg-1];el.style.setProperty("--h",200);el.innerHTML=`<b>Nhóm ${fg} (${a[0]}) – ${a[1]}</b> – cấu hình lớp ngoài cùng chung: <b>${a[2]}</b><br>${a[4]}`}
function bohr(z){const sh=shells(z),W=24+sh.length*28;let s=`<svg class="bohr" width="${W*2}" height="${W*2}" viewBox="${-W} ${-W} ${W*2} ${W*2}" role="img" aria-label="Mô hình lớp electron"><circle r="9" fill="hsl(${CATS[cat(z)][1]} 70% 50%)"/>`;
 sh.forEach((n,i)=>{const R=22+i*14*1;const rr=R+i*0;s+=`<circle r="${rr}" fill="none" stroke="currentColor" stroke-opacity=".25"/>`;for(let j=0;j<n;j++){const a=2*Math.PI*j/n-Math.PI/2;s+=`<circle cx="${(rr*Math.cos(a)).toFixed(1)}" cy="${(rr*Math.sin(a)).toFixed(1)}" r="2.8" fill="currentColor"/>`}});
 return s+"</svg>"}
function open(z){cur=z;const e=E[z-1],k=cat(z),[r,c]=pos(z),rad=(z>=84&&z!=92&&z!=90&&z!=91)||z==43||z==61;
 const K=v=>v==null?"—":v+" K ("+Math.round(v-273.15)+" °C)";
 const row=(t,v,w)=>`<div${w?' class="w"':""}><dt>${t}</dt><dd>${v}</dd></div>`;
 document.getElementById("dl").innerHTML=`<div class="top" style="--h:${CATS[k][1]}"><div class="big"><small>${z}</small><b>${e.s}</b></div><div><h2>${e.n}</h2><p>${CATS[k][0]}</p><p>Khối ${block(z,k)} · Chu kỳ ${r<=7?r:r-3} · Nhóm ${r<=7?c:"—"}</p></div></div>
 ${bohr(z)}<dl class="info" style="margin:0">
 ${row("Số hiệu nguyên tử (Z)",z)}${row("Khối lượng nguyên tử",rad?"["+e.m+"] u":e.m+" u")}
 ${row("Trạng thái (25 °C)",state(e))}${row("Độ âm điện (Pauling)",e.en??"—")}
 ${row("Nhiệt độ nóng chảy",K(e.mp))}${row("Nhiệt độ sôi",K(e.bp))}
 ${row("Số electron mỗi lớp",shells(z).join(", "))}${row("Tên tiếng Việt",e.v)}
 ${row("Cấu hình electron rút gọn",short(z),1)}${row("Cấu hình electron đầy đủ",fmt(cfg(z)),1)}${r<=7?row("Nhóm "+c+" ("+GRP[c-1][0]+") – "+GRP[c-1][1],"Cấu hình chung: "+GRP[c-1][2]+'<br><span style="font-weight:400;font-size:.8rem;color:var(--mut)">'+GRP[c-1][4]+'</span>',1):""}${row("Cấu hình chung theo loại ("+CATS[k][0]+")",GEN[k][0]+'<br><span style="font-weight:400;font-size:.8rem;color:var(--mut)">'+GEN[k][1]+'</span>',1)}</dl>
 ${rad?'<p style="font-size:.78rem;color:var(--mut);margin:10px 0 0">Nguyên tố phóng xạ: khối lượng ghi theo số khối của đồng vị bền nhất.</p>':""}
 <div class="nav"><button onclick="open(cur>1?cur-1:118)">‹ Trước</button><button onclick="close_()">Đóng</button><button onclick="open(cur<118?cur+1:1)">Sau ›</button></div>`;
 document.getElementById("ov").classList.add("show")}
function close_(){document.getElementById("ov").classList.remove("show")}
document.getElementById("ov").onclick=e=>{if(e.target.id=="ov")close_()};
document.addEventListener("keydown",e=>{if(!document.getElementById("ov").classList.contains("show"))return;
 if(e.key=="Escape")close_();if(e.key=="ArrowLeft")open(cur>1?cur-1:118);if(e.key=="ArrowRight")open(cur<118?cur+1:1)});
</script></body></html>

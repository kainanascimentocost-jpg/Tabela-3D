<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elementa 3D — Tabela Periódica</title>
<style>
*{box-sizing:border-box;margin:0;padding:0;}
:root{
    --bg:#060a12;--panel:#0d1422;--panel2:#111b2d;
    --text:#f5f7ff;--muted:#8490a5;--border:rgba(255,255,255,.09);
    --blue:#55a7ff;--purple:#9b72ff;
}
body{
    background:radial-gradient(circle at 15% 0%,rgba(54,130,255,.15),transparent 30%),radial-gradient(circle at 90% 20%,rgba(139,71,255,.12),transparent 30%),var(--bg);
    color:var(--text);font-family:Arial,Helvetica,sans-serif;min-height:100vh;
}
header{
    height:75px;padding:0 5%;display:flex;align-items:center;justify-content:space-between;
    border-bottom:1px solid var(--border);background:rgba(5,9,17,.75);backdrop-filter:blur(15px);position:sticky;top:0;z-index:100;
}
.logo{display:flex;align-items:center;gap:12px;}
.logo-icon{width:42px;height:42px;border:1px solid var(--blue);border-radius:11px;display:flex;align-items:center;justify-content:center;font-size:22px;font-weight:bold;color:var(--blue);box-shadow:0 0 25px rgba(85,167,255,.2);}
.logo-text strong{display:block;letter-spacing:3px;font-size:15px;}
.logo-text span{color:var(--muted);font-size:8px;letter-spacing:2px;}
.controls{width:92%;max-width:1450px;margin:20px auto;display:flex;gap:12px;}
.search{flex:1;height:52px;background:var(--panel);border:1px solid var(--border);border-radius:14px;display:flex;align-items:center;padding:0 16px;gap:10px;}
.search input{width:100%;background:none;border:0;outline:0;color:white;font-size:14px;}
select{width:230px;border:1px solid var(--border);background:var(--panel);color:white;border-radius:14px;padding:0 15px;outline:0;}
.table-wrapper{width:92%;max-width:1450px;margin:auto;overflow-x:auto;padding-bottom:20px;}
.periodic-table{min-width:1050px;display:grid;grid-template-columns:repeat(18,1fr);grid-auto-rows:78px;gap:5px;}
.element{background:var(--panel);border:1px solid var(--border);border-radius:9px;padding:7px;cursor:pointer;transition:.2s;position:relative;overflow:hidden;}
.element:hover{transform:translateY(-5px) scale(1.04);border-color:var(--blue);background:var(--panel2);box-shadow:0 15px 30px rgba(0,0,0,.4);z-index:5;}
.number{font-size:8px;color:var(--muted);}
.symbol{font-size:24px;font-weight:bold;margin-top:2px;}
.name{font-size:7px;color:var(--muted);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.mass{position:absolute;right:6px;bottom:5px;color:var(--muted);font-size:7px;}
.element[data-cat="nao-metal"] .symbol{color:#55b8ff}
.element[data-cat="metal-alcalino"] .symbol{color:#ff6f91}
.element[data-cat="alcalino-terroso"] .symbol{color:#ffad5c}
.element[data-cat="transicao"] .symbol{color:#9b72ff}
.element[data-cat="pos-transicao"] .symbol{color:#9aa7b8}
.element[data-cat="metaloide"] .symbol{color:#54d4a0}
.element[data-cat="halogenio"] .symbol{color:#e4c85d}
.element[data-cat="gas-nobre"] .symbol{color:#d478ff}
.element[data-cat="lantanideo"] .symbol{color:#52c8dc}
.element[data-cat="actinideo"] .symbol{color:#e57bca}
.fblock{width:90%;max-width:1300px;margin:25px auto;}
.f-title{color:var(--muted);font-size:10px;margin:12px 0 6px;}
.f-row{display:grid;grid-template-columns:repeat(15,1fr);gap:5px;}
.modal{display:none;position:fixed;inset:0;z-index:200;background:rgba(0,0,0,.75);backdrop-filter:blur(15px);align-items:center;justify-content:center;padding:20px;}
.modal.show{display:flex;}
.modal-box{width:min(1100px,100%);max-height:94vh;overflow:auto;background:#0b1321;border:1px solid var(--border);border-radius:24px;padding:30px;position:relative;}
.close{position:absolute;right:18px;top:15px;width:38px;height:38px;border-radius:50%;border:1px solid var(--border);background:var(--panel);color:white;font-size:25px;cursor:pointer;}
.element-header{display:flex;align-items:center;gap:20px;}
.big-symbol{font-size:75px;font-weight:bold;color:var(--blue);}
.modal-grid{display:grid;grid-template-columns:1.3fr 1fr;gap:20px;margin-top:25px;}
.atom{height:470px;background:radial-gradient(circle,rgba(65,130,255,.12),transparent 55%),#040811;border-radius:18px;overflow:hidden;position:relative;}
#canvas{width:100%;height:100%;}
.properties{background:var(--panel);border:1px solid var(--border);border-radius:18px;padding:22px;}
.property{display:flex;justify-content:space-between;border-bottom:1px solid var(--border);padding:11px 0;font-size:12px;}
.property span{color:var(--muted);}
.config{margin-top:18px;padding:15px;background:rgba(85,167,255,.07);border:1px solid rgba(85,167,255,.12);border-radius:12px;}
@media(max-width:850px){.modal-grid{grid-template-columns:1fr;}.controls{flex-direction:column;}.atom{height:350px;}}
</style>
</head>
<body>

<header>
    <div class="logo">
        <div class="logo-icon">E</div>
        <div class="logo-text">
            <strong>ELEMENTA</strong>
            <span>TABELA PERIÓDICA 3D</span>
        </div>
    </div>
</header>

<div class="controls">
    <div class="search">
        <input id="search" type="text" placeholder="Pesquisar elemento, símbolo ou número..." oninput="filterElements()">
    </div>
    <select id="category" onchange="filterElements()">
        <option value="all">Todas as categorias</option>
        <option value="nao-metal">Não metais</option>
        <option value="metal-alcalino">Metais alcalinos</option>
        <option value="alcalino-terroso">Alcalino-terrosos</option>
        <option value="transicao">Metais de transição</option>
        <option value="pos-transicao">Pós-transição</option>
        <option value="metaloide">Metaloides</option>
        <option value="halogenio">Halogênios</option>
        <option value="gas-nobre">Gases nobres</option>
    </select>
</div>

<div class="table-wrapper">
    <div id="table" class="periodic-table"></div>
</div>

<div class="fblock">
    <div class="f-title">LANTANÍDEOS</div>
    <div id="lanthanides" class="f-row"></div>
    <div class="f-title">ACTINÍDEOS</div>
    <div id="actinides" class="f-row"></div>
</div>

<div id="elementModal" class="modal">
    <div class="modal-box">
        <button class="close" onclick="closeElement()">×</button>
        <div class="element-header">
            <div>
                <div id="bigNumber" style="color:#8490a5">1</div>
                <div id="bigSymbol" class="big-symbol">H</div>
            </div>
            <div>
                <h2 id="bigName">Hidrogênio</h2>
                <p id="bigCategory" style="color:var(--muted)">Não metal</p>
            </div>
        </div>
        <div class="modal-grid">
            <div class="atom">
                <canvas id="canvas"></canvas>
            </div>
            <div class="properties">
                <h3>Propriedades</h3>
                <div class="property"><span>Número atômico</span><strong id="pNumber">1</strong></div>
                <div class="property"><span>Massa atômica</span><strong id="pMass">1.008</strong></div>
                <div class="property"><span>Prótons</span><strong id="pProtons">1</strong></div>
                <div class="property"><span>Elétrons</span><strong id="pElectrons">1</strong></div>
                <div class="property"><span>Nêutrons aproximados</span><strong id="pNeutrons">0</strong></div>
                <div class="config">
                    <span style="font-size:10px;color:var(--muted);display:block;margin-bottom:5px;">CONFIGURAÇÃO ELETRÔNICA</span>
                    <strong id="pConfig">1s¹</strong>
                </div>
            </div>
        </div>
    </div>
</div>

<script type="module">
import * as THREE from "https://cdn.jsdelivr.net/npm/three@0.185.0/build/three.module.js";
import { OrbitControls } from "https://cdn.jsdelivr.net/npm/three@0.185.0/examples/jsm/controls/OrbitControls.js";

const names = ["Hidrogênio","Hélio","Lítio","Berílio","Boro","Carbono","Nitrogênio","Oxigênio","Flúor","Neônio","Sódio","Magnésio","Alumínio","Silício","Fósforo","Enxofre","Cloro","Argônio","Potássio","Cálcio","Escândio","Titânio","Vanádio","Cromo","Manganês","Ferro","Cobalto","Níquel","Cobre","Zinco","Gálio","Germânio","Arsênio","Selênio","Bromo","Criptônio","Rubídio","Estrôncio","Ítrio","Zircônio","Nióbio","Molibdênio","Tecnécio","Rutênio","Ródio","Paládio","Prata","Cádmio","Índio","Estanho","Antimônio","Telúrio","Iodo","Xenônio","Césio","Bário","Lantânio","Cério","Praseodímio","Neodímio","Promécio","Samário","Európio","Gadolínio","Térbio","Disprósio","Hólmio","Érbio","Túlio","Itérbio","Lutécio","Háfnio","Tântalo","Tungstênio","Rênio","Ósmio","Irídio","Platina","Ouro","Mercúrio","Tálio","Chumbo","Bismuto","Polônio","Astato","Radônio","Frâncio","Rádio","Actínio","Tório","Protactínio","Urânio","Neptúnio","Plutônio","Amerício","Cúrio","Berquélio","Califórnio","Einstênio","Férmio","Mendelévio","Nobélio","Laurêncio","Rutherfórdio","Dúbnio","Seabórgio","Bóhrio","Hássio","Meitnério","Darmstádio","Roentgênio","Copernício","Nihônio","Fleróvio","Moscóvio","Livermório","Tenessino","Oganessônio"];
const symbols = ["H","He","Li","Be","B","C","N","O","F","Ne","Na","Mg","Al","Si","P","S","Cl","Ar","K","Ca","Sc","Ti","V","Cr","Mn","Fe","Co","Ni","Cu","Zn","Ga","Ge","As","Se","Br","Kr","Rb","Sr","Y","Zr","Nb","Mo","Tc","Ru","Rh","Pd","Ag","Cd","In","Sn","Sb","Te","I","Xe","Cs","Ba","La","Ce","Pr","Nd","Pm","Sm","Eu","Gd","Tb","Dy","Ho","Er","Tm","Yb","Lu","Hf","Ta","W","Re","Os","Ir","Pt","Au","Hg","Tl","Pb","Bi","Po","At","Rn","Fr","Ra","Ac","Th","Pa","U","Np","Pu","Am","Cm","Bk","Cf","Es","Fm","Md","No","Lr","Rf","Db","Sg","Bh","Hs","Mt","Ds","Rg","Cn","Nh","Fl","Mc","Lv","Ts","Og"];
const masses = [1.008,4.003,6.94,9.012,10.81,12.011,14.007,15.999,18.998,20.180,22.990,24.305,26.982,28.085,30.974,32.06,35.45,39.948,39.098,40.078,44.956,47.867,50.942,51.996,54.938,55.845,58.933,58.693,63.546,65.38,69.723,72.630,74.922,78.971,79.904,83.798,85.468,87.62,88.906,91.224,92.906,95.95,98,101.07,102.906,106.42,107.868,112.414,114.818,118.710,121.760,127.60,126.904,131.293,132.905,137.327,138.905,140.116,140.908,144.242,145,150.36,151.964,157.25,158.925,162.500,164.930,167.259,168.934,173.045,174.967,178.49,180.948,183.84,186.207,190.23,192.217,195.084,196.967,200.592,204.38,207.2,208.980,209,210,222,223,226,227,232.038,231.036,238.029,237,244,243,247,247,251,252,257,258,259,266,267,268,269,270,277,278,281,282,285,286,289,290,293,294,294];

const grid = [
    [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2],
    [3,4,0,0,0,0,0,0,0,0,0,0,5,6,7,8,9,10],
    [11,12,0,0,0,0,0,0,0,0,0,0,13,14,15,16,17,18],
    [19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36],
    [37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54],
    [55,56,0,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86],
    [87,88,0,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118]
];

function getCategory(num) {
    if (num >= 57 && num <= 71) return "lantanideo";
    if (num >= 89 && num <= 103) return "actinideo";
    if ([1, 6, 7, 8].includes(num)) return "nao-metal";
    if ([2, 10, 18, 36, 54, 86, 118].includes(num)) return "gas-nobre";
    if ([3, 11, 19, 37, 55, 87].includes(num)) return "metal-alcalino";
    if ([4, 12, 20, 38, 56, 88].includes(num)) return "alcalino-terroso";
    if ([5, 14, 32, 33, 51, 52].includes(num)) return "metaloide";
    if ([9, 17, 35, 53, 85, 117].includes(num)) return "halogenio";
    if ([13, 31, 49, 50, 81, 82, 83, 113, 114, 115, 116].includes(num)) return "pos-transicao";
    return "transicao";
}

function getElectronConfiguration(z) {
    const subshells = [{name:"1s",max:2},{name:"2s",max:2},{name:"2p",max:6},{name:"3s",max:2},{name:"3p",max:6},{name:"4s",max:2},{name:"3d",max:10},{name:"4p",max:6},{name:"5s",max:2},{name:"4d",max:10},{name:"5p",max:6},{name:"6s",max:2},{name:"4f",max:14},{name:"5d",max:10},{name:"6p",max:6},{name:"7s",max:2},{name:"5f",max:14},{name:"6d",max:10},{name:"7p",max:6}];
    const superscripts = {'0':'⁰','1':'¹','2':'²','3':'³','4':'⁴','5':'⁵','6':'⁶','7':'⁷','8':'⁸','9':'⁹','10':'¹⁰','11':'¹¹','12':'¹²','13':'¹³','14':'¹⁴'};
    let remaining = z, config = [];
    for (const sub of subshells) {
        if (remaining <= 0) break;
        const count = Math.min(remaining, sub.max);
        remaining -= count;
        config.push(`${sub.name}${superscripts[count] || count}`);
    }
    return config.join(" ");
}

function createElementCard(num) {
    if (num === 0) return document.createElement("div");
    const div = document.createElement("div");
    const cat = getCategory(num);
    div.className = "element";
    div.setAttribute("data-cat", cat);
    div.setAttribute("data-num", num);
    div.innerHTML = `<div class="number">${num}</div><div class="symbol">${symbols[num - 1]}</div><div class="name">${names[num - 1]}</div><div class="mass">${masses[num - 1]}</div>`;
    div.onclick = () => openElement(num);
    return div;
}

function renderTable() {
    const tableEl = document.getElementById("table");
    tableEl.innerHTML = "";
    grid.forEach(row => row.forEach(num => tableEl.appendChild(createElementCard(num))));
    const lanthEl = document.getElementById("lanthanides");
    const actEl = document.getElementById("actinides");
    lanthEl.innerHTML = ""; actEl.innerHTML = "";
    for (let i = 57; i <= 71; i++) lanthEl.appendChild(createElementCard(i));
    for (let i = 89; i <= 103; i++) actEl.appendChild(createElementCard(i));
}

let scene, camera, renderer, controls, atomGroup;
const orbits = [];

function init3D() {
    const container = document.querySelector(".atom");
    const canvas = document.getElementById("canvas");
    scene = new THREE.Scene();
    camera = new THREE.PerspectiveCamera(45, container.clientWidth / container.clientHeight, 0.1, 1000);
    renderer = new THREE.WebGLRenderer({ canvas, antialias: true, alpha: true });
    renderer.setSize(container.clientWidth, container.clientHeight);
    renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
    controls = new OrbitControls(camera, renderer.domElement);
    controls.enableDamping = true;

    const light = new THREE.PointLight(0xffffff, 2, 100);
    light.position.set(10, 10, 10);
    scene.add(light);
    scene.add(new THREE.AmbientLight(0xffffff, 0.8));
    atomGroup = new THREE.Group();
    scene.add(atomGroup);

    function animate() {
        requestAnimationFrame(animate);
        if (atomGroup) {
            atomGroup.rotation.y += 0.003;
            orbits.forEach((orbit, index) => { orbit.rotation.z += 0.01 * (index % 2 === 0 ? 1 : -1); });
        }
        controls.update();
        renderer.render(scene, camera);
    }
    animate();
}

function updateAtom3D(number) {
    while (atomGroup.children.length > 0) atomGroup.remove(atomGroup.children[0]);
    orbits.length = 0;

    const nucleusGeo = new THREE.SphereGeometry(1.2, 32, 32);
    const nucleusMat = new THREE.MeshStandardMaterial({ color: 0x55a7ff, roughness: 0.2, metalness: 0.5 });
    atomGroup.add(new THREE.Mesh(nucleusGeo, nucleusMat));

    const shells = [2, 8, 18, 32, 32, 18, 8];
    let remaining = number, radius = 2.2;

    for (let i = 0; i < shells.length && remaining > 0; i++) {
        const count = Math.min(remaining, shells[i]);
        remaining -= count;
        const shellGroup = new THREE.Group();
        shellGroup.rotation.x = (Math.PI / 4) * i;

        const orbitGeo = new THREE.RingGeometry(radius - 0.02, radius + 0.02, 64);
        const orbitMat = new THREE.MeshBasicMaterial({ color: 0x55a7ff, side: THREE.DoubleSide, opacity: 0.2, transparent: true });
        const orbitMesh = new THREE.Mesh(orbitGeo, orbitMat);
        orbitMesh.rotation.x = Math.PI / 2;
        shellGroup.add(orbitMesh);

        for (let j = 0; j < count; j++) {
            const angle = (j / count) * Math.PI * 2;
            const electron = new THREE.Mesh(new THREE.SphereGeometry(0.18, 16, 16), new THREE.MeshStandardMaterial({ color: 0x9b72ff, emissive: 0x331166 }));
            electron.position.set(Math.cos(angle) * radius, 0, Math.sin(angle) * radius);
            shellGroup.add(electron);
        }
        atomGroup.add(shellGroup);
        orbits.push(shellGroup);
        radius += 1.3;
    }
    camera.position.set(0, radius * 1.2, radius * 2.2);
    camera.lookAt(0, 0, 0);
}

window.openElement = function(num) {
    document.getElementById("bigNumber").innerText = num;
    document.getElementById("bigSymbol").innerText = symbols[num - 1];
    document.getElementById("bigName").innerText = names[num - 1];
    document.getElementById("bigCategory").innerText = getCategory(num).replace("-", " ").toUpperCase();
    document.getElementById("pNumber").innerText = num;
    document.getElementById("pMass").innerText = masses[num - 1];
    document.getElementById("pProtons").innerText = num;
    document.getElementById("pElectrons").innerText = num;
    document.getElementById("pNeutrons").innerText = Math.round(masses[num - 1]) - num;
    document.getElementById("pConfig").innerText = getElectronConfiguration(num);
    document.getElementById("elementModal").classList.add("show");
    if (!renderer) init3D();
    updateAtom3D(num);
};

window.closeElement = function() { document.getElementById("elementModal").classList.remove("show"); };

window.filterElements = function() {
    const query = document.getElementById("search").value.toLowerCase();
    const cat = document.getElementById("category").value;
    document.querySelectorAll(".element").forEach(el => {
        const num = el.getAttribute("data-num");
        if (!num) return;
        const name = names[num - 1].toLowerCase();
        const symbol = symbols[num - 1].toLowerCase();
        const elementCat = getCategory(parseInt(num));
        const matches = (name.includes(query) || symbol.includes(query) || num.toString().includes(query)) && (cat === "all" || elementCat === cat);
        el.style.opacity = matches ? "1" : "0.15";
        el.style.pointerEvents = matches ? "auto" : "none";
    });
};

document.addEventListener("DOMContentLoaded", renderTable);
</script>
</body>
</html>.

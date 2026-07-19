<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SIMDA PPNS | Provinsi Nusa Tenggara Timur</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#eef2f7;
}

.header{
height:70px;
background:#003366;
color:white;
display:flex;
justify-content:space-between;
align-items:center;
padding:0 30px;
box-shadow:0 3px 10px rgba(0,0,0,.2);
}

.logo{
display:flex;
align-items:center;
gap:15px;
}

.logo img{
width:45px;
}

.logo h2{
font-size:22px;
}

.container{
display:flex;
}

.sidebar{
width:250px;
background:#0b4a8b;
height:calc(100vh - 70px);
color:white;
padding-top:20px;
}

.sidebar ul{
list-style:none;
}

.sidebar li{
padding:18px 25px;
cursor:pointer;
transition:.3s;
}

.sidebar li:hover{
background:#1565c0;
}

.main{
flex:1;
padding:30px;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:20px;
margin-bottom:30px;
}

.card{
background:white;
padding:25px;
border-radius:12px;
box-shadow:0 8px 20px rgba(0,0,0,.08);
}

.card h3{
font-size:18px;
margin-bottom:10px;
color:#003366;
}

.card h1{
color:#1565c0;
}

.search-box{
background:white;
padding:20px;
border-radius:12px;
box-shadow:0 5px 15px rgba(0,0,0,.08);
margin-bottom:30px;
}

.search-box input{
width:100%;
padding:15px;
border:1px solid #ccc;
border-radius:8px;
font-size:15px;
}

table{
width:100%;
border-collapse:collapse;
background:white;
border-radius:12px;
overflow:hidden;
box-shadow:0 5px 15px rgba(0,0,0,.08);
}

th{
background:#003366;
color:white;
padding:15px;
}

td{
padding:15px;
border-bottom:1px solid #ddd;
}

tr:hover{
background:#f5f5f5;
}

.footer{
margin-top:30px;
text-align:center;
color:#666;
}

@media(max-width:900px){

.sidebar{
display:none;
}

.main{
padding:15px;
}

.header h2{
font-size:18px;
}

}

</style>

</head>

<body>

<div class="header">

<div class="logo">

<img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Coat_of_arms_of_East_Nusa_Tenggara.svg">

<div>

<h2>SIMDA PPNS</h2>

<small>Provinsi Nusa Tenggara Timur</small>

</div>

</div>

<div>

Administrator

</div>

</div>

<div class="container">

<div class="sidebar">

<ul>

<li>🏠 Dashboard</li>

<li>👮 Data PPNS</li>

<li>🏢 Instansi</li>

<li>📑 SK PPNS</li>

<li>📂 Dokumen</li>

<li>📊 Laporan</li>

<li>⚙ Pengaturan</li>

</ul>

</div>

<div class="main">

<div class="cards">

<div class="card">

<h3>Total PPNS</h3>

<h1>245</h1>

</div>

<div class="card">

<h3>Instansi</h3>

<h1>34</h1>

</div>

<div class="card">

<h3>Aktif</h3>

<h1>230</h1>

</div>

<div class="card">

<h3>Tidak Aktif</h3>

<h1>15</h1>

</div>

</div>

<div class="search-box">

<h3>Pencarian Database PPNS</h3>

<br>

<input type="text" id="searchInput" placeholder="Cari Nama atau Instansi...">

</div>

<table id="ppnsTable">

<thead>

<tr>

<th>Nama</th>

<th>NIP</th>

<th>Instansi</th>

<th>Status</th>

</tr>

</thead>

<tbody>

<tr>

<td>Andi Saputra</td>

<td>198901011</td>

<td>Satpol PP NTT</td>

<td>Aktif</td>

</tr>

<tr>

<td>Maria Yosefa</td>

<td>198705122</td>

<td>Dinas Perhubungan</td>

<td>Aktif</td>

</tr>

<tr>

<td>Yohanes Ledo</td>

<td>199001033</td>

<td>Dinas Lingkungan Hidup</td>

<td>Aktif</td>

</tr>

<tr>

<td>Agustinus Benu</td>

<td>198512200</td>

<td>Dinas Perikanan</td>

<td>Tidak Aktif</td>

</tr>

</tbody>

</table>

<div class="footer">

<p>

© 2026 Sistem Informasi Manajemen Database PPNS

<br>

Pemerintah Provinsi Nusa Tenggara Timur

</p>

</div>

</div>

</div>

<script>

const input=document.getElementById("searchInput");

input.addEventListener("keyup",function(){

let filter=input.value.toUpperCase();

let table=document.getElementById("ppnsTable");

let tr=table.getElementsByTagName("tr");

for(let i=1;i<tr.length;i++){

let td=tr[i].getElementsByTagName("td");

let tampil=false;

for(let j=0;j<td.length;j++){

if(td[j]){

if(td[j].innerHTML.toUpperCase().indexOf(filter)>-1){

tampil=true;

}

}

}

tr[i].style.display=tampil?"":"none";

}

});

</script>

</body>
</html>

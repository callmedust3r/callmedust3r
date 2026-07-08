<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Моё портфолио</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
}

:root{

--bg:#050505;
--card:rgba(255,255,255,.05);
--border:rgba(255,255,255,.08);
--text:#ffffff;
--sub:#a6a6a6;

--accent:#4F8CFF;
--accent2:#7F5AF0;

}

body{

font-family:Inter,sans-serif;
background:var(--bg);
color:white;
overflow-x:hidden;

}

/* ============================= */
/* ФОН */
/* ============================= */

.background{

position:fixed;
inset:0;
z-index:-10;

background:
radial-gradient(circle at 20% 30%,#4F8CFF33,transparent 30%),
radial-gradient(circle at 80% 60%,#7F5AF033,transparent 35%),
linear-gradient(#050505,#090909);

overflow:hidden;

}

.blur{

position:absolute;
width:700px;
height:700px;

border-radius:50%;

filter:blur(140px);

animation:float 14s infinite ease-in-out;

opacity:.55;

}

.blur:nth-child(1){

background:#4F8CFF;

top:-250px;
left:-180px;

}

.blur:nth-child(2){

background:#7F5AF0;

right:-200px;
bottom:-200px;

animation-delay:4s;

}

@keyframes float{

50%{

transform:
translateY(80px)
translateX(40px)
scale(1.15);

}

}

/* ============================= */

header{

position:fixed;
top:0;
left:0;

width:100%;

padding:20px 9%;

display:flex;

justify-content:space-between;

align-items:center;

backdrop-filter:blur(25px);

background:rgba(5,5,5,.35);

border-bottom:1px solid rgba(255,255,255,.05);

z-index:999;

}

.logo{

font-size:26px;
font-weight:800;

letter-spacing:1px;

}

.logo span{

color:var(--accent);

}

nav{

display:flex;
gap:35px;

}

nav a{

text-decoration:none;

color:white;

font-weight:500;

transition:.3s;

position:relative;

}

nav a::after{

content:"";

position:absolute;

left:0;
bottom:-7px;

height:2px;

width:0;

background:var(--accent);

transition:.3s;

}

nav a:hover::after{

width:100%;

}

/* ============================= */

.hero{

min-height:100vh;

display:grid;

grid-template-columns:1.1fr .9fr;

align-items:center;

padding:0 10%;

gap:60px;

}

.hero h3{

color:var(--accent);

margin-bottom:15px;

letter-spacing:2px;

}

.hero h1{

font-size:72px;

line-height:1.05;

margin-bottom:25px;

}

.hero p{

font-size:18px;

line-height:1.8;

color:var(--sub);

margin-bottom:45px;

max-width:700px;

}

.buttons{

display:flex;

gap:20px;

flex-wrap:wrap;

}

.btn{

padding:16px 34px;

border-radius:14px;

font-weight:700;

text-decoration:none;

transition:.35s;

}

.btn-primary{

background:linear-gradient(135deg,var(--accent),var(--accent2));

color:white;

}

.btn-secondary{

border:1px solid rgba(255,255,255,.15);

color:white;

}

.btn:hover{

transform:translateY(-5px);

}

/* ============================= */

.hero-photo{

display:flex;

justify-content:center;

}

.avatar{

width:390px;
height:390px;

border-radius:40px;

object-fit:cover;

border:2px solid rgba(255,255,255,.1);

box-shadow:

0 20px 80px rgba(79,140,255,.35);

transition:.45s;

}

.avatar:hover{

transform:
rotate(-2deg)
scale(1.03);

}

/*
=====================================

TODO

ЗАМЕНИ ЭТУ КАРТИНКУ

images/avatar.jpg

=====================================
*/

section{

padding:120px 10%;

}

.title{

font-size:48px;

margin-bottom:25px;

}

.subtitle{

color:var(--sub);

max-width:760px;

line-height:1.8;

}

/* ============================= */

.grid{

display:grid;

grid-template-columns:
repeat(auto-fit,minmax(260px,1fr));

gap:25px;

margin-top:60px;

}

.card{

background:var(--card);

border:1px solid var(--border);

backdrop-filter:blur(30px);

border-radius:24px;

padding:35px;

transition:.4s;

}

.card:hover{

transform:
translateY(-10px);

border-color:#4F8CFF55;

}

.card h3{

margin-bottom:15px;

}

.card p{

color:var(--sub);

line-height:1.8;

}

/* ============================= */

.projects{

display:grid;

grid-template-columns:
repeat(auto-fit,minmax(360px,1fr));

gap:35px;

margin-top:60px;

}

.project{

background:#111;

border-radius:24px;

overflow:hidden;

border:1px solid rgba(255,255,255,.06);

transition:.45s;

}

.project:hover{

transform:translateY(-10px);

}

.project img{

width:100%;

height:230px;

object-fit:cover;

}

/*

TODO

images/project1.jpg

TODO

images/project2.jpg

TODO

images/project3.jpg

*/

.project-content{

padding:30px;

}

.project-content h3{

margin-bottom:15px;

}

.project-content p{

line-height:1.8;

color:var(--sub);

margin-bottom:25px;

}

.project a{

display:inline-block;

padding:12px 22px;

border-radius:12px;

background:linear-gradient(135deg,var(--accent),var(--accent2));

color:white;

text-decoration:none;

font-weight:700;

}

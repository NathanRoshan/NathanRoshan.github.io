<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nathan Roshan | DevOps Engineer</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Poppins,sans-serif;
scroll-behavior:smooth;
}

body{

background:#0d1117;
color:white;

}

nav{

position:fixed;
width:100%;
padding:20px;
display:flex;
justify-content:space-between;
align-items:center;
background:#111827cc;
backdrop-filter:blur(12px);
z-index:999;

}

nav a{

color:white;
text-decoration:none;
margin-left:20px;
transition:.3s;

}

nav a:hover{

color:#00d8ff;

}

.hero{

height:100vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
flex-direction:column;

}

.hero h1{

font-size:70px;

background:linear-gradient(90deg,#00d8ff,#00ff99);

-webkit-background-clip:text;
-webkit-text-fill-color:transparent;

}

.hero h2{

margin-top:15px;
font-size:30px;
height:40px;

}

.hero p{

margin-top:30px;
max-width:800px;
line-height:1.8;
color:#bbb;

}

.btn{

margin-top:40px;
padding:15px 35px;
background:#00d8ff;
color:black;
font-weight:bold;
border-radius:50px;
text-decoration:none;
transition:.3s;

}

.btn:hover{

transform:scale(1.08);

}

section{

padding:100px 10%;

}

.title{

font-size:40px;
margin-bottom:50px;
text-align:center;

}

.skills{

display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:25px;

}

.card{

background:#161b22;
padding:30px;
border-radius:15px;
transition:.4s;
border:1px solid #222;

}

.card:hover{

transform:translateY(-10px);
box-shadow:0 0 30px #00d8ff44;

}

.card h3{

margin-bottom:15px;

}

footer{

padding:40px;
text-align:center;
color:#999;

}

.fade{

opacity:0;
transform:translateY(40px);
transition:1s;

}

.fade.show{

opacity:1;
transform:translateY(0);

}

</style>

</head>

<body>

<nav>

<h2>Roshan</h2>

<div>

<a href="#about">About</a>
<a href="#skills">Skills</a>
<a href="#contact">Contact</a>

</div>

</nav>

<section class="hero">

<h1>Roshan Nathan</h1>

<h2 id="typing"></h2>

<p>

Associate Technical Lead – DevOps Engineer with expertise in Kubernetes,
AWS, Terraform, Docker, GitHub Actions, ArgoCD, Linux, CI/CD Automation,
Infrastructure as Code, Cloud Security, and GitOps.

</p>

<a href="#skills" class="btn">Explore My Skills</a>

</section>

<section id="about" class="fade">

<h2 class="title">About Me</h2>

<p style="text-align:center;max-width:900px;margin:auto;line-height:2;color:#ccc;">

I specialize in designing highly available cloud platforms,
automating infrastructure,
implementing GitOps,
container orchestration,
and securing enterprise Kubernetes environments.

I enjoy solving complex infrastructure challenges and building scalable platforms.

</p>

</section>

<section id="skills" class="fade">

<h2 class="title">Technical Skills</h2>

<div class="skills">

<div class="card">
<h3>☁ AWS</h3>
EC2 • IAM • VPC • EKS • Route53 • S3
</div>

<div class="card">
<h3>☸ Kubernetes</h3>
EKS • kubeadm • Helm • Istio • Cilium
</div>

<div class="card">
<h3>⚙ DevOps</h3>
GitHub Actions • Jenkins • ArgoCD • GitOps
</div>

<div class="card">
<h3>🐳 Containers</h3>
Docker • containerd • Harbor
</div>

<div class="card">
<h3>🏗 IaC</h3>
Terraform • Ansible • Packer
</div>

<div class="card">
<h3>🖥 Linux</h3>
RHEL • Rocky Linux • Ubuntu • Oracle Linux
</div>

</div>

</section>

<section id="contact" class="fade">

<h2 class="title">Contact</h2>

<div style="text-align:center;line-height:2;">

<p>📧 your-email@example.com</p>

<p>
<a href="https://github.com/NathanRoshan" style="color:#00d8ff;">
GitHub
</a>
</p>

<p>
<a href="https://linkedin.com" style="color:#00d8ff;">
LinkedIn
</a>
</p>

</div>

</section>

<footer>

© 2026 Roshan Nathan | DevOps Engineer

</footer>

<script>

const words=[
"Associate Technical Lead",
"DevOps Engineer",
"AWS Specialist",
"Kubernetes Expert",
"Cloud Architect",
"Automation Engineer"
];

let i=0;
let j=0;
let current="";
let isDeleting=false;

function type(){

current=words[i];

document.getElementById("typing").textContent=current.substring(0,j);

if(!isDeleting){

j++;

if(j>current.length){

isDeleting=true;

setTimeout(type,1000);

return;

}

}else{

j--;

if(j==0){

isDeleting=false;

i=(i+1)%words.length;

}

}

setTimeout(type,isDeleting?60:120);

}

type();

const observer=new IntersectionObserver(entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

});

document.querySelectorAll(".fade").forEach(el=>observer.observe(el));

</script>

</body>
</html>

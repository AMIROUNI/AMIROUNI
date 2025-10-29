# Creating a custom SVG banner for the user and returning a base64 data URI
svg = """<svg xmlns='http://www.w3.org/2000/svg' width='2000' height='600' viewBox='0 0 2000 600'>
  <defs>
    <linearGradient id='g' x1='0' x2='1'>
      <stop offset='0' stop-color='#0f172a'/>
      <stop offset='1' stop-color='#0ea5a3'/>
    </linearGradient>
    <pattern id='code' width='20' height='20' patternUnits='userSpaceOnUse'>
      <rect width='20' height='20' fill='rgba(255,255,255,0.02)'/>
      <text x='10' y='14' font-family='monospace' font-size='10' fill='rgba(255,255,255,0.03)' text-anchor='middle'>{}</text>
    </pattern>
  </defs>
  <rect width='100%' height='100%' fill='url(#g)'/>
  <rect x='0' y='0' width='100%' height='100%' fill='url(#code)'/>
  <g transform='translate(80,120)'>
    <text x='0' y='0' font-family='Inter, Arial, sans-serif' font-weight='700' font-size='72' fill='white'>Amir Ouni</text>
    <text x='0' y='90' font-family='Inter, Arial, sans-serif' font-weight='600' font-size='36' fill='rgba(255,255,255,0.9)'>Software Engineer — AI · Backend · DevOps</text>
    <rect x='0' y='120' width='1400' height='3' fill='rgba(255,255,255,0.12)' rx='2'/>
    <g transform='translate(0,160)'>
      <text x='0' y='40' font-family='Inter, Arial, sans-serif' font-size='26' fill='rgba(255,255,255,0.85)'>Languages: Python • Java • JavaScript • SQL</text>
      <text x='0' y='80' font-family='Inter, Arial, sans-serif' font-size='20' fill='rgba(255,255,255,0.7)'>Tools: Git • Docker • Kubernetes • PyTorch • Spring Boot</text>
    </g>
  </g>
  <g transform='translate(1450,30)'>
    <rect x='0' y='0' width='500' height='540' rx='18' fill='rgba(255,255,255,0.06)'/>
    <text x='40' y='110' font-family='monospace' font-size='20' fill='rgba(255,255,255,0.7)'>{"{ }"}</text>
    <text x='40' y='150' font-family='monospace' font-size='18' fill='rgba(255,255,255,0.65)'>// build • test • deploy</text>
    <text x='40' y='190' font-family='monospace' font-size='18' fill='rgba(255,255,255,0.65)'>// reliable • scalable • clean</text>
  </g>
</svg>
"""
import base64
svg_bytes = svg.encode('utf-8')
b64 = base64.b64encode(svg_bytes).decode('ascii')
data_uri = f"data:image/svg+xml;base64,{b64}"

markdown = f"[![Amir Ouni Banner]({data_uri})](https://amirouni.github.io/Portfolio/)\n\n" \
           f"**Direct image link (works 2025+)**:\n\n`{data_uri}`\n\n" \
           f"Paste the first line into your GitHub README to show the banner."

# Show small preview info and provide download
from pathlib import Path
out_path = "/mnt/data/amir_banner.svg"
Path(out_path).write_text(svg, encoding='utf-8')

print("data_uri_preview=", data_uri[:200], "...")  # shortened preview
print("\nSaved SVG to:", out_path)
print("\nMarkdown snippet ready. Copy the full data URI from the 'Direct image link' line in the output.")
markdown, data_uri, out_path



<h1 align="center">Hi 👋, I'm Amir Ouni</h1>
<h3 align="center">Software Engineering Student</h3>

---

### 🔭 Current Projects  
- Developing a **mobile application**  
- Building a **web application**

### 🌱 Currently Learning  
- **Node.js**  
- **Android Development**  
- **.NET**  
- **Angular**  
- **Web Services (RESTful & GraphQL)**

### 👯 Looking to Collaborate On  
Software development projects, especially in **web and mobile development**.  

### 🤝 Seeking Help With  
Enhancing my **software development skills** and exploring career paths as a **Java OSA (Operations System Administrator)**.

### 💬 Ask Me About  
- **Frontend Development:** React, Vue, Angular, GSAP  
- **Backend & APIs:** Spring Boot, RESTful APIs, GraphQL  
- **AI & Deep Learning:** PyTorch, NLP, Binary Classification Models  
- **System Administration:** Red Hat (RHCSA Certified), Podman, Linux  

### 📫 How to Reach Me  
📧 **Email:** amirouni162@gmail.com  

### 👨‍💻 My Work  
🔗 **Portfolio:** [amirouni.github.io/Portfolio/](https://amirouni.github.io/Portfolio/)  
🔗 **GitHub:** [github.com/AMIROUNI](https://github.com/AMIROUNI)  
🔗 **LinkedIn:** [linkedin.com/in/amir-el-ouni](https://www.linkedin.com/in/amir-el-ouni-8808662a1/)

<br>
<p align="center">
  <img alt="Coding" width="400" src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExNm13MmdybjI3ZjJ5MnQ4Nmd1dW5sOWtpdTZnbmR3dWRpNjBud3g1OCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/ua7vVw9awZKWwLSYpW/giphy.gif">
</p>

## 🛠️ Languages and Tools  

<p align="left">
  <a href="https://dotnet.microsoft.com/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dot-net/dot-net-original.svg" alt=".NET" width="40" height="40"/>
  </a>
  <a href="https://angular.io/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/angularjs/angularjs-original.svg" alt="Angular" width="40" height="40"/>
  </a>
  <a href="https://developer.android.com/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original.svg" alt="Android" width="40" height="40"/>
  </a>
  <a href="https://graphql.org/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/graphql/graphql-plain.svg" alt="GraphQL" width="40" height="40"/>
  </a>
  <a href="https://restfulapi.net/" target="_blank">
    <img src="https://img.icons8.com/external-flatart-icons-outline-flatarticons/64/000000/external-api-web-development-flatart-icons-outline-flatarticons.png" alt="RESTful API" width="40" height="40"/>
  </a>
  <a href="https://nodejs.org/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" alt="Node.js" width="40" height="40"/>
  </a>
  <a href="https://spring.io/projects/spring-boot" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original.svg" alt="Spring Boot" width="40" height="40"/>
  </a>
  <a href="https://git-scm.com/" target="_blank">
    <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" width="40" height="40"/>
  </a>
  <a href="https://www.linux.org/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="Linux" width="40" height="40"/>
  </a>
  <a href="https://www.redhat.com/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redhat/redhat-original.svg" alt="Red Hat (RHCSA Certified)" width="40" height="40"/>
  </a>
  <a href="https://vuejs.org/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original.svg" alt="Vue.js" width="40" height="40"/>
  </a>
  <a href="https://www.react.dev/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="React" width="40" height="40"/>
  </a>
  <a href="https://www.python.org/" target="_blank">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="40" height="40"/>
  </a>
</p>

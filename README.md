from pathlib import Path
import zipfile

readme = r'''<div align="center">

<h1>
  <span style="color:#38BDF8;">ÅR RAAD</span>
</h1>

<h3>💻 Web Developer in Progress</h3>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=900&color=38BDF8&center=true&vCenter=true&width=720&lines=Code+%E2%80%A2+Build+%E2%80%A2+Grow+%F0%9F%9A%80;Learning+Web+Development+%F0%9F%92%BB;HTML+%7C+CSS+%7C+Tailwind+CSS+%7C+React+JS+%7C+Next+JS;Small+Steps+%E2%86%92+Big+Progress+%F0%9F%8C%B1" alt="Typing Animation"/>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:020617,50:0B1F4D,100:06B6D4&height=4&section=header" width="90%"/>

</div>

<br/>

<table>
<tr>
<td width="48%" valign="top">

## 👋 Hi, I'm ÅR RAAD

I'm a passionate **Web Developer in Progress**, currently learning and building modern web applications.

💡 I love turning ideas into real projects and exploring new technologies.

🚀 **Let's build something amazing!**

### 📍 Location
**Kapasia, Gazipur, Bangladesh**

</td>

<td width="52%" valign="top">

## 📫 Contact Me

<table>
<tr>
<td>🟢 <b>WhatsApp</b></td>
<td>01814725084</td>
</tr>
<tr>
<td>📧 <b>Email</b></td>
<td><a href="mailto:raad73575@gmail.com">raad73575@gmail.com</a></td>
</tr>
<tr>
<td>📍 <b>Location</b></td>
<td>Kapasia, Gazipur, Bangladesh</td>
</tr>
</table>

<br/>

<a href="https://wa.me/8801814725084">
<img src="https://img.shields.io/badge/WhatsApp-01814725084-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>

<a href="mailto:raad73575@gmail.com">
<img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</td>
</tr>
</table>

---

<div align="center">

# 🧑‍💻 My Tech Stack

<table>
<tr>
<td align="center" width="150">

<img src="https://skillicons.dev/icons?i=html" width="60"/>

### HTML

</td>
<td align="center" width="150">

<img src="https://skillicons.dev/icons?i=css" width="60"/>

### CSS

</td>
<td align="center" width="150">

<img src="https://skillicons.dev/icons?i=tailwind" width="60"/>

### Tailwind CSS

</td>
<td align="center" width="150">

<img src="https://skillicons.dev/icons?i=react" width="60"/>

### React JS

</td>
<td align="center" width="150">

<img src="https://skillicons.dev/icons?i=nextjs" width="60"/>

### Next JS

</td>
</tr>
</table>

</div>

---

<div align="center">

# 📊 GitHub Stats

<table>
<tr>
<td>

<img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&rank_icon=github" height="180"/>

</td>
<td>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=tokyonight&hide_border=true" height="180"/>

</td>
</tr>
</table>

</div>

---

<div align="center">

# 🔥 Contribution Streak

<img src="https://streak-stats.demolab.com?user=YOUR_GITHUB_USERNAME&theme=tokyonight&hide_border=true&border_radius=12" />

</div>

---

<div align="center">

# 🐍 Contribution Animation

<img src="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_GITHUB_USERNAME/output/github-contribution-grid-snake.svg" alt="GitHub Contribution Snake"/>

</div>

---

<div align="center">

# 🚀 What I'm Learning

<table>
<tr>
<td align="center">

<img src="https://skillicons.dev/icons?i=html" width="50"/><br/>
<b>HTML</b>

</td>
<td>➡️</td>
<td align="center">

<img src="https://skillicons.dev/icons?i=css" width="50"/><br/>
<b>CSS</b>

</td>
<td>➡️</td>
<td align="center">

<img src="https://skillicons.dev/icons?i=tailwind" width="50"/><br/>
<b>Tailwind</b>

</td>
<td>➡️</td>
<td align="center">

<img src="https://skillicons.dev/icons?i=js" width="50"/><br/>
<b>JavaScript</b>

</td>
<td>➡️</td>
<td align="center">

<img src="https://skillicons.dev/icons?i=react" width="50"/><br/>
<b>React JS</b>

</td>
<td>➡️</td>
<td align="center">

<img src="https://skillicons.dev/icons?i=nextjs" width="50"/><br/>
<b>Next JS</b>

</td>
</tr>
</table>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&pause=1100&color=A78BFA&center=true&vCenter=true&width=620&lines=Keep+Coding+%F0%9F%92%BB;Keep+Learning+%F0%9F%8C%B1;Keep+Building+%F0%9F%9A%80;Better+Code+%E2%86%92+Bigger+Dreams+%E2%9C%A8" alt="Footer Animation"/>

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:2563EB,100:7C3AED&height=110&section=footer" width="100%"/>

</div>
'''

out = Path("/mnt/data/README.md")
out.write_text(readme, encoding="utf-8")

zip_path = Path("/mnt/data/raad-readme-only.zip")
with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:
    z.write(out, "README.md")

print(out)
print(zip_path)

from pathlib import Path
import shutil
import zipfile

src = Path("/mnt/data/ChatGPT Image Sep 25, 2026, 07_56_05 PM.png")
out_dir = Path("/mnt/data/raad-github-profile")
out_dir.mkdir(exist_ok=True)

banner = out_dir / "profile-banner.png"
shutil.copy2(src, banner)

readme = r'''<div align="center">

<!-- Replace profile-banner.png with your banner image if you want to use another one -->
<img src="./profile-banner.png" alt="ÅR RAAD Developer Banner" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=900&color=38BDF8&center=true&vCenter=true&width=760&lines=Hi%2C+I'm+%C3%85R+RAAD+%F0%9F%91%8B;Web+Developer+in+Progress+%F0%9F%92%BB;Learning+%E2%80%A2+Building+%E2%80%A2+Improving+%F0%9F%9A%80;Small+Steps+%E2%86%92+Big+Progress+%F0%9F%8C%B1" alt="Typing Animation"/>

</div>

---

## 👋 Hi, I'm <span style="color:#38BDF8">ÅR RAAD</span>

I'm a passionate **Web Developer in Progress**, currently learning and building modern web applications. I enjoy turning ideas into real projects and exploring new technologies.

> 💙 **Let's build something amazing! 🚀**

---

## 💻 Skills & Technologies

<div align="center">

| HTML | CSS | Tailwind CSS | React JS | Next JS |
|:---:|:---:|:---:|:---:|:---:|
| <img src="https://skillicons.dev/icons?i=html" width="60"> | <img src="https://skillicons.dev/icons?i=css" width="60"> | <img src="https://skillicons.dev/icons?i=tailwind" width="60"> | <img src="https://skillicons.dev/icons?i=react" width="60"> | <img src="https://skillicons.dev/icons?i=nextjs" width="60"> |
| **HTML** | **CSS** | **Tailwind CSS** | **React JS** | **Next JS** |

</div>

---

## 📫 Contact Me

<div align="center">

<a href="https://wa.me/8801814725084">
<img src="https://img.shields.io/badge/WhatsApp-01814725084-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
</a>

<a href="mailto:raad73575@gmail.com">
<img src="https://img.shields.io/badge/Email-raad73575%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

</div>

📍 **Location:** Kapasia, Gazipur, Bangladesh

---

## 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&rank_icon=github" />

<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=tokyonight&hide_border=true" />

</div>

---

## 🔥 Contribution Streak

<div align="center">

<img src="https://streak-stats.demolab.com?user=YOUR_GITHUB_USERNAME&theme=tokyonight&hide_border=true&border_radius=10" alt="GitHub Contribution Streak" />

</div>

---

## 🐍 Contribution Animation

<div align="center">

<img src="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_GITHUB_USERNAME/output/github-contribution-grid-snake.svg" alt="Contribution Snake" />

</div>

---

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1200&color=A78BFA&center=true&vCenter=true&width=600&lines=Keep+Coding+%F0%9F%92%BB;Keep+Learning+%F0%9F%8C%B1;Keep+Building+%F0%9F%9A%80;Better+Code%2C+Bigger+Dreams+%E2%9C%A8" alt="Footer Animation"/>

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:2563EB,100:7C3AED&height=110&section=footer" width="100%"/>

</div>
'''

readme_path = out_dir / "README.md"
readme_path.write_text(readme, encoding="utf-8")

zip_path = Path("/mnt/data/raad-github-profile.zip")
with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:
    z.write(readme_path, "README.md")
    z.write(banner, "profile-banner.png")

print(readme_path)
print(zip_path)

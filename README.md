<h1 align="center">Hi 👋, I'm Supratik Patra</h1>
<h3 align="center">An innovative Computer Science Student & Embedded Systems Hobbyist from India</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-Embedded_Systems_&_IoT-9cf?style=for-the-badge&logo=arduino" />
  <img src="https://img.shields.io/badge/Domain-AI_/_ML_/_Computer_Vision-blue?style=for-the-badge&logo=opencv" />
  <img src="https://img.shields.io/badge/Location-India-orange?style=for-the-badge" />
</p>

---

### 🚀 About Me

<img align="right" height="150" src="https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExNnA3YmoxZmN6bTI0Ym8wdG05MXN5Nzh6MXZsczZ6eW84dGZubW90NCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Q3XbK6v8006E8/giphy.gif" alt="Circuit Board Animation" />

- 🔭 **Current Projects:** Building smart assistive technologies, intelligent hardware integrations, and computer vision frameworks.
- ⚡ **Recent Builds:** Developed a *Facial Recognition Attendance System*, an *Air Guitar* using an MPU6050 accelerometer, and working on *Silent Communicator* assistive tech.
- 🌱 **Actively Learning:** Advanced algorithmic problem solving, machine learning pipelines, and embedded software architectures.
- 💬 **Ask me about:** Microcontrollers, circuit troubleshooting, C/C++, and Python.
- 📫 **How to reach me:** [patrasupratik2006@gmail.com](mailto:patrasupratik2006@gmail.com)

<p align="left">
  <a href="https://www.linkedin.com/in/supratik-patra06" target="blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

---

### 🛠️ Languages and Tools

<p align="left">
  <!-- Languages -->
  <strong style="display:block; margin-bottom: 5px;">Programming Languages:</strong>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" width="42" height="42"/>&nbsp;
  <br><br>
  
  <!-- Hardware & IoT -->
  <strong style="display:block; margin-bottom: 5px;">Hardware & Embedded Systems:</strong>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/arduino/arduino-original.svg" alt="Arduino" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/raspberrypi/raspberrypi-original.svg" alt="Raspberry Pi" width="42" height="42"/>&nbsp;
  <img src="https://www.vectorlogo.zone/logos/espressif/espressif-icon.svg" alt="ESP32/NodeMCU" width="42" height="42"/>&nbsp;
  <br><br>

  <!-- Dev Tools -->
  <strong style="display:block; margin-bottom: 5px;">Development Tools:</strong>
  <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" width="42" height="42"/>&nbsp;
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg" alt="VS Code" width="42" height="42"/>&nbsp;
</p>

---

### 📊 GitHub Analytics

<p align="center">
  <img align="left" src="https://github-readme-stats.vercel.app/api?username=Supratik06patra&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" alt="Supratik's GitHub Stats" height="180px" />
  <img align="right" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Supratik06patra&layout=compact&theme=tokyonight" alt="Supratik's Top Languages" height="180px" />
</p>

<br clear="both">
<br>

### 🐍 Contribution Graph

name: Generate Snake

on:
  schedule:
    # Runs every 12 hours automatically
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          

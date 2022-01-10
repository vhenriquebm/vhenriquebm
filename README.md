### Hi there 👋



<div align="center">
  <a href="https://github.com/vhenriquebm">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=vhenriquebm&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=vhenriquebm&layout=compact&langs_count=7&theme=dark"/>
</div>

  
  
  <div style="display: inline_block"><br>
  <img align="center" alt="Vitor-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Vitor-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Vitor-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Vitor-Swift" height="30" width="40" src="https://image.flaticon.com/icons/png/512/732/732250.png">
  </div>
  
  <br>
  
  <div> 
  <a href = "mailto:vhenriquebm@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"</a>
  <a href="https://www.linkedin.com/in/vitor-henrique-736b72213/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 

    
    
      ![Snake animation](https://github.com/vhenriquebm)
    
    name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

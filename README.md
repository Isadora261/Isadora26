# Isadora26
- 🔭 Atualmente sou aluna do 3C
- 🌱 Atualmente estou aprendendo pensamento computacional
- 📫 Como entrar em contato comigo: @_isadora_winck
<div>
<a href="https://github.com/seu-usuário-aqui">
<img loading="lazy" height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=seu-usuário-aqui&layout=compact&langs_count=7&theme=dracula"/>
<img loading="lazy" height="180em" src="https://github-readme-stats.vercel.app/api?username=seu-usuário-aqui&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
</div>

![Snake animation](https://github.com/Isadora261/Isadora261/blob/output/github-contribution-grid-snake.svg)

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
          github_user_name: seu-usuário-aqui
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

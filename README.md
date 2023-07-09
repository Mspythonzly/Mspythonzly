### 大家好！我是蟒蛇，一名IT运维专家。我热衷于解决技术难题，擅长服务器管理和协议制定。我对各种操作系统和网络架构都非常熟悉，并且乐于与团队协作。拥有丰富的工作经验，我喜欢不断学习和探索新的技术领域，以提供高质量的解决方案。我对技术的激情驱使着我不断进步，致力于为客户提供卓越的服务和支持。👋

# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Hong_Kong
          plugin_lines: yes
          plugin_lines_history_limit: 1
          plugin_lines_repositories_limit: 4
          plugin_lines_sections: base
          plugin_posts: yes
          plugin_posts_limit: 4
          plugin_posts_user: .user.login
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: starred
          plugin_topics_sort: stars

</br>

<div align="center"> <img height="137px" src="https://github-readme-stats.vercel.app/api?username=sun0225SUN&hide_title=true&hide_border=true&show_icons=trueline_height=21&text_color=000&icon_color=000&bg_color=0,ea6161,ffc64d,fffc4d,52fa5a&theme=graywhite" /> </div>

### Shiny
- Host Shiny app with Shiny Server ^[https://www.rstudio.com/products/shiny/shiny-server/?_ga=2.72750996.603836587.1657812871-447252997.1657812871]

![[Pasted image 20220714113724.png]]

- Deploy your Shiny App ^[https://bookdown.org/hadrien/how_to_build_a_shiny_app_from_scratch/deploying-your-shiny-application.html]
- Shiny server ^[https://www.rstudio.com/products/shiny/download-server/]
- Shiny Server Admin Guide ^[https://docs.rstudio.com/shiny-server/]
- Need script that automatically pulls files and only new files
- Database?
- Redesign for new App?

How to deploy shiny server on AWS ^[https://www.youtube.com/watch?v=0h9VOQZX6QM]
- EC2^[https://youtu.be/0h9VOQZX6QM?t=299]
- Security groups need to be set up to open up app to traffic from internet^[https://youtu.be/0h9VOQZX6QM?t=437]
- custom TCP shiny port 3838 ^[https://youtu.be/0h9VOQZX6QM?t=559]
	- can be changed
- open Custom TCP, HTTP, and HTTPS to traffic from anywhere (source) 
- key-pair needed ^[https://youtu.be/0h9VOQZX6QM?t=621]
	- only want root user 
- install shiny server^[https://youtu.be/0h9VOQZX6QM?t=882]^[https://www.r-bloggers.com/2015/10/install-shiny-server-for-r-on-ubuntu-the-right-way/]
- install shiny library ^[https://youtu.be/0h9VOQZX6QM?t=1015]
- More advanced permission system need to use more advanced version of shiny server ^[https://youtu.be/0h9VOQZX6QM?t=1714]

#### Shiny meeting
- 10 days
- Give David O GH repo

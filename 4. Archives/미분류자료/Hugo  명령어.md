Hugo  명령어

blogdown::new_site(theme = "yoshiharuyamashita/blackburn", theme_example = TRUE)



servr::daemon_stop("206614776")


file.edit("~/.Rprofile")

blogdown::build_site(local = TRUE)


blogdown::build_site(local = FALSE)


build_site(local = FALSE, method = c("html", "custom"), run_hugo = TRUE)


blogdown::hugo_build()
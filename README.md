# gradcade_app
RShiny app analyzing the economics admissions process using data from www.thegradcafe.com

This project scrapes and analyzes data from www.thegradcafe.com in order to understand the application process for economics PhD programs.  It includes the following scripts:

1)	gradcafe_scrape_clean.R – this script scrapes every post to economics PhD programs on www.thegradcafe.com and cleans them to get them ready to be used in the app.  It also incorporates rankings from USNEWS (https://www.usnews.com/best-graduate-schools/top-humanities-schools/economics-rankings).
2)	app.R – this scripts creates the app with three tabs.  
  a.	The first one creates overall summary visualizations of when decisions were sent out, as well as when       specific schools sent out decisions and how gradcafe users did at each school.  
  b.	The second tab allows the user to pick a school they want analyzed more thoroughly.  It then displays histograms for when that school sent out acceptances and rejections in the prior year, as well as a scatterplot of what the applicants GPA and GRE quant scores were, sorted by whether they were accepted or rejected.
  c.	The third tab helps the user understand what range of schools their GPA/GRE scores will get them into.  The slider bar has them set the range of school rankings they want to apply to.  They then input their own GPA and GRE scores and they will see a scatterplot for all of the applicants from the prior year who posted decisions for that range of schools.

The project includes the following data files:
1)	gradcafe.csv – this is the raw scraped data from www.thegradcafe.com
2)	app_data.csv – this is the cleaned version of gradcafe.csv
3)	rankings.dta – this contains the school rankings from USNEWS, cleaned so that it will string-match with app_data.csv
4)	modal_acpt.csv – this contains the modified strings from app_data to get all of the school names into the “Modal Acceptance Date by USNEWS Ranking” graph.

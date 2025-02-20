# STA 380: Intro to Machine Learning  

Welcome to part 2 of STA 380, a course on machine learning in the MS program in Business Analytics at UT-Austin.  All course materials can be found through this GitHub page.  Please see the [course syllabus](syllabus.md) for links and descriptions of the readings mentioned below.

Instructors:  
- Dr. James Scott.  Office hours on M T W, 12:30 to 1:15 PM, CBA 6.478.  
- Dr. David Puelz.  Office hours on M T W, 4-4:45p in CBA 6.444.  


## Exercises

The exercises are [available here](exercises/).  These are due Monday, August 15th at 5 PM, U.S central time.  Pace yourself over the next few weeks, and start early on the first couple of problems!  
 

## Outline of topics  

### (1) The data scientist's toolbox

Slides: [The data scientist's toolbox](slides/01_datascience_toolbox/01_datascience_toolbox.pdf)  
Good data-curation and data-analysis practices; R; Markdown and RMarkdown; the importance of replicable analyses; version control with Git and Github.

Readings:  
- [Introduction to RMarkdown](http://rmarkdown.rstudio.com)  
- [RMarkdown tutorial](https://rmarkdown.rstudio.com/lesson-1.html)  
- [Introduction to GitHub](https://guides.github.com/activities/hello-world/)   
- [Getting starting with GitHub Desktop](https://help.github.com/en/desktop/getting-started-with-github-desktop)  
- [Jeff Leek's guide to sharing data](https://github.com/jtleek/datasharing)  

Your assignment after the first class day:  
- Create a GitHub account.  
- Create your first GitHub repository.  
- Inside that repository (on your local machine), create a toy RMarkdown file that does something---e.g. simulates some normal random variables and plots a histogram.  
- Knit that RMarkdown file to a Markdown (.md) output.  
- Push the changes to GitHub and view the final (knitted) .md file.  

These instructions will make sense after you read the tutorials above!  


### (2) Probability: a refresher  

Slides: [Some fun topics in probability](slides/02_probability_refresher/probability_fun_topics.pdf)  

Optional reference: [Chapter 1 of these course notes.](./notes/Bertsekas_Tsitsiklis_Introduction_to_probability.pdf)  There's a lot more technical stuff in here, but Chapter 1 really covers the basics of what every data scientist should know about probability. 



### (3) Data wrangling and visualization

Topics: data visualization and wrangling with R.  

Slides:  
- [Data visualization](slides/03_data_exploration/datavis.pdf)  
- [Data wrangling](slides/03_data_exploration/wrangling.pdf)  


R materials:  

- Lessons 4-6 of [Data Science in R: A Gentle Introduction](https://bookdown.org/jgscott/DSGI/).  You'll find lesson 5 a bit basic so feel free to breeze through that.  The main thing you need to take away from lesson 5 is the use of pipes (`%>%`) and the `summarize` function.    
- [datavis_intro.R](R/datavis_intro.R) and [nycflights_wrangle.R](R/nycflights_wrangle.R).  


### (4) Resampling methods

The bootstrap; joint distributions; using the bootstrap to approximate value at risk (VaR).  

Slides: [Introduction to the bootstrap](slides/04_resampling/bootstrap_STA380.pdf)  
  
Reference: ISL Section 5.2 for a basic overview of the bootstrap.    

For the class exercises, you will need to refer to any basic explanation of the concept of value at risk (VaR) for a financial portfolio, e.g. [here](https://en.wikipedia.org/wiki/Value_at_risk), [here](http://www.investopedia.com/articles/04/092904.asp), or [here](http://people.stern.nyu.edu/adamodar/pdfiles/papers/VAR.pdf). 


R scripts and data:    
- [creatinine_bootstrap.R](./R/creatinine_bootstrap.R) and [creatinine.csv](data/creatinine.csv)   
- [portfolio.R](R/portfolio.R)  


Supplemental resources:  
- Lessons 8 and 9 of [Data Science in R: A Gentle Introduction](https://bookdown.org/jgscott/DSGI/)  
- [Section 2 of these notes](notes/decisions_supplement.pdf), on bootstrap resampling.  You can ignore the stuff about utility if you want.  


### (5) Clustering

Basics of clustering; K-means clustering; hierarchical clustering.  

Slides: [Introduction to clustering.](slides/05_clustering/05-clustering.pdf)      

Scripts and data:  
- [cars.R](R/cars.R) and [cars.csv](data/cars.csv) 
- [hclust_examples.R](R/hclust_examples.R)   
- [linkage_minmax.R](R/linkage_minmax.R)   
<!-- - [we8there.R](R/we8there.R)   -->  


Readings:  
- ISL Section 10.1 and 10.3 or Elements Chapter 14.3 (more advanced)    
- K-means++ [original paper](http://ilpubs.stanford.edu:8090/778/1/2006-13.pdf) or [simple explanation on Wikipedia](https://en.wikipedia.org/wiki/K-means%2B%2B).  This is a better recipe for initializing cluster centers in k-means than the more typical random initialization.


### (6) PCA

Principal component analysis (PCA).  

Slides: [Introduction to PCA](slides/06_PCA/06-PCA.pdf)      

Scripts and data for class:  
- [pca_intro.R](R/pca_intro.R)  
- [nbc.R](R/nbc.R), [nbc_showdetails.csv](data/nbc_showdetails.csv), [nbc_pilotsurvey.csv](data/nbc_pilotsurvey.csv)  
- [congress109.R](R/congress109.R), [congress109.csv](data/congress109.csv), and [congress109members.csv](data/congress109members.csv)  
- [ercot_PCA.R](R/ercot_PCA.R), [ercot.zip](data/ercot.zip)  


A few other examples we may or may not have time to cover in class:  
- [FXmonthly.R](R/FXmonthly.R), [FXmonthly.csv](data/FXmonthly.csv), and [currency_codes.txt](data/currency_codes.txt)    
- [NCI60.R](R/NCI60.R)   
- [gasoline.R](R/gasoline.R) and [gasoline.csv](data/gasoline.csv)   


Readings:  
- ISL Section 10.2 for the basics or Elements Chapter 14.5 (more advanced)  
- Shalizi Chapters 18 and 19 (more advanced).  In particular, Chapter 19 has a lot more advanced material on factor models, beyond what we covered in class.      



### (7) Networks and association rules  

Networks and association rule mining.  If time: spectral clustering.  

Slides: [Intro to networks](slides/Networks.pdf).  Note: these slides refer to "lastfm.R" but this is the same thing as "playlists.R" below.  

Some supplemental [slides on association rule mining.](slides/association_rules.pdf) These contain the details of the apriori algorithm.  If there's time we might cover some of this in class, but mainly we'll focus on the shorter intro slides above, together with the example R scripts below.     

Software you'll need:   
- [Gephi](https://gephi.org/), a great piece of software for exploring graphs  
- [The Gephi quick-start tutorial](https://gephi.org/tutorials/gephi-tutorial-quick_start.pdf)  

Scripts and data: 
- [medici.R](R/medici.R) and [medici.txt](data/medici.txt)  
- [playlists.R](R/playlists.R) and [playlists.csv](data/playlists.csv)  
- [microfi.R](R/microfi.R), [microfi_households.csv](data/microfi_households.csv), and [microfi_edges.txt](data/microfi_edges.txt).  

Supplemental resource: [In-depth explanation of the Apriori algorithm](http://www.rsrikant.com/papers/vldb94_rj.pdf)  



### (8) Text data

Co-occurrence statistics; naive Bayes; TF-IDF; topic models; vector-space models of text (if time allows).

Slides:  
- [Introduction to text](notes/text_intro.pdf).   
- [Introduction to Naive Bayes text classification](notes/naive_bayes_text.pdf)  

Scripts and data:  
- [congress109_bayes.R](R/congress109_bayes.R)  
- [tm_examples.R](R/tm_examples.R) and [selections from the Reuters newswire](https://github.com/jgscott/STA380/tree/master/data/ReutersC50)  
- [smallbeer.R](R/smallbeer.R) and [smallbeer.csv](data/smallbeer.csv)  


# netflix-1990s-analysis
Exploratory Data Analysis (EDA) of Netflix movies from the 1990s using Python, pandas, and matplotlib. Includes data cleaning, visualization, and insights for portfolio presentation.
Investigating Netflix Movies (1990s)

#Author: Hiba Derragui

#Project overview:

-This project performs exploratory data analysis (EDA) on Netflix titles to investigate movies released in the 1990s. The primary goals are:

1.Identify the most frequent movie duration in the 1990s.

2.Count the number of short Action movies released in the 1990s (short defined as duration < 90 minutes).

3.Provide additional descriptive analyses and visualizations (genre distribution, average duration by genre, yearly release trends, and top directors) to demonstrate data handling, EDA, and visualization skills.

-This repository contains the Jupyter Notebook Netflix_1990s_Analysis.ipynb with code, comments, and figures.

#Dataset

-Source: Kaggle dataset "netflix-titles" (commonly referenced as shivamb/netflix-shows).

-File used: netflix_titles.csv (place in the same folder as the notebook).

-Size and structure (dataset examined): 8,807 rows and 12 columns. Key columns used:

+show_id

+type (Movie or TV Show)

+title

+director

+cast

+country

+date_added

+release_year

+rating

+duration

+listed_in (renamed to genre)

+description

#Notes on cleaning:

-The duration column contains mixed formats (e.g., "90 min", "2 Seasons"). I extracted numeric minutes into a new numeric column duration_min for analysis of movies.

-listed_in was renamed to genre for clarity.

#Tools and environment:

-Programming language: Python 3.x

-Main libraries: pandas, numpy, matplotlib

-Recommended environment: Jupyter Notebook (local).

#Requirements file: requirements.txt (pandas, matplotlib, numpy)

#Methods and workflow:

-Load netflix_titles.csv into pandas DataFrame.

-Clean and normalize columns:

     + Rename listed_in to genre.

     + numeric duration values into duration_min.

-Filter dataset for entries where type == "Movie" and 1990 <= release_year <= 1999. Save the filtered DataFrame as nineties_movies.

-Compute required variables:

duration: the most frequent movie duration (mode of duration_min) — must be an integer.

short_movie_count: the number of Action movies in the 1990s with duration_min < 90.

-Produce extra visualization: top genres, average duration by genre, movies per year, top directors.

-Document findings and add conclusions.

#Core results:

Total 1990s movies analyzed: 241

Most frequent duration (variable duration): 94 minutes

Number of short Action movies (variable short_movie_count): 10

#Visualizations and interpretation:

-Top 10 Genres of 1990s Movies

X label: Genre; Y label: Count.

Interpretation:

Drama is the most frequent genre, with over 100 movies.

Comedy is the second most frequent, with around 80 movies.

International movies appear frequently (roughly 60–80 titles), indicating a strong international presence in Netflix’s 1990s catalog.

Action and Adventure have moderate representation (around 60 titles each).

Other genres in descending order include Romance, Thriller, Classics, Independent, Children & Family, and Sci-Fi & Fantasy.

Implication: The 1990s catalog is dominated by narrative-driven genres (Drama, Comedy, Romance), which reflects the cinematic focus of that era.

-Average Duration by Genre (Top 10)

X label: Genre; Y label: Average duration (minutes).

Interpretation:

International movies have the highest average duration, close to 130 minutes.

Music & Musicals average about 129 minutes.

Dramas average about 128 minutes.

Classics average about 123 minutes.

Romance averages around 120 minutes.

Other genres (Thrillers, Action & Adventure, Independent, LGBTQ+, Comedy) are slightly shorter but still generally above 100 minutes.

Implication: Most genres in the 1990s tended to produce full-length feature films (100+ minutes). Longer runtimes for international and music genres suggest emphasis on extended storytelling or performance recordings.

-Number of Movies Released Per Year (1990–1999)

X label: Year; Y label: Count.

Interpretation:

Year-to-year fluctuations are present.

Small drop between 1991 and 1992, then a rise until 1993, decline in 1994, rise in 1995, small dip in 1996.

Peak in 1997 with approximately 33–34 releases (the highest in the decade).

Slight decrease after 1997 and stabilization around 30–31 releases in 1998–1999.

Implication: The mid-to-late 1990s appear to be the most active period. This pattern could reflect production cycles and the increasing availability of international titles in Netflix’s catalog.

-Top 10 Directors with Most 1990s Movies

X label: Number of movies; Y label: Director names.

Interpretation:

One director (listed as "Johnnie to" in the dataset) leads the list with 4 movies.

Several directors each have 3 movies: Gregory Hoblit, Rajkumar Santoshi, Phillip Noyce, Mahesh Bhatt, Youssef Chahine, Subhash Ghai, Sooraj R. Barjatya, Umesh Mehra.

Paul W.S. Anderson appears at the lower end among the top 10 with 2 movies.

Implication: A small group of directors are responsible for several entries in the 1990s Netflix collection, showing concentration by certain filmmakers; this can be useful when studying authorship or era-specific curation.

#summary:

-The 1990s movies subset contains 241 titles in the dataset.

-The most common runtime is 94 minutes, reflecting the typical feature-length standard of that decade.
There are 10 short Action movies (under 90 minutes), confirming that most Action films from the 1990s were full-length productions.

-Genre analysis shows that Drama and Comedy dominate the catalog, while International Movies, Action, and Adventure genres also appear prominently.
Average durations are notably high across genres—most are longer than 100 minutes—with International Movies, Music & Musicals, and Dramas among the longest on average.
This indicates that 1990s cinema emphasized rich storytelling and longer narrative structures typical of that era.

-Yearly release counts peak around 1997, marking the most active production period of the decade.
Although the number of movies fluctuates slightly between years, the overall trend shows a steady increase in the mid-to-late 1990s, suggesting a growing film output and broader international inclusion in Netflix’s 1990s catalog.

-Director analysis reveals that a small group of filmmakers were particularly active during this decade.
Directors such as Johnnie To, Gregory Hoblit, Rajkumar Santoshi, Philip Noyce, and Mahesh Bhatt appear frequently, with Johnnie To standing out as the most prolific director, contributing four movies.
This shows that Netflix’s 1990s movie selection highlights both mainstream and international directors with multiple influential works.

-Overall, the analysis demonstrates that 1990s films on Netflix are largely story-driven, feature-length productions, showcasing strong representation of Drama and Comedy, a growing international presence, and contributions from several prominent directors.
These findings highlight the narrative depth, diversity, and cinematic style of the 1990s and showcase practical skills in data cleaning, filtering, aggregation, visualization, and interpretation using Python, pandas, and matplotlib.

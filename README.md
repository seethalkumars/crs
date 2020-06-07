# CouReco :mortar_board:
Building a Simple Course Recommendation system for online courses

## About the Project
CouReco is a minimalistic system built on the idea to help learners navigate through the courses on Coursera, aided by a data-driven strategy. Currently, CouReco only performs the task of identifying the most similar and most dissimilar courses to a selected course that is chosen by the learner from a pool of courses relevant to the skills the learner is interested in.  
  
*NOTE: This is a personal project initiated with the author's requirement for an end-to-end data science project that could help learn the skills of creating a dataset through web scraping, deploying a web-app via [Streamlit](https://www.streamlit.io/) and a basic primer into content-based recommendation systems. Though this tool makes reasonable recommendations as of now, it is far from being "intelligent". However, you could download this repo and work on it and make it "smarter"!* :smile: 
 

## Dataset Used
For the purpose of building CouReco, data from Coursera was scraped using the requests and beautifulsoup4 libraries. The ```scraper.py``` file contains code for scraping data from [https://www.coursera.org/courses](https://www.coursera.org/courses) and generates [coursera-courses-overview.csv](https://github.com/ry05/couReco/blob/master/data/coursera-courses-overview.csv). The ```course_scraper.py``` file contains code to scrape details of each individual course and the output is [coursera-individual-courses.csv](https://github.com/ry05/couReco/blob/master/data/coursera-individual-courses.csv).  

Both these above datasets have been combined to give [coursera-courses.csv](https://github.com/ry05/couReco/blob/master/data/coursera-courses.csv). This file consists of 1000 instances and 14 features and has a size of 1.41 MB.

### Features in the Dataset
The following features have been extracted for the dataset created above:  
  
**course_url:** The URL to the course homepage  
**course_name:** The name of the course  
**learning_product:** The type of product that the instance is. It can be a course, professional certificate or a specialization. *(While all instances of the dataset are referred to as courses , this is not be confused with the learning_product of a particular instance)*  
**course_provided_by:** The organization/partner that is providing the course  
**course_rating:** Overall rating of the course  
**course_rated_by:** The number of students who have rated the course  
**enrolled_student_count:** The number of learners who have enrolled into this course  
**course_difficulty:** The difficulty level of the course. It can take values of beginner, intermeditae, advanced and mixed  
**skills:** The main skills that the course works at developing in a learner  
**description:** About the course  
**percentage_of_new_career_starts:** Percentage of learners who have had a new career start after completing this course  
**percentage_of_pay_increase_or_promotion:** Percentage of learners who have had a pay increment or received a promotion after completing this course  
**estimated_time_to_complete:** The estimated tome to complete the course  
**instructors:** The instructors taking the course  

## Usage
The instructions to run CouReco on your local system are as follows:

1. Create a virtual enviornment on your local system to install this project's dependencied and run it
2. Download or clone this repository into your virtual environment
3. Run the following command to install necessary libraries for CouReco to run
  ```
  pip install -r requirements.txt
  ```
4. Run the streamlit app with
  ```
  streamlit run recommender.py
  ```
5. The app should open at http://localhost:8501

## What can CouReco do?
CouReco is a minimalistic system built with an idea to help learners navigate through the courses on Coursera, aided by a data-driven strategy. A learner should ideally be able to visualize different features provided in the dataset or interact with this app to find suitable courses to take based on what they have already learnt. However, in this inchoate stage t

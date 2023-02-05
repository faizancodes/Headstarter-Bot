# Headstarter-Bot
Documentation on the Headstarter Discord Bot

## Contents
  - [Commands Available](#Commands-Available)
  - [Video Demo](#Video-Demo)
  - [Examples](#Examples)
  - [How it Works](#How-It-Works)


## Commands Available
  - `/resume_score` : See how well your resume matches with different job positions, allows you to quantify your resume and be able to track how changes to your resume affects how well you match different jobs

  - `/job-match` : See how well your resume matches with a specified job description, this command compares the contents of your resume to the contents of a job description and calculates a match score based on the similarities in the text 

  - `/improve-resume` : This command suggests improved bullet points that you can put on your resume, based on the job position you are aiming for and the experiences you have on your resume  

  - `/tailor-resume` : This command ouputs a set of tailored bullet points that you can add to your resume, based on the job description you input

  - `/generate-cover-letter` : This command generates a cover letter for a specified job position based on the experiences on your resume 
  
## Video Demo
https://user-images.githubusercontent.com/43652410/216802677-96efff71-6241-465b-b8ab-ec25524e0554.mp4

  
## Examples
  
  - `/resume_score`
  <img width="342" alt="Screenshot 2023-02-04 at 11 54 23 PM" src="https://user-images.githubusercontent.com/43652410/216802371-9ca1fa42-d5f3-4785-897b-bc446719d5a1.png">
  
  
  - `/job_match`
<img width="410" alt="Screenshot 2023-02-04 at 11 56 16 PM" src="https://user-images.githubusercontent.com/43652410/216802418-9396972f-51fc-4622-b77c-89adc8814263.png">

  - `/improve_resume`
  <img width="614" alt="Screenshot 2023-02-04 at 11 56 54 PM" src="https://user-images.githubusercontent.com/43652410/216802438-e0315dc3-c648-4d7f-b96f-e6fcbe21dcc9.png">
  
  - `/tailor_resume` 
<img width="616" alt="Screenshot 2023-02-04 at 11 59 21 PM" src="https://user-images.githubusercontent.com/43652410/216802593-808953f2-1bde-4f9e-9c3d-f64da77b2e87.png">

  - `/generate_cover_letter` 
<img width="603" alt="Screenshot 2023-02-05 at 12 29 44 AM" src="https://user-images.githubusercontent.com/43652410/216803401-ac7fec0a-4807-4750-b1a0-722e0096c370.png">


## How it Works
  
  - `/resume_score`
  
    - This bot utilizes ensembles of NLP models I trained on 4000+ different tech jobs to be able to accurately match resumes to specific job positions. 
      These job positions include:

        - Software Engineer
        - Data Scientist
        - Data Analyst
        - Data Engineer
        - Product Manager
        - Security Engineer 
        - Network Engineer
        - UI/UX Designer
        - Technical Consultant 
        - Penetration Tester
        - Information Security Analyst 

    When the bot extracts all the text from your resume, it is fed to the NLP models to classify what job position text matches to. 
    The output of the NLP models is an array of values which represent the probability of the resume text matching to a specific job from the list above, and the array of values sum to 100. So when using the `/resume_score` command, you see the top 5 job positions you match to and your corresponding match scores. 

    - **Match Scores above 65 can be considered a good match and means that your resume is well suited towards that particular job.** Anything less than a value of 50 means your resume needs significant improvement. Using the other commands such as `/improve_resume` and `/tailor_resume` can be used to reach a match score above 65. 
    
    - The true utility of this command is shown when used several times after implementing changes to your resume. After every change you make to your resume, this command can be used to quantify any improvements - it can be used as a tool to see how much your resume actually improved.  

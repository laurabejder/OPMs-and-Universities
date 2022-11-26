
## Contents of the repository


The FOIA 

## Data Diary

This document explains the process of data collection and data cleaning of this project.

The original dataset was aquired from this GitHub repository: 

https://github.com/HigherEdData/Outsourcing-Online-Education 

The file [filename] is based on their dataset but we have collected new rounds of data which are also included in the file. 

We filed a new round of FOIA requests to the universities in the original data and as a result of the responses, we have added new partnerships between universities and online program managers. 

### Updating the data
We have updated the invisibility meassurement. 

    0 - no mention of the partnership on University program website, may have 1 press release 
        from the provost, head of university, etc when the partnership began, but definitely 
        not clear to potential students. You would need to specifically look up key terms 

    1 - Mentioned somewhere on the university website, but not clear that there is an external 
        partnership in place "available but not accessible"

    2 - Partnership is clear on the university program’s website, clear differentiation between
        the university and an external tool


### Cleaning the data
We decided to narrow the sample to contracts that are still active or expired later than 2019. We did so to ensure that the project only include recent partnerships – and exclude contracts that expired years or decades ago. By doing so we drop 104 partnerships. 

We also exclude partnerships where the online program manager only provides an online learning platform - known as Learning Program Managers (LMS) to make the cases in the sample more comparable. The LMS are coded as -999 in the invisibility column. 
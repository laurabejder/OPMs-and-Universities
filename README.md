
## Contents of the repository

- **FOIA-2019:** Contracts between schools and OPMs collected by the Century Foundation before 2022. 
- **FOIA-2022:** Contracts between schools and OPMs collected through FOIA requests to the schools in the fall of 2022



| Header         | Definition |
|----------------|------------|
|`partnership_id`|Speficic numeric id for each partnership|

## Methodology

This document explains the process of data collection and data cleaning of this project.

### Data aquisition
The original dataset was aquired from this GitHub repository: 

https://github.com/HigherEdData/Outsourcing-Online-Education 

The file [filename] is based on their dataset but we have collected new rounds of data which are also included in the file. 

A new round of FOIA  requests was filed to the universities in the original data and as a result of the responses, new partnerships between universities and online program managers were added to the data. 

### Updating the data

updating the data as we receive new responses to our FOIA requests – contracts that are extentet or renewed. 
- new expiration dates, new contract content, new contracts added.

#### Updated invisibility meassurement
We have updated the invisibility meassurement. 

WHERE DID WE FIND THE INFORMATION AND HOW DID WE FIND IT?
ADD DATES FOR DATA COLLECTION! 

    0 - There is no mention of the partnership on University program website, may have 1 press 
        release from the provost, head of university, etc when the partnership began, but definitely 
        not clear to potential students. You would need to specifically look up key terms 

    1 - The partnership is mentioned somewhere on the university website, but not clear that 
        there is an external partnership in place "available but not accessible".

    2 - The partnership is clear on the university program’s website, clear differentiation between
        the university and an external tool


### Cleaning the data
The sample includes to contracts that are still active or expired later than 2019. Contracts that expired before that are excluded to ensure that the project only include recent partnerships. By doing so, we drop 104 partnerships. 

We also exclude partnerships where the online program manager only provides an online learning platform - known as Learning Program Managers (LMS) to make the cases in the sample more comparable. The LMS are coded as -999 in the invisibility column. As a result, we drop 37 partnerships.
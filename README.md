
## Contents of the repository

- `FOIA-2019`: Contracts between schools and OPMs collected by the Century Foundation before 2022. 
- `FOIA-2022`: Contracts between schools and OPMs collected through FOIA requests to the schools in the fall of 2022
- `data.csv`: Data on the partnerships including name of the university/college, OPM, invisitibility meassure and start and end dates for the contracts. See variable description below.
- `contact_content.csv`: Descriptions of the content of each contract. See variable description below. Only invisible partnerships are included.

`data.csv`

| Header         | Definition |
|----------------|------------|
|`partnership_id`|Unique numeric id for each partnership.|
|`institution`   |Name of the university or college.|
|`provider`      |Name of the OMP company.|
|`invisibility`  |Numeric score (0-2) of the invisibility of the partnership on the university/college's website. -999 means that the OPM provides an online learning platform.|
|`start_month`   |The start month of the first contract.|
|`start_year`    |The start year of the first contract.|
|`term_primary_contract`|The lenght of the first contract. 888 mean that the contract remains effective or is automatically renewed until terminated by one of the parties.|
|`last_start_year`|The start year for the lastest contract.|
|`end_date_last_contract`|The expiration year for the latest contract.|

`contact_content.csv`

| Header         | Definition |
|----------------|------------|
|`partnership_id`|Unique numeric id for each partnership.|
|`institution`   |Name of the university or college.|
|`provider`      |Name of the OMP company.|
|`2019_contract`  |Yes/No to whether the database includes a contract aquired by the Century Foundation. If yes, it can be found in the `FOIA-2019` directory.|
|`2022_contract`   |Yes/No to whether the database includes a contract aquired by Columbia. If yes, it can be found in the `FOIA-2022` directory.|
|`2019_contract_content`|Summary of the content of the 2019 contract.|
|`2022_contract_content`|Summary of the content of the 2022 contract.|
|`keywords`|Keywords categorizing the content of the contract: course development, course content, course material, course instruction, revenue share, academic support, recruitment, marketing, software, tutoring.|
|`price_per_year`|If the payment is a fixed amount, the yearly price is listed.|
|`revenue_share`|If the payment is a revenue share agreement, the companies share (in percent) is listed.|
|`programs_courses`|Specifict programs/courses included in the partnership, if they are listed in the contract.|

## Methodology

This document explains the process of data collection and data cleaning of this project.

### Data aquisition
The original data was collected by Heather Daniels, Christian Smith, Laura T. Hamilton, and Charlie Eaton from the University of California, Merced. It can be aquired from [this GitHub repository](https://github.com/HigherEdData/Outsourcing-Online-Education). 

The file `data.csv` is based on their dataset but we have collected new rounds of data which are also included in the file. 

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
The sample includes to contracts that are still active or expired later than 2019. Contracts that expired before that are excluded to ensure that the project only include recent partnerships. By doing so, 104 partnerships were dropped. 

Partnerships where the online program manager only provides an online learning platform - known as Learning Program Managers (LMS) – were excluded to make the cases in the sample more comparable. The LMS are coded as -999 in the invisibility column. As a result, 37 partnerships were dropped.
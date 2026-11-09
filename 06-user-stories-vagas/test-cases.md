# Test cases para as user stories — Vagas.com

23 casos de teste derivados dos critérios de aceite (AC) das 6 user stories, cada um com prioridade. Conteúdo original em inglês.

### User story 1

> As a candidate, I want to choose a technical test related to my field so that I can demonstrate my skills before applying for a job.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The candidate can view a list of available tests based on their field of expertise. | | |
| TC001 | Verify that the list of technical tests is displayed correctly based on the candidate’s field. | Critical |
| *AC:* The candidate can select a test and start when ready. | | |
| TC002 | Ensure that a candidate can successfully select and start a test. | Critical |
| *AC:* The system displays a time limit for completing the test. | | |
| TC003 | Validate that a time limit is displayed during the test. | Medium |
| *AC:* The test is available only for registered candidates. | | |
| TC004 | Only logged in users should be able to start a test. | Critical |

### User story 2

> As a candidate, I want to receive a performance report on the technical test so that I can understand my strengths and areas for improvement.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The system generates a report with the candidate’s score and feedback after completing the test. | | |
| TC005 | Check that a report is generated with scores and feedback after test completion. | Critical |
| *AC:* • Correct and incorrect answers are highlighted.<br> • Improvement suggestions are provided for incorrect answers. | | |
| TC006 | Validate that correct and incorrect answers are highlighted with improvement suggestions. | Medium |
| *AC:* The candidate can view the report in the “My Tests” section. | | |
| TC007 | Verify that candidates can access reports in the ‘My Tests’ section. | Critical |
| *AC:* The candidate cannot retake the test before the specified waiting period. | | |
| TC008 | The test should not be retaken before the specified waiting period. | Critical |

### User story 3

> As a recruiter, I want to see candidates’ technical test results so that I can evaluate their skills before scheduling interviews.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The recruiter can view the candidate’s test results on their profile. | | |
| TC009 | Verify that recruiters can see test results in a candidate’s profile. | Critical |
| *AC:* The candidate’s test scores and proficiency levels (beginner, intermediate, advanced) are displayed correctly. | | |
| TC010 | Ensure that test scores and proficiency levels are displayed correctly. | Medium |
| *AC:* Recruiters can filter candidates based on specific tests completed. | | |
| TC011 | Check that recruiters can filter candidates by relevant test completion. | High |
| *AC:* The recruiter cannot view the test results of candidates without proper permissions. | | |
| TC012 | Attempt to view test results of a candidate without proper permissions. | Critical |

### User story 4

> As a candidate, I want to opt into the Talent Pool so that companies can find me even if I haven’t applied for a specific job.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The candidate can opt in or out of the Talent Pool from their profile settings. | | |
| TC013 | Verify that candidates can opt in and out of the Talent Pool. | Critical |
| *AC:* Only profiles that have been updated within the last 30 days are included in the Talent Pool. | | |
| TC014 | Check that only updated profiles are included in the Talent Pool. | Medium |
| *AC:* Candidates receive notifications when a recruiter views their profile. | | |
| TC015 | Ensure that candidates receive notifications when their profile is viewed. | High |
| *AC:* Candidates with outdated profiles are not allowed to access the Talent Pool feature. | | |
| TC016 | Attempt to access the Talent Pool feature without an updated profile. | Critical |

### User story 5

> As a recruiter, I want to access a talent pool filtered by skills and experience so that I can quickly find qualified candidates.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The recruiter can search for candidates using keywords, skills, and experience. | | |
| TC017 | Verify that the recruiter can search for candidates using keywords, skills, and experience. | Critical |
| *AC:* The system suggests candidates who match an open position. | | |
| TC018 | Ensure that the system suggests candidates who match an open position. | Critical |
| *AC:* The suggested profiles include relevant information, such as completed technical tests and availability. | | |
| TC019 | Validate that suggested profiles include relevant information such as completed technical tests and availability. | High |
| *AC:* The recruiter can save interesting profiles for future opportunities. | | |
| TC020 | Check that the recruiter can save interesting profiles for future opportunities. | Medium |

### User story 6

> As a candidate, I want to receive notifications when a job that matches my profile is posted so that I can increase my chances of getting hired.

| AC / ID | Summary | Priority |
|---|---|---|
| *AC:* The candidate receives notifications via email or on the platform about new relevant job openings. | | |
| TC021 | Verify that the candidate receives notifications via email or on the platform about new relevant job openings. | Critical |
| *AC:* The candidate can adjust their notification preferences. | | |
| TC022 | Ensure that the candidate can adjust their notification preferences. | High |
| *AC:* The system recommends jobs based on the candidate’s profile and completed technical tests. | | |
| TC023 | Validate that the system recommends jobs based on the candidate’s profile and completed technical tests. | Critical |

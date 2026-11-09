# Test Report — Huntd

> Conteúdo do relatório original (planilha) em inglês, reorganizado em Markdown.

## Project information

| Item | Value |
|---|---|
| Project name | Huntd (https://huntd.tech/) |
| Product | The best app for hiring web3 developers. |
| Mission | Conduct testing to verify the quality of the web and mobile application. Ensure the application is released without defects. |
| Output | Test Summary report and Defects evaluation |
| Project type | Testing |
| Duration | 2026-09-22 → 2026-09-25 |

**Product description.** Huntd is a comprehensive job search and application tracking app designed to assist job seekers in their quest for employment. With its user-friendly interface and powerful features, this app is essential for individuals actively seeking job opportunities.

## Test objectives

The test objectives are the functionality of the web version and mobile version of the “Huntd”. The project focuses on the possibility to interact with the main objects of the website and app.

- For Website the main objectives are to verify the functionality of user registration, authentication, candidate and recruiter profiles, candidate search and filtering, job vacancies, Web3 companies, chats, navigation, permissions and other implemented web features according to the specified requirements.
- For Mobile the main objectives are to verify the functionality of the implemented mobile features, including authentication, profile settings, chat functionality and other available features according to the implemented application requirements.

## Execution summary

| App | Executed | Passed | Failed | Pass rate |
|---|---|---|---|---|
| Web | 129 | 123 | 6 | 95.3% |
| Mobile | 26 | 26 | 0 | 100% |

### Web — results by feature

| No. | Feature | Tests | Passed | % Passed | Failed | % Failed |
|---|---|---|---|---|---|---|
| 1 | Main Page | 8 | 7 | 87.5% | 1 | 12.5% |
| 2 | For Companies | 6 | 6 | 100% | 0 | 0% |
| 3 | For Engineers | 8 | 7 | 87.5% | 1 | 12.5% |
| 4 | Authentication / Registration | 7 | 7 | 100% | 0 | 0% |
| 5 | Candidates | 17 | 17 | 100% | 0 | 0% |
| 6 | Candidate Profile | 31 | 28 | 90.3% | 3 | 9.7% |
| 7 | Recruiter Profile | 6 | 6 | 100% | 0 | 0% |
| 8 | Jobs | 19 | 19 | 100% | 0 | 0% |
| 9 | Chats / Messages | 15 | 14 | 93.3% | 1 | 6.7% |
| 10 | Bonus | 4 | 4 | 100% | 0 | 0% |
| 11 | Footer | 8 | 8 | 100% | 0 | 0% |
| | **Total** | **129** | **123** | **95.3%** | **6** | **4.7%** |

### Mobile — results by feature

| No. | Feature | Tests | Passed | % Passed | Failed | % Failed |
|---|---|---|---|---|---|---|
| 1 | Login / Authentication | 8 | 8 | 100% | 0 | 0% |
| 2 | My Chats | 7 | 7 | 100% | 0 | 0% |
| 3 | Profile | 6 | 6 | 100% | 0 | 0% |
| 4 | Preferences | 4 | 4 | 100% | 0 | 0% |
| 5 | Sign Out | 1 | 1 | 100% | 0 | 0% |
| | **Total** | **26** | **26** | **100%** | **0** | **0%** |

### Web bugs by priority (Jira)

| Priority | Bugs | % |
|---|---|---|
| Critical | 0 | 0% |
| High | 3 | 37.5% |
| Medium | 5 | 62.5% |
| Low | 0 | 0% |

## Test report

The testing activities covered the implemented web and mobile features of Huntd. Web testing included 129 test cases, with 123 passed and 6 failed, resulting in a 95% pass rate. Mobile testing included 26 test cases, with 26 passed and 0 failed, resulting in a 100% pass rate. A total of 8 defects were identified and reported in Jira for the web application. No defects were identified during mobile testing.

## Test conclusion

The planned test cases were executed for both web and mobile applications. The identified defects were documented in Jira and linked to the corresponding TestRail results. The Test Summary provides the detailed execution statistics and defect distribution.





<h1  align="center">Google Summer of Code 2024 <img  src="https://media0.giphy.com/media/u2pmTWUi0MXjyrMaVj/giphy.webp?cid=ecf05e47s80k4ssg3a6cqwqs6j8hxyctvqtlw7oywfnoajuo&ep=v1_gifs_search&rid=giphy.webp&ct=g"  width="30"></h1>

  

<p  align="center"><i>A full report on my Google Summer of Code 2024 work with FOSSology</i></p>

<p  align="center"><i>Project: "REST API Improvements" </i> 👨‍💻</p>

  

<p  align="center">

<img  src="https://media0.giphy.com/media/u2pmTWUi0MXjyrMaVj/giphy.webp?cid=ecf05e47s80k4ssg3a6cqwqs6j8hxyctvqtlw7oywfnoajuo&ep=v1_gifs_search&rid=giphy.webp&ct=g"  width="20">

</p>

  

<div align = "center">
    <img src="https://github.com/user-attachments/assets/94976eda-9d37-4bbe-862a-154984209d8a"/>
</div>

  

<h3 align="center"><a href="#project-details">Table of contents</a></h3>


<p align="center">
	<a href="#project-details">Project Details</a> | 
	<a href="#contributions">Contributions</a> | 
	<a href="#documentation">Documentation</a> | 
	<a href="#deliverables">Deliverables</a> | 
	<a href="#major-takeaways">Major Takeaways</a> |
    <a href="#acknowledgements">Acknowledgements</a> |
    <a href="#future-ventures">Future ventures</a>
</p>
<!-- /TOC -->

 
<!--**About me** -->



<!--Hello, I'm **Valens NIYONSENGA**, a graduate in Software Engineering, Cybersecurity, and Embedded Systems from Rwanda Coding Academy. Over the past three years, I’ve had the opportunity to dive deep into building and designing full-stack applications. Being part of the FOSSology community through Google Summer of Code 2024 is something I’m really excited about.-->

<!--This article is a detailed report of my contributions, documenting the progress I’ve made during my 12 weeks of coding with FOSSology as part of GSoC 2024.-->

<h1 align = "center" id = "project-details">📝 Project Details</h1>


## Overview

<p align="justify">
This project aims to address the need for improving and upgrading APIs on FOSSology to version 2 by identifying areas for enhancement, fixing issues, and ensuring that clients using V1 aren't affected. To solve this, There are three main objectives to focus on. First, enhancing existing APIs by adding missing features for comprehensive implementation. Second, upgrading REST APIs to version 2, fixing bugs, and adopting new design patterns for efficient functionality. Additionally, any new endpoints added will adhere to Version 2 standards. My plan includes quality assurance measures, such as unit and integration testing, to ensure all requirements are met satisfactorily. Overall, my goal is to improve the usability and effectiveness of FOSSology's APIs for a better user experience.
</p>

## Milestones and Tasks

### Milestone 1: Enhance the existing unit test coverage for APIs

- Enhance Unit Tests for `/folder`, `/group`, `/license`, `/upload` endpoints.
- Enhance Unit Tests for `/maintenance`, `/upload_tree`, `/info` endpoints.

### Milestone 2: Complete upgradation & improvement of all endpoints' tests to veersion 2.

- Upgrade & Improve `/folder`, `/group`, `/info`,`overview`,`job`,`copyright` tests.
- Upgrade & Improve `/license`, `/maintenance`, `/upload`, `/user` tests.

### Milestone 3: Complete addition of new Unit tests for all endpoints

- Add Unit Tests for `/upload`, `/folder`, `/group`, `/license` endpints.
- Add Unit Tests for `/maintenance`, `/copyright`, `/overview`, `/report`,`/job` endpoints.

### Milestone 4: Complete addition of  Unit tests for all models

- Add Unit Tests for `upload`, `folder`, `group`, `scanCode`,`GroupPermissions`, and `UploadSummary` models.
- Add Unit Tests for `UserGroupMember`, `Job`, `BulkHistory`, `Analysis`, and `ApiVersion` models.
- Add Unit Tests for `agent`, `decider`, `fileInfo`, `group`,`licenseCandidate`, and `permissions` models.

### Milestone 5: Complete addition of  integration tests for Data Acess Objects (DAOs)

- Add integration Tests for `folder`, `agent`, and `pfile` DAOs.
- Add integration Tests for `license`, `upload`, `uploadPermssions`, and `showJobs` models.
<br />
</br />

<h1 align = "" id = "contributions">🌏 Contributions</h1>

  
During my participation in the Google Summer of Code (GSoC) program, I focused on enhancing the quality of the system by improving and adding new unit and integration test cases.Through this, I tested all functionalities to verify whether they work as expected and meet the requirements. After finishing unit test cases development for APIs and models, I tackeled integration tests for Data Access Objects (DAOs).

1.  #### Unit tests development
 
- I developed new unit test cases for all controllers and models contributing to the quality improvement of the software, verifying that API units and models are working as expected.
2.  #### Api test cases upgrade to version 2
- Since my collegue [Divij](https://github.com/dvjsharma) was upgrading REST APIs to version 2, the same to my side, I dedicate my time to upgrade all test cases to version 2.

3.  #### Integration tests development
- Finally, After improving and enhancing some integration tests that were available in Data Access Objects (DAOs), I developed new integration test cases verifying that all DAOs components and database are properly working together to meet the requirements as expected.


## Unit test cases development:

  ### 1.Controllers.
  - Upgraded different tests including `MaintenanceControllerTest`,`LicenseControllerTest`, `GroupControllerTest`, `CopyrightsControllerTest`,`UploadControllerTest`, and `UserContollerTest` to support version 2 specification [#2826](https://github.com/fossology/fossology/pull/2826)
   <br />
   <br />
  - Added `MaintenanceControllerTest`, and `UploadTreeControllerTest`. [#2764](https://github.com/fossology/fossology/pull/2764)
  <br />

    `MaintenanceControllerTest`

   I added more than 5 test cases to ensure that maintenance functionalities work as expected.

  ![image](./assets/maintenance.png) 

    `UploadTreeControllerTest`

      - Improved up to 30 test cases, checking whether they work propery and meet the expected needs.
      - Added 16 more test cases, making sure that all APIs in UploadTreeControllerTest are covered.
      - Checked and verified that the UploadTree API works as expected and meets the requirements.

  ![image](./assets/upload_tree.png)

    - `LicenseControllerTest`, `GroupControllerTest`, `CopyrightsControllerTest`,`UploadControllerTest`, and `FolderControllerTest` [#2827](https://github.com/fossology/fossology/pull/2827) and [#2834]https://github.com/fossology/fossology/pull/2834
  <br />

    `LicenseControllerTest`

      - Improved up to 19 test cases in LicenseControllerTest, checking whether they work propery and meet the expected needs.
      - Added more than 31 new test cases, making sure that all APIs in LicenseController are covered.
      - Checked and verified that the Upload API works as expected and meets the requirements.

  ![image](./assets/license.png) 

    `UploadControllerTest`

      - Improved up to 30 test cases, checking whether they work propery and meet the expected needs.
      - Added more than 16 new test cases, making sure that all APIs in UploadController are covered.
      - Checked and verified that the Upload API works as expected and meets the requirements.

  ![image](./assets/upload_controller.png)

    `FolderControllerTest`

      - Improved up to 20 test cases, checking whether they work propery and meet the expected needs.
      - Added up to 10 new test cases, making sure that all APIs in FolderController are covered.
      - Checked and verified that the Folder API works as expected and meets the requirements.

  ![image](./assets/folder_controller.png)

    `GroupControllerTest`

      - Improved up to 8 existing test cases, checking whether they work propery and meet the expected needs.
      - Added up to 17 new test cases, making sure that all APIs in GroupController are covered.
      - Checked and verified that the Group API works as expected and meets the requirements.

  ![image](./assets/group.png)

   `CopyrightsControllerTest`

      - Initiated the test and added up to 20 new test cases, making sure that all APIs in CopyrightsController are covered.
      - Checked and verified that the Copyrights API works as expected and meets the requirements.

  ![image](./assets/Copyright.png) 

#### Models test cases.
Models tests are numerous but I would like to show some screenshoots.
 - `AnaysisTest`, `BulkHistroryTest`, `ScanCodeTest`, `FolderTest` and so on.. [#2825](https://github.com/fossology/fossology/pull/2825)
  <br />

  `AnaysisTest`

      - Improved up to 5 existing test cases, checking whether member variables and methods in Analysis model work as expected and meet the requirements.
      - Added up to 11 new test cases, making sure that all member variables and methods in Analysis model are covered.
      - Checked and verified that the Analysis model works as expected and meets the requirements.

  ![image](./assets/models/analysis.png) 

  `ScanCodeTest`  

      - Created the test and introduced up to 5 new tests, making sure that all member variables and methods in ScanCode model are covered.
      - Checked and verified that the ScanCode model works as expected and meets the requirements.

  ![image](./assets/models/scancode.png)

  `BulkHistroryTest`

      - Created the test and introduced up to 8 new tests, making sure that all member variables and methods in BulkHistrory model are covered.
      - Checked and verified that the BulkHistrory model works as expected and meets the requirements.

  ![image](./assets/models/history.png) 

  `FolderTest`

      - Improved 1 test case that was existing.
      - Added up to 5 new test cases, making sure that all member variables and methods in Folder model are covered.
      - Checked and verified that the Folder model works as expected and meets the requirements.

  ![image](./assets/models/folders.png)

   - `LicenseCandidateTest`, `AgentTest`, `DeciderTest`,and so on.. [#2829](https://github.com/fossology/fossology/pull/2829)
  <br />
  `LicenseCandidateTest`

      - Created the test model and introduced up to 13 new tests, making sure that all member variables and methods in LicenseCandidate model are covered.
      - Checked and verified that the LicenseCandidate model works as expected and meets the requirements.

  ![image](./assets/models/lisence_candidate.png) 

  `AgentTest`

      - Created the test model and introduced up to 13 new tests, making sure that all member variables and methods in Agent model are covered.
      - Checked and verified that the Agent model works as expected and meets the requirements.

  ![image](./assets/models/agent.png)

  `DeciderTest`

      - I enhanced up to 4 tests that were existing.
      - I added up to 2 new tests, making sure that all member variables and methods in Decider model are covered.
      - Checked and verified that the Decider model works as expected and meets the requirements.

  ![image](./assets/models/decider.png) 

## Integration test cases development.
   - `FolderDAOTest` [#2830](https://github.com/fossology/fossology/pull/2830)
  <br />
  `FolderDAOTest`

      - I enhanced up to 16 tests that were existing.
      - I added up to 13 new tests, making sure that all member variables and methods in FolderDao model are covered.
      - Checked and verified that the integration between Database, FolderDao and other components work as expected and meets the requirements.

  ![image](./assets/daos/folder.png) 

   - `PfileDAOTest`, `ShowJobsDAOTest`,`UploadPermissionsDAOTest`, `UploadDATest` and so on.. [#2832](https://github.com/fossology/fossology/pull/2832)
  <br />

    `UploadPermissionsDAOTest`

      - I enhanced and added new test cases, making sure that all member variables and methods in UploadPermissionsDAO model are covered.
      - Checked and verified that the integration between Database, UploadPermissionsDAO and other components work as expected and meets the requirements.

  ![image](./assets/daos/upload_permissions.png) 

    `PfileDAOTest`

      - I enhanced and added new test cases, making sure that all member variables and methods in PfileDAO model are covered.
      - Checked and verified that the integration between Database, PfileDAO and other components work as expected and meets the requirements.

  ![image](./assets/daos/pfile1.png) 
   ![image](./assets/daos/pfile2.png) 

    `ShowJobsDAOTest`

      - I enhanced and added new test cases, making sure that all member variables and methods in ShowJobsDAO model are covered.
      - Checked and verified that the integration between Database, ShowJobsDAO and other components work as expected and meets the requirements.

  ![image](./assets/daos/showjobs1.png) 
  ![image](./assets/daos/showjobs2.png) 
  
  
<h1 align = "" id = "documentation">Documentation:📄</h1>


Throughout the 12 weeks of the GSoC period, I created weekly documentation for recording and tracking my progress. The documentation can be found [**here**](https://fossology.github.io/gsoc/docs/2024/rest/updates/valens/2024-05-30)


<h1 align="center" id="deliverables">👨🏻‍🏫 DELIVERABLES <img src="https://api.ezeelo.com/Scripts/QRCode/Done.gif" width="40"></h1>

| Tasks   | Planned | Completed     | Remarks    |
| :---:       |    :----:   |    :---:      |    :---:      |
| Upgrade and Improve all REST API unit tests | Yes | :heavy_check_mark: | 
| I have improved and added new unit tests for APIs | Yes       | :heavy_check_mark: |  |
| Enhanced and added new unit tests for models| Yes        | :heavy_check_mark:  |  |
| Improved and added new integration tests for Data Access Objects| Yes | :heavy_check_mark:(partially) | There's still a work ahead to ensure that all the DAOs follow integration testing standards and also making sure that the test coverage for each is at least 75%. |
| Adding end-to-end tests for APIs | NO  | :x: | I am going to finalize this in coming weeks after GSoC.

<h1 align = "" id = "future-ventures">Future ventures🚀</h1>


- #### Implement end-to-end tests for FOSSology APIs:
   To ensure high quality software, there is still a work to do. I look forward to finalizing additional end-to-end tests development for FOSSology APIs to verify that all functionalities are working as expected and meeting the requirements.
In the pipeline are several exciting improvements to look forward to:

- #### Guiding new contributors to FOSSology:
   I look forward to providing a full guidance new contributors for not only contributing to FOSSology Excellence in license compliance but also broadening the open-source family.
- #### Provide more contributions:
   As I started the open-source journey, I won't step back.I will keep my dedication , determination and love to open-source. I will keep contributing to FOSSology, guiding and mentoring new contributors as well.

<h1 align = "" id = "major-takeaways">Major Takeaways 📚</h1>



- Developed a deeper understanding of the open-source world and the collaborative nature of open-source projects.
- Improved in writing `clean`, `maintainable code` and `creating clear`, clear commit messages and pull requests..
- Improved `communication` and `leadership` abilities by learning from mentors’ guidance.
- learned how to quickly adapt to the community’s coding standards.
- I realized and learned the importance of communication and collaboration in open-source projects.
- I learned how to break down a large project into smaller tasks, set timelines, and stay disciplined to meet deadlines. This experience improved my project management skills.
- Gained the ability to research and explore unfamiliar technologies, tools, and concepts efficiently.
- Developed the ability to navigate, understand, and contribute to large, complex codebases.
- Contributing to an open-source project enhanced my sense of responsibility.
- Created friendships and professional connections with people from other countries.

## Links of work done: 🎯

### Pull Requests 🔗

 1. [https://github.com/fossology/fossology/pull/2764](https://github.com/fossology/fossology/pull/2764)
 2. [https://github.com/fossology/fossology/pull/2834](https://github.com/fossology/fossology/pull/2834).
 3. [https://github.com/fossology/fossology/pull/2832](https://github.com/fossology/fossology/pull/2832)
 4. [https://github.com/fossology/fossology/pull/2830](https://github.com/fossology/fossology/pull/2830)
 5. [https://github.com/fossology/fossology/pull/2829](https://github.com/fossology/fossology/pull/2829)
 6. [https://github.com/fossology/fossology/pull/2827](https://github.com/fossology/fossology/pull/2827)
 7. [https://github.com/fossology/fossology/pull/2826](https://github.com/fossology/fossology/pull/2826)
 8. [https://github.com/fossology/fossology/pull/2825](https://github.com/fossology/fossology/pull/2825)

<h1  id = "acknowledgements">🎓 Acknowledgements</h1>

<p align="justify">
Being a part of FOSSology was a rewarding experience and journey of growth in my crucial aspects of life. The journey was really exciting more than I expected. As my first  endeavor into open-source, I learned the ropes and gained invaluable skills including communication, teamwork, writing clean code and other technical skills that are very crucial in my future ventures. I deeply extend heartfelt gratitude  for the whole FOSSology team especially my mentors for the kindness, patience and invaluable support they gave me throughtout this journey. 
<br />
Special thanks to <a href="https://github.com/shaheemazmalmmd" target="_blank">Shaheem Azmal M MD</a>, <a href="https://github.com/GMishx" target="_blank">Gaurav Mishra</a>,  <a href="https://github.com/dushimsam" target="_blank">Samuel Dushimimana</a>, and <a href="https://github.com/soham4abc" target="_blank">Soham Banerjee</a> as my mentors. I really appreciate how humble and polite these people are, their full guidance and support has truly shaped me and made me who I am today.
    <br/>
    <br/>
    In conclusion, It has been an exciting journey working with this wonderful community, and I've gained so much from the experience. This is not an end but a good start to tackle as many open-source projects. I will embrace the open-cource culture I gained from GSoC, keep contributing as well as guiding new contributors!
</p>

<h1 align = "center" id = "connections">🌐 Let's connect! </h1>

  

- [LinkedIn](https://www.linkedin.com/in/valens-niyonsenga-947440228/)

- [GitHub](https://github.com/valens200)

- [Twitter](https://x.com/200Valens)

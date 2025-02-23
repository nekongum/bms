**Login** 

**Use case description** 



|**Use Case Name:**  Login |**ID:** U001 |**Importance Level:**  High |
| - | - | - |
|**Primary Actor:**  User |**Use Case Type:**  Essential ||
|**Stakeholders and Interests:** Astronomer, Administrator, Science Observer |||
|**Brief Description:** This shows how users log in to the Gemini website |||
|**Trigger:** The user wants to log in to the  Gemini website. **Type:** Internal  |||
|<p>**Relationships:** </p><p>`    `Association: User     Include: - </p><p>`    `Extend: - </p><p>`    `Generalization: - </p>|||
|<p>**Normal Flow of Events:**  </p><p>1. The astronomer and science observer input email and password.  </p><p>2. The astronomer and science observer clicks the login button to enter the website. </p>|||
|<p>**Subflows:** </p><p>●  In case of issues: The user types their email or password correctly.** </p>|||

**Alternate/Exceptional Flow: ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.001.png)**

- If the users’ accounts don’t exist, they have to inform the support to add their accounts. 

**Activity diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.002.png)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.003.png)

**Create science plans** 

**Use case description** 



|**Use Case Name:** Create science plans |**ID:** U002  |**Importance Level:**  High |
| - | - | - |
|**Primary Actor:** Astronomer |**Use Case Type:** Overview, Essential ||
|<p>**Stakeholders and Interests:** </p><p>**Astronomer** – Needs to create detailed observation plans for successful data collection. **Science Observer** – Uses these plans to execute observations. </p><p>**Telescope Operator** – Uses the plans to configure telescope settings. </p>|||
|**Brief Description:** The astronomer creates an observation plan by defining scientific objectives, observational  methods,  and  telescope  configurations.  This  plan  is  then  used  to  execute observations. |||
|**Trigger:** The astronomer initiates the creation of a new science plan. **Type:**  External |||
|<p>**Relationships:** </p><p>`    `Association: Science Observer, Telescope Operator </p><p>`    `Include: Test Science Plans (UC2), Submit Science Plans (UC3)     Extend: Transform Science Plans (UC4) </p><p>`    `Generalization:- </p>|||



|<p>**Normal Flow of Events:** </p><p>1. The astronomer logs into the Gemini Telescope System. </p><p>2. The astronomer selects the option to Create a New Science Plan. </p><p>3. The system prompts the astronomer to enter: </p><p>a. Observation objectives (e.g., study exoplanets, analyze star formations). </p><p>b. Observational methods (e.g., long-exposure imaging, spectroscopy). </p><p>c. Telescope configurations (e.g., instrument selection, exposure time, filters). </p><p>4. The system validates the plan for completeness and feasibility. </p><p>5. The astronomer reviews and finalizes the plan. </p><p>6. The system saves the science plan and marks it as ready for testing. </p>|
| - |
|**Subflows:** If the astronomer misses any required fields, the system highlights missing information and requests input before proceeding. |
|<p>**Alternate/Exceptional Flow:**  </p><p>- **Incomplete Information:** If the astronomer attempts to submit an incomplete form, the system displays an error message and prevents submission. </p><p>- **Technical Issues:** If the system encounters an error while validating the plan, an error message is displayed, and the astronomer is advised to retry later. </p>|

**Activity diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.004.png)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.005.jpeg)

**Test Science Plans** 

**Use case description** 



|**Use Case Name:** Test Science Plans |**ID:** U003 |**Importance Level:**  High |
| - | - | - |
|**Primary Actor:** Astronomer |**Use Case Type:** Detail, Essential ||
|<p>**Stakeholders and Interests:**  </p><p>**Astronomers:** Check that the science plans will give useful data and ensure the necessary tools and resources are set up properly. </p>|||
|**Brief Description:** This use case describes the process of testing a Science Plan using a Virtual Telescope  and  Interactive  Observing  Mode.  The  system  allows  astronomers  to  simulate observations in real time, interact with parameters, and validate the feasibility of the plan before execution. |||
|<p>**Trigger:** The testing of a science plan is triggered when a new plan is created or when an existing plan requires validation before execution. </p><p>**Type:** External </p>|||
|<p>**Relationships:** </p><p>`    `Association: Astronomer </p><p>`    `Include: Login, Operate the interactive observing (virtual telescope)     Extend: - </p><p>`    `Generalization: - </p>|||
|<p>**Normal Flow of Events:** </p><p>1. The astronomer logs in to the Gemini website. </p><p>2. The astronomer selects the science plan session. </p><p>3. The astronomer chooses a science plan from the available list. </p>|||



|<p>4. The astronomer clicks the test button on the selected science plan's interface. </p><p>5. If the test passes → Review the result. </p><p>6. If the test fails → Proceed to log errors. </p><p>7. Error classification: </p><p>- Warning → Log as a Warning Log. </p><p>- Serious → Log as a Serious Log. </p><p>- Fatal → Log as a Fatal Log. </p><p>8. The astronomer reviews the result. </p><p>9. The astronomer sends the result (which may contain errors) to the science observer. </p>|
| - |
|**Subflows:**  Logging in and selecting a science plan is a preparatory process before testing. |
|<p>**Alternate/Exceptional Flow:** </p><p>- If the test fails, it is categorized into different error logs based on severity. </p><p>- If no errors occur, sending results to the science observer may not be necessary. </p>|

**Activity diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.006.png)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.007.jpeg)

**Submit a Science Plan** 

**Use case description** 



|**Use Case Name:** Submit a Science Plan |**ID:** U004 |**Importance Level:**  High |
| - | - | - |
|**Primary Actor:** Astronomer |**Use Case Type:** Essential ||
|<p>**Stakeholders and Interests:**  </p><p>- Astronomer: Wants to submit a science plan for telescope observation. </p><p>- System: Ensures validation, scheduling, and execution of the submitted science plan. </p>|||
|**Brief Description:** The Astronomer submits a science plan containing observation details such as target selection, instrument configuration, and exposure settings. The plan undergoes validation by the Science Observer before being converted into an observing program for execution. |||
|**Trigger:** The Astronomer decides to submit a science plan for approval. **Type:** External |||
|<p>**Relationships:** </p><p>`    `Association: Astronomer, Science Observer     Include: -    </p><p>`    `Extend: - </p><p>`    `Generalization:- </p>|||
|<p>**Normal Flow of Events:** </p><p>1\.  The astronomer logs into the Gemini website. </p><p>- The astronomer enters their email and password. </p><p>- The system verifies the credentials and grants access. </p>|||
2. The astronomer selects a science plan session. ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.008.png)
   1. The astronomer chooses an available session to submit the science plan. 
   1. The system creates a science plan session. 
2. The system verifies the astronomer’s authorization. 
   1. The system checks the astronomer’s authorization. 
2. The astronomer submits the science plan. 
   1. The astronomer finalizes and submits the science plan through the system. 
2. The system logs and stores the submitted science plan. 
   1. The system records and stores the submitted science plan. 
2. The astronomer modifies and resubmits if required. 
   1. If necessary, the astronomer updates the plan and resubmits it. 
2. The system validates the observing program. 
   1. The system verifies the validity of the observing program. 
2. The system confirms approval and scheduled execution. 
- The system confirms approval. 
- The system schedules the execution of the observing program. 

**Subflows:**  

**1: Auto-Save Draft** 

- If the astronomer does not submit the science plan within a certain timeframe, the system automatically saves the current progress as a draft. 
- The astronomer can later resume editing and finalize submission without losing their work. 

**2: Authorization Check** 

- If the astronomer is not authorized, the system rejects the submission and notifies the astronomer. 

`            `**3: Notification to Science Observer** 

- Once the science plan is successfully submitted, the system automatically notifies the assigned Science Observer. 
- The Science Observer receives details of the submitted plan for further review and processing. 

**Alternate/Exceptional Flow: ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.009.png)**

**1: Incomplete Submission** 

- If the astronomer submits a science plan with missing required fields, the system prompts  the  astronomer  to  complete  all  necessary  fields  before  allowing submission. 

**2: Authorization Failure** 

- If an unauthorized user attempts to submit a science plan: 
  - The system denies access and displays an error message. 

**Activity diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.010.png)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.011.jpeg)

**Manage astronomical data** 

**Use case description** 



|**UseCase Name:** Manage astronomical data |**ID:** U005 |**Importance Level:**  High |
| - | - | - |
|<p>**Primary Actor:  Science Observer** (Primary Actor) </p><p>`                 `**Astronomer** (May have access to certain data) </p>|**Use Case Type:** Business Use Case ||
|<p>**Stakeholders and Interests:**  </p><p>- **Science Observer:** Needs to manage, validate, and organize astronomical data for research and analysis. </p><p>- **Astronomer:** May require access to properly managed datasets for scientific studies. </p><p>- **System  Administrator:**  Ensures  that  user  access  and  system  integrity  are maintained, and assists in error resolution. </p>|||
|**Brief Description:** This use case allows the Science Observer to manage collected astronomical data, including validation, tagging, categorization, and metadata updates. The system ensures data integrity and logs all modifications for security and traceability. |||
|<p>**Trigger:**  </p><p>**Event-Driven:** When new data is collected and needs to be processed. </p><p>**User-Driven:** When the Science Observer manually selects datasets for management. **Type:** External </p>|||
|<p>**Relationships:** </p><p>Association: Science Observer, Astronomer,System Admin Include: - </p><p>Extend: - </p>|||



|<p>**Normal Flow of Events:** </p><p>1. The Science Observer logs into the system. </p><p>2. The system presents a list of available astronomical datasets. </p><p>3. The observer selects a dataset for management. </p><p>4. The observer performs one or more of the following actions: </p><p>a. Tagging data with metadata. </p><p>b. Validating data integrity. </p><p>c. Categorizing data into relevant projects. </p><p>5. The system validates data integrity. </p><p>a. If valid, the system saves changes and updates logs. </p><p>b. If invalid, the observer receives error details and can retry. </p><p>6. The observer can view, retrieve, or further modify the managed data. </p><p>7. The system confirms successful management operations. </p>|
| - |
|<p>**Subflows:** </p><p>**Data  Tagging:**  The  observer  assigns  relevant  metadata  (e.g.  celestial  objects,  observation  date, telescope used,). </p><p>**Data Validation:** The system runs an integrity check and reports any errors or missing data. **Categorization:** The observer organizes the data into projects or observational programs. </p>|
|<p>**Alternate/Exceptional Flow:** </p><p>**Astronomer Requests Access to Managed Data:** </p><p>1. The Astronomer requests access to a dataset. </p><p>2. The system checks permissions and either grants or denies access. </p><p>3. If denied, the Astronomer has two options: </p><p>- Request elevated permissions from the System Administrator. </p><p>- Accept the restriction and move on. </p><p>4. If  the  Astronomer  requests  elevated  access,  the  System  Administrator  reviews  the request: </p><p>- If approved, the Astronomer gains access. </p><p>- If  rejected,  the  decision  is  final,  and  they  cannot reattempt access without a change in permissions. </p><p>**Data Validation Fails (With Retry Limit):** </p><p>1\.  The system detects an error in the data and notifies the observer. </p>|

2. The observer can retry fixing the issue and revalidate the data. ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.012.png)
2. Retry Limit Rule: 
   1. The observer can attempt to fix and revalidate up to 3 times. 
   1. If all 3 attempts fail, the system automatically flags the data for review. 
   1. The System Administrator is notified for further action. 
2. If the observer flags the data manually, the admin is notified immediately. 

**Activity diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.013.png)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.014.jpeg)

**Validate  a Science Plan** 

**Use case description** 



|**UseCase Name:** Validate a Science Plan |**ID:** U006 |**Importance Level:**  High |
| - | - | - |
|**Primary Actor:** Science Observer |**UseCase Type:** Essential ||
|**Stakeholders  and  Interests:**  Telescope  Operator  –  May  need  to  check  if  the  program  is compatible with telescope operations and constraints. |||
|**Brief Description: The** Science Observer validates the plan to ensure it aligns with telescope and instrument capabilities. |||
|<p>**Trigger:** When an Astronomer submits a science plan to the system for review. This occurs after the astronomer has created and tested the plan using the virtual telescope and interactive observing mode. </p><p>**Type:** External </p>|||
|<p>**Relationships:**  </p><p>`    `Association: Telescope Operator, Astronomer     Include:  - </p><p>`    `Extend: - </p><p>`    `Generalization:- </p>|||
|<p>**Normal Flow of Events:** </p><p>1. The Science Observer logs in to the Gemini system. </p><p>2. The Science Observer navigates to the Science Plan Validation section. </p><p>3. The Science Observer selects a submitted science plan from the available list. </p><p>4. The Science Observer reviews the details of the science plan, including target selection, exposure time, and instrument configuration. </p>|||
5. The Science Observer clicks the validate button to check the plan’s feasibility. ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.015.png)
5. The system runs validation checks on telescope compatibility, scheduling constraints, and observation feasibility. 
5. The Science Observer reviews the validation results displayed by the system. 
5. If the plan is valid, the Science Observer approves it for transformation into an observing program. 
5. If issues are found, the Science Observer requests modifications, and the plan is sent back to the Astronomer for revision. 

**Subflows:** 

1. **Telescope Capability Check Subflow** 
1. The system checks if the selected telescope and instruments match the science plan requirements. 
1. If any instrument is unavailable or incompatible, the system flags the issue. 
1. The Science Observer reviews flagged issues and determines whether adjustments can be made or if the plan must be revised. 
2. **Scheduling Constraint Check Subflow** 
1. The  system  verifies  if  the  requested  observation  time  fits  within  the  telescope's available schedule. 
1. If  conflicts  exist  (e.g.,  overlapping  schedules,  maintenance  periods),  the  system suggests alternative slots. 
1. The Science Observer reviews conflicts and may adjust the plan or request revisions. 
3. **Observation Feasibility Check Subflow** 
1. The  system  evaluates  factors  like  weather  conditions,  visibility,  and  technical constraints. 
1. If conditions are unfavorable, the system suggests alternative observation times or locations. 
1. The Science Observer decides whether to approve the plan with modifications or return it for revision. 

**Alternate/Exceptional Flow:** 

1. **If the Science Plan Fails Validation** 
1. The  system  highlights  errors  or  conflicts  (e.g.,  scheduling  issues,  incompatible instruments). 
1. The Science Observer reviews the specific validation failures. 
3. The  Science  Observer  adds  comments  and  requests  modifications  from  the Astronomer. ![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.016.png)
3. The system notifies the Astronomer to revise and resubmit the science plan. 
2. **If the Science Plan Passes Validation** 
1. The system marks the plan as validated. 
1. The Science Observer confirms the validation and approves the science plan. 
1. The system transforms the approved science plan into an observing program. 
1. The system notifies relevant users that the plan is ready for execution. 

**Activity diagram**  

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.017.jpeg)

**Sequence Diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.018.jpeg)

**Class diagram** 

![](Aspose.Words.b1c67eca-e4f8-4baa-8242-e05a0be2fd64.019.png)

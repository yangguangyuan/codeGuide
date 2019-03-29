# Algorithm

两数之和

* 个人

```java
public class Solution {

    public static void main(String[] args) {
        Solution solution = new Solution();
        int[] re = new int[4];
        re[0] = 3;
        re[1] = 3;


        int[] aa =  solution.twoSum(re,6);
        System.out.println("["+aa[0]+","+aa[1]+"]");
    }

    public int[] twoSum(int[] nums, int target) {
        int[] re = new int[2];
        for(int i=0;i<nums.length;i++){
            for(int j=i+1;j<nums.length;j++){
                int result = nums[i]+nums[j];
                if(target==result){
                    re[0] = i;
                    re[1] = j;
                    break;
                }
            }
        }

        return re;
    }
}

```

* 官方

```java
public int[] twoSum(int[] nums, int target) {
    Map<Integer, Integer> map = new HashMap<>();
    for (int i = 0; i < nums.length; i++) {
        int complement = target - nums[i];
        if (map.containsKey(complement)) {
            return new int[] { map.get(complement), i };
        }
        map.put(nums[i], i);
    }
    throw new IllegalArgumentException("No two sum solution");
}
```



# Review

[uipath](<https://forum.uipath.com/>)

# Tip

## 解决问题

问题:企业中业务流程重复操作,耗费大量的人力,物力,财力

Robotic Process Automation (RPA),机器人过程自动化,RPA机器人利用用户界面捕获数据并像人类一样操纵应用程序,提高效率,减少成本

## 优势劣势

### 优势

- 不会破坏底层系统
- 高度可扩展
- 当今企业唯一的自动化软件

### 劣势

- 普及度尚低

## 适用场景

1：Robotic Process Automation
数据输入，多个应用程序间的数据共享等的固定业务流程的简单业务
例如人事，财务，总务，情报部门等等的后台部门的事务，管理业务，销售管理和经费处理等等应用程序的输入等等业务。
2：Enhanced Process Automation
不能结构化的数据收集和分析等的业务
例如安全日志的分析，各种因素叠加的销售分析，各种推荐广告数据等等的多种数据为基础的分析业务。
3：Cognitive Automation
基于大量数据的学习进而做出分析判断的业务。

## 组成部分

### 官网

[官网](<https://www.uipath.com/>)

[文档](<https://studio.uipath.com/v2016.2/docs/introduction>)

[中文文档](<https://www.jianshu.com/c/441bdfa8ae43>)

[论坛](<https://forum.uipath.com/>)

[破解](<https://www.sdbeta.com/wg/2019/0218/228513.html>)

### uipath学院

#### 课程答案

##### Non-Technical Trainings

###### Business Analyst Training

1)

**Which of the factors below influence the complexity of a process proposed for RPA?**

- Citrix/ VDI/ Remote desktops
- The number of variations and the exception rate
- The input type: standard or non-standard, structured or unstructured
- The number of applications and number of screens

Score: 10

Multiple Choice

2)

**What are some of the best practices in the Process Description and documentation?**

- Before starting the 1st workshop with the Subject Matter Expert, gather and understand the process-related documents: Standard Operating Procedures, Process maps, Organizational Chart, User manuals etc.
- Business rules: Index each business rule and use the index as reference in the AS-IS process description

Score: 0

Multiple Choice

3)

**What are some of the best practices in the Process Description and documentation?**

- Process activities should be detailed at the keystroke level and accompanied by representative screenshots
- Business rules: create a separate document containing a list of values and rules that can be used by the robot, and link the file to the PDD
- Before asking for the AS IS Process validation, ensure that the SME performs all the steps described in the PDD

Score: 0

Multiple Choice

4)

**Which of the actions below can be applied on the existing requirements if a change occurs?**

- Change
- Add
- Keep
- Remove

Score: 10

Multiple Choice

5)

**What are the advantages of using the Traceability Matrix?**

- It helps in maintaining a versioning of the business requirements, easing the identification of all the tasks affected by the change
- It provides the ability to map all the requirements and deliverables to prevent them from being omitted later
- It provides the ability to trace the overall progress, from the Business requirements to the test cases and the Go-live materials: Procedures, User manuals, etc.

Score: 0

Multiple Choice

6)

**If part of a process is left out of scope for RPA, what could be the impact on the TO BE process mapping?**

- The output of that manual out of scope activity might need to be used or not by the robot
- The order of the steps might change
- The robot might need to wait for the human to complete that part of the process before proceeding further

Score: 0

Multiple Choice

7)

**What are the possible reasons for deciding to automate only a part of a process using the RPA technology?**

- The other parts the process involve human input, due to the rule complexity and the human knowledge involved
- Some activities are liable to change in the next 3 to 6 months
- The necessary input for the robot is unstructured and non-standard or involves handwritten papers

Score: 0

Multiple Choice

8)

**What is the role of a Business Analyst during the Go-Live preparation phase in the RPA journey?**

- Handover all the documents produced and updated throughout all the project phases
- Delivering Trainings along with the SMEs that are already involved in testing
- Providing support in updating the existing procedures
- Providing User Manuals of the RPA process

Score: 10

Single choice

9)

**What is the main scope of RPA testing?**

- The output of the robot which is usually the existing output of the automated process

Score: 10

Multiple Choice

10)

**Which of the below are the ways turning unstructured or non-standard inputs to structured, standard ones?**

- Converting non-digital inputs (paper documents) into digital ones with the help of OCR
- Translating voice discussions into a template form, with the request details
- Templatizing the information (different geographical business units using different templates to send the same information to be processed by a back office department; the solution would be to create a unique template for all business units)

Score: 10

Multiple Choice

11)

**Which of the options below are prerequisites of the testing phase?**

- Dependencies on other projects related to test environment and test data used
- Test environment ready
- Test scenarios to cover for all the business use-cases, all the exceptions and business rules
- Test data prepared for all test scenarios

Score: 10

Multiple Choice

12)

**What is the purpose of filling in the Process Definition Document?**

- To prove that performed development is in accordance with the given requirements
- To hand over the document to the developer
- To validate the content with the Process and the Business owners and the other involved stakeholders

Score: 10

Multiple Choice

13)

**How can you split a process to better describe it?**

- In sub-processes per applications used
- In Input, Process, Output

Score: 0

Multiple Choice

14)

**What are the process metrics that indicate the advantages of RPA implementation?**

- Decrease in the Error Rate Indicator on overall process which indicates an improvement in the process quality
- Decrease in the Average Handling Time and the Cycle Time

Score: 0

Multiple Choice

15)

**How is an RPA process prioritized?**

- By taking into consideration other business factors, such as compliance, increase of volumes of activity on some areas
- By measuring the Process Complexity from RPA implementation perspective
- By measuring the potential FTE savings

Score: 10

Single choice

16)

**What is the role of a Business Analyst during the Testing phase of RPA implementation?**

- Coordinating testing and collecting testing results

Score: 0

Multiple Choice

17)

**Which of the input classifications below is structured?**

- 1 predefined report in Excel file format
- An application screen containing 25 fields

Score: 0

Multiple Choice

18)

**Which of the input below are standard?**

- An application screen containing 5 fields
- An application screen containing 25 fields
- A predefined report in Excel file format

Score: 0

Multiple Choice

19)

**Which of the system and business exceptions below are classified correctly?**

- Business exception: the invoice is not attached to an email that triggers the robot for invoice processing
- System exception: the application stops responding

Score: 0

Multiple Choice

20)

**What is the role of a Business Analyst throughout the RPA journey?**

- **Solution design**: Prepare Process Definition Document, Prepare Test Scenarios
- **Prepare RPA:** Inventory of the Processes, Opportunity assessment

###### RPA Awareness Training

1)

**What processes should I automate?**

- Simple, stable, manual, and repetitive processes with high transaction volumes and standard electronic input type

2)

**Which UiPath component provides robot management capabilities?**

- UiPath Orchestrator

3)

**Which UiPath component executes processes?**

- Robots

4)

**What is Robotic Process Automation?**

- Automation that perfectly emulates repetitive tasks performed by human workers through the User Interface
- Automation that interacts with computer-centric processes through a software User Interface

Score: 0

Multiple Choice

5)

**What are the benefits of RPA implementation?**

- Improved customer experience - RPA boosts the quality of the services delivered by minimizing manual intervention, errors and work duplication, while rapidly decreasing processing times, which leads to better SLAs
- The technology is non-invasive**,** which means that companies do not need to make changes to existing legacy systems when implementing RPA
- Increased compliance by eliminating human error
- Cost reduction and Rapid ROI - An RPA robot costs a fraction of an FTE and can work 24/7/365; the ROI occurs in 6 to 9 months, due the high speed of automation

Score: 0

Multiple Choice

6)

**Which of the robot types below are currently provided by UiPath?**

- Attended robots
- Unattended robots

Score: 0

Multiple Choice

7)

**What are the disadvantages of each CoE type?**

- Centralized COE: Automation prioritization challenges
- Hybrid COE: Discrepancy in know-how between the main and the smaller RPA COEs

Score: 10

Multiple Choice

8)

**What are the advantages of each CoE type?**

- Centralized COE: Expertise; the learned lessons and the best practices are more easily disseminated
- Hybrid COE: Decreased risk of prioritization challenges due to smaller and dedicated RPA COEs

9)

**What is the UiPath designer tool?**

- Studio

10)

**What are the phases of an RPA journey?**

- Assessing the RPA capability, building a Business Case, running a POC or a Hackathon, enabling a COE, initializing the pilot RPA project, evaluating the pilot and documenting the learned lessons, institutionalizing the RPA solution

###### RPA Implementation Methodology Training

1. Can RPA developers be trained exclusively online? yes

2. Do developers have access to the Production environment in the Warranty period? no

3. Should the process pipeline be created before moving to the project's Analysis phase? yes

4. What are the criteria that a process should meet in order to be suitable for automation ? 

   Is rule-based  Is highly manual 

5. What are some of the RPA Solution Architect's attributions?

   Supervise the solution build and delivery of the workflow  

   Perform hands-on coding 

6. What are the three recommended environments for a typical infrastructure setup?

   QA 

   Production
   Development

7. What developer collaboration tools are integrated in UiPath Studio?

   SVN TFS

8. **What are some of the advantages of using the Robotic Enterprise Framework?**

   Reporting functionalities

   Proper exception handling

## 底层原理

RPA机器人能够模仿许多（如果不是大多数）人类用户的行为。他们登录应用程序，移动文件和文件夹，复制和粘贴数据，填写表单，从文档中提取结构化和半结构化数据，抓取浏览器等。

## 相似对比

与其他传统IT解决方案相比，RPA允许组织以之前遇到的成本和时间的一小部分进行自动化。RPA本质上也是非侵入性的，可以利用现有的基础设施，而不会对基础系统造成干扰，这些系统的更换难度大，成本高。使用RPA，成本效率和合规性不再是运营成本，而是自动化的副产品。

# Share

[uipath文档](<https://www.jianshu.com/c/938e6c0d92ed>)






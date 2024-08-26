# GRAVISU

CS492G Human-AI Interaction 2023 Fall KAIST | Design Project

Team Name: **Brown Bear**

Members: Hyeongu Kang, Jiseung Hong, Haeseul Cha

## Video URL

[https://youtu.be/3VNBYNze80U](https://youtu.be/3VNBYNze80U)

## **Quality Arguments**

There are **two human-AI interaction goals** to be achieved through UI.

1. Users can identify and provide the necessary elements(model / dataset) when using the Gra-Visu service.
2. Users can analyze the characteristics of their AI models and datasets through the results of Gra-Visu.

**For the first goal, 1) Well-structured and 2) Intuitive & Clear UI Items were considered.**

1) Well-structured UI

- Left ↔ Right: Divide Input ↔ Output part
- UP ↔ Down: Placement by Service process

![UI 설명 1.png](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/UI_%25EC%2584%25A4%25EB%25AA%2585_1.png)

2) Clear & Intuitive UI Item  

- Clear request for user action : Drag and drop / upload / Run Gra-Visu
- Intuitive message : activate button & message when process is done

![UI 설명 2.png](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/UI_%25EC%2584%25A4%25EB%25AA%2585_2.png)

As a result, an average of **4.16 / 4.5** points was achieved for each of the following two question between a total of 8 user tests. (1~5 points)

Q1. Were there any blockages, inconveniences, or difficulties in using the Gra-Visu service step by step?

Q2. Did Gra-Visu help lower entry barriers or reduce hassle for image analysis using AI models?

**To achieve the second goal, we design 1) Help message UI and 2) Tutorial document.**

- 1) Help message
    - Help message appears when mouse is placed on '?'
- 2) Tutorial document
    - explain ‘How to analysis AI model & dataset by Gra-Visu service’
    - give test example to understand Gra-Visu service

![UI 설명 3.png](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/UI_%25EC%2584%25A4%25EB%25AA%2585_3.png)

However, it would have been better if the contents of the Tutorial document were melted on the UI.

- A user commented on the test, "It would be better if the explanation or instructions were briefly explained not only on Google Form but also on the UI."
- In addition, when interviewed separately with those who participated in the test, they answered, "I understand when I hear additional explanations about the service or when I look at the Tutorial Document, but at first I didn't reach out to how to use the results."

In addition, at the time of service design, we think that the user group would generally know the AI model, especially the GradCAM method, but there was a big difference in understanding for each user.

- The Ph.D. user immediately understood the GradCAM result without a Tutorial
- Most master's program users had no idea how to understand GradCAM results.

Therefore, it seems necessary to **1) reflect the Tutorial content on the UI** and **2) UI design considering the difference in user understanding.**

## Evaluation

Our team faced several limitations in the deployment process. Due to the lack of a suitable server for hosting, we proceeded with deployment by hosting on a local machine through the KAIST IP, limiting user testing to KAIST members only. Our application, being designed for deployment targeting developers familiar with AI models, made it challenging to gather participants for user testing. Therefore, we conducted deep user tests with six graduate students.

The user test involved participants following a tutorial we provided, then answering questions in three areas: GradCAM Results, Keyword Statistics, and User Experience.

**GradCAM Results**

In GradCAM Results, we asked users 1) if they could understand the features the AI model used for classification based on the GradCAM result images, 2) if sufficient information was provided to understand the AI model's decision-making process, and 3) if it was appropriate to judge the model's classification direction based on the GradCAM results. The first question received respectable scores as mentioned in Quality Arguments, and for the second question, all six participants responded that sufficient information was provided. However, one user commented, "I think there are significant limitations to judging solely with the human eye. Accurate, quantitative indicators are necessary." This feedback highlighted that visual explanations alone may not fully instill user confidence, and quantitative indicators are needed.

Regarding the last question, responses were generally positive but somewhat divided, as shown in the chart below. This suggests that GradCAM Results alone may not conclusively reflect the criteria an AI model uses for decision-making, underscoring the need for a more persuasive tool than GradCAM.

![Untitled](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/Untitled.png)

**Keyword Statistics**

Keyword Statistics involved generating captions for images in each class and visualizing the frequency of words in these captions as histograms. When asked if Keyword Statistics helped identify trends or biases in each class, most agreed, with all six participants stating that it provided enough information to discern dataset trends. One user commented, "The histogram was very effective for analyzing my dataset," teaching us that visualizing quantitative information can be effective.

![Untitled](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/Untitled%201.png)

However, there were also negative views on judging dataset trends based on histograms. A tool that could more convincingly persuade users of dataset biases or trends was needed.

![Untitled](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/Untitled%202.png)

**User Experience**

Regarding the question of whether Gra-Visu helped lower the entry barrier or reduce the hassle in using AI models for image analysis, we received positive feedback as shown below.

![Untitled](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/Untitled%203.png)

However, there were negative opinions in response to whether the purpose and overall execution process of the Gra-Visu service were easy and intuitive to understand.

![Untitled](Final%20Report%2004baad9c376249c592f2eb22bebf52f4/Untitled%204.png)

In terms of aspects related to user fatigue, participants left comments like, “The running time was too long,” and “It would be better if explanations or instructions were briefly described in the UI as well.” From this, we learned that it is very important to reduce user fatigue, such as waiting time and difficulty in understanding the service. We also realized that it would be beneficial to have more detailed and readily accessible progress monitoring.

## Discussion

In this design project ‘Gra-Visu’, we can link our core ideas with these topics of human-AI interaction: fairness, ethics(transparency), and explainable & interpretable AI. Overall, by applying visualization, it was good that we presented an intuitive solution to easily approach problems that are not visible or cannot be addressed by quantitative analysis. However, our project has limitations in deriving direct user insights beyond the identified points due to the inability to actively encourage users to take additional actions or extract thoughts proactively. As the goal of this project is to learn the design principles of user-centered AI systems that involve human-AI collaboration, we tried to support users in observing and coming up with an idea for ways to control models in a user-friendly way.

- **Fairness**: Gra-Visu aims to help users discover invisible features of AI models and adjust them with more accurate samples. This can also provide clues to determining the fairness of the model. By comparing images at a glance and grasping keyword statistics in a unit of the class, users can guess the potential of bias from a macroscopic point of view. It was well done that while developing concepts, a possible way of use is related to the fairness of the model. However, offering just simple image classification results and its keyword statistic was not sufficient to fully derive users’ inference. Providing more insights to users through additional methods such as a Q&A system with text prompts for bias checks should be considered.
- **Ethics(Transparency)**: The main deliverable message of Gra-Visu is directly connected to the transparency of ethical issues in AI. The purpose of Gra-Visu is to solve the black box problem of AI by revealing invisible features. The black box of AI, the major problem we approached in our project, is one of the big obstacles that disturbs transparency. We visually offered detailed information and statistics about classified images. According to the survey evaluation, we could transfer AI’s decision to end-users in a more intuitive way and non-technical terms. However, it is still difficult to escape the imperfections of explaining real-world tasks by simply presenting the analysis results of image classification.
- **Explainable & Interpretable AI**: In stages of AI design, constructing an explainable and interpretable AI is an important process. In Gra-Visu, we tried to replace complicated steps such as modifying codes with simple uploading actions and direct visualization. Also, showing saliency maps of images which we applied by utilizing GradCAM is one of the examples of explainable AI techniques. Yet more interactions and feedback from users are still needed. This can be improved by bringing in features such as follow-up questions and exchanging feedback. Moreover, since the survey result shows different satisfaction and understanding by their backgrounds, considering various user dimensions and needs is necessary to satisfy user-centered explanation.

## Individual Reflections

### Hyeongu Kang

- *What worked well and not in your team? How did you overcome any hurdle in teamwork? What lesson about teamwork did you learn that you might apply to your next team project?*
    
    Notably, the absence of prior Full Stack service development experience among team members posed a significant dilemma in terms of delineating roles and responsibilities. To address this, I needed to familiarize myself with new areas such as FastAPI and JavaScript code, crucial for facilitating communication between these components. The environment where collaboration is indispensable, such as the development of a full-stack service, will come back anytime. In preparation for such a case, I learned that my own efforts are needed to meet the minimum level of communication in each field.
    
- *Through the team-based design project experience, what did you learn about human-AI interaction and web-based implementation?*
    
    I've identified two key aspects in Human-AI interaction and Web-based Implementation. Firstly, despite participants in user testing having an AI modeling background, there was a notable variance in their comprehension of the service. This underscores the need for meticulous service planning that considers differences in user understanding. Secondly, I've realized the significant challenge in creating a practical Web-based implementation, with tasks taking 8 to 9 times longer than in a local environment. This highlights the importance of carefully considering factors, including processing speed, to achieve a seamless web-based implementation.
    

### Jiseung Hong

- *What worked well and not in your team? How did you overcome any hurdle in teamwork? What lesson about teamwork did you learn that you might apply to your next team project?*
    
    Our team found it quite easy to select a topic and set a direction for our project. We quickly decided to use GradCAM technology to reduce user entry barriers for our project, and we never deviated from this path. However, the biggest problem was that none of us had experience in web hosting. This lack of experience led to difficulties in role distribution and overall planning for the project. Disagreements arose as we lacked basic knowledge about which APIs to use or which frameworks to implement. I resolved these hardships by understanding the entire process and taking on the burden of this new field. I learned that in application development projects, dividing roles is not as straightforward as implementing and merging different program modules. Eventually, one person needs to study, understand, and lead the entire process, assigning small roles to other team members, and then integrate the results with a sense of responsibility. Our team overcame these difficulties because I took on this responsibility, and the team members effectively implemented the parts I needed.
    
    In summary, teamwork depends on how well the team leader manages the project, how well roles are distributed among team members, and how effectively each member performs their role. For the next project, it seems more efficient to quickly assign the most capable person as the leader and have them lead the team.
    
- *Through the team-based design project experience, what did you learn about human-AI interaction and web-based implementation?*
    
    In this Human-AI project, we not only implemented what we aimed and planned but also deeply contemplated the advantages and disadvantages of human interaction. It was meaningful to discuss these questions with the team. There were times when what I thought was sufficient, another team member did not, and this conflict of opinions led to discussions that ultimately improved the user experience. This project was my first experience in web development, overcoming technical issues and challenges in Human-Computer Interaction (HCI) to complete the application. From being a developer focused solely on improving model performance, I now aim to become a system builder who contemplates what lies beyond that.
    

### Haeseul Cha

- *What worked well and not in your team? How did you overcome any hurdle in teamwork? What lesson about teamwork did you learn that you might apply to your next team project?*
    
    At first, the topic selection for the project went smoothly, and each person had a clear expertise in their respective fields, making it easy to divide roles accordingly. However, as we defined the detailed development direction, all team members had to learn areas in which they were not proficient. Adjusting to our different background knowledge, understanding the overall flow of the project, and following up on parts done by each member was not easy. To synchronize with team members, it was necessary to accumulate as much prior knowledge as others and understand the code, but gauging each other's level of understanding proved challenging. Therefore, we scheduled meetings twice a week to frequently share progress, and actively engage in questions and answers during each session. Additionally, everyone tried to familiarize themselves with unfamiliar development areas, not just their well-known fields. Through this teamwork, I reminded myself of the mindset of an active approach with team members, regardless of the field or topic. I will give my best in areas where I excel and not be afraid to face challenges together, matching the pace with my colleagues in areas where neither I nor my peers are well-versed.
    
- *Through the team-based design project experience, what did you learn about human-AI interaction and web-based implementation?*
    
    The process of considering two fields simultaneously, neither being solely human nor artificial intelligence, was novel. I remember discussions during the initial topic selection, focusing on two directions: 'facilitating more convenient processing by applying AI methods to human tasks' and 'evolving existing AI methods to be more human-friendly.' While it wasn't easy to grasp issues related to human interaction without much background knowledge of AI, I could gradually explore the points where the topics learned in class are applied through direct involvement in design projects.
    
    Even with experience in web development, it feels like acquiring new knowledge each time the language or framework used changes slightly. The process of integrating Python, the language mainly used to operate AI models, with JavaScript, frequently used in web development, was particularly unfamiliar. As myself who primarily handled frontend web development, I felt the desire to explore and utilize methods beyond simple visual implementation in the web environment, ones that could be used for human interaction.

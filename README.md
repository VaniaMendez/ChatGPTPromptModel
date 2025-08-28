# ChatGPTPromptModel 
# Model for the Adoption of AI Tools in the Software Development Life Cycle. Usage, Analysis and Proposals for ChatGPT Optimization.




<p>One of the most important phases in the software development life cycle is system deployment. However, developers often lack sufficient experience or clear guidance on how to configure a server, manage a domain, or correctly deploy their application in a production environment. This process can involve a number of technical challenges, such as assigning a static IP, configuring DNS, installing security certificates, or even managing server ports and services. Given these difficulties, the use of artificial intelligence tools such as ChatGPT becomes a valuable ally, as it can generate detailed instructions, resolve specific questions, and adapt recommendations to the technological environment we are using.

In this context, the artifact proposed in the article allows for the structuring of effective prompts that guide the developer through this critical stage, facilitating task automation, decision-making, and understanding of the deployment process, even for those without specialized training in infrastructure.</p>

**Proof of Concept 3: Application Deployment**

<div style="text-align: justify;">

<p> In proof of concept number 3, the AI was given the necessary instructions to generate a series of steps for deploying an application developed in Spring Boot on an AWS server.</p>

<div style="align: center;">
    <img src="images/artifact.png" alt="Descripción" width="500"/>
</div> <br>
<div style="text-align: center;">
    <img src="images/image.png" alt="Descripción" width="500"/>
</div>

<p>The generated prompt gave us a satisfactory result because it generated the steps required to configure a deployment environment with AWS for an application developed in SpringBoot in a way that was understandable to the developer.
It correctly generated a guide that helps configure a deployment environment in the aforementioned technologies, in simple steps.</p>

<p>In the first section ChatGPT shows the steps for creating a domain in AWS, from registration to DNS configuration.</p>

<div style="text-align: center;">
    <img src="images/image00.png" alt="Descripción" width="500"/>
</div>

<p> The first step is to register the domain. Initially, we searched for the domain <i>chatgpt-prompt-model.com</i>, but since it was already taken, we changed it to <strong>.org.</strong></p>

<div style="text-align: center;">
    <img src="images/image01.png" alt="Descripción" width="500"/>
</div>

<p>Once the domain has been registered, we can verify its creation in the AWS domain list and, once we see that it appears, we can continue with the elastic IP assignment and DNS configuration.</p>

<div style="text-align: center;">
    <img src="images/image06.png" alt="Descripción" width="500"/>
</div>


<p> To configure the elastic IP, go to the EC2 Dashboard and, in the Elastic IPs section, go to “Allocate Elastic IP” and click on “Allocate.”And after creation, we will associate it with our created instance. </p>


<div style="text-align: center;">
    <img src="images/image2.png" alt="Descripción" width="500"/>
</div>


<div style="text-align: center;">
    <img src="images/image3.png" alt="Descripción" width="500"/>
</div>




</div>


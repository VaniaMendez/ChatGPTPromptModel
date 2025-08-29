# Model for the Adoption of AI Tools in the Software Develop-ment Life Cycle: A Framework for Prompt Optimization in LLMs.
## ChatGPT Prompt Model


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


**Domain registration and configuration**

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
    <img src="images/image7.png" alt="Descripción" width="500"/>
</div>

<div style="text-align: center;">
    <img src="images/image8.png" alt="Descripción" width="500"/>
</div>

<p> With the elastic IP assigned, we can continue with the configuration of the DNS records. To do this, we will follow the path indicated in point 1.3 and add the two A records, following the instructions provided by ChatGPT.</p>

<div style="text-align: center;">
    <img src="images/image2.png" alt="Descripción" width="500"/>
</div>

<div style="text-align: center;">
    <img src="images/image3.png" alt="Descripción" width="500"/>
</div>

<p> To assign the record with www, you must enter “www” in the record name section and enable the “Alias” to be able to select the traffic route for that record.</p>

<div style="text-align: center;">
    <img src="images/image9.png" alt="Descripción" width="500"/>
</div>

<p>To conclude this first part, we used the online tool “Whatsmydns.net” to verify the propagation of our domain and make sure that our configurations were correct.</p>

<div style="text-align: center;">
    <img src="images/image10.png" alt="Descripción" width="500"/>
</div>
<br>


**EC2 instance configuration**

<p>In the second part, we will configure the virtual machine in AWS, following the instructions provided by ChatGPT regarding our request. </p>

<div style="text-align: center;">
    <img src="images/image11.png" alt="Descripción" width="500"/>
</div>

<p>Following the instructions, we created the instance and changed the name to “chatgpt-prompt-model.” </p>

<div style="text-align: center;">
    <img src="images/image12.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image13.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image14.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image15.png" alt="Descripción" width="500"/>
</div>

<p>To access the settings of the virtual machine we created, we used the WinSCP program, connected to the instance, and accessed the machine.</p>

<div style="text-align: center;">
    <img src="images/image16.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image17.png" alt="Descripción" width="500"/>
</div>

<p>The commands used to install and configure the programs on the virtual machine provided by ChatGPT were correct, but it is recommended that the program versions be checked, as sometimes it takes installation paths from pages that are no longer in operation.</p>

<div style="text-align: center;">
    <img src="images/image18.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image19.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image20.png" alt="Descripción" width="500"/>
</div>


**Configuring the NGNIX server and connecting to the domain**

<p>We use NGINX in a Spring Boot project when deploying to production because it acts as a reverse proxy in front of the application. This provides key benefits:
</p>
<ul> 
<li> Security: it only exposes standard ports (80/443) and hides the internal Spring Boot port (8080). It also simplifies HTTPS with SSL/TLS certificates.</li>
<li>Performance: it serves static files (images, CSS, JavaScript) more efficiently and reduces the load on the application.</li>
<li> Scalability: it can balance traffic across multiple Spring Boot instances.</li>
<li> Stability: it helps control traffic, prevents overloads, and improves availability.</li>
</ul>
<p>In short: NGINX is the “shield” and performance booster for the users, while Spring Boot focuses on business logic.</p>

<div style="text-align: center;">
    <img src="images/image21.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image22.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image24.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image23.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image25.png" alt="Descripción" width="500"/>
</div>

**Uploading the project to the server**

<p>In the fourth step, we are shown how to build and upload our Spring Boot project to our virtual machine, from packaging it into a .jar file to the paths where we should place it. For this step, we used the WinSCP tool as a file explorer between our computer and the virtual machine..</p>
<div style="text-align: center;">
    <img src="images/image26.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image27.png" alt="Descripción" width="500"/>
</div>

**Test via Swagger UI**

<p>Finally, in the last step, we are told how to access Swagger to check that our application has loaded correctly.
To do this, we must ensure that our project has the Swagger extension before packaging it in a .jar file.</p>

<div style="text-align: center;">
    <img src="images/image28.png" alt="Descripción" width="500"/>
</div>
<div style="text-align: center;">
    <img src="images/image29.png" alt="Descripción" width="500"/>
</div>

<p>Contact: vaniali00518@gmail.com</p>

</div>


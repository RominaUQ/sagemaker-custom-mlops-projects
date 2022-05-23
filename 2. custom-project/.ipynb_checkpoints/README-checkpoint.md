# sagemaker-custom-mlops-projects
## Create Custom Project Templates
If the SageMaker-provided templates do not meet your needs (for example, you want to have more complex orchestration in the CodePipeline with multiple stages or custom approval steps), create your own templates.
We recommend starting by using SageMaker-provided templates to understand how to organize your code and resources and build on top of it. https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-projects-templates-custom.html

To do this, after you enable administrator access to the SageMaker templates, 
1-	log in to the https://console.aws.amazon.com/servicecatalog/, 

2-	On the AWS **Service Catalog** console, under Administration, choose **Portfolios**.

3-	Choose Create a new portfolio.

4-	Name the portfolio **SageMaker Organization Templates**.

5-	Download the **train-build-deploy.yml** to your computer.

6-	Choose the new portfolio.

7-	Choose **Upload a new product**.

8-	For Product name¸ enter a name for your template. We chose **build-deploy-template**.

9-	For Description, enter my custom build and deploy template.

10-	For Owner, enter your name.

11-	Under Version details, for Method, choose **Use a template file**.

12-	Choose Upload a template.

13-	Upload the template you downloaded.

14-	For Version title, choose 1.0.

15.	Choose Review.

16.	Review your settings and choose Create product.

17.	Choose Refresh to list the new product.

18.	Choose the product you just created.

19.	On the Tags tab, add the following tag to the product:
  a.	Key – **sagemaker:studio-visibility**
  b.	Value – **true**

20.	 Back in the portfolio details, you see something similar to the following screenshot (with different IDs). ![alt text](images/img1.JPG)

16-	On the Constraints tab, choose **Create constraint**.

17-	For Product, choose build-deploy-template (the product you just created).

18-	For Constraint type, choose Launch.

19-	Under Launch Constraint, for Method, choose Select IAM role.

20-	Choose **AmazonSageMakerServiceCatalogProductsLaunchRole**.

21-	Choose Create.

22-	On the Groups, roles, and users tab, choose Add groups, roles, users.

23-	On the **Roles** tab, select the **role** you used when configuring your SageMaker Studio domain. This is where the SageMaker Domain Role can be found. ![alt text](images/img2.JPG)

24-	Choose Add access.

## Creating your project

In the previous sections, you prepared the Custom MLOps project environment. The next step is to create a project using your new template.

Sign in to the console with the data science account.
On the SageMaker console, open SageMaker Studio with your user.
Choose the Components and registries
On the drop-down menu, choose Projects.
Choose Create project.
Now go to SageMaker studio, choose Project from the left hand side ![alt text](images/img3.JPG)

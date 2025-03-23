# IAMCloudSecurity

In AWS, a "user" can be an individual or an automated system that interacts with the vast capabilities of the AWS cloud. 

Through AWS Identity and Access Management (IAM), you gain precise control over who can access your resources, ensuring that only authenticated users—those securely signed in, are granted the specific permissions they need to execute tasks. IAM empowers you to safeguard your cloud environment by meticulously defining and managing access rights, so you maintain both security and operational efficiency.

Let’s dive in and start building the key AWS components together, one step at a time:

🚀 Launch and manage EC2 instances

🛠️ Design and implement IAM Policies

👥 Set up IAM Users and User Groups

🏷️ Customize your AWS Account with an alias

**Step #1- Start EC2 Instances**

* Launch two Amazon EC2 instances.
* Log in to your AWS Management Console.
* Head to EC2.
* Set up the EC2 instances for production and development
* Choose Add additional tags, as it will help us with identifying all resources with the same tag at once.

**Step #2- Create an IAM Policy**

* Create an IAM policy that gives access to the development instance.
* Choose Create policy in the IAM Console.
* Choose policies and in policies,switch your Policy editor tab to JSON.
* Add the IAMPolicy.json in the policy editor tab.

**Step #3- **Create an AWS Account Alias****

* In the IAM Dashboard, we are gonna make it easier for users to log into your AWS account.
* We create account alias to make it easier to remember and share your AWS console's login URL with others.

**Step #4-Create IAM Users and User Groups**

* Set up a dedicated IAM group for the users.
* Select User groups in your left-hand navigation panel.
* Choose Create group.
* Setup the group and attach the policy(IAMPolicy.json) which we created previously.
* And then we can add users to the group.

**Step #5- Test the User's access**

* Log into the AWS Console using the user access.
* If you're a new user, you'll notice that some of your dashboard panels are showing **Access denied** already.
* In EC2 console, and make sure you're in the same Region as the one where you deployed your two production and development instances and we could see the instance states as running.
* Select your **production instance**, and in the Actions dropdown, select Manage instance state.
* When you try to stop the instance it throws an error and tells us we've failed to stop this instance.
* This happens because of the **IAMPolicy** ,where it denies ec2 development instance creation or deletion.
* If we try to stop the **development instance** it stops successfully.




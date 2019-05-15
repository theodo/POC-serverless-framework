# POC-serverless-framework

Le but de ce POC est de créer une auhentification avec des AWS Lambda en utilisant le framework Serverles

## AWS Configuration

To let the Serverless Framework access your AWS account, we're going to create an IAM User, and attach a JSON file policy to your new user. This IAM User will have its own set of AWS Access Keys.

- Create or login to your Amazon Web Services Account and go to the Identity & Access Management (IAM) page.

- Click on Users and then Add user. Enter a name in the first field to remind you this User is the Framework, like serverless-agent. Enable Programmatic access by clicking the checkbox. Click Next to go through to the Permissions page. Click on Create policy. Select the JSON tab, add the following JSON file you'll find in this gist.

When you are finished, select Review policy. You can assign this policy a Name and Description, then choose Create Policy. Check everything looks good and click Create user. Later, you can create different IAM Users for different apps and different stages of those apps. That is, if you don't use separate AWS accounts for stages/apps, which is most common.

- View and copy the API Key & Secret to a temporary place. You'll need it in the next step.

As you add additional functions and services, your permission needs will change. Though not advised, you can create an IAM User with Admin access, which can configure the services in your AWS account. This IAM User will have its own set of AWS Access Keys.

Note: In a production environment, we recommend reducing the permissions to the IAM User which the Framework uses. Unfortunately, the Framework's functionality is growing so fast, we can't yet offer you a finite set of permissions it needs (we're working on this). Consider using a separate AWS account in the interim, if you cannot get permission to your organization's primary AWS accounts.

- Create or login to your Amazon Web Services Account and go to the Identity & Access Management (IAM) page.

- Click on Users and then Add user. Enter a name in the first field to remind you this User is the Framework, like serverless-admin. Enable Programmatic access by clicking the checkbox. Click Next to go through to the Permissions page. Click on Attach existing policies directly. Search for and select AdministratorAccess then click Next: Review. Check everything looks good and click Create user. Later, you can create different IAM Users for different apps and different stages of those apps. That is, if you don't use separate AWS accounts for stages/apps, which is most common.

- View and copy the API Key & Secret to a temporary place. You'll need it in the next step.

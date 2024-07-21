## Project #1: Host A Website on Amazon S3!
In this project, using Amazon S3 (which stands for Amazon Simple Storage Service) to host a website.

### Step 1: Create a bucket in Amazon S3

* Login in to your amazon [**AWS Console**](https://us-east-2.console.aws.amazon.com/console/home) as a root user.
* In the **AWS Management Console**, search for **S3**.
* Click on **Create Bucket**.
* **AWS Region**: select the Region closest to you.
* For Bucket name, enter nextwork-website-project-name. Make sure to replace project-name with your name.
* For **Object Ownership**, choose **ACLs enabled**.
* For **Block Public Access settings for this bucket**, clear the check box for **Block all public access**.
* Check the box that says "**I acknowledge that the current settings might result in this bucket and the objects within becoming public.**"
* For **Bucket Versioning**, choose **Enable**.
* Choose **Create bucket**.
* After you create a S3 bucket you will see the following screen.

![Screenshot 2024-07-16 140637](https://github.com/user-attachments/assets/4d363a62-b0fb-4d39-90f1-f5f520a8b517)

### Step 2: Upload website content to your bucket

* In the **Buckets** section, choose the name of your new bucket.
* Upload these files into your bucket (right click on each link, and select Save link as...):
  * index.html
  * NextWork - Everyone should be in a job they love_files
* Files should upload in a few minutes! Choose **Close** when you see the green **Upload succeeded** banner.
* After sucessfully uploading the files you will see the following screen.
![Screenshot 2024-07-16 141359](https://github.com/user-attachments/assets/9c99c086-ead7-4bf7-8a60-a0f84f58c33b)

### Step 3: Configure a static website on Amazon S3
* Choose the **Properties** tab.
* Scroll allllllllll the way down to the **Static website hosting** panel.
* Choose **Edit**.
* Configure the following settings:
  * Static web hosting: Choose **Enable**.
  * Hosting type: Choose **Host a static website**.
  * Index document: Enter **index.html**
![Screenshot 2024-07-16 141628](https://github.com/user-attachments/assets/9601c0c6-06b7-41ae-b250-a3e200731ed8)
* After you open the link generated in the previous step, you would see the following screen.
![Screenshot 2024-07-16 142059](https://github.com/user-attachments/assets/e65d1e68-b870-4661-84b1-7b9a95cf013f)
* The error message you're seeing is telling you that your static website is being hosted by S3, but the actual HTML/image files you've uploaded are still private. It's kind of like having a bucket on display, so everyone can see the bucket - but the contents are covered up, preventing anyone from seeing what's inside.

### Step 4: Use ACLs to make objects in your S3 bucket public
* Select the checkboxes next to your **index.html** file and the folder of website assets.
* In the **Actions** dropdown, choose **Make public using ACL**.
![image](https://github.com/user-attachments/assets/7a7265af-d66f-487e-ba04-18e6701ef23b)
* Choose **Make public**.
* Once the green banner pops up, choose **Close**.
* Return to the web browser tab that has the **403 Forbidden** message.
* Refresh the tab.
* The website is successfully hosted!
![Screenshot 2024-07-16 142237](https://github.com/user-attachments/assets/b7a23ea7-033e-46bd-b89e-5e4252cbaf4f)

## Important Step: Delete your resources
* Make sure to delete all resources to avoid getting charged. This is a super important task for every single project you set up.
* Use the following guide:
  * To delete an S3 object, head back to your browser tab with the AWS Management Console.
  * Select the Objects tab.
  * Select the checkboxes next to the three objects in your bucket, and choose Delete.
  * Type delete to confirm.
  * Select Delete objects.




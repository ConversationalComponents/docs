# How to Connect your Dialogflow bot to a face on Zoom

We all have dialogs during our lives, right? Some of us even built bots on a platform called Dialogflow. Let’s say you know one of them, or maybe you’re this person (we’re not judgemental) and now you want to connect the Dialogflow chatbot to one of our publishing channels, such as Zoom. Whatcha gonna do?

## The Dialogflow Part

1. On **Dialogflow Essentials**, go to the left navigation bar, and at the top of it, pick the chatbot that you want to transfer. Click on the wheel near its name (a.k.a: Settings).

2. Under **Google project** on the next page, see the **Project ID** row? There's a Google Cloud link there. Click on it.

3. Now, open the left menu and pick **IAM & Admin**, then click on **Service Accounts**

4. Find the relevant service account (it will be an email address with the relevant account name; under Name, you need to have “App Engine default service account”)

5. Click on the three dots on the right of the same row, then click on **Manage Keys **in the drill-down menu.

6. Click on **Add Key**, then pick **Create new key**

7. Pick **Json**, then **Create**

8. The json is downloaded to your computer.

## The CoCoHub Part

9. Go to My Components on the left navigation bar, then click the + sign on the top right corner, then click **Using Dialogflow agent** in the drilldown menu

10. “Click to select or drag&drop service-account JSON file”, then upload the json file you downloaded.

11. Give your chatbot a component ID, description, name, goal. Under Categories, pick one of our predefined categories (Sales and Info, Small Talk, etc), pick a language, then click “Save”

12. Your chatbot flow is ready! Now connect it to Zoom the regular way, as we explained here.

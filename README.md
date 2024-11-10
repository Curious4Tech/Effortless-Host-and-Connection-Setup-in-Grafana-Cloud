# Effortless-Host-and-Connection-Setup-in-Grafana-Cloud
This repository offers a step-by-step guide to seamlessly adding new hosts and connections in Grafana Cloud. Simplify your data integration process and enhance your monitoring capabilities with ease.

# Adding Hosts or New Connections in Grafana Cloud

## Introduction

This guide will walk you through the steps to add hosts or new connections in Grafana Cloud, helping you to leverage your data effectively.

## Prerequisites

- A Grafana Cloud account.
- Necessary credentials for the data source you want to connect.

## Steps to Add New Connections

1. **Log in to Grafana Cloud**
   - Navigate to [Grafana Cloud](https://grafana.com/) and log in with your credentials.

2. **Navigate to Connections**
   - Once logged in, find the **Connections** option in the left-hand menu and click on it.

![image](https://github.com/user-attachments/assets/0bbe49d6-214f-4ed3-af89-72d5d696190e)


3. **Add New Connection**
   - Click on **Add new connection** to start setting up a new connection.

![image](https://github.com/user-attachments/assets/c9bed67d-a103-44a4-aeac-fbe74e44fd2e)

4. **Choose Data Source**
   - In the search bar, type **Windows** and then slect it.

![image](https://github.com/user-attachments/assets/f854fc5a-2a95-4451-a795-a9b51eb68d21)

5. **Install Grafana Alloy**

- Install grafana alloyon windows machine, here am using **Windows server 2022**


![image](https://github.com/user-attachments/assets/5205847d-caf7-4b1f-ad32-746f124a6d05)

6. **Create a Token**
   - In the new windows that is going to open, you will have to create a new token by giving it a name or use an existing one.
Then click on **Create**.

![image](https://github.com/user-attachments/assets/408246de-1f85-4ac1-b33f-3562f6875cc5)

8. **Run then script**
- It will generate a script to run on your server that you want to add. Just copy the script and go to your server, open the command with **Admin privelege** and then run the script. It will take a little bit of time.


![image](https://github.com/user-attachments/assets/18f9a995-63ed-4aa6-8b32-126504888974)


- After some few minutes, the exucution has succeeded.

![image](https://github.com/user-attachments/assets/4d227245-476a-4bdb-bca8-11ec571a19f8)


-Go back to your grafana page and click on **Test Alloy connection**

- After clicking on **Test Alloy connection**, you will a message in green as hsown on the screenshot. Click on **Proceed with the installation**


![image](https://github.com/user-attachments/assets/544c1c19-280e-4904-9da2-d3beee81065a)


- On the step 2 as provided my grafana, check logs, metrics and default


![image](https://github.com/user-attachments/assets/a6efd661-3c4c-41e8-8c30-33b3f9ec7ec8)

  
9. **Edit Alloy config file**
   - Edit the alloy configuration file to add some script, this is provided by grafana, you just have to copy and past on the alloy config file. On your command prompt, run this following (Step 3 on grafana page).
  
     ```
     notepad "C:\Program Files\GrafanaLabs\Alloy\config.alloy"
     ```

10. **Restart Grafana Alloy**
    - Once you’ve changed your configuration file, run the following command to restart Grafana Alloy.
```
sc stop "Alloy" 
sc start "Alloy" 
sc query "Alloy" | find "STATE"
```


![image](https://github.com/user-attachments/assets/2d025991-8cc0-480f-97e9-5095e3a69ddc)


11. **Test connection**
    - Go back to your grafana cloud  page and then click on **Test connection**. You will see a message in green `Integration is collecting data and sending it to Grafana Cloud`.


![image](https://github.com/user-attachments/assets/8b8191ce-8020-451e-9252-e973e12f4348)


12. **Install dashboards and alerts**

   - Just click on **Install**. This will install you pre-configured dashboards and alerts that work right away


![image](https://github.com/user-attachments/assets/cef69527-2bb3-4f5c-a4a9-bad92e1059a5)


13. **View dashboards and alerts**

Click on either **View dashboards** or **View alerts and recording rules** based on what you want to see right away.


![image](https://github.com/user-attachments/assets/335b09af-e288-4c30-bea5-348378bb5336)


Now you can start monitoring your Windows server 2022 metrics and logs


![pic1](https://github.com/user-attachments/assets/729686f5-ff41-44da-a4ab-05102073d884)


## Conclusion

By following these steps, you can easily add new connections or hosts in Grafana Cloud, allowing you to visualize and analyze your data effectively.

If you have any questions or run into any issues, feel free to reach out for further assistance!

---

Happy visualizing! 🎉


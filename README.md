![image](https://github.com/user-attachments/assets/5329459b-e1f6-407a-939c-e834aa5f7a74)# Investigating-with-ELK-101

![image](https://github.com/user-attachments/assets/7ab5c6ec-f157-45e5-9840-85a9f025dce7)


## Introduction

As I progressed through my journey in cybersecurity, I moved from Endpoint Security Monitoring to exploring Security Information and Event Management (SIEM). While I had some prior experience with Splunk, I was eager to dive into a new SIEM tool: the ELK Stack. This was my first exposure to ELK, and I was excited to learn more about it. This project write-up captures my hands-on experience with ELK through a series of tasks designed to deepen my understanding of its capabilities.
Task 3: ElasticStack Overview

I began with an overview of ElasticStack, specifically focusing on the roles of Logstash and Kibana.

Task 3 ElasticStack Overview

    Logstash is used to visualize the data. (yay/nay)
        This is actually Kibana’s function.
        Answer: Nay

    Elasticstash supports all data formats apart from JSON. (yay/nay)
        Contrary to the statement, Elasticstash supports JSON.
        Answer: Nay

Task 4: Kibana Overview

![image](https://github.com/user-attachments/assets/deb9ae89-cdff-4618-beb6-b6f07166d9c9)

After ensuring I was connected to TryHackMe’s network using a VPN, I accessed Kibana via the provided IP address.
Task 5: Discover Tab

Here, I explored the Discover tab in Kibana, which allowed me to filter and analyze data.


![image](https://github.com/user-attachments/assets/5059370d-94cf-4681-a4d5-b55fd9be6ec8)

![image](https://github.com/user-attachments/assets/c374888e-238b-4955-a823-24c096bc20b8)

![image](https://github.com/user-attachments/assets/e5f3747d-95fd-430e-bd52-e09e5bedcd88)


    Select the index vpn_connections and filter from 31st December 2021 to 2nd Feb 2022. How many hits are returned?
    Answer: 2861

    Which IP address has the max number of connections?

    ![image](https://github.com/user-attachments/assets/fe4a6610-e7f3-4243-843e-79f699f1f233)

    Answer: 238.163.231.224

    Which user is responsible for max traffic?

    ![image](https://github.com/user-attachments/assets/1cc54c73-b731-40ad-a565-e7adaf2056b2)


    Answer: James

    Create a table with the fields IP, UserName, Source_Country and save.

    ![image](https://github.com/user-attachments/assets/f4dece30-6eea-4221-b771-ea80ab792f13)

        I created a table that displayed the fields of interest by expanding results and toggling the columns in the table.
        
![image](https://github.com/user-attachments/assets/33fa702a-c29d-4b31-bac7-742ddb0d8181)

    Apply Filter on UserName Emanda; which SourceIP has max hits?
    
    ![image](https://github.com/user-attachments/assets/87aa4d10-af6e-4a1f-a22f-7840a19572b8)

    Answer: 107.14.1.247

![image](https://github.com/user-attachments/assets/d1cdfdae-4f87-4764-b9b9-7e303d504ee5)


    On 11th Jan, which IP caused the spike observed in the time chart?

    ![image](https://github.com/user-attachments/assets/fb99c561-8287-4521-a0d6-9425ba28e84d)
![image](https://github.com/user-attachments/assets/398ad482-17b0-4823-94a0-557f3f745abf)

    Answer: 172.201.60.191

    How many connections were observed from IP 238.163.231.224, excluding the New York state?
    Answer: 48

Task 6: KQL Overview

In this task, I practiced creating search queries using Kibana Query Language (KQL).

    Create a search query to filter out the logs from Source_Country as the United States and show logs from User James or Albert. How many records were returned?
    Answer: 161

    As User Johny Brown was terminated on 1st January 2022, create a search query to determine how many times a VPN connection was observed after his termination.
    Answer: 1

Task 7: Creating Visualizations

Visualizations are crucial for analyzing and interpreting data effectively.
![image](https://github.com/user-attachments/assets/c94427c2-b04e-491c-bfb0-5fe4c8a5f4fc)

    Which user was observed with the greatest number of failed attempts?
    Answer: Simon


    How many wrong VPN connection attempts were observed in January?
    Answer: 274

Lab Work

In the static lab attached to this project, I explored a sample dashboard displaying various events and alerts triggered by suspicious activities. Here’s a summary of the lab work:

    Which process caused the alert?
    Answer: cudominer.exe

    Which user was responsible for the process execution?
    Answer: chris.fort

    What is the hostname of the suspect user?
    Answer: HR_02

    Which term matched the rule that caused the alert?
    Answer: miner

    What is the best option that represents the event?
    Answer: True-Positive

Conclusion

This room provided me with valuable exposure to the ELK Stack as a SIEM tool. I found ELK to be somewhat more intuitive than Splunk, though this may be due to the introductory nature of the exercises. I particularly appreciated how beginner-friendly the filtering process in Kibana was. I look forward to applying what I’ve learned in more advanced scenarios.

Can't wait to utilize what I learned in the next challenge!

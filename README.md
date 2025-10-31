# ETL-in-Python
A simple ETL process created in Python for practice.


In this practice project, I wanted to create an ETL process by only using Python. 
In my latest project using raw Spotify data, I used Excel, SSIS and Python for data transformation and SQL for data cleaning. That’s one too many tools for the job, right? Gladly I learned how to go through this process by only using Python. 
I also couldn’t find any easy project or file in the internet going through this process, so here I am!

What are we going to do? I learned how to create a basic ETL process using Python, I have a raw Spotify data waiting to be used. We’ll get to know our data and start defining functions for the process.

Our Data:

<img width="860" height="169" alt="stream history files" src="https://github.com/user-attachments/assets/b25ce98f-40e7-4aa6-b90a-f9369fe77eab" />

We have 5 different json files, holding an extensive music and podcast streaming data. Before we start the process, we should check out the information about our data

<img width="913" height="581" alt="a look at our data" src="https://github.com/user-attachments/assets/a2e04880-35bd-4373-a65b-72f6f5750eb4" />

As we check our dataset, we can see some problems that we have to solve during transformation phase

Phase 1: Extract

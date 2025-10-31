# ETL-in-Python
A simple ETL process created in Python for practice.


In this practice project, I wanted to create an ETL process by only using Python. 
In my latest project using raw Spotify data, I used Excel, SSIS and Python for data transformation and SQL for data cleaning. That’s one too many tools for the job, right? Gladly I learned how to go through this process by only using Python. 
I also couldn’t find any easy project or file in the internet going through this process, so here I am!

What are we going to do? I learned how to create a basic ETL process using Python, I have a raw Spotify data waiting to be used. We’ll get to know our data and start defining functions for the process.

To see the detailed coding with explanations, see the file ETL-PROCESS-TEST

Our Data:

<img width="860" height="169" alt="stream history files" src="https://github.com/user-attachments/assets/b25ce98f-40e7-4aa6-b90a-f9369fe77eab" />

We have 5 different json files, holding an extensive music and podcast streaming data. Before we start the process, we should check out the information about our data

<img width="913" height="581" alt="a look at our data" src="https://github.com/user-attachments/assets/a2e04880-35bd-4373-a65b-72f6f5750eb4" />

As we check our dataset, we can see some problems that we have to solve during transformation phase

Phase 1: Extract

<img width="793" height="44" alt="extract" src="https://github.com/user-attachments/assets/1485b40c-0d5d-41fe-9b16-873c59a3faf0" />

If the dataset is in your notebook’s system files, you can use the files’ name. If not, you can use the file path to access.
This function will allow us to read the json file by showing Python where the data is located.

Phase 2: Transform

We got the required information from our dataset by running dataframe.info(). I advise going through the columns by seeing the head or tail of the data. I didn’t give place to them because ip_addr is revealing my ip address.
Problems with this dataset is that:

1- ts column holding date and time information is not in the correct format and data type. We have to correct it and extract date and time into separate columns.

2- We have too many unnecessary columns starting with conn_country and ip_addr. Start by removing them from the dataframe.

3- Some column names are too long to be properly used, renaming them can be useful in further steps.

4- The dataset holds both music and audiobook/podcast data. We should separate by filtering them if we wish to get only one part of it.

5- We should check the data again, see which columns can be used for analysis and get rid of the remaining unnecessary ones.

<img width="1102" height="576" alt="transform" src="https://github.com/user-attachments/assets/b6f36fc2-a1b1-4603-b7f3-2ee74df7ee23" />

Phase 3: Load

With Python, you can save your data in various different formats. For his project, I’ll be using a .csv file to store my data.

<img width="941" height="628" alt="load" src="https://github.com/user-attachments/assets/3db56c58-ac27-4365-a2cb-81f3bc52b7c5" />

Phase 4: Connecting the Pieces

We have 5 different files to load into one single file. We have to create another function to run with our current functions, take them as a whole and make the process cleaner and easier.

<img width="894" height="703" alt="etl f" src="https://github.com/user-attachments/assets/489912b2-850c-4435-bd1e-9de3f2449889" />



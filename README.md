# Onemap_Analytics
I learned about OneMap through my work, as we needed to integrate its Map Service into our projects. During this process, I discovered the Population Query section, which offered a wealth of information. This sparked my interest to collect this data and store it in my S3 Bucket for further analysis and use.

## Collecting our Data
### Setting up AWS S3 Bucket

<img width="1616" alt="image" src="https://github.com/caizhitan/OneMap_Analytics/assets/150103035/917d0a85-79b5-42d6-880b-c630addee2b2">

Here is my S3 Bucket `onemap-s3` with all the categories of data as my file structure. As the Data is not continuously updated, there was no reason to setup a AWS Lambda Function to automate this data collection process. 

## Using Python Requests library
There are two ways to perform API calls:
- Synchronous Requests (slow)
- Asyncronous Requests (fast)

### Synchronous Requests
Synchronous requests are processed sequentially, meaning each request is sent and must be fully completed before the next request can begin this can lead to delays. However the positives of using Synchronus requests is that this method ensures each task is finished in order.

### Asyncronous Requests
Asyncronous requests are processed in parallel, without waiting for one to complete before starting the next. This leads to overall faster speeds when collecting api data. 

### Video Demo of Synchronous vs Asyncronous Requests

[![Watch the video](https://github.com/caizhitan/OneMap_Analytics/assets/150103035/5c461e47-5c85-42db-9df4-845f332a9a08)](https://www.youtube.com/watch?v=gAG4koLhJOI)

As we can see the data collected on the left (Syncronous) processes them one-by-one. The data collected on the right (Asyncronous) is faster and in parallel.

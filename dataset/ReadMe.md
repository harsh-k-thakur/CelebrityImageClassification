# How to store the data-set

One way is to just download the data-set from my [google-drive](https://tinyurl.com/IndianCricketTeamData).
The data-set is divided into 3 folders. 

## 1. Folder 1: pre_processed_data

In this folder, the dataset I have saved is after cleaning through python and manually deleting some wrongly classified images.

  ### a. Data Collection
  
  If you have this dataset you can skip the [data_collection.ipynb](/code/data_collection.ipynb) and [data_cleaning.ipynb](/code/data_cleaning.ipynb).
  In which the first file is used to understand the concept of Data Scrapping with Selenium.
  Google changes their elemnt id so this might not work in future.
  But this is good way to understand basics of data-scrapping using python.
  
  ### b. Data Cleaning
  
  I have used Haarcascasde in order to detect faces.
  Once we have the (x, y, w, h) of the face we can go ahead and detect eyes.
  I tried to make it simple but cleaning the data in an effective way so that in my training phase model works well.
  Thus faces with two eyes visible will be stores in the pre_processed_data.
  
## 2. Folder 2: raw_data

in order to create raw data i have used [data_collection.ipynb](/code/data_collection.ipynb).
Again, this is done using Selenium, if the element id changes, might or might not work in future.
This contains all the images from the google query.

## 3. Folder 3: trail_data

This is just the trail data used to do certain maniupulation and testing if the data cleaning method is working.
Once the data-cleaning method is working for 3-4 images. 
It should basically work for every images in pre_processed_data folder.

# IDS-BLUProject
 Github repo for the Bike Lane Uprising class project

#Requirements 
(from Sergey's project Readme)
"The final project should represent original work applying data science techniques to an interesting problem. You own your final projects, but you should be talking frequently with your instructor and classmates about them."

"Address a data-related problem in any field you're passionate about. If you care about the subject matter, you'll create a better project and it will be a lot more fun for you!"

"You can either use [publicly available data](public_data.md) or your own data that you can legally share with the rest of the class. Competing in a data science/stats competition (INCLUDING ANY PAST COMPETITIONS) is also a project option."

#Introduction: 
This project will analyze a publically available data set to determine if traffic tickets being issued in Chicago for obstruction of bike lanes are actually correlated with complaints of bike lane obstruction in that city.  I am working with Bike Lane Uprising to assist me in identification of datasets and geoidentification.  https://www.bikelaneuprising.com.  

#Update8-5: 
Given the time constraints, I have only been able to perform an analysis of the first set (ProPublica)

#Update8-12
Today I discovered the dataset I've been using 


For this, I have two publically available datasets.  


#Dataset #1: 
ProPublica's analysis of Chicago traffic ticket issuance.  This data can be downloaded at: https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data.  I have included the data compressed in  my repository, but I believe it will not be posted when I make the repo public as it exceeds the size requirements.  

#Dataset #2: 
311 Service Requests: https://data.cityofchicago.org/Service-Requests/311-Service-Requests/v6vf-nfxy

#Geographic identification
 (for mapping tickets to their location): City of Chicago's Data Portal for geographic identirication (the City Data Portal a lot of cool public data and Github repositories!): https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw
    
**write-up** 
    1. What is the question you hope to answer?

The purpose of this data analysis is to determine whether there is a way to improve public safety by 
identifying areas of bike lane obstruction (as represented by the 311 complaint database) and correlating it with the actual tickets being written (represented by the ProPublica data).  The city also has the opportunity to increase revenue through parking tickets by identifying places where there are bike lane obstructions.  

    2. What data are you planning to use to answer that question?

The parking ticket data being utilized is from the ProPublica data set.  https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data

The bike lane obstruction data is from the 311 data.  https://data.cityofchicago.org/Service-Requests/311-Service-Requests/v6vf-nfxy

The geographic maps of the area are from the City Data Portal.  https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw

    3. What do you know about the data you're using so far?

The ProPublica data:

The data that ProPublica obtained from the City of Chicago was enriched by interviews with the Finance Department in order to establish the data dictionary.  The license plate numbers are hashed to anonymize the data.  

In terms of the features available for this dataset, the zipcode data is unstructured.  There are some Zip plus 4 data and some 5 digit zipcode data.  Review of the data dictionary reveals that rather than containing the violation_location zipcode, in fact, it contains the zipcode of the vehicle registration.  


    4. Why did you choose this topic?

    
    If it's not practical to include your entire dataset in your GitHub repository, you should link to your data source and provide a sample of the data. (GitHub has a [size limit](https://help.github.com/articles/what-is-my-disk-quota/) of 100 MB per file and 1 GB per repository.)


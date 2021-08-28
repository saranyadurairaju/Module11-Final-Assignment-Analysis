# UFO Analysis with Javascript

* HTML is the markup language that we use to structure and give meaning to our web content, for example defining paragraphs, headings, and data tables, or embedding images and videos in the page.

* CSS is a language of style rules that we use to apply styling to our HTML content, for example setting background colors and fonts, and laying out our content in multiple columns.

* JavaScript is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else. (Okay, not everything, but it is amazing what you can achieve with a few lines of JavaScript code.)

## Overview of Project

Dana is a data journalist who got a chance to write about her hometown McMinnville, Oregon where UFOs are important topic. This city is famous for its sighting and even has an annual gathering of UFO enthusiasts. Also, Dana has been interested in this topic since her childhood. She has a Javascript file with sighting information like datetime, countries, cities, states, shape, duration and other details. With this file Dana is going to create a UFO sighting details in a neat webpage. Below is the story board for the webpage: 

![image](https://user-images.githubusercontent.com/85472349/131205437-0158d724-e9f8-4d87-9914-0fee8ef572c3.png)

## Analysis 

Dana can create a basic details of the webpage and bring a intial webpage of UFO sighting. Now the important part is to create a table with the data file we have and to provide a more in-depth analysis of UFO sightings by allowing users to filter for multiple criteria at the same time.

Before we start doing our Analysis, we need to set the basic HTML tags with existing information in index.html file. Also, in app.js we can set the variable values and buildTable function. The upper part of the webpage will look like below: 

![image](https://user-images.githubusercontent.com/85472349/131206203-3ec0d675-f26d-4fc1-afad-e7e0bfdd62fb.png)


### Filter UFO sightings on multiple criteria

We are creating a u1 and li (list elements) html tags for each search criteria like **Date, City, State, Country and Shape** with id and place holder to use it in our .js file. 

![image](https://user-images.githubusercontent.com/85472349/131206292-ca76a086-ee1b-478c-8545-2fbf5a4ba040.png)

And we event listener to detect changes to each filter ![image](https://user-images.githubusercontent.com/85472349/131206523-a3cd4aec-6ea7-4b7f-b4a6-a812714f2819.png)


**The updateFilters function:**

In this function we save the element, value, and the id of the filter that was changed in the 5 search criterias:

![image](https://user-images.githubusercontent.com/85472349/131206490-2f154f9c-1a99-4443-9b1d-1bd23de22d7b.png)

**The filterTable function:**

In filterTable() function we loop through all of the filters and keeps any data that matches the filter values from the original data file.

![image](https://user-images.githubusercontent.com/85472349/131206545-b814865a-2d60-462a-843d-96d934319305.png)

So after the update in the app.js and index.html files we are ready with table values and filters. So, the default webpage table will look like below image:

![image](https://user-images.githubusercontent.com/85472349/131206636-4e715f06-d755-4e3b-bdbc-304c5abb362b.png)

## RESULTS

The webpage is looking nice with the data values in table with multiple search criterias. We can search for values in different ways like below:

### Date filter

We are filtering the data with the date criteria. As we have only one record with 1/3/2010 date, we can see the result in the table after entering it.

![image](https://user-images.githubusercontent.com/85472349/131206851-9f40a8c2-1a48-4964-b8c8-f22d1fca7db9.png)

### Date, Shape filter

When we give date as 1/12/2010 and shape as disk, we are getting single record which match the criteria. Other filter values are sample values we are giving in "li tag" placeholder element. And note that it won't be the filter criteria:

![image](https://user-images.githubusercontent.com/85472349/131206885-cd69c961-2308-4a06-b4b6-263b9af68179.png)

### Empty table

The table will show the empty values or we can show No values will be displayed when the criteria is not matching. For example in the above criteria we have only one record with has State as "wi". But if we try to filter with State "ca", we will get empty table as there is no record which match all three criterias (date:1/12/2010, Shape:disk, State:ca).

![image](https://user-images.githubusercontent.com/85472349/131207031-327bd2ec-db58-49f8-849b-9226cbca7b26.png)

Like the above filters, we can do many other combination of filters to find the values we are interested. 

## SUMMARY

However the webpage looks nice with data and the filters are working perfectly, we can always do more things to make it better or work for all situations etc. Below are few drawback and recommendations.

### Drawback

1) Search criteria values are not very clear:

Not all the users will come up with proper search criteria values or we can say some users won't be having the search values. In that case, they need to go through the full table values to find what they need to enter in the search boxes.

2) Matching the filter values with original data:

When we are matching the filter values with the original data values, we are simply comparing it. So, we need to enter the exact value as in data. We can use Slicing or case sensitive methods to show the data when users are entering half of the value or entering any upper or lower case letters.

For example if we consider city "london (canada)", we need to give the exact same value in city filter. If we give "london" or "London (canada)", it will give us empty table.

![image](https://user-images.githubusercontent.com/85472349/131207456-94e972a4-a89c-4b14-8498-ce74025c575e.png)

![image](https://user-images.githubusercontent.com/85472349/131207432-7f602f82-4a95-4577-9bc7-daf0524ac347.png)

![image](https://user-images.githubusercontent.com/85472349/131207443-a1efc150-73d1-4af4-809e-d890c86a9632.png)

### Recommendations

1) Drop down values for criteria

If we have a list of drop down values for each criteria, then it will be very easy for the users who are coming to search about UFOs to enter/select the values they are interested. Also they will have a option for many combination of values which will help them to learn more. 

2) Data update from web for more details

For this webpage we used a fixed data in data.js file which is displayed and filtered according to criteria. But we can make this webpage to generic and list all the latest news and details of UFO if we fetch the data from web using scrapping or other techniques. In that case we need to do changes in our code to display the data in pages and filter criteria accordingly. But after doing all these this Webpage will definitely be one of the important sites for UFO. 

## Full Final Webpage

![image](https://user-images.githubusercontent.com/85472349/131207695-c6ff2607-e760-44b7-8c5e-fe17be711817.png)

**DANA is very proud and happy for her work as a journalist especially in her town and her favorite topic UFO sightings !!!**


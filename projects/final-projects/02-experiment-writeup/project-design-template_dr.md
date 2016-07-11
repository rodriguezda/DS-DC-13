# Project Design Writeup and Approval Template

### Project Problem and Hypothesis
Well-articulated problem statement with "specific aim" and hypothesis, based on your lightning talk

'''My goal is to take 2016 YTD NYC Airbnb renter/rentee data (listings.csv + calendar.csv) and use it to identify which properties are "hot", as in, which properties are the most desired and "rentable", and identify the attributes that contribute to that status. This is not an analysis of the top grossing properties, this analysis is meant to determine the "best" properties and their criteria.

My hypothesis based on the lightning talk is that top properties (homes, apartments, condos, boats, etc) are properties that on average, have the least amount of availability per week/month/year. At this time, I have not identified any other relevant attributes that help define what a top property is, but I am obviously continuing to investigate.'''   

Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?
'''Machine learning is essentially pattern recognition. If we can create a model for "hot/top" properties, we can use it to predict marketability/success for new ones. there is a spectrum of success, but i think we're predicting a binary value: is it "hot," or is it not?'''

What kind of impact do you think it could have?
'''there are a lot of applications for this. As a renter, if your property  was marked as a "top" property, it would incentivize you to maintain that status, for the benefit of making more money. if "popularity" was a factor in denoting status, it would incentivize renters who don't have top properties to open up availability, which is better for rentees. for airbnb, having a quantifiable way of identifying top properties (and property owners) can have advocational value.''' 

### Datasets
Description of data set available, at the field level (see table)

'''my central dataset, from which I am pulling features, is a june 2, 2016 scrape of airbnb data from here: http://insideairbnb.com/get-the-data.html

There are two relevant files form which I can source data. listings.csv and calendar.csv. Listings contains over 90 data points about the property (id, availibility, price per night, location, transit, house rules, description, number of reviews), the host (name, their location, "host since," response time). Calendar denotes their availability over a given month, and how much it costs per night. you can essentially use this info to tabulate how many days per month (in our case it's june) it's being rented, and how much money it's made that month (as far as cost goes). I know cost is a factor for a lot of consumers, in determining whether a property is even rented or not, and there will be a bit of hard coding necessary to identify the average profit of a property per month in order to create a usable number for modeling. '''

### An outline of any potential methods and models
'''I believe my data science project is a classification problem. A classification and class probability probelm attempts to predict, for each item in a population, to which class does this thing belong to. In my case, the there we will identify a pull of hot properties from which we can pull insights from.

Detailed explanation of extant data available (ie: build a data dictionary or link to pre-built data dictionaries)
Describe any outstanding questions, assumptions, risks, caveats
Define your goals and criteria, in order to explain what success looks like


### Domain knowledge
* What experience do you already have around this area? Include specific features or relevant benchmarks from similar projects
'''none. I've never created a model for airbnb data or residential data.'''

### Project Problem and Hypothesis
* What's the project about? What problem are you solving?

There's a lot to be learned qualitatively and quantitatively from properties that are profiting the most, or  have no way of rewarding 
* Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?
* What do you think will have the most impact in predicting the value you are interested in solving for?

### Datasets
* Description of data set available, at the field level (see table)
* If from an API, include a sample return (this is usually included in API documentation!) (if doing this in markdown, use the javacription code tag)

   
### Project Concerns
* What questions do you have about your project? What are you not sure you quite yet understand? (The more honest you are about this, the easier your instructors can help).
'''I don't understand how much profitability is going to be a factor, as far as modeling goes. I think the only way to know is to calculate monthly profits for a property, and then go from there. it could be that availability (or lack of) plays a bigger impact than profit. only one way to find out...'''
* What are the assumptions and caveats to the problem?
* What data do you not have access to but wish you had?
'''Weekly/monthly profit. but a number can be calculated at 30, 60, 90, 356 day intervals with the data at hand.'''
        
* What is already implied about the observations in your data set? For example, if your primary data set is twitter data, it may not be representative of the whole sample (say, predicting who would win an election)
'''this dataset is limited to new york city. but the model theoretically could be applied to other cities as well.'''
* What are the risks to the project?
    '''n/a'''
* What's the cost of your model being wrong? (What's the benefit of your model being right?)
'''there are benefits to creating a model. and they benefit the consumer, the hosts and airbnb.'''
* Is any of the data incorrect? Could it be incorrect?
'''this data was scrapped and cleaned by the scrapper. there are null values throughout, but they are few.'''

### Outcomes
*Define your goals and criteria, in order to explain what success looks like
'''we'll be able to identify how many top properties exist in the nyc market, and the attributes that make them that. we should be able to apply the model to other cities (say washington dc) and identify similar attributes in those properites as well.'''

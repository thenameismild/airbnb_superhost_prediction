# Airbnb Superhost Prediction

### Introduction
We are interested in exploring Airbnb as a business and explore what problems the business might need solving. We will be exploring the data, data
mining and answering business questions using Python programming.

### Business Understanding
Airbnb is a community-based, two-sided online marketplace that facilitates and connects
people who want to rent out their home with people who are looking for lodging in a specific
location around the world. On the Airbnb platform, there are 2.9 million hosts worldwide and
more than 7 million listings in over 200 countries, with more than 150 million users. This means
that their biggest assets are the individuals and the hosts, where their revenue is from:
 - Commission host: Everytime guest makes payment, Airbnb takes 10% of the payment
amount as commission.
- Guest Transaction fee: When travelers make payments for stays, they are charged a 3%
fee for the transaction.

Since the hosts are the base of Airbnb business model, we want to help Airbnb better
define who are qualified to be a superhost. Superhosts are hosts that provide outstanding
hospitality, which means being highly-rated, experienced, reliable, and responsive. We notice
that the definition of a superhosts is vague without any qualitative values to base on. We want to
explore what features make a superhost, and if there are any features that are weighted more
than others. This would also allow us to use the findings to help the host better align themselves
to become superhost on Airbnb.

The business question we are trying to answer is: **“What criteria can be used to more effectively identify and qualify Airbnb hosts as Superhosts?”**

### Data Understanding
As mentioned in the introduction, we are using Airbnb’s data from the listings in the
United States. We have obtained the data through insideairbnb.com. For feasibility of the project
we decided to focus on the west coast data, which contained 131,388 observations and 58
variables. It contained 6 States in the west coast which consisted of: California, Colorado,
Hawaii, Nevada, Oregon, Washington and 14 cities between the states. In the target variables
there are 45,595 superhosts and 85,793 normal host. Therefore, as this is a classification
problem, the base rate is 34.7% for the positive class.

Our problem is a supervised classification problem, where we will identify if a current host
is a superhost or not. The features we wil be using includes:
- Property features
  - Description (long-text), property type
  - Location
  - Amenities & Rooms
  - Booking availability
  - Ratings
- Host features
  - Response time, response and acceptance rate
  - Host tenure
  - Host description (long-text)
  - Host listing count

We believe features related to review scores, host response & acceptance rate, and availability
are most useful as it seems to relate with the definition that Airbnb gave of what makes a
superhost.

### Modeling Approach
As there are two types of data we are working with, we decided to split the classification
method into two phase, classification using numerical data and classification using text data. We
believe that this will give us a better understanding of the data and what are the qualities that
Airbnb looks for in a superhost.

The classification using numerical data will be able to provide us with features that are
important for a superhost in Airbnb, while classification using text data will give the host an idea
of what a superhost property looks like.

### Model Evaluation
Evaluating superhost classification, we have to cosider the false positive and false
negative impact on Airbnb, the hosts and the guests. False positives (predicting a host as a
superhost when they are not) can lead to disappointment and dissatisfied guest. False negatives
(predicting a host as not a superhost when they are) could lead to upset host who might not get
the recognition they deserve. In this case, precision is more important as false positive have a
larger impact on the cost of the business more than false negative. This is because unhappy
guest can cost Airbnb, as the guest may not return to the platform or pivot to hotels. However,
false negatives.

We chose to proritze our evaluation metric on precision, because it is more costly when
there an incorrect prediction of a superhost is made. Precision focus on the proportion of
correctly predicted superhosts among all the positive predictions. A high precision score
indicates the model making fewer false positives predictions.

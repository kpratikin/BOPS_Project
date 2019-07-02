<b>Buy Online and Pick Up in-store Strategy for Jewelry Retailer </b>
 
<b>Background:</b><br> 
In the era of digital economy, traditional retailers are adopting innovative strategies to better serve their customers. In the past we have observed that retailers have introduced online channels along with their traditional brick-andmortar channels to increase sales. Originally, these channels are kept separated from each other. However, many retailers are now adopting integration strategies (i.e. both Online-offline) to enrich the customer value proposition and/or reduce costs.

Online-offline integrations can be achieved in different ways. One such strategy that is popular among retailers is the option to buy products online and pick them up in store (BOPS) strategy. In this strategy, the retailer shows online viewers the locations at which the items are available and gives customers the option to close the transaction online and then pick up the products at one of the retailer’s locations shortly after closing the purchase.

BOPS provides tangible benefits to both consumers and retailers, as per eMarketer's website "with BOPS, Consumers get convenience, instant gratification and avoid shipping costs. Retailers reduce operational costs, and it gives them the opportunity to bring customers back to physical stores for additional purchase opportunities.” There has been a lot of traction in this space and more than 90% of the retailers plan to implement BOPS by 2021. But one must question, whether this strategy really works? In order to answer we conducted below analysis to extract the truth based on the available data. 
 <br><br>
<b>Business objective of the analysis: 
<br>To evaluate <br>
1. What is the impact of implementing BOPS strategy on online channel sales?  
2. What is the impact of implementing BOPS strategy on online channel returns? 
 </b>
 
 <b><br>
About available data:</b><br>
The data is from national jewelry retailer (In order to maintain confidentiality, the name of the company is not disclosed). The data covers all online transactions made between August 1st, 2010 and July 31st, 2013. 

<p align="center"><img src="https://github.com/kpratikin/BOPS_Project/blob/master/Data%20availiability%20and%20timeline.PNG">
 <br>Figure: Data Timeline
 </p>
 
 There are three online channels. Store number for these channels are 2, 6, and 5998. 
 <ul><li>Online channels 2 and 6 started the BOPS strategy on August 1st, 2011.</li> 
<li>Online channel 5998 started the BOPS strategy on September 27th, 2012.</li></ul>
<br>
<b><ul><li>TRANSACTION LEVEL DATA:</b> This dataset includes all transactions made between August 1st, 2010 and July 31st, 2013.
<b><li>CONSUMER LEVEL DATA:</b>  This dataset includes the purchase information of all customers who both made at least one purchase before the BOPS implementation and made at least one purchase after the BOPS implementation  
<b><li>ONLINE LEVEL DATA:</b> Online daily sales-returns dataset includes sales and returns at each online store for a given day.</ul>
<br>
 
<b>Methodology for evaluating the impact of BOPS</b><br>

One approach to evaluate impact of BOPS is to look at the difference in variables of interest between pre-implementation and post implementation period. However, this approach will not give us the right answer because many things differ between the pre-implementation and post-implementation periods that are completely unrelated to implementing BOPS. For example, you might observe change in sales because of other external factors like seasonal effects, economic condition in that periods etc. To deal with this challenge, we consider difference-in difference approach.

For difference in difference approach, we need to have control and treatment groups. For this, we divided time period into dummy variable (i.e. Time Dummy where 0- indicates period where BOPS is not implemented (in any of the stores) and 1- indicates period where BOPS is implemented (in stores 2&6 but not in 5998)). Here stores 2&6 are treatment groups (store dummy-1) and store 5998 is control group (store dummy-0). 

<p align="center"><img src="https://github.com/kpratikin/BOPS_Project/blob/master/timeline%20and%20treatment.PNG">
 <br>Figure: Timeperiod
 </p>

<p align="center"><img src="https://github.com/kpratikin/BOPS_Project/blob/master/impact%20of%20bops.PNG">
 <br>Figure: Difference in Difference approach to capture 'Impact of BOPS on sales'
 </p>

Figure above, indicates how we captured the impact of BOPS keeping every other factors as constant. If the control and treatment groups does not change their slopes (from pre-implementation (Time Dummy=0) to post-implementation (Time Dummy=1) i.e. they slopes are parallel), then it indicates that there is no impact of BOPS on sales/returns. However, if we observe change in slope between pre-implementation (Time Dummy=0) to post-implementation (Time Dummy=1) period (i.e. for stores, where BOPS implemented we observed slope change as compared to store where BOPS are not implemented) then this change is because of BOPS strategy.

<br><b>Analysis:</b>
Refer code - https://github.com/kpratikin/BOPS_Project/blob/master/BOPS.rmd

<br><b>Conclusion & Suggestions:</b><br>
Our analysis of the impact of BOPS strategy on online sales and returns shows that online sales and returns do not increase with the implementation of this strategy. It rather decreases. 

<p align="center"><img src="https://github.com/kpratikin/BOPS_Project/blob/master/Conclusion.PNG">
 </p>


One of the anticipated reason behind this decrease is ‘Channel-Shift’ effect i.e. after checking the product online, customers are visiting nearby stores to buy that product, instead of buying it online. This corroborates with the consumer behavior phenomenon i.e. research online, purchase offline. Because of this effect, we may be observing decrease in online sales/returns but if we include offline sales/returns data in our analysis, we may observe that there is net increase in sales/returns. Therefore, we recommend to include offline store data for the analysis to come up with the net impact of the BOPS on overall sales and return instead of focusing on one channel.

<br><b>References:</b>
<ol><li>Santa Clara University: OMIS 2392 – Econometric for Business Analytics with R Course – Dr. Necati Ertekin.
<li>eMarketer : What Do Shoppers Want from BOPUS?
<li>Invespcro: Buy Online Pick Up In Store – Statistics and Trends
<li>Santiago Gallino, Antonio Moreno (2014) Integration of Online and Offline Channels in Retail: The Impact of Sharing Reliable Inventory Availability Information. Management Science 60(6):1434-1451. https://doi.org/10.1287/mnsc.2014.1951
<li>Gao, F., & Su, X. (2017). Omnichannel Retail Operations with Buy-Online-and-Pick-up-in-Store. Management Science, 63 (8), 2478-2492. http://dx.doi.org/10.1287/mnsc.2016.2473 </ol>

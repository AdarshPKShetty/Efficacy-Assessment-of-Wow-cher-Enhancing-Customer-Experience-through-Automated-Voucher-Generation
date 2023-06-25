# Efficacy assessment of Wow-cher:Enhancing customer experience through automated voucher generation
Case Study for Senior Product Analyst
— Context —
At a food delivery company x, we aim to delight our customers with the quickest on-demand delivery for any choice of products. Sometimes, there are delays caused by a variety of factors: higher demand at vendors, availability of riders who make delivery or other region-specific causes. When that happens, we strive to do right by our customers and provide compensation in the form of vouchers to mitigate the negative experience and incentivise future orders.
In order to streamline this compensation process, we have built a new in-house product called “Wow-cher” to automate voucher generation based on certain predefined criteria.

— Instructions —
The Wow-cher Product Manager and senior leadership team of x’s Service tribe want to know if/how this product is helping improve the customer experience. Please use the attached data files to solve the following tasks and put together a 4-6 slide presentation with your findings.

Tasks
A. Based on the available data, visualize a simple funnel that you would recommend the Wow-cher product manager to use. Calculate relevant metrics and present them alongside your funnel.
B. Determine whether Wow-cher is helping improve the customer experience by using customers who did not receive compensation as a control group.
C. Explorecountryandcustomer_value_index.Summarizeyourfindingsandany recommendations you would give to the product manager.

Besides the specific tasks listed above, feel free to include any additional insights you uncover from the data.
Include any assumptions you have made and whether additional data could have helped. Call out any data issues you observed. Separately include all code and files you built as part of the analysis.

Tools/Technologies
Use SQL for data manipulation. You can access and query the data-sets via BigQuery web console, using the google account associated with your email address.
The choice of tooling for visualization is up to you.

— Data —
The data-sets are located under dh-interview-case-study:logistics_service_product_analytics.

Data-set: orders
Description: Daily aggregates of orders per country Fields:
- date : date of the order
- country : country in which the order was placed
- orders : aggregated number of orders
  
Data-set: events
Description: Order delays for which the Wow-cher API was called to determine compensation Fields:
- event_id : unique identifier of the delay
- event_ts : time at which the delay occurred
- event_type : description of the delay
- customer_id : unique identifier of the customer who placed the order that got delayed
- country : country that the delayed order was placed in
- action_type : action taken by Wow-cher
- voucher_id : unique identifier of the voucher issued, if any
- customer_value_index : numerical index between 1-4 based on the predicted life-time
value of the customer (4 is highest, -1 means not available)

Data-set: customer_surveys
Description: We send satisfaction surveys to some of our customers after they placed an order with us. The data-set holds survey responses.
Fields:
- survey_id : unique identifier of the survey
- survey_response_ts : time at which the survey was filled out
- customer_id : unique identifier of the customer who filled out the survey
- survey_rating : 1 if the customer was satisfied, 0 if the customer was unsatisfied

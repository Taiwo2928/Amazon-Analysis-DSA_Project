# Amazon-Analysis-DSA_Project
My first project on Excel workbook Analysis

 ## Project Topic: Amazon Product Review Analysis
 ### Project Overview
 I was given an Amazon Product excel data set of 1,465 rows and 16 columns.
 Role: Junior Data Analyst
 ### Aim 
 Analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.
 
 ## Mode of Analysis
      - Microsoft Excel; Pivot Tables, Calculated Tables, and Visualization on Excel Dashboard
 ### Steps Involved
  1. **Data Cleaning and formating**
      1. Reduce the data set to 1,389 rows with 16 columns by deleting unnecessary/unimportant columns and removing duplicates
      2. Change datatype
      3. Extract Product_category and Product_type from Category, Review_new from Review_id
      4. From the cleaned data set, calculated tables are derived;

       *For Calculated Price Range*:
             <pre>
            ```excel=IF(F2<=199, "<£200",IF(F2<=499, "£200-£499",
             IF(F2<=1999, "£500-£1,999", IF(F2<=9999, "£2,000-£9,999",
             IF(F2<=19999, "£10,000-£19,999",IF(F2<=49999, "£20,000-£49,999", 
             IF(F2<=99999, "£50,000-£99,999", IF(F2>1000000, ">£1,000,000")))))))) ```
         </pre>

        *For Combined Score = rating * rating_count to calculate top 5 products by number of review and rating*

                        =H2 * LOG(I2 + 1) 

        *For Calculated Rating Distribution"*
                <pre>
                ``` excel=IF(H2<=2, "<=2.0",IF(H2<=2.4, "2.1-2.4",
                    IF(H2<=3, "2.5-3.0", IF(H2<=3.4, "3.1-3.4",
                    IF(H2<=4, "3.5-4.0",IF(H2<=4.4, "4.1-4.4", IF(H2<=5, "4.5-5.0"))))))) ```
                </pre>
                
        *For calculated count of products with discount greater than 50%*

                      =COUNTIF(G2:G1390, ">=50%")
     
        *For calculated products with number of reviews <1000*

                     =COUNTIF(I2:I1390,"<1000")

        *To calculate relationship between Rating and Level of Discount*

                       =CORREL(H2:H1390,E2:E1390)
     
   2. **Explorative Data Analysis**
          This is where i explored the data to derive my analysis.

      *Files Included*
           `Amazon case study-Project New.xlsx`

       ##### Dashboard
        ![image](https://github.com/user-attachments/assets/e904e763-2c97-45bd-b6df-518271fccf10)
       ##### Pivot Tables
        ![image](https://github.com/user-attachments/assets/5634429a-bd59-460c-bded-cf26e2a5409e)
        ![image](https://github.com/user-attachments/assets/9a7ed91b-ac70-423d-9bcd-7e5e8136b96d)

   3.  **Insights from Data**

   #### Product Improvement Insights
        1. Low Ratings in Some Categories: Products rated below 3.5 (totaling over 100 items) may need quality improvements.
            1. Focus on analyzing user feedback for products in these buckets and optimize features or quality.
        2. Skewed Discounting: Categories like Toys & Games and Office Products have 0%–6% discount but may still underperform in sales.
            1. Consider offering targeted promotions or bundle deals in these categories to test responsiveness.
        3. Price Optimization: High actual vs discounted price gaps in Electronics and Home & Kitchen suggest room for pricing strategy review or bundling improvements.
             4. High Review but Low Rating Products: For example, USB Cables have 2.75M reviews, but are not in top rating buckets.
                 1. Analyze product quality or delivery issues that might be lowering ratings despite high engagement.
           
       #### 📢 Marketing Strategy Insights
             1. Leverage Top Review Categories:
                 1. Electronics dominates reviews (15.6M). Capitalize on this by running campaigns, influencer reviews, or product highlight reels in this category.
             2. Highlight High-Rated Products:
                 1. Products like Tablets with the highest average rating (4.6) should be placed in ads, front-page features, or "Top Picks" sections.
             3. Discount Engagement Strategy:
                 1. Products with higher discounts tend to have better ratings but from my analysis, there is no correlation between the ratings and level of discount, as the level of discount does not influence the product rating by customers. Some products with no or low discount are rated high while with high discount are rated low.
      
          `relationship between rating and level of discount= 0.119018491` by calculation

                 1. Tips: Create marketing campaigns around "smart savings" or "best-rated discounted products."
            4. Revenue-Driven Focus:
                 1. Focus ad budgets on Electronics, Computers & Accessories, and Home & Kitchen, which account for ~125B in potential revenue.These categories are clearly high-margin and high-volume.

       #### 👥 Customer Engagement Insights
            1. Engage Low-Review Products:
                  1. 311 products have <1,000 reviews—these are good targets for customer review campaigns, e.g., incentives for leaving reviews.
            2. Review-Based Recommendations:
                  1. Promote products with high ratings and many reviews, such as HDMI Cables, MicroSD and In-Ear Products, use them in "most loved" or "what others are buying" features.
            3. Target by Price Sensitivity:
                  1. Most products are in £200–£500 and £1,000–£5,000 buckets, offer tiered discounts, financing options, or cart reminders for these groups to improve conversions.
            4. Focus on Mid-Tier Products:
                  1. The "Mid" and "Lower-Mid" product segments account for over 70% of product count.
                  Tip: Tailor marketing messages toward value-conscious buyers, emphasizing durability, affordability, and customer satisfaction.

        
   #### Product Improvement Insights
        1. Low Ratings in Some Categories:
           1. Products rated below 3.5 (totaling over 100 items) may need quality improvements.
           2. Focus on analyzing user feedback for products in these buckets and optimize features or quality.
        2. Skewed Discounting:
Categories like Toys & Games and Office Products have 0%–6% discount but may still underperform in sales.
Consider offering targeted promotions or bundle deals in these categories to test responsiveness.
Price Optimization:
High actual vs discounted price gaps in Electronics and Home & Kitchen suggest room for pricing strategy review or bundling improvements.
High Review but Low Rating Products:
For example, USB Cables have 2.75M reviews, but are not in top rating buckets.
Analyze product quality or delivery issues that might be lowering ratings despite high engagement.

📢 Marketing Strategy Insights
Leverage Top Review Categories:
Electronics dominates reviews (15.6M). Capitalize on this by running campaigns, influencer reviews, or product highlight reels in this category.
Highlight High-Rated Products:
Products like Tablets (4.6 rating) should be placed in ads, front-page features, or "Top Picks" sections.
Discount Engagement Strategy:
Products with higher discounts tend to have better ratings (see the positive trend in "Rating vs Discount").
Create marketing campaigns around "smart savings" or "best-rated discounted products."
Revenue-Driven Focus:
Focus ad budgets on Electronics, Computers & Accessories, and Home & Kitchen, which account for ~125B in potential revenue.
These categories are clearly high-margin and high-volume.

👥 Customer Engagement Insights
Engage Low-Review Products:
311 products have <1,000 reviews—these are good targets for customer review campaigns, e.g., incentives for leaving reviews.
Review-Based Recommendations:
Promote products with high ratings and many reviews, such as:
HDMI Cables (24.77 average rating * # of reviews)
MicroSD and In-Ear Products
Use them in "most loved" or "what others are buying" features.
Target by Price Sensitivity:
Most products are in £200–£500 and £1,000–£5,000 buckets.
Offer tiered discounts, financing options, or cart reminders for these groups to improve conversions.
Focus on Mid-Tier Products:
The "Mid" and "Lower-Mid" product segments account for over 70% of product count.
Tailor marketing messages toward value-conscious buyers, emphasizing durability, affordability, and customer satisfaction.

 


  
      

          

      
          
      

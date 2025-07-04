# Amazon-Analysis-DSA_Project
My first project on Excel workbook Analysis

 ## Project Topic: Amazon Product Review Analysis
 ### Project Overview
 I was given an Amazon Product excel data set of 1,465 rows and 16 columns.
 #### Aim 
 Analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.
 
 ##### Mode of Analysis
      - Microsoft Excel; Pivot Tables, Calculated Tables, and Visualization on Excel Dashboard
 ###### Steps Involved
  1. **Data Cleaning and formating**
      1. Reduce the data set by deleting unnecessary/unimportant columns and removing duplicates.
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

                       ``` =H2 * LOG(I2 + 1) ```

        *For Calculated Rating Distribution"*
                <pre>
                ``` excel=IF(H2<=2, "<=2.0",IF(H2<=2.4, "2.1-2.4",
                    IF(H2<=3, "2.5-3.0", IF(H2<=3.4, "3.1-3.4",
                    IF(H2<=4, "3.5-4.0",IF(H2<=4.4, "4.1-4.4", IF(H2<=5, "4.5-5.0"))))))) ```
                </pre>
                
     *For calculated count of products with discount greater than 50%*

            ```=COUNTIF(G2:G1390, ">=50%")```
     
   3. **Explorative Data Analysis**
          This is where i explored the data to answer required questions
  
      ##### Files Included
        `Amazon case study-Project New.xlsx`

          

      
          
      

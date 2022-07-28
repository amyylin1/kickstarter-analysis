# kickstarter-analysis
analysis on kickstarter to uncover trend


## 1. Overview of Project:  Explain the purpose of this analysis.

### The purpose of this analysis is to determine what factors contribute to a successful fundraising campaign. 
    
    
## 2. Analysis and Challenges: explain how you performed your analysis using images and links to code, as well as any challenges you encountered and how you overcame them.  

### Analysis of Outcomes Based on Launch Date: 

    year = YEAR(the cell for "Date Created Conversion")
    
    PivotTable Fields set up:
    1. Filters:  "Category" (set to "theater" later), "Years" 
    2. Columns:  "outcomes" (sort the outcomes of "sucessful" in descending order)
    3. Rows:  "Date Created Conversion"
    4. Value:  Count of outcomes
    
    ![screenshot](/Users/yinglin/Desktop/test.png)
    
### Analysis of Outcomes Based on Goals:
    
    COUNTIFS syntax:
    COUNTIFS(criteria_range 1, criteria, [criteria_range2, criteria2]...)
    e.g., =COUNTIFS(kickstarter!$F:$F,"successful",kickstarter!$D:$D,"<1000", kickstarter!$R:$R, "plays")
    Note: make sure to change the criteria of "kicstarter!$F:$F" and the goal accordingly for each cell
    
    SUM syntax: SUM(A2:A10)
    e.g., = SUM(B2:D2)
    
    % successful, failed, and canceled project:
    formula = Number Successful (Failed or Canceled) / Total Project 
   
    
### Challenges and Difficulties Encountered:

    1.  Get familiar with the relevant function of excels
    2.  Understand rows vs. columns variables in the pivot table.  How will the table look like if rows and columns are switched?


## 3. Results:  Answer the following questions in complete and coherent sentences.

- What are two conclusions you can draw about the Theater Outcomes by Launch Date? 
    1. The most successful theater campaigns launched in May. 
    2. The least successful theater campaigns launched in December.
    
- What can you conclude about the Outcomes based on Goals?
    1. Goal of 45000 to 49999 have the lowest percentage successful (0%) and the highest percentage failed (100%).  
    2. Goal of less than 1000 have the hightest percentage successful (76%) and the lowest percentage failed (24%).
    
      
- What are some limitations of this dataset?
    Goal alone can't predict how successful the campaign is.  Besdies the types of catogories and difference in timing, other factors must be in play.   
    For example,  what other factors for the goal of 45000 to 49999 contribute to the 100 % failed rate?  Most of failed campaigns are underfunded.  The data does not indicate why they are underfunded.  
    
     
- What are some of other possible tables and/or graphs that we could create? 
    It would be nice to have table to measure the interest from the public and donors for the successful campaigns.  What makes these successful campaigns well funded.  

    

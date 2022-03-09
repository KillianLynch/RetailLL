# HR Payroll and Attrition Analysis

## Introduction

In this lab, we will analyze payroll and attrition to help us understand why there's a decrease in headcount while payroll costs us increasing. We will use Oracle Analytic Server's built in advanced analytic capabilities to create trend lines and forecasts into payroll costs and attrition to help our retail executives make informed decisions. We will also explore employee surveys to help us understand reasons for turnover.


Estimated Time: 20 minutes

### Objectives

In this lab, you will:
* Explore Oracle Analytics Server's advanced analytic capabilities and create a forecast of base salary vs. overtime
* Analyze turnover by department and create trend lines
* Create a word cloud to understand reasons for attrition
* Create a scatter plot to understand the distribution of employees by age, salary, and department
* [relative lab url test](?lab=need-help)

### Prerequisites

This lab assumes you have:
* All previous labs successfully completed

  > **Note:** If you have a **Free Trial** account, when your Free Trial expires your account will be converted to an **Always Free** account. You will not be able to conduct Free Tier workshops unless the Always Free environment is available. **[Click here for the Free Tier FAQ page.](https://www.oracle.com/cloud/free/faq.html)**

*This is the "fold" - below items are collapsed by default*
![](images/ "")

## Task 1: Using Forecasts to make predictions

<!-- Images -->
In this exercise, we are going to create a 12 month forecast using OAS's built in ML capabilities to help us predict where our payroll trends are heading.

1. **Create** a new canvas and **rename** it "HR Analysis"

    ![Create new canvas](images/1create-canvas.png "Create new canvas")
    ![Rename canvas](images/2rename-canvas.png "Rename canvas")

2. From the "OAX_PL_Payroll" dataset, **Control select** 'Base Salary' and 'Overtime Cost'. **Right click** and **select** "Pick Visualization" and **select** the Bar chart.

    ![Create bar chart](images/3create-bar-chart.png "Create bar chart")

3. From the grammar pane, **drag** 'Overtime Cost' and **place** it in the Values box under 'Base Salary'.

    ![Select Overtime Cost](images/4select-overtime-cost.png "Select Overtime Cost")
    ![Move Overtime Cost](images/5move-overtime-cost.png "Move Overtime Cost")

4. Now lets **select** 'Month' and **drag** it in the Category section.

    ![Drag Month](images/6add-month.png "Add month")

5. You have now just created a bar chart that compares Base Salary and Overtime Costs by Month. Let's apply quick and easy advanced analytics to this visual to help us understand the trend and forcase of this cost comparison.

6. **Right click** the visual and **select** 'Add Statistics' and then **select** 'Trendline'.
  ![Add trendline](images/7add-trendline.png "Add Trendline")

7.  **Right click** the visual and **select** 'Add Statistics' and then **select** 'Forecast'. This will create a forecast into the next 3 periods (months) by default.

  ![Add forecast](images/8add-forecast.png "Add Forecast")

8. We are more interested in seeing the forecast for the next 12 months so lets **click** the analytics tab in the Data Pane and **change** the 'Periods' to '12'.

  ![Edit forecast](images/10.1edit-forecast.png "Edit Forecast")

  Immediately you're presented with an updated visualization and results show that over a period of 12 months if this trend continues, payroll costs will continue to increase exponentially and will put major pressure on margins.


9. Lets now create a line graph of Voluntary Turnover by Fiscal Period and Department to help us understand the changes in turnover. **Control select** 'Voluntary Turnover', 'Department', and 'Fiscal Period' from the 'HCMLeavers' data set and **drag** it into the canvas under the bar graph we just created.

![Create linegraph](images/12create-line-graph.png "Create Linegraph")

Your canvas should now look like this:

![Line graph result](images/13line-graph-result.png "Linegraph result")

9. **Right click** and add a trendline like we did earlier.

  ![Add trendline](images/14add-trend-line-graph.png "Add trendline")
  ![Trendline result](images/15trend-line-result.png "Trendline result")

The resulting trend line shows us that Voltuntary Turnover is steadily increasing overall but there was a spike in July for Line Cooks just as there was a spike in Overtime Cost in July.

10. Let's now use customer survey responses for Voluntary Turnover and build a Tag Cloud to help us understand reasons for why employees are leaving. **Control select** 'Reason' and 'Voluntary Turnover' from 'HCMLeavers', **right click** and select 'Pick Visualization' and **select** the Tag Cloud.

  ![Create Tag Cloud](images/16create-tag-cloud.png "Create tag cloud")


11. Now **select** 'Voluntary Turnover' from 'HCMLeavers' and **drag** it into the Color section.


  ![Edit tag cloud](images/17tagcloud-color.png "Edit tag cloud")


12. Let's shift our visualizations around for a better layout. **Hover** over the title of the Tag Cloud until you see the four corner arrows and **click and drag** the Tag Cloud to the right of the Salary vs. Overtime cost bar chart.

  ![Move Tag cloud](images/18move-tagcloud.png "Move Tag Cloud")
  ![Move Tag cloud right](images/19move-tagcloud-right.png "Move Tag Cloud right")

The result should look like this:

  ![Tag cloud result](images/20tagcloud-move-result.png "Tag cloud result")

Based on the Tag Cloud, we see that the top three reasons for voluntary attrition was because our employees want higher pay rates, better opportunities, and a better work-life balance.

13. Now let's create the final visualization which is a scatter plot to help us understand the relationship between the age and salaries of our employees by department. **Control select** 'Department', 'Employee ID', 'Age' and 'Salary' from 'HCMLeavers'. Then, **drag and drop** the selected columns to the right of the Tag Cloud we just created.

  ![Create Scatter Plot](images/22drag-scatter-canvas.png "Create scatter plot")

The result should look like this:

  ![Scatter Plot Result](images/23scatter-result.png "Scatter plot result")

14. In the grammar pane, **switch** 'Department' and 'Employee ID' so that 'Department' is in the Color section and 'Employee ID' is in the Category section.

  ![Edit scatter attributes](images/24edit-scatter-attributes.png "Edit attributes")

15. **Navigate** to the Data Pane on the bottom left of your screen and **click** on the Axix tab. **Find** the 'Start' option and **change** it to 'Min Data'.

  ![Edit scatter axis](images/25edit-scatter-axis.png "Edit scatter axis")

16. **Move** the legend to the right for better positioning by **clicking** on the General tab and **changing** the 'Legend' option to 'Right'.

  ![Edit scatter legend](images/26edit-scatter-legend.png "Edit scatter legend")

Your canvas should now look like this:

  ![Result after scatter](images/27result-after-scatter.png "Result after scatter")

17. Lets improve the position of the visualizations so that our charts are easier to read. **Drag** the Tag Cloud on top of the Scatter Plot and **drop** it once a solid blue line appears above the Tag Cloud.

![Re-arrange charts](images/28move-tagcloud-above-scatter.png "Re-arrange charts")

18. Save your analysis. Our final canvas should now look like this:
![Final canvas](images/30final-dashboard.png "Final canvas")

19. Based on our analysis and prediction of Base Salary vs. Overtime Cost we learned that if this trend continues, it will put pressures on our margins. We also learned that a spike in turnover within our line cooks resulted in the spike in overtime costs in July. From the tag cloud, we discovered the top 3 reasons for why our employees are voluntarily leaving and finally we were able to understand the relationship between the age and salary of our employees within each department.

Our executives now need to put together a strategy to retain existing employees and fill the open positions as soon as possible. By doing so, payroll costs will be normalized, headcount will be restored, and her customers won't experience long wait times anymore.

**This concludes the lab**


## Learn More

* [Oracle Analytics Server Documentation](https://docs.oracle.com/en/middleware/bi/analytics-server/index.html)
* [Become a Business Analytics Expert Certification](https://mylearn.oracle.com/learning-path/become-a-business-analytics-expert/35644/91371)


## Acknowledgements
* **Authors** - Killian Lynch, Nagwang Gyamtso, Luke Wheless, Akash Dharamshi, Solution Engineer Specialist Hub Team, NA Technology
* **Contributors** -  Nagwang Gyamtso, Solution Engineer Specialist Hub Team, Na Technology
* **Last Updated By/Date** - Nagwang Gyamtso, March 2022

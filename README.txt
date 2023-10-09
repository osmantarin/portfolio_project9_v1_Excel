1) We start with the raw dataset in Excel

2) We create three new sheets titled: "Dashboard", "Pivot Table", and "Working Sheet"

3) We copy all our raw data onto the "Working Sheet" -- this keeps our raw data as our original reference point that does not change 

4) Before we clean the data, we should check for duplicates. We click on the "Data" section at the top and click directly on the
"Remove Duplicates" button (Be sure to click the "My data has headers" option)


26 duplicate values were found and removed 


5) Click on column B and hit CTRL+H which brings up the "Find and Replace" menu 

We instruct the dialogue box to find "M" within the column and replace with "Married" -- 539 replacements are made

We do the same for the "S" option to become "Single" -- 463 replacements are made 

We do the same for Column C to convert the gender abbreviations "M" and "F" into "Male" and "Female" respectively 


6) Next we remove the decimal places from the "Income" column to circumvent future errors (Note, we first standardize the format
in the column by highlighting the entire column and clicking on the "Number Format" drop down option and selecting "Currency".

We then click the "decrease decimal" box directly below the "Number Format" drop down 

7) We continue reviewing the data column by column, mostly glancing over the data before utilizing the filer option next to the 
column name for a deeper look. 

8) We notice the "Age" column contains various ages individually which will be difficult to visualize later. Our goal is to 
create a new column with various Age Brackets. 

We insert a new column and label it "Age Brackets" 

We start with the formula using an IF statement as follows: =IF(L2<31,"Adolescent", "Invalid"). The formula evaluates the value in cell L2
and returns "Adolescent" if the value is less than 31, and "Invalid" if the value is 31 or greater. We build further on this formula to develop
a nested formula. 

The final formula: =IF(L2>=31, "Middle Age", IF(L2<31,"Adolescent", "Invalid"))

The formula above compares every row in the "Age" column and if the value is less than 31 it states "Adolescent" and if the value 
is greater than 31 it states "Middle Age"

We add one final layer to the "Age Bracket" column in order to report ages greater than 54 as "Old" 

=IF(L4>54,"Old",(IF(L4>=31,"Middle Age",IF(L4<31,"Adolescent","Invalid"))))


9) We will now build pivot tables with this data

We navigate to the "Pivot Table" sheet we created initially 

We click on the "Insert" at the very top and click on "PivotTable"

Next we navigate to the "PivotTable Fields" on the right hand side. We click and drag the "Gender" option to Rows, "Income" to Values, 
and "Purchased Bike" to columns -- the final result is a pivot table showing...

We create a bar chart by nevigating to the Insert menu and clicking on the "Insert Column or Bar Chart" option.

We add axis titles and a chart title via the "Chart Elements" menu directly on the chart 

We also decide to remove decimals in the original data set to reduce clutter in the pivot table 


10) We will now build our second pivot table directly below our first 

We add "Commute Distance" to the Rows field and "Purchased Bike" to both the Values field and Columns field 

We immediately notice the column containing the commute distance is not sorted by lowest to highest. In attempting to sort the column
we notice that the entry "10+ miles" does not sort no matter what method we utilize. In order to correct this, we attempt to change the 
name of the entry. The entry "More than 10 miles" finally allows the column to sort correctly. 

We add a chart to visualize the average income per purchase 


11) We will now build our third pivot table directly below our second

We add "Age Brackets" to our Rows field and "Purchased Bike" to both the Values field and Columns field 

Note the importance of creating the age brackets. If we did not group our data into collective brackets ahead of time
and proceeded directly to the visualization, we would be left with a visualization containing a seemingly endless sea of data points. The
data brackets allow us to visualize the data trend which is a huge jump in sales in the middle age bracket compared to the two other age 
groups 


12) We now copy our charts and paste them into the Dashboard sheet we created initially. 

We should have three charts in our Dashboard. 

We navigate to the View menu and click out of the "Gridlines" option to obtain a cleaner look 

We create a header ranging from A1 to O6 titled "Bike Sales Dashboard" -- we adjust the font and size. We
center the text accordingly 

We utilize the Align option in the "Shape Format" menu to align our charts


13) To enable functionality in our dashboard, we add a Pivot Table Slicer via the "Insert Slicer" button 
on the PivotChart Analyze menu 

We distribute the functionalist across all pivot tables in the dashboard via the "Report Connections" option 
in the "Slicer" menu 

We also add pivot slicers for Region and Education as well 

We can now filter the data on the dashboard by Martial Status, Region, and Education 


14) We are sure to save the dashboard in the appropriate file and we also create a back up in safe location 



















# Gem-Stone-Price-Prediction
Predict price of gemstone using linear regression<br><br>
<b>Problem Statement</b><br>
You are hired by a company Gem Stones co ltd, which is a cubic zirconia manufacturer. You are provided with the dataset containing the prices and other attributes of almost 27,000 cubic zirconia (which is an inexpensive diamond alternative with many of the same qualities as a diamond). The company is earning different profits on different prize slots. You have to help the company in predicting the price for the stone on the bases of the details given in the dataset so it can distinguish between higher profitable stones and lower profitable stones so as to have better profit share. Also, provide them with the best 5 attributes that are most important.

<b>Data Description</b><br>

<li>Carat	 Carat weight of the cubic zirconia.</li>
<li>Cut	 Describe the cut quality of the cubic zirconia. Quality is increasing order Fair, Good, Very Good, Premium, Ideal.</li>
<li>Color 	 Colour of the cubic zirconia.With D being the best and J the worst.</li>
<li>Clarity	 cubic zirconia Clarity refers to the absence of the Inclusions and Blemishes. (In order from Best to Worst, FL = flawless, I3= level 3 inclusions) FL, IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3</li>
<li>Depth	 The Height of a cubic zirconia, measured from the Culet to the table, divided by its average Girdle Diameter.</li>
<li>Table	 The Width of the cubic zirconia's Table expressed as a Percentage of its Average Diameter.</li>
<li>Price	 the Price of the cubic zirconia.</li>
<li>X	 Length of the cubic zirconia in mm.</li>
<li>Y	 Width of the cubic zirconia in mm.</li>
<li>Z	 Height of the cubic zirconia in mm.</li><br>

<b>Model building</b><br>
There is a linear relationship between carat and price only for carat less than 1.<br>
I did feature engineerring and found out a linear relationship between cuberoot of carat and log price. I did label encoding of ordinal variables.<br>
Carat weight above 2  are outliers .But removing all that value would result in losing a lot of data. So I removed only extreme outliers, with carat weight > 2.5 and replaced it with 2.5.<br>
I build a regression model using LinearRegression function in sklearn.linear_model and smf function in statsmodel in api. There was multicollinearity. <br>
Since x,y,z are highly correlated to price I dropped x,y and z and build a new model.<br>
Selected model with lowest RMSE value.<br>


<b>Business Insights</b><br>
•	Important attributes are 	Carat,Clarity,Color,Cut<br> 
•	Zirconium carat weight has the most impact on the price  and hence the most important attribute<br>
•	Heavier the stone more it cost up untill 2.5 carats. After that there are fluctuations and price of stone depends on other attributes as well.<br>
•	CLarity is the next important attribute. Stone with Internally flawless clarity  cost significantly more( at least around 3500)when compared to same weight stone with I1 inclusions. <br>
•	Price of the stone varies with color.<br>
•	Cut influences the price of stones directly for lower weight stones. When carat weight increases, price depends on clarity and colour as well

<b>Recommendations:</b><br>
•	Invest on lower weight stones  between 1 and 2 carats with F,IF and VVSI clarity and color D or E.<br>
•	Stones more than 3 carat weight has to be of VSI,VVSI or IF clarity ,premium or ideal cut and color D,E,F to yield more money. Despite higher carat weight if it has inclusions, price is low, so need to be cautious.<br>
•	Invest on stones of color D.<br>
•	Invest on stones of IF and VVSI clarity.<br>
•	Avoid stones with inclusions(I1) unless it is of color D.<br>


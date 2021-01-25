# Gem-Stone-Price-Prediction
Predict price of gemstone using linear regression
<b>Problem Statement</b>
You are hired by a company Gem Stones co ltd, which is a cubic zirconia manufacturer. You are provided with the dataset containing the prices and other attributes of almost 27,000 cubic zirconia (which is an inexpensive diamond alternative with many of the same qualities as a diamond). The company is earning different profits on different prize slots. You have to help the company in predicting the price for the stone on the bases of the details given in the dataset so it can distinguish between higher profitable stones and lower profitable stones so as to have better profit share. Also, provide them with the best 5 attributes that are most important.

<b>Data Description</b>
Variable Name	Description
Carat	 Carat weight of the cubic zirconia.
Cut	 Describe the cut quality of the cubic zirconia. Quality is increasing order Fair, Good, Very Good, Premium, Ideal.
Color 	 Colour of the cubic zirconia.With D being the best and J the worst.
Clarity	 cubic zirconia Clarity refers to the absence of the Inclusions and Blemishes. (In order from Best to Worst, FL = flawless, I3= level 3 inclusions) FL, IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3
Depth	 The Height of a cubic zirconia, measured from the Culet to the table, divided by its average Girdle Diameter.
Table	 The Width of the cubic zirconia's Table expressed as a Percentage of its Average Diameter.
Price	 the Price of the cubic zirconia.
X	 Length of the cubic zirconia in mm.
Y	 Width of the cubic zirconia in mm.
Z	 Height of the cubic zirconia in mm.

EDA
There is a linear relationship between carat and price only for carat less than 1. 

I did feature engineerring and found out a linear relationship between cuberoot of carat and log price and build a linear regression model.

<b>Business Insights</b>
•	Important attributes are 	Carat,Clarity,Color,Cut
 
•	Zirconium carat weight has the most impact on the price  and hence the most important attribute

•	Heavier the stone more it cost up untill 2.5 carats. After that there are fluctuations and price of stone depends on other attributes as well.
•	CLarity is the next important attribute. Stone with Internally flawless clarity  cost significantly more( at least around 3500)when compared to same weight stone with I1 inclusions. 
•	Price of the stone varies with color.
•	Cut influences the price of stones directly for lower weight stones. When carat weight increases, price depends on clarity and colour as well

<b>Recommendations:</b>
•	Invest on lower weight stones  between 1 and 2 carats with F,IF and VVSI clarity and color D or E.
•	Stones more than 3 carat weight has to be of VSI,VVSI or IF clarity ,premium or ideal cut and color D,E,F to yield more money. Despite higher carat weight if it has inclusions, price is low, so need to be cautious.
•	Invest on stones of color D.
•	Invest on stones of IF and VVSI clarity.
•	Avoid stones with inclusions(I1) unless it is of color D.


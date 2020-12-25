# Bike-Sharing-Prediction-Using-Gradient-Boosting-Regressor

![wallpaperflare com_wallpaper](https://user-images.githubusercontent.com/59309459/103134901-784c1900-46da-11eb-9cec-888023aacf2b.jpg)

The main theme of this dataset is to predict total bike sharing count in a day using Grdient Boosting Regressor.

Pre-Processing steps followed before predicting:

First we import the dataset called Bike.csv.

The dataset contains the following the columns:

![Capture](https://user-images.githubusercontent.com/59309459/103135315-6b7cf480-46dd-11eb-9a18-72b1373d37ce.JPG)

Consider the "Season" column in that we have 4 unique values as (1,2,3,4) we replace these numbers as 'spring','summer','fall','winter'.

Consider the "Month" column in that we have 12 unique values as (1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12) we replace these numbers as 'January', 'February', 'March','April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'.

Consider the "Weekday" column in that we have 6 unique values as (0,1,2,3,4,5,6) we replace these numbers as
'Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday'.

Consider the "Weather_Sit" column in that we have 3 unique values as (1,2,3) we replace these numbers as 'A','B','C'.

## Plot representing the Temp and Atemp:

### Temp:
![Capture](https://user-images.githubusercontent.com/59309459/103135457-7d12cc00-46de-11eb-8488-22c7ef67daf2.JPG)

### Atemp:
![Capture](https://user-images.githubusercontent.com/59309459/103135474-93208c80-46de-11eb-9f31-e6a77909a91e.JPG)

## Plot representing the Hum, Windspeed and Cnt:

### Hum:
![Capture](https://user-images.githubusercontent.com/59309459/103135512-d11db080-46de-11eb-916a-5d749bc9b60b.JPG)

### Windspeed:
![Capture](https://user-images.githubusercontent.com/59309459/103135529-ed215200-46de-11eb-819d-039adad3a304.JPG)

### Cnt:
![Capture](https://user-images.githubusercontent.com/59309459/103135550-04f8d600-46df-11eb-93b4-00d1613b38ba.JPG)

## A sub dataset was created from the main dataset as data_categorical as shown below:
![Capture](https://user-images.githubusercontent.com/59309459/103135607-6faa1180-46df-11eb-9537-f099d3d7579a.JPG)

## Box plot has been drawn for Season, Holiday, Working_Day:
![Capture](https://user-images.githubusercontent.com/59309459/103135673-d3ccd580-46df-11eb-97a9-9cd4067cd3a2.JPG)

## Box plot has been drawn for Weather_Sit, Month, Weekday, Year:
![Capture](https://user-images.githubusercontent.com/59309459/103135707-25756000-46e0-11eb-925d-7ad65b49add8.JPG)

## Dummification has been done on data_categorical(on subset):
data_dummies = pd.get_dummies(data_categorical,drop_first=True)

## A final data was created with the following columns:
'Year', 'Holiday', 'Working_Day', 'Temp', 'Atemp', 'Hum', 'Windspeed',
'Casual', 'Registered', 'Cnt', 'Season_spring', 'Season_summer',
'Season_winter', 'Month_August', 'Month_December', 'Month_February',
'Month_January', 'Month_July', 'Month_June', 'Month_March', 'Month_May',
'Month_November', 'Month_October', 'Month_September', 'Weekday_Monday',
'Weekday_Saturday', 'Weekday_Sunday', 'Weekday_Thursday',
'Weekday_Tuesday', 'Weekday_Wednesday', 'Weather_Sit_B',
'Weather_Sit_C'

Before applying the data to the model target variable 'Y' is taken as 'Cnt' and the rest of the columns as 'X'.

And x, y are splitted as x_train,x_test,y_train,y_test.

After this the gradient booster algorithm is imported from Sci-kit learn library and applied to the x, y variables.

## Output:

![Capture](https://user-images.githubusercontent.com/59309459/103135984-64a4b080-46e2-11eb-902f-673dd10a56de.JPG)

# Conclusion:

According to the analysis the gradient booster is predicting the Count of bikes with 98% Accuracy.

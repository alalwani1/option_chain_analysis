# Option Chain Analysis

# Motivation behind this Project
In last year(2020 Dec) i was learning about Nifty option Segment. Nifty Option segment can be understand by option chain data and in the beginning i got to know that anyone can fetch data from NSEIndia website(https://www.nseindia.com) as they provides Rest APIs for the same without ny cost and during this time i thougth to create a Node.js project on this. This project was developed for education purpose only, it has no commercial use. I have learned about option chain data from Sameer Dharasker Sir.

#Features
 
 a) Expiry Date Selection
    UI will give you Expiry Date selection through which you can access data based upon selected expiry date.
  
 b) Tables(Two):
        First table represents option chain data in the range of +-400 of current Nifty price with their call and put writers. Example: currrent price= 15300 so it will show you data beteen 14900 to 15700 strike prices. This table helps to decide the major support and resistenance of current Nifty price in this range.
        Second table represents sum of call and put writers of three consecutive strike prices. example: current price = 15350 so call writer of (15300+15350+15400) and put writer of (15300+15350+15400). This table helps to decide buy call/put based upon call and put writers data.

 c) There is no manual intervention.

 d) Captures option data in every 2 minutes.(reason for 2 minutes can be seen in Notes).

 e) No need of external database storage system as Option chain data is getting store in browser's localstorage.

 f) you can take option chain data from localStorage for further analysis of market after working hours.

 g) Data Accuracy
    The data is being fetched in realtime when a user visits the webpage via server. The data is accurate and unmodified version of NSE option chain. I have used CURL for scrapping option chain data which I found was working, NodeJs Request and Native HTTPs library was not working. 

## Page Screenshot
<img width="1082" alt="Screenshot 2021-07-22 at 4 33 18 PM" src="https://user-images.githubusercontent.com/87809858/126629499-4e383e3c-c792-46bf-90e7-97b009a0a942.png">

Required Setup:
You should have installed node and npm in your machine.

#How to run this project:
After cloning his project in your local workspace. Go inside of option_chain_analysis folder abd run below command:
 npm install

and run below command also:
npm start

now go to your browser and paste the below given URL:
http://localhost:3000

## Note:
https://www.nseindia.com/ update data in every 2 minute. so our tables will be updated after every 2 minutes. unlike kite and upstox API's.

## Update 22 July 2021 (working)

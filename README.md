# SpeedyCheers

For a totally not-fake-at-all reason, a Technical Product Manager (TPM) brings to you the proposal to build a product called “SpeedyCheers”.
Speedy Cheers is an Uber equivalent, except that rather than getting a ride, by “Requesting a Cheer” a SpeedyCheer driver will come to your location, and “cheer you on” on whatever task you are doing. If you are telling a joke, they’ll come to laugh. If you are lifting weights, they’ll pump you up. If giving a speech, they’ll clap louder than anyone else. You feel great, they feel great (cause they get paid); it’s a win-win!
The TPM gives you these requirements:
When requesting a cheer, the closest SpeedyCheer driver will be notified of your location.
SpeedyCheers will be paid in 5-minute increments charging $10/5 minute.
Please share your proposal for how you’d architect and implement SpeedyCheers. For your reference, at Galvanize we heavily use AWS and primarily implement it in a Serverless fashion. While your proposal does not need to be with AWS or Serverless, it is definitely an asset if you can comfortably incorporate it into your diagram.
Please make sure to:
Share an overall diagram of how SpeedyCheers will work. We recommend having a user icon on the diagram and showing how the user’s request flows through the different components of your architecture.
You are welcome to use https://www.draw.io or any other tool you prefer.
Explain your architecture in plain English. As great as your diagram maybe, it’ll require some level of explanation for us to understand what you were thinking about.
Explain your choices behind your technology and programming language selection and why it is a great fit for the product you are building.
You can write as much as you like, as long as it is clear We do not want to limit your creativity; but definitely more is not always better, it all depends on what you are elaborating on.	

Requirements:
1.	Cheers Requestor create a request for cheer leader and with pickup details shared.
2.	The system will provide the estimated cost, estimated time and request for acceptance.
3.	The system takes the help of location service, cheer leaders available and select the appropriate leader based on nearest location available 
4.	The cheer leader will be notified about the cheer leader request, estimated price and upon acceptance, the requestor will receive the cheer leader information and the real-time location updates.
5.	Upon the cheers actions completed, the cheer leader confirms the completion.
6.	The actual amount bill will be generated and send to requestor
7.	Upon the payment completion, the cheer leader will be paid the actual amount.

Future Solution Integration:
1.	Chat bot app to provide more details about questions about the cheer leader and cheer requestor.
Allow requestor and cheer leader to interact, so that requestor can provide more details about the request details.


Project Name: SpeedyCheers
Users: 
1.	SpeedyCheers Driver
2.	Cheers Requestor
Assumption: 
Limitations:
1.	Requestor will be requesting only one cheer leader at a time and requestor can create more than cheer leader request.
2.	Supports only immediate schedule and no preplanned support at this time.
3.  



Steps:
------
1. The cheers requestor login to speedycheers app and request for the cheer leader and time taken by the task to complete.
2.  The find cheers leader lambda function will peform below functions
3.  Using Location service get the requestor location
4. Find the near by driver based on the hexagonal geo spactial ring defined
5. Estimate the price using pricing service and distance to travel.
5.1. With estimated price, get approval from requesttor.
6. Cheer request is assigned to a cheer leader. SQS
7. Cheer leader either accept or reject the request.
8. Upon accepting the request, the cheer leader will start moving to the pickup location
9. Cheer leader will complete the task and notify the task is completed in the app.
10. send task completed event to notification service
11. Notification service will send message to Requestor to complete the payment.
12. Upon payment completion done by stripe, stripe send message to billing service using webhook and API gateway.
13. Billing service will confirm the payment done and send notification to SQS so that billing information is sent to cheer requestor.
14. Payment will be done to cheer leader later.

Components:
1. Cheers Requestor App & Speedy Cheers cheer leader app is built using AWS Amplify React JS.
2. API Cognito is used for authentication and authrorization on mobile app.
3. API Gateway will allow websocket connection from Cheer Requestor app to Cheer Requestor API
4. API Gateway will allow websocket connection from Cheer Leader app to Cheer Leader API
5. Cheers Requestor API is used to 
5.1. Request Cheer leader


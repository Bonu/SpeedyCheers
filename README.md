﻿# SpeedyCheers

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





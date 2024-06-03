# streaming-05-smart-smoker
by Andy Asher 2024


We want to stream information from a smart smoker. Read one value every half minute. (sleep_secs = 30)

smoker-temps.csv has 4 columns:

[0] Time = Date-time stamp for the sensor reading
[1] Channel1 = Smoker Temp --> send to message queue "01-smoker"
[2] Channel2 = Food A Temp --> send to message queue "02-food-A"
[3] Channel3 = Food B Temp --> send to message queue "03-food-B"

Requirements

RabbitMQ server running
pika installed in your active environment
RabbitMQ Admin

See http://localhost:15672/Links to an external site.

The python file creates and sends messages to three message queues.
1. The smoker temp with time stamp
2. Food A temp with time stamp
3. Food B temp with time stamp

![Screenshot of messages sending](Screenshot.png)

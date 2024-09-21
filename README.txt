# DS_Projects
Motivation - 
  1. Learn Regex
  2. Elections were around, So if any useful data can be extracted 
  3. Learning and fun to do 

Problems Faced - 
  1. The data exported was not the dataframe format normal .txt file 
  2. No indication to whom which message was replied 
  3. No emotions as the data was plain txt

So Basically project : 
  1. For the project, I used regex expression to seperate date and user message. 
     Further from user message I seperated UserName and Message. 
     Basically I observed and found that each line was basically timestamp - 
     Then If there is a notification , no : were there , but in case of some convo the chats had User : Message Format. 
     
     \s - whitespace  
     \d - character 
     
     user_msg = re.split()[1:]
     date_time = re.findall(split_formats[key], raw_string) 
     
  2. Futher the dataset was prepared in this way, not by read_csv. 
    Since I had exported the file without media , all the messages where there was media got <media-ommited>
    Basic EDA included watchin How many messages has every group member done.
    
      Which hour had the most messages?  
      It showed that 8pm to 10pm was the most chatting time and nearly no message from 3am to 7am in the whole history.
    
    Then I compared the traffic on Weekends vs Weekdays of the top 5 users ? 
    The messages were comparitley high on Fridays -maybe due to ITC meetings.
    
    Number of messages may not be appropriate metric, so I decided to take length of message and summed it up.
    To my suprise 4 / 5 also had the most words. But one was expection (Maybe he like convening his message in a go not engaging in conversations)
    
    When I checked Average Message Size - I saw a new trend that Person who use it as just information channel showed up. 
    Very Less Message with high word count shows using for information channel no conversation.
    
    I also plotted the heatmap for Time vs Day. Thursday nights were also very silent maybe all clubs busy in event planning for Saturday evening.
    I also tried to see whom I had replied more as who has the message just before me (Assumption).
    There was also a very evident trend that the group started there were high messages and now they are decreasing. 
    Maybe people using personal channels for communication.
    
    Collab Link - https://colab.research.google.com/drive/1ksavTAP9LpiYdLp8Y4E9Acf8b7kfs04x?usp=sharing

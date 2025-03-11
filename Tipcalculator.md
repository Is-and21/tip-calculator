START  


  DISPLAY "Enter the total bill amount: "  
  READ bill_amount  

  IF bill_amount <= 0 THEN  
    DISPLAY "Error: Bill amount must be a positive number."  
    EXIT  
  END IF  

  
  DISPLAY "Enter service quality (poor, fair, good, excellent): "  
  READ service_quality  

 
  IF service_quality = "poor" THEN  
    tip_percentage = 10  
  ELSE IF service_quality = "fair" THEN  
    tip_percentage = 15  
  ELSE IF service_quality = "good" THEN  
    tip_percentage = 18  
  ELSE IF service_quality = "excellent" THEN  
    tip_percentage = 20  
  ELSE  
    DISPLAY "Error: Invalid service quality. Choose from (poor, fair, good, excellent)."  
    EXIT  
  END IF  


  DISPLAY "Enter the number of people splitting the bill: "  
  READ num_people  


  IF num_people <= 0 THEN  
    DISPLAY "Error: Number of people must be a positive integer."  
    EXIT  
  END IF  


  tip_amount = (bill_amount * tip_percentage) / 100  

 
  total_amount = bill_amount + tip_amount  

 
  amount_per_person = total_amount / num_people  

  
  DISPLAY "Bill amount: $" + bill_amount  
  DISPLAY "Service quality: " + service_quality + " (" + tip_percentage + "%)"  
  DISPLAY "Tip amount: $" + tip_amount  
  DISPLAY "Total amount: $" + total_amount  
  DISPLAY "Number of people: " + num_people  
  DISPLAY "Amount per person: $" + amount_per_person  

END

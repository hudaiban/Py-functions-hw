# Py-functions-hw - hw 3
Question 1: Build a phone book program that receives the phone number, and returns the name of the owner.
You can follow the table below:
## Contact Table
| Name | Number |
| --- | ------------- |
| Ahmed | 0551112222 |
| Saad | 0551113333 |
| Sultan | 0551114444 |
| Morad | 0551115555 |
| Abdullah| 0551116666 |

This is the list of dictionaries you can use to build this function:

```contactTable=[{"name":"Ahmed","Phone":"0551112222"},{"name":"Saad","Phone":"0551113333"},{"name":"Sultan","Phone":"0551114444"},{"name":"Morad","Phone":"0551115555"},{"name":"Abdullah","Phone":"0551116666"}] ```

- If the number exists, print the owner. Otherwise, print "Sorry, the number is not found".
- If the number is less or more than 10 numbers, print "This is invalid number".
- If the number contains letters or symbols, print "This is invalid number".


<!---->

contactTable=[{"name":"Ahmed","Phone":"0551112222"},                                         
              {"name":"Saad","Phone":"0551113333"},                                          
              {"name":"Sultan","Phone":"0551114444"},                                        
              {"name":"Morad","Phone":"0551115555"},                                         
              {"name":"Abdullah","Phone":"0551116666"}                                       
            ]                                                                                
                                                                                             
a = input("Enter a number :")                                                                
                                                                                             
def isValidNumber(phone):                                                                    
    return not (len(a) != 10 or a.isdigit() != True)                                         
                                                                                             
def findPhone(input_phone, contacts):                                                        
    for contact in contacts:                                                                 
        phone = contact.get("Phone")                                                         
        name = contact.get("name")                                                           
        if phone == input_phone:                                                             
            return contact                                                                   
    return False                                                                             
                                                                                             
if isValidNumber(a):                                                                         
    contact = findPhone(a, contactTable)                                                     
    if contact:                                                                              
        print("this phone number:",contact.get("Phone"), "belong to :", contact.get("name")) 
    else:                                                                                    
        print("Sorry, the number is not found")                                              
else:                                                                                        
    print("This is invalid number")

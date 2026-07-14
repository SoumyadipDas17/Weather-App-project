def forecast(data):
    for day in data["weather"]:

        print("\nDATE:", day["date"])
        print("MAXIMUM TEMPERATURE:", day["maxtempC"], "°C")
        print("MINIMUM TEMPERATURE:", day["mintempC"], "°C")
        print("AVERAGE TEMPERATURE:", day["avgtempC"], "°C")
        print("SUNRISE:", day["astronomy"][0]["sunrise"])
        print("SUNSET:", day["astronomy"][0]["sunset"])

        
        desc = day["hourly"][0]["weatherDesc"][0]["value"]
        print("WEATHER DESCRIPTION:", desc.upper())






def currentweatherreport(city):     #1
    
    if city in history:
        history.remove(city)
    history.append(city)
    f=open("weather report","ab+")
    f.seek(0)
    pickle.dump(history,f)
    f.close()
    url=f"https://wttr.in/{city}?format=j1"
    response=requests.get(url)
    if response.status_code==200 :
        data=response.json()
        print ("THE CURRENT CONDITIONS OF",city.upper(),":")
        print ("TEMPERATURE(°C):",data["current_condition"][0]['temp_C'])
        print ("HUMIDITY(%):",data["current_condition"][0]['humidity'])
        print("WEATHER DESCRIPTION:",data["current_condition"][0]['weatherDesc'][0]["value"])
        print ("WIND SPEED(KPH):",data["current_condition"][0]['windspeedKmph'])
    fore=input("press 'y' to see the weather forecast from today to  upcoming  two days ;else press the enter key :").upper()
    if fore =="Y" :
        forecast(data)
            
def searchhistory(history):         #2
    f=open("weather report","ab+")
    f.seek(0)
    try :
        while True :
            history=(pickle.load(f))
           
    except EOFError :
        pass
    
    
    print("Your search history is:")
    
    for i in range(-1,-1*(len(history)+1 ),-1):
        print ((-1*i),"----",history[i])
    c=int(input("Enter the number present before the city to know the weather report else enter '0' :"))
    if c!=0 :
        currentweatherreport(history[-1*c])
                   
        
#main                   
import requests
import pickle
f=open("weather report","ab+")
history=[]
f.seek(0)
try :
    while True :
        history=(pickle.load(f))           
except EOFError :
    pass
f.seek(0)
while True :
    a="|1.CURRENT WEATHER REPORT\t|2.SEARCH HISTORY\t|3.DELETE SEARCH HISTORY\t|4.EXIT\t|"
    b=len(a)+25
    print("\n")
    print("_"*b,)
    print("MAIN MENU:-")
    print("_"*b)
    print(a)
    print("_"*b)
    print("\n")


    a=int(input("Enter the number present before the option in order to use it:"))
    if a==1:
        f=open("weather report","ab+")
        f.seek(0)
        city=input("Enter city : ").upper()
        currentweatherreport(city)
    elif a==2 :
        searchhistory(history)

    elif a==3 :
        choice=int(input("1.DELETE PARTICULAR SEARCH(ES) FROM SEARCH HISTORY\n2.DELETE ENTIRE SEARCH HISTORY\nENTER YOUR CHOICE (1/2):"))
        if choice ==2 :
            c2=input("DO YOU WANT YOUR ENTIRE SEARCH HISTORY TO BE DELETED? PRESS 'Y' IF SO...").upper()
            if c2=='Y':
                f=open("weather report","wb")
                f.close()
                history=[]
                print("ENTIRE SEARCH HISTORY HAS BEEN DELETED!")
        elif choice==1 :
            f=open("weather report","wb")
            f.seek(0)
            ans="Y"
            storage=[]
            serial=[]
            while ans=="Y" :
                b=int(input("enter the number present before the searched city in order to delete it from search history:"))
                serial.append(history[(-1)*b])
                ans=input("enter 'Y' to delete more:").upper()
            for element in serial :
                history.remove(element)
                            
            print("required elements are deleted")
            f=open("weather report","wb")
            f.seek(0)
            
            pickle.dump(history,f)
            f.close()               
                
                    
        
        
        
    elif a==4:
        f.close()
        break
        exit()
    else:
        print("INVALID CHOICE")




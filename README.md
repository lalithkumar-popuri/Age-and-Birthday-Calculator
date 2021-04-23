# python-programming
#program for print the month calendar
#give input month and year separated by space
month,year=map(int,input("enter month and year ").split())
week=(0,1,2,3,4,5,6)
date=1
cent=year/100
rem=year%100
odd1=int(rem/4)
count=0
if year%400==0 or year%4==0 and year%100!=0:
    count=1    
if month==1 or month==10:
    
    month_odd=0
elif month==2 or month==3 or month==11:
    
    month_odd=3
elif month==4 or month==7:
    
    month_odd=6
elif month==9 or month==12:
    
    month_odd=5
elif month==5:

    month_odd=1
elif month==6:
    
    month_odd=4 
elif month==8:
    
    month_odd=2
else:
    print ("please enter the month in between 1 and 12\n")
    exit()
if (year>=1600 and year<=1699) or (year>=2000 and year<=2099):
    
    year_odd=6
elif (year >= 1700 and year<=1799): 
    
    year_odd =4
elif(year>=1800 and year<=1899): 

    year_odd =2 
elif(year>=1900 and year<=1999):  
    
    year_odd=0
else:   
    print("please enetr the year in between 1600 to 2099\n")  
    exit()
odd2=month_odd+year_odd+rem+odd1+date
if count==1 and (month==1 or month==2):
    odd2-=1
temp=odd2%7  
print(month,year)   
print("SUN MON TUE WED THU FRI SAT")
if temp== week[0]:
    print("","-   "*week[0],end="")
elif temp==week[1]:
    print("","-   "*week[1],end="")
elif temp==week[2]:
    print("","-   "*week[2],end="")
elif temp==week[3]:
    print("","-   "*week[3],end="")
elif temp==week[4]:
    print("","-   "*week[4],end="")
elif temp==week[5]:
    print("","-   "*week[5],end="")
else:
    print("","-   "*week[6],end="")   
if month==1 or month==3 or month==5 or month==7  or month==8 or month ==10 or month ==12:
    for i in range(1,32):
        print(i,end="  ")
        if i <10:
            print(" ",end="")
        if (temp+i)%7==0:
            print()
elif month==4 or month==6 or month==9 or month==11:        
    for i in range(1,31):
        print(i,end="  ") 
        if i<10:
            print(" ",end="") 
        if (temp+i)%7==0:
            print()           
else:        
    if count==1:   
        for i in range(1,30):
            print(i,end="  ") 
            if i<10:
                print(" ",end="") 
            if (temp+i)%7==0:
                print()
    else:
        for i in range(1,29):
            print(i,end="  ") 
            if i<10:
                print(" ",end="") 
            if (temp+i)%7==0:
                print()                               
            
  

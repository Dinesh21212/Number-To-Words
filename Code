ones=["zero","one","two","three","four","five","six","seven","eight","nine"]
double=[" ","eleven","twelve","thirteen","fourteen","fifteen","sixteen","seventeen","eighteen","nineteen"]
tens=[" ","ten","twenty","thirty","forty","fifty","sixty","seventy","eighty","ninety","hundred"]

def lt_thousand(n):             #lt_thousand

        if n ==0:
                return "zero"   
        elif n < 10:
                return(ones[n])
        elif 10 < n < 20:
                return(double[n-10])
        elif  n < 100:
                a,b = divmod(n,10)
                if b ==0:
                    return tens[a]
                else:
                    return tens[a]+" "+ ones[b]
        else :
                a1,b1 = divmod(n,100)
                if b1 == 0:
                    return (num2words(a1) +" hundred")
                else:
                    return (num2words(a1) +" hundred and " + num2words(b1))


def lt_ten_thousand(n):         #less than ten thousand

        a2,b2 = divmod(n,1000)
        if b2 == 0:
                return (ones[a2] +" thousand")
        else:
                return (ones[a2] +" thousand "+ num2words(b2))

def lt_lakh(n):                 #less than lakh
        a3,b3 = divmod(n,1000)
        if b3 == 0:
                return (num2words(a3) +" thousand")
        else:
                return (num2words(a3) +" thousand "+ num2words(b3))

def lt_ten_lakh(n):             #less than ten lakh
        a4,b4 = divmod(n,100000)
        if b4 == 0:
                return (num2words(a4) +" lakh")
        else:
                return (num2words(a4) +" lakh "+ num2words(b4))

def lt_crore(n):                #less than crore
                   
        a5,b5 = divmod(n,100000)
        if b5 == 0:
                return (num2words(a5) +" lakh")
        else:
                return (num2words(a5) +" lakh "+ num2words(b5))

def lt_ten_crore(n):            #less than ten crore
             
        a6,b6 = divmod(n,10000000)
        if b6 == 0:
                return (num2words(a6) +" crore")
        else:
                return (num2words(a6) +" crore "+ num2words(b6))

def lt_hundred_crore(n):        #less than Hundred  crore
                     
        a6,b6 = divmod(n,10000000)
        if b6 == 0:
                return (num2words(a6) +" crore")
        else:
                return (num2words(a6) +" crore "+ num2words(b6))


def num2words(n):
        if 0 <= n < 1000:
                return lt_thousand(n)
        elif 1000 <= n < 10000:
                return lt_ten_thousand(n)
        elif 10000 <= n < 100000:
                return lt_lakh(n)
        elif 100000 <= n < 1000000:
                return lt_ten_lakh(n)
        elif 1000000 <= n < 10000000:
                return lt_crore(n)
        elif 10000000 <= n < 100000000:
                return lt_ten_crore(n)
        elif 100000000 <= n < 1000000000:
                return lt_hundred_crore(n)
        
def func():
    while True:
        try:
            n= input("enter the number(or quit to exit): ")     # user input
                                                        
            if n.lower() == "quit":             #exit criteria
                print("Exiting program.")
                break
                                 
            if n.__contains__("."):        #decimal number checking
                if n[0] == ".":
                    n = "0" + n

                else:   
                    if n[0] == "-" and n[1] == "." :
                        n = n[0]+ "0" + n[1::] 
                splt=n.split(".")       #split by point
                n=float(n)
                
                if -100000000 <= n < 100000000:          #range checking
        
                    n1=[int(i) for  i in splt[1]]
                    
                    n2=int(splt[0])

                    decimal_result= " "
       
                    for val in n1:
                        decimal_result += ones[val]
                        decimal_result += " "
                    if n < 0:
                            
                            print("minus ",end="")
                            print(num2words(abs(n2)),"point",end="")
                            print(decimal_result)
                    else:
                         print(num2words(abs(n2)),"point",end="")
                         print(decimal_result)   
                    
                    continue   
            else:
                number=int(n)                
                               
            if -1000000000 <= number < 1000000000:        #integer range checking
                                            
                if number < 0 :
                        print("minus ",end="")
                        print(num2words(abs(number)))
                else:
                    
                    print(num2words(abs(number)))
                    
            else:
                print("Number out of range. Please enter a number between -100 crore and  100 crore.")
                
        #Error handling
                
        except SyntaxError :
                print("SyntaxError: leading zeros in decimal integer literals are not permitted")       

        except ValueError:
            print("Invalid input. Please enter a valid integer.")
        

# main Function
func()
               

# passwordgenerator
Generate and save passwords...

Import the required modules.
 i.e. string and random
 
We will make a variable i.e. 'forwhat' ,which will handle for what the password user want to generate.
 forwhat = input("Enter the website or application for which you want to generate password:\n")

We will make another integer variable that will take the length of the password.
 length = int(input("Enter the length of password:\n"))
The maximum length of password it can create is 94 because there are only 94 elements we are using here that variable elements is handling.
So of max length crosses it will quit automatically.
See the statement here:
  if length >= 94:
	print("Max length crossed.") 
	quit()

Then will make four variables for four diffrent groups of different elements that is lowercase and uppercase alphabets,punctuations and numbers.
 s1 = list(string.ascii_lowercase)
 s2 = list(string.ascii_uppercase)
 s3 = list(string.digits)
 s4 = list(string.punctuation)
 
After making these for variables that assigns groups of different elements,we will concatenate them all assign to another variable that is elements.
 elements = s1+s2+s3+s4
 
Using shuffle() function of random module,we will shuffle all the elements of that are present in element variable.
 random.shuffle(elements)

The elements present in element variable are present in the form of different lists,so we will join them as shown below:
 password = "".join(elements[0:length])
 As you can I made password variable that will store our final password.
 And in the beginning we took length from user,so we will take specific elememts from 0 to the length that user gave.

Then we will print the generated password.
 print("The safe generated password is :",password,"\n")
 
Till here our basic program is done.

Wait there is more.

Now it will ask whether the user wants to save his password or not.
So here will make if statement.
if saveyn == "Yes":
	f = open("generatedpasswords.txt","a")
	f.write(forwhat + " - " + password+"\n")
	f.close()
	
if saveyn == "No":
	quit()

Here if the input is equal to "Yes" then it will save the password along with website or app(i.e. forwhat variable) to a text file "generatedpasswords.txt".

Now use this program to generate passwords and save them.
No worry about forgiving you passwords now they are saved in a safe file.
Thank you.

Author:. Vishwajeet Bamane



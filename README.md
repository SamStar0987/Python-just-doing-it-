# Python-just-doing-it- Automated File Sorter :
import os , shutil
path = r"C:/Users/ahmed/OneDrive/Desktop/MINE/"
file_name = os.listdir(path)
folder_name = ["txt file", "image file"]

for loop in range (0,2):
    if not os.path.exists(path + folder_name[loop]):
       print(path + folder_name[loop])
       os.makedirs(path + folder_name[loop])

for file in file_name:
    
    if "txt" in file and not os.path.exists(path + "txt file/" + file):
        shutil.move(path + file , path + "txt file/" + file)
        
    elif "jpg" in file and not os.path.exists(path + "image file/" + file):
        shutil.move(path + file , path + "image file/" + file)
        ----------------------------------------------------------------------

# Python-just-doing-it-   BMI Calculator:

name = input("Enter you name: ")

weight = int(input("Enter your wight in pounds: "))
height = int(input("Enter your height in inches: "))

BMI = (weight * 703) / (height * height)

print(BMI)

if BMI>0:
    if(BMI<18.5):
        print(name +", you are underweight.")
    elif (BMI<=24.9):
        print(name +", you are normal weight.")
    elif (BMI<29.9):
        print(name +", you are overweight. You need to exercise more and stop sitting and writing so many python tutorials.")
    elif (BMI<34.9):
        print(name +", you are obese.")
    elif (BMI<39.9):
        print(name +", you are severely obese.")
    else:
        print(name +", you are morbidly obese.")
else:
    print("Enter valid input")
  ---------------------------------------------------------------------------------------------      



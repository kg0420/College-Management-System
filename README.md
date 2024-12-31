# College-Management-System


class collegemanager:
    def __init__(self,name,age,department,feespaid):
        self.name=name
        self.age=age
        self.department=department
        self.feespaid=feespaid
        self.details=[]
    
    def display(self):
        print("1. Add Student")
        print("2. View Student")
        print("3. View Total Fees Paid")
        print("4. Exit")
        print()

    def addstudent(self,name,age,department,feespaid):
        student = {
            "name": name,
            "age": age,
            "department": department,
            "feespaid": feespaid
        }
        self.details.append(student)
    def total_fees_paid(self):
        total = sum(student['feespaid'] for student in self.details)
        print(f"Total Fees Paid by all students: {total}")

    def viewdetails(self):
        for student in self.details:
            print(f"Name: {student['name']}  , Age: {student['age']}  , Department: {student['department']}  ,  Fees Paid: {student['feespaid']}")

    def Exitdetails():
        exit()

if __name__=="__main__":
    object=collegemanager("name","age","department","feespaid")
    while(True):
        object.display()

        choice=int(input("Enter Choice: "))
        if choice==1:
            name=input("Enter the name of student: ")
            age=int(input("Enter Age: "))
            department=input("Enter the department: ")
            feespaid=int(input("Enter Fees paid: "))
            print(object.addstudent(name,age,department,feespaid))

        elif choice==2:
            print(object.viewdetails())

        elif choice==3:
            print(object.Exitdetails())
        elif choice==4:
            print(object.total_fees_paid())


        choice2=input("click c to continue and q to quit:- ")
        if choice2=="c" :
            continue
        elif choice2=="q":
            break
        else:
            print("invalid input..........")

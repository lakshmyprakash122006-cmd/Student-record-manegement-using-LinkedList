# Student-record-manegement-using-LinkedList
Data structure practical program 
# Student Record using Linked List

class Node:
    def __init__(self, id, name):
        self.id = id
        self.name = name
        self.next = None

head = None

def add_student():
    global head
    sid = input("Enter Student ID: ")
    name = input("Enter Student Name: ")

    newnode = Node(sid, name)

    if head is None:
        head = newnode
    else:
        temp = head
        while temp.next:
            temp = temp.next
        temp.next = newnode

def display():
    temp = head
    while temp:
        print("ID:", temp.id, "Name:", temp.name)
        temp = temp.next

while True:
    print("\n1.Add Student 2.Display Students 3.Exit")
    ch = int(input("Enter choice: "))

    if ch == 1:
        add_student()
    elif ch == 2:
        display()
    elif ch == 3:
        break
    else:
        print("Invalid choice")
  output:
  1.Add Student 2.Display Students 3.Exit
Enter choice: 1
Enter Student ID: 101
Enter Student Name: Ravi

Enter choice: 1
Enter Student ID: 102
Enter Student Name: Anu

Enter choice: 2
ID: 101 Name: Ravi
ID: 102 Name: Anu

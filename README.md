# Linked-list-integer-occurence
Counts the number of times an integer occurs in Linked List
# Creating node class

class node:

    def __init__(self,data):

        self.data=data
        self.next=None

# Creating linked list class

class linked_list:

    c=0

    def __init__(self): # Creating header

        self.head=None

# Creating function for inserting data


    def insert(self,new_data):

        new_node=node(new_data)
        temp=self.head

        while(temp!=None and temp.next!=None):

            temp=temp.next

        if(temp!=None):

            temp.next=node(new_data)

        else:

            temp=node(new_data)
            self.head=node(new_data)


# Creating function for printing linked list data


    def print_list(self):
        
        temp=self.head
        
        while(temp):
            
            print(temp.data)
            temp=temp.next
            
# Creating function for counting number of times an integer occurs
# using iteration method


    def count_int(self,key):
         
         count=0
         temp=self.head
         
         while(temp!=None):
             
             if(temp.data==key):
                 count=count+1
                 
             temp=temp.next
             
         return(count)


        


if(__name__=='__main__'):

    llist=linked_list()
    llist.insert(2)
    llist.insert(5)
    llist.insert(2)
    llist.insert(8)
    llist.insert(2)
    print("The linked list is given as:")
    llist.print_list
    print("Using iteration method, the number of times integer 2 occurs is:",llist.count_int(2))
 
    

               
               

    
             
             



    


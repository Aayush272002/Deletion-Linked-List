#include<iostream>
using namespace std;

class Node{
    public:

    int data;
    Node* next;

    //Constructor
    Node(int data){
        this -> data = data;
        this -> next = NULL;
    }
};

void insertatHead(Node* &head , int d){
    Node* temp = new Node(d);
    temp -> next = head;
    head = temp;
}

void print(Node* &head){
    Node* temp = head;

    while(temp != NULL){
        cout << temp -> data << " ";
        temp = temp -> next;
    }
    cout << endl;
}

//DELETION 
void deletefrommiddle(Node* &head , int position , int d){
    
}

int main(){
    //Creating a new node
    Node* Node1 = new Node(10);

    cout << Node1 -> data << endl;
    cout << Node1 -> next << endl;

    //Inserting at head
    Node* head = Node1;
    
    insertatHead(head , 20);
    print(head);

    insertatHead(head , 30);
    print(head);

    insertatHead(head , 30);
    print(head);

    insertatHead(head , 40);
    print(head);

    insertatHead(head , 50);
    print(head);
}

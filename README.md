#include <stdio.h>
#define SIZE 100
int stack[SIZE];
int top=-1;
void push(int value){
if(top==SIZE-1){
printf("Stack Overflow!);
}else{
stack[++top]=value;
printf("%d pushed to stack",value);
}
void pop(){
if(top==-1){
printf("Stack Underflow!Nothing to pop");
}else{
printf("%d is popped from stack\n",stack[top--]);
}
void peek(){
if(top==-1){
printf("Stack is Empty\n");
}else{
printf("top element is:%d\n",stack[top]);
}
void display(){
if(top==-1){
printf("Stack is Empty!\n");
}else{
printf("Stack Elements:\n");
for(int i=top;i>=0;i--){
printf("%d",stack[i]);
}
printf("\n");
}
}
int main(){
int choice,value;
while(1){
printf("Stack operations:");
printf("1.Push\n 2.Pop\n 3.Peek\n 4.Display\n 5.Exit\n");
printf("Enter your choice:");
scanf("%d",&choice);
switch(choice){
case 1:
printf("Enter value to insert:");
scanf("%d",&value);
push(value);
break;
case 2:
pop();
break;
case 3:
peek();
break;
case 4:
display();
break;
case 5:
printf("exiting..!");
return 0;
default:
printf("invalid choice");
}
}
return 0;
}

#include <stdio.h>

int top = -1;
int stack[100];

void push(int x) {
    stack[++top] = x;
}

int pop() {
    return stack[top--];
}

int peek() {
    return stack[top];
}

int isEmpty() {
    return top == -1;
}

void display() {
    for(int i=top;i>=0;i--) printf("%d ",stack[i]);
}

void memoryView() {
    printf("Index  Value  Address\n");
    for(int i=top;i>=0;i--)
        printf("%d      %d     %p\n", i, stack[i], &stack[i]);
}

int main() {
    int choice, val;

    while(1) {
        printf("\n1.Push\n2.Pop\n3.Peek\n4.Display\n5.Memory View\n6.Exit\n");
        scanf("%d",&choice);

        if(choice==1) {
            scanf("%d",&val);
            push(val);
        }

        else if(choice==2) {
            if(isEmpty()) printf("Underflow");
            else printf("Popped: %d", pop());
        }

        else if(choice==3) {
            if(isEmpty()) printf("Empty");
            else printf("%d", peek());
        }

        else if(choice==4) {
            if(isEmpty()) printf("Empty");
            else display();
        }

        else if(choice==5) {
            if(isEmpty()) printf("Empty");
            else memoryView();
        }

        else if(choice==6) break;
    }
    return 0;
}

#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node* next;
};

struct node* top = NULL;

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    for(int i = 0; i < n; i++) {
        struct node* newNode = (struct node*)malloc(sizeof(struct node));
        printf("Enter value: ");
        scanf("%d", &newNode->data);
        newNode->next = top;
        top = newNode;
    }

    printf("Top element: %d", top->data);

    return 0;
}

# ROTATION-AND-TRANSPOSE-OF-SQUARE-MATRIX
#include <stdio.h>
int main() {
int row,column;
printf("Enter Row of matrix: ");
scanf("%d",&row);
printf("Enter column of matrix: ");
scanf("%d",&column);
int arr[row][column];
printf("Enter values : ");
for(int i=0;i<row;i++){
    for (int j=0;j<column;j++){
        scanf("%d",&arr[i][j]);
    }
}
printf("Matrix\n");
for(int i=0;i<row;i++){
    for (int j=0;j<column;j++){
        printf("%d",arr[i][j]);
    }
    printf("\n");
}
for(int i=0;i<row;i++){
    for(int j=0;j<=i;j++){
        int temp=arr[i][j];
        arr[i][j]=arr[j][i];
        arr[j][i]=temp;
    }
}
printf("TRANPOSE\n");
for(int i=0;i<row;i++){
    for (int j=0;j<column;j++){
        printf("%d",arr[i][j]);
    }
    printf("\n");
}
//rotate
for(int i=0;i<row;i++){
    int j=0;
    int k=row-1;
    while(j<k){
        int temp=arr[i][j];
        arr[i][j]=arr[i][k];
        arr[i][k]=temp;
        j++;
        k--; 
    }
}
printf("reverse\n");
for(int i=0;i<row;i++){
    for (int j=0;j<column;j++){
        printf("%d",arr[i][j]);
    }
    printf("\n");
}

return 0;
}

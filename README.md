# Men-para-entregar
#include<stdio.h>
int main(){
    int x,a=0,b=0,c=0,n;
    float cambio;
    char z,z1,z2;

	FILE *f,*r,*m;

	f=fopen("menu.txt","r");
	z=fgetc(f);

	while( z!=EOF ){
            printf("%c",z);
            z=fgetc(f);

	}
	fclose(f);
    while(1){
            printf("1) Torta cubana\n 2) Torta de jamon\n 3) Torta de Milanesa\n");
            scanf("%d", &x);
    switch(x){
    case 1:
        a=a+50;
        b=b+1;
        break;
    case 2:
        a=a+24;
        b=b+1;
        break;
    case 3:
        a=a+35;
        b=b+1;
        break;
    default:
        printf("error");
        }
        r=fopen("orden1.txt", "w");
        printf("Tu orden es:\n %dTorta(s):%d\n", b,a);
        z1=fclose(r);
        printf("Tu orden es:\n %dTorta(s):%d\n", b,a);
        printf("Deseas ordenar algo mas?");
        scanf("%d", &n);
}
        if(n!=0){
        m=fopen("orden2.txt", "w");
        printf("Total a pagar: %d\n Recido: 300\n Cambio:%f", a,cambio=300-a);
        z2=fclose(m);
         printf("Total a pagar: %d\n Recido: 300\n Cambio:%f", a,cambio=300-a);

}
}

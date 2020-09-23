<div align="center">

## DOS  \- Turbo C Calendar


</div>

### Description

Include Display a Calendar in DOS based C Programs, Learn How to calculate day, month year
 
### More Info
 
Month and Year as integers

Modify If applied in Unix-C

Calendar Displayed


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[technicalganesh](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/technicalganesh.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\), Borland C\+\+, UNIX C\+\+
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/technicalganesh-dos-turbo-c-calendar__3-10929/archive/master.zip)





### Source Code

```
#include<stdio.h>
#include<conio.h>
void main()
{
	int month[13]={0,31,28,31,30,31,30,31,31,30,31,30,31};
	int m,d,y,fh,h,f,i,jd=0,dow,j;
	clrscr();
	printf("Enter Month : ");
	scanf("%d",&m);
	printf("Enter the Year : ");
	scanf("%d",&y);
	/* To adjust 29 days for the Leap Year */
	if (y%4==0) month[2]=29;
	for(i=1;i< m; i++)
		jd=jd+month[i];
	jd=jd+1;
	dow=(jd+y+((y-1)/400)+((y-1)/4)-((y-1)/100))%7;
	printf(" Sat Sun Mon Tue Wed Thu Fri\n");
	for(j=0;j< dow;j++) printf("%4s");
	for(i=1;i< month[m]; i++)
	{
		printf("%4d",i);
		j=(j+1)%7;
		if(j==0) printf("\n");
	}
	getch();
}
```


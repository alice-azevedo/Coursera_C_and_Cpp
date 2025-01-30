## C For Everyone: Coding Fundamentals

This course, by professor Ira Pohl, at the Coursera Plataform, was the first one I subscribed to after joining my Free Trial <br>
I have had for a long time been interested in Low-Level Programming, and I thought C was a great place to start.

Here's an Overview of what I learned: 

#### Module One
Learned the basics of C, how to print and get input from the user

```c
#include <stdio.h>
int main(void) {

    printf("Hello World");

    return 0;
}
```
```c
#include<stdio.h>
int main(void)
{   
    printf("Someday, somebody will remember us - I say - Even in another time\n");
    return 0;
} 
```
```c
#include <stdio.h>
int main(void) {

  int radius;
  printf("Enter radius:");
  scanf("%d", &radius);
  printf("volume is : %d \n\n", 4 *radius*radius*radius/3 );

    return 0;
}
```

#### Module Two
Learned how to use the math.h directory to manipulate sine and cosine operations
```c
#include <stdio.h>
#include <math.h>

int main(void) {

    double x;
    printf("Enter a value between 0 and 1: ");
    scanf("%lf", &x);

    if (x > 0 && x < 1) {
        double sine_value = sin(x);
        printf("The sine of %lf is: %lf\n", x, sine_value);
    }
    else {
        printf("Please enter a valid number\n");
    }

    return 0;
}
```
```c
#include<stdio.h>
#include<math.h> 

int main(void)
{ 
    double interval;
    int i;

    for(i = 0; i < 30; i++)
    {
        interval = i / 10.0;
        printf("sin( %lf ) = %lf \t", interval, fabs(sin(interval)));
    }

    printf("\n+++++++\n");

    return 0;
}
```
#### Module Four and Five
Learned about arrays, pointers and functions

```c
#include <stdio.h>
#include <math.h>

/* creates the trigonomic table for 5 angles */
void table() {

	int steps = 5;

	for (int i = 0; i <=steps; i++) {
	
		double angle = (double)i / steps;

		printf("Angle: .2f, Sine: %.4f, Cosine: %.4f\n", angle, sin(angle), cos(angle));

	}
}

int main(void) {

	table();

	return 0;
}

```

```c
#include <stdio.h>

int main(void) {

	int weight[600];
	int num_of_weights = 0;
	double sum_of_weights = 0.0;
	int num_of_data;

	int data[] = {
      5713 	6936 	8764 	6702 	8535 	
	};

	int num_of_data = sizeof(data) / sizeof(data[0]);

	for (int i = 0; i < num_of_data; i++) {

		sum_of_weights += data[i];
	}

	double avarage = sum_of_weights / num_of_data;
	
	printf("the avarage is: %.2f\n", avarage);

return 0;
}
```



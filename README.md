#include <stdio.h>
#include <math.h>
#define f(x) exp(x)*log(sin(x))

int main(void)
{
	double ans = 0;
	for (double i = 0, h = 1; i < 30; h /= 2, i++)
	{
		ans = (f(1 + h) - f(1)) / h;
	}
	printf("%.5f\n", ans);
	
	return 0;
}

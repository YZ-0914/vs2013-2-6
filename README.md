# vs2013-2-6
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>
#include<stdlib.h>

//统计二进制中1的个数
//写一个函数返回参数二进制中1的个数
//比如  15   0000 1111 4个1
//int count_bit_one(unsigned int n)
//{
//	int count = 0;
//	while (n)
//	{
//		if (n % 2 == 1)
//		{
//			count++;
//		}
//		n = n / 2;
//	}
//	return count;
//}

//int main()
//{
//	int a = 0;
//	scanf("%d", &a);
//	//写一个函数求a的二进制（补码）表示中有几个1
//	int count = count_bit_one(a);
//	//-1
//	//10000000000000000000000000000001
//	//11111111111111111111111111111110
//	//11111111111111111111111111111111
//
//	//13
//	//00000000000000000000000000001101
//	//
//	printf("count=%d\n", count);
//	//system("pause");//system库函数 - 执行系统命令 - pause(暂停)
//	return 0;
//}
//int count_bit_one(int n)
//{
//	int count = 0;
//	int i = 0;
//	for (i = 0; i < 32; i++)
//	{
//		if (((n >> i) & 1) == 1)
//		{
//			count++;
//		}
//	}
//	return count;
//}
//int main()
//{
//	int a = 0;
//	scanf("%d", &a);
//	//写一个函数求a的二进制（补码）表示中有几个1
//	int count = count_bit_one(a);
//	//-1
//	//10000000000000000000000000000001
//	//11111111111111111111111111111110
//	//11111111111111111111111111111111
//
//	//13
//	//00000000000000000000000000001101
//	//
//	printf("count=%d\n", count);
//	//system("pause");//system库函数 - 执行系统命令 - pause(暂停)
//	return 0;
//}
//
//int count_bit_one(int n)
//{
//	int count = 0;
//	while (n)
//	{
//		n = n&(n - 1);
//		count++;
//	}
//	return count;
//}
////n=n&(n-1)
////n
////13
////1101 n
////1100 n-1
////1100 n
////1011 n-1
////1000 n
////0111 n-1
////0000 n
//
//int main()
//{
//	int a = 0;
//	scanf("%d", &a);
//	//写一个函数求a的二进制（补码）表示中有几个1
//	int count = count_bit_one(a);
//	//-1
//	//10000000000000000000000000000001
//	//11111111111111111111111111111110
//	//11111111111111111111111111111111
//
//	//13
//	//00000000000000000000000000001101
//	//
//	printf("count=%d\n", count);
//	//system("pause");//system库函数 - 执行系统命令 - pause(暂停)
//	return 0;
//}

////求二进制中不同位的个数
////两个int(32位)整数m和n的二进制表达中，有多少个位（bit）不同？
////1999 2299  7
//int count_bit_one(int tmp)
//{
//	int count = 0;
//	while (tmp)
//	{
//		tmp = tmp&(tmp - 1);
//		count++;
//	}
//	return count;
//}
//
//int get_diff_bit(int m, int n)
//{
//	int tmp = m^n;
//	return count_bit_one(tmp);
//}
//
//int main()
//{
//	int m = 0;
//	int n = 0;
//	scanf("%d%d", &m, &n);
//	int count = get_diff_bit(m, n);
//
//	printf("count=%d\n", count);
//
//	return 0;
//}
//
////交换二进制的奇数位和偶数位
////获取一个整数二进制序列中所有的偶数位和奇数位，分别打印出二进制序列
////思路：
////1.提取所有的奇数位，如果该位是1，输出1，是0则输出0
////2.以同样的方式提取偶数位置
////检测num中某一位是0还是1的公式
////1.将num向右移动1位
////2.将移完位之后的结构与1按位与，如果：
////结果是0，则第i个比特位是0；
////结果是非0，则第i个比特位是1.
//void print(int m)
//{
//	int i = 0;
//	printf("奇数位：\n");
//	for (i = 30; i >= 0; i -= 2)
//	{
//		printf("%d", (m >> i) & 1);
//	}
//	printf("\n");
//	printf("偶数位：\n");
//	for (i = 30; i >= 0; i -= 2)
//	{
//		printf("%d", (m >> i) & 1);
//	}
//	printf("\n");
//}
//int main()
//{
//	int m = 0;
//	scanf("%d", &m);
//	print(m);
//	return 0;
//}


////使用指针打印数组内容
////写一个函数打印arr数组的内容，不使用数组下标，使用指针。arr是一个整形一维数组。
//void print(int *p, int sz)
//{
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d", *(p + i));
//	}
//
//}
//int main()
//{
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	print(arr, sz);
//
//	return 0;
//}

//1*1=1
//2*1=2 2*2=4
//3*1=3 3*2=6 3*3=9
//
//void print_table(int n)
//{
//	int i = 0;
//	for (i = 1; i <= n; i++)
//	{
//		int j = 0;
//		for (j = 1; j <= i; j++)
//		{
//			printf("%d*%d=%-3d ", i, j, i*j);
//		}
//		printf("\n");
//	}
//}
//int main()
//{
//	int n = 0;
//	scanf("%d", &n);
//	print_table(n);
//	return 0;
//}
//字符串逆序（递归实现）
//编写一个函数reverse_string(char * string)（递归实现）
//实现：将参数字符串中的字符反向排列
//要求：不能使用c函数库中的字符串操作函数
#include<string.h>

//void reverse_string(char arr[])
//{
//	int left = 0;
//	int right = strlen(arr) - 1;
//
//	whilr(left < right)
//	{
//		int tmp = arr[left];
//		arr[left] = arr[right];
//		arr[right] = tmp;
//		left++;
//		right--;
//	}
//	
//}
//int main()
//{
//	char arr[] = "abcdef";//fedcba
//	reverse_string(arr);
//	printf("%s\n", arr);
//	return 0;
//}
//int my_strlen(char* str)
//{
//	int count = 0;
//	while (*str != '\0')
//	{
//		count++;
//		str++;
//	}
//	return count;
//}
//void reverse_string(char arr[])
//{
//	int left = 0;
//	int right = my_strlen(arr) - 1;
//
//	whilr(left < right)
//	{
//		int tmp = arr[left];
//		arr[left] = arr[right];
//		arr[right] = tmp;
//		left++;
//		right--;
//	}
//
//}
//int main()
//{
//	char arr[] = "abcdef";//fedcba
//	reverse_string(arr);
//	printf("%s\n", arr);
//	return 0;
//}
//
//void reverse_string(char arr[])
//{
//	char tmp = arr[0];
//	int len = my_strlen(arr);
//	arr[0] = arr[len - 1];
//	arr[len - 1] = '\0';
//	if (my_strlen(arr+1)>=2)
//	reverse_string(arr + 1);
//
//	arr[len - 1] = tmp;
//
//
//}
//int main()
//{
//	char arr[] = "abcdef";//fedcba
//	reverse_string(arr);
//	printf("%s\n", arr);
//	return 0;
//}

//写一个递归函数DigitSum(n),输入一个非负整数，返回组成它的数字之和
//
//例如，调用DigitSum(1729)，则应该返回1+7+2+9，它的和是19
//
//输入：1729，输出：19
//DigitSum(1729)
//DigitSum(172)+1729%10
//DigitSum(17)+172%10+1729%10
//DigitSum(1)+17%10+....
//1+7
//int DigitSum(unsigned int num)
//{
//	if (num > 9)
//	{
//		return DigitSum(num / 10) + num % 10;
//	}
//	else
//	{
//		return num;
//	}
//}
//int main()
//{
//	unsigned int num = 0;
//	scanf("%d", &num);//1729
//	int ret = DigitSum(num);
//	printf("ret=%d\n", ret);
//
//	return 0;
//}


//递归实现n的k次方
//编写一个函数实现n的k次方，使用递归实现。
//int Pow(int n, int k)
//{
//	//n^k=n*n^(k-1)
//	if (k<0)
//		return (1.0/(Pow(n, -k)));
//	else if (k == 0)
//		return 1;
//	else
//		return n*Pow(n, k - 1);
//}
//int main()
//{
//	int n = 0;
//	int k = 0;
//	scanf("%d%d", &n, &k);
//	double ret = Pow(n, k);
//	printf("ret=%lf\n", ret);
//	return 0;
//}

//计算斐波那契数
//递归和非递归分别实现求第n个斐波那契数
//例如：
//输入 5 输出 5
//输入 10 输出 55
//输入 2  输出 1

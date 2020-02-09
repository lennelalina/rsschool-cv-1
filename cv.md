# My own information
*Vladislav Stelmakh*
## Contact information
The name of the means of communication| links(numbers)
-----------------------|------------------------
Phone number|+375(33)304-60-93|
E-mail|stelmakh.vladislav02@mail.ru|
VK|[Vladislav Stelmakh](https://vk.com/vladizlavstelmakh)
## Summary
 My name is Vladislav, I'm from Belarus, Minsk city. I'm 18 years old. I'm in the habit of doing some sport activities such as football, volleyball etc. I'm very hard-working person thanks for it I like to get new knowledge because during working I getting new information for develop my self.
I want to develop myself in the sphere of programming because without knowledge in IT science you can't live in modern world.

I have the task of becoming Front-end Developer. There is just one of my tasks I want to reach.
## Skills
1.Programming languages:
* C, C++;
* Basic HTML5 and CSS;

2.Tools:
* Visual Studio 2019;
* VS code 2019;

### Code examples:
```C++
// The first code example;
#include <locale>
#include <stdio.h>

int main()
{
	setlocale(LC_ALL, "russian");
	int cv, cikl = 0;
	do
	{
		system("cls");
		printf("Меню.\n\n1-Задание №1.\n2-Задание №2.\n3-Задание №3.\n4-Выход.\nВвод: ");
		scanf_s("%d", &cv);
		switch (cv)
		{
		case 1:
		{
			system("cls");
			int a, b, i, j, nMax = 0, nMin = 0;
			float mass[100][100], summ = 0, max = 0, min = 0, value = 0;
			printf("Введите кол-во строк матрицы: ");
			scanf_s("%d", &a);
			printf("Введите кол-во столбцов матрицы: ");
			scanf_s("%d", &b);
			for (i = 0; i < a; i++)
			{
				for (j = 0; j < b; j++)
				{
					printf("Элемент матрицы[%d][%d]: ", i + 1, j + 1);
					scanf_s("%f", &mass[i][j]);
				}
			}
			for (i = 0; i < a; i++)
			{
				max = mass[i][0];
				min = mass[i][0];
				for (j = 0; j < b; j++)
				{
					if (max < mass[i][j])
					{
						max = mass[i][j];
						nMax = j;
					}
					if (min > mass[i][j])
					{
						min = mass[i][j];
						nMin = j;
					}
				}
				value = mass[i][nMax];
				mass[i][nMax] = mass[i][nMin];
				mass[i][nMin] = value;
				nMax = 0;
				nMin = 0;
			}
			printf("\n\nВсе элементы матрицы:\n\n");
			for (i = 0; i < a; i++)
			{
				for (j = 0; j < b; j++)
				{
					printf("Элемент матрицы[%d][%d]: %.1f", i + 1, j + 1, mass[i][j]);
					printf("\n");
				}
			}
			system("pause");
			int maso[100][100], lm, lk, suml = 0;
			printf("Введите, пожалуйста, элементы матрицы(cтроки, столбцы): ");
			for (i = 0; i < lk; i++)
			{
				for (j = 0; j < lk; j++)
				{
					printf("Введите элемент массива[%d][%d]: ");
					scanf_s("%d", &maso[i][j]);
				}
			}
			for (i = 0; i < lk; i++)
			{
				for (j = 0; j < lk; j++)
				{
					if (i == j)
					{
						suml += maso[i][j];
					}
				}

			}
			printf("Сумма элементов главной диагонали: %d", suml);
			break;
		}
		case 2:
		{
			system("cls");
			int matrix[100][100], h, k, n, l = 0, max = 0, number = 0, i, j;
			printf("Введите кол-во строк матрицы: ");
			scanf_s("%d", &h);
			printf("Введите кол-во столбцов матрицы: ");
			scanf_s("%d", &k);
			for (i = 0; i < h; i++)
			{
				for (j = 0; j < k; j++)
				{
					printf("Элемент матрицы[%d][%d]: ", i + 1, j + 1);
					scanf_s("%d", &matrix[i][j]);
				}
			}
			for (i = 0; i < h; i++)
			{
				for (j = 0; j < k; j++)
				{
					if (matrix[j][i] == 0)
						l++;
				}
			}
			printf("\nКоличество столбцов, содержащих нулевой элемент: %d\n\n", l);
			int strk[100];
			for (i = 0; i < h; i++)
			{
				for (j = 0; j < k; j++)
				{
					if (matrix[i][j] == matrix[i][j + 1])
						strk[i]++;
				}
			}
			max = strk[0];
			printf("%d", strk[i]);
			for (i = 0; i < h; i++)
			{
				for (j = 0; j < k; j++)
				{
					if (strk[i] > strk[0])
					{
						max = strk[i];
						number = i;
					}
					else
					{
						max = strk[0];
						number = 0;
					}
				}
			}
			printf("Строка с самой длинной серией одинаковых элементов: %d\n\n", number);
			system("pause");
			break;
		}
		case 3:
		{
			system("cls");
			int mat[100][100], m, v, x, i, j, strok = 0, stolb = 0, elem;
			printf("Введите кол-во строк матрицы: ");
			scanf_s("%d", &m);
			printf("Введите кол-во столбцов матрицы: ");
			scanf_s("%d", &v);
			for (i = 0; i < m; i++)
			{
				for (j = 0; j < v; j++)
				{
					printf("Введите элемент матрицы[%d][%d]: ", i + 1, j + 1);
					scanf_s("%d", &mat[i][j]);
				}
			}
			for (i = 0; i < m; i++)
			{
				for (j = 0; j < v; j++)
				{
					if (mat[i][j] == 0)
					{
						strok = i;
						stolb = j;
						elem = mat[0][j];
					}
				}
			}
			printf("Номер строки, содержащей нулевой элемент: %d\nНомер столбца, содержащего нулевой элемент: %d\n", strok + 1, stolb + 1);
			for (i = 0; i < m; i++)
			{
				for (j = 0; j < v; j++)
				{
					mat[i][j] -= elem;
				}
			}
			printf("Все элементы матрицы:\n");
			for (i = 0; i < m; i++)
			{
				for (j = 0; j < v; j++)
				{
					printf("Элемент матрицы[%d][%d]: %d\n", i + 1, j + 1, mat[i][j]);
				}
			}
			system("pause");
			break;
		}
		case 4:
		{
			system("cls");
			cikl = 1;
			exit(0);
		}
		default: system("cls"); printf("ERROR:\n\n\tУпс!\n\tВы, кажется, ввели не существующий пункт меню - повторите, пожалуйста, попытку!\n\n"); system("pause"); break;
		}
	} while (cikl != 1);
	return 0;
}
```
```C++
//The second code example;
#include <stdio.h>
#include <locale>

int main()
{
	setlocale(LC_ALL, "russian");
	int s, i, maxv = 0, minv = 0, cikl = 0, v;
	double massive[1000], sum = 0, proizv = 1;
	float max = 0, min = 0;
	do
	{
		system("cls");
		printf("Меню.\n\n1-Задание 1.\n2-Задание 2.\n3-Задание 3.\n4-Выход.\n\nВвод: ");
		scanf_s("%d", &v);
		switch (v)
		{
			case 1:
			{
				system("cls");
				printf("Введите размер массива: ");
				scanf_s("%d", &s);
				for (i = 0; i < s; i++)
				{
					printf("Массив [%d] = ", i + 1);
					scanf_s("%lf", &massive[i]);
				}
				system("pause");
				system("cls");
				printf("\nПроизвожу действия с элементами массива...\n\n");
				for (i = 0; i < s; i++)
				{
					sum += massive[i];
					proizv = proizv * massive[i];
				}
				printf("Сумма элементов массива: %.1f\nПроизведение элементов массива: %.1f\n\n", sum, proizv);
				system("pause");
				system("cls");
				min = massive[0];
				for (i = 1; i < s; i++)
				{
					if (min > massive[i])
					{
						min = massive[i];
						minv = i;
					}
				}
				max = massive[0];
				for (i = 1; i < s; i++)
				{
					if (max < massive[i])
					{
						max = massive[i];
						maxv = i;
					}
				}
				printf("\n\nНаибольший элемент массива: %.1f\nНаименьший элемент массива: %.1f\n\n", max, min);
				system("pause");
				system("cls");
				printf("Элемент массива.\n");
				for (i = 0; i < s; i++)
				{
					printf("Массив[%d]: %.1f\n", i + 1, massive[i]);
				}
				float z = massive[minv];
				massive[minv] = massive[maxv];
				massive[maxv] = z;
				system("pause");
				for (i = 0; i < s; i++)
				{
					printf(" Массив[%d]: %.1f\n", i + 1, massive[i]);
				}
				system("pause");
				break;
			}
			case 2:
			{
				system("cls");
				double m2[1000], proizved = 1, maximum = 0;
				int p, j = 0, c;
				printf("Введите размер массива: ");
				scanf_s("%d", &p);
				for (i = 0; i < p; i++)
				{
					printf("Массив[%d]: ", i + 1);
					scanf_s("%lf", &m2[i]);
				}
				printf("\nВведите число C: ");
				scanf_s("%d", &c);
				printf("Считаю кол-во элементов массива больших числа %d...\n", c);
				system("pause");
				for (i = 0; i < p; i++)
				{
					if (c < m2[i])
						j++;
				}
				printf("Кол-во элементов массива: %d\n\n", j);
				maximum = m2[0];
				int mp = 0;
				for (i = 1; i < p; i++)
				{
					float temp = m2[i];
					if (m2[i] < 0)
						temp = m2[i] * -1;
					if (maximum < temp)
					{
						maximum = m2[i];
						mp = i;
					}
				}
				for (i = mp + 1; i < p; i++)
				{
					proizved = proizved * m2[i];
				}
				printf("Произведение элементов массива, больших числа %d: %.2f\n\n", c, proizved);
				system("pause");
				break;
			}
			case 3:
			{
				system("cls");
				int a[100], n, k;
				printf("Введите размер массива: ");
				scanf_s("%d", &n);
				for (i = 0; i < n; i++)
				{
					printf("Массив [%d]: ", i+1);
					scanf_s("%d", &a[i]);
				}
				printf("Введите число K: ");
				scanf_s("%d", &k);
				printf("\n\nЭлементы массива, меньших числа %d: ", k);
				for (i = 0; i < n; i++)
				{
					if (k > a[i])
					{
						printf("%d ", i + 1);
					}
				}
				printf("\n\nЭлементы массива, больших числа %d: ", k);
				for (i = 0; i < n; i++)
				{
					if (k < a[i])
					{
						printf("%d ", i+1);
					}
				}
				printf("\n\nЭлементы массива, равных числу %d: ", k);
				for(i = 0; i < n; i++)
				{
					if (a[i] == k)
					{
						printf("%d ", i + 1);
					}
				}
				printf("\n\n");
				system("pause");
				break;
			}
			case 4:
			{
				cikl = 1;
				system("cls");
				exit(0);
			}
			default: system("cls"); printf("\nУпс!\n\tТакого пункта меню не существует - повторите попытку!\n"); system("pause");
		}
	} while (cikl != 1);
	return 0;
}
```
# Experience
I passed courses about HTML and CSS([Badges](https://www.codecademy.com/users/bit9126210447/achievements), [Courses](https://www.codecademy.com/profiles/bit9126210447)) and learned C/C++ languages at the BSUIR University.

# Education
*A middle school №208*(2008-2019), *BSUIR University*(2019-...), *The Rolling Scopes School*(2020-...)

# English
I have the **B1 level** of English language, but I havn't practice somewhere.

### Hi there π

<!--
**leepureun/leepureun** is a β¨ _special_ β¨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- π­ Iβm currently working on ...
- π± Iβm currently learning ...
- π― Iβm looking to collaborate on ...
- π€ Iβm looking for help with ...
- π¬ Ask me about ...
- π« How to reach me: ...
- π Pronouns: ...
- β‘ Fun fact: ...
-->
#include <iostream>
#include <time.h>
using namespace std;
void Numbergame()
{
	srand(time(0));
	int RanNum = 1 + rand() % 100; //λλ€ν μ«μ μμ±1-100κΉμ§ boolκ°μμ°λΌκ³ ??
	bool Success = false;
	for (int i = 1; i <= 10; ++i) //10λ²μ κΈ°νκ° μμ
	{
		int Num = 0;
		cin >> Num; //μ«μλ₯Ό μλ ₯λ°λλ€
		if (Num > RanNum) { cout << "ν¬λ€" << endl; }
		else if (Num < RanNum) { cout << "μλ€" << endl; }
		else {
			Success = true;
			break;
		}
	}
	if (Success)
		cout << "μ±κ³΅" << endl;
	else
		cout << "μ€ν¨" << endl;
}
int main()
{
	Numbergame();
}

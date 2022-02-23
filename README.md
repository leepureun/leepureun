### Hi there 👋

<!--
**leepureun/leepureun** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
#include <iostream>
#include <time.h>
using namespace std;
void Numbergame()
{
	srand(time(0));
	int RanNum = 1 + rand() % 100; //랜덤한 숫자 생성1-100까지 bool값을쓰라고??
	bool Success = false;
	for (int i = 1; i <= 10; ++i) //10번의 기회가 잇음
	{
		int Num = 0;
		cin >> Num; //숫자를 입력받는다
		if (Num > RanNum) { cout << "크다" << endl; }
		else if (Num < RanNum) { cout << "작다" << endl; }
		else {
			Success = true;
			break;
		}
	}
	if (Success)
		cout << "성공" << endl;
	else
		cout << "실패" << endl;
}
int main()
{
	Numbergame();
}

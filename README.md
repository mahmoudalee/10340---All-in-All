# 10340---All-in-All

#include <iostream>

#include <queue>

using namespace std;

queue<char>q;

int main()
{

	string s, w;
	while (cin >> s >> w) 
	{
		while (!q.empty()) q.pop();

		for (int i = 0; i < s.size(); i++)
		{
			q.push(s[i]);
		}
		for (int i = 0; i < w.size(); i++)
		{
			if (q.empty())
				break;
			if (q.front() == w[i])
				q.pop();
		}
		if (q.empty())
			cout << "Yes" << endl;
		else
			cout << "No" << endl;
	}
	return 0;
}

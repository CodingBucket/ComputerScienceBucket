> Simple C++ program to find the size of int type

```cpp
#include <cstdio>
#include <iostream>

using namespace std;

int main() 
{
    cout << sizeof(int);
    return 0;
}
```
> int array size and value print

```cpp
#include <iostream>

int main()
{
	int a[4] = {10, 11, 12, 13};
	int a_size = sizeof(a)/sizeof(*a);
	for(int i = 0; i < a_size; i++)
		cout << a[i] << endl;
	return 0;
}
```
> String in cpp
```cpp
#include <bits/stdc++.h>

int main()
{
	string s("this is a string.");
	cout << "Length of string is " << s.length() << endl;
	cout << "Character at index 4 is " << s.at(4) << endl;
	s.clear();
	cout << s << endl;
	return 0;
}
```
> Pointer holds ther memory address.
```cpp
int n = 10;
int *pointer = &n;
cout << pointer;
```
> **Stack:** Last in First out. (LIFO)
```cpp
#include <iostream>
#include <stack>

using namespace std;

int main()
{
	stack <int> s;
	s.push(10);
	s.push(20);
	s.push(30);
	cout << "Size of the stack: " << s.size() << endl;
	while(!s.empty())
	{
		cout << s.top() << endl;
		s.pop();
	}
	return 0;
}
```
> **Queue:** First in First out (FIFO)
```cpp
#include <iostream>
#include <queue>

using namespace std;

int main()
{
	queue <int> q;
	q.push(10);
	q.push(20);
	q.push(30);
	cout << "Size of the queue: " << q.size() << endl;
	while(!q.empty())
	{
		cout << q.front() << endl;
		q.pop();
	}
	return 0;
}
```
> **Vector:** Vectors are same as dynamic arrays with the ability to resize itself automatically when an element is inserted or deleted.
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main()
{
    vector<int> v;
    for(int i = 0; i < 5; i++)
        v.push_back(i);
    for(int j = 0; j < 5; j++)
        cout << v[j] << endl;
    cout << "Capacity = " << v.capacity() << endl;
    cout << "Size = " << v.size() << endl;
    cout << "Max size = " << v.max_size() << endl;
    return 0;
}
```
> **Vector Iterators:** 
> * begin() – Returns an iterator pointing to the first element in the vector
> * end() – Returns an iterator pointing to the theoretical element that follows last element in the vector
> * rbegin() – Returns a reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element
> * rend() – Returns a reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end)
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main()
{
    vector <int> g1;
    vector <int> :: iterator i;
    vector <int> :: reverse_iterator ir;

    for (int i = 1; i <= 5; i++)
        g1.push_back(i);

    cout << "Output of begin and end: ";
    for (i = g1.begin(); i != g1.end(); ++i)
        cout << *i << ' ';

    cout << endl;

    cout << "Output of rbegin and rend: ";
    for (ir = g1.rbegin(); ir != g1.rend(); ++ir)
        cout << ' ' << *ir;

    return 0;
}

```

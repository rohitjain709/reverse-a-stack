# reverse-a-stack

/******************************************************************************

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <iostream>
#include <stack>
using namespace std;


void insert(stack <int> &st,int a)
{
    if(st.empty())
    {
      st.push(a);
      return ;
    }
int t = st.top();
st.pop();
insert(st,a);
st.push(t);

    
    
}

void rev(stack <int> &st)
{
    if(st.empty())
    {
        return;
    }
    
    int a=st.top();
    st.pop();
    rev(st);
    insert(st,a);
    
    
}

int main()
{
      stack<int> s;

    

    s.push(10);

 
    s.push(30);

    s.push(40);
     
     rev(s);
     while(!s.empty()){
        cout<<s.top()<<endl;
        s.pop();
    }
    
    
    
      
     while(!s.empty()){
        cout<<s.top()<<endl;
        s.pop();
    }

    return 0;
}

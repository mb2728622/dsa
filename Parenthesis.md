#include<iostream>
using namespace std;

class parenthesis {
    char str[20];
    char s1[20];
    int top;
    pubic:
parenthesislic:
    (){
        top=-1;
    }
    int isstackfull();
    int isstackempty();
    void push(char );
    char pop();
    void checkwellness();
};

int parenthesis::isstackfull(){
    if(top==19){
        return 1;
    }
    else {
        return 0;
    }
}


int parenthesis::isstackempty (){
    if(top==-1){
        return 1;
    }
    else{
        return 0;
    }
}

void parenthesis::push(char x){
    top=top+1;
    s1[top]=x;
    
}


char parenthesis::pop(){
    char x2;
    x2=s1[top];
    top--;
}

void parenthesis::checkwellness (){
    int i=0;
    char p;
    cout<<"Enter the string :"<<endl;
    cin>>str;
    
    while(str[i]!='\0'){
        p=str[i];
        if(p=='(' || p=='{' || p=='['){
            push(p);
        }
        else if(p==')' || p=='}' ||p==']'){
            pop();
        }
        i++;
    }
    
    if(isstackempty ()){
        cout<<"\nGiven string is parenthesized "<<endl;
    }
    else{
        cout<<"\nGiven string is NOT parenthesized"<<endl;
    }
}


int main(){
    parenthesis p1;
    char ans='n';
    do{
        p1. checkwellness ();
        cout<<"\nYOU WANTS CHECK ANOTHER STRING (y/n) :-"<<endl;
        cin>>ans;
    }
    while(ans=='y' || ans=='Y');
}

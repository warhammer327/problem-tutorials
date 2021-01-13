# LOJ 1107 - How Cow
*You are given the lower-left and upper-right coordinates of a rectangle field. Then you are also given M coordinates. You have to print 'Yes' for the coordinates that are inside the rectangle, otherwise print 'No'.*
___
### Summary 
This is a straight geometry problem. Let us assume, ```(x1,y1)``` is the lower-left coordinate, ```(x2,y2)``` is the upper right coordinate, ```(p,q)``` is coordinate for the cow. The cow will be in the rectangle field, if ```p``` on the x-axis has a value between ```x1``` and ```x2```. If simply put, value of p has to be ```x1<=p<=x2```. In the same way, value of y has to be ```y1<=q<=y2```.  

*The trick is to keep in mind that if a cow is standing on the line, it should be treated as it is inside the rectangle.*
### Solution
- Inside each test case, take input for the value of ```x1```,```y1```,```x2```,```y2```.
- Take input of ```m``` which indicates the number of cows.
- Print the serial of the test case.  
- Start a loop with that runs ```m``` times. 
- Inside this new loop, take input of ```p``` and ```q```. 
- If  ```x1<=p<=x2``` and ```y1<=q<=y2``` both are true, print ```Yes```. 
- Else, print ```No```. 
___
### Code in C++
```cpp
int main()
{    
    int cs,x1,y1,x2,y2,p,q,m,t;
    scanf("%d",&t);
    for(cs=1;cs<=t;cs++){
        scanf("%d %d %d %d",&x1,&y1,&x2,&y2);
        scanf("%d",&m);
        printf("Case %d:\n",cs);
        while(m--){
            scanf("%d %d",&p,&q);
            if ((x1<=p && p<=x2) && (y1<=q && q<=y2)) {
                printf("Yes\n");
            }
            else
                printf("No\n"); 
        }
    }
    return 0;
}
```





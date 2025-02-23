# Given a 2D matrix, Compute the the principal and secondary diagonal and return their absolute differences

```C++
long int compute(std::vector<vector<int>> Matrix){
    int sizeOfEachElement = Matrix[0].size();
    long principalDiagonal = 0;
    long secondaryDiagonal = 0;
    for(int i=0; i<sizeOfEachElement; i++){
        principalDiagonal+= arr[i][i]
        secondaryDiagonal+=arr[i][columSize-(i+1)];
    }
    return std::abs(principalDiagonal-secondaryDiagonal);
}
int main(){
    std::vector<vector<int>> Mat = {
        {1, 2, 3},
        {4, 5, 6},
        {9, 8, 9}
    }
    std::cout << compute(Mat) << stdd::endl;
}
```

# Given an unsorted array of positive integers, print out the minimum and maximum of 4 numbers that can be calculated from the array
```C++
    inline int MIN(int a, int b){
    return (a>b) ? b : a;
}
inline int MAX(int a, int b){
    return (a>b) ? a : b;
}
void miniMaxSum(vector<int> arr) {
    /*
    Algorithm
    1.) For min - Get first 4 elements, check if last element is less than any, then change
    2.) For max - Do same as above
    */
    long int min = 0;
    long int max = 0;
    int currentMin = arr.at(0);
    int currentMax = arr.at(0);
    for(int i=0; i<arr.size();i++){
        currentMax = MAX(arr.at(i),currentMax);
        currentMin = MIN(arr.at(i),currentMin);
    }
    for(int i=0;i<arr.size();i++){
        min+=arr.at(i);
        max+=arr.at(i);
    }
    min-=currentMax;
    max-=currentMin;
    std::cout<<min<<" "<<max<<std::endl;
}

int main(){
    std::vector<int> values = {1,2,3,4,5}
}
```
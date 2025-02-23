# Given a 2 matrix, Compute the the principal and secondary diagonal and return their absolute differences

```c++
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
````
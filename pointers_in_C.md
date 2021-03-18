# Pointers in C

### Swap two 2D arrays
```
void swap(int** a, int** b){
    int* temp = *a;
    *a = *b;
    *b = temp;
}
```

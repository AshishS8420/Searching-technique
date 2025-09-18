import java.lang.*;
class Test {
    public static int binarySearch(int A[], int left, int right, int x) {
        int mid;
        while (left <= right) 
        {
            mid = (left + right)/2;
            if (A[mid] == x) {
                return mid;
            } 
            else if (A[mid] > x) 
            {
                right = mid - 1;
            } 
            else 
            {
                left = mid + 1;
            }
        }
        return -1;
    }
}

public class Search 
{
    public static void main(String[] args) 
    {
        int A[] = {112, 231, 301, 445, 619, 718, 738};
        int n = A.length;
        int x = 119;

        
        int result = Test.binarySearch(A, 0, n - 1, x);

        if (result == -1) 
        {
            System.out.println("Flight no  is not found"  +x);
        } 
        else 
        {
            System.out.println("Flight no  is found "  +x);
        }
    }
}# Searching-technique

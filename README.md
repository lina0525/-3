import java.util.Scanner;  
import java.util.Stack;  
  
public class Main {  
  
    public static void main(String[] args) {  
        Scanner sc =new Scanner(System.in);  
        Stack<Integer> st =new Stack<>();  
        int a=0,b=0;  
        while (sc.hasNext()){  
            String s=sc.next();  
            switch (s){  
                case "+":  
                b=st.pop();  
                a=st.pop();  
                st.push(a+b);  
                break;  
                case "-":  
                    b=st.pop();  
                    a=st.pop();  
                    st.push(a-b);  
                    break;  
                case "*":  
                    b=st.pop();  
                    a=st.pop();  
                    st.push(a*b);  
                    break;  
                case "/":  
                    b=st.pop();  
                    a=st.pop();  
                    st.push(a/b);  
                    break;  
                default:  
                    st.push(Integer.parseInt(s));  
            }  
        }  
        System.out.println(st.peek());  
    }  
}  

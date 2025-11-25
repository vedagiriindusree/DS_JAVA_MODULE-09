# Ex16 Check for Balanced Parentheses Using Stack
## DATE:25/11/2025
## AIM:
To write a Java program that verifies whether the parentheses (brackets) in an input string are balanced — meaning each opening bracket (, {, [ has a corresponding and correctly ordered closing bracket ), }, ].

## Algorithm
1. Start the program.
2. Create an empty stack.
3. Traverse each character in the string.
4. Push opening brackets onto the stack.
5. When a closing bracket is encountered, check if it matches the top of the stack.
7. If any mismatch or leftover element exists, the parentheses are not balanced.
8. If the stack is empty at the end, the parentheses are balanced.
## Program:
```
/*
/*
Program to verify whether the parentheses (brackets) in an input string are balanced
Developed by: Vedagiri Indu Sree
RegisterNumber: 212223230236
*/
import java.util.*;

public class BalancedParentheses {
    public static boolean isBalanced(String str) {
        Stack<Character> stack = new Stack<>();
        for (char ch : str.toCharArray()) {
            if (ch == '(' || ch == '{' || ch == '[') {
                stack.push(ch);
            } else if (ch == ')' || ch == '}' || ch == ']') {
                if (stack.isEmpty()) return false;
                char top = stack.pop();
                if ((ch == ')' && top != '(') ||
                    (ch == '}' && top != '{') ||
                    (ch == ']' && top != '['))
                    return false;
            }
        }
        return stack.isEmpty();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter expression: ");
        String expr = sc.nextLine();
        if (isBalanced(expr))
            System.out.println("Balanced");
        else
            System.out.println("Not Balanced");
        sc.close();
    }
} 
*/
*/
```

## Output:
<img width="406" height="58" alt="image" src="https://github.com/user-attachments/assets/a824562e-0f52-44d2-8f7f-6a51990de867" />

## Result:
Thus,the program correctly checks whether an input string has balanced parentheses using a stack.

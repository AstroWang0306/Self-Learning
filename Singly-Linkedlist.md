To check if a singly linked list is continous or not, we can use `slow and fast` startegy. 

Problem:

Given head, the head of a linked list, determine if the linked list has a cycle in it.
There is a cycle in a linked list if there is some node in the list that can be reached again by continuously following the next pointer. Internally, pos is used to denote the index of the node that tail's next pointer is connected to. Note that pos is not passed as a parameter.

Solution:

public class Solution {

    public boolean hasCycle(ListNode head) {
    
        if (head == null) {
        
            return false;
            
        } else {
        
            ListNode fast = head;
            
            ListNode slow = head;
            
            while (fast.next != null && fast.next.next != null) {
            
                slow = slow.next;
                
                fast = fast.next.next;
                
                if (slow == fast) {
                
                    return true;
                    
                }
                
            }
            
            return false;
            
        }
        
    }
    
}

Reasons why use `fast and slow` strategy:

1. Declare two new listNodes: slow and fast
2. In the while loop, `slow = slow.next` and `fast = fast.next.next`, use if statement.
3. Assume the singly linked list is continuos, slow and fast will be the same eventually. 
4. If it is not continuos, it will jump out of the while loop and return false.






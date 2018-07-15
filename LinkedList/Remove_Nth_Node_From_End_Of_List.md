##Remove Nth Node From End of List

Given a linked list, remove the n-th node from the end of list and return its head.

Example:

Given linked list: 1->2->3->4->5, and n = 2.

After removing the second node from the end, the linked list becomes 1->2->3->5.
Note:

Given n will always be valid.

Follow up:

Could you do this in one pass?

My Answers:

C++:

class Solution{
  ListNode* RemoveNthNode(ListNode* node, int N){
    ListNode newNode = ListNode(-1);
    newNode.next = &node;
    ListNode* first = newNode;
    ListNode* second = newNode;
    
    while(N > 0){
        first = firs->next;
        N--;    
    } 
    while(!first.next){
        first = first->next;
        second = second->next;    
    }
    
    ListNode* to_be_deleted = second.next;
    second->next = second->next->next;
    delete to_be_deleted;
    return newNode.next;
    
  }

}



Java:





Python3:


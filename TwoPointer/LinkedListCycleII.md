Given a linked list, return the node where the cycle begins. If there is no cycle, return null.

Note: Do not modify the linked list.

Follow up:
Can you solve it without using extra space?


Python3:
class ListNode(object):  
  def __init__(self, x):
    self.val = x
    self.next = None
    
class Solution(object):
  def LinkedListCycleII(self, head):
    if not head:
      return head;
    slow, fast = head, head
    while(fast and fast.next and slow != fast):
      slow = slow.next
      fast = fast.next.next
    if(fast is None or fast.next is None):
      return None
    fast = head
    while(slow != fast):
      slow = slow.next
      fast = fast.next
    return slow
      
    
    

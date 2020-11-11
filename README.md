# OS-Project-5th-SEM
  The analogy is based upon a hypothetical barber shop with one barber. There is a barber shop which has one barber, one barber chair, and n chairs for waiting for customers if there are any to sit on the chair.

ABSTRACT

Topic: Sleeping Barber problem in Process Synchronization

Prerequisite – Inter Process Communication

Problem: The analogy is based upon a hypothetical barber shop with one barber. There is a barber shop which has one barber, one barber chair, and n chairs for waiting for customers if there are any to sit on the chair.


•	If there is no customer, then the barber sleeps in his own chair.
•	When a customer arrives, he has to wake up the barber.
•	If there are many customers and the barber is cutting a customer’s hair, then the remaining customers either wait if there are empty chairs in the waiting room or they leave if no chairs are empty.

Solutions:
Many possible solutions are available. The key element of each is a mutex, which ensures that only one of the participants can change state at once. The barber must acquire/enforce this mutual exclusion (of room status) before checking for customers and release it when they begin either to sleep or cut hair. A customer must acquire it before entering the shop and release it once they are sitting in either a waiting room chair or the barber chair, and also when they leave the shop because no seats were available. This eliminates both of the problems mentioned in the previous section. A number of semaphores is also required to indicate the state of the system. For example, one might store the number of people in the waiting room.
A multiple sleeping barbers problem has the additional complexity of coordinating several barbers among the waiting customers.



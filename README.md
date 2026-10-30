# DMA-access-controller
Smart Airport Check-in Queue System
A console based C college project demonstrating FIFO queues , circular queues , and multiple counters in an airport check-in and baggage drop scenario.

Features
Generates sequential passenger tokens such as AP-001.

Maintains one circular FIFO queue per check-in counter/desk.

Assigns each new passenger to the counter with the shortest line.

Allows ground staff to call the next passenger and process their boarding pass and baggage.

Displays all queues and the currently served passenger.

Looks up a passenger token's position and estimated waiting time.

Shows the number of completed check-ins.
How the queue works:
Each counter has a fixed-size circular array with front, rear, and size fields. Enqueue advances the rear index with modulo arithmetic; dequeue advances the front index the same way. This reuses array slots after passengers leave, while keeping FIFO order.   

For passenger assignment, the program compares the number waiting plus the passenger currently being served at each counter. Estimated waiting time assumes each check-in process takes three minutes.   

Menu:
Issue a passenger check-in token

Call the next passenger at a counter

Complete the current check-in (then automatically call the next)

Display all counter queues

Check a passenger's token status

Show completed check-in count

Exit

Project scope:
  
This is a single-computer classroom simulation. Queue state exists only while the program is running. Each counter can hold up to 100 waiting passengers.

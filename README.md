# ♟️ Chess Game Using Multithreading

A mini project developed in C using **POSIX threads (Pthreads)** to implement a simple chessboard simulation. This project demonstrates how multithreading can enhance interactivity, simulate concurrent player actions, and apply synchronization principles from operating systems.

---

## 📌 Project Overview

This project explores how **multithreading** can be used to handle:
- **User input** (through one thread)
- **Computer moves** (through another thread)
- **Shared game state logic** (chessboard updates)

Each component runs concurrently using **pthreads**, enabling a basic turn-based chess game experience with input validation and board updates.

---

## 🧵 Technologies Used

- **C Programming**
- **POSIX Threads (pthreads)**
- **Multithreading**
- **Linux/GCC environment**

---

## 🧠 Concepts Applied

- Thread creation and execution using `pthread_create`
- Synchronization (planning for locks and semaphores)
- Game state sharing between threads
- Basic console-based input/output for chess moves

---

## 🔩 How It Works

- `user_thread_func`:
  - Handles user input (source and destination coordinates)
  - Validates and updates the chessboard
  - Ends game when user enters -1 -1 -1 -1

- `computer_thread_func`:
  - Placeholder thread for future AI or automated response logic

- Threads are joined at the end using `pthread_join`

---

## 📄 Sample Code Snippet

```c
pthread_t user_thread;
pthread_create(&user_thread, NULL, user_thread_func, NULL);

pthread_t computer_thread;
pthread_create(&computer_thread, NULL, computer_thread_func, NULL);

pthread_join(user_thread, NULL);
pthread_join(computer_thread, NULL);
```

---

## 🖥️ How to Compile & Run

```bash
gcc -o chess_game chess_game.c -lpthread
./chess_game
```

💡 You must have `gcc` and `pthread` support installed (Linux recommended).

---

## ✅ Features

- Multithreaded simulation
- Basic move validation
- Game ends with user exit command
- Modular design for extending AI logic

---

## 🔮 Future Enhancements

- Add full move legality checks based on chess rules
- Implement basic AI for computer moves
- Add mutex locks for shared memory safety
- Visual representation using graphics libraries (optional)

---

## 📚 References

1. [GeeksforGeeks - Multithreading in C](https://www.geeksforgeeks.org/multithreading-in-c/)
2. [TutorialsPoint - Multithreading](https://www.tutorialspoint.com/multithreading-in-c)
3. [POSIX Thread Programming](https://man7.org/linux/man-pages/man7/pthreads.7.html)
4. [YouTube Guide](https://www.youtube.com/watch?v=L7F4vsPl3sE)

---

## 📞 Contact Me
Feel free to reach out to me via email at bhuvani1102@gmail.com or connect with me on LinkedIn at https://www.linkedin.com/in/bhuvani1102


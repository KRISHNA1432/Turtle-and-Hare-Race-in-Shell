# Turtle-and-Hare-Race-in-Shell
Turtle and hare race shell script simulator with real time inter process communication to behave randomly. With wild card entries like, GOD to manipulate positions of racers.

System Programming

Assignment: Hare and Turtle

Prerequisite:- Carefully read the following man pages: signal, kill, ualarm, umask, sigprocmask,
gettimeofday, wait, exec, fork, pipe,open, ipc, clone, msgctcl, msgsnd, msgrcf, rand, srand48.

Situation:-
As we know since our childhood, hare and turtle went for a race, and turtle wins !! why ? may be
God was on it’s side. Now, let’s recreate the scene and assert that it’s the God who decides the
winner. We have four entities who are working in this scenario,

Turtle()

{

	while (not finish)
	
	{
	
		moveleg1();
	
		moveleg2();
		
		moveleg3();
		
		moveleg4();
	
	}

}

Hare()

{

	while (not finish)

	{

		while (Turtle is far behind)

		Sleep(for_a_while);

		RunLikeCrazy_A_bit();

	}

}

God()

{

	while (game not over)

	{

		wait for keyboard;

		choose hare or turtle from keyboard;

		reposition hare or turtle;

	}

}

Report()

{

	while (game not over)

	{

		report positions of hare and turtle;

		/* use ncurses for graphics if you are ambitious,

		printf otherwise */

	}

}

Main()

{

	fork {

		Tutle();

		Hare();

		God();

		Report();

	}

	loop until somebody wins;

}


Task 1: Processes:-

1. Expand the process descriptions and implement IPC solutions by defining cooperating
processes fora.Turtle b.Hare c.God d.Reporter

2. Use fork() and execve() to create the processes and develop complete applications using
Linux IPC (message passing) mechanisms: pipes.

Task 2: Threads:-
Now, develop the same application (hare and turtle) using Linux pthreads (shared memory).
Notice that you have shared memory between threads so you do not need explicit
communication channels. You can communicate using shared variables. However, you will
need to ensure that different threads synchronize their access to shared variables to avoid
inconsistencies. In particular, you should use mutexes (see tutorial) to protect all accesses to
shared variables.

Reading Material:- For pthreads tutorial, you may go through this link:
http://www.yolinux.com/TUTORIALS/LinuxTutorialPosixThreads.html

Tests:-
● The current outcome of the race should be displayed after fixed intervals.
● Try varying the speed and the sleeping time of the hare to see different outcomes.

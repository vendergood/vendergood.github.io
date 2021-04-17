---
title: 'Operating Systems'
subtitle: '운영체제·랩 관련 공부한 내용들'
date: 2021-03-11 00:00:00
featured_image: '/images/under-construction.jpg'
---

![](/images/under-construction.jpg)


*****
## Intro
 
우선 옛날얘기 부터 해보자. 사실 컴퓨터라는 것의 역사가 그리 길지는 않다. 1900년대 중반, 이 시기에 최초의 컴퓨터가 탄생하게 된다. 

최초의 컴퓨터가 어떻게 발전하게 되고, 그리고 그 과정에서 운영체제가 어떤 역할을 하게 되었는지 한번 살펴보자.
 
 
### ● 1G (1945-55)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
1세대 컴퓨터라 하는 것은 Vacuum Tubes(진공관)와 Plugboard(플러그판)의 조합이었다. 그래서 사진에 보이는 것 처럼, 거대한 기계들의 거대한 진공관들이 박혀있고, 그런것들이 서로 연결해 가면서 계산을 하는 그런 기계였던 것이다. 
 
우리가 흔히 최초의 컴퓨터라고 하는 이 ENIAC 시스템이 이 진공관들로 이루어진 시스템이다. 
 
이 시기에는 OS, 프로그래밍 언어, 어셈블리 언어.. 이런것들이 존재하지 않았다. 그냥 단순한 기계적인 시스템으로 필요한 계산들을 했던 것이다.
 
### ● 2G (1955-65)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
이 다음 세대는 트랜지스터. 트랜지스터라는 소재에 의해서 그 다음 컴퓨팅 시스템의 시대가 열리게 되는데, 이런 트랜지스터라는 소재료를 활용해서 Mainframe이라는 시스템이 만들어졌다.  Mainframe는 아주 거대한 컴퓨터였고, 다수의 사람들이 공유해서 사용하는 그런 컴퓨터를 일컫는 말이다. 다만 현대와 같은 발전된 형태의 Computing System은 아니었다.

이때는 Batch System이라고 얘기했다. 거대한 컴퓨터는 있지만, 이 거대한 컴퓨터에서 한번의 하나의 프로그램만 작동할 수 있었던 것이다.

이 시기의 OS는 어느 한 순간에 하나의 프로그램을 돌리기만 하면 되었기 때문에, 이 시기의 OS는 Library의 형태에 가까웠다고 한다.
 
우리가 흔히 최초의 컴퓨터라고 하는 이 ENIAC 시스템이 이 진공관들로 이루어진 시스템이다. 
 
이 시기에는 OS, 프로그래밍 언어, 어셈블리 언어.. 이런것들이 존재하지 않았다. 그냥 단순한 기계적인 시스템으로 필요한 계산들을 했던 것이다.

### ● 3G (1965-80)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
이 다음 세대는 IC 회로(Integrated Circuit)의 등장으로 인해서, 컴퓨팅 성능이 급증하게 되고, 가격은 낮아지게 되었다.

또한 Disk drives나 On-line terminals과 같은 하드웨어들도 등장하기 시작했고, 이로 인해서 Computer Architecture 라는 개념이 등장하였다.

System call 이라는 개념도 이때 등장하게 된다. 이는 우리가 소프트웨어를 만들때, 운영체제 혹은 하드웨어가 제공하는 기능들을 사용하기 쉽게 제공해주는 일종의 인터페이스이다. 

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>

이런 IC 기반의 컴퓨터들로부터, 현대 컴퓨터 운영체제의 기틀이 다져지기 시작하는데, 그중의 하나의 특성이 바로 Multiprogrammed systems 이다.

아까 위에서 Batch System 라고 언급한것이 있다. 이는 거대한 컴퓨터에서 한번의 하나의 프로그램만 작동할 수 있었던 것인데, Multiprogrammed systems는 이런 형태를 벗어난 것이다.

Multiprogrammed systems으로 인해, OS의 중요성이 매우 높아지게 되었다. 하나의 컴퓨터 시스템에서 여러 개의 프로그램을 돌아가려면 여러개의 소프트웨어가 하나의 하드웨어를 공유해야 하는데, 이에 의한 여러 문제점들이 발생하기 때문이다.

대표적인 문제 중의 하나가 바로 Memory management이다. 제한된 Memory 영역에서 여러개의 소프트웨어가 돌아가려면, 어떤 소프트웨어가 어디까지 Memory를 쓰게 할지가 관건인 것이다.

또다른 대표적인 문제로 Protection이 있다. 하나의 소프트웨어가 다른 소프트웨어가 돌아가는 영역을 침범하면 안되는 것이다.


<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>

Multiprogrammed systems에서 중요한 개념중에 하나는 바로 Time-sharing systems이다.

Time-sharing systems은 짧은 시간 간격으로 CPU를 각 프로세스에 할당하여 마치 여러 프로세스들이 동시에 CPU를 할당 받아 동작하는 것처럼 만드는 것을 말한다.

Time-sharing systems을 실행을 하기 위해서는 더 복잡한 OS가 필요하게 된다. Time-sharing systems이 가능하게 되면서 Batch System 처럼 기다릴 필요없이 다수의 사용자가 동시에 접속할 수 있게 되었다.

### ● 4G (1980-)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
이 다음 세대는 IC 회로(Integrated Circuit)의 집적도가 급증하게 되어서, LSI(Large Scale Integration) 및 VLSI(Very Large Scale Integration) 등의 회로들이 등장하게 되어 컴퓨터가 소형화되고 성능도 발전하게 되었다. PC(Personal Computer)이 이 시기에 탄생하게 된다.

우리에게 친숙한 현대적인 멀티미디어, 인터넷, 모바일 등등의 GUI(Graphical User Interface)가 이때 발전하게 되었다.

*****
## OS concepts

프로그램이 실행될때, 무슨 일이 일어날까? 프로그램이 시작된다는 것은 다음의 Instructions을 하나하나 연속적으로 실행한다는 것이다.

1. Fetch라는 과정을 통해서, 메모리에서 Instruction을 하나 가져온다.
2. 그 다음, Decoding을 하여 이 Instruction이 과연 어떤 Instruction인지를 해석을 한다.
3. 그리고 나서 Instruction를 Decode하여 해석한 결과에 따라 Instruction을 Execute 한다.
4. 한 Instruction이 끝난 후, 다른 Instruction에 대해 ①~③ 과정을 무한 반복한다.

이런 과정 내에서 OS는 컴퓨터 시스템이 올바르고 효율적으로 작동할 수 있게 도와주는 역할을 한다.

### Virtualization

Virtualization(가상화) = OS가  Processor, Memory, Disk와 같은 물리적인 자원을 Virtual Form, 즉 가상적인 형태로 변환해서 유저나 어플리케이션들에게 제공하는 것. Virtual Form은 좀더 일반적이고, 유용하고, 더쉽게 쓸수 있는 형태이다.

그렇기에 우리는 OS를 Virtual Machine이라고 부른다.

### System call

System call은 사용자가 컴퓨터 시스템의 민감한 부분을 건드리지 않고, 그것을 OS보고 대신 제어해달라는 형태의 인터페이스이다. OS는 API등의 인터페이스를 제공을 한다. 

그리고 그 API 인터페이스들은 OS 차원에서 이 시스템을 제어할 수 있는 온갖 일을 한다. (ex. Run programs, Access memory, Access devices)

### The OS is a resource manager

OS는 CPU, Memory, Disk와 같은 리소스들을 관리해주기 때문에, 다음과 같은 것들을 가능하게 한다.

* 여러 개의 프로그램이 동시에 run하고 싶다 ㅁ CPU를 공유하게 해준다.
* 시스템에서 돌아가는 여러 개의 프로그램들이 Memory에 동시에 access하고 싶다 ➜ Memory를 공유하게 해준다.
* 컴퓨터에 붙어있는 많은 access 기기를 여러 프로그램들이 사용하고 싶다 ➜ Disk를 공유하게 해준다.

### Virtualizing the CPU

CPU를 Virtualizing한다는 말의 의미는, 물리적으로는 한계가 존재하는 CPU를 수의 제한이 없는 여러개의 CPU로 보이게끔 만들어주는 기술이다.

예를 들어, 다음과 같은 예제가 있다.

##### Simple Example(cpu.c): Code That Loops and Prints
```html
1 	#include <stdio.h>
2 	#include <stdlib.h>
3 	#include <sys/time.h>
4 	#include <assert.h>
5 	#include "common.h"
6
7 	int
8 	main(int argc, char *argv[])
9 	{
10	 	if (argc != 2) {
11	 	fprintf(stderr, "usage: cpu <string>\n");
12	 	exit(1);
13	 	}
14	 	char *str = argv[1];
15	 	while (1) {
16	 		Spin(1); // Repeatedly checks the time and returns once it has run for a second
17	 		printf("%s\n", str);
18	 	}
19 		return 0;
20 	}
```

이 파일을 compile해서 실행을 해보면, 

```html
prompt> gcc -o cpu cpu.c -Wall
prompt> ./cpu "A"
A
A
A
ˆC
prompt>
```

이렇게 argv[1] 에 해당하는 A라는 문자가 반복적으로 출력이 된다. 그리고 ˆC를 누르면 이 프로그램이 강제로 종료된다.

그런데 앞에서 만든 이 cpu.c라는 프로그램을 동시에 4개를 실행을 한다면?

```html
prompt> ./cpu A & ; ./cpu B & ; ./cpu C & ; ./cpu D &
[1] 7353
[2] 7354
[3] 7355
[4] 7356
A
B
D
C
A
B
D
C
A
C
B
D
...
```

실행을 해보면, 4개의 프로그램이 동시에 실행이 되는것 처럼 보인다. 다만 내부적으로는 그렇지 않다. CPU가 하나 뿐이어도 4개의 프로그램 모두 동시에 실행되는 것처럼 '보이는' 것이다.

### Virtualizing Memory

Virtualization 에서 또다른 중요한 자원은, Physical Memory이다. Physical Memory는 bytes의 array처럼 생겼다.

어떤 프로그램을 우리가 실행한다고 했을 때, 그것은 Memory를 통해서 읽고 쓰게 되는 것이다.

예를 들어, 다음과 같은 예제가 있다.

##### A program that Accesses Memory (mem.c)
```html
1 	#include <unistd.h>
2 	#include <stdio.h>
3 	#include <stdlib.h>
4 	#include "common.h"
5
6 	int
7 	main(int argc, char *argv[])
8 	{
9 		int *p = malloc(sizeof(int)); 	// a1: allocate some memory
10 		assert(p != NULL);
11 		printf("(%d) address of p: %08x\n",
12 		getpid(), (unsigned) p); 	// a2: print out the address of the memory
13 		*p = 0; 			// a3: put zero into the first slot of the memory
14	
15 		while (1) {
16 			Spin(1);
17 			*p = *p + 1;
18 			printf("(%d) p: %d\n", getpid(), *p); // a4
19 		}
20 	return 0;
21 	}
```

이 파일을 compile해서 실행을 해보면, 

```html
prompt> ./mem
(2134) memory address of p: 00200000
(2134) p: 1
(2134) p: 2
(2134) p: 3
(2134) p: 4
(2134) p
```

이렇게 p라는 포인터가 0x00200000의 Memory 공간을 가리키는 값을 가지고, 이 공간의 값을 1씩 증가시킨다.

그런데 앞에서 만든 이 mem.c라는 프로그램을 동시에 2개를  실행을 한다면?

```html
prompt> ./mem &; ./mem &
[1] 24113
[2] 24114
(24113) memory address of p: 00200000
(24114) memory address of p: 00200000
(24113) p: 1
(24114) p: 1
(24114) p: 2
(24113) p: 2
(24113) p: 3
(24114) p: 3
...
```

실행을 해보면, (24113)와 (24114) 두 프로세서 모두 0x00200000의 Memory 공간을 가리키는 값을 가지고, 2개의 프로그램이 동시에 실행이 되는것 처럼 보이는 것을 알 수 있다. 

다만 만약 동시에 실행이 된다면 p의 값이 1씩 증가할때, (24113) p: 1 ➜ (24114) p: 2가 되어야 한다((24113)와 (24114) 두 프로세서 모두 0x00200000의 Memory 공간을 가리키므로). 그런데  마치 (24113) 와 (24114) 둘이 다른 공간을 가리키는 것처럼, 마치 서로 독립적인 Memory를 가지고 있는 것 처럼 작동된다.

이것이 바로 Virtualization 이다. OS에서 하나의 프로그램이 하나의 공간을 다 차지하는 '것처럼' 가상화하는 것이다.

즉, 각 프로세스는 각각 개인적인 Virtual Address Space에 access한다. 이는 실제 Physical Address Space 는 아니지만, OS가 Address Space를 Physical Memory와 연결해 주는 것이다.

Virtualizing Memory를 이용하면, 한 프로그램에서 돌리고 있는 Memory Reference는 다른 프로그램의 Memory 프로세서에 영향을 미치지 않는다. Virtualize 되었기 때문이다. Virtualizing Memory은 OS가 해준다. 여기서 Physical memory는 OS의 관리를 받는 Shared Resource인 것이다.

### The problem of Concurrency

Virtualizing을 이용하면 문제가 하나 생긴다. 바로 Concurrency 문제이다.

한 컴퓨터에서 여러가지 프로그램이 run할 경우, 내부적으로 OS는 많은 일을 하게 된다. Multi-Threaded Programs들도 Concurrency 문제가 터지게 된다.

Multi-Threaded Programs의 예제를 하나 살펴보자.

##### A Multi-threaded Program (thread.c)
```html
1 	#include <stdio.h>
2 	#include <stdlib.h>
3 	#include "common.h"
4
5 	volatile int counter = 0;
6 	int loops;
7
8	void *worker(void *arg) {
9 		int i;
10 		for (i = 0; i < loops; i++) {
11 			counter++;
12 		}
13 		return NULL;
14 	}
15
16 	int
17 	main(int argc, char *argv[])
18 	{
19 		if (argc != 2) {
20 			fprintf(stderr, "usage: threads <value>\n");
21 			exit(1);
22 		}
23 		loops = atoi(argv[1]);
24 		pthread_t p1, p2;
25 		printf("Initial value : %d\n", counter);
26
27 		Pthread_create(&p1, NULL, worker, NULL);
28 		Pthread_create(&p2, NULL, worker, NULL);
29 		Pthread_join(p1, NULL);
30 		Pthread_join(p2, NULL);
31 		printf("Final value : %d\n", counter);
32 		return 0;
33 	}
```

이 파일을 compile해서 실행을 해보면, main 함수가 2개의 worker() thread를 만들어 준다는 것을 알 수 있다. 여기서 Thread는 하나의 프로그램 내에서 동시에 독립적으로 실행되는 함수이다.

Thread를 실행하게 되면, 이 프로그램이 가지고 있는 Memory 영역을 공유하면서, 동시에 그 함수 두 개가 실행이 된다.

##### loops: 1000.
```html
prompt> gcc -o thread thread.c -Wall -pthread
prompt> ./thread 1000
Initial value : 0
Final value : 2000
```

loop가 1000번을 하면, worker() thread가 두개 이므로 1000 + 1000 = 2000. 즉, counter가 2000이 찍히는건 너무나 자연스럽다. 

그런데...

##### loops: 10000.
```html
prompt> ./thread 100000
Initial value : 0
Final value : 143012 		// ??????
prompt> ./thread 100000
Initial value : 0
Final value : 137298 		// 이게 뭐얔ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ
```

loop가 10000번을 하면, worker() thread가 두 개 이므로 10000 + 10000 = 20000. 즉, counter가 20000이 찍혀야 한다. 찍혀야 하는데...

실질적으로는 그렇게 나오지 않는다. 실행할때마다 결과가 바뀐다. 이것이 바로 Concurrency에 대한 Issue이다.

### Why is this happening? 

```html
8	void *worker(void *arg) {
9 		int i;
10 		for (i = 0; i < loops; i++) {
11 			counter++;
12 		}
13 		return NULL;
14 	}
```

아까 counter라는 공유하는 변수의 값을 두 Thread가 동시에 업데이트 하는 것인데, 사실 아까 counter++; 라는 코드는 내부적으로는 사실 3개 이상의 Instructions 로 이루어져 있다. 

1. counter 변수에 들어있는 값을 Memory로 불러들어오는 것
2. 이 값을 하나 증가시키는 것
3. 증가한 값을 Memory에 다시 넣어주는 것

이 세 단계로 이루어져 있는데, 두개의 Thread가 돌면서 수행하는 Instructions의 순서가 꼬이기 때문에 Concurrency 문제가 일어난다. 이를 보통 non-atomic 하다고 지칭한다.

### Persistence

Concurrency 말고도 문제가 하나 더 있다. 바로 Persistence 문제이다.

아까 컴퓨터의 중요한 요소는 CPU와 Memory라고 했다. 그런데 Memory는 volatile하다. volatile하다는 의미는 전원이 꺼지면 좆된다는 이야기이다.

그래서 data를 Persistence하게 저장할 필요가 있다. 이런 Persistence적인 문제를 OS 차원에서 support 한다.

하드웨어 입장에서는 hard drive나 SSD 등의 각종 Device들이 있고, 이런 Device들의 data를 어떻게 표현하고 저장을 하느냐가 소프트웨어의 입장이고, 이런 것들을 OS에서 지원을 한다. 

다음의 예제처럼 말이다.

##### Create a file (/tmp/file) that contains the string “hello world”
```html
1 	#include <stdio.h>
2 	#include <unistd.h>
3 	#include <assert.h>
4 	#include <fcntl.h>
5 	#include <sys/types.h>
6
7 	int
8 	main(int argc, char *argv[])
9 	{
10 		int fd = open("/tmp/file", O_WRONLY | O_CREAT | O_TRUNC, S_IRWXU);
11 		assert(fd > -1);
12 		int rc = write(fd, "hello world\n", 13);
13 		assert(rc == 13);
14 		close(fd);
15 		return 0;
16 	}
```

위의 파일을 compile하면, 단순하게 제대로 파일이 하나 생기고 disk에 저장이 된다. 얼핏보면 당연한 과정 같지만, 이 과정에도 OS는 많은 일을 한다.

이 새로 만들어진 파일을 Disk의 어느 위치에다가 저장해야 하는지 부터 시작을 해서, 이 위치에 저장을 하기 위해 어떤식으로 하드웨어에 명령을 주고, 어떤식으로 해당 위치에 넣어줄 것인가 까지 말이다.

File system 또한 많은 일을 한다. 파일을 읽고 쓰는데 어떤 방법이 더 효율적인가(ex. Journaling or copy-on-write) 등등의 최적화기법을 고려한다.

### Design Goals

Virtualiaztion, Concurrency, Persistence의 요소를 고려하여 OS가 지향하는 목표가 있다.

물론 그 중의 하나는 고오급 Abstraction을 만드는 것이다. 즉 여러 프로그램들의 입장에서 봤을때, 하나의 CPU를 '어떻게 하면 나만 쓸수 있는 CPU처럼 보이게 만들것인가'.

그리고 OS가 Abstraction을 만들고나서도, 여전히 빠르고 반응성이 좋아야하는 Performance를 유지해야 한다.

또한, 하나의 CPU를 동시에 여러 프로그램이 공유하는데, 이 프로그램들은 서로 Isolate 되어야 한다. 이는 해킹의 위험성 때문이다. 또한 몇날몇일 실행될 수 있게 하는 Reliability도 높아야 한다. 에너자이저 광고 처럼...

------------- 
## Process

Process에 대한 내용을 살펴보자.

### CPU Virtualization
 
Virtualization에서 큰축은 CPU와 Memory이다. CPU Virtualization 문제의 핵심은 이 질문이다.

```html
실제 하드웨어 에는 하나의 CPU만 있는 상황인데, 어떻게 하면 다수의 프로그램들이 자신이 이 CPU를 통채로 쓸 수 있다고 여기게 하려면 어떤 Abstraction을 설계해야 하는가? 
```

저 질문에 대답할 수 있는 기술이 Time sharing, Context switch, Scheduling Policy 등의 기술이다.

### The Abstraction: a Process

앞에서 언급한 Time sharing, Context switch, Scheduling Policy등을 하기 위해서 중요한 concenpt은 바로 Process이다.

이 Process 라는 것은, 실행되고 있는 프로그램의 instance를 말한다. 이 Process의 핵심 구성요소는 바로 Machine state이다. 

Machine state라는 것은 말그대로... Process가 실행중인 프로그램이라고 하지 않았는가? Process가 열심히 실행중 일때의 그 기계의 상태를 말한다

그 기계의 상태라 하면 그 기계의 Memmory에 저장된 값이나, Register(컴퓨터의 프로세서 내에서 자료를 보관하는 작은 장소)를 말한다.
 
### Process vs Program?

Process와 Program은 뭐가 다를까? 

어떤 instructions나 data 의 집합, 즉 명령어의 집합이 바로 Program이다. 

그러다 우리가 Program을 실행할 시, 컴퓨터의 입장에서는 OS가 Program의 instructions나 data를 CPU나 Memory로 load을 한다. 그럼 CPU는 Program의 instructions들을 실행하고, Memory는 Program의 data들을 받아들인다.

이렇게 loading 되어서 실행되고 있는 Program을 우리가 Process라고 부르는 것이다.
 
### Process API

Process을 만들고 제어하기 위해서, OS에서는 다양한 인터페이스를 제공해준다.

만들고(Create), 죽이고(Destroy), 다른 Process가 변화가 생기기를 기다리고(Wait), 다른 Process를 제어하거나(Miscellaneous Control), Process의 상태를 모니터링하거나(Status)...

이런 형태의 인터페이스를 제공해준다

### Process Creation

이런 인터페이스를 통해서 앞에서의 그 loading 과정이 이루어지게 된다.

Process가 생성될때, Program의 코드가 Memory로 loading이 된다. Program이라는 것은 disk 내에 executable한 format으로 저장되어 있다.  

1. OS 입장에서 제일 처음하는 일들은, executable한 format으로 되어 있는 실행 파일을 불러들어서 code부분을 Memory에 먼저 올려주는 것이다. 이 과정에서 여기 data에 해당하는 Static data들이 있다. Static data들은 전역변수, 혹은 어떤 변수에 like time이 프로그램 시작부터 끝으로 지정되어 있는 그런 변수들이다. 그런 Static data들도 같이 loading을 해준다.  
 
2. 그 다음으로 run-time stack을 만들어 준다. stack이란 Memory space의 어떤 영역인데 local variables, function parameters, return address 등의 변수들이 저장되는 공간이다. main() 함수에 있는 argc와 argv로 부터 첫번째 stack frame을 만들어 준다.  
 
3. Program의 heap이 만들어 진다. heap도 Memory space의 어떤 영역인데, 주로 dynamic allocation에서 사용되는 data들을 위한 공간이다. Program 할때 쓰는 malloc()이나 free() 등의 Memory management 할때 쓰이는 그런 library들을 통해서 dynamic allocation을 할수 있지 않은가? dynamic allocation해서 사용하는 data를 위한 공간인 heap 공간을 만들어 준다.
   
4. 그 다음 OS는 초기화 작업을 해준다. 대표적인 것이 (I/O) setup이다. 이 과정에서 세개의 File descriptors를 열어 준다. 전형적으로 Standard input, output, error의 File descriptor이다.  
 
5. 그 이후 최종적으로 방금 loading한 프로그램을 entry point, 즉 main() 함수 위치 부터 실행을 해준다. 이 과정은 OS가 CPU의 제어권을 새로만든 Process에 넘겨주는 과정이다.  

### Process States

Process가 시작이 된 후에는, Process는 여러가지의 State를 갖는다. Process의 state는 다음의 세가지 state로 표현될 수 있다. 

* Running : 현재 이 Process의 code가 CPU에서 실행되고 있는 state. 좀더 쉽게 그냥 현재 Process가 실행중이면 Running state이다.
 
* Ready : 현재 이 Process가 실행할 준비가 다 되었지만, 실행을 안하고 기다리고 있는 state이다. 이 Process가 실행할 준비가 다 되었음에도 실행을 하지 않는 이유는, 여러가지 이유가 있긴 하지만 보통은 현재 CPU를 다른 Process가 사용하고 있는 경우에 대체로 Ready state이다.
 
* Blocked : 해당 Process가 실행을 하고 그 결과를 기다리고 있는 state이다. 따라서 그 실행하고 있던 뭔가가 끝나기 전까지는, 실행이 될 수 없는 그런 state를 말한다. I/O request를 하는 경우, state가 Blocked가 된다. 예를들어, 파일을 읽고 수정하는 프로그램의 경우 open() 함수를 실행해야 하기 때문에 I/O request를 하고 state가 Blocked 상태가 된다.

##### Process State Transitions

##### Tracing Process State: CPU Only

##### Tracing Process State: CPU and I/O

### Data Structures

Process라는 것도 솔직히 소프트웨어적인 개념이라고 할수 있다. Process를 나타내는 Data Structure가 OS내에 구현이 되어있다. 밑의 사진들은 Xv6의 Data structures 들이다. 

##### Data Structure – The Process List

앞에서 봤던 이런 struct proc이라는 Process의 정보를 담는 Data Structure를 Process Control Block (PCB)라고 한다.

PCB (Process Control Block) 는 Process와 관련된 온갖 정보를 다 담고 있다. CPU registers, PID, PPID, process group, priority, process state, signals, CPU scheduling information, Memory management information, Accounting information, File management information, I/O status information, Credentials 등등...

------------- 
## Process API

Process가 내부적으로는 OS내에 Data Structure로 이루어져 있다는 사실을 우리는 앞에서 알았다. 이런 OS에서 제공하는 API들에 대해서 본격적으로 살펴보자.

### fork()

fork()는 실행 중인 Process의 복사본 Process를 생성하는 함수이다. 일반적으로 실행 중인 Process는 Parent Process, 복사본 Process는 Child Process라고 불린다. 주로 실행 중에 별도의 독립된 작업이 필요한 경우 fork()로 복사된 Child Process가 수행하도록 만든다

### wait()

wait()는 Child Process를 기다릴때 사용하는 함수이다.

### exec()

exec()는 fork()로 Child Process 를 만든 후 그 Process를 새로운 독립적인 Process로 만들어주는 역할을 한다. 현재의 Process 이미지를 새로운 Process 이미지로 '덮어씌우는' 것이다. 그러므로 exec()는 기존의 Memory 경로정보를 가진다.

### Separation of fork() and exec() 

fork() 와 exec()가 분리된 이유는, 리눅스를 생각하면 간단하다. 리눅스 OS 입장에서 Shell를 실행해도 결국 Shell을 띄었을때 다른 프로그램을 실행한다. Shell도 하나의 Process이다. 즉, 우리가 명령프롬프트에 실행파일을 실행하는 것과 비슷한 이치이다.

------------- 
## Limited Direct Execution

CPU Virtualization의 중요한 Mechanism인 Limited Direct Execution에 대해서 알아보자. 

효율적인 CPU Virtualization를 위해선 어떻게 해야하는가? OS는 동시에 진행되는 것 처럼 '보이는' Process들을 하나의 Physical CPU에서 공유해야 한다. 이전에 언급했던 **time sharing**을 통해서 이러한 CPU Virtualization를 달성할 수 있다.

허나 '추가적인 시스템의 overhead없이 어떻게 Virtualization를 달성할 것인가?' 에 대한 Performance issue와,  'CPU에 대한 control을 점유하고 있는 동안에 어떻게하면 Process를 효율적으로 run할 것인가?'에 대한 Control issue가 있다. 

이 두가지 Issue를 달성하기 위한 방법으로 **Limited Direct Execution**가 있다. 

### Direct Execution

Limited Direct Execution에 대해서 이야기 하기전에 Direct Execution에 대해서 알아보자. Direct Execution은 프로그램을 CPU에서 직접적으로 실행하는 것을 의미한다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

위 그림과 같이 진행하는 것이 바로 Direct Execution이라고 할 수 있다. 그런데 위와 같이 limit없이 프로그램을 실행할 시, OS는 제어할 수 없고 단지 library같은 역할을 하게 된다. 

그래서 Direct Execution에 따라 프로그램을 실행하면 우리가 원하는 대로의 CPU Virtualization을 할 수 없는 문제들이 있다.

대체로 어떤 **문제**들이 있냐면... 

만약 하나의 프로그램이 임의의 포인터로 Memory에 접근을 해서 값을 바꾸는 경우 OS가 이를 어떻게 처리할 것인가?에 대한 **Restricted Operation** 문제가 있고, 또한 무한루프가 돌고있는 프로그램이 있을 때 어떻게 다시 CPU에서 control을 가져올 것인가? 에 대한 **Switching Between Processes** 문제도 있다.

이런 문제들을 위한 해결책이 바로 Limited Direct Execution인 것이다.

### Problem 1: Restricted Operation

Direct Execution은 CPU에서 바로 실행되어 속도가 빠르다는 장점이 있지만, 만약 disk에 파일을 I/O한다거나, CPU 또는 Memory에 대한 access을 갖는등의 Restricted Operation이 필요하다면 어떤 문제가 일어나는가?

뭐, 모든 권한을 다 줄 수도 있겠지만... 컴퓨터 내의 Disk, Memory들에 대한 모든 권한이 있다면, 컴퓨터 시스템을 망가트릴 수도 있을 것이다. 

그렇기에 나온 해결책이 **protected control transfer**를 활용하는 것이다. **protected control transfer**라는 것을 활용하여 privileged operation, 즉 일종의 '특권 모드' 이라는 개념을 만들어서 mode를 **User mode** 와 **Kernel mode**라는 두가지 mode로 나누는 것이다.

**User mode**로 돌아가는 프로그램은 하드웨어에 대한 제한적인 권한을 갖고, **Kernel mode**로 동작하면 모든 권한을 다 가질 수 있도록 하는 것이다.

### System Call

허나 만약 User mode인 상태에서 privileged operation을 원한다면? 이를 위한 해결책이 바로 **System Call**이다

System Call을 통해 File System에 access, Process의 생성과 파괴, 다른 Process와의 통신, Memory allocating등의 제한된 작업을 수행할 수 있는 것이다.

System Call을 호출할 때 프로그램을 특정한 **trap 명령**을 수행한다.

이 trap 명령은 User mode에서 Kernel mode로의 변경을 하게 해준다. 그 후 제한되었던 operation들을 수행한 후 특정한 **return-from-trap** 명령을 수행해서 다시 Kernel mode에서 User mode로 다시 되돌아오게 된다.

##### Limited Direction Execution Protocol

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

그런데 위 그림과 같이, 하드웨어에서는 **trap 명령** 수행 후 **return-from-trap**할 때 다시 돌아와야할 Memory Address가 필요하기 때문에 좀 더 주의가 필요하다.

예컨데 x86의 경우, Kernel stack에 program counter 및 flag등 여러가지의 register를 push한 후 명령을 수행할 때마다 pop을 해서 최종적으로는 **return-from-trap**을 수행해서 다시 User Program으로 돌아올 수 있도록 한다.

그렇다면 trap 명령이 어떻게 OS안에서 어떤 명령을 수행해야하는지 알수 있는 것인가?

이를 위해서 trap table이 부팅시에 설정된다. 이 **trap table**안에 trap 명령어들이 적혀있어서 OS가 하드웨어에게 특정한 이벤트가 발생했을 때, 또는 system call이 호출되었을 때 특정한 함수 - 물론 trap() 함수 - 를 실행하도록 할 수 있다.

### Problem 2: Switching Between Processes

Direct Execution의 또다른 문제인 Switching Between Processes에 대해서 알아보자. 이는 Process간 switch를 어떻게 할 것인가에 대한 문제이다.

만약 Process가 CPU에서 동작중이라면, CPU는 한번에 한가지의 동작을 수행하기 때문에 그 말은 즉 OS는 동작하고 있지 않다는 것이다. 

그렇다면 어떻게 OS가 동작중인 Process에서 control을 가져와서 다른 Process에 할당할 수 있을까?

이 문제에 대해서 두가지 방법을 생각해볼수 있다. 하나는 Cooperative Approach와 하나는 Non-Cooperative Approach 이다.

### Cooperative Approach: Wait For System Calls

Cooperative Approach, 즉 협력적인 방법에서는 OS가 시스템의 Process를 신뢰한다. 

너무 오랫동안 동작하는 Process는 control을 포기하는 것으로 OS가 다른 작업을 할 수 있게 한다. 그런데 너무 오랫동안 동작하는 Process가 없는 경우가 있을 수 있기 때문에 Cooperative Approach는 다음의 2가지의 상황을 기다린다.

1. System Call이 호출될 때, 이때 호출되는 System Call은 Yield System Call이라고 불리며 System Calll을 호출해서 현재 Process가 가진 control을 OS에게 양보하는 기능을 한다.
2. illegal한 상황이 발생할 때 OS로 trap을 생성하여 OS가 control을 가질 수 있도록 한다.

그런데 만약 illegal하지 않은 무한루프가 발생하고, System Call도 발생하지 않는다면?

### Non-Cooperative Approach: The OS Takes Control

하드웨어의 도움없이는 OS가 system call의 거부에서 다시 control을 얻어도 할 수 있는 것이 아무것도 없다.

Cooperative Approach에서는 무한루프같은 문제가 발생했을 때 rebooting말고는 답이없다. 그래서 Non-Cooperative Approach, 즉 비협력적인 방법에선 **timer interrupt**라는 것을 사용한다.

매 ms(millisecond)마다 **주기적으로** interrupt를 확인해서 interrupt가 발생하면 **interrupt handler**를 동작시켜 OS가 다시 CPU의 control을 가질 수 있도록 한다.

System Call에서 발생할 수 있는 문제들 때문에 **timer interrupt**도 부팅시에 table을 지니고 있다.

### Saving and Restoring Context

이제 CPU에 대한 control을 다시 System Call을 기다리거나, time interrupt를 통해서 다시 가져올 수 있게되었다.

남은 것은 현재 진행중인 Process를 더 진행할 것인지, 아니면 중단하고 다른 Process를 진행시킬 것인지에 대한 결정을 해야하는데, 이에 대한 결정은 scheduler가 하게된다.

프로세스를 변경하기로 결정했다면 OS는 context switch를 실행하게 된다.

---------------
## CPU Scheduling

low-level mechanism (context switch)은 알게되었으니, 좀더 high-level의 **OS scheduling policies**에 대해서 알아보자.

참고로 Policy란 '무엇을 해야 하는가' 에 해당하는 것이고, Mechanism이란 '결과물을 얻기위해 수행하는 일련의 기술, Process'에 해당하는 것이다.

CPU Scheduling이란 실행가능한 Process가 주어질 경우, 다음에 무슨 Process를 실행해야 하는것에 대한 Policy이다.

### Workload Assumption

**Workload** 는 실행중인 Process에 대한 가정이다. 아래의 가정들을 할 것이다.

1. 각각의 Process는 같은 시간동안 동작한다.
2. 모든 Process는 같은 시간에 시스템에 도착한다. (시스템에 도달하는데 걸리는 시간이 모두 0이다)
3. Process가 한번 시작하면 각 Process는 완료될 때 까지 동작한다.
4. 모든 Process는 CPU만 사용한다.
5. 각 Process의 run-time을 알고있다

### Scheduling Metrics

Workload에 대한 가정 이외에도 **scheduling metric**을 이용해서 scheduling policies를 비교할 수 있다.

T<sub>turnaround time</sub> = T<sub>completion time</sub> - T<sub>arrival time</sub>

여러가지 metric이 있겠지만 **turnaround time**(프로세스 완료까지 걸리는 시간)만을 사용할 것이다.

### FIFO

FIFO는 First In First Out의 약자로써, 단순해서 이해가 쉬운 Policy이다. 먼저 도착하면 먼저 실행된다는 개념이다.

위와같은 상황에서 평균 turnaround time은 20초다.

하지만 위와같은 상황에서는 평균 turnaround time은 110초로 상당히 길다. B, C는 실행 시간은 짧지만 대기시간이 너무 길다는 단점이 있다.

### Shortest Job First

Shortest Job First은 이름 그대로 실행시간이 짧은 Process부터 먼저 실행하겠다는 것이다.

우리의 가정들로 봤을 때 시스템에 모두 동시에 Process가 안착하고, 실행시간도 알고있으므로 최적의 scheduling policy이다.

하지만 실제는 이렇지 않으므로 이상적인 이야기에 불과하다.

실제로 A가 0초에 시스템에 도착해서 실행되고, B,C는 시스템에 도착하기까지 10초가 걸린다면 실제 실행결과는 위와같게된다.

### Shortest Time-To-Completeion First

이 방법은 Process를 실행할 때 **preempt(선점)** 하는 방식으로 진행된다. 

위에서 한 '가정 3. Process가 한번 시작하면 각 Process는 완료될 때 까지 동작한다'를 조금 변경하여 Process가 끝까지 진행되는 것이 아니라 앞서 배운 timer interrupt처럼 동작되는 것이다.

위의 그림처럼 A라는 Process를 선점하고 새로운 B, C Process가 시스템에 도착했을 때 종료되는 시간이 더 짧으면 A를 멈추고 B, C 즉, 더 짧게 걸리는 Process 먼저 실행하는 것이다.

### Response Time

과거의 일괄처리 시스템(batch computing system)에서는 STCF가 적합했다. 하지만 Time-shared machine이 도입되면서 상황이 바뀌었다.

이제 User는 터미널을 통해서 컴퓨터 시스템과 상호작용하게되었기 때문에 **response time**이라는 metric이 새롭게 필요해졌다.

T<sub>response</sub> = T<sub>firstrun</sub> - T<sub>arrival</sub>

response time은 **Process가 시스템에 도달하는데 걸리는 시간**이다.

터미널을 열고, 명령어를 입력하고 10초 뒤에나 시스템으로부터 response가 온다면 생각만해도 끔찍하다..

따라서 response time에 민감한 scheduler가 필요해졌다.

### Round Robin (RR) Scheduling

Round Robin은 **Process를 잘게 쪼개서 실행한다(time slice, scheduling quantum)**. A,B,C라는 Process가 있고, 이것들을 5초동안 진행된다고 생각해보자.

RR은 1초단위로 time slicing해서 평균 response time은 1이지만, SJF인 경우 평균 response time은 5가된다.

RR에서는 time slicing을 하기 때문에 **몇번이나 time slincing을 하는지**가 매우 중요하다.

time slice를 **많이 할 수록 response time에 대한 performance가 좋아지**지만,

너무 많다면 **모든 resorce의 performance가 context swtiching에 집중되는 문제**가 있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

turnaround time을 생각하면 RR은 딱히 좋지않다.

위의 그림에서 볼 수 있듯이 평균 turnaround time은 무려 14초이다.

일반적으로 time slicing을 통해서 CPU을 fair하게 나누는 policy들은 turnaround time을 생각했을 땐 성능이 좋지않다.

이처럼 turnaround time과 response time은 **trade-off** 관계에 있다.

### Incorporating I/O

모든 프로그램은 I/O를 수행할 수 있다.

프로그램이 I/O request를 수행하면 CPU를 사용하지 않는 **block**상태에 있기 때문에 schedler가 그동안 다른 Process를 CPU에 할당할 필요가 있다.

그 후 I/O가 끝나면 다시 scheduler가 block상태에서 ready상태로 Process를 바꿔주어야 한다.

예를들어 50ms동안 실행되는 Process A, B가 있다. A는 10ms 동안 I/O request를 수행하고 B는 I/O없이 실행된다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

A를 실행할 때 I/O를 독립적으로 처리하고, 그 사이에 B를 선점하여 실행시키는 Overlap방식을 활용해서 효율적으로 Process를 운용할 수 있다.

## MLFQ (Multi-Level Feedback Queue)

그런데 아까 우리가 가장 처음에 한 가정 중 가장 말도 안되는 가정이 있다. 바로 '가정 5. 각 Process의 run-time을 알고있다'이다.

그렇다면 이런 가정없이 어떤 Policy를 어떻게 써야할까...? 이 Issue를 해결하기 위한 MLFQ(Multi-Level Feedback Queue)에 대해 알아보자.

MLFQ으로 해결하고자 하는 문제는 2개이다.

1. turnaround time의 최적화 -> 하지만 우리는 프로그램이 얼마동안 실행될지 알 수 없다.
2. response time의 최소화 -> response time을 최소화할 수 있는 Round Robin 같은 경우 turnaround time은 최악이다.

### Basic Rule

MLFQ는 priority를 갖는 여러 개의 queue를 갖고있다. 그리고 특정한 시간에 어떤 하나의 queue에는 실행 준비가 완료된 Process가 있다.

그래서 MLFQ는 priority를 고려하여, 그 시간에 어떤 Process를 실행해야 하는지를 결정할 수 있다.

같은 priority를 갖는 Process가 동시에 큐에 존재할 수 있기 때문에 이 경우에는 Round Robin 방법을 통해서 Process를 실행한다.

MLFQ sheduling의 핵심은 priority를 어떻게 매기는가에 달려있다. MLFQ는 Observed behavior에 기반하여 priority를 매긴다.

예를들어 키보드 입력을 기다리느라 반복적으로 CPU 에 대한 control을 양보하는 Process는 priority가 높고, 오랫동안 CPU 이용률이 높은 Process는 priority가 낮다. 이러한 방식이 대화형 Process가 동작하는 방식이다. 

###  How to Change Priority 

우리는 CPU control을 자주 양보하는 short-running Process와 CPU control을 오랫동안 갖고있는 longer-running Process 모두를 다뤄야 한다.
아래는 priority 적용 알고리즘의 규칙이다.

1. Process가 시스템에 도착하면 가장 높은 priority를 부여한다.
2. Process가 실행되는 동안 모든 작업에 대해 time slice가 이루어진다면 priority를 하나 낮춘다.
3. time slice가 끝나기 전에 CPU control을 양도한다면 같은 priority를 유지한다.

##### A Single Long-Running Job

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

위의 그림에서 볼 수 있듯이 하나의 Long-Running Process가 있을 경우 처음에 Q2에 위치하고 time slice를 한 이후에 priority를 하나씩 내린다.

##### Along Came A Short Job

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

검은색인 A는 long-running process, 회색인 B는 short-running process이다.

A는 실행이후 Q2, Q1을 거쳐 가장 낮은 우선순위인 Q0에서 실행되고 있고, t=100일 때 B가 최상위 우선순위에 도착해서 실행된다.

이 알고리즘에서 우리가 알아야할 것은 처음에 시스템에 들어오는 Process가 short-running process인지 long-running process인지 알 수 없기 때문에, short-running process라고 가정하고 높은 priority를 부여하는 것이다.

만약 실제로 short-running process라면 실행되고 빠르게 종료될 것이고 아니라면 time slice를 통해서 queue의 아래로 점점 내려갈 것이다. 

그래서 MLFQ가 SJF로 근사될 수 있게된다.

### Problem With Our Current MLFQ

이제 기본적인 MLFQ에 대해서는 알게되었지만, 현재 MLFQ에는 큰 문제가 있다.

1. Starvation에 관한 문제이다. 너무 많은 interative한 작업이 계속된다면 long-running process는 절대 CPU control을 가질 수 없다.

2. Gaming the scheduler에 대한 문제이다. 똑똑한 프로그래머는 time slicing이 끝나기 전에 I/O를 요청해서 계속해서 프로세스가 우선순위의 상단에 위치하게 할 수 있다. (rule 3을 악용하는 경우이다.)

##### Priority Boost

우선 첫번째로 Starvation에 대한 문제를 어떻게 해결하면 좋을까? 그 문제는 Priority Boost라고 하는 방법으로 해결할 수 있다.

Priority Boost는 주기적인 시간마다 모든 process의 우선순위를 최상단으로 높여주는 방법이다.

##### Better Accounting

그 다음으로 Gaming the scheduler에 대한 문제는 어덯게 해결하면 좋을지에 대해서 생각해보자. 이는 Better Accounting이라고 부르는 방법으로 해결할 수 있다.

process가 해당 queue에서 할당된 시간을 다 활용했다면 강제로 priority를 낮춰주는 것이다.

### Tuning MLFQ And Other Issues

몇가지 MLFQ에 대한 질문들이 남아있다.

1. sheduler의 parameter는 어떻게 할 것인가?
2. 몇개의 queue가 필요한가?
3. queue당 time slice는 몇번을 해야하는가?
4. priority boost는 얼마나 자주 일어나야 하는가?

무엇하나 쉬운 질문이 없다.

3에 대한 예를 들면 여러가지 queue에서는 여러가지 time slice length가 활용된다.

priority가 높은 queue에서는 interative한 작업이 주로 이루어지므로 short time slice를 하고, priority가 낮은 queue에서는 long-running process가 주로 동작하므로 long time slice가 적합하다.

운영체제마다 어떠한 규칙을 적용시킬 것인가에 대한 내용이 모두 다르다.


## Address Translation

CPU를 가상화 하기위해서는 Limited Direct Execution을 활용했다.

Memory 가상화를 제공할 때도 효율성과 통제권(Efficiency and Control)을 얻기위해서 비슷한 방법이 필요하다.

효율성을 위해서는 분명히 하드웨어가 뒷받침되어야 하고, 처음에는 register 정도로 간단하지만 필요한게 더 많아지다보면 점점 complex해지는 문제가 있다.

통제권을 위해서는 프로그램이 아무 Memory에 접근하지 못하도록 막을 필요가 있다. 따라서 역시 하드웨어가 뒷받침 되어야 한다.

마지막으로 Flexibility를 위해서 Memory 가상화 시스템이 필요하다.

왜냐하면 특히 우리는 프로그램이 물리적 메모리의 어디에 있건, address space에서 동작하길 원하기 때문이다.

이를 위해서 LDE와 같은 hardware-based address transition(address transition)이라고 불리는 방법을 사용해 볼 것이다.

address transition을 통해 하드웨어는 각각의 메모리 접근(명령 저장하기, 불러오기..)을 virtual address에서 실제 physical address로 변환한다. 그래서 모든 프로그램으로의 Memory 참조는 사실 하드웨어가 프로그램의 Memory 참조를 실제 물리적 메모리로 redirect한, address transition의 결과이다.

물론 하드웨어만으로는 Memory를 효율적으로 활용하기 위한 낮은 수준의 mechanisim만 제공할 뿐임으로 Memory 가상화를 수행할 순 없다. 따라서 OS가 적절한 때에 하드웨어를 호출하여 적절한 transition이 발생하도록 해야한다. 따라서 이를 위해 어떤 Memory가 비어있고, 어떤 Memory는 사용중인지를 추적하기 위한 Memory 관리가 필수적이다.

Address Translation을 위한 다음의 세가지 가정이 있다

1. address space는 physical memory의 연속적인 공간에 위치한다.
2. address space는 너무 크지 않다.
3. 모든 address space의 크기는 같다.

### Example: Address Translation

address transition를 수행하기 위해 무엇을 해야하는지, 그리고 왜 이러한 mechanism이 필요한지를 알기위한 예제를 보자.

아래와 같은 코드가 있을 때

##### C - Language code

```html
void func()
	int x;
	...
	x = x + 3; // this is the line of code we are interested in
```

컴파일러가 이 코드를 아래와 같이 바꾼다.

##### Assembly

```html
128 : movl 0x0(%ebx), %eax ; load 0+ebx into eax
132 : addl $0x03, %eax ; add 3 to eax register
135 : movl %eax, 0x0(%ebx) ; store eax back to mem
```

x의 주소는 ebx에 존재하고, eax에 3을 더하고, eax에 있던 값을 메모리로 옮긴다

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

이 코드를 address space에서 살펴보면 위와 같다. 코드는 주소 128, 코드섹션에 있고, x는 3000, stack영역에 있다. 

그리고 아래와 같은 메모리 엑세스를 수행한다.


• 주소 128에 있는 명령을 가져온다.
• 명령을 수행한다. (load from address 15 KB)
• 주소 132의 명령을 가져온다.
• 명령을 수행한다. (no memory reference)
• 주소 135의 명령을 수행한다.
• 명령을 수행한다. (store to address 15 KB)

프로그램의 관점에서 해당 프로그램의 address space는 0에서 시작해서 16KB의 크기를 갖고, 모든 메모리참조는 이 범위내에서 이루어진다. 그러나 OS는 메모리 가상화를 위해 이 address space에서의 참조를 실제 physical memory로 전달해주어야 한다.

그렇다면 어떻게 Process에 transparent하게 memory에서 이 Process를 재배치 할 것인가?
또한 어딘가에 있는 실제 physical memory가 0에서 시작하는 가상의 address space라는 환상을 어떻게 제공할 것인가?

### Dynamic(hardware-based) relocation

1950년대 time-sharing 기계에서 소개된 base-and-bound, dynamic relocation라는 기술이다.

이를 위해서 CPU에 있는 base register, bound(limit)register라는 2가지 하드웨어가 필요하다. 

base-and-bound를 통해서 우리는 물리적 Memory가 어디에 있건 Process가 자신의 address space에 있는것 처럼 만들 수 있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

프로그램은 자신이 0번 주소에 위치한 것 처럼 작성되고, 컴파일 된다. 그리고 프로그램이 실행될 때 OS는 물리적 메모리의 어떤 위치에 프로그램을 올리고, base-register에 해당 주소값을 할당해야 한다.

위의 그림에서 보면 OS는 물리적 메모리의 32KB에 프로그램을 올리고, base-register에 이 주소값을 할당한다.

따라서 메모리 참조가 발생할 때 이는 이렇게 해석될 수 있다.

```html
physical address = virtual address + base(register value)
```

program counter(PC)가 128에 설정되어있고, 

OS는 프로그램이 위치하는 주소인 32KB(32768)를 base register로 만들고 해당 base register에 명령의 주소값(128)을 더해주어 물리적 메모리의 주소(32896)를 얻는다. 

그 다음 하드웨어가 명령을 가져오고, 프로세서가 명령을 수행한다.

```html
128: movl 0x0(%ebx), %eax
```

그 후 프로세서가 가상주소에서 15KB만큼 로드를 발행시킨다. 따라서 실제 물리적 메모리에서는 32KB + 15KB = 47KB까지의 메모리가 활용된다.

이러한 address relocation은 runtime시에 발생하기 때문에 프로그램이 실행중이더라도 수행될 수 있고 이러한 이유 때문에 dynamic relocation이라고 부른다.

그렇다면 base-and-bound에서 base의 역할은 알았는데 bound(limit)의 역할은 무엇일까?

bound(limit) register는 protection을 위한 기능을 한다.

프로세서는 항상 bound 내부에서 메모리 참조가 이루어져야 하고, 이 예시에서는 bound가 16KB로 제한돼있기 때문에 이 bound보다 작거나, 큰 주소를 참조하려 할 경우에는 exception을 발생시키고 프로그램을 종료시킨다.

따라서 bound register는 2가지 기능을 한다고 할 수 있다.

1. address space의 크기를 나타낸다.
2. physical memory에서 address space의 끝을 나타낸다.

그리고 base, bound register는 CPU에 쌍으로 존재하는 하드웨어라는 점을 명심해야한다.

```html
ASIDE : Software-base relocation

hardware-base relocation이 도입되기 이전엔 software-base relocation이 사용되었다. 
static-relocation이라고도 하며, loader라고 불리는 소프트웨어가 실행되려고 하는 프로그램을 가져와서 실제 물리적 메모리의 적절한 시작위치에 메모리를 재배치 시킨다.

예를들어 명령이 1000번 주소에 있고 address space가 3000에서 시작한다면 loader는 프로그램을 0이 아닌 3000의 위치로 옮긴다. 따라서 명령행은 4000번 주소에 위치한다.
이러한 static-relocation은 다음과 같은 문제가 있다.

1. protection을 제공하지 못함
2. 한번 relocation이 이루어진 후 또다른 위치로 relocation을 수행하기 어렵다고 한다.
```

### Operating System Issue

Memory 가상화를 달성하기 위해서 OS와 hardware가 결합되어야 한다.

OS는 새로운 Process가 실행되면 free list라고하는 자료구조를 통해 어떤 Memory 공간이 비어있고, 어떤 Memory 공간이 사용중인지를 파악한다. 

그래서 비어있는 Memory 공간에 새로운 Process를 할당하고 사용중으로 변경시킨다. 

물론 Process마다 사용하는 address space의 크기가 다를것이고, 실행되는 기간도 다르겠지만 이러한 문제점들은 나중에 알아보도록하자.

위의 그림에서 볼 수 있듯이 OS는 물리적 Memory의 가장 처음부터 실행되며 2개의 free space가 존재한다. 따라서 free list에는 2개의 free list가 존재한다. 그리고 프로그램이 문제를 일으켜서 OS가 강제로 종료하게되는 경우 해당 Memory를 다시 free list에 추가 해 두어야 한다.

그리고 CPU에는 1쌍의 base-and-bound register만 있기 때문에 context switch마다 OS는 각각의 프로세스의 base, bound register의 값을 process structure 또는 Process Control Block(PCB)라고 불리는 자료구조에 저장하고, 불러올 수 있어야 한다.

프로세스의 address space를 옮기기 위해서 OS는

1. 프로세스를 deschedule한다.
2. 현재의 address space를 옮길 address space로 복사한다.
3. base register를 새로운 address space에 업데이트한다.

그리고 OS는 exception handler를 제공해야 한다.

*****
## Segmentation

위 그림에서 보면 알 수 있듯이 address space를 구성할 때 실제 물리적 메모리에는 free space가 있기 때문에, base and bound 방법은 우리가 생각하는 것 만큼 유용하지 않을 수 있다.

### Generalize Base and Bound

이러한 문제를 해결하기 위해 segmentation이라는 방법이 나왔다.

이 개념은 쉽게 말해 CPU에만 한 쌍으로 존재하는 base and bound register를 address apce의 논리적인 segment마다 갖고 있는것을 말한다.

segment란 address space에서의 연속적인 부분을 뜻하는데, 우리는 이 부분들이 code, stack, heap의 3개의 논리적 segment를 알고 있다.

각각의 segment를 physical Memory의 서로 다른 부분에 독립적으로 배치하여 사용되지 않는 virtual address space가 생기는 것을 막을 수 있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

위 그림에서 알 수 있듯이 실제 physical Memory의 서로 다른 영역에 어떤 한 Process의 stack, code, heap segment가 독립적으로 존재하고, 

또 다른 Process의 stack, code, heap이 사용되고 있지 않은 not in use space에 위치한다면, 사용되지 않는 virtual address space가 생기는 것을 최대한 막을 수 있다.

따라서 각 segment마다 base and bound register가 존재하면 아래와 같은 모습이 된다.

### Which segment Are We Referring to?

transition시에 하드웨어는 segment register를 사용한다.

그렇다면 어떻게 segment의 시작위치와, address를 아는 것일까?

explicit approach라 불리는 방법인데, virtual address의 상위 몇 비트를 기반으로 address space를 segment로 분할하는 기법이다.

우리는 stack, heap, code의 3가지 segment가 있기 때문에 2개의 비트가 필요하다.

만약 14비트의 virtual address에서 2비트를 segment로 잡으면 virtual address는 다음과 같아진다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

그래서 만약 상위 2개의 비트가 00이면 code영역으로 생각하고, 01이면 heap영역으로 생각하면 아래와 같은 그림이 된다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

따라서 상위 2개의 비트는 segment를 판별하는데 사용하고, 하위 12개의 bit는 offset으로 사용한다. 

base register에 offset을 더함으로써 실제 물리적 메모리에서의 위치를 알 수 있다. 

(base register에 virtual address를 더하는 것이 아니라는 점에 유의하자!)

### What about Stack?

stack은 위의 그림에서 28KB에 위치해있고, 더 작은 주소값으로 즉 0KB 방향으로 크기가 증가한다. 28KB -> 16KB -> 14KB....로 변한다. 

그리고 추가적으로 base and bound register외에도 어떤 방향으로 segment가 증가하는지를 알기위한 하드웨어가 필요하다. 예를들어 비트가 1로 설정되어있으면 positive방향으로 0이라면 negative방향으로 segment가 증가한다.

예를들어 virtual address 15KB 실제로는 physical address 27KB에 접근하려한다. 2진수로는 11 1100 0000 0000(hex 0x3C00)이다. 하드웨어는 상위 2개 비트를 사용하여 segment를 결정한다. 따라서 남은 offset은 3KB이다. 올바른 negative offset을 얻기위해서 3KB에서 최대 offset의 크기인 4KB를 빼야한다. 

base register인 28KB에서 negative offset인 -1KB를 더해서 물리적 메모리인 27KB를 알 수 있다. bound check는 negative offset의 절대값이 segment의 현재 크기보다 작거나 같은지를 확인하여 파악할 수 있다 (이 경우 2KB).


### Support for Sharing

메모리를 절약하기 위해서 특정한 메모리 segment를 공유하는것이 효과적임을 알게되었다. 특히 code sharing은 여전히 유용하다.

sharing을 위해서 protection bits의 형태로 하드웨어의 도움이 필요하다. 

기본적으로 프로그램이 segment를 읽거나 쓸 수 있는지 또는 segment내에 있는 코드를 실행할 수 있는지의 여부를 나타내는 segment당 몇개의 비트를 추가한다. 

code segment를 읽기전용으로 설정하므로써 multi-process에서 독립성을 훼손하지 않으면서 코드를 공유하는 것이 가능하고, 여전히 프로세스들은 자신만의 private 메모리를 소유하고있다고 생각한다.

### Fine-grained vs Coarse-grained Segmentation

지금까지 살펴본 내용은 시스템에서 고작 몇개의 segment(code, stack, heap)만을 알아보았다. 

이런 비교적 거대한 segment들을 I'm coarse-grained segmentation이라고 부른다.
반면에 초기의 시스템에는 flexible함이 필요했기 때문에 크기가 더 작고 개수가 더 많은 fine-grained segmentation이 필요했다.

많은 segment들이 더 많은 하드웨어의 지원과 메모리에 저장된 segment table이 필요하게 되었다. segment table을 활용함으로써 시스템은 좀 더 flexible한 방식으로 많은 개수의 segment를 만들어서 활용할 수 있게되었다.

### OS Support

이제 segmentation이 어떻게 동작하는지를 알게되었다. 하지만 segmentation은 OS에게 몇가지 문제를 야기한다.

1. context switch시에는 어떻게 할 것인가?

이를 위해서 각각의 프로세스가 가지고 있는 virtual address의 base and bound register를 저장했다가 프로세스 재시작 전에 다시 불러와야 한다는 점을 알 수 있을 것이다.

2. segment의 크기가 커지거나, 줄어들 때 OS는 어떤 관련이 있는가?

예를들어 현재 heap segment의 크기만으로 malloc()을 감당할 수 있는 경우에는 할당을하면 되지만 이 크기를 넘어서는 새로운 메모리를 할당해야할 경우에는 sbrk()라는 시스템 콜을 해서 heap segment의 크기를 증가시킨다. 그래서 변화된 크기만큼을 다시 register에 등록하고 메모리 할당을 성공할 수 있다. 하지만 만약 물리적인 메모리 자체가 모자르다면 OS는 메모리할당을 거부할 수도 있다는 것을 명심히자.

3. 물리적 메모리의 free space를 어떻게 관리 할 것인가?

일반적으로 프로세스마다 segment가 생길 것이고 이 크기는 제각각일 것이다. 따라서 물리적 메모리의 중간 중간에는 free space의 구멍이 뻥뻥 뚫려있을 것이고 이는 새로운 segment의 할당을 어렵게 만들 것이다. 이러한 문제를 external-fragmentation라고 부른다.

따라서 segment들을 재조정하여 물리적 메모리를 compact하게 사용함으로써 문제를 해결할 수 있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

하지만 segment들을 재조정하는 방식은 매우 무거운 작업이다. 예를들어 재조정이 끝난 이후에 중간에 있는 프로세스의 heap segment가 증가되야 한다면 또 다시 추가적인 재조정이 일어나야만 한다.

따라서 좀 더 간단한 방법은 할당에 필요한 큰 메모리 공간을 유지하려는 free-list를 관리하는 것이다. 이 외에도 여러가지 알고리즘을 통해서 external-fragmentation을 해결하기 위해 노력하지만 external-fragmentation을 없앨 수는 없고 최소화 할 뿐이다.

*****
## Free-space Management

이번 장에서는 근본적인 메모리 관리, 특히 free-space management에 대한 내용을 중점적으로 살펴볼 것이다.

관리하는 Memory 공간을 고정된 크기(fixed-size unit)로 나누면 쉽다. 고정된 크기의 Memory 리스트를 갖고있다가 요청이 오면 리스트의 첫번째 원소를 리턴하면 된다.

하지만 free-space가 다양한 크기의 메모리 유닛으로 구성되어진다면 관리하는 것이 어려워진다. 이것은 유저레벨에서의 메모리 할당과 해제( malloc(), free() ), virtual memory를 활용하기 위해 OS가 실행하는 segmentation, external-fragmentation등에서 찾아볼 수 있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

위의 그림에서 볼 수 있듯이 free-space는 총 20byte인데 fragmented되어있기 때문에 15byte의 할당이 필요한 요청은 실패하게된다.

### Low-level mechanism

allocator들의 splitting(나누기), coalescing(합치기) 방법과 어떻게하면 빠르고 쉽게 할당한 메모리 크기를 알 수 있는지에 대해서 알아볼 것이다. 

그리고 free-space를 파악할 수 있는 간단한 free list에 대해서 알아볼 것이다.

##### Splitting and Coalescing

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

위의 그림에서 볼 수 있듯이 총 30byte의 heap segment에서 0-9, 20-29byte가 free-space이다.

언급했듯이 10byte 이상의 메모리 할당은 실패할 것이다. 정확하게 10byte의 요청이 오면 쉽게 성공 할 것인데 만약 10byte보다 더 작은 메모리 할당 요청이 온다면 어떻게될까...?

예를들어 free list에 10byte의 free chunk가 존재하는데 1byte의 할당 요청이온다면 이 경우 splitting이라는 방법을 활용하게된다.

그래서 1byte를 할당할 수 있는 free list에 존재하는 2개의 free chunk에서 allocator가 2번째(20-29)를 사용하기로 했다면 2번째 free chunk를 2개의 chunk로 splitting한다.

그래서 첫번째 chunk는 1byte를 할당하고 두번째 chunk는 그대로 free list에 남아있는다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

따라서 free list에서는 20-29byte를 차지하던 2번째 chunk가 21-29byte로 크기가 변하게된다.
이처럼 free chunk보다 요청되는 메모리의 크기가 더 작을 때 splitting이 유용하게 사용된다.

그렇다면 또다른 예시로 만약 사용중이던 10byte의 메모리를 free()한다면 어떻게될까?

그렇다면 단순하게 free list에 반환된 10byte만큼을 아래와같이 추가하면 된다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

만약 10byte씩 3개의 chunk로 나뉜 상태에서 20byte의 할당 요청이 들어온다면 당연히 할당에 실패할 것이다. 이러한 문제를 해결하기위해서 allocator는 3개의 free chunk를 하나의 free chunk로 coalescing한다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>

## Tracking The Size Of Allocated Regions

free()에 해제해야 하는 Memory의 크기가 없다는 것을 알고있으므로, 우리는 해제 할 포인터를 매개변수로 받았을 때 해제되어야 할 크기를 파악하고, 해제된 Memory를 free list에 추가해야함을 알고있다.

이를 위해서 대부분의 allocator들은 약간의 Memory를 더 써서 head block이라는 곳에 추가적인 정보를 저장하고 있다.

예를들어 20byte의 Memory를 할당받았다고 하자, 이때 헤더에는 해제를 위한 포인터주소와, 무결성검사를 제공하기 위한 magic number 및 기타 다른 정보들을 갖고있다.

<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
</div>



We've included everything you need to create engaging posts about your work, and show off your case studies in a beautiful way.

**Obviously,** we’ve styled up *all the basic* text formatting options [available in markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You can create lists:

* Simple bulleted lists
* Like this one
* Are cool

And:

1. Numbered lists
2. Like this other one
3. Are great too

You can also add blockquotes, which are shown at a larger width to help break up the layout and draw attention to key parts of your content:

> “Simple can be harder than complex: You have to work hard to get your thinking clean to make it simple. But it’s worth it in the end because once you get there, you can move mountains.”

The theme also supports markdown tables:

| Item                 | Author        | Supports tables? | Price |
|----------------------|---------------|------------------|-------|
| Duet Jekyll Theme    | Jekyll Themes | Yes              | $49   |
| Index Jekyll Theme   | Jekyll Themes | Yes              | $49   |
| Journal Jekyll Theme | Jekyll Themes | Yes              | $49   |

And footnotes[^1], which link to explanations[^2] at the bottom of the page[^3].

[^1]: Beautiful modern, minimal theme design.
[^2]: Powerful features to show off your work.
[^3]: Maintained and supported by the theme developer.

You can throw in some horizontal rules too:

---

### Image galleries

Here's a really neat custom feature we added – galleries:

<class="gallery" data-columns="3">
	<img src="/images/demo/demo-portrait.jpg">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-square.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

Inspired by the Galleries feature from WordPress, we've made it easy to create grid layouts for your images. Just use a bit of simple HTML in your post to create a masonry grid image layout:

```html
<div class="gallery" data-columns="3">
    <img src="/images/demo/demo-portrait.jpg">
    <img src="/images/demo/demo-landscape.jpg">
    <img src="/images/demo/demo-square.jpg">
    <img src="/images/demo/demo-landscape-2.jpg">
</div>
```

*See what we did there? Code and syntax highlighting is built-in too!*

Change the number inside the 'columns' setting to create different types of gallery for all kinds of purposes. You can even click on each image to seamlessly enlarge it on the page.

---

### Image carousels

Here's another gallery with only one column, which creates a carousel slide-show instead.

A nice little feature: the carousel only advances when it is in view, so your visitors won't scroll down to find it half way through your images.

<div class="gallery" data-columns="1">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

### What about videos?

Videos are an awesome way to show off your work in a more engaging and personal way, and we’ve made sure they work great on our themes. Just paste an embed code from YouTube or Vimeo, and the theme makes sure it displays perfectly:

<iframe src="https://player.vimeo.com/video/19536258?color=ffffff&title=0&byline=0&portrait=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

---

## Pretty cool, huh?

We've packed this theme with powerful features to show off your work. Why not put them to use on your new portfolio?

<a href="https://jekyllthemes.io/theme/index-portfolio-jekyll-theme" class="button button--large">Get This Theme</a>

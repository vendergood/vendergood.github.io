---
title: 'Operating Systems'
subtitle: '운영체제·랩 관련 공부한 내용들'
date: 2021-03-11 00:00:00
featured_image: '/images/under-construction.jpg'
---

![](/images/under-construction.jpg)

Intro
------------- 

### Some History
 
우선 옛날얘기 부터 해보자. 사실 컴퓨터라는 것의 역사가 그리 길지는 않다. 1900년대 중반, 이 시기에 최초의 컴퓨터가 탄생하게 된다. 

최초의 컴퓨터가 어떻게 발전하게 되고, 그리고 그 과정에서 운영체제가 어떤 역할을 하게 되었는지 한번 살펴보자.
 
 
#### ● 1G (1945-55)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
1세대 컴퓨터라 하는 것은 Vacuum Tubes(진공관)와 Plugboard(플러그판)의 조합이었다. 그래서 사진에 보이는 것 처럼, 거대한 기계들의 거대한 진공관들이 박혀있고, 그런것들이 서로 연결해 가면서 계산을 하는 그런 기계였던 것이다. 
 
우리가 흔히 최초의 컴퓨터라고 하는 이 ENIAC 시스템이 이 진공관들로 이루어진 시스템이다. 
 
이 시기에는 OS, 프로그래밍 언어, 어셈블리 언어.. 이런것들이 존재하지 않았다. 그냥 단순한 기계적인 시스템으로 필요한 계산들을 했던 것이다.
 
#### ● 2G (1955-65)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
이 다음 세대는 트랜지스터. 트랜지스터라는 소재에 의해서 그 다음 컴퓨팅 시스템의 시대가 열리게 되는데, 이런 트랜지스터라는 소재료를 활용해서 Mainframe이라는 시스템이 만들어졌다.  Mainframe는 아주 거대한 컴퓨터였고, 다수의 사람들이 공유해서 사용하는 그런 컴퓨터를 일컫는 말이다. 다만 현대와 같은 발전된 형태의 Computing System은 아니었다.

이때는 Batch System이라고 얘기했다. 거대한 컴퓨터는 있지만, 이 거대한 컴퓨터에서 한번의 하나의 프로그램만 작동할 수 있었던 것이다.

이 시기의 OS는 어느 한 순간에 하나의 프로그램을 돌리기만 하면 되었기 때문에, 이 시기의 OS는 Library의 형태에 가까웠다고 한다.
 
우리가 흔히 최초의 컴퓨터라고 하는 이 ENIAC 시스템이 이 진공관들로 이루어진 시스템이다. 
 
이 시기에는 OS, 프로그래밍 언어, 어셈블리 언어.. 이런것들이 존재하지 않았다. 그냥 단순한 기계적인 시스템으로 필요한 계산들을 했던 것이다.

#### ● 3G (1965-80)
 
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

#### ● 4G (1980-)
 
<div class="gallery" data-columns="3">
	<img src="/images/under-construction.jpg">
	<img src="/images/under-construction.jpg">
</div>
 
이 다음 세대는 IC 회로(Integrated Circuit)의 집적도가 급증하게 되어서, LSI(Large Scale Integration) 및 VLSI(Very Large Scale Integration) 등의 회로들이 등장하게 되어 컴퓨터가 소형화되고 성능도 발전하게 되었다. PC(Personal Computer)이 이 시기에 탄생하게 된다.

우리에게 친숙한 현대적인 멀티미디어, 인터넷, 모바일 등등의 GUI(Graphical User Interface)가 이때 발전하게 되었다.

### OS concepts

프로그램이 실행될때, 무슨 일이 일어날까? 프로그램이 시작된다는 것은 다음의 Instructions을 하나하나 연속적으로 실행한다는 것이다.

1. Fetch라는 과정을 통해서, 메모리에서 Instruction을 하나 가져온다.
2. 그 다음, Decoding을 하여 이 Instruction이 과연 어떤 Instruction인지를 해석을 한다.
3. 그리고 나서 Instruction를 Decode하여 해석한 결과에 따라 Instruction을 Execute 한다.
4. 한 Instruction이 끝난 후, 다른 Instruction에 대해 ①~③ 과정을 무한 반복한다.

이런 과정 내에서 OS는 컴퓨터 시스템이 올바르고 효율적으로 작동할 수 있게 도와주는 역할을 한다.

#### Virtualization

Virtualization(가상화) = OS가  Processor, Memory, Disk와 같은 물리적인 자원을 Virtual Form, 즉 가상적인 형태로 변환해서 유저나 어플리케이션들에게 제공하는 것. Virtual Form은 좀더 일반적이고, 유용하고, 더쉽게 쓸수 있는 형태이다.

그렇기에 우리는 OS를 Virtual Machine이라고 부른다.

#### System call

System call은 사용자가 컴퓨터 시스템의 민감한 부분을 건드리지 않고, 그것을 OS보고 대신 제어해달라는 형태의 인터페이스이다. OS는 API등의 인터페이스를 제공을 한다. 

그리고 그 API 인터페이스들은 OS 차원에서 이 시스템을 제어할 수 있는 온갖 일을 한다. (ex. Run programs, Access memory, Access devices)

#### The OS is a resource manager

OS는 CPU, Memory, Disk와 같은 리소스들을 관리해주기 때문에, 다음과 같은 것들을 가능하게 한다.

* 여러 개의 프로그램이 동시에 run하고 싶다 ㅁ CPU를 공유하게 해준다.
* 시스템에서 돌아가는 여러 개의 프로그램들이 Memory에 동시에 access하고 싶다 ➜ Memory를 공유하게 해준다.
* 컴퓨터에 붙어있는 많은 access 기기를 여러 프로그램들이 사용하고 싶다 ➜ Disk를 공유하게 해준다.

#### Virtualizing the CPU

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

#### Virtualizing Memory

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

#### The problem of Concurrency

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

#### Why is this happening? 

```html
8	void *worker(void *arg) {
9 		int i;
10 		for (i = 0; i < loops; i++) {
11 			**counter++;
12 		}
13 		return NULL;
14 	}
```

아까 counter라는 공유하는 변수의 값을 두 스레드가 동시에 업데이트 하는 것인데, 사실 아까 counter++ 라는 코드는 사실 2~3개의 Instructions 로 이루어져 있다. 




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

<div class="gallery" data-columns="3">
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

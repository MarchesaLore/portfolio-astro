---
title: Nardwuar
publishDate: 2022-04-01 00:00:00
img: /assets/work/nardwuar_1.jpg
img_alt: Nardwuar homepage
img2: /assets/work/nardwuar_2.jpg
img2_alt: Nardwuar timeline
description: |
  This is a personal project, just to practice and show my Angular skills
tags:
  - Dev
  - Angular
  - Front-end
---

This is a personal project, just to practice and show my Angular skills.

On a side note, <a href="https://en.wikipedia.org/wiki/Nardwuar" target="_blank">Nardwuar</a> is a Canadian Jourlanist that is very funny and has interviewed many many musicians, his interviews are not only hilarous but have some incredible deep cuts one of my favorite is the one with Questlove he can't quite believe how deep Nardwuar knowledge in music and history is and he can't keep focus on the conversation! highly suggested!

I have created a new Angular project. Added routing so that I can have multiple pages, currently having Welcome and Timeline.

few things about the timeline:

the interviews are just in a json I am loading those interviews in the timeline controller and sorting them by date.

the space between one interview and the next one is a day difference with the method calculatePosition I assign to the interview a position from the top.

youtube video: I have a youtubevideo component, needed or the video would not load due to security issues it is using:

import { DomSanitizer, SafeResourceUrl } from '@angular/platform-browser';

so that I can dinamically load the video in SafeResourceUrl, with this.sanitizer.bypassSecurityTrustResourceUrl(youtubeUrl);

when clicking on the interview on the timeline, the video get loaded in the main section of the container, that is to show the communication between two elements @Output() interviewSelected = new EventEmitter(); and the method onInterviewSelected

<a href="https://github.com/MarchesaLore/nardwuar-timeline/tree/main" target="_blank">Github link to the project</a>
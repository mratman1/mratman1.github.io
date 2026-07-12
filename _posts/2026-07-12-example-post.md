---
title: "Pólya's recurrence theorem"
date: 2026-07-12
categories: maths
---

## Introduction

Recently in my research I ended up using the concept of self-avoiding random walks in order to design obstacles with desired properties. This led me to think about the probabilities of a regular random walk overlapping with itself and reminded me of a quote I read once, attributed to Shizuo Kakutani, "A drunk man will find his way home, but a drunk bird may get lost forever" [2]. This is a reference to something known as the Pólya recurrence theorem [1], which effectively states that random walks (on a lattice) in $1$ and $2$ dimensions will return to their starting location with probability $1$ given enough time. Random walks in dimensions $3$ and higher do not share this property. That's why the extra spatial degree of freedom in the drunk bird's case makes it get lost forever.

I was very curious about the proof of this theorem, and especially about the probability of the $d \geq 3$ dimensional walkers returning to the starting point, as that might have a practical application for my case. Naturally, the probability of returning to the start $p(d) \to 0$ as $d \to \infty$, but I wondered about the scaling of this decay. Turns out there are plenty of resources about this online, so I figured this would be a nice opportunity to test out the blog capabilities of the website and put some of the mathematics in an accessible format for future reference. 

## Definition and Intuition

Before jumping into a proof, let's first formally state the problem and develop some intuition for why $d=3$ should be the transition point. The theorem states 


*The simple random walk on $\mathbf{Z}^d$ is recurrent in dimensions $d=1, 2$ and transient in dimensions $d \geq 3$.* [3]



The intuition I attribute to a nice reddit comment by user aquamongoose. 

## Citations

[1] Pólya's Recurrence Theorem, Shrirang Mare, 2013

[2] Armin Straub, Colloquial catchy statements encoding serious mathematics, URL (version: 2024-06-23): https://mathoverflow.net/q/3562

[3] G. Pólya, Uber eine Aufgabe der Wahrscheinlichkeitsrechnung betreffend die 
Irrfahrt im Strassennetz, Math. Ann. 84 (1921),149-160.




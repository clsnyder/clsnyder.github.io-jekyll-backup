---
title: The Gale-Shapley Algorithm (you've never heard of) and the national residency match program
last_modified_at: 2024-12-04 T09:20:02-05:00   
excerpt_separator: “<!—more—>”
categories:
  - Blog   
tags:  
  - PedSurg 
  - Math  
---



 ### Understanding the Gale-Shapley Algorithm and the National Residency Match Program (NRMP)

The Gale-Shapley algorithm is one of the most famous solutions in game theory and has practical implications that influence thousands of lives every year, particularly in the National Residency Match Program (NRMP). This blog explores the history of the algorithm, explains how it works, and delves into its role in matching medical residents with hospitals, addressing the age-old question: does it favor applicants or institutions?

The History of the Gale-Shapley Algorithm

The Gale-Shapley algorithm, also known as the Stable Marriage Algorithm, was introduced in 1962 by mathematicians David Gale and Lloyd Shapley. It solved the problem of stable matching—ensuring that a group of individuals could be paired in such a way that no two individuals would prefer each other over their assigned partners.

What is Stable Matching?

A matching is “stable” if:
	1.	No individual can improve their outcome by switching to someone else.
	2.	No pair of individuals would both be better off by leaving their assigned matches.

This concept initially applied to pairing individuals (e.g., men and women in the marriage problem). However, its practical applications extend far beyond this, particularly in scenarios like assigning students to schools, organ donation, and the NRMP.

In 2012, Shapley and economist Alvin Roth won the Nobel Prize in Economic Sciences for their work on this and related algorithms, emphasizing its real-world impact.

#### How Does the Gale-Shapley Algorithm Work?

The Gale-Shapley algorithm operates as follows:
	1.	Proposal Phase:
	•	One group (e.g., residents) proposes to members of the other group (e.g., hospitals) in order of their preference.
	•	The receiving group tentatively accepts the proposal if it is the most preferred so far but may reject it later if a better option comes along.
	2.	Rejection and Re-Proposal:
	•	Rejected members of the proposing group move down their list and propose to their next choice.
	3.	Stability:
	•	The process continues until no more proposals can be made, and all participants are matched in a way that no one would benefit from switching.

The National Residency Match Program (NRMP)

The NRMP, established in 1952, is one of the most well-known implementations of the Gale-Shapley algorithm. It matches graduating medical students (or other applicants) with residency programs at hospitals across the United States. Each year, tens of thousands of applicants rank residency programs, and hospitals rank applicants. The NRMP uses a modified version of Gale-Shapley to produce matches.

How the NRMP Works

	1.	Applicant Preferences:
	•	Applicants rank residency programs based on their preferences.
	2.	Program Preferences:
	•	Residency programs rank applicants based on interviews and evaluations.
	3.	The Match:
	•	The algorithm processes these rankings:
	•	Applicants “propose” to their most preferred program.
	•	Programs tentatively accept applicants based on their rankings but may later reject them if higher-ranked applicants propose.
	•	This continues until all matches are stable.
	4.	Results:
	•	The algorithm ensures that no applicant-program pair would prefer each other over their assigned matches.

Does the NRMP Favor Applicants or Programs?

The NRMP’s version of the Gale-Shapley algorithm is applicant-proposing, meaning that applicants make the first “proposals” in the matching process. This favors applicants in the following ways:
	1.	Applicant Preferences:
	•	Applicants are matched to the highest-ranked program that accepts them. They are never removed from a program they prefer unless a more preferred program accepts them.
	2.	Programs Are Passive:
	•	Programs must accept applicants based on their rankings without actively proposing to their most desired candidates.

However, this does not mean programs are disadvantaged. Programs can optimize their rankings based on their preferences, and they benefit from stable matches where there is less risk of applicants reneging on offers.

Illustrative Diagram: Gale-Shapley in Action

**Initial Rankings**

![Rankings](/assets/images/initial_rankings.png)

Applicants	Ranked Programs	Programs	Ranked Applicants
A	[P1, P2, P3]	P1	[A, B, C]
B	[P2, P1, P3]	P2	[B, A, C]
C	[P3, P2, P1]	P3	[C, B, A]

Step 1: Applicants Propose

	•	A proposes to P1.
	•	B proposes to P2.
	•	C proposes to P3.
	•	Programs tentatively accept all proposals.

Step 2: Re-Proposals

	•	If B is rejected by P2 in favor of A, B proposes to P1. If P1 prefers B to its current match, it accepts B and rejects A.

**Final Matching**
![Final](/assets/images/initial_rankings.png)
Applicant	Match
A	P2
B	P1
C	P3

This ensures all matches are stable, and no one would prefer switching.

**Conclusion**

The Gale-Shapley algorithm underpins the NRMP, ensuring fairness and stability in residency matches. Its applicant-proposing nature gives applicants an edge, helping them secure their most preferred program that ranks them highly. For hospitals, the algorithm ensures they are matched with applicants they value, minimizing the risk of disruptions in the matching process.

This elegant balance between competing interests highlights the power of stable matching theory in solving real-world problems. Understanding this process not only demystifies the residency match but also sheds light on the interplay of preferences and fairness in modern algorithms.

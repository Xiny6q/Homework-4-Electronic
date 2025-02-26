Download link :https://programming.engineering/product/homework-4-electronic/

# Homework-4-Electronic
Homework 4 Electronic
Model-Based RL:Grid

Assuming we have four observed episodes for training,

Episode 1:A,south,C,-1;C,south,E,-1;E,exit,x,+10

Episode 2:B,east,C,-1;C,south,D,-1;D,exit,x,-10

Episode 3:B,east,C,-1;C,south,D,-1;D,exit,x,-10

Episode 4:A,south,C,-1;C,south,E,-1;E,exit,x,+10

What model would be learned from the above observed episodes?

T(A; south ; C) =

T(B; east ; C) =

T(C; south ; E) =

T(C; south ; D) =

(Your answer should be 1,0.5,0.25,0.35 for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Direct Evaluation

Consider the situations in problem 1, what are the estimates for the following quantities as obtained by direct evaluation:

Vb (A) =

Vb (B) =

Vb (C) =

Vb (D) =

Vb (E) =

(Your answer should be 1,-1,0,0,5 for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Temporal Di erence Learning


^

V (A)=

^

V (B)=

^

V (C)=

^

V (D)=

^

V (E)=

(Your answers should be 1,-1,0,0,5 for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Model-Free RL:Cycle


A

B

C

Clockwise

-0.93

1.24

0.439

Counterclockwise

-5.178

5

3.14

The agent encounters the following samples,

s

a

s’

r

A

clockwise

C

-4

C

clockwise

D

3

Process the sample given above. Fill in the Q-values after both samples have been accounted for.

Q(A,clockwise)=

Q(B,clockwise)=

Q(C,clockwise)=

Q(A,counterclockwise)=

Q(B,counterclockwise)=

Q(C,counterclockwise)=

(You answer should be 1,-1,0,0,5,6 for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Q-Learning Properties

In general, for Q-Learning to converge to the optimal Q-values…

A. It is necessary that every state-action pair is visited in nitely often.

B. It is necessary that the learning rate (weight given to new samples) is decreased to 0 over time.

C. It is necessary that the discount is less than 0.5.

D. It is necessary that actions get chosen according to arg maxa Q(s; a).

(You answers should be ABCD for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Exploration and Exploitation

For each of the following action-selection methods, indicate which option describes it best.

A: With probability p, select arg maxa Q(s; a). With probability 1-p, select a random action. p = 0.99.

A. Mostly exploration

B. Mostly exploitation

C. Mix of both

B: Select action a with probability

e

Q(s;a)

P (ajs) =

Pa0

e

Q(s;a0 )

where is a temperature parameter that is decreased over time.

A. Mostly exploration

B. Mostly exploitation

C. Mix of both

C: Always select a random action.

A. Mostly exploration

B. Mostly exploitation

C. Mix of both

D: Keep track of a count, Ks;a, for each state-action tuple,(s,a), of the number of times that tuple has

been seen and select arg maxa [Q(s; a) Ks;a].

A. Mostly exploration

B. Mostly exploitation

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

C. Mix of both

Which method(s) would be advisable to use when doing Q-Learning?

(Your answers should be A,B,C,C,ABCD for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Feature-Based Representation: Actions


STOP

RIGHT

LEFT

DOWN

Using the weight vector w = [0.2,-1], which action, of the ones shown above, would the agent take from

state A?

STOP

RIGHT

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

LEFT

DOWN

(Your answer should be A,D for example)

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Feature-Based Representation: Update

Consider the following feature based representation of the Q-function:

Q(s; a) = w1f1(s; a) + w2f2(s; a)

with:

f1(s; a) = 1=(Manhattan distance to nearest dot after having executed action a in state s)

f2(s; a) =(Manhattan distance to nearest ghost after having executed action a in state s) Part 1

Assume w1 = 2, w2 = 5. For the state s shown below, nd the following quantities. Assume that the red and blue ghost are both setting on top of a dot.


Q(s,West)=

Q(s,South)=

Based on this approximate Q-function, which action would be chosen:

A.West

B.South

VE 492 : Electronic #4 (Due June 17th, 2020 at 11:59pm)

Part 2

Assume Pac-Man moves West. This results in the state s0 shown below.


Q(s’,West)=

Q(s’,East)=

What is the sample value (assuming =1)?

Sample = [r + maxa0 Q (s0 ; a0 )] =

Part 3

Now let’s compute the update to the weights. Let = 0:5

di erence = = [r + maxa0 Q (s0 ; a0 )] Q(s; a) =

w1

w1 + ( di erence )f1(s; a) ==

w2

w2 + ( di erence )f2(s; a) ==

(Your answer should be 1,2,A,1,2,3,1,2,3 for example)


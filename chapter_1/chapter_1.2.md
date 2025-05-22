1.2 Applications of Propositional Logic
Introduction
Logic has many important applications to mathematics, computer science, and numerous other
disciplines. Statements in mathematics and the sciences and in natural language often are imprecise
or ambiguous. To make such statements precise, they can be translated into the language
of logic. For example, logic is used in the specification of software and hardware, because these
specifications need to be precise before development begins. Furthermore, propositional logic
and its rules can be used to design computer circuits, to construct computer programs, to verify
the correctness of programs, and to build expert systems. Logic can be used to analyze and
solve many familiar puzzles. Software systems based on the rules of logic have been developed
for constructing some, but not all, types of proofs automatically.We will discuss some of these
applications of propositional logic in this section and in later chapters.
Translating English Sentences
There are many reasons to translate English sentences into expressions involving propositional
variables and logical connectives. In particular, English (and every other human language) is
often ambiguous. Translating sentences into compound statements (and other types of logical
expressions, which we will introduce later in this chapter) removes the ambiguity. Note that
this may involve making a set of reasonable assumptions based on the intended meaning of the
sentence. Moreover, once we have translated sentences from English into logical expressions
we can analyze these logical expressions to determine their truth values, we can manipulate
them, and we can use rules of inference (which are discussed in Section 1.6) to reason about
them.
To illustrate the process of translating an English sentence into a logical expression, consider
Examples 1 and 2.
EXAMPLE 1 How can this English sentence be translated into a logical expression?
“You can access the Internet from campus only if you are a computer science major or you
are not a freshman.”
Solution: There are many ways to translate this sentence into a logical expression. Although it is
possible to represent the sentence by a single propositional variable, such as p, this would not be
useful when analyzing its meaning or reasoning with it. Instead, we will use propositional variables
to represent each sentence part and determine the appropriate logical connectives between
them. In particular, we let a, c, and f represent “You can access the Internet from campus,”
“You are a computer science major,” and “You are a freshman,” respectively. Noting that “only
if” is one way a conditional statement can be expressed, this sentence can be represented as
a → (c ∨¬f ).
▲
EXAMPLE 2 How can this English sentence be translated into a logical expression?
“You cannot ride the roller coaster if you are under 4 feet tall unless you are older than 16
years old.”
Solution: Let q, r, and s represent “You can ride the roller coaster,” “You are under 4 feet tall,”
and “You are older than 16 years old,” respectively. Then the sentence can be translated to
(r ∧¬s)→¬q.
Of course, there are other ways to represent the original sentence as a logical expression,
but the one we have used should meet our needs.
▲
System Specifications
Translating sentences in natural language (such as English) into logical expressions is an essential
part of specifying both hardware and software systems. System and software engineers take
requirements in natural language and produce precise and unambiguous specifications that can
be used as the basis for system development. Example 3 shows how compound propositions
can be used in this process.
EXAMPLE 3 Express the specification “The automated reply cannot be sent when the file system is full”
using logical connectives.
Solution: One way to translate this is to let p denote “The automated reply can be sent” and
q denote “The file system is full.” Then ¬p represents “It is not the case that the automated
reply can be sent,” which can also be expressed as “The automated reply cannot be sent.”
Consequently, our specification can be represented by the conditional statement q →¬p.
▲
System specifications should be consistent, that is, they should not contain conflicting
requirements that could be used to derive a contradiction.When specifications are not consistent,
there would be no way to develop a system that satisfies all specifications.
EXAMPLE 4 Determine whether these system specifications are consistent:
“The diagnostic message is stored in the buffer or it is retransmitted.”
“The diagnostic message is not stored in the buffer.”
“If the diagnostic message is stored in the buffer, then it is retransmitted.”
Solution: To determine whether these specifications are consistent, we first express them using
logical expressions. Let p denote “The diagnostic message is stored in the buffer” and let q
denote “The diagnostic message is retransmitted.” The specifications can then be written as
p ∨ q, ¬p, and p → q. An assignment of truth values that makes all three specifications true
must have p false to make ¬p true. Because we want p ∨ q to be true but p must be false,
q must be true. Because p → q is true when p is false and q is true, we conclude that these
specifications are consistent, because they are all true when p is false and q is true. We could
come to the same conclusion by use of a truth table to examine the four possible assignments
of truth values to p and q.
▲
EXAMPLE 5 Do the system specifications in Example 4 remain consistent if the specification “The diagnostic
message is not retransmitted” is added?
Solution: By the reasoning in Example 4, the three specifications from that example are true
only in the case when p is false and q is true. However, this new specification is ¬q, which is
false when q is true. Consequently, these four specifications are inconsistent.
▲ Boolean Searches
Logical connectives are used extensively in searches of large collections of information, such
as indexes of Web pages. Because these searches employ techniques from propositional logic,
they are called Boolean searches.
In Boolean searches, the connective AND is used to match records that contain both of
two search terms, the connective OR is used to match one or both of two search terms, and the
connective NOT (sometimes written as AND NOT ) is used to exclude a particular search term.
Careful planning of how logical connectives are used is often required when Boolean searches
are used to locate information of potential interest. Example 6 illustrates how Boolean searches
are carried out.
EXAMPLE 6 Web Page Searching MostWeb search engines support Boolean searching techniques, which
usually can help findWeb pages about particular subjects. For instance, using Boolean searching
to find Web pages about universities in New Mexico, we can look for pages matching NEW
AND MEXICO AND UNIVERSITIES. The results of this search will include those pages that
contain the three words NEW, MEXICO, and UNIVERSITIES. This will include all of the
pages of interest, together with others such as a page about new universities in Mexico. (Note
that in Google, and many other search engines, the word “AND” is not needed, although it is
understood, because all search terms are included by default. These search engines also support
the use of quotation marks to search for specific phrases. So, it may be more effective to search
for pages matching “New Mexico” AND UNIVERSITIES.)
Next, to find pages that deal with universities in New Mexico or Arizona, we can search
for pages matching (NEW AND MEXICO OR ARIZONA) AND UNIVERSITIES. (Note: Here
the AND operator takes precedence over the OR operator. Also, in Google, the terms used for
this search would be NEW MEXICO OR ARIZONA.) The results of this search will include
all pages that contain the word UNIVERSITIES and either both the words NEW and MEXICO
or the word ARIZONA. Again, pages besides those of interest will be listed. Finally, to find
Web pages that deal with universities in Mexico (and not New Mexico), we might first look
for pages matching MEXICO AND UNIVERSITIES, but because the results of this search will
include pages about universities in New Mexico, as well as universities in Mexico, it might be
better to search for pages matching (MEXICO AND UNIVERSITIES) NOT NEW. The results
of this search include pages that contain both the words MEXICO and UNIVERSITIES but
do not contain the word NEW. (In Google, and many other search engines, the word “NOT” is
replaced by the symbol “-”. In Google, the terms used for this last search would be MEXICO
UNIVERSITIES -NEW.)
▲
Logic Puzzles
Puzzles that can be solved using logical reasoning are known as logic puzzles. Solving logic
puzzles is an excellent way to practice working with the rules of logic. Also, computer programs
designed to carry out logical reasoning often use well-known logic puzzles to illustrate their
capabilities. Many people enjoy solving logic puzzles, published in periodicals, books, and on
theWeb, as a recreational activity.
We will discuss two logic puzzles here.We begin with a puzzle originally posed by Raymond
Smullyan, a master of logic puzzles, who has published more than a dozen books containing
challenging puzzles that involve logical reasoning. In Section 1.3 we will also discuss the
extremely popular logic puzzle Sudoku.
EXAMPLE 7 In [Sm78] Smullyan posed many puzzles about an island that has two kinds of inhabitants,
knights, who always tell the truth, and their opposites, knaves, who always lie. You encounter
two people A and B. What are A and B if A says “B is a knight” and B says “The two of us are
opposite types?”
Solution: Let p and q be the statements that A is a knight and B is a knight, respectively, so that
¬p and ¬q are the statements that A is a knave and B is a knave, respectively.
We first consider the possibility that A is a knight; this is the statement that p is true. If A is
a knight, then he is telling the truth when he says that B is a knight, so that q is true, and A and B
are the same type. However, if B is a knight, then B’s statement that A and B are of opposite
types, the statement (p ∧¬q) ∨ (¬p ∧ q), would have to be true, which it is not, because A
and B are both knights. Consequently, we can conclude that A is not a knight, that is, that p is
false.
If A is a knave, then because everything a knave says is false, A’s statement that B is
a knight, that is, that q is true, is a lie. This means that q is false and B is also a knave.
Furthermore, if B is a knave, then B’s statement that A and B are opposite types is a lie,
which is consistent with both A and B being knaves. We can conclude that both A and B are
knaves.
▲
We pose more of Smullyan’s puzzles about knights and knaves in Exercises 19–23. In
Exercises 24–31 we introduce related puzzles where we have three types of people, knights and
knaves as in this puzzle together with spies who can lie.
Next, we pose a puzzle known as the muddy children puzzle for the case of two children.
EXAMPLE 8 A father tells his two children, a boy and a girl, to play in their backyard without getting dirty.
However, while playing, both children get mud on their foreheads. When the children stop
playing, the father says “At least one of you has a muddy forehead,” and then asks the children
to answer “Yes” or “No” to the question: “Do you know whether you have a muddy forehead?”
The father asks this question twice. What will the children answer each time this question is
asked, assuming that a child can see whether his or her sibling has a muddy forehead, but cannot
see his or her own forehead? Assume that both children are honest and that the children answer
each question simultaneously.
Solution: Let s be the statement that the son has a muddy forehead and let d be the statement that
the daughter has a muddy forehead. When the father says that at least one of the two children
has a muddy forehead, he is stating that the disjunction s ∨ d is true. Both children will answer
“No” the first time the question is asked because each sees mud on the other child’s forehead.
That is, the son knows that d is true, but does not know whether s is true, and the daughter
knows that s is true, but does not know whether d is true.
After the son has answered “No” to the first question, the daughter can determine that d
must be true. This follows because when the first question is asked, the son knows that s ∨ d is
true, but cannot determine whether s is true. Using this information, the daughter can conclude
that d must be true, for if d were false, the son could have reasoned that because s ∨ d is true,
then s must be true, and he would have answered “Yes” to the first question. The son can reason
in a similar way to determine that s must be true. It follows that both children answer “Yes” the
second time the question is asked.
▲
Logic Circuits
Propositional logic can be applied to the design of computer hardware. This was first observed
in 1938 by Claude Shannon in his MIT master’s thesis. In Chapter 12 we will study this topic
in depth. (See that chapter for a biography of Shannon.) We give a brief introduction to this
application here.
A logic circuit (or digital circuit) receives input signals p1, p2, . . . , pn, each a bit [either
0 (off) or 1 (on)], and produces output signals s1, s2, . . . , sn, each a bit. In this section we will
In Chapter 12 we design
some useful circuits.
restrict our attention to logic circuits with a single output signal; in general, digital circuits may
have multiple outputs.
RAYMOND SMULLYAN (BORN 1919) Raymond Smullyan dropped out of high school. He wanted to study
what he was really interested in and not standard high school material. After jumping from one university to
the next, he earned an undergraduate degree in mathematics at the University of Chicago in 1955. He paid
his college expenses by performing magic tricks at parties and clubs. He obtained a Ph.D. in logic in 1959 at
Princeton, studying under Alonzo Church. After graduating from Princeton, he taught mathematics and logic at
Dartmouth College, Princeton University,Yeshiva University, and the City University of NewYork. He joined
the philosophy department at Indiana University in 1981 where he is now an emeritus professor.
Smullyan has written many books on recreational logic and mathematics, including Satan, Cantor, and
Infinity; What Is the Name of This Book?; The Lady or the Tiger?; Alice in Puzzleland; To Mock a Mockingbird;
Forever Undecided; and The Riddle of Scheherazade: Amazing Logic Puzzles, Ancient and Modern. Because his logic puzzles are
challenging, entertaining, and thought-provoking, he is considered to be a modern-day Lewis Carroll. Smullyan has also written
several books about the application of deductive logic to chess, three collections of philosophical essays and aphorisms, and several
advanced books on mathematical logic and set theory. He is particularly interested in self-reference and has worked on extending
some of Gödel’s results that show that it is impossible to write a computer program that can solve all mathematical problems. He is
also particularly interested in explaining ideas from mathematical logic to the public.
Smullyan is a talented musician and often plays piano with his wife, who is a concert-level pianist. Making telescopes is one
of his hobbies. He is also interested in optics and stereo photography. He states “I’ve never had a conflict between teaching and
research as some people do because when I’m teaching, I’m doing research.” Smullyan is the subject of a documentary short film
entitled This Film Needs No Title.
p
p ∨ q
q
p
q
p p ∧ q
Inverter OR gate AND gate
¬p
FIGURE 1 Basic logic gates.
q (p ∧ ¬q) ∨ ¬r
p p ∧ ¬q
¬q
r
¬r
FIGURE 2 A combinatorial circuit.
Complicated digital circuits can be constructed from three basic circuits, called gates, shown
in Figure 1. The inverter, or NOT gate, takes an input bit p, and produces as output ¬p. The
OR gate takes two input signals p and q, each a bit, and produces as output the signal p ∨ q.
Finally, the AND gate takes two input signals p and q, each a bit, and produces as output the
signal p ∧ q.We use combinations of these three basic gates to build more complicated circuits,
such as that shown in Figure 2.
Given a circuit built from the basic logic gates and the inputs to the circuit, we determine
the output by tracing through the circuit, as Example 9 shows.
EXAMPLE 9 Determine the output for the combinatorial circuit in Figure 2.
Solution: In Figure 2 we display the output of each logic gate in the circuit.We see that theAND
gate takes input of p and ¬q, the output of the inverter with input q, and produces p ∧¬q.
Next, we note that the OR gate takes input p ∧¬q and ¬r, the output of the inverter with
input r, and produces the final output (p ∧¬q)∨¬r.
▲
Suppose that we have a formula for the output of a digital circuit in terms of negations,
disjunctions, and conjunctions. Then, we can systematically build a digital circuit with the
desired output, as illustrated in Example 10.
EXAMPLE 10 Build a digital circuit that produces the output (p ∨¬r) ∧ (¬p ∨ (q ∨¬r)) when given input
bits p, q, and r.
Solution: To construct the desired circuit, we build separate circuits for p ∨¬r and for ¬p ∨
(q ∨¬r) and combine them using an AND gate. To construct a circuit for p ∨¬r, we use an
inverter to produce ¬r from the input r. Then, we use an OR gate to combine p and ¬r. To
build a circuit for ¬p ∨ (q ∨¬r), we first use an inverter to obtain ¬r. Then we use an OR gate
with inputs q and ¬r to obtain q ∨¬r. Finally, we use another inverter and an OR gate to get
¬p ∨ (q ∨¬r) from the inputs p and q ∨¬r.
To complete the construction, we employ a final AND gate, with inputs p ∨¬r and ¬p ∨
(q ∨¬r). The resulting circuit is displayed in Figure 3.
▲
We will study logic circuits in great detail in Chapter 12 in the context of Boolean algebra,
and with different notation.
FIGURE 3 The circuit for (p ∨¬r) ∧ (¬p ∨ (q ∨¬r)).
Exercises
In Exercises 1–6, translate the given statement into propositional
logic using the propositions provided.
1. You cannot edit a protected Wikipedia entry unless you
are an administrator. Express your answer in terms of e:
“You can edit a protected Wikipedia entry” and a: “You
are an administrator.”
2. You can see the movie only if you are over 18 years old
or you have the permission of a parent. Express your answer
in terms of m: “You can see the movie,” e: “You are
over 18 years old,” and p: “You have the permission of a
parent.”
3. You can graduate only if you have completed the requirements
of your major and you do not owe money to the
university and you do not have an overdue library book.
Express your answer in terms of g: “You can graduate,”
m: “You owe money to the university,” r: “You have completed
the requirements of your major,” and b: “You have
an overdue library book.”
4. To use the wireless network in the airport you must pay
the daily fee unless you are a subscriber to the service.
Express your answer in terms ofw: “You can use the wireless
network in the airport,” d: “You pay the daily fee,”
and s: “You are a subscriber to the service.”
5. You are eligible to be President of the U.S.A. only if you
are at least 35 years old, were born in the U.S.A, or at the
time of your birth both of your parents were citizens, and
you have lived at least 14 years in the country. Express
your answer in terms of e: “You are eligible to be President
of the U.S.A.,” a: “You are at least 35 years old,”
b: “You were born in the U.S.A,” p: “At the time of your
birth, both of your parents where citizens,” and r: “You
have lived at least 14 years in the U.S.A.”
6. You can upgrade your operating system only if you have
a 32-bit processor running at 1 GHz or faster, at least
1 GB RAM, and 16 GB free hard disk space, or a 64-
bit processor running at 2 GHz or faster, at least 2 GB
RAM, and at least 32 GB free hard disk space. Express
you answer in terms of u: “You can upgrade your operating
system,” b32: “You have a 32-bit processor,” b64:
“You have a 64-bit processor,” g1: “Your processor runs
at 1 GHz or faster,” g2: “Your processor runs at 2 GHz or
faster,” r1: “Your processor has at least 1 GB RAM,” r2:
“Your processor has at least 2 GB RAM,” h16: “You have
at least 16 GB free hard disk space,” and h32: “You have
at least 32 GB free hard disk space.”
7. Express these system specifications using the propositions
p “The message is scanned for viruses” and q “The
message was sent from an unknown system” together
with logical connectives (including negations).
a) “The message is scanned for viruses whenever the
message was sent from an unknown system.”
b) “The message was sent from an unknown system but
it was not scanned for viruses.”
c) “It is necessary to scan the message for viruses whenever
it was sent from an unknown system.”
d) “When a message is not sent from an unknown system
it is not scanned for viruses.”
8. Express these system specifications using the propositions
p “The user enters a valid password,” q “Access is
granted,” and r “The user has paid the subscription fee”
and logical connectives (including negations).
a) “The user has paid the subscription fee, but does not
enter a valid password.”
b) “Access is granted whenever the user has paid the
subscription fee and enters a valid password.”
c) “Access is denied if the user has not paid the subscription
fee.”
d) “If the user has not entered a valid password but has
paid the subscription fee, then access is granted.”
9. Are these system specifications consistent? “The system
is in multiuser state if and only if it is operating normally.
If the system is operating normally, the kernel is functioning.
The kernel is not functioning or the system is
in interrupt mode. If the system is not in multiuser state,
then it is in interrupt mode. The system is not in interrupt
mode.”
10. Are these system specifications consistent? “Whenever
the system software is being upgraded, users cannot access
the file system. If users can access the file system,
then they can save new files. If users cannot save new
files, then the system software is not being upgraded.”
11. Are these system specifications consistent? “The router
can send packets to the edge system only if it supports the
new address space. For the router to support the new address
space it is necessary that the latest software release
be installed. The router can send packets to the edge system
if the latest software release is installed, The router
does not support the new address space.”
12. Are these system specifications consistent? “If the file
system is not locked, then new messages will be queued.
If the file system is not locked, then the system is functioning
normally, and conversely. If newmessages are not
queued, then they will be sent to the message buffer. If
the file system is not locked, then new messages will be
sent to the message buffer. New messages will not be sent
to the message buffer.”
13. What Boolean search would you use to look for Web
pages about beaches in New Jersey? What if you wanted
to findWeb pages about beaches on the isle of Jersey (in
the English Channel)?
14. What Boolean search would you use to look for Web
pages about hiking inWestVirginia? What if you wanted
to findWeb pages about hiking inVirginia, but not inWest
Virginia?
∗15. Each inhabitant of a remote village always tells the truth
or always lies.A villager will give only a “Yes” or a “No”
response to a question a tourist asks. Suppose you are a
tourist visiting this area and come to a fork in the road.
One branch leads to the ruins you want to visit; the other
branch leads deep into the jungle. A villager is standing
at the fork in the road. What one question can you ask the
villager to determine which branch to take?
16. An explorer is captured by a group of cannibals. There are
two types of cannibals—those who always tell the truth
and those who always lie. The cannibals will barbecue
the explorer unless he can determine whether a particular
cannibal always lies or always tells the truth. He is
allowed to ask the cannibal exactly one question.
a) Explain why the question “Are you a liar?” does not
work.
b) Find a question that the explorer can use to determine
whether the cannibal always lies or always tells the
truth.
17. When three professors are seated in a restaurant, the hostess
asks them: “Does everyone want coffee?” The first
professor says: “I do not know.” The second professor
then says: “I do not know.” Finally, the third professor
says: “No, not everyonewants coffee.” The hostess comes
back and gives coffee to the professors who want it. How
did she figure out who wanted coffee?
18. When planning a party you want to know whom to invite.
Among the people you would like to invite are three
touchy friends.You know that if Jasmine attends, she will
become unhappy if Samir is there, Samir will attend only
if Kanti will be there, and Kanti will not attend unless Jasmine
also does.Which combinations of these three friends
can you invite so as not to make someone unhappy?
Exercises 19–23 relate to inhabitants of the island of knights
and knaves created by Smullyan, where knights always tell
the truth and knaves always lie. You encounter two people,
A and B. Determine, if possible, what A and B are if they
address you in the ways described. If you cannot determine
what these two people are, can you draw any conclusions?
19. A says “At least one of us is a knave” and B says nothing.
20. A says “The two of us are both knights” and B says “A
is a knave.”
21. Asays “I am a knave orB is a knight” andB says nothing.
22. Both A and B say “I am a knight.”
23. A says “We are both knaves” and B says nothing.
Exercises 24–31 relate to inhabitants of an island on which
there are three kinds of people: knights who always tell the
truth, knaves who always lie, and spies (called normals by
Smullyan [Sm78]) who can either lie or tell the truth. You
encounter three people, A, B, and C. You know one of these
people is a knight, one is a knave, and one is a spy. Each of the
three people knows the type of person each of other two is. For
each of these situations, if possible, determine whether there
is a unique solution and determine who the knave, knight, and
spy are. When there is no unique solution, list all possible
solutions or state that there are no solutions.
24. A says “C is the knave,” B says, “A is the knight,” and C
says “I am the spy.”
25. A says “I am the knight,” B says “I am the knave,” and
C says “B is the knight.”
26. A says “I am the knave,” B says “I am the knave,” and C
says “I am the knave.”
27. A says “I am the knight,” B says “A is telling the truth,”
and C says “I am the spy.”
28. A says “I am the knight,” B says, “A is not the knave,”
and C says “B is not the knave.”
29. A says “I am the knight,” B says “I am the knight,” and
C says “I am the knight.”
30. A says “I am not the spy,” B says “I am not the spy,” and
C says “A is the spy.”
31. A says “I am not the spy,” B says “I am not the spy,” and
C says “I am not the spy.”
Exercises 32–38 are puzzles that can be solved by translating
statements into logical expressions and reasoning from these
expressions using truth tables.
32. The police have three suspects for the murder of Mr.
Cooper: Mr. Smith, Mr. Jones, and Mr.Williams. Smith,
Jones, and Williams each declare that they did not kill
Cooper. Smith also states that Cooper was a friend of
Jones and that Williams disliked him. Jones also states
that he did not know Cooper and that he was out of town
the day Cooper was killed. Williams also states that he
saw both Smith and Jones with Cooper the day of the
killing and that either Smith or Jones must have killed
him. Can you determine who the murderer was if
a) one of the three men is guilty, the two innocent men
are telling the truth, but the statements of the guilty
man may or may not be true?
b) innocent men do not lie?
33. Stevewould like to determine the relative salaries of three
coworkers using two facts. First, he knows that if Fred
is not the highest paid of the three, then Janice is. Second,
he knows that if Janice is not the lowest paid, then
Maggie is paid the most. Is it possible to determine the
relative salaries of Fred, Maggie, and Janice from what
Steve knows? If so, who is paid the most and who the
least? Explain your reasoning.
34. Five friends have access to a chat room. Is it possible to
determine who is chatting if the following information is
known? Either Kevin or Heather, or both, are chatting.
Either Randy orVijay, but not both, are chatting. If Abby
is chatting, so is Randy. Vijay and Kevin are either both
chatting or neither is. If Heather is chatting, then so are
Abby and Kevin. Explain your reasoning.
35. A detective has interviewed four witnesses to a crime.
From the stories of the witnesses the detective has concluded
that if the butler is telling the truth then so is the
cook; the cook and the gardener cannot both be telling the
truth; the gardener and the handyman are not both lying;
and if the handyman is telling the truth then the cook is
lying. For each of the four witnesses, can the detective determine
whether that person is telling the truth or lying?
Explain your reasoning.
36. Four friends have been identified as suspects for an unauthorized
access into a computer system. They have made
statements to the investigating authorities. Alice said
“Carlos did it.” John said “I did not do it.” Carlos said
“Diana did it.” Diana said “Carlos lied when he said that
I did it.”
a) If the authorities also know that exactly one of the
four suspects is telling the truth, who did it? Explain
your reasoning.
b) If the authorities also know that exactly one is lying,
who did it? Explain your reasoning.
37. Suppose there are signs on the doors to two rooms. The
sign on the first door reads “In this room there is a lady,
and in the other one there is a tiger”; and the sign on the
second door reads “In one of these rooms, there is a lady,
and in one of them there is a tiger.” Suppose that you
know that one of these signs is true and the other is false.
Behind which door is the lady?
∗38. Solve this famous logic puzzle, attributed to Albert Einstein,
and known as the zebra puzzle. Five men with
different nationalities and with different jobs live in consecutive
houses on a street. These houses are painted different
colors. The men have different pets and have different
favorite drinks. Determine who owns a zebra and
whose favorite drink is mineral water (which is one of the
favorite drinks) given these clues: The Englishman lives
in the red house. The Spaniard owns a dog. The Japanese
man is a painter. The Italian drinks tea. The Norwegian
lives in the first house on the left. The green house is
immediately to the right of the white one. The photographer
breeds snails. The diplomat lives in the yellowhouse.
Milk is drunk in the middle house. The owner of the green
house drinks coffee. The Norwegian’s house is next to the
blue one. The violinist drinks orange juice. The fox is in
a house next to that of the physician. The horse is in a
house next to that of the diplomat. [Hint: Make a table
where the rows represent the men and columns represent
the color of their houses, their jobs, their pets, and their
favorite drinks and use logical reasoning to determine the
correct entries in the table.]
39. Freedonia has fifty senators. Each senator is either honest
or corrupt. Suppose you knowthat at least one of the Freedonian
senators is honest and that, given any two Freedonian
senators, at least one is corrupt. Based on these
facts, can you determine how many Freedonian senators
are honest and how many are corrupt? If so, what is the
answer?
40. Find the output of each of these combinatorial circuits.
q
p
p
q
a) p
b)
41. Find the output of each of these combinatorial circuits.
r
q
p
r
p
q
p
a)
b)
42. Construct a combinatorial circuit using inverters,
OR gates, and AND gates that produces the output
(p ∧¬r) ∨ (¬q ∧ r) from input bits p, q, and r.
43. Construct a combinatorial circuit using inverters,
OR gates, and AND gates that produces the output
((¬p ∨¬r)∧¬q) ∨ (¬p ∧ (q ∨ r)) from input bits p,
q, and r.
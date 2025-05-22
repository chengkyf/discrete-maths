1.1 Propositional Logic
Introduction
The rules of logic give precise meaning to mathematical statements. These rules are used to
distinguish between valid and invalid mathematical arguments. Because a major goal of this book
is to teach the reader how to understand and how to construct correct mathematical arguments,
we begin our study of discrete mathematics with an introduction to logic.
Besides the importance of logic in understanding mathematical reasoning, logic has numerous
applications to computer science. These rules are used in the design of computer circuits,
the construction of computer programs, the verification of the correctness of programs, and in
many other ways. Furthermore, software systems have been developed for constructing some,
but not all, types of proofs automatically.We will discuss these applications of logic in this and
later chapters.
Propositions
Our discussion begins with an introduction to the basic building blocks of logic—propositions.
A proposition is a declarative sentence (that is, a sentence that declares a fact) that is either true
or false, but not both.
EXAMPLE 1 All the following declarative sentences are propositions.
1. Washington, D.C., is the capital of the United States of America.
2. Toronto is the capital of Canada.
3. 1 + 1 = 2.
4. 2 + 2 = 3.
Propositions 1 and 3 are true, whereas 2 and 4 are false.
▲
Some sentences that are not propositions are given in Example 2.
EXAMPLE 2 Consider the following sentences.
1. What time is it?
2. Read this carefully.
3. x + 1 = 2.
4. x + y = z.
Sentences 1 and 2 are not propositions because they are not declarative sentences. Sentences 3
and 4 are not propositions because they are neither true nor false. Note that each of sentences 3
and 4 can be turned into a proposition if we assign values to the variables.We will also discuss
other ways to turn sentences such as these into propositions in Section 1.4.
▲
We use letters to denote propositional variables (or statement variables), that is, variables
that represent propositions, just as letters are used to denote numerical variables. The
ARISTOTLE (384 b.c.e.–322 b.c.e.) Aristotlewas born in Stagirus (Stagira) in northern Greece. His fatherwas
the personal physician of the King of Macedonia. Because his father died when Aristotle was young, Aristotle
could not follow the custom of following his father’s profession. Aristotle became an orphan at a young age
when his mother also died. His guardian who raised him taught him poetry, rhetoric, and Greek. At the age of
17, his guardian sent him to Athens to further his education. Aristotle joined Plato’s Academy, where for 20
years he attended Plato’s lectures, later presenting his own lectures on rhetoric. When Plato died in 347 B.C.E.,
Aristotle was not chosen to succeed him because his views differed too much from those of Plato. Instead,
Aristotle joined the court of King Hermeas where he remained for three years, and married the niece of the
King. When the Persians defeated Hermeas, Aristotle moved to Mytilene and, at the invitation of King Philip
of Macedonia, he tutored Alexander, Philip’s son, who later became Alexander the Great. Aristotle tutored Alexander for five years
and after the death of King Philip, he returned to Athens and set up his own school, called the Lyceum.
Aristotle’s followers were called the peripatetics, which means “to walk about,” because Aristotle often walked around as he
discussed philosophical questions. Aristotle taught at the Lyceum for 13 years where he lectured to his advanced students in the
morning and gave popular lectures to a broad audience in the evening. WhenAlexander the Great died in 323 B.C.E., a backlash against
anything related to Alexander led to trumped-up charges of impiety against Aristotle. Aristotle fled to Chalcis to avoid prosecution.
He only lived one year in Chalcis, dying of a stomach ailment in 322 B.C.E.
Aristotle wrote three types of works: those written for a popular audience, compilations of scientific facts, and systematic
treatises. The systematic treatises included works on logic, philosophy, psychology, physics, and natural history. Aristotle’s writings
were preserved by a student and were hidden in a vault where a wealthy book collector discovered them about 200 years later. They
were taken to Rome, where they were studied by scholars and issued in new editions, preserving them for posterity.
conventional letters used for propositional variables are p, q, r, s, . . . . The truth value of a
proposition is true, denoted by T, if it is a true proposition, and the truth value of a proposition
is false, denoted by F, if it is a false proposition.
The area of logic that deals with propositions is called the propositional calculus or propositional
logic. It was first developed systematically by the Greek philosopher Aristotle more
than 2300 years ago.
We now turn our attention to methods for producing new propositions from those that
we already have. These methods were discussed by the English mathematician George Boole
in 1854 in his book The Laws of Thought. Many mathematical statements are constructed by
combining one or more propositions. New propositions, called compound propositions, are
formed from existing propositions using logical operators.
DEFINITION 1 Let p be a proposition. The negation of p, denoted by¬p (also denoted by p), is the statement
“It is not the case that p.”
The proposition ¬p is read “not p.” The truth value of the negation of p, ¬p, is the opposite
of the truth value of p.
EXAMPLE 3 Find the negation of the proposition
“Michael’s PC runs Linux”
and express this in simple English.
Solution: The negation is
“It is not the case that Michael’s PC runs Linux.”
This negation can be more simply expressed as
“Michael’s PC does not run Linux.”
▲
EXAMPLE 4 Find the negation of the proposition
“Vandana’s smartphone has at least 32GB of memory”
and express this in simple English.
Solution: The negation is
“It is not the case that Vandana’s smartphone has at least 32GB of memory.”
This negation can also be expressed as
“Vandana’s smartphone does not have at least 32GB of memory”
or even more simply as
“Vandana’s smartphone has less than 32GB of memory.”
TABLE 1 The
Truth Table for
the Negation of a
Proposition.
p ¬p
T F
F T
Table 1 displays the truth table for the negation of a proposition p. This table has a row
for each of the two possible truth values of a proposition p. Each row shows the truth value of
¬p corresponding to the truth value of p for this row.
The negation of a proposition can also be considered the result of the operation of the
negation operator on a proposition. The negation operator constructs a new proposition from
a single existing proposition.We will now introduce the logical operators that are used to form
new propositions from two or more existing propositions. These logical operators are also called
connectives.
DEFINITION 2 Let p and q be propositions. The conjunction of p and q, denoted by p ∧ q, is the proposition
“p and q.” The conjunction p ∧ q is true when both p and q are true and is false otherwise.
Table 2 displays the truth table of p ∧ q. This table has a row for each of the four possible
combinations of truth values of p and q. The four rows correspond to the pairs of truth values
TT, TF, FT, and FF, where the first truth value in the pair is the truth value of p and the second
truth value is the truth value of q.
Note that in logic the word “but” sometimes is used instead of “and” in a conjunction. For
example, the statement “The sun is shining, but it is raining” is another way of saying “The sun
is shining and it is raining.” (In natural language, there is a subtle difference in meaning between
“and” and “but”; we will not be concerned with this nuance here.)
EXAMPLE 5 Find the conjunction of the propositions p and q where p is the proposition “Rebecca’s PC has
more than 16 GB free hard disk space” and q is the proposition “The processor in Rebecca’s
PC runs faster than 1 GHz.”
Solution: The conjunction of these propositions, p ∧ q, is the proposition “Rebecca’s PC has
more than 16 GB free hard disk space, and the processor in Rebecca’s PC runs faster than 1
GHz.” This conjunction can be expressed more simply as “Rebecca’s PC has more than 16 GB
free hard disk space, and its processor runs faster than 1 GHz.” For this conjunction to be true,
both conditions given must be true. It is false, when one or both of these conditions are false. ▲
DEFINITION 3 Let p and q be propositions. The disjunction of p and q, denoted by p ∨ q, is the proposition
“p or q.” The disjunction p ∨ q is false when both p and q are false and is true otherwise.
Table 3 displays the truth table for p ∨ q.
TABLE 2 The Truth Table for
the Conjunction of Two
Propositions.
p q p ∧ q
T T T
T F F
F T F
F F F
TABLE 3 The Truth Table for
the Disjunction of Two
Propositions.
p q p ∨ q
T T T
T F T
F T T
F F F
The use of the connective or in a disjunction corresponds to one of the two ways the word
or is used in English, namely, as an inclusive or. A disjunction is true when at least one of the
two propositions is true. For instance, the inclusive or is being used in the statement
“Students who have taken calculus or computer science can take this class.”
Here, we mean that students who have taken both calculus and computer science can take the
class, as well as the students who have taken only one of the two subjects. On the other hand,
we are using the exclusive or when we say
“Students who have taken calculus or computer science, but not both, can enroll in this
class.”
Here, we mean that students who have taken both calculus and a computer science course cannot
take the class. Only those who have taken exactly one of the two courses can take the class.
Similarly, when a menu at a restaurant states, “Soup or salad comes with an entrée,” the
restaurant almost always means that customers can have either soup or salad, but not both.
Hence, this is an exclusive, rather than an inclusive, or.
EXAMPLE 6 What is the disjunction of the propositions p and q where p and q are the same propositions as
in Example 5?
Solution: The disjunction of p and q, p ∨ q, is the proposition
“Rebecca’s PC has at least 16 GB free hard disk space, or the processor in Rebecca’s PC
runs faster than 1 GHz.”
This proposition is true when Rebecca’s PC has at least 16 GB free hard disk space, when the
PC’s processor runs faster than 1 GHz, and when both conditions are true. It is false when both
of these conditions are false, that is, when Rebecca’s PC has less than 16 GB free hard disk
space and the processor in her PC runs at 1 GHz or slower.
▲
As was previously remarked, the use of the connective or in a disjunction corresponds
to one of the two ways the word or is used in English, namely, in an inclusive way. Thus, a
disjunction is true when at least one of the two propositions in it is true. Sometimes, we use or
in an exclusive sense. When the exclusive or is used to connect the propositions p and q, the
proposition “p or q (but not both)” is obtained. This proposition is true when p is true and q is
false, and when p is false and q is true. It is false when both p and q are false and when both
are true.
GEORGE BOOLE (1815–1864) George Boole, the son of a cobbler, was born in Lincoln, England, in
November 1815. Because of his family’s difficult financial situation, Boole struggled to educate himself while
supporting his family. Nevertheless, he became one of the most important mathematicians of the 1800s.Although
he considered a career as a clergyman, he decided instead to go into teaching, and soon afterward opened a
school of his own. In his preparation for teaching mathematics, Boole—unsatisfied with textbooks of his day—
decided to read the works of the great mathematicians. While reading papers of the great French mathematician
Lagrange, Boole made discoveries in the calculus of variations, the branch of analysis dealing with finding
curves and surfaces by optimizing certain parameters.
In 1848 Boole published The Mathematical Analysis of Logic, the first of his contributions to symbolic logic.
In 1849 he was appointed professor of mathematics at Queen’s College in Cork, Ireland. In 1854 he published The Laws of Thought,
his most famous work. In this book, Boole introduced what is now called Boolean algebra in his honor. Boole wrote textbooks
on differential equations and on difference equations that were used in Great Britain until the end of the nineteenth century. Boole
married in 1855; his wife was the niece of the professor of Greek at Queen’s College. In 1864 Boole died from pneumonia, which
he contracted as a result of keeping a lecture engagement even though he was soaking wet from a rainstorm.
TABLE 4 The Truth Table for
the Exclusive Or of Two
Propositions.
p q p ⊕ q
T T F
T F T
F T T
F F F
TABLE 5 The Truth Table for
the Conditional Statement
p → q.
p q p → q
T T T
T F F
F T T
F F T
DEFINITION 4 Let p and q be propositions. The exclusive or of p and q, denoted by p ⊕ q, is the proposition
that is true when exactly one of p and q is true and is false otherwise.
The truth table for the exclusive or of two propositions is displayed in Table 4.
Conditional Statements
We will discuss several other important ways in which propositions can be combined.
DEFINITION 5 Let p and q be propositions. The conditional statement p → q is the proposition “if p, then
q.” The conditional statement p → q is false when p is true and q is false, and true otherwise.
In the conditional statement p → q, p is called the hypothesis (or antecedent or premise)
and q is called the conclusion (or consequence).
The statement p → q is called a conditional statement because p → q asserts that q is true
on the condition that p holds. A conditional statement is also called an implication.
The truth table for the conditional statement p → q is shown in Table 5. Note that the
statement p → q is true when both p and q are true and when p is false (no matter what truth
value q has).
Because conditional statements play such an essential role in mathematical reasoning, a
variety of terminology is used to express p → q. You will encounter most if not all of the
following ways to express this conditional statement:
“if p, then q” “p implies q”
“if p, q” “p only if q”
“p is sufficient for q” “a sufficient condition for q is p”
“q if p” “q whenever p”
“q when p” “q is necessary for p”
“a necessary condition for p is q” “q follows from p”
“q unless ¬p”
A useful way to understand the truth value of a conditional statement is to think of an
obligation or a contract. For example, the pledge many politicians make when running for office
is
“If I am elected, then I will lower taxes.”
If the politician is elected, voters would expect this politician to lower taxes. Furthermore, if the
politician is not elected, then voters will not have any expectation that this person will lower
taxes, although the person may have sufficient influence to cause those in power to lower taxes.
It is only when the politician is elected but does not lower taxes that voters can say that the
politician has broken the campaign pledge. This last scenario corresponds to the case when p
is true but q is false in p → q.
Similarly, consider a statement that a professor might make:
“If you get 100% on the final, then you will get an A.”
If you manage to get a 100% on the final, then you would expect to receive an A. If you do not
get 100% you may or may not receive an A depending on other factors. However, if you do get
100%, but the professor does not give you an A, you will feel cheated.
Of the various ways to express the conditional statement p → q, the two that seem to cause
the most confusion are “p only if q” and “q unless ¬p.” Consequently, we will provide some
guidance for clearing up this confusion.
To remember that “p only if q” expresses the same thing as “if p, then q,” note that “p only
if q” says that p cannot be true when q is not true. That is, the statement is false if p is true,
but q is false. When p is false, q may be either true or false, because the statement says nothing
about the truth value of q. Be careful not to use “q only if p” to express p → q because this is
incorrect. To see this, note that the true values of “q only if p” and p → q are different when
p and q have different truth values.
You might have trouble
understanding how
“unless” is used in
conditional statements
unless you read this
paragraph carefully.
To remember that “q unless ¬p” expresses the same conditional statement as “if p, then
q,” note that “q unless ¬p” means that if ¬p is false, then q must be true. That is, the statement
“q unless ¬p” is false when p is true but q is false, but it is true otherwise. Consequently,
“q unless ¬p” and p → q always have the same truth value.
We illustrate the translation between conditional statements and English statements in Example
7.
EXAMPLE 7 Let p be the statement “Maria learns discrete mathematics” and q the statement “Maria will
find a good job.” Express the statement p → q as a statement in English.
Solution: From the definition of conditional statements, we see that when p is the statement
“Maria learns discrete mathematics” and q is the statement “Maria will find a good job,” p → q
represents the statement
“If Maria learns discrete mathematics, then she will find a good job.”
There are many other ways to express this conditional statement in English. Among the most
natural of these are:
“Maria will find a good job when she learns discrete mathematics.”
“For Maria to get a good job, it is sufficient for her to learn discrete mathematics.”
and
“Maria will find a good job unless she does not learn discrete mathematics.”
▲
Note that the way we have defined conditional statements is more general than the meaning
attached to such statements in the English language. For instance, the conditional statement in
Example 7 and the statement
“If it is sunny, then we will go to the beach.”
are statements used in normal language where there is a relationship between the hypothesis
and the conclusion. Further, the first of these statements is true unless Maria learns discrete
mathematics, but she does not get a good job, and the second is true unless it is indeed sunny,
but we do not go to the beach. On the other hand, the statement
“If Juan has a smartphone, then 2 + 3 = 5”
is true from the definition of a conditional statement, because its conclusion is true. (The truth
value of the hypothesis does not matter then.) The conditional statement
“If Juan has a smartphone, then 2 + 3 = 6”
is true if Juan does not have a smartphone, even though 2 + 3 = 6 is false. We would not use
these last two conditional statements in natural language (except perhaps in sarcasm), because
there is no relationship between the hypothesis and the conclusion in either statement. In mathematical
reasoning, we consider conditional statements of a more general sort than we use in
English. The mathematical concept of a conditional statement is independent of a cause-andeffect
relationship between hypothesis and conclusion. Our definition of a conditional statement
specifies its truth values; it is not based on English usage. Propositional language is an artificial
language; we only parallel English usage to make it easy to use and remember.
The if-then construction used in many programming languages is different from that used
in logic. Most programming languages contain statements such as if p then S, where p is a
proposition and S is a program segment (one or more statements to be executed).When execution
of a program encounters such a statement, S is executed if p is true, but S is not executed if p
is false, as illustrated in Example 8.
EXAMPLE 8 What is the value of the variable x after the statement
if 2 + 2 = 4 then x := x + 1
if x = 0 before this statement is encountered? (The symbol := stands for assignment. The
statement x := x + 1 means the assignment of the value of x + 1 to x.)
Solution: Because 2 + 2 = 4 is true, the assignment statement x := x + 1 is executed. Hence,
x has the value 0 + 1 = 1 after this statement is encountered.
▲
CONVERSE, CONTRAPOSITIVE, AND INVERSE We can form some new conditional
statements starting with a conditional statement p → q. In particular, there are three related
conditional statements that occur so often that they have special names. The proposition q → p
is called the converse of p → q. The contrapositive of p → q is the proposition ¬q →¬p.
The proposition ¬p →¬q is called the inverse of p → q. We will see that of these three
conditional statements formed from p → q, only the contrapositive always has the same truth
value as p → q.
We first show that the contrapositive, ¬q →¬p, of a conditional statement p → q always
has the same truth value as p → q. To see this, note that the contrapositive is false only when
¬p is false and ¬q is true, that is, only when p is true and q is false.We now show that neither
the converse, q → p, nor the inverse, ¬p →¬q, has the same truth value as p → q for all
possible truth values of p and q. Note that when p is true and q is false, the original conditional
statement is false, but the converse and the inverse are both true.
Remember that the
contrapositive, but neither
the converse or inverse, of
a conditional statement is
equivalent to it.
When two compound propositions always have the same truth value we call them equivalent,
so that a conditional statement and its contrapositive are equivalent. The converse and
the inverse of a conditional statement are also equivalent, as the reader can verify, but neither is
equivalent to the original conditional statement. (We will study equivalent propositions in Section
1.3.) Take note that one of the most common logical errors is to assume that the converse
or the inverse of a conditional statement is equivalent to this conditional statement.
We illustrate the use of conditional statements in Example 9.
EXAMPLE 9 What are the contrapositive, the converse, and the inverse of the conditional statement
“The home team wins whenever it is raining?”
Solution: Because “q whenever p” is one of the ways to express the conditional statement
p → q, the original statement can be rewritten as
“If it is raining, then the home team wins.”
Consequently, the contrapositive of this conditional statement is
“If the home team does not win, then it is not raining.”
The converse is
“If the home team wins, then it is raining.”
The inverse is
“If it is not raining, then the home team does not win.”
Only the contrapositive is equivalent to the original statement.
▲
BICONDITIONALS We now introduce another way to combine propositions that expresses
that two propositions have the same truth value.
DEFINITION 6 Let p and q be propositions. The biconditional statement p ↔ q is the proposition “p if
and only if q.” The biconditional statement p ↔ q is true when p and q have the same truth
values, and is false otherwise. Biconditional statements are also called bi-implications.
The truth table for p ↔ q is shown in Table 6. Note that the statement p ↔ q is true when both
the conditional statements p → q and q → p are true and is false otherwise. That is why we use
the words “if and only if” to express this logical connective and why it is symbolically written
by combining the symbols→and←. There are some other common ways to express p ↔ q:
“p is necessary and sufficient for q”
“if p then q, and conversely”
“p iff q.”
The last way of expressing the biconditional statement p ↔ q uses the abbreviation “iff” for
“if and only if.” Note that p ↔ q has exactly the same truth value as (p → q) ∧ (q → p).
TABLE 6 The Truth Table for the
Biconditional p ↔ q.
p q p ↔ q
T T T
T F F
F T F
F F T
EXAMPLE 10 Let p be the statement “You can take the flight,” and let q be the statement “You buy a ticket.”
Then p ↔ q is the statement
“You can take the flight if and only if you buy a ticket.”
This statement is true if p and q are either both true or both false, that is, if you buy a ticket and
can take the flight or if you do not buy a ticket and you cannot take the flight. It is false when
p and q have opposite truth values, that is, when you do not buy a ticket, but you can take the
flight (such as when you get a free trip) and when you buy a ticket but you cannot take the flight
(such as when the airline bumps you).
▲
IMPLICIT USE OF BICONDITIONALS You should be aware that biconditionals are not
always explicit in natural language. In particular, the “if and only if” construction used in
biconditionals is rarely used in common language. Instead, biconditionals are often expressed
using an “if, then” or an “only if” construction. The other part of the “if and only if” is implicit.
That is, the converse is implied, but not stated. For example, consider the statement in English
“If you finish your meal, then you can have dessert.” What is really meant is “You can have
dessert if and only if you finish your meal.” This last statement is logically equivalent to the
two statements “If you finish your meal, then you can have dessert” and “You can have dessert
only if you finish your meal.” Because of this imprecision in natural language, we need to
make an assumption whether a conditional statement in natural language implicitly includes its
converse. Because precision is essential in mathematics and in logic, we will always distinguish
between the conditional statement p → q and the biconditional statement p ↔ q.
Truth Tables of Compound Propositions
We have now introduced four important logical connectives—conjunctions, disjunctions, conditional
statements, and biconditional statements—as well as negations.We can use these connectives
to build up complicated compound propositions involving any number of propositional
variables.We can use truth tables to determine the truth values of these compound propositions,
as Example 11 illustrates. We use a separate column to find the truth value of each compound
expression that occurs in the compound proposition as it is built up. The truth values of the
compound proposition for each combination of truth values of the propositional variables in it
is found in the final column of the table.
EXAMPLE 11 Construct the truth table of the compound proposition
(p ∨¬q) → (p ∧ q).
Solution: Because this truth table involves two propositional variables p and q, there are four
rows in this truth table, one for each of the pairs of truth values TT, TF, FT, and FF. The first
two columns are used for the truth values of p and q, respectively. In the third column we find
the truth value of ¬q, needed to find the truth value of p ∨¬q, found in the fourth column. The
fifth column gives the truth value of p ∧ q. Finally, the truth value of (p ∨¬q) → (p ∧ q) is
found in the last column. The resulting truth table is shown in Table 7.
▲
TABLE 7 The Truth Table of (p ∨¬q) → (p ∧ q).
p q ¬q p ∨¬q p ∧ q (p ∨¬q) → (p ∧ q)
T T F T T T
T F T T F F
F T F F F T
F F T T F F
recedence of Logical Operators
We can construct compound propositions using the negation operator and the logical operators
defined so far.We will generally use parentheses to specify the order in which logical operators
in a compound proposition are to be applied. For instance, (p ∨ q) ∧ (¬r) is the conjunction
of p ∨ q and ¬r. However, to reduce the number of parentheses, we specify that the negation
operator is applied before all other logical operators. This means that ¬p ∧ q is the conjunction
of¬p and q, namely, (¬p) ∧ q, not the negation of the conjunction ofp and q, namely¬(p ∧ q).
Another general rule of precedence is that the conjunction operator takes precedence over
the disjunction operator, so that p ∧ q ∨ r means (p ∧ q) ∨ r rather than p ∧ (q ∨ r). Because
this rule may be difficult to remember, we will continue to use parentheses so that the order of
the disjunction and conjunction operators is clear.
TABLE 8
Precedence of
Logical Operators.
Operator Precedence
¬ 1
∧ 2
∨ 3
→ 4
↔ 5 Finally, it is an accepted rule that the conditional and biconditional operators → and ↔
have lower precedence than the conjunction and disjunction operators, ∧ and ∨. Consequently,
p ∨ q → r is the same as (p ∨ q) → r. We will use parentheses when the order of the conditional
operator and biconditional operator is at issue, although the conditional operator has
precedence over the biconditional operator. Table 8 displays the precedence levels of the logical
operators, ¬, ∧, ∨,→, and↔.
Logic and Bit Operations
Computers represent information using bits.A bit is a symbol with two possible values, namely,
0 (zero) and 1 (one). This meaning of the word bit comes from binary digit, because zeros and
ones are the digits used in binary representations of numbers. The well-known statistician John
Tukey introduced this terminology in 1946.A bit can be used to represent a truth value, because
there are two truth values, namely, true and false. As is customarily done, we will use a 1 bit to
represent true and a 0 bit to represent false. That is, 1 represents T (true), 0 represents F (false).A
variable is called a Boolean variable if its value is either true or false. Consequently, a Boolean
variable can be represented using a bit.
Truth Value Bit
T 1
F 0
Computer bit operations correspond to the logical connectives. By replacing true by a one
and false by a zero in the truth tables for the operators ∧, ∨, and ⊕, the tables shown in Table 9
for the corresponding bit operations are obtained.We will also use the notation OR, AND, and
XOR for the operators ∨,∧, and ⊕, as is done in various programming languages.
JOHN WILDER TUKEY (1915–2000) Tukey, born in New Bedford, Massachusetts, was an only child. His
parents, both teachers, decided home schooling would best develop his potential. His formal education began
at Brown University, where he studied mathematics and chemistry. He received a master’s degree in chemistry
from Brown and continued his studies at Princeton University, changing his field of study from chemistry to
mathematics. He received his Ph.D. from Princeton in 1939 for work in topology, when he was appointed an
instructor in mathematics at Princeton.With the start ofWorldWar II, he joined the Fire Control Research Office,
where he began working in statistics. Tukey found statistical research to his liking and impressed several leading
statisticians with his skills. In 1945, at the conclusion of the war, Tukey returned to the mathematics department
at Princeton as a professor of statistics, and he also took a position at AT&T Bell Laboratories. Tukey founded
the Statistics Department at Princeton in 1966 and was its first chairman. Tukey made significant contributions to many areas of
statistics, including the analysis of variance, the estimation of spectra of time series, inferences about the values of a set of parameters
from a single experiment, and the philosophy of statistics. However, he is best known for his invention, with J.W. Cooley, of the fast
Fourier transform. In addition to his contributions to statistics, Tukey was noted as a skilled wordsmith; he is credited with coining
the terms bit and software.
Tukey contributed his insight and expertise by serving on the President’s Science Advisory Committee. He chaired several
important committees dealing with the environment, education, and chemicals and health. He also served on committees working
on nuclear disarmament. Tukey received many awards, including the National Medal of Science.
HISTORICAL NOTE There were several other suggested words for a binary digit, including binit and bigit, that never were widely
accepted. The adoption of the word bit may be due to its meaning as a common English word. For an account of Tukey’s coining
of the word bit, see the April 1984 issue of Annals of the History of Computing.
TABLE 9 Table for the Bit Operators OR,
AND, and XOR.
x y x ∨ y x ∧ y x ⊕ y
0 0 0 0 0
0 1 1 0 1
1 0 1 0 1
1 1 1 1 0
Information is often represented using bit strings, which are lists of zeros and ones. When
this is done, operations on the bit strings can be used to manipulate this information.
DEFINITION 7 A bit string is a sequence of zero or more bits. The length of this string is the number of bits
in the string.
EXAMPLE 12 101010011 is a bit string of length nine.
▲
We can extend bit operations to bit strings. We define the bitwise OR, bitwise AND, and
bitwise XOR of two strings of the same length to be the strings that have as their bits the OR,
AND, and XOR of the corresponding bits in the two strings, respectively. We use the symbols
∨,∧, and⊕to represent the bitwise OR, bitwiseAND, and bitwise XOR operations, respectively.
We illustrate bitwise operations on bit strings with Example 13.
EXAMPLE 13 Find the bitwise OR, bitwise AND, and bitwise XOR of the bit strings 01 1011 0110 and
11 0001 1101. (Here, and throughout this book, bit strings will be split into blocks of four
bits to make them easier to read.)
Solution: The bitwise OR, bitwise AND, and bitwise XOR of these strings are obtained by taking
the OR, AND, and XOR of the corresponding bits, respectively. This gives us
01 1011 0110
11 0001 1101
11 1011 1111 bitwise OR
01 0001 0100 bitwise AND
10 1010 1011 bitwise XOR
▲
Exercises
1. Which of these sentences are propositions? What are the
truth values of those that are propositions?
a) Boston is the capital of Massachusetts.
b) Miami is the capital of Florida.
c) 2 + 3 = 5.
d) 5 + 7 = 10.
e) x + 2 = 11.
f ) Answer this question.
2. Which of these are propositions?What are the truth values
of those that are propositions?
a) Do not pass go.
b) What time is it?
c) There are no black flies in Maine.
d) 4 + x = 5.
e) The moon is made of green cheese.
f ) 2n ≥ 100.
3. What is the negation of each of these propositions?
a) Mei has an MP3 player.
b) There is no pollution in New Jersey.
c) 2 + 1 = 3.
d) The summer in Maine is hot and sunny.
4. What is the negation of each of these propositions?
a) Jennifer and Teja are friends.
b) There are 13 items in a baker’s dozen.
c) Abby sent more than 100 text messages every day.
d) 121 is a perfect square.
5. What is the negation of each of these propositions?
a) Steve has more than 100 GB free disk space on his
laptop.
b) Zach blocks e-mails and texts from Jennifer.
c) 7 · 11 · 13 = 999.
d) Diane rode her bicycle 100 miles on Sunday.
6. Suppose that SmartphoneAhas 256MBRAMand 32GB
ROM, and the resolution of its camera is 8 MP; Smartphone
B has 288 MB RAM and 64 GB ROM, and the
resolution of its camera is 4 MP; and Smartphone C has
128 MB RAM and 32 GB ROM, and the resolution of
its camera is 5 MP. Determine the truth value of each of
these propositions.
a) SmartphoneBhas the mostRAMof these three smartphones.
b) Smartphone C has more ROM or a higher resolution
camera than Smartphone B.
c) Smartphone B has more RAM, more ROM, and a
higher resolution camera than Smartphone A.
d) If Smartphone B has more RAM and more ROMthan
Smartphone C, then it also has a higher resolution
camera.
e) Smartphone A has more RAM than Smartphone B if
and only if Smartphone B has moreRAMthan Smartphone
A.
7. Suppose that during the most recent fiscal year, the annual
revenue of Acme Computer was 138 billion dollars
and its net profit was 8 billion dollars, the annual revenue
of Nadir Software was 87 billion dollars and its net profit
was 5 billion dollars, and the annual revenue of Quixote
Media was 111 billion dollars and its net profit was
13 billion dollars. Determine the truth value of each of
these propositions for the most recent fiscal year.
a) Quixote Media had the largest annual revenue.
b) Nadir Software had the lowest net profit and Acme
Computer had the largest annual revenue.
c) Acme Computer had the largest net profit or Quixote
Media had the largest net profit.
d) If Quixote Media had the smallest net profit, then
Acme Computer had the largest annual revenue.
e) Nadir Software had the smallest net profit if and only
if Acme Computer had the largest annual revenue.
8. Let p and q be the propositions
p : I bought a lottery ticket this week.
q : I won the million dollar jackpot.
Express each of these propositions as an English sentence.
a) ¬p b) p ∨ q c) p → q
d) p ∧ q e) p ↔ q f ) ¬p →¬q
g) ¬p ∧¬q h) ¬p ∨ (p ∧ q)
9. Let p and q be the propositions “Swimming at the New
Jersey shore is allowed” and “Sharks have been spotted
near the shore,” respectively. Express each of these compound
propositions as an English sentence.
a) ¬q b) p ∧ q c) ¬p ∨ q
d) p →¬q e) ¬q → p f ) ¬p →¬q
g) p ↔¬q h) ¬p ∧ (p∨ ¬q)
10. Let p and q be the propositions “The election is decided”
and “The votes have been counted,” respectively. Express
each of these compound propositions as an English sentence.
a) ¬p b) p ∨ q
c) ¬p ∧ q d) q → p
e) ¬q →¬p f ) ¬p →¬q
g) p ↔ q h) ¬q ∨ (¬p ∧ q)
11. Let p and q be the propositions
p : It is below freezing.
q : It is snowing.
Write these propositions using p and q and logical connectives
(including negations).
a) It is below freezing and snowing.
b) It is below freezing but not snowing.
c) It is not below freezing and it is not snowing.
d) It is either snowing or below freezing (or both).
e) If it is below freezing, it is also snowing.
f ) Either it is below freezing or it is snowing, but it is
not snowing if it is below freezing.
g) That it is below freezing is necessary and sufficient
for it to be snowing.
12. Let p, q, and r be the propositions
p :You have the flu.
q :You miss the final examination.
r :You pass the course.
Express each of these propositions as an English sentence.
a) p → q b) ¬q ↔ r
c) q →¬r d) p ∨ q ∨ r
e) (p →¬r) ∨ (q →¬r)
f ) (p ∧ q) ∨ (¬q ∧ r)
13. Let p and q be the propositions
p :You drive over 65 miles per hour.
q :You get a speeding ticket.
Write these propositions using p and q and logical connectives
(including negations).
a) You do not drive over 65 miles per hour.
b) You drive over 65 miles per hour, but you do not get
a speeding ticket.
c) You will get a speeding ticket if you drive over
65 miles per hour.
d) If you do not drive over 65 miles per hour, then you
will not get a speeding ticket.
e) Driving over 65 miles per hour is sufficient for getting
a speeding ticket.
f ) You get a speeding ticket, but you do not drive over
65 miles per hour.
g) Whenever you get a speeding ticket, you are driving
over 65 miles per hour.
14. Let p, q, and r be the propositions
p :You get an A on the final exam.
q :You do every exercise in this book.
r :You get an A in this class.
Write these propositions using p, q, and r and logical
connectives (including negations).
4 1 / The Foundations: Logic and Proofs
a) You get an A in this class, but you do not do every
exercise in this book.
b) You get anA on the final, you do every exercise in this
book, and you get an A in this class.
c) To get anA in this class, it is necessary for you to get
an A on the final.
d) You get an A on the final, but you don’t do every exercise
in this book; nevertheless, you get an A in this
class.
e) Getting an A on the final and doing every exercise in
this book is sufficient for getting an A in this class.
f ) You will get anA in this class if and only if you either
do every exercise in this book or you get an A on the
final.
15. Let p, q, and r be the propositions
p : Grizzly bears have been seen in the area.
q : Hiking is safe on the trail.
r : Berries are ripe along the trail.
Write these propositions using p, q, and r and logical
connectives (including negations).
a) Berries are ripe along the trail, but grizzly bears have
not been seen in the area.
b) Grizzly bears have not been seen in the area and hiking
on the trail is safe, but berries are ripe along the
trail.
c) If berries are ripe along the trail, hiking is safe if and
only if grizzly bears have not been seen in the area.
d) It is not safe to hike on the trail, but grizzly bears have
not been seen in the area and the berries along the trail
are ripe.
e) For hiking on the trail to be safe, it is necessary but not
sufficient that berries not be ripe along the trail and
for grizzly bears not to have been seen in the area.
f ) Hiking is not safe on the trail whenever grizzly bears
have been seen in the area and berries are ripe along
the trail.
16. Determine whether these biconditionals are true or
false.
a) 2 + 2 = 4 if and only if 1 + 1 = 2.
b) 1 + 1 = 2 if and only if 2 + 3 = 4.
c) 1 + 1 = 3 if and only if monkeys can fly.
d) 0 > 1 if and only if 2 > 1.
17. Determine whether each of these conditional statements
is true or false.
a) If 1 + 1 = 2, then 2 + 2 = 5.
b) If 1 + 1 = 3, then 2 + 2 = 4.
c) If 1 + 1 = 3, then 2 + 2 = 5.
d) If monkeys can fly, then 1 + 1 = 3.
18. Determine whether each of these conditional statements
is true or false.
a) If 1 + 1 = 3, then unicorns exist.
b) If 1 + 1 = 3, then dogs can fly.
c) If 1 + 1 = 2, then dogs can fly.
d) If 2 + 2 = 4, then 1 + 2 = 3.
19. For each of these sentences, determine whether an inclusive
or, or an exclusive or, is intended. Explain your
answer.
a) Coffee or tea comes with dinner.
b) A password must have at least three digits or be at
least eight characters long.
c) The prerequisite for the course is a course in number
theory or a course in cryptography.
d) You can pay using U.S. dollars or euros.
20. For each of these sentences, determine whether an inclusive
or, or an exclusive or, is intended. Explain your
answer.
a) Experience with C++ or Java is required.
b) Lunch includes soup or salad.
c) To enter the country you need a passport or a voter
registration card.
d) Publish or perish.
21. For each of these sentences, state what the sentence means
if the logical connective or is an inclusive or (that is, a disjunction)
versus an exclusive or. Which of these meanings
of or do you think is intended?
a) To take discrete mathematics, you must have taken
calculus or a course in computer science.
b) When you buy a newcar fromAcme Motor Company,
you get $2000 back in cash or a 2% car loan.
c) Dinner for two includes two items from column A or
three items from column B.
d) School is closed if more than 2 feet of snow falls or if
the wind chill is below −100.
22. Write each of these statements in the form “if p, then q”
in English. [Hint: Refer to the list of common ways to express
conditional statements provided in this section.]
a) It is necessary to wash the boss’s car to get promoted.
b) Winds from the south imply a spring thaw.
c) A sufficient condition for the warranty to be good is
that you bought the computer less than a year ago.
d) Willy gets caught whenever he cheats.
e) You can access the website only if you pay a subscription
fee.
f ) Getting elected follows from knowing the right people.
g) Carol gets seasick whenever she is on a boat.
23. Write each of these statements in the form “if p, then q”
in English. [Hint: Refer to the list of common ways to
express conditional statements.]
a) It snows whenever the wind blows from the northeast.
b) The apple trees will bloom if it stays warm for a week.
c) That the Pistons win the championship implies that
they beat the Lakers.
d) It is necessary to walk 8 miles to get to the top of
Long’s Peak.
e) To get tenure as a professor, it is sufficient to beworldfamous.
f ) If you drive more than 400 miles, you will need to buy
gasoline.
g) Your guarantee is good only if you bought your CD
player less than 90 days ago.
h) Jan will go swimming unless the water is too cold.
24. Write each of these statements in the form “if p, then q”
in English. [Hint: Refer to the list of common ways to express
conditional statements provided in this section.]
a) I will remember to send you the address only if you
send me an e-mail message.
b) To be a citizen of this country, it is sufficient that you
were born in the United States.
c) If you keep your textbook, it will be a useful reference
in your future courses.
d) The RedWings will win the Stanley Cup if their goalie
plays well.
e) That you get the job implies that you had the best
credentials.
f ) The beach erodes whenever there is a storm.
g) It is necessary to have a valid password to log on to
the server.
h) You will reach the summit unless you begin your climb
too late.
25. Write each of these propositions in the form “p if and
only if q” in English.
a) If it is hot outside you buy an ice cream cone, and if
you buy an ice cream cone it is hot outside.
b) For you to win the contest it is necessary and sufficient
that you have the only winning ticket.
c) You get promoted only if you have connections, and
you have connections only if you get promoted.
d) If youwatch television your mind will decay, and conversely.
e) The trains run late on exactly those days when I take
it.
26. Write each of these propositions in the form “p if and
only if q” in English.
a) For you to get an A in this course, it is necessary and
sufficient that you learn how to solve discrete mathematics
problems.
b) If you read the newspaper every day, you will be informed,
and conversely.
c) It rains if it is a weekend day, and it is a weekend day
if it rains.
d) You can see the wizard only if the wizard is not in,
and the wizard is not in only if you can see him.
27. State the converse, contrapositive, and inverse of each of
these conditional statements.
a) If it snows today, I will ski tomorrow.
b) I come to class whenever there is going to be a quiz.
c) A positive integer is a prime only if it has no divisors
other than 1 and itself.
28. State the converse, contrapositive, and inverse of each of
these conditional statements.
a) If it snows tonight, then I will stay at home.
b) I go to the beach whenever it is a sunny summer day.
c) When I stay up late, it is necessary that I sleep until
noon.
29. How many rows appear in a truth table for each of these
compound propositions?
a) p →¬p
b) (p ∨¬r) ∧ (q ∨¬s)
c) q ∨ p ∨¬s ∨¬r ∨¬t ∨ u
d) (p ∧ r ∧ t) ↔(q ∧ t)
30. How many rows appear in a truth table for each of these
compound propositions?
a) (q →¬p) ∨ (¬p →¬q)
b) (p ∨¬t) ∧ (p ∨¬s)
c) (p → r) ∨ (¬s →¬t) ∨ (¬u → v)
d) (p ∧ r ∧ s) ∨ (q ∧ t) ∨ (r ∧¬t)
31. Construct a truth table for each of these compound propositions.
a) p ∧¬p b) p ∨¬p
c) (p ∨¬q) → q d) (p ∨ q) → (p ∧ q)
e) (p → q) ↔ (¬q →¬p)
f ) (p → q) → (q → p)
32. Construct a truth table for each of these compound propositions.
a) p →¬p b) p ↔¬p
c) p ⊕ (p ∨ q) d) (p ∧ q) → (p ∨ q)
e) (q →¬p) ↔ (p ↔ q)
f ) (p ↔ q) ⊕ (p ↔¬q)
33. Construct a truth table for each of these compound propositions.
a) (p ∨ q) → (p ⊕ q) b) (p ⊕ q) → (p ∧ q)
c) (p ∨ q) ⊕ (p ∧ q) d) (p ↔ q) ⊕ (¬p ↔ q)
e) (p ↔ q) ⊕ (¬p ↔¬r)
f ) (p ⊕ q) → (p ⊕¬q)
34. Construct a truth table for each of these compound propositions.
a) p ⊕ p b) p ⊕¬p
c) p ⊕¬q d) ¬p ⊕¬q
e) (p ⊕ q) ∨ (p ⊕¬q) f ) (p ⊕ q) ∧ (p ⊕¬q)
35. Construct a truth table for each of these compound propositions.
a) p →¬q b) ¬p ↔ q
c) (p → q) ∨ (¬p → q) d) (p → q) ∧ (¬p → q)
e) (p ↔ q) ∨ (¬p ↔ q)
f ) (¬p ↔¬q) ↔ (p ↔ q)
36. Construct a truth table for each of these compound propositions.
a) (p ∨ q) ∨ r b) (p ∨ q) ∧ r
c) (p ∧ q) ∨ r d) (p ∧ q) ∧ r
e) (p ∨ q)∧¬r f ) (p ∧ q)∨¬r
37. Construct a truth table for each of these compound propositions.
a) p → (¬q ∨ r)
b) ¬p → (q → r)
c) (p → q) ∨ (¬p → r)
d) (p → q) ∧ (¬p → r)
e) (p ↔ q) ∨ (¬q ↔ r)
f ) (¬p ↔¬q) ↔ (q ↔ r)
38. Construct a truth table for ((p → q) → r) → s.
39. Construct a truth table for (p ↔ q) ↔ (r ↔ s).
16 1 / The Foundations: Logic and Proofs
40. Explain, without using a truth table, why (p ∨¬q) ∧
(q ∨¬r) ∧ (r ∨¬p) is true when p, q, and r have the
same truth value and it is false otherwise.
41. Explain, without using a truth table, why (p ∨ q ∨ r) ∧
(¬p ∨¬q ∨¬r) is true when at least one of p, q, and r
is true and at least one is false, but is false when all three
variables have the same truth value.
42. What is the value of x after each of these statements is
encountered in a computer program, if x = 1 before the
statement is reached?
a) if x + 2 = 3 then x := x + 1
b) if (x + 1 = 3) OR (2x + 2 = 3) then x := x + 1
c) if (2x + 3 = 5) AND (3x + 4 = 7) then x := x + 1
d) if (x + 1 = 2) XOR (x + 2 = 3) then x := x + 1
e) if x < 2 then x := x + 1
43. Find the bitwise OR, bitwise AND, and bitwise XOR of
each of these pairs of bit strings.
a) 101 1110, 010 0001
b) 1111 0000, 1010 1010
c) 00 0111 0001, 10 0100 1000
d) 11 1111 1111, 00 0000 0000
44. Evaluate each of these expressions.
a) 1 1000 ∧ (0 1011 ∨ 1 1011)
b) (0 1111 ∧ 1 0101) ∨ 0 1000
c) (0 1010 ⊕ 1 1011) ⊕ 0 1000
d) (1 1011 ∨ 0 1010) ∧ (1 0001 ∨ 1 1011)
Fuzzy logic is used in artificial intelligence. In fuzzy logic, a
proposition has a truth value that is a number between 0 and 1,
inclusive.Aproposition with a truth value of 0 is false and one
with a truth value of 1 is true. Truth values that are between 0
and 1 indicate varying degrees of truth. For instance, the truth
value 0.8 can be assigned to the statement “Fred is happy,”
because Fred is happy most of the time, and the truth value
0.4 can be assigned to the statement “John is happy,” because
John is happy slightly less than half the time. Use these truth
values to solve Exercises 45–47.
45. The truth value of the negation of a proposition in fuzzy
logic is 1 minus the truth value of the proposition. What
are the truth values of the statements “Fred is not happy”
and “John is not happy?”
46. The truth value of the conjunction of two propositions in
fuzzy logic is the minimum of the truth values of the two
propositions. What are the truth values of the statements
“Fred and John are happy” and “Neither Fred nor John is
happy?”
47. The truth value of the disjunction of two propositions in
fuzzy logic is the maximum of the truth values of the two
propositions. What are the truth values of the statements
“Fred is happy, or John is happy” and “Fred is not happy,
or John is not happy?”
∗48. Is the assertion “This statement is false” a proposition?
∗49. The nth statement in a list of 100 statements is “Exactly
n of the statements in this list are false.”
a) What conclusions can you draw from these statements?
b) Answer part (a) if the nth statement is “At least n of
the statements in this list are false.”
c) Answer part (b) assuming that the list contains 99
statements.
50. An ancient Sicilian legend says that the barber in a remote
town who can be reached only by traveling a dangerous
mountain road shaves those people, and only those people,
who do not shave themselves. Can there be such a
barber?
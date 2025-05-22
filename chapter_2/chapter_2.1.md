2.1 Sets
Introduction
In this section, we study the fundamental discrete structure on which all other discrete structures
are built, namely, the set. Sets are used to group objects together. Often, but not always, the
objects in a set have similar properties. For instance, all the students who are currently enrolled
in your school make up a set. Likewise, all the students currently taking a course in discrete
mathematics at any school make up a set. In addition, those students enrolled in your school
who are taking a course in discrete mathematics form a set that can be obtained by taking the
elements common to the first two collections. The language of sets is a means to study such
collections in an organized fashion. We now provide a definition of a set. This definition is an
intuitive definition, which is not part of a formal theory of sets.
DEFINITION 1 A set is an unordered collection of objects, called elements or members of the set. A set is
said to contain its elements.We write a ∈ A to denote that a is an element of the set A. The
notation a ∈ A denotes that a is not an element of the set A.
It is common for sets to be denoted using uppercase letters. Lowercase letters are usually
used to denote elements of sets.
There are several ways to describe a set. One way is to list all the members of a set, when
this is possible. We use a notation where all members of the set are listed between braces. For
example, the notation {a, b, c, d} represents the set with the four elements a, b, c, and d. This
way of describing a set is known as the roster method.
EXAMPLE 1 The set V of all vowels in the English alphabet can be written as V = {a, e, i, o, u}.
▲
EXAMPLE 2 The set O of odd positive integers less than 10 can be expressed by O = {1, 3, 5, 7, 9}.
▲
EXAMPLE 3 Although sets are usually used to group together elements with common properties, there is
nothing that prevents a set from having seemingly unrelated elements. For instance, {a, 2, Fred,
New Jersey} is the set containing the four elements a, 2, Fred, and New Jersey.
▲
Sometimes the roster method is used to describe a set without listing all its members. Some
members of the set are listed, and then ellipses (. . .) are used when the general pattern of the
elements is obvious.
EXAMPLE 4 The set of positive integers less than 100 can be denoted by {1, 2, 3, . . . , 99}.
▲
Another way to describe a set is to use set builder notation. We characterize all those
elements in the set by stating the property or properties they must have to be members. For
instance, the set O of all odd positive integers less than 10 can be written as
O = {x | x is an odd positive integer less than 10},
or, specifying the universe as the set of positive integers, as
O = {x ∈ Z+ | x is odd and x < 10}.
We often use this type of notation to describe sets when it is impossible to list all the elements
of the set. For instance, the set Q+ of all positive rational numbers can be written as
Q+ = {x ∈ R | x = p
q , for some positive integers p and q}.
Beware that mathematicians
disagree
whether 0 is a natural
number.We consider it
quite natural.
These sets, each denoted using a boldface letter, play an important role in discrete mathematics:
N = {0, 1, 2, 3, . . .}, the set of natural numbers
Z = {. . . ,−2,−1, 0, 1, 2, . . .}, the set of integers
Z+ = {1, 2, 3, . . .}, the set of positive integers
Q = {p/q | p ∈ Z, q ∈ Z, and q = 0}, the set of rational numbers
R, the set of real numbers
R+, the set of positive real numbers
C, the set of complex numbers.
(Note that some people do not consider 0 a natural number, so be careful to check how the term
natural numbers is used when you read other books.)
Recall the notation for intervals of real numbers. When a and b are real numbers with
a < b, we write
[a, b] = {x | a ≤ x ≤ b}
[a, b) = {x | a ≤ x < b}
(a, b] = {x |a < x ≤ b}
(a, b) = {x |a < x < b}
Note that [a, b] is called the closed interval from a to b and (a, b) is called the open interval
from a to b.
Sets can have other sets as members, as Example 5 illustrates.
EXAMPLE 5 The set {N, Z,Q,R} is a set containing four elements, each of which is a set. The four elements
of this set are N, the set of natural numbers; Z, the set of integers; Q, the set of rational numbers;
and R, the set of real numbers.
▲
Remark: Note that the concept of a datatype, or type, in computer science is built upon the
concept of a set. In particular, a datatype or type is the name of a set, together with a set of
operations that can be performed on objects from that set. For example, boolean is the name of
the set {0, 1} together with operators on one or more elements of this set, such as AND, OR,
and NOT.
Because many mathematical statements assert that two differently specified collections of
objects are really the same set, we need to understand what it means for two sets to be equal.
DEFINITION 2 Two sets are equal if and only if they have the same elements. Therefore, if A and B are sets,
then A and B are equal if and only if ∀x(x ∈ A ↔ x ∈ B).We write A = B if A and B are
equal sets.
EXAMPLE 6 The sets {1, 3, 5} and {3, 5, 1} are equal, because they have the same elements. Note that the
order in which the elements of a set are listed does not matter. Note also that it does not matter
if an element of a set is listed more than once, so {1, 3, 3, 3, 5, 5, 5, 5} is the same as the set
{1, 3, 5} because they have the same elements.
▲
GEORG CANTOR (1845–1918) Georg Cantor was born in St. Petersburg, Russia, where his father was a
successful merchant. Cantor developed his interest in mathematics in his teens. He began his university studies
in Zurich in 1862, but when his father died he left Zurich. He continued his university studies at the University
of Berlin in 1863, where he studied under the eminent mathematicians Weierstrass, Kummer, and Kronecker.
He received his doctor’s degree in 1867, after having written a dissertation on number theory. Cantor assumed
a position at the University of Halle in 1869, where he continued working until his death.
Cantor is considered the founder of set theory. His contributions in this area include the discovery that the
set of real numbers is uncountable. He is also noted for his many important contributions to analysis. Cantor
also was interested in philosophy and wrote papers relating his theory of sets with metaphysics.
Cantor married in 1874 and had five children. His melancholy temperament was balanced by his wife’s happy disposition.
Although he received a large inheritance from his father, he was poorly paid as a professor. To mitigate this, he tried to obtain a
better-paying position at the University of Berlin. His appointment there was blocked by Kronecker, who did not agree with Cantor’s
views on set theory. Cantor suffered from mental illness throughout the later years of his life. He died in 1918 from a heart attack.
THE EMPTY SET There is a special set that has no elements. This set is called the empty set,
or null set, and is denoted by ∅. The empty set can also be denoted by { } (that is, we represent
the empty set with a pair of braces that encloses all the elements in this set). Often, a set of
elements with certain properties turns out to be the null set. For instance, the set of all positive
integers that are greater than their squares is the null set.
A set with one element is called a singleton set. A common error is to confuse the empty {∅} has one more
element than ∅. set ∅ with the set {∅}, which is a singleton set. The single element of the set {∅} is the empty set
itself!A useful analogy for remembering this difference is to think of folders in a computer file
system. The empty set can be thought of as an empty folder and the set consisting of just the
empty set can be thought of as a folder with exactly one folder inside, namely, the empty folder.
NAIVE SET THEORY Note that the term object has been used in the definition of a set,
Definition 1, without specifying what an object is. This description of a set as a collection
of objects, based on the intuitive notion of an object, was first stated in 1895 by the German
mathematician Georg Cantor. The theory that results from this intuitive definition of a set, and
the use of the intuitive notion that for any property whatever, there is a set consisting of exactly
the objects with this property, leads to paradoxes, or logical inconsistencies. This was shown
by the English philosopher Bertrand Russell in 1902 (see Exercise 46 for a description of one of
these paradoxes). These logical inconsistencies can be avoided by building set theory beginning
with axioms. However, we will use Cantor’s original version of set theory, known as naive set
theory, in this book because all sets considered in this book can be treated consistently using
Cantor’s original theory. Students will find familiarity with naive set theory helpful if they go on
to learn about axiomatic set theory. They will also find the development of axiomatic set theory
much more abstract than the material in this text. We refer the interested reader to [Su72] to
learn more about axiomatic set theory.
Venn Diagrams
Sets can be represented graphically using Venn diagrams, named after the English mathematician
JohnVenn, who introduced their use in 1881. InVenn diagrams the universal set U, which
contains all the objects under consideration, is represented by a rectangle. (Note that the universal
set varies depending on which objects are of interest.) Inside this rectangle, circles or
other geometrical figures are used to represent sets. Sometimes points are used to represent the
particular elements of the set.Venn diagrams are often used to indicate the relationships between
sets.We show how a Venn diagram can be used in Example 7.
EXAMPLE 7 Draw a Venn diagram that represents V, the set of vowels in the English alphabet.
Solution:We draw a rectangle to indicate the universal set U, which is the set of the 26 letters
of the English alphabet. Inside this rectangle we draw a circle to represent V . Inside this circle
we indicate the elements of V with points (see Figure 1).
▲
U
V
a
u e
o i
FIGURE 1 Venn Diagram for the Set of Vowels.
Subsets
It is common to encounter situations where the elements of one set are also the elements of
a second set. We now introduce some terminology and notation to express such relationships
between sets.
DEFINITION 3 The set A is a subset of B if and only if every element of A is also an element of B.We use
the notation A ⊆ B to indicate that A is a subset of the set B.
We see that A ⊆ B if and only if the quantification
∀x(x ∈ A → x ∈ B)
is true. Note that to show that A is not a subset of B we need only find one element x ∈ A with
x /∈ B. Such an x is a counterexample to the claim that x ∈ A implies x ∈ B.
We have these useful rules for determining whether one set is a subset of another:
Showing that A is a Subset of B To show that A ⊆ B, show that if x belongs to A then x
also belongs to B.
Showing that A is Not a Subset of B To show that A ⊆ B, find a single x ∈ A such that
x ∈ B.
EXAMPLE 8 The set of all odd positive integers less than 10 is a subset of the set of all positive integers less
than 10, the set of rational numbers is a subset of the set of real numbers, the set of all computer
science majors at your school is a subset of the set of all students at your school, and the set of
all people in China is a subset of the set of all people in China (that is, it is a subset of itself).
Each of these facts follows immediately by noting that an element that belongs to the first set
in each pair of sets also belongs to the second set in that pair.
▲
EXAMPLE 9 The set of integers with squares less than 100 is not a subset of the set of nonnegative integers
because −1 is in the former set [as (−1)2 < 100], but not the later set. The set of people who
have taken discrete mathematics at your school is not a subset of the set of all computer science
majors at your school if there is at least one student who has taken discrete mathematics who is
not a computer science major.
▲
BERTRAND RUSSELL (1872–1970) Bertrand Russell was born into a prominent English family active in
the progressive movement and having a strong commitment to liberty. He became an orphan at an early age
and was placed in the care of his father’s parents, who had him educated at home. He entered Trinity College,
Cambridge, in 1890, where he excelled in mathematics and in moral science. He won a fellowship on the basis
of his work on the foundations of geometry. In 1910 Trinity College appointed him to a lectureship in logic and
the philosophy of mathematics.
Russell fought for progressive causes throughout his life. He held strong pacifist views, and his protests
against World War I led to dismissal from his position at Trinity College. He was imprisoned for 6 months in
1918 because of an article he wrote that was branded as seditious. Russell fought for women’s suffrage in Great
Britain. In 1961, at the age of 89, he was imprisoned for the second time for his protests advocating nuclear disarmament.
Russell’s greatest work was in his development of principles that could be used as a foundation for all of mathematics. His
most famous work is Principia Mathematica, written with Alfred North Whitehead, which attempts to deduce all of mathematics
using a set of primitive axioms. He wrote many books on philosophy, physics, and his political ideas. Russell won the Nobel Prize
for literature in 1950.
U
A B
FIGURE 2 Venn Diagram Showing that A Is a Subset of B.
Theorem 1 shows that every nonempty set S is guaranteed to have at least two subsets, the
empty set and the set S itself, that is, ∅ ⊆ S and S ⊆ S.
THEOREM 1 For every set S, (i ) ∅ ⊆ S and (ii ) S ⊆ S.
Proof:We will prove (i ) and leave the proof of (ii ) as an exercise.
Let S be a set. To show that∅ ⊆ S, we must show that ∀x(x ∈ ∅ → x ∈ S) is true. Because
the empty set contains no elements, it follows that x ∈ ∅ is always false. It follows that the
conditional statement x ∈ ∅ → x ∈ S is always true, because its hypothesis is always false and
a conditional statement with a false hypothesis is true. Therefore, ∀x(x ∈ ∅ → x ∈ S) is true.
This completes the proof of (i). Note that this is an example of a vacuous proof.
When we wish to emphasize that a set A is a subset of a set B but that A = B, we write
A ⊂ B and say that A is a proper subset of B. For A ⊂ B to be true, it must be the case that
A ⊆ B and there must exist an element x of B that is not an element of A. That is, A is a proper
subset of B if and only if
∀x(x ∈ A → x ∈ B) ∧ ∃x(x ∈ B ∧ x ∈ A)
is true. Venn diagrams can be used to illustrate that a set A is a subset of a set B. We draw the
universal set U as a rectangle.Within this rectangle we draw a circle for B. Because A is a subset
of B, we draw the circle for A within the circle for B. This relationship is shown in Figure 2.
A useful way to show that two sets have the same elements is to show that each set is a
subset of the other. In other words, we can show that if A and B are sets with A ⊆ B and B ⊆ A,
then A = B. That is, A = B if and only if ∀x(x ∈ A → x ∈ B) and ∀x(x ∈ B → x ∈ A) or
equivalently if and only if ∀x(x ∈ A ↔ x ∈ B), which is what it means for the A and B to be
equal. Because this method of showing two sets are equal is so useful, we highlight it here.
JOHN VENN (1834–1923) John Venn was born into a London suburban family noted for its philanthropy.
He attended London schools and got his mathematics degree from Caius College, Cambridge, in 1857. He was
elected a fellow of this college and held his fellowship there until his death. He took holy orders in 1859 and,
after a brief stint of religious work, returned to Cambridge, where he developed programs in the moral sciences.
Besides his mathematical work, Venn had an interest in history and wrote extensively about his college and
family.
Venn’s book Symbolic Logic clarifies ideas originally presented by Boole. In this book, Venn presents a
systematic development of a method that uses geometric figures, known now as Venn diagrams. Today these
diagrams are primarily used to analyze logical arguments and to illustrate relationships between sets. In addition
to his work on symbolic logic,Venn made contributions to probability theory described in his widely used textbook on that subject.
Showing Two Sets are Equal To show that two sets A and B are equal, show that A ⊆ B
and B ⊆ A.
Sets may have other sets as members. For instance, we have the sets
A = {∅, {a}, {b}, {a, b}} and B = {x | x is a subset of the set {a, b}}.
Note that these two sets are equal, that is, A = B. Also note that {a} ∈ A, but a /∈ A.
The Size of a Set
Sets are used extensively in counting problems, and for such applications we need to discuss
the sizes of sets.
DEFINITION 4 Let S be a set. If there are exactly n distinct elements in S where n is a nonnegative integer,
we say that S is a finite set and that n is the cardinality of S. The cardinality of S is denoted
by |S|.
Remark: The term cardinality comes from the common usage of the term cardinal number as
the size of a finite set.
EXAMPLE 10 Let A be the set of odd positive integers less than 10. Then |A| = 5.
▲
EXAMPLE 11 Let S be the set of letters in the English alphabet. Then |S| = 26.
▲
EXAMPLE 12 Because the null set has no elements, it follows that |∅| = 0.
▲
We will also be interested in sets that are not finite.
DEFINITION 5 A set is said to be infinite if it is not finite.
EXAMPLE 13 The set of positive integers is infinite.
▲
We will extend the notion of cardinality to infinite sets in Section 2.5, a challenging topic
full of surprising results.
Power Sets
Many problems involve testing all combinations of elements of a set to see if they satisfy some
property. To consider all such combinations of elements of a set S, we build a new set that has
as its members all the subsets of S.
DEFINITION 6 Given a set S, the power set of S is the set of all subsets of the set S. The power set of S is
denoted by P(S).
EXAMPLE 14 What is the power set of the set {0, 1, 2}?
Solution: The power set P({0, 1, 2}) is the set of all subsets of {0, 1, 2}. Hence,
P({0, 1, 2}) = {∅, {0}, {1}, {2}, {0, 1}, {0, 2}, {1, 2}, {0, 1, 2}}.
Note that the empty set and the set itself are members of this set of subsets.
▲
EXAMPLE 15 What is the power set of the empty set? What is the power set of the set {∅}?
Solution: The empty set has exactly one subset, namely, itself. Consequently,
P(∅) = {∅}.
The set {∅} has exactly two subsets, namely, ∅ and the set {∅} itself. Therefore,
P({∅}) = {∅, {∅}}.
▲
If a set has n elements, then its power set has 2n elements. We will demonstrate this fact in
several ways in subsequent sections of the text.
Cartesian Products
The order of elements in a collection is often important. Because sets are unordered, a different
structure is needed to represent ordered collections. This is provided by ordered n-tuples.
DEFINITION 7 The ordered n-tuple (a1, a2, . . . , an) is the ordered collection that has a1 as its first element,
a2 as its second element, . . . , and an as its nth element.
We say that two ordered n-tuples are equal if and only if each corresponding pair of their
elements is equal. In other words, (a1, a2, . . . , an) = (b1, b2, . . . , bn) if and only if ai = bi ,
for i = 1, 2, . . . , n. In particular, ordered 2-tuples are called ordered pairs. The ordered pairs
(a, b) and (c, d) are equal if and only if a = c and b = d. Note that (a, b) and (b, a) are not
equal unless a = b.
RENÉ DESCARTES (1596–1650) René Descartes was born into a noble family near Tours, France, about
200 miles southwest of Paris. He was the third child of his father’s first wife; she died several days after his
birth. Because of René’s poor health, his father, a provincial judge, let his son’s formal lessons slide until, at
the age of 8, René entered the Jesuit college at La Flèche. The rector of the school took a liking to him and
permitted him to stay in bed until late in the morning because of his frail health. From then on, Descartes spent
his mornings in bed; he considered these times his most productive hours for thinking.
Descartes left school in 1612, moving to Paris, where he spent 2 years studying mathematics. He earned
a law degree in 1616 from the University of Poitiers. At 18 Descartes became disgusted with studying and
decided to see the world. He moved to Paris and became a successful gambler. However, he grew tired
of bawdy living and moved to the suburb of Saint-Germain, where he devoted himself to mathematical study. When his gambling
friends found him, he decided to leave France and undertake a military career. However, he never did any fighting. One day, while
escaping the cold in an overheated room at a military encampment, he had several feverish dreams, which revealed his future career
as a mathematician and philosopher.
After ending his military career, he traveled throughout Europe. He then spent several years in Paris, where he studied mathematics
and philosophy and constructed optical instruments. Descartes decided to move to Holland, where he spent 20 years wandering
around the country, accomplishing his most important work. During this time he wrote several books, including the Discours, which
contains his contributions to analytic geometry, for which he is best known. He also made fundamental contributions to philosophy.
In 1649 Descartes was invited by Queen Christina to visit her court in Sweden to tutor her in philosophy. Although he was
reluctant to live in what he called “the land of bears amongst rocks and ice,” he finally accepted the invitation and moved to Sweden.
Unfortunately, the winter of 1649–1650 was extremely bitter. Descartes caught pneumonia and died in mid-February.
Many of the discrete structures we will study in later chapters are based on the notion of the
Cartesian product of sets (named after René Descartes). We first define the Cartesian product
of two sets.
DEFINITION 8 Let A and B be sets. The Cartesian product of A and B, denoted by A × B, is the set of all
ordered pairs (a, b), where a ∈ A and b ∈ B. Hence,
A × B = {(a, b) | a ∈ A ∧ b ∈ B}.
EXAMPLE 16 Let A represent the set of all students at a university, and let B represent the set of all courses
offered at the university. What is the Cartesian product A × B and how can it be used?
Solution: The Cartesian product A × B consists of all the ordered pairs of the form (a, b), where
a is a student at the university and b is a course offered at the university. One way to use the set
A × B is to represent all possible enrollments of students in courses at the university.
▲
EXAMPLE 17 What is the Cartesian product of A = {1, 2} and B = {a, b, c}?
Solution: The Cartesian product A × B is
A × B = {(1, a), (1, b), (1, c), (2, a), (2, b), (2, c)}.
▲ Note that the Cartesian products A
×
B
and B
×
A
are not equal, unless A
=
∅
or B
=
∅
(so that A × B = ∅) or A = B (see Exercises 31 and 38). This is illustrated in Example 18.
EXAMPLE 18 Show that the Cartesian product B × A is not equal to the Cartesian product A × B, where A
and B are as in Example 17.
Solution: The Cartesian product B × A is
B × A = {(a, 1), (a, 2), (b, 1), (b, 2), (c, 1), (c, 2)}.
This is not equal to A × B, which was found in Example 17.
▲
The Cartesian product of more than two sets can also be defined.
DEFINITION 9 The Cartesian product of the sets A1,A2, . . . , An, denoted by A1 × A2 ×· · ·×An, is the
set of ordered n-tuples (a1, a2, . . . , an), where ai belongs to Ai for i = 1, 2, . . . , n. In other
words,
A1 × A2 ×· · ·×An = {(a1, a2, . . . , an) | ai ∈ Ai for i = 1, 2, . . . , n}.
EXAMPLE 19 What is the Cartesian product A × B × C, where A = {0, 1}, B = {1, 2}, and C = {0, 1, 2} ?
Solution: The Cartesian productA × B × C consists of all ordered triples (a, b, c), where a ∈ A,
b ∈ B, and c ∈ C. Hence,
A × B × C = {(0, 1, 0), (0, 1, 1), (0, 1, 2), (0, 2, 0), (0, 2, 1), (0, 2, 2),
(1, 1, 0), (1, 1, 1), (1, 1, 2), (1, 2, 0), (1, 2, 1), (1, 2, 2)}.
▲
Remark: Note that when A, B, and C are sets, (A × B) × C is not the same as A × B × C (see
Exercise 39).
We use the notation A2 to denote A × A, the Cartesian product of the set A with itself.
Similarly, A3 = A × A × A, A4 = A × A × A × A, and so on. More generally,
An = {(a1, a2, . . . , an) | ai ∈ A for i = 1, 2, . . . , n}.
EXAMPLE 20 Suppose that A = {1, 2}. It follows that A2 = {(1, 1), (1, 2), (2, 1), (2, 2)} and A3 =
{(1, 1, 1), (1, 1, 2), (1, 2, 1), (1, 2, 2), (2, 1, 1), (2, 1, 2), (2, 2, 1), (2, 2, 2)}.
▲
A subset R of the Cartesian product A × B is called a relation from the set A to the set
B. The elements of R are ordered pairs, where the first element belongs to A and the second
to B. For example, R = {(a, 0), (a, 1), (a, 3), (b, 1), (b, 2), (c, 0), (c, 3)} is a relation from the
set {a, b, c} to the set {0, 1, 2, 3}. A relation from a set A to itself is called a relation on A.
EXAMPLE 21 What are the ordered pairs in the less than or equal to relation, which contains (a, b) if a ≤ b,
on the set {0, 1, 2, 3}?
Solution: The ordered pair (a, b) belongs to R if and only if both a and b belong to {0, 1, 2, 3}
and a ≤ b. Consequently, the ordered pairs in R are (0,0), (0,1), (0,2), (0,3), (1,1), (1,2), (1,3),
(2,2), (2, 3), and (3, 3). ▲
We will study relations and their properties at length in Chapter 9.
Using Set Notation with Quantifiers
Sometimes we restrict the domain of a quantified statement explicitly by making use of a
particular notation. For example, ∀x∈S(P(x)) denotes the universal quantification of P(x)
over all elements in the set S. In other words, ∀x∈S(P(x)) is shorthand for ∀x(x ∈ S → P(x)).
Similarly, ∃x∈S(P(x)) denotes the existential quantification of P(x) over all elements in S.
That is, ∃x∈S(P(x)) is shorthand for ∃x(x ∈ S ∧ P(x)).
EXAMPLE 22 What do the statements ∀x∈R (x2 ≥ 0) and ∃x∈Z (x2 = 1) mean?
Solution: The statement ∀x∈R(x2 ≥ 0) states that for every real number x, x2 ≥ 0. This statement
can be expressed as “The square of every real number is nonnegative.” This is a true
statement.
The statement ∃x∈Z(x2 = 1) states that there exists an integer x such that x2 = 1. This
statement can be expressed as “There is an integer whose square is 1.” This is also a true statement
because x = 1 is such an integer (as is −1).
Truth Sets and Quantifiers
We will now tie together concepts from set theory and from predicate logic. Given a predicate
P, and a domain D, we define the truth set of P to be the set of elements x in D for which
P(x) is true. The truth set of P(x) is denoted by {x ∈ D | P(x)}.
EXAMPLE 23 What are the truth sets of the predicates P(x), Q(x), and R(x), where the domain is the set of
integers and P(x) is “|x| = 1,” Q(x) is “x2 = 2,” and R(x) is “|x| = x.”
Solution: The truth set of P, {x ∈ Z | |x| = 1}, is the set of integers for which |x| = 1. Because
|x| = 1 when x = 1 or x = −1, and for no other integers x, we see that the truth set of P is the
set {−1, 1}.
The truth set of Q, {x ∈ Z | x2 = 2}, is the set of integers for which x2 = 2. This is the
empty set because there are no integers x for which x2 = 2.
The truth set of R, {x ∈ Z | |x| = x}, is the set of integers for which |x| = x. Because
|x| = x if and only if x ≥ 0, it follows that the truth set of R is N, the set of nonnegative
integers.
▲
Note that ∀xP(x) is true over the domain U if and only if the truth set of P is the set U.
Likewise, ∃xP(x) is true over the domain U if and only if the truth set of P is nonempty.
Exercises
1. List the members of these sets.
a) {x | x is a real number such that x2 = 1}
b) {x | x is a positive integer less than 12}
c) {x | x is the square of an integer and x < 100}
d) {x | x is an integer such that x2 = 2}
2. Use set builder notation to give a description of each of
these sets.
a) {0, 3, 6, 9, 12}
b) {−3,−2,−1, 0, 1, 2, 3}
c) {m, n, o, p}
3. For each of these pairs of sets, determine whether the first
is a subset of the second, the second is a subset of the first,
or neither is a subset of the other.
a) the set of airline flights from NewYork to New Delhi,
the set of nonstop airline flights from New York to
New Delhi
b) the set of people who speak English, the set of people
who speak Chinese
c) the set of flying squirrels, the set of living creatures
that can fly
4. For each of these pairs of sets, determine whether the first
is a subset of the second, the second is a subset of the first,
or neither is a subset of the other.
a) the set of people who speak English, the set of people
who speak English with an Australian accent
b) the set of fruits, the set of citrus fruits
c) the set of students studying discrete mathematics, the
set of students studying data structures
5. Determine whether each of these pairs of sets are equal.
a) {1, 3, 3, 3, 5, 5, 5, 5, 5}, {5, 3, 1}
b) {{1}}, {1, {1}} c) ∅, {∅}
6. Suppose that A = {2, 4, 6}, B = {2, 6}, C = {4, 6}, and
D = {4, 6, 8}. Determine which of these sets are subsets
of which other of these sets.
7. For each of the following sets, determine whether 2 is an
element of that set.
a) {x ∈ R | x is an integer greater than 1}
b) {x ∈ R | x is the square of an integer}
c) {2,{2}} d) {{2},{{2}}}
e) {{2},{2,{2}}} f ) {{{2}}}
8. For each of the sets in Exercise 7, determine whether {2}
is an element of that set.
9. Determine whether each of these statements is true or
false.
a) 0 ∈ ∅ b) ∅ ∈ {0}
c) {0} ⊂ ∅ d) ∅ ⊂ {0}
e) {0} ∈ {0} f ) {0} ⊂ {0}
g) {∅} ⊆ {∅}
10. Determine whether these statements are true or false.
a) ∅ ∈ {∅} b) ∅ ∈ {∅, {∅}}
c) {∅} ∈ {∅} d) {∅} ∈ {{∅}}
e) {∅} ⊂ {∅, {∅}} f ) {{∅}} ⊂ {∅, {∅}}
g) {{∅}} ⊂ {{∅}, {∅}}
11. Determine whether each of these statements is true or
false.
a) x ∈ {x} b) {x} ⊆ {x} c) {x} ∈ {x}
d) {x} ∈ {{x}} e) ∅ ⊆ {x} f ) ∅ ∈ {x}
12. Use aVenn diagram to illustrate the subset of odd integers
in the set of all positive integers not exceeding 10.
13. Use a Venn diagram to illustrate the set of all months of
the year whose names do not contain the letter R in the
set of all months of the year.
14. Use a Venn diagram to illustrate the relationship A ⊆ B
and B ⊆ C.
15. Use aVenn diagram to illustrate the relationships A ⊂ B
and B ⊂ C.
16. Use aVenn diagram to illustrate the relationships A ⊂ B
and A ⊂ C.
17. Suppose that A,B, and C are sets such that A ⊆ B and
B ⊆ C. Show that A ⊆ C.
18. Find two sets A and B such that A ∈ B and A ⊆ B.
19. What is the cardinality of each of these sets?
a) {a} b) {{a}}
c) {a, {a}} d) {a, {a}, {a, {a}}}
20. What is the cardinality of each of these sets?
a) ∅ b) {∅}
c) {∅, {∅}} d) {∅, {∅}, {∅, {∅}}}
21. Find the power set of each of these sets, where a and b
are distinct elements.
a) {a} b) {a, b} c) {∅, {∅}}
22. Can you conclude that A = B if A and B are two sets
with the same power set?
23. How many elements does each of these sets have where
a and b are distinct elements?
a) P({a, b, {a, b}})
b) P({∅, a, {a}, {{a}}})
c) P(P(∅))
24. Determine whether each of these sets is the power set of
a set, where a and b are distinct elements.
a) ∅ b) {∅, {a}}
c) {∅, {a}, {∅, a}} d) {∅, {a}, {b}, {a, b}}
25. Prove that P(A) ⊆ P(B) if and only if A ⊆ B.
26. Show that if A ⊆ C and B ⊆ D, then A × B ⊆ C × D
27. Let A = {a, b, c, d} and B = {y, z}. Find
a) A × B. b) B × A.
28. What is the Cartesian product A × B, where A is the set
of courses offered by the mathematics department at a
university and B is the set of mathematics professors at
this university? Give an example of how this Cartesian
product can be used.
29. What is the Cartesian product A × B × C, where A is
the set of all airlines and B and C are both the set of all
cities in the United States? Give an example of how this
Cartesian product can be used.
30. Suppose that A × B = ∅, where A and B are sets. What
can you conclude?
31. Let A be a set. Show that ∅×A = A×∅ = ∅.
32. Let A = {a, b, c}, B = {x, y}, and C = {0, 1}. Find
a) A × B × C. b) C × B × A.
c) C × A × B. d) B × B × B.
33. Find A2 if
a) A = {0, 1, 3}. b) A = {1, 2, a, b}.
34. Find A3 if
a) A = {a}. b) A = {0, a}.
35. How many different elements does A × B have if A has
m elements and B has n elements?
36. How many different elements does A × B × C have if A
hasmelements, B has n elements, and C has p elements?
37. How many different elements does An have when A has
m elements and n is a positive integer?
38. ShowthatA × B = B × A, whenAandB are nonempty,
unless A = B.
39. Explain why A × B × C and (A × B) × C are not the
same.
40. Explain why (A × B) × (C × D) and A × (B × C) ×
D are not the same.
41. Translate each of these quantifications into English and
determine its truth value.
a) ∀x∈R (x2 = −1) b) ∃x∈Z (x2 = 2)
c) ∀x∈Z (x2 > 0) d) ∃x∈R (x2 = x)
42. Translate each of these quantifications into English and
determine its truth value.
a) ∃x∈R (x3 = −1) b) ∃x∈Z (x + 1 > x)
c) ∀x∈Z (x − 1 ∈ Z) d) ∀x∈Z (x2 ∈ Z)
43. Find the truth set of each of these predicates where the
domain is the set of integers.
a) P(x): x2 < 3 b) Q(x): x2 > x
c) R(x): 2x + 1 = 0
44. Find the truth set of each of these predicates where the
domain is the set of integers.
a) P(x): x3 ≥ 1 b) Q(x): x2 = 2
c) R(x): x < x2
∗45. The defining property of an ordered pair is that two ordered
pairs are equal if and only if their first elements
are equal and their second elements are equal. Surprisingly,
instead of taking the ordered pair as a primitive concept,
we can construct ordered pairs using basic notions
from set theory. Show that if we define the ordered pair
(a, b) to be {{a}, {a, b}}, then (a, b) = (c, d) if and only
if a = c and b = d. [Hint: First show that {{a}, {a, b}} =
{{c}, {c, d}} if and only if a = c and b = d.]
∗46. This exercise presents Russell’s paradox. Let S be the
set that contains a set x if the set x does not belong to
itself, so that S = {x | x /∈ x}.
a) Show the assumption that S is a member of S leads to
a contradiction.
b) Showthe assumption that S is not a member of S leads
to a contradiction.
By parts (a) and (b) it follows that the set S cannot be defined
as it was. This paradox can be avoided by restricting
the types of elements that sets can have.
∗47. Describe a procedure for listing all the subsets of a finite
set.
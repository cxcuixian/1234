# Munger-Style Math Learning

## Study Strategy

如果把“芒格会怎样学数学书”理解为一种 **Munger-style reconstruction**（不是他公开的固定课程），他不会从头到尾线性读完，而会把数学变成一张可迁移的“思维模型网络”。

### 1. 把《数学伴侣》当地图，不当教材

对 [[2/2a-math/The Princeton Companion to Mathematics.md]]：

- 先读 Part I，建立总地图：
  - 集合、函数、关系、逻辑
  - 数、群、域、向量空间、环
  - 极限、连续、微分、积分
  - 代数、几何、分析、概率、数论
- Part II 用来理解：这些概念为什么被发明。
- Part III 当作参考百科，不必线性通读。
- 每次只选择一条主线深入。

### 2. 只保留“一本主教材 + 一本题书 + 一本地图书”

不要收藏十本相似的书：

1. 一本循序渐进的主教材；
2. 一本有大量题目的练习书；
3. 《数学伴侣》作为地图、背景和查阅工具。

真正的学习发生在“解释和解题”，不是阅读数量。

### 3. 每个概念都问七个问题

读完一小节后，合上书回答：

1. 它要解决什么问题？
2. 基本对象是什么？
3. 允许进行哪些操作？
4. 哪些假设不可缺少？
5. 最简单的例子是什么？
6. 反例是什么？
7. 如果去掉一个假设，会发生什么？

例如学习函数时，不只记住定义，还要理解：

- domain 和 range；
- injection、surjection、bijection 的区别；
- 为什么只有双射才有真正的逆函数；
- 一个函数在哪些条件下不能被逆转。

### 4. 用“反转思考”学习证明

每个定理都从相反方向问：

- 结论为什么可能失败？
- 哪个条件最关键？
- 有没有看似相同但不成立的例子？
- 这个定理能否推广？
- 有没有更短、更结构化的证明？

数学中尤其要注意这些边界：

- equality vs. inequality；
- finite vs. infinite；
- necessary vs. sufficient；
- intuition vs. proof；
- algebraic formula vs. analytic estimate。

### 5. 采用“读—合上—重建—应用”循环

每次只处理 5–10 页：

1. 阅读并标记主线；
2. 合上书，用自己的话解释；
3. 重画定义和定理之间的关系；
4. 独立重建一个证明或推导；
5. 解 2–3 道题；
6. 自己造一个例子和一个反例；
7. 记录错误，而不是只记录漂亮的结论。

可以用这个笔记模板：

```text
概念：
它解决的问题：
基本对象：
关键假设：
最简单例子：
反例：
证明/推导骨架：
去掉假设后会怎样：
与哪些概念相连：
我做错的地方：
```

### 6. 推荐学习顺序

```text
集合、函数、逻辑
→ 数系
→ 线性代数
→ 极限与微积分
→ 概率与组合
→ 数论、抽象代数、几何
```

这条顺序不是为了“学完数学”，而是为了建立一组可复用的模型：结构、映射、对称性、极限、计数、证明和不变量。

### 7. 判断是否真的学会

不要用“读了多少页”衡量，而要检查：

- 能否不看书解释概念；
- 能否指出适用条件；
- 能否解决表面不同的新问题；
- 能否构造反例；
- 一周后能否重新调用。

一句话总结：

> 芒格式学数学，不是积累公式，而是寻找少数深层结构，并不断用例子、反例和问题验证它们。

## Learning Log

### Lesson 1: Functions（函数）

我们从 [[2/2a-math/The Princeton Companion to Mathematics.md]] 的 **I.2 §2.2 Functions** 开始。

#### Munger-Style Approach

今天只学一个高杠杆模型：

> **函数 = 把一个对象转换成另一个对象的规则。**

不要先背定义。先问：

**它解决什么问题？**
数学中有大量过程：加 4、开平方、取余数、计算重心。把这些过程当作“对象”，我们就能比较它们、组合它们、研究它们是否可以逆转。

#### Core Definition

函数
$$
f:A\to B
$$
表示：
- 每一个 $x\in A$；
- 都对应唯一的 $f(x)\in B$。

其中：
- $A$：domain，定义域；
- $B$：codomain，陪域；
- 实际被用到的输出集合：image，像集。

#### Key Properties

1. **Injective（单射）**
   不同输入不会得到相同输出, diferent input get different output 
$$
x\neq y\Rightarrow f(x)\neq f(y)
$$

2. **Surjective（满射）**
   陪域中的每一个元素都被击中。every ouput have input

3. **Bijective（双射）**
   同时是单射和满射，因此存在真正的逆函数。bijective=injective+surjective

#### Examples

##### Example 1

$$
f(x)=x+4,\quad f:\mathbb Z\to\mathbb Z
$$
它是双射，逆函数是：
$$
f^{-1}(y)=y-4
$$

##### Example 2

$$
f(x)=2x,\quad f:\mathbb Z\to\mathbb Z
$$
它是单射，但不是满射，因为奇数永远不会出现。

##### Example 3

$$
f(x)=x^2,\quad f:\mathbb R\to\mathbb R
$$
它既不是单射，也不是满射：
- $f(1)=f(-1)$，所以不是单射；
- 没有任何实数 $x$ 能使 $x^2=-1$，所以不是满射。

但如果改成：
$$
f:[0,\infty)\to[0,\infty),\quad f(x)=x^2
$$
它就变成双射，可以有逆函数：
$$
f^{-1}(y)=\sqrt y
$$
这说明一个芒格式问题：

> **同一个规则，改变定义域或陪域，性质可能完全改变。**

#### Closed-Book Retrieval Practice

1. $f(x)=x^2,\ f:\mathbb Z\to\mathbb Z$ 是单射吗？满射吗？为什么？
   - No, $-x$ and $x$ have the same results
   - Yes, $f(x) \in \mathbb R$， every element can attained
2. $f(x)=3x-7,\ f:\mathbb R\to\mathbb R$ 是双射吗？它的逆函数是什么？
   - yes，$f^{-1}(y)=\frac{1}{3}(y+7)$
3. 为什么“定义域和陪域”不能被忽略？
   - If ignore, some function will be wrong, domain example: $f(x)=\sqrt{ x },x<0$, codomain example: $y=e^x, y<0$
4. 如果一个函数不是单射，逆转时会出现什么问题？
   - one function will have more than one solution values
5. 请自己举一个“单射但不是满射”的例子。
   - $f(x)=2x,x=2k,k\in \mathbb Z$

---
1. **$f(x)=x^2,\ f:\mathbb Z\to\mathbb Z$**
   1. **Not injective:** $f(1)=f(-1)=1$.
   2. **Not surjective:** no integer input produces $-1$, for example. The codomain is $\mathbb Z$, not $\mathbb R$; and even being in the codomain wouldn’t prove every value is attained.
2. $f(x)=3x-7,\ f:\mathbb R\to\mathbb R$
   Correct: it’s bijective, and  $f^{-1}(y)=\frac{y+7}{3}$.
3. **Domain and codomain**  Your examples point toward the right issue, but need adjustment:
   1. For real-valued $\sqrt{x}$, negative inputs are invalid, so use $f:[0,\infty)\to[0,\infty)$, $f(x)=\sqrt{x}$.
   2. $e^x$ is always positive. So $e^x:\mathbb R\to(0,\infty)$ is onto, while $e^x:\mathbb R\to\mathbb R$ is not onto. Declaring its codomain to be negative numbers would make it **not a valid function into that codomain**.
   3. The same rule can have different properties when its domain or codomain changes.
4. **If a function isn’t injective**
   1. Right idea: an output can come from multiple inputs, so reversing it gives multiple answers—not a function. For example, $x^2=1$ gives $x=1$ or $x=-1$.
5. **Injective but not surjective**
   1. Your example works if you specify it as $f:2\mathbb Z\to\mathbb Z$, $f(x)=2x$: it’s injective, but its outputs are multiples of 4, so it misses (for example) 1. A simpler standard example is $f:\mathbb Z\to\mathbb Z,\ f(n)=2n$: it misses all odd integers.

**Key correction to keep:** *Injective asks whether two inputs can share an output. Surjective asks whether every element of the stated codomain is reached.*

**Retrieval-practice note:** The first five questions were answered closed-book; corrections follow.

### Lesson 2: Relations

We continue in book order with [[2/2a-math/The Princeton Companion to Mathematics.md#2.3 Relations|I.2 §2.3: Relations]]. The learning move is to define the relation, test it on examples, and look for where its properties break.

*Quick check from the last exercise:* $e^x$ has image $(0,\infty)$. It’s injective, but not onto $[0,\infty)$, because it never reaches 0.

#### What Is a Relation?

A **function** assigns exactly one output to every input. A **relation** is more flexible: it tells us whether a pair of objects is related. A given object might be related to no others, one other, or many.

For example, $<$ is a relation on the integers. Since $4<5$, the pair $(4,5)$ is related. But 4 is less than many integers—5, 6, 7, …—so $<$ isn’t a function that gives each input exactly one output.

Formally, a relation from $A$ to $B$ is a collection of pairs from $A\times B$. A function is a special kind of relation: for each input, it pairs that input with **exactly one** output.

#### Equivalence Relations

Sometimes we want to treat different objects as equivalent under a chosen criterion. For example, integers that leave the same remainder when divided by 3 are equivalent **modulo 3**:
$$
a\sim b \quad\text{if and only if}\quad a-b\text{ is divisible by }3.
$$

This is an **equivalence relation** if it passes three tests:
- **Self:** $a\sim a$.
- **Reverse:** if $a\sim b$, then $b\sim a$.
- **Chain:** if $a\sim b$ and $b\sim c$, then $a\sim c$.

For modulo 3, all three work:
- $a-a=0$, which is divisible by 3.
- Reversing $a-b$ just changes its sign, so divisibility by 3 is preserved.
- Adding two differences divisible by 3 gives another difference divisible by 3.

This groups all integers into three **equivalence classes**: those with remainder 0, 1, or 2. For example, $2$ belongs to the class $\{\ldots,-4,-1,2,5,8,\ldots\}$.

##### Counterexamples

The relation $<$ on positive integers is **transitive**, but it fails the other tests: $2<2$ is false, and $2<3$ doesn’t imply $3<2$. So it isn’t an equivalence relation.

A relation can even pass “self” and “reverse” but fail “chain.” On integers, define $a\sim b$ to mean $|a-b|\leq 1$. Then $0\sim1$ and $1\sim2$, but $0\not\sim2$.

#### Practice: Parity

On the integers, define $a\sim b$ to mean **$a$ and $b$ have the same parity**.

Does this relation pass the self, reverse, and chain tests? What are its equivalence classes?

The question means: **group all integers into “even” and “odd,” then check whether “has the same parity” follows three simple rules.**

---
“Same parity” means both numbers are even or both are odd. For example, $2\sim 8$, because both are even; $3\not\sim 8$, because one is odd and the other is even.

- **Self:** Is every number the same parity as itself? Yes. For example, $5\sim5$.
- **Reverse:** If $a$ has the same parity as $b$, does $b$ have the same parity as $a$? Yes.
- **Chain:** If $a$ has the same parity as $b$, and $b$ as $c$, must $a$ and $c$ have the same parity? Yes. For example, if $a$ and $b$ are both even, and $b$ and $c$ are both even, then $a$ and $c$ are even too.

So it passes all three tests and is an **equivalence relation**.

An **equivalence class** is the group of numbers equivalent to a chosen number. There are two groups:

- The even integers: $\{\ldots,-4,-2,0,2,4,\ldots\}$
- The odd integers: $\{\ldots,-3,-1,1,3,5,\ldots\}$

For instance, 6 belongs to the even group, and $-5$ belongs to the odd group.

---

### Lesson 3: Binary Operations

In [[2/2a-math/The Princeton Companion to Mathematics.md#2.4 Binary Operations|I.2 §2.4]], the book moves from **relations** to **operations**.

Compare these two parts of $2+3=5$:
- $+$ takes two numbers and **produces** another number: $2+3=5$. That’s an operation.
- $=$ checks whether two numbers are **equal**. That’s a relation.

A **binary operation** takes two elements from a set and returns one element of that same set. “Binary” means it has two inputs. For example, addition on the integers works:

$$
+:\mathbb Z\times\mathbb Z\to\mathbb Z
$$

#### Closure: Does the Result Stay in the Set?

The important boundary check is: **does every allowed pair produce an answer that stays in the set?**

Subtraction works on the integers: $3-5=-2$, and $-2$ is an integer. But subtraction is **not** a binary operation on the positive integers: $3-5=-2$, which is not positive.

#### Commutativity and Associativity

- **Commutative:** swap the inputs. Does the answer stay the same?
  Addition: $2+5=5+2$.
  Subtraction: $2-5\ne5-2$.

- **Associative:** change the grouping. Does the answer stay the same?
  Addition: $(2+5)+3=2+(5+3)$.
  Subtraction: $(9-5)-3=1$, but $9-(5-3)=7$.

**Munger-style check:** test the boundaries and try to break the claim. One pair whose result leaves the set disproves that it’s a binary operation on that set; one counterexample disproves commutativity or associativity.

**Your turn—one question:** On the positive integers, is subtraction a binary operation? Use $3-5$ to decide.
**Your answer:** No. $3-5=-2$, so $-2$ is not positive.

---
Exactly. You used the **closure test**: if even one allowed pair gives a result outside the set, subtraction isn’t a binary operation on the positive integers.

#### Identity and Inverse

For an operation, an **identity** is the “do nothing” value:

- With addition, $0$ is the identity: $x+0=x$.
- With multiplication, $1$ is the identity: $x\cdot1=x$.

An **inverse** is a value that undoes another value, returning the identity:

- Under addition, $7$’s inverse is $-7$: $7+(-7)=0$.
- Under multiplication, $7$’s inverse is $\tfrac17$: $7\cdot\tfrac17=1$. But $0$ has no multiplicative inverse.

The set still matters: on the positive integers, addition has no identity, because its identity $0$ isn’t in that set.

**Your turn:** What is the additive inverse of $-8$, and which identity do they add to?
**Your answer:** The additive inverse is $8$; the additive identity is $0$.

Correct: the additive inverse of $-8$ is $8$, and together they give the addition identity, $0$:

$$
-8+8=0.
$$

### Lesson 4: Logic and Mathematical Language

#### Logical Connectives

A **logical connective** joins statements. For example, if $P$ and $Q$ are statements:
- $P\land Q$ means “$P$ **and** $Q$” — both must be true.
- $P\lor Q$ means “$P$ **or** $Q$” — at least one must be true; both can be true.
- $P\Rightarrow Q$ means “if $P$, then $Q$.”

The last one is easy to misread. It means **whenever $P$ is true, $Q$ must also be true**. It does not mean that $P$ causes $Q$.

Example:
- $P$: “$n$ is divisible by 4.”
- $Q$: “$n$ is even.”

Then $P\Rightarrow Q$ is true: every number divisible by 4 is even. But the reverse is not guaranteed: 6 is even, yet not divisible by 4.

**Munger-style check:** keep the direction straight, then try to break the claim with a counterexample. One counterexample disproves the reverse implication.

Your turn: Is “If $n$ is even, then $n$ is divisible by 4” always true? If not, give one counterexample.

**Your answer:** 2 is not divisible by 4.

Correct. $2$ is even but not divisible by $4$, so it disproves the claim “every even number is divisible by $4$.” A single counterexample is enough to disprove an “all” claim.

#### Quantifiers

A **quantifier** tells us how many objects a statement is about:

- $\forall$ means **for every**.
- $\exists$ means **there exists at least one**.

The order matters:
- “For every person, there is a drink they like” allows each person to like a **different** drink.
- “There is a drink that every person likes” means the **same** drink works for everyone.

In symbols:

$$\forall p\,\exists d:\ p\text{ likes }d
\qquad\text{versus}\qquad
\exists d\,\forall p:\ p\text{ likes }d
$$

Munger-style check: ask **“Can the choice depend on the person?”** In the first statement, yes; in the second, one drink must work for everyone.

**Your turn:** “Every student owns at least one book.” Must all students own the same book, or can each student own a different one?

**Your answer:** Each student can own a different book.

Exactly. It means each student may have their own book—not that there’s one book they all share.

#### Negation

Here’s a useful inversion rule: to disprove an **“every”** claim, you only need **one exception**.

If the claim is:

> Every number in $A$ is odd.

Its negation is:

> At least one number in $A$ is not odd.

It is **not** “every number in $A$ is even.” The original claim fails as soon as you find one even number; the other numbers could be odd or even.

In symbols:

$$
\neg(\forall n\in A,\ P(n))
\quad\Longleftrightarrow\quad
\exists n\in A\text{ such that }\neg P(n).
$$

**Your turn:** Let $A=\{2,4,7\}$. What is the negation of “Every number in $A$ is even”?

**Your answer:** At least one number in $A$ is not even.

Correct: **at least one number in $A$ is not even**. You only need one exception to disprove “every.”

#### Free and Bound Variables

In [[2/2a-math/The Princeton Companion to Mathematics.md#3.4 Free and Bound Variables|I.2 §3.4]], the book distinguishes two roles a letter can play:
- A **bound variable** is controlled by a phrase like “for every $a$” or “there exists $a$.”
- A **free variable** hasn’t been given a value or controlled by a quantifier; the statement’s truth may depend on it.

Example:

$$
\forall a\in\{1,2,3\},\quad a<m
$$

Here, $a$ is **bound**: we check each number in $\{1,2,3\}$. The letter $m$ is **free**: the result depends on its value. If $m=4$, the statement is true; if $m=3$, it’s false.

A useful check: **Can I change the letter’s name without changing the meaning?** We could replace bound $a$ with $x$ and nothing changes. But changing free $m$ requires knowing what value it stands for.

**Your turn:** In $\forall x\in\{1,2,3\},\ x<k$, which variable is bound, and which is free?
**Your answer:** I thought $\{1,2,3\}$ was bound; $k$ is free.

---
You got **$k$ is free** right. One correction: **$x$** is the bound variable—not the numbers $1,2,3$.

Read the formula aloud:

> “For every $x$ in the set $\{1,2,3\}$, $x<k$.”

Here, $x$ is the placeholder that takes the values $1$, then $2$, then $3$. The set $\{1,2,3\}$ is the list of allowed values; it isn’t a variable.

A quick test: we can rename $x$ to $n$ without changing the statement. That shows $x$ is bound. But we can’t rename $k$ freely, because the statement depends on what $k$ is.

**Quick check:** In $\forall n\in\{2,4,6\},\ n>1$, which variable is bound?

---
**Your answer:** I thought $2,4,6$ were bound.

You’re right that **all three numbers are covered** by “for every.” The technical term **bound variable**, though, refers to the letter $n$—the placeholder being checked.

Think of it this way:

- $n$: the placeholder (**bound variable**)
- $\{2,4,6\}$: the allowed values of $n$ (**the set/domain**)
- $n>1$: the condition checked for each value

So we check $2>1$, $4>1$, and $6>1$. The quantifier binds the letter $n$, and ranges over the three numbers.

---
You’re right that the quantifier covers all of $2,4,6$; the technical name **bound variable** refers to the letter $n$, whose value we check against each number.

#### Levels of Formality

In [[2/2a-math/The Princeton Companion to Mathematics.md#4 Levels of Formality|I.2 §4]], the book shows that the same mathematical idea can be written in ordinary language, precise English, or symbols. The point is to switch between them when it helps.

The book’s example is:

> Every nonempty set of positive integers has a least element.

In precise English: if $A$ contains positive integers, then there is an $x$ in $A$ that is less than or equal to every $y$ in $A$.
$$
\exists x\in A\quad \forall y\in A,\ x\le y
$$

Here, $x$ is a **candidate** for the smallest number. The phrase $\forall y\in A$ means “check every member of $A$.”

Concrete test: if $A=\{2,5,9\}$, choose $x=2$. It satisfies $2\le2,\ 2\le5,\ 2\le9$, so it is the least element.

**Munger-style habit:** when symbols feel abstract, translate them into words, then test the words on a small example.

Your turn: in this formula, what does $\forall y\in A$ mean in plain English?
**Your answer:** Check every member of $A$.

---
Correct: $\forall y\in A$ means “check every member of $A$.”

### Lesson 5: Number Systems

#### Why Number Systems Expand

In [[2/2a-math/The Princeton Companion to Mathematics.md#1 The Main Number Systems|I.3 §1]], the book treats number systems as sets that let us perform different operations. When an operation takes us outside a set—or an equation has no solution there—we can enlarge the system.

| System | What it lets us do |
| --- | --- |
| $\mathbb N$: counting numbers | Subtraction can fail: $8-13$ is not natural. |
| $\mathbb Z$: integers | $8-13=-5$ is allowed. |
| $\mathbb Q$: rational numbers | Fractions such as $\frac57$ are allowed; division works except by zero. |
| $\mathbb R$: real numbers | Includes $\sqrt2$, the diagonal of a unit square, which is not rational. |
| $\mathbb C$: complex numbers | Includes $i$ with $i^2=-1$, so $x^2=-1$ has solutions. |

**Munger-style model:** when a number system fails, ask, “What operation or equation caused the failure?” The next system adds what is needed to handle that failure. You don’t need the biggest system for every task—counting usually needs only $\mathbb N$.

**Your turn:** What is the smallest system in the table that contains $\sqrt2$?
**Your answer:** The real numbers, $\mathbb R$.

---

Your answer: the real numbers, $\mathbb R$. Correct: $\sqrt2$ is irrational, so it is not in $\mathbb Q$, but it is in $\mathbb R$.

#### Complex Numbers

In [[2/2a-math/The Princeton Companion to Mathematics.md#1.5 The Complex Numbers|I.3 §1.5: The Complex Numbers]], the book asks what happens when real numbers are not enough.

No real number solves $x^2=-1$, because the square of a real number is never negative. The book introduces a new number $i$ with the defining rule:

$$
i^2=-1
$$

A complex number has the form $a+bi$, where $a$ and $b$ are real numbers. Real numbers are included as the special case $b=0$.

Use the defining rule to multiply:

$$
(2+3i)(1+i)=2+2i+3i+3i^2=2+5i-3=-1+5i.
$$

**Munger-style check:** identify the problem the new idea fixes, then test calculations against its defining rule. Here, $i^2=-1$; it does **not** mean $i=-1$.

**Your turn:** Compute $(1+i)^2$ and use $i^2=-1$ to simplify it.
$(1+i)^2=2i$


Correct: $\boxed{2i}$. Expand the square before substituting the defining rule:

$$
(1+i)^2=(1+i)(1+i)=1+2i+i^2=1+2i-1=2i.
$$

The important check is the middle term $2i$. A common failure is to square each term separately and incorrectly write $(1+i)^2=1^2+i^2$; the cross term does not disappear.

##### From Algebra to Geometry

In the complex plane, $1+i$ is the point $(1,1)$. Its distance from the origin is $\sqrt2$, and its angle from the positive real axis is $\pi/4$. Multiplication by $1+i$ therefore stretches lengths by $\sqrt2$ and rotates points by $\pi/4$.

Squaring means multiplying by $1+i$ twice, so the stretch factors multiply and the angles add:

$$
(\sqrt2)^2=2,\qquad \frac{\pi}{4}+\frac{\pi}{4}=\frac{\pi}{2}.
$$

A point at distance $2$ and angle $\pi/2$ is $2i$. This gives a second, geometric check of the algebra.

**Munger-style connection:** one operation has two useful descriptions—algebraically, expand and use $i^2=-1$; geometrically, combine a stretch and a rotation. Two independent views make mistakes easier to catch.

##### Complex Conjugate and Modulus

The book next defines the **conjugate** of $z=a+bi$ as $\bar z=a-bi$. Multiplying a number by its conjugate cancels the imaginary terms:

$$
(a+bi)(a-bi)=a^2+b^2=|z|^2.
$$

For example, $(1+i)(1-i)=1-i^2=2$. Geometrically, $|z|$ is the distance from the origin, while $z\bar z$ is the **square** of that distance. Keep those two quantities distinct.

**Your turn (closed book):** For $z=3+4i$, find $\bar z$, then calculate $z\bar z$ and $|z|$. Which of the two numerical results is the squared distance?
$\bar{z}=3-4i$, $z\bar{z}=(3+4i)(3-4i)=25$, $|z|=5$ $z\bar{z}$ is the squared distance


Correct. Since $3^2+4^2=25$, the conjugate product is $25=|z|^2$, while the distance itself is $|z|=5$. This is the familiar $3$–$4$–$5$ right triangle, now read in the complex plane.

##### Polar Form: Distance and Direction

A complex number $z=a+bi$ can be pictured as the point $(a,b)$. Cartesian form records horizontal and vertical coordinates; **polar form** records distance $r$ from the origin and angle $\theta$:

$$
z=r(\cos\theta+i\sin\theta)=re^{i\theta},\qquad r=|z|.
$$

The shorthand $e^{i\theta}=\cos\theta+i\sin\theta$ connects the angle to the real and imaginary coordinates. For $z=3+4i$, $r=5$ and $\theta=\arctan(4/3)$ in the first quadrant, so $z=5e^{i\theta}$.

This form makes multiplication easier to see: **multiply distances; add angles.** That is the same scale-and-rotate rule we used for $(1+i)^2$.

**Invert the common mistake:** $\arctan(b/a)$ by itself may give the wrong angle because it does not identify the quadrant. Check the signs of $a$ and $b$ on the Argand plane. Also, the argument is defined only for $z\ne0$ and can differ by multiples of $2\pi$; a convention chooses one representative.

**Your turn (closed book):** For $z=-1+i$, give its modulus and its argument in the range $0\leq\theta<2\pi$.
modulus:$\sqrt{ 1+1 }=\sqrt{ 2 }$ ,  argument $\frac{3\pi}{2}$
$\theta=\arctan \left( -\frac{1}{1} \right)=\frac{3\pi}{4}$

Your modulus calculation is correct: $|-1+i|=\sqrt{(-1)^2+1^2}=\sqrt2$. The argument needs a quadrant correction. The point $(-1,1)$ is **upper-left** (Quadrant II), so rotating counterclockwise from the positive real axis gives $\theta=3\pi/4$. The angle $3\pi/2$ points straight down, toward $-i$.

##### Multiplication in Polar Form

Now use the rule **multiply moduli; add arguments**:

$$
1+i=\sqrt2e^{i\pi/4},\qquad -1+i=\sqrt2e^{i3\pi/4}.
$$

Therefore,

$$
(1+i)(-1+i)=2e^{i\pi}=-2.
$$

Check by ordinary expansion: $(1+i)(-1+i)=-1+i-i+i^2=-2$. The agreement is a useful error check: polar form shows the geometry, while algebra checks the arithmetic.

**Your turn (closed book):** Use polar form to find $(1+i)^3$. Give its modulus and argument first, then write it as $a+bi$.
$(1+i)^3=\left[ \sqrt{ 2 }\left( \frac{\sqrt{ 2 }}{2}+\frac{\sqrt{ 2 }}{2}i \right) \right]^3=(\sqrt{ 2 }e^{\pi/4i})^3=2^{3/2}e^{3\pi/4}$


Your polar setup is right: the modulus is $(\sqrt2)^3=2^{3/2}=2\sqrt2$, and the angle is $3(\pi/4)=3\pi/4$. One notation fix: keep the $i$ in the exponential, so write $e^{i3\pi/4}$.

Convert back to Cartesian form:

$$
(1+i)^3=2\sqrt2\left(\cos\frac{3\pi}{4}+i\sin\frac{3\pi}{4}\right)
=2\sqrt2\left(-\frac{\sqrt2}{2}+i\frac{\sqrt2}{2}\right)
=-2+2i.
$$

Independent algebra check: $(1+i)^3=(1+i)^2(1+i)=2i(1+i)=-2+2i$. Both routes agree.

**Power rule:** for a positive integer $n$, $(re^{i\theta})^n=r^ne^{in\theta}$: repeat the same stretch $n$ times and add the same angle $n$ times.

**Your turn (closed book):** Use polar form to find $(1+i)^4$, first as modulus-and-angle form and then as $a+bi$.

$$(1+i)^4=[\sqrt{ 2 }(e^{\pi i/4})]^4=4e^{\pi i}=4(\cos \pi+i\sin \pi)=-4$$


Correct: the modulus is $4$, the angle is $\pi$, and the Cartesian value is $-4$. You used the power rule correctly: multiply the modulus four times and add the angle four times.

The angle wraps around: adding $2\pi$ makes one full turn, so it represents the same direction. Thus a nonzero complex number has arguments that differ by multiples of $2\pi$; a chosen interval selects one principal argument. For example, all arguments of $-4$ are $\pi+2k\pi$ for integers $k$, and the one in $0\leq\theta<2\pi$ is $\pi$.

**Your turn (closed book):** Give two different arguments for $-i$, then give its principal argument in $0\leq\theta<2\pi$.

arguments $\frac{3\pi}{2}$ or $-\frac{\pi}{2}$, the principal argument $\frac{3\pi}{2}$


Correct: $3\pi/2$ and $-\pi/2$ differ by $2\pi$, so they describe the same direction. Under the requested convention $0\leq\theta<2\pi$, the principal argument is $3\pi/2$.

### Lesson 6: Groups and Symmetry

In [[2/2a-math/The Princeton Companion to Mathematics.md#2.1 Groups|I.3 §2.1]], the book moves from number systems to **algebraic structures**: a set together with operations that obey useful rules. Its first example is the symmetries of an equilateral triangle.

Start with rotations only: $R_0$, $R_{120}$, and $R_{240}$. The operation is composition—perform one rotation, then another. Angles add modulo $360^\circ$, so the result is still one of these three rotations (**closure**). $R_0$ does nothing (**identity**), and every rotation can be undone (**inverse**). Composition is associative, so these rotations form a group.

**Munger-style connection:** before, the elements were numbers and the operation was addition or multiplication. Here, the elements are transformations and the operation is “do one, then the other.” The same abstract rules work in a new setting.

**Your turn (closed book):** Which rotation undoes $R_{120}$? Show it using addition modulo $360^\circ$.
$R_{360}-R_{120}=R_{240}$


Correct result: $R_{240}$ undoes $R_{120}$ because $120^\circ+240^\circ=360^\circ$, which is the identity rotation $R_0$. Your subtraction reaches the same answer; the group operation itself is composition, represented here by adding angles modulo $360^\circ$.

#### Slow Practice: Three Rotations

The reflection labels and order-of-composition example were too big a jump, so we will postpone them. For now, use just these three possible turns of the triangle:

- $R_0$: turn $0^\circ$ (do nothing);
- $R_{120}$: turn $120^\circ$;
- $R_{240}$: turn $240^\circ$.

To combine turns, add the angles and wrap around after $360^\circ$:

$$
120^\circ+120^\circ=240^\circ,\qquad 120^\circ+240^\circ=360^\circ=0^\circ.
$$

So two $120^\circ$ turns make $R_{240}$; a $120^\circ$ turn followed by $R_{240}$ returns to $R_0$. That is the group idea in this example: allowed moves can be combined, there is a do-nothing move, and moves can be undone. We will add the remaining formal details gradually.

**Gentle check:** What rotation undoes $R_{240}$? Check by adding the angles and wrapping after $360^\circ$.
add $R_{120}$, do nothing move


Correct: add $R_{120}$ to $R_{240}$. The combined turn is $360^\circ$, which is $R_0$—the do-nothing move. So $R_{120}$ is the undo turn; $R_0$ is where the combination ends.

**One more small step:** combine $R_{240}$ with another $R_{240}$. Add $240^\circ+240^\circ=480^\circ$, then remove one full turn ($360^\circ$). What rotation is left?
$R_{120}$


Correct: $480^\circ-360^\circ=120^\circ$, so the result is $R_{120}$.

This shows **closure** in our small example: when we combine two allowed turns, the result is still one of the allowed turns ($R_0$, $R_{120}$, or $R_{240}$).

**One easy check:** If you apply $R_0$ (the do-nothing turn) to $R_{240}$, where do you end up?
$R_{240}$


Correct: $R_0$ changes nothing, so applying it leaves $R_{240}$ unchanged. That is why $R_0$ is called the identity rotation.

#### A Familiar Example: Integers Under Addition

The same pattern appears with ordinary integers:

- Adding two integers gives another integer.
- $0$ changes nothing: $n+0=n$.
- Every integer can be undone: $n+(-n)=0$.

So $\mathbb Z$ under addition is another group. The elements are numbers instead of rotations, but the useful pattern is the same: combine, do nothing, undo.

**Your turn (easy):** What number must you add to $-5$ to get $0$?
$5$


Correct: $-5+5=0$, so $5$ undoes $-5$ under addition.

#### Same Numbers, Different Operation

A set and its operation both matter. With multiplication, the number that undoes $2$ must make $2\cdot ?=1$. The answer is $1/2$, which is **not an integer**. So the integers do not have multiplicative inverses for every nonzero element; they are not a group under multiplication.

**Your turn (easy):** What number goes in $3\cdot ?=1$, and is it an integer?
$\frac{1}{3}$, not


Correct: $1/3$ is the number, and it is **not an integer**—though it is a rational number. This is why $\mathbb Z$ fails to have multiplicative inverses, while $\mathbb Q$ can divide by any nonzero rational.

#### From Groups to Fields: Familiar Arithmetic

A **field** is a number system where addition and multiplication work together with the familiar rules. The key connection between the two operations is distributivity:

$$
a(b+c)=ab+ac.
$$

The rational numbers $\mathbb Q$, real numbers $\mathbb R$, and complex numbers $\mathbb C$ are examples. We will build the idea one small rule at a time. One important exception: zero has no multiplicative inverse.

**Your turn (easy):** Is there any number $x$ for which $0\cdot x=1$? Why?
NO, $x=1/0$ not exist


Your “no” is right. A direct reason is: for every number $x$, $0\cdot x=0$, so it cannot equal $1$. Saying $1/0$ is undefined is correct, but the multiplication equation shows why zero has no reciprocal.

**Next easy check:** Use the distributive rule to expand $3(2+5)$, then evaluate it.
$3(2+5)=6+15=21$


Correct: $3(2+5)=3\cdot2+3\cdot5=6+15=21$. You distributed the $3$ to both terms. This is what makes addition and multiplication work together in a field.

Inside $\mathbb Q$, nonzero fractions also have reciprocals that stay in $\mathbb Q$. For example, multiplying a fraction by its reciprocal gives $1$.

**Your turn (easy):** What is the multiplicative inverse of $2/5$? Check by multiplying them.
$\frac{5}{2}\times \frac{2}{5}=1$


Correct: $\frac52$ is the multiplicative inverse of $\frac25$, because their product is $1$.

#### Next: Vectors as Coordinate Pairs

In [[2/2a-math/The Princeton Companion to Mathematics.md#2.3 Vector Spaces|I.3 §2.3]], the book introduces vectors. Start with the familiar plane: represent a vector by a pair $(x,y)$.

Add pairs coordinate by coordinate:

$$
(2,1)+(1,3)=(2+1,\,1+3)=(3,4).
$$

Multiplying a vector by a number (a **scalar**) also acts coordinate by coordinate: $2(1,3)=(2,6)$. These two simple operations let us build linear combinations, such as $2\mathbf v+\mathbf w$.

**Your turn (easy):** If $\mathbf v=(2,1)$ and $\mathbf w=(1,3)$, what is $\mathbf v+\mathbf w$?
$\mathbf v+\mathbf w=(2+1,1+3)=(3,4)$


Correct: add the first coordinates ($2+1$) and the second coordinates ($1+3$), giving $(3,4)$.

##### A Linear Combination: Two Basic Directions

Let $\mathbf e_1=(1,0)$ mean one step horizontally, and $\mathbf e_2=(0,1)$ mean one step vertically. Then any coordinate pair can be built from these two directions:

$$
(a,b)=a\mathbf e_1+b\mathbf e_2,
$$

because $a\mathbf e_1=(a,0)$ and $b\mathbf e_2=(0,b)$. A **linear combination** just means: scale vectors, then add them.

**Your turn (easy):** Write $(4,1)$ as $a\mathbf e_1+b\mathbf e_2$.
$4\mathbf e_1+1\mathbf e_2$


Correct: $4\mathbf e_1+\mathbf e_2=(4,0)+(0,1)=(4,1)$.

The pair $\mathbf e_1=(1,0)$ and $\mathbf e_2=(0,1)$ is called a **basis** for the plane: every coordinate pair can be made from them in exactly one way. The coefficients tell how far to move in each direction. A negative coefficient means move in the opposite direction.

**Your turn (easy):** Write $(-2,3)$ as a combination of $\mathbf e_1$ and $\mathbf e_2$.
$-2\mathbf e_1+3\mathbf e_2$


Correct: $-2\mathbf e_1+3\mathbf e_2=(-2,0)+(0,3)=(-2,3)$. The negative coefficient means two steps left; the positive one means three steps up.

##### Why Linear Combinations Matter: Equations

The same idea helps solve simultaneous equations. For example, add the equations $x+y=5$ and $x-y=1$:

$$
(x+y)+(x-y)=5+1\quad\Longrightarrow\quad 2x=6.
$$

The $y$ and $-y$ cancel. Combining equations this way is another useful linear combination.

**Your turn (one step):** Add $x+y=7$ and $x-y=3$. What equation involving only $x$ do you get?
$x+y+x-y=7+3=10$


Your setup is right. Now combine like terms: $y-y=0$ and $x+x=2x$, so $2x=10$ and $x=5$. Substitute into $x+y=7$: $5+y=7$, hence $y=2$. Check: $5-2=3$, so both original equations hold.

**Munger-style habit:** eliminate one unknown, substitute back, then check the answer against both original conditions.

**Your turn (one step):** Add $x+y=9$ and $x-y=3$. What equation remains after the $y$ terms cancel?
$x+y+x-y=9+3 ,2x=12$


Correct: $x+x=2x$ and $y-y=0$, so $2x=12$ and $x=6$. Substituting gives $y=3$.

**Pace adjustment:** You handled the last two cancellation problems correctly, so we can skip more of those and make the next step a little harder: the $y$ coefficients will not cancel until we scale one equation.

##### Elimination with a Scaling Step

Use the book’s example:

$$
3x+2y=6,\qquad x-y=7.
$$

The first equation has $+2y$, while the second has $-y$. Multiply the second equation by $2$ to make $-2y$:

$$
2x-2y=14.
$$

**Your turn:** Add this to $3x+2y=6$. What equation remains after the $y$ terms cancel?
$5x=20$


Correct: $(3x+2y)+(2x-2y)=6+14$ simplifies to $5x=20$, because $+2y$ and $-2y$ cancel. Therefore $x=4$.

Now substitute $x=4$ into the first equation, $3x+2y=6$:

$$
3(4)+2y=6.
$$

**Your turn:** Solve this for $y$.
$2y=6-12 \implies y=-3$


Correct: $2y=6-12=-6$, so $y=-3$. The solution is $(x,y)=(4,-3)$. Check in the other equation: $4-(-3)=7$.

**Pace adjustment:** You correctly eliminated a variable, solved for $x$, and substituted to find $y$. Let’s raise the difficulty: now the coefficient to scale by is $3$, and you’ll solve the whole pair.

**Your turn:** Solve

$$
2x+3y=13,\qquad 4x-y=5.
$$

Hint: multiply the second equation by $3$ so its $y$ term cancels the $+3y$ in the first.
$$2x+12x+3y-3y=13+15 \implies 14x=28 \implies x=2 $$
$$4+3y=13\implies y=3$$


Correct: $(x,y)=(2,3)$. Check both equations: $2(2)+3(3)=13$ and $4(2)-3=5$.

**Pace adjustment:** You solved the full system with scaling and substitution. Now we’ll use that linear-combination idea to understand when a set of vectors has a redundant direction.

##### Span and Redundancy

The two basic directions $\mathbf e_1=(1,0)$ and $\mathbf e_2=(0,1)$ can make every point in the plane. Add $\mathbf u=(1,1)$, but notice $\mathbf u=\mathbf e_1+\mathbf e_2$: it was already available from the first two directions.

A set of vectors **spans** the plane if it can make every point. A **basis** does that without redundant directions, so each point has just one representation. Since $\mathbf u$ is made from $\mathbf e_1$ and $\mathbf e_2$, the three-vector set has redundancy.

**Your turn:** Write $(3,1)$ in two different ways using $\mathbf e_1$, $\mathbf e_2$, and $\mathbf u$; use $\mathbf u$ in one of the ways.
$$(3,1)=3\mathbf{e}_{1}+1\mathbf{e}_{2}=\mathbf{e}_{1}+2\mathbf{e}_{1}+\mathbf{e}_{2}=\mathbf{u}+2\mathbf{e}_{1}$$


Correct. One form is $3\mathbf e_1+\mathbf e_2$; another is $2\mathbf e_1+\mathbf u$, since $\mathbf u=(1,1)$. Both give $(3,1)$. This is the redundancy: the same vector has two descriptions.

##### Transfer: Polynomials Can Be Vectors Too

A vector does not have to be an arrow. The book also treats polynomials as vectors. For polynomials of degree at most $2$, the basic pieces are $1$, $x$, and $x^2$:

$$
2x^2-3x+4=2(x^2)+(-3)(x)+4(1).
$$

The coefficients act like coordinates. The three polynomials $1,x,x^2$ are a basis: they can build every polynomial of degree at most $2$, and the coefficients are unique.

**Your turn:** Write $x^2+4x-3$ as a linear combination of $1$, $x$, and $x^2$.
$$x^2+4x-3=1(x^2)+4(x)-3(1)$$


Correct: $x^2+4x-3=(-3)(1)+4x+1(x^2)$. The coefficients are the coordinates in the polynomial basis $1,x,x^2$.

##### Dimension Counts Independent Pieces

The **dimension** is the number of vectors in a basis. For polynomials of degree at most $2$, the basis $1,x,x^2$ has three elements, so the space has dimension $3$.

More generally, polynomials of degree at most $n$ have basis $1,x,x^2,\ldots,x^n$, so their dimension is $n+1$. For example, degree at most $4$ uses $1,x,x^2,x^3,x^4$ and has dimension $5$.

**Your turn:** What is the dimension of the space of polynomials of degree at most $5$?
6


Correct: the basis is $1,x,x^2,x^3,x^4,x^5$, so there are six independent pieces and the dimension is $6$.

##### Finite and Infinite Dimensions

The space of **all** polynomials has no maximum degree. Its basis continues without end:

$$
1,x,x^2,x^3,x^4,\ldots
$$

So it is infinite-dimensional: no finite list of these basic powers can build every polynomial. A linear combination can scale and add the listed powers, but it cannot create a higher power that is missing.

**Your turn:** If your list stops at $1,x,x^2,x^3,x^4,x^5$, can a linear combination of them produce $x^6$? Why?
NO, $x^{6}\ne a(x^5)+b(x^4)+c(x^3)+d(x^2)+e(x^1)+f$

Correct. More precisely, **no choice** of coefficients $a,b,c,d,e,f$ can make this an identity of polynomials: the combination has degree at most $5$, while $x^6$ has degree $6$. Adding and scaling lower powers cannot create a missing higher power; cancellation can only lower the degree further. In vector-space language, $x^6$ is not in the span of $1,x,x^2,x^3,x^4,x^5$.

##### Rings: Addition and Multiplication Without Guaranteed Division

You have the key idea of dimension and span, so let’s connect it to the next algebraic structure in the book. A **field** lets us add, subtract, multiply, and divide by every nonzero element. A **ring** keeps addition and multiplication (with the usual distributive rules), but does not require every nonzero element to have a multiplicative inverse.

For example, the integers form a commutative ring, but not a field: $2$ is a nonzero integer, yet there is no integer $n$ such that $2n=1$. The obstacle is not multiplication itself; it is that the needed inverse, $1/2$, is missing from $\mathbb Z$. The rationals include it, so $\mathbb Q$ is a field.

**Your turn:** In $\mathbb Q$, what is the multiplicative inverse of $\frac{2}{3}$? Check it by multiplying, and say why this inverse is allowed in $\mathbb Q$ but not in $\mathbb Z$.
$\frac{3}{2}$ $\frac{3}{2}\times \frac{2}{3}=1$, $2\in \mathbb{Z},\frac{1}{2} \notin \mathbb{Z}$

Correct: $\frac{3}{2}\cdot\frac{2}{3}=1$. Your note that $1/2\notin\mathbb Z$ correctly shows why the integer $2$ has no integer inverse. To match the specific inverse you calculated, also note that $\frac{3}{2}\in\mathbb Q$ but $\frac{3}{2}\notin\mathbb Z$.

##### Substructures: A Smaller Set That Keeps the Rules

The book now asks how to build useful structures from familiar ones. A **subfield** is a subset of a field that is itself a field using the same operations. Being a subset is not enough: the subset must stay closed under the operations, especially taking the inverse of a nonzero element.

A book example is

$$
\mathbb Q(i)=\{a+bi:a,b\in\mathbb Q\}\subseteq\mathbb C.
$$

Addition and multiplication keep us inside this set:

$$
(a+bi)+(c+di)=(a+c)+(b+d)i,
$$

$$
(a+bi)(c+di)=(ac-bd)+(ad+bc)i.
$$

All the new coefficients are still rational. For inverses, use the conjugate—the idea you already used when calculating $z\bar z$:

$$
\frac{1}{a+bi}=\frac{a-bi}{a^2+b^2}\qquad (a+bi\ne0).
$$

Here $a^2+b^2$ is a nonzero rational, so the resulting real and imaginary coefficients are rational too. Thus $\mathbb Q(i)$ passes the closure tests and is a subfield of $\mathbb C$. The laws like associativity also hold because they already hold in the larger field $\mathbb C$.

**Your turn:** Find the inverse of $2+i$ in the form $a+bi$. Check your result by multiplying by $2+i$, and say whether it belongs to $\mathbb Q(i)$.
$2-i$, $(2+i)(2-i)=4-i^{2}= 5 \in\mathbb{Q}$

Almost there: $2-i$ is the conjugate, and multiplying by it gives $5$, not $1$. So divide the conjugate by $5$:

$$
(2+i)^{-1}=\frac{2-i}{5}=\frac{2}{5}-\frac{1}{5}i.
$$

Then $(2+i)\left(\frac{2-i}{5}\right)=1$. Both coefficients are rational, so this inverse belongs to $\mathbb Q(i)$.

##### A Smaller Field Can Have Fewer Solutions

A subfield keeps the arithmetic rules, but because it contains fewer elements, some equations that have solutions in the larger field may have none in the smaller one. For instance, $z^2=2$ has solutions in $\mathbb C$, namely $\sqrt2$ and $-\sqrt2$, but neither is in $\mathbb Q(i)$: a real number in $\mathbb Q(i)$ must be a rational number, and $\sqrt2$ is irrational.

**Your turn:** Suppose $z=a+bi$ with rational $a,b$, and $z^2=2$. Expand the square and equate real and imaginary parts. What two equations must $a$ and $b$ satisfy?
$z^2=(a+bi)^2=a^{2}+2abi+i^{2}=2\implies a^2-b^2=2,2ab=0$

Correct: the resulting equations are $a^2-b^2=2$ and $2ab=0$. Tiny expansion fix: write $(a+bi)^2=a^2+2abi+b^2i^2$, so the $b^2$ is carried through before using $i^2=-1$.

Since $a,b$ are rational (hence real), $2ab=0$ means $a=0$ or $b=0$. If $a=0$, then $-b^2=2$, impossible; if $b=0$, then $a^2=2$, impossible for rational $a$. So $z^2=2$ has no solution in $\mathbb Q(i)$, even though it has solutions in the larger field $\mathbb C$.

##### Products: Pairing Structures

The next construction in the book combines structures by making ordered pairs. For two fields, the natural coordinatewise rules would be

$$
(a,b)+(c,d)=(a+c,b+d),\qquad (a,b)(c,d)=(ac,bd).
$$

Many familiar laws still work—but test the field rule that every nonzero element has an inverse. The pair $(1,0)$ is nonzero. Multiplying it by any pair $(x,y)$ gives

$$
(1,0)(x,y)=(x,0).
$$

The multiplicative identity for this pair system would be $(1,1)$.

**Your turn:** Can any choice of $(x,y)$ make $(1,0)(x,y)=(1,1)$? Which field requirement does your answer test?
$(1,0)(x,y)=(x,0)\ne(1,1)$, NO, multiplicative field

Correct: the second coordinate stays $0$, so the product can never be $(1,1)$. This tests the field rule that every nonzero element must have a multiplicative inverse; $(1,0)$ has none under coordinatewise multiplication.

But the same pairs can form a field if we choose a different multiplication. Identify $(x,y)$ with the complex number $x+iy$. Then $i^2=-1$ forces

$$
(x_1,y_1)\star(x_2,y_2)
=(x_1x_2-y_1y_2,\;x_1y_2+x_2y_1).
$$

This is ordinary complex multiplication written in pair notation—not coordinatewise multiplication. For example, $(x,y)$ represents $x+iy$, so the formula comes from expanding $(x_1+iy_1)(x_2+iy_2)$ and using $i^2=-1$.

**Your turn:** Using $\star$, calculate $(2,1)\star(1,3)$. Give both the resulting pair and its equivalent complex number.
$(2,1)\star(1,3)=(2\times 1-1\times 3,2\times 3+1)=(-1,7)$
$(2,1)\star(1,3)=(2+i)(1+3i)=2+6i+i+3i^2=2-3+7i=(-1,7)$

Correct: the product pair is $(-1,7)$, which represents $-1+7i$. Your complex-number check confirms it.

**Correction to my previous chat message:** I mistyped the last term of the general rule as $x_2y_2$. It must be $x_2y_1$:

$$
(x_1,y_1)\star(x_2,y_2)=(x_1x_2-y_1y_2,\;x_1y_2+x_2y_1).
$$

Your calculation used the correct rule; the formula already written in this note is also correct.

##### Products of Vector Spaces: Dimensions Add

The book also forms a product of vector spaces. The elements are pairs $(v,w)$, and addition and scalar multiplication happen coordinatewise:

$$
(v,w)+(v',w')=(v+v',w+w'),\qquad c(v,w)=(cv,cw).
$$

Each factor contributes its own independent coordinates, so $\dim(V\times W)=\dim V+\dim W$. For example, let $V=P_{\le2}$ have basis $1,x,x^2$ and let $W=\mathbb R^2$ have basis $(1,0),(0,1)$. The product has dimension $3+2=5$. Its basis is made by placing each basis vector from one factor alongside zero in the other factor.

**Your turn:** Write those five basis vectors explicitly as elements $(p,w)$ of $P_{\le2}\times\mathbb R^2$. Use $\mathbf 0_P$ for the zero polynomial and $(0,0)$ for the zero vector in $\mathbb R^2$.
basis vector: $1,x,x^2,x^3,x^4$

You noticed there are five basis elements, but these five cannot all be polynomial powers: the space is a pair $(p,w)$, with $p\in P_{\le2}$ and $w\in\mathbb R^2$. In particular, $x^3$ and $x^4$ are not in $P_{\le2}$. Lift each basis element into its own coordinate and put zero in the other coordinate. The correct basis is

$$
\bigl\{(1,(0,0)),(x,(0,0)),(x^2,(0,0)),(\mathbf 0_P,(1,0)),(\mathbf 0_P,(0,1))\bigr\}.
$$

The first three vectors span the polynomial coordinate; the last two span the $\mathbb R^2$ coordinate. Before moving to the next construction, try the same idea once more in a smaller example.

**Your turn:** Write a basis for $P_{\le1}\times\mathbb R$ as three pairs $(p,r)$.
$(1,0),(x,0)(\mathbf{0}_{p},1)$

Correct: those are the three basis directions. With punctuation and the zero-polynomial notation made explicit, the basis is $\{(1,0),(x,0),(\mathbf 0_P,1)\}$.

##### Quotients: Treating Equivalent Representations as One

The next idea is a **quotient**: start with objects, decide which ones count as equivalent, and then treat each whole equivalence class as one object. A familiar example is rational numbers: $\frac12$ and $\frac36$ are different written fractions, but they represent the same rational number.

There is an important stress test: an operation on these new objects must not depend on which equivalent representation you chose. For example, someone might try to define

$$
\frac{a}{b}\circ\frac{c}{d}=\frac{a+c}{b+d}.
$$

**Your turn:** Compute $\frac12\circ\frac13$, then compute $\frac36\circ\frac13$. Do the answers represent the same rational number? What does this tell you about whether $\circ$ is a valid operation on $\mathbb Q$?

$\frac12\circ\frac13=\frac{1+1}{2+3}=\frac{2}{5}$
$\frac36\circ\frac13=\frac{3+1}{6+3}=\frac{4}{9}$
yes
yes

Your calculations are right, but the comparison is **no**: $\frac25\ne\frac49$, since $2\cdot9=18$ while $4\cdot5=20$. The same rational input $\frac12=\frac36$ gave different outputs, so $\circ$ is **not well-defined** on $\mathbb Q$. Both outputs being rational does not make them the same rational.

Now the book applies quotienting to polynomials. It declares $x^3-x-1$ equivalent to $0$, which lets us replace $x^3$ by $x+1$ inside any polynomial. This is a rule for simplifying representatives of the same quotient element.

**Your turn:** Using $x^3\sim x+1$, reduce $x^4$ to a polynomial of degree at most $2$. (Start with $x^4=x\cdot x^3$.)

$x^4=x\cdot x^3=x(x+1)=x^2+x$

Correct: $x^4\sim x^2+x$. Each replacement uses the relation $x^3-(x+1)=x^3-x-1\sim0$, and you can apply it again whenever a higher power remains.

For example, reduce $x^5$ step by step:

$$
x^5=x^3x^2\sim(x+1)x^2=x^3+x^2\sim(x+1)+x^2=x^2+x+1.
$$

So every polynomial is equivalent to one of degree at most $2$.

**Your turn:** Reduce $x^6$ to degree at most $2$, showing the replacements you use.
$x^6=x^3\times x^3=(x+1)^2=x^2+2x+1$

Correct: $x^6\sim(x+1)^2=x^2+2x+1$. You substituted for both factors and got a representative of degree at most $2$.

Now notice what quotienting can accomplish: in the quotient, equivalent polynomials count as equal. The book uses this to find inverses. For example, it claims that $x^2$ has inverse $1+x-x^2$, because their product is equivalent to $1$.

**Your turn:** Verify the claim by expanding $x^2(1+x-x^2)$, then reducing with $x^3\sim x+1$ and $x^4\sim x^2+x$. What does the product become?

$x^2(1+x-x^2)=x^2+x^3-x^4=x^2+x+1-x^2-x=1$

Correct: after reduction, the product is equivalent to $1$. Thus in the quotient, the class of $1+x-x^2$ really is the multiplicative inverse of the class of $x^2$.

##### Functions That Preserve Structure

The next section studies maps between algebraic structures. A **homomorphism** preserves the operations: for additive groups, $\phi(a+b)=\phi(a)+\phi(b)$. For rings or fields, it must preserve the relevant addition and multiplication too.

A familiar example is reduction modulo $5$: $\phi:\mathbb Z\to\mathbb Z/5\mathbb Z$, where $\phi(n)$ is the remainder class of $n$. It preserves addition, even though it is not one-to-one: $\phi(1)=\phi(6)$. Preserving structure does not automatically mean keeping different inputs distinct.

**Your turn:** Compute $\phi(7+8)$ and $\phi(7)+\phi(8)$ in $\mathbb Z/5\mathbb Z$. Do they agree?
$\phi(7+8)=\phi(15)=\phi(5)$
$\phi(7)+\phi(8)=\phi(2)+\phi(3)=\phi(5)$

Correct: both sides are the zero residue modulo $5$: $\phi(15)=\phi(5)=\overline{0}$, and $\phi(2)+\phi(3)=\phi(5)=\overline{0}$. This confirms addition is preserved.

A **homomorphism** preserves operations. An **isomorphism** is a homomorphism that is also bijective, so it preserves the structure without collapsing distinct elements or missing any elements of the target. An **automorphism** is an isomorphism from a structure to itself.

**Your turn:** Is the reduction map $\phi:\mathbb Z\to\mathbb Z/5\mathbb Z$ an isomorphism? Use $\phi(1)$ and $\phi(6)$ to justify your answer.

$\phi(6)=\phi(1)$, isomorphism is bijective, one input only can get one output, there are two input get the same result

Correct: $\phi(1)=\phi(6)=\overline1$, so $\phi$ is not injective and therefore not an isomorphism. Small wording distinction: it is still a function—each input has one output. What fails is that two different inputs can share an output.

##### Automorphisms: Symmetries of a Structure

An automorphism is an isomorphism from a structure to itself: it is a bijection that preserves the operations. For the field $\mathbb Q(\sqrt2)$, consider

$$
\sigma(a+b\sqrt2)=a-b\sqrt2,\qquad a,b\in\mathbb Q.
$$

This resembles complex conjugation: it fixes rational numbers and swaps the two roots $\sqrt2$ and $-\sqrt2$. Applying $\sigma$ twice returns the original number, so the map is bijective; it also preserves addition and multiplication.

**Your turn:** Let $u=1+\sqrt2$ and $v=2-\sqrt2$. Compute $\sigma(uv)$ and $\sigma(u)\sigma(v)$. Do they agree, as multiplication preservation requires?
$\sigma(uv)=\sigma((1+\sqrt{ 2 })(2-\sqrt{ 2 }))=\sigma((1+\sqrt{ 2 })(2-\sqrt{ 2 }))=\sigma(\sqrt{ 2 })=-1\sqrt{ 2 }$
$\sigma(u)\sigma(v)=\sigma(1+\sqrt{ 2 })\sigma(2-\sqrt{ 2 })=(1-\sqrt{ 2 })(2+\sqrt{ 2 })=2+\sqrt{ 2 }-2\sqrt{ 2 }-2=-\sqrt{ 2 }$

Correct: $uv=\sqrt2$, and both $\sigma(uv)$ and $\sigma(u)\sigma(v)$ equal $-\sqrt2$. This verifies multiplication preservation for this pair; a general proof must cover every pair.

##### Linear Maps: The Basis Determines the Map

The book's next section, I.3 §4.2, connects homomorphisms to vector spaces. A **linear map** preserves linear combinations:

$$
T(a\mathbf u+b\mathbf v)=aT(\mathbf u)+bT(\mathbf v)
$$

for every pair of vectors and scalars.

**Connection to bases:** transform the basis vectors, then rebuild the result using the original coefficients.

Let $T:\mathbb R^2\to\mathbb R^2$ be linear, with $\mathbf e_1=(1,0)$ and $\mathbf e_2=(0,1)$, and suppose

$$
T(\mathbf e_1)=(1,3),\qquad T(\mathbf e_2)=(2,-1).
$$

Since $(x,y)=x\mathbf e_1+y\mathbf e_2$,

$$
T(x,y)=x(1,3)+y(2,-1).
$$

Those two basis images determine the map on every vector. This depends on linearity: two values would not determine an arbitrary function.

**Your turn:** Using $(2,-1)=2\mathbf e_1-\mathbf e_2$, compute $T(2,-1)$. Show the linear combination of the basis images.
$T(2,-1)=2(1,0)-1(0,1)$

Your coefficients $2$ and $-1$ are correct, but $2(1,0)-(0,1)$ reconstructs the **input**, not its image under $T$. Apply $T$ to the basis vectors as well:

$$
\begin{aligned}
T(2,-1)&=2T(\mathbf e_1)-T(\mathbf e_2)\\
&=2(1,3)-(2,-1)\\
&=(2,6)-(2,-1)=(0,7).
\end{aligned}
$$

**Recall aid:** same coefficients, transformed basis vectors. Here $\mathbf e_1=(1,0)$, but $T(\mathbf e_1)=(1,3)$; they are different vectors.

Let's check this distinction before introducing matrix notation.

**Your turn:** With the same $T(\mathbf e_1)=(1,3)$ and $T(\mathbf e_2)=(2,-1)$, compute $T(1,2)$. Show the linear combination of the two basis images.
$T(1,2)=1T(\mathbf{e}_{1})+2T_{2}(\mathbf{e}_{2})=1(1,3)+2(2,-1)=(5,1)$

Correct: $T(1,2)=(5,1)$. You kept the coefficients and used the transformed basis vectors. One notation fix: write $2T(\mathbf e_2)$, not $2T_2(\mathbf e_2)$—the same map $T$ acts on both basis vectors.

##### Matrices: Columns Store the Basis Images

Using the standard bases, place $T(\mathbf e_1)=(1,3)$ in the first column and $T(\mathbf e_2)=(2,-1)$ in the second:

$$
A=\begin{pmatrix}1&2\\3&-1\end{pmatrix}.
$$

Matrix-vector multiplication is the same linear-combination rule you just used:

$$
A\begin{pmatrix}x\\y\end{pmatrix}
=x\begin{pmatrix}1\\3\end{pmatrix}
+y\begin{pmatrix}2\\-1\end{pmatrix}
=\begin{pmatrix}x+2y\\3x-y\end{pmatrix}.
$$

For your input, $A\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}5\\1\end{pmatrix}$.

**Recall aid:** column $j$ records where the $j$th basis vector goes. This representation depends on the chosen bases; we are using the standard ones.

**Your turn:** A new linear map is $S(x,y)=(2x-y,\;x+4y)$. Write its matrix in the standard bases. Find $S(\mathbf e_1)$ and $S(\mathbf e_2)$ first, then arrange them as columns.

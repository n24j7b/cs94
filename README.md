java c
CO   372:   Portfolio   Optimization   Models 
Fall   2024 
Problem Set 1 Due:   Friday   2024-09-20   at   4   pm   EDT.   Papers   must   be   handed   in   on-line   using   the   labeled   dropbox   on   Crowdmark. Each   question   is   handed   in   as   a   separate   upload. You   can   either   prepare   your   solutions   electronically   using,   e.g.,   LaTeX,   or   else   you   can   hand-write   them   and   submit   a   scan.   In   the   latter   case,   please   take   care   that   the   scan   is   of good   quality   with   a   white   background.Your   papers   may   be   handed   in   up   to   24   hours   late,   in   which   case   there   is   a   10%   late   penalty.   Please use the late-paper dropbox on Crowdmark if you   are handing   in   a   late   paper. You   may   hand   in   some   questions   on   time   and   others   late. In   this   case,   use   the   on-time   dropbox for the on-time questions   and the   late   dropbox   for   the   late   questions. However, you may   not   split   the   parts   of a   question   (i.e.,   (a),   (b),   etc.) between   the   two   dropboxes.    .
Collaboration policy. 
1.    Students   are   allowed   to   discuss   question   with   each   other   in   general   terms   including   helping   each   other   on   Piazza.   Do   not   post   solutions   or   partial   solutions   on   Piazza.
2.    No   student   should   hand   in   work   that   entirely   represents   someone   else’s   effort.
3.    Students   who   work   together   privately   on   homework   should   list   their   teammates   in   their   submission.   Teams   of size   up   to   5   are   allowed.
1.    (a)   Show   that   for   any   A   ∈ Rm ×n ,   rank(A)   =   rank(AT   A). Suggested   approach:    Show   that   A   and   AT   A   have   the   same   null   space,   in   which   case   the   result   follows   from   the   rank-nullity   theorem. It   is   straightforward   to   show   that   Null(A) ⊆   Null(AT   A)   by considering   a   test   vector x ∈   Rn. To   show   then   that   Null(AT   A)   ⊆   Null(A),   again consider   a   test   vector x ∈ Rn    and   use   the   fact   that   Ax = 0 if and   only   if   ⅡAxⅡ2      = 0.(b)   Construct   three   30   ×   60   random   matrices   in   Matlab   using   the   randn   function   like   this: A=randn(30,60);   For   each   such   matrix,   say   A,   ask   Matlab   for   rank(A)   and rank(A’*A).   Do   the   answers   come   out   equal?Note:    For   part    (b)   and   part    (c),   please   hand   in   a   copy   of   your   interaction   with   the   Matlab   command   window. In   Windows,   if   you   right-click   on   the   command   window and   select   “Print”,   and   then “Microsoft   Print   to   PDF”   as   the   printer, you   can   make   a PDF   copy   of the   command   window.   Alternatively,   you   can   use   screenshots   to   capture   the   command   window.
(c)   In   principle,   one   could   iterate   the   process   in   (b)   indefinitely,   and   the   rank   should   come   out   the   same. In   other   words, starting   from   a   random   30   ×   60   matrix   A, if   B   :=   AT   A   (Matlab: B=A’*A;),   C   :=   BT   B   ,   D   :=   CT   C,   and   so   on,   all   these   matrices A,B,C, . . . should   have   the   same   rank. Try   this   for   12 iterations   in   Matlab, and   report on   the   results.    Note:   It   is   not   required   to   provide   an   explanation   of   this   behavior   from Matlab.
2.    Let   U   be   an   n   ×   n   upper   triangular   matrix   with   nonzeros   on   the   diagonal.    Consider   solving   the   system   of   linear   eq代 写CO 372: Portfolio Optimization Models Fall 2024 Problem Set 1Matlab
代做程序编程语言uations   Ux = b,   where b ∈   Rn      is   given   and x ∈   Rn      is   the   unknown.
(a)   Write   down   the   last   (nth)   equation   of   the   system   Ux = b explicitly,   and   argue that   this   equation   uniquely   determines   x(n)   (last   entry   of   n).
(b)   Assuming   x(n)   has   been   computed   as   in   part   (a),   argue   that   x(n −   1)   is   uniquely   determined   by   the   second-to-last   ((n −   1)st)   equation   of the   system.
(c)   Proceeding   by   reverse   induction,   argue   that   for   k   = n,n −   1, . . . , 1,   all   entries   of x are   uniquely   determined.
(d)   Does   the   argument   in   (a)–(c)   still   work   in   the   case   that   U   has   one   or   more   zeros   on   the   diagonal?
3.    Suppose   by   accident   that   a   firm   lists   the   same   security   twice   in   its   catalog:   say   in   the   universe   of   n   securities   that   securities   1   and   2   are   actually   the   same.    In   this   case,    a   portfolio   with   x(1)   =   20,   x(2)   =   80   is   equivalent   to   one   with   x(1)   =   90,   x(2)   =   10,   assuming   that   the   remaining   x(i)’s   (i =   3,   4,...,   n)   are   equal.(a) In this situation, one might regard portfolios as consisting of   only n−1 securities, say   in   amounts   y(1),   y(3),   y(4),...,   y(n) where   y(1)   := x(1) + x(2)   and   y(i)   = x(i)   for   i   =   3, . . . ,n.   Write   down   an   (n−1)×n   matrix   M   that   maps   the   vector   [x(1);x(2); ··· ;x(n)]   to   [y(1);y(3); ···   ;y(n)].
(b)   Argue   that   rank(M) = n   −   1,   where   M   is   as   in   (a).
(c)   Suppose x1   , x2      are   portfolios   that   equivalent   in   the   sense   of   this   question.    Char-   acterize   the   difference d := x1      − x2   .    Show    that    the   set   of   such   differences d is   a   1-dimensional   subspace   of Rn   ,   and   find   a   basis   for   this   subspace.4.   The following is   awell known theorem   that   will   be   used   in   this   course.    Let   C   ⊆   Rn      be
closed,   bounded,   and   nonempty.   Let   f,   g   be   two   continuous   functions   C   →   R.   Then
min{f(x) + g(x)   : x ∈   C}   ≥   min{f(x)   : x ∈   C}   + min{g(x)   : x ∈   C}. 
(a)   Prove   this   theorem.
(b) Take   n   =   1 and   C   =   [0, 1]   (the   unit   interval).    Come   up   with   an   example   f,g   where the   inequality   in   the   theorem   is   strict.
(c)   Again   with   n   =   1,   C   =   [0, 1],   come   up   with   an   example   f,g   where   the   inequality in   the   theorem   is   satisfied   as   an   equation.
5.    Suppose   in   a   universe   of   n   securities   that x1   , x2      ∈   Rn      are   two   portfolios.    Let   r(¯) ∈   Rn   denote   the   expected   return   vector,   so   that   the   expected   return   of x1      is   r(¯)Tx1      while   the expected   return   of x2    is   r(¯)Tx2   .
(a)   Show   the   following   fact:    if x′ is   a   convex   combination   of x1, x2   ,   i.e., x′ =   (1   −   λ)x1   + λx2    for   some   λ   ∈   [0, 1], then   r(¯)Tx′ ≤   max(r(¯)Tx1   ,   r(¯)Tx2   ).
(b)   Focus   on   the   case   n   =   2,   and   suppose

is   the   covariance   matrix.   Find   two   portfolios x1   , x2 ∈ R2   such   that   if x′ = 0.5x1   +0.5x2   ,   then   (x′ )TH(x′ ) < min(x1(T)Hx1   , x2(T)Hx2   ).
This   question   illustrates   a   basic   principle   of   investing:   diversifying   a   portfolio   cannot   increase   the   maximum   return,   but   it   can   decrease   the   risk.







         
加QQ：99515681  WX：codinghelp

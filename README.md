これは何
========
[lisp-unit.lisp] を xyzzy で動くようにしたついでに微妙に改造したものです。

  [lisp-unit.lisp]: http://www.cs.northwestern.edu/academics/courses/325/readings/lisp-unit.html

インストール
============
（工事中）

使い方
======
TODO: ちゃんと書くべし

    ;; 2011-03-31
    ;; とりあえず現状でも動かすことはできるのでそのサンプル
    (load "~/work/xyzzy.lisp-unit/site-lisp/lisp-unit.l")
    t
    
    (use-package :lisp-unit)
    t
    
    (define-test add
    	     (assert-eql 1 (add 0 1))
    	     (assert-eql 2 (add 1 1)))
    add
    
    (let ((*trace-output* *standard-output*))
      (run-tests 'add))
        add: 関数が定義されていません: add
    
    (defun add (x y) (* x y))
    add
    
    (let ((*trace-output* *standard-output*))
      (run-tests 'add))
    add: (add 0 1) failed: 
    Expected 1 
    but saw 0
    add: (add 1 1) failed: 
    Expected 2 
    but saw 1
    add: 0 assertions passed, 2 failed.
    
    (defun add (x y) (+ x y))
    add
    
    (let ((*trace-output* *standard-output*))
      (run-tests 'add))
    add: 2 assertions passed, 0 failed.


注意点、既知の問題など
======================

バグ報告、質問、要望などは [GitHubIssues] か [@bowbow99] あたりへお願い
します。

  [GitHubIssues]: http://github.com/bowbow99/xyzzy.lisp-unit/issues
  [@bowbow99]: http://twitter.com/bowbow99


ライセンス
==========
MIT/X

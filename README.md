����͉�
========
[lisp-unit.lisp] �� xyzzy �œ����悤�ɂ������łɔ����ɉ����������̂ł��B

  [lisp-unit.lisp] http://www.cs.northwestern.edu/academics/courses/325/readings/lisp-unit.html

�C���X�g�[��
============
�i�H�����j

�g����
======
TODO: �����Ə����ׂ�

    ;; 2011-03-31
    ;; �Ƃ肠��������ł����������Ƃ͂ł���̂ł��̃T���v��
    (load "~/work/xyzzy.lisp-unit/site-lisp/lisp-unit.l")
    t
    
    (use-package :lisp-unit)
    t
    
    (symbol-plist 'define-test)
    nil
    
    
    (define-test add
    	     (assert-eql 1 (add 0 1))
    	     (assert-eql 2 (add 1 1)))
    add
    
    (let ((*trace-output* *standard-output*))
      (run-tests 'add))
        add: �֐�����`����Ă��܂���: add
    
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


���ӓ_�A���m�̖��Ȃ�
======================

�o�O�񍐁A����A�v�]�Ȃǂ� [GitHubIssues] �� [@bowbow99] ������ւ��肢
���܂��B

  [GitHubIssues] http://github.com/bowbow99/xyzzy.lisp-unit/issues
  [@bowbow99] http://twitter.com/bowbow99


���C�Z���X
==========
MIT/X

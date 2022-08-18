一米阳光
========


不输出错误信息
--------------

.. code:: c

   sed -i "s/xxx/$FULL_LOWER/g" `grep xxx -rl $FILE` 2> /dev/null

   # 原理
   2> /dev/null


替换字符串
----------

.. code:: c

   sed -i "s/oldstr/newstr/g" file

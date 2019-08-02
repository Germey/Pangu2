Pangu2
========

Split From English and Chinese.

Installation
============

.. code-block:: bash

    $ pip install -U pangu2

Usage
=====

In Python
---------

.. code-block:: py

    import pangu2

    new_text = pangu2.spacing_text('當你凝視著bug，bug也凝視著你')
    # new_text = '當你凝視著 bug，bug 也凝視著你'

    nwe_content = pangu2.spacing_file('path/to/file.txt')
    # nwe_content = '與 PM 戰鬥的人，應當小心自己不要成為 PM'

In CLI
------

.. code-block:: bash

    $ pangu2 "請使用uname -m指令來檢查你的Linux作業系統是32位元或是[敏感词已被屏蔽]位元"
    請使用 uname -m 指令來檢查你的 Linux 作業系統是 32 位元或是 [敏感词已被屏蔽] 位元

    $ python -m pangu2 "為什麼小明有問題都不Google？因為他有Bing"
    為什麼小明有問題都不 Google？因為他有 Bing

    $ echo "未來的某一天，Gmail配備的AI可能會得出一個結論：想要消滅垃圾郵件最好的辦法就是消滅人類" >> path/to/file.txt
    $ pangu2 -f path/to/file.txt >> pangu_file.txt
    $ cat pangu_file.txt
    未來的某一天，Gmail 配備的 AI 可能會得出一個結論：想要消滅垃圾郵件最好的辦法就是消滅人類

    $ echo "心裡想的是Microservice，手裡做的是Distributed Monolith" | pangu2
    心裡想的是 Microservice，手裡做的是 Distributed Monolith

    $ echo "你從什麼時候開始產生了我沒使用Monkey Patch的錯覺?" | python -m pangu2
    你從什麼時候開始產生了我沒使用 Monkey Patch 的錯覺？

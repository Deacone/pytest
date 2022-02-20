:orphan:

..
    .. sidebar:: Next Open Trainings

       - `Professional Testing with Python <https://www.python-academy.com/courses/specialtopics/python_course_testing.html>`_, via `Python Academy <https://www.python-academy.com/>`_, February 1st to 3rd, 2022, Leipzig (Germany) and remote.

       Also see `previous talks and blogposts <talks.html>`_.

.. _features:

pytest: 帮助你更好的编写程序
=======================================

备注：这个项目是对 ``pytest`` 项目的中文翻译，持续更新中

.. module:: pytest

``pytest`` 测试框架能够用简单的方式编写小而简的测试用例，并且可以扩展用来支持应用程序和库中的复杂的功能测试


``pytest`` 运行要求: Python 3.7+ or PyPy3.

**PyPI 包名称**: :pypi:`pytest`

**PDF格式文档**: `下载最新PDF版本 <https://media.readthedocs.org/pdf/pytest/latest/pytest.pdf>`_


一个简单的例子
---------------

.. code-block:: python

    # content of test_sample.py
    def inc(x):
        return x + 1


    def test_answer():
        assert inc(3) == 5


运行用例:

.. code-block:: pytest

    $ pytest
    =========================== test session starts ============================
    platform linux -- Python 3.x.y, pytest-7.x.y, pluggy-1.x.y
    rootdir: /home/sweet/project
    collected 1 item

    test_sample.py F                                                     [100%]

    ================================= FAILURES =================================
    _______________________________ test_answer ________________________________

        def test_answer():
    >       assert inc(3) == 5
    E       assert 4 == 5
    E        +  where 4 = inc(3)

    test_sample.py:6: AssertionError
    ========================= short test summary info ==========================
    FAILED test_sample.py::test_answer - assert 4 == 5
    ============================ 1 failed in 0.12s =============================

``pytest`` 有详细的断言机制，这里只展示了简单的断言。

有关 ``pytest`` 的基本使用介绍，请参阅 :ref:`开始 <开始>` 。


功能特征
--------
- 失败的详细信息：:ref:`断言描述 <断言>` （不需要专门去记断言名字：``self.assert*`` ）

- :ref:`自动化识别覆盖 <test discovery>` 模块和函数

- :ref:`模块化的夹具 <夹具>` 在整个测试周期中管理小型的或参数化的用例

- 可以用 :ref:`unittest <unittest>` 和 :ref:`nose <noseintegration>` 的方式来运行测试用例

- Python 3.7+ or PyPy 3

- 拥有 800+ 丰富的插件体系 :ref:`扩展插件 <plugin-list>` 和活跃的社区


文档
-------------

* :ref:`快速开始 <开始>` - 只需 20 分钟即可安装 pytest 并掌握其基础知识
* :ref:`操作指南 <how-to>` - 分步操作指南，
* :ref:`参考指南 <reference>` - 包括完整的pytest API参考，插件列表参考等
* :ref:`解释说明 <explanation>` - 问题背后的逻辑，关键主题的讨论，回答更高层次的问题


Bugs/需求
-------------

请使用 `GitHub 问题管理 <https://github.com/pytest-dev/pytest/issues>`_ 来提bug和需求功能。


变更日志
---------

Bug修复和新增功能的每一个版本请参考 :ref:`变更日志 <changelog>` 。

支持 pytest
--------------

`Open Collective`_ 是一个在线的开放式的透明的资金平台。
它提供了以完全透明的方式筹集资金和分享您的财务的工具。

It is the platform of choice for individuals and companies that want to make one-time or
monthly donations directly to the project.

See more details in the `pytest collective`_.

.. _Open Collective: https://opencollective.com
.. _pytest collective: https://opencollective.com/pytest


pytest for enterprise
---------------------

Available as part of the Tidelift Subscription.

The maintainers of pytest and thousands of other packages are working with Tidelift to deliver commercial support and
maintenance for the open source dependencies you use to build your applications.
Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use.

`Learn more. <https://tidelift.com/subscription/pkg/pypi-pytest?utm_source=pypi-pytest&utm_medium=referral&utm_campaign=enterprise&utm_term=repo>`_

Security
~~~~~~~~

pytest has never been associated with a security vulnerability, but in any case, to report a
security vulnerability please use the `Tidelift security contact <https://tidelift.com/security>`_.
Tidelift will coordinate the fix and disclosure.


License
-------

Copyright Holger Krekel and others, 2004.

Distributed under the terms of the `MIT`_ license, pytest is free and open source software.

.. _`MIT`: https://github.com/pytest-dev/pytest/blob/main/LICENSE

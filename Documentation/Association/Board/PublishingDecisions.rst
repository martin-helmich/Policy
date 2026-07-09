:navigation-title: Publishing decisions
..  include:: /Includes.rst.txt
..  _t3a-board-publishing-decisions:

===================================================
Publishing Decisions of the TYPO3 Association Board
===================================================

:Document Owner: T3A Secretary, `Martin Helmich`_
:Version: 1.0, 7 July 2026

.. _Martin Helmich: https://my.typo3.org/u/mhelmich

-----------------------
1. Publication location
-----------------------

All decisions of the TYPO3 Association Board are published as reStructured Text documents in the `Decision directory`_ of the TYPO3 Association Board documentation. The decision directory is structured by year, and each decision is published as a separate document.

Document naming and location *MUST* follow the pattern `Documentation/Association/Board/Decisions/YYYY/MM-DD-<DECISION TITLE>.rst`.

.. _Decision directory: /Documentation/Association/Board/Decisions/index.rst

-----------------------
2. Publication workflow
-----------------------

1. Decision papers are published in the documentation repository as soon as the decision has been accepted or rejected by the Board. Templates for decision documents are available at `Documentation/Association/Board/Decisions/YYYY/.template.rst`.

2. The decision paper must be added to the repository via a pull request, which must be approved by at least one other Board member. This is verified by the pull request approval workflow of the repository.

--------------------------
3. Decision implementation
--------------------------

1. Decisions that are implemented in the form of a policy change are implemented in the policy repository. The policy change should be published in the same pull request as the decision paper, if possible. If not, a separate pull request should be created for the policy change, which must reference the decision paper.

2. An exception to the above are changes to the Bylaws, which require a vote by the General Assembly. In this case, the Bylaws change must be documented by a link to the General Assembly protocol in which the bylaws change was approved.
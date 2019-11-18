common-crawl-subdomains
=======================

``common-crawl-subdomains`` is a list of subdomains. It is intended to be used
for subdomain enumeration. The list is a compilation of all subdomains I could
find in the `Common Crawl`_ data, sorted by popularity (most common first).

www is the most common subdomain at 10.863.742 occurences. Of the total
17.525.849 subdomains found, this means that www accounts for 61.99% of all
subdomains.


How common is a subdomain?
--------------------------

The popularity of the subdomains decline quickly.

* The 10th most common subdomain appeared 7482 times.
* The 100th most common subdomain appeared 977 times.
* The 1000th most common subdomain appeared 119 times.
* The 10000th most common subdomain appeared 17 times.
* The 100000th most common subdomain appeared 3 times.


Use a smaller list
------------------

As the popularity of the subdomains quickly decline, I advice you to use a much
smaller list than ``common-crawl-subdomains``. Something like 10000 seems
reasonable. You can use ``head`` to create a smaller list::

    head -n 10000 common-crawl-subdomains > common-crawl-subdomains-10000

The list with 10000 is in this repository (``common-crawl-subdomains-10000``).
In my experience, it yields many results.


Use with subbrute.py
--------------------

subbrute_ is a (very) fast subdomain spider. It is simple to use
``common-crawl-subdomains`` with subbrute_::

    ./subbrute --subs common-crawl-subdomains-10000 example.com


.. _Common Crawl: https://commoncrawl.org/
.. _subbrute: https://github.com/TheRook/subbrute/

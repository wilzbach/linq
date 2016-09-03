
General Indexes
a.filter(a, b)
a.map(a, b)

Filtering
---------

LINQ   | D
-------|-----
[`Where`](https://msdn.microsoft.com/en-us/library/bb534803.aspx) | [`filter`](http://dlang.org/phobos/std_algorithm_iteration.html#.filter)
[`OfTyp`](https://msdn.microsoft.com/en-us/library/bb360913.aspx) | [`castSwitch`](http://dlang.org/phobos/std_algorithm_comparison.html#.castSwitch)

Projections
-----------

LINQ   | D
-------|-----
[`Select`](https://msdn.microsoft.com/en-us/library/bb384087.aspx) | [`map`](http://dlang.org/phobos/std_algorithm_iteration.html#.map)
[`SelectMany`](https://msdn.microsoft.com/en-us/library/bb534336.aspx) |=
Anonoymous Types | Tuples
Indexed | [`enumerate`](http://dlang.org/phobos/std_range.html#enumerate)

```
from c in customers
from o in c.Orders
where c.Region == "WA"
```

Partitioning
------------

LINQ   | D
-------|-----
[`Take`](https://msdn.microsoft.com/en-us/library/bb503062.aspx) |  [`take`](http://dlang.org/phobos/std_range.html#take)
[`Skip`](https://msdn.microsoft.com/en-us/library/bb358985.aspx) |  [`drop`](http://dlang.org/phobos/std_range.html#.drop)
[`TakeWhile`](https://msdn.microsoft.com/en-us/library/system.linq.enumerable.takewhile.aspx) | [`until`](https://dlang.org/phobos/std_algorithm_searching.html#.until)
[`SkipWhile`](https://msdn.microsoft.com/en-us/library/system.linq.enumerable.skipwhile.aspx) |

Ordering
--------

LINQ   | D
-------|-----
[`OrderBy`](https://msdn.microsoft.com/en-us/library/bb534966.aspx) | [`sort`](http://dlang.org/phobos/std_algorithm_sorting.html#.sort)
`OrderBy` + Comparer | `sort` + `opCmp`
[`OrderByDescending`](https://msdn.microsoft.com/en-us/library/bb534855.aspx) | [`sort`](http://dlang.org/phobos/std_algorithm_sorting.html#.sort)
`OrderByDescending` + Comparer | `sort` + `opCmp`
[`ThenBy`](https://msdn.microsoft.com/en-us/library/bb534743.aspx) | [`multiSort`](http://dlang.org/phobos/std_algorithm_sorting.html#.multiSort)
`ThenBy` + Comparer | `multiSort` + `opCmp`
[`ThenByDescending`](https://msdn.microsoft.com/en-us/library/bb534736.aspx) | [`multiSort`](http://dlang.org/phobos/std_algorithm_sorting.html#.multiSort)
`ThenByDescending` + Comparer | `multiSort` + `opCmp`
[`Reverse`](https://msdn.microsoft.com/en-us/library/bb358497.aspx) | [`retro`](http://dlang.org/phobos/std_range.html#.retro)

Grouping
--------

LINQ   | D
-------|-----
`group` | [`group`]( (D version needs to be sorted!)
[`GroupBy`](https://msdn.microsoft.com/en-us/library/system.linq.enumerable.groupby.aspx) |
GroupJoin |

https://msdn.microsoft.com/en-us/library/mt693097.aspx

Set operators
-------------

LINQ   | D
-------|-----
[`Distinct`](https://msdn.microsoft.com/en-us/library/bb348436.aspx) | [`uniq`]( (D version needs to be sorted!)
[`Union`](https://msdn.microsoft.com/en-us/library/bb341731.aspx) | [`chain`](http://dlang.org/phobos/std_range.html#chain), [`merge`]()
[`Intersect`](https://msdn.microsoft.com/en-us/library/bb460136.aspx) | [`setIntersection`](http://dlang.org/phobos/std_algorithm_setops.html#.setIntersection)
[`Except`](https://msdn.microsoft.com/en-us/library/bb300779.aspx) |

Conversion
----------

LINQ   | D
-------|-----
[`ToArray`](https://msdn.microsoft.com/en-us/library/bb298736.aspx) | [`array`](http://dlang.org/phobos/std_array.html#array)
[`ToList`](https://msdn.microsoft.com/en-us/library/bb549277.aspx) | [`array`](http://dlang.org/phobos/std_array.html#array)
[`ToDictionary`](https://msdn.microsoft.com/en-us/library/bb549277.aspx) | [`assocArray`](http://dlang.org/phobos/std_array.html#.assocArray)
[`ToLookup`](https://msdn.microsoft.com/en-us/library/bb549073.aspx) |
[`Cast`](https://msdn.microsoft.com/en-us/library/bb341406.aspx) |
[`AsQueryable`](https://msdn.microsoft.com/en-us/library/bb353734.aspx) |
[`AsEnumerable`](https://msdn.microsoft.com/en-us/library/bb335435.aspx) |

- OfType

Element operators
-----------------

LINQ   | D
-------|-----
[`First`](https://msdn.microsoft.com/en-us/library/bb291976.aspx) | [`front`](https://dlang.org/phobos/std_range_primitives.html#.front)
[`FirstOrDefault`](https://msdn.microsoft.com/en-us/library/bb340482.aspx) |
[`ElementAt`](https://msdn.microsoft.com/en-us/library/bb299233.aspx) | [`[]`]()
[`ElementAtOrDefault`](https://msdn.microsoft.com/en-us/library/bb494386.aspx)
[`Last`](https://msdn.microsoft.com/en-us/library/bb358775.aspx) | [`back`](https://dlang.org/phobos/std_range_primitives.html#.back)
[`LastOrDefault`](https://msdn.microsoft.com/en-us/library/bb301849.aspx) |
[`Single`](https://msdn.microsoft.com/en-us/library/bb155325.aspx) |
[`SingleOrDefault`](https://msdn.microsoft.com/en-us/library/bb342451.aspx) |

Generation operators
-------------------

LINQ   | D
-------|-----
[`Range`](https://msdn.microsoft.com/en-us/library/system.linq.enumerable.range.aspx) | [`iota`](http://dlang.org/phobos/std_range.html#iota)
[`Repeat`](https://msdn.microsoft.com/en-us/library/bb348899.aspx) | [`repeat`](http://dlang.org/phobos/std_range.html#repeat)
[`Empty`](https://msdn.microsoft.com/en-us/library/bb341042.aspx)
[`DefaultIfEmpty`](https://msdn.microsoft.com/en-us/library/bb360179.aspx)

Quantifiers
------------

LINQ   | D
-------|-----
[`Any`](https://msdn.microsoft.com/en-us/library/bb548541.aspx) | [`any`](http://dlang.org/phobos/std_algorithm_searching.html#.any)
[`All`](https://msdn.microsoft.com/en-us/library/bb534972.aspx) | [`all`](http://dlang.org/phobos/std_algorithm_searching.html#.all)
[`Contains`](https://msdn.microsoft.com/en-us/library/bb352880.aspx) | [`find`](https://dlang.org/phobos/std_algorithm_searching.html#.find), [`canFind`](http://dlang.org/phobos/std_algorithm_searching.html#.canFind)

- find with count?

Aggregate
---------

LINQ   | D
-------|-----
[`Count`](https://msdn.microsoft.com/en-us/library/bb338038.aspx) | [`walkLength`](https://dlang.org/phobos/std_range_primitives.html#.walkLength)
[`Sum`](https://msdn.microsoft.com/en-us/library/bb298138.aspx) | [`sum`](http://dlang.org/phobos/std_algorithm_iteration.html#.sum)
[`Min`](https://msdn.microsoft.com/en-us/library/bb298087.aspx) | [`minElement`]()
[`Max`](https://msdn.microsoft.com/en-us/library/bb335614.aspx) | [`maxElement`]()
[`Average`](https://msdn.microsoft.com/en-us/library/bb354760.aspx) |
[`Aggregate`](https://msdn.microsoft.com/en-us/library/bb548651.aspx) | [`reduce`](http://dlang.org/phobos/std_algorithm_iteration.html#.reduce)
- [`LongCount`](https://msdn.microsoft.com/en-us/library/bb353539.aspx) |

Equality
--------

LINQ   | D
-------|-----
[`SequenceEqual`](https://msdn.microsoft.com/en-us/library/bb348567.aspx)  | [`equal`](http://dlang.org/phobos/std_algorithm_comparison.html#.equal)

Concatenation
-------------

LINQ   | D
-------|-----
[`Concat`](https://msdn.microsoft.com/en-us/library/bb302894.aspx) | [`chain`](http://dlang.org/phobos/std_range.html#.chain)

Query execution
---------------

LINQ   | D
-------|-----
Deferred Execution | Ranges in D are lazy
Immediate Execution | e.g. [`each`](http://dlang.org/phobos/std_algorithm_iteration.html#.each)
Query Reuse | [`save`](https://dlang.org/phobos/std_range_primitives.html#.save)
Custom generator | [`Generator`](https://dlang.org/phobos/std_concurrency.html#.Generator) fibers - why is there no reference in std.range?, [`generate`](http://dlang.org/phobos/std_range.html#.generate)

Joins
-----

- Cross Join
- Group Join
- Cross Join with Group Join
- Left Outer Join

https://msdn.microsoft.com/en-us/library/mt693045.aspx

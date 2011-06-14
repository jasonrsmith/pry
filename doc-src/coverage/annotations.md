
Many projects contain code that can not be covered by unit tests. Having these
portions show up in test coverage statistics is not helpful, so __pry__
provides a way to annotate code to exempt lines from coverage. 

### Example

<!--( block | syntax("py") )-->
$!showsrc("../examples/project/module/two.py")!$
<!--(end)-->

Even though the code within the __nocover__ block is unreachable, it does not
show up in analysis output, and _two.py_ has 100% coverage:

$!examples.pry("examples/project/test", "-s")!$

If a <strong>#begin nocover</strong> directive is not matched by an
<strong>#end nocover</strong> directive, it applies to the remainder of the
file. 


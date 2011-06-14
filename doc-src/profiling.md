
__pry__ includes functionality to allow quick-and-dirty profiling and
benchmarking of code. Consider the following simple example test module:

<!--( block | syntax("py") )-->
$!showsrc("../examples/test_profile.py")!$
<!--(end)-->

The -n flag specifies the number of times each test being run should be
repeated. When the verbosity is bumped up to show individual test timings
(-vv), this is a handy quick comparative benchmarking tool.

$!examples.pry("examples", "-vvn 100000 test_profile.py")!$

The -p flag specifies that a profile run should be done: 

$!examples.pry("examples", "-pn 10000 test_profile.py")!$


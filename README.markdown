# simpleopt.py

## ABOUT

simpleopt.py: A Python module for dead simple command-line option parsing.

Copyright (C) 2009 Patrick Dubroy <pdubroy@gmail.com>
Licensed under the MIT License.

## Description

Best described with an example. The following function:

	def example(input_file, output_file, passes=3, debug=False, quiet=True):
		'''Do some cool stuff and write the results to a new file.

		passes -- the number of passes to make on input_file
		debug -- Print extra debug information to the console
		quiet -- Print as little information as possible
		'''
		pass

wrapped like this:

	import simpleopt
	simpleopt.parse_args(example)
	
allows you to parse the command line options just like you'd expect:

	Usage: example.py [OPTION]... <input_file> <output_file> 

	Do some cool stuff and write the results to a new file.

	Options:
	  -h, --help            show this help message and exit
	  -d, --debug           Print extra debug information to the console
	  -p PASSES, --passes=PASSES
			                the number of passes to make on input_file
	  -q, --quiet           Print as little information as possible

## TODO

- Handle variable-length arguments lists (*args)
- When signalling errors, use the return value rather than an exception
- Better messages when wrong args are passed in

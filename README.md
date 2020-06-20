## Easy Webserving

Sometimes you want a dirt-simple way of serving one or more files via HTTP. You may be in the middle of developing some software and just want to easily test downloading a file, or often it's the easiest way to copy a file from your local machine, etc.

Below are multiple ways of doing so, separated by language.

I encourage you to open a [pull request](https://github.com/profburke/webserving-made-easy/pulls) or [issue](https://github.com/profburke/webserving-made-easy/issues) to add to this list!

- [Go](#go)
- [Python 2](#python2)
- [Python 3](#python3)
- [Ruby](#ruby)
- [Rust](#rust)



### <a name="go"></a>Go

- go exec 'http.ListenAndServe(`:8080`, http.FileServer(http.Dir(`.`)))'

1. ### <a name="python2"></a>Python 2

- python -m SimpleHTTPServer <*port#*>

	> supports GET, HEAD

	> default port 8000

- [woof.py](https://gist.github.com/robcowie/372849)

	> easy, one-time file servring (i.e. quits after file is downloaded)
	
	> when run will display URL where file is served
	
### <a name="python3"></a>Python 3

- python3 -m http.server <*port#*>

	> default port 8000

### <a name="ruby"></a>Ruby

- ruby -run -e httpd .  <-p *port#*>

	> default port 880

### <a name="rust"></a>Rust

- [microserver](https://github.com/robertohuertasm/microserver)

	> cargo install microserver
	
	> From the command line: microserver <*path/to/folder*>
	
	> Will serve single single page applications

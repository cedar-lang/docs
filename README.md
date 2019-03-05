# Getting Started

If you're on Linux or mac and you can launch a command line, it's just:

```
$ git clone --recursive git@github.com:cedar-lang/cedar.git
$ cd cedar
$ make
$ sudo make install
```

This compiles both the command line program and libcedar, placing both of them in `bin` and the standard library is located in `lib` .

{% hint style="info" %}
Cedar is only tested on MacOS and Linux, so there are no guarantees that it will work on windows \(¯\\_\(ツ\)\_/¯\) 
{% endhint %}

## Hello, World

Once you have the interpreter compiled and installed, you can begin writing code! Thing to do is print hello world. So launching `cedar` will throw you into an interactive repl allowing you to enter cedar code and evaluate it on the spot. Here's something to try:  

```scheme
(println "Hello, World")
```

Or something a little more exciting:

```scheme
(map (fn (x) (* x x)) (range 0 100))
```

Awesome! We'll get into what all this means in the next sections. The next step is to read through some of the docs and if you run into any bugs, have any questions, or just want to contribute, any of the following are a good place to start:

* Submit an [Issue](https://github.com/cedar-lang/cedar)
* Tell me on twitter [@nickwanninger](https://twitter.com/nickwanninger)
* Send a pull request


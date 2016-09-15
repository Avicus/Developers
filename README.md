# Avicus Developers

So you want to be an Avicus developer? Follow these easy steps!

* Learn Avicus coding style.
* Discover how we go from development to deployment.
* ????
* Profit!*

In all seriousness, I (and hopefully the rest of the team) expect developers to follow what is documented here. By most accounts, this simply reiterates clean and proper Java programming, good developer practices and more.


## Code Style

We follow Google's [Java Style Guide](http://google.github.io/styleguide/javaguide.html) with a few notable `Exception`'s (hah). Each section in question is linked, with the change explained afterwards.


* [4.1.1](http://google.github.io/styleguide/javaguide.html#s4.1.1-braces-always-used) - 
  Braces are used with `if`, `else`, `for`, `do` and `while` statements, except when the body contains a single statement and there is no following statement that has multiple statements in its body.
    
  ```java
  if (condition())
      return true;
  
  if (condition()) {
      return true;
  }
  else if (otherCondition()) {
      // multiple statements here, so braces everywhere.
      int i = 0;
      return true;
  }
  
  // no braces, since all the statements have single-lined bodies.
  if (condition())
      return true;
  else if (otherCondition())
      return true;
  ```

* [4.1.2](http://google.github.io/styleguide/javaguide.html#s4.1.2-blocks-k-r-style) -
  Line breaks after the closing brace _except_ prior to `catch` clauses.

  ```java
  return () -> {
      while (condition()) {
          method();
      }
  };
  
  return new MyClass() {
      @Override 
      public void method() {
          if (condition()) {
              try {
                  something();
              } catch (ProblemException e) {
                  recover();
              }
          }
          else if (otherCondition()) {
              somethingElse();
          }
          else {
              lastThing();
          }
      }
  };
  ```

* [4.2](http://google.github.io/styleguide/javaguide.html#s4.2-block-indentation) -
  Use 4 spaces (until further notice).

* [4.8.5](https://google.github.io/styleguide/javaguide.html#s4.8.5-annotations) - 
  Field annotations should be on the same line (exceptions may be made when there are two or more annotations on the same field). Method annotations should always be on a separate line.

Google's style guide makes no comment in regards to Java 8 [streams](https://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html). They are acceptable in most cases, as long as they are made readable. Use line breaks. Please.
 
```java 
final List<String> filtered = list.stream()
    .filter(s -> s.startsWith("s"))
    .map(s -> s.toUpperCase())
    .collect(Collectors.toList());
```

Instead of this:

```java
final List<String> filtered = new ArrayList<>();
    for (String word : list) {
        if (word.startsWith("s"))
            filtered.add(word.toUpperCase())
    }
}
```


## Development Environment

* We :heart: [Jetbrains](https://www.jetbrains.com/) products, including [IntelliJ IDEA](https://www.jetbrains.com/idea/). If you don't use it, give it a shot. Other Jetbrains products we use include:
  * [Rubymine](https://jetbrains.com/rubymine) for website development.
  * [DataGrip](https://www.jetbrains.com/datagrip/) for SQL database work.
* Any operating system is acceptable, though Windows can be a hassle at times when working with a number of our tools (Maven, Github/SSH).
* Latest [Maven](https://maven.apache.org/docs/history.html) (3.3.9) for software project and library management.
* [Git](https://git-scm.com/) for version control. Our repository is hosted by [Github](https://github.com/Avicus).


## Application

If you are interested in becoming a developer on the Avicus Network, do so by sending an email to [keenan@avicus.net](mailto:keenan@avicus.net) that addresses the following information (in any style you wish):

* Your full name, what you would like to be called (nickname?) and your age
* Details about your experience with the following languages and technologies: Java, Ruby, Ruby on Rails, HTML/CSS, SQL Databases, Redis, continuous integration (Jenkins), bash/SSH, Git (or Subversion) and Maven
* Links to projects of which you have contributed (open source Github projects, or private projects you wish to share with us)
* Why you are interested in joining our team

Your application may be shared with other developers and admins on the network.

\* We do not currently offer paid positions. All positions on the network are volunteer until further notice.  

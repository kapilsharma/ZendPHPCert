# Basics

Any language, like English or Hindi, consist of many words and grammar. To communicate in any language, we must know most common words and some grammar.

Similarly, a programming language also consist of words (keywords) and grammar (rules). In this chapter, we are going to learn these words and grammar of PHP. In short, we are going to learn the basics of PHP.

A decent PHP programmer must know and remember all the topics of this chapter so that (s)he never need to refer any reference for these topics while programming. These topics are so inportant for a programmer that you can expect comparatively high number of questions from this chapter.

So lets start by writing our first PHP program.

## First Script

So as usual, let's print popular 'Hello world' program.

```php
<?PHP
echo "Hello world!";
?>
```

Here line 1 is PHP opening tag, that we are going to discuss in detail in next section. It simply tell Zend Engine (software which interpret PHP programs) that we are starting code and it must be parsed.

Line 2 is actual PHP statement. Here we are commanding to print string `Hello world!`. So echo statement is used to display the output.

Line 3 is PHP closing tag. Any thing before PHP opening tag and after PHP closing tag will be ignored. Lets try another program, where we will have simple HTML page but also PHP tags with HTML to display some text from PHP.

~~~~~HTML
<html>
  <head>
    <title>Testing PHP inside HTML</title>
  </head>
  <body>
    <h1>Following line is printed by PHP</h1>
    <?PHP
      echo "Printed from PHP";
    ?>
  </body>
</html>
~~~~~

Here line 7-9 are PHP programs. Other then line 7-9, all text will be simply ignored by Zend Engine and will be sent to the output as it is. However line 7-9 will be parsed. There too, line 7 and 9 are simply PHP opening and closing tags. Real PHP code (line 8) will actually be parsed and text 'Printed from PHP' will be sent to the output.

Another important point, we must save this file with `.php` extention. So lets same this file as `hello.php`.

Now we know how PHP programs runs. So lets go through PHP basics in more details.

## PHP Tags

There are four different tags available in PHP. They are:

* Standard tags
* Script tags
* Short tags
* ASP tags

Lets check all available tags in details.

### Standard tags

We already saw standard tags in our *first script*. Each tags have two sets of tags; opening tags and closing tags. Standard opening tags are

> `<?PHP`

Standard closing tags are

> `?>`

As we discussed above, any code between PHP opening and closing tags is valid php script and will be parsed by Zend engine. Any other text, outside php tags will be ignored by Zend engine and sent to output as it is.

As the name suggest, standard php tags are most common and recommended. Standard tags are always available to use, regardless of php.ini settings.

### Script tags

Opening script tag

> `<script language="PHP">`

Closing script tag

> `</script>`

Like standard tags, script tags too are always available, regardless of php.ini settengs. Historically, PHP developers generally uses HTML editors. So they were added for the HTML editors which were capable to ignore script tags but could not understand PHP standard tags.

However due to long syntax, PHP developers never liked them. They are still available but generally not in use. It is not recommended to use script tags.

### Short tags

Opening short tag

> <?

closing short tag

> ?>

Although it is short form of standard PHP tags, it depends on php.ini settings. To work properly, it need `short_open_tag` directive of php.ini.

Since it depends on php.ini settings, its availability could not be guaranteed and **use of short tags is not recommend.**

Short tag also support short hand to print value of a variable as follow

> <?= $variable ?>

above code is equivalent to

```php
<?PHP
  echo $variable;
?>
```

*We will discuss more about variables in next section.*

As of PHP version 5.4, short hand is available regardless of `short_open_tag` setting of php.ini.

### ASP Tags

PHP also support asp tag in case some one prefer them but they are rarely/never used. **We strongly recommend not to use them.** Opening asp tag is

> `<%`

Closing asp tag is

> `%>`

Asp tags depends on `asp_tags` setting of php.ini

> **Short, script and asp tags are available in php but it is strongly recommended not to use them. Only standard tags `<?PHP` & `?>` and shorthand `<?=` are recommended in current PHP applications.**

### Important points about tags

We can mix php tags. Following program is perfectly valid provided `short_open_tag` and `asp_tags` are set in php.ini file.

```php
<html>
  <head>
    <title>Mixing php tags example</title>
  </head>
  <body>
    <h1>Mixing php tags example</h1>
    <?PHP echo "This line is printed between standard and script tags." </script>
    <br/>
    This line is printed in html.
    <br/>
    <? echo "This line is printed between short and asp tags." %>
  </body>
<html>
```

*`echo` in above program is language constructs used to display some data. We will shortly look about language constructs.*

## Language Constructs

We can consider language constructs as basic grammar of php. Php interpreter knows how to handle a language construct and have special rules for them. If you are aware of function in php, language constructs might look like functions but unlike functions, they have special meaning for the interpreter. Language construct in php are:

* echo()
* isset()
* unset()
* include()
* require()
* die()
* empty()

`echo` used in previous example is also a language construct which is used to display some value. We will look about other language constructs in details in the following chapters.

## Variables

As the name suggest, variables are some data that can change over time. In other words, variables are temporary data storage.

To understand variables, please consider following program:

```php
echo 1 + 2;
```

We already discussed `echo` is a language construct, used to display value. It can also display a result of some calculation as above. So the output of above program will be `3`

However both 1 and 2 are constant values and above program will always display sum of 1 and 2, that is 3. What if we want to add different numbers? We must write a new program. This is where variables can help us. Consider following program.

```php
echo $a + $b;
```

This program looks similar to above program. The difference is, it add two variables and we can assign values to these variables at run time, may be taken as input from user or coming from database or any file.

### Variable name

As you can see in above program, a variable name always start with `$` symbol. `$` is not the part of variable name but just tell php interpreter that we are going to write a variable. So in above example, variable names are `a` and `b`.

There are some rules for variable names. Rules are:

* Variable names are case sensitive so `$a` and `$A` are two different variables.
* Variable name may contain letters (English alphabat), digits (0-9) or underscore (_).
* First character must be an letter or underscore.

Based on above rules, below are few examples of valid variable names.

* $name
* $md5Value
* $_phoneNumber
* first_name
* firstName

Example of invalid variable names are:

* $1meter (Variable name can't start with digit)
* $first.name  ('.' can't be used as variable name, only letter, digit and underscore allowed)

### Creating variable

In many programming languages, we must declare a variable before we first use it. However in php, a variable is created as soon as we use it  for first time.

```php
$name = "Kapil";
```

### Declaration and initialization

Since variable can be created as soon as we use it first, we could have variable without any value like

```php
$firstName;
```

This is called declaring a variable. We created a variable but didn't assigned any value to it. However it is recommended to assign some value to the variable as soon as we declare it.

```php
$firstName = "Kapil";
```

In second program, we not only declared variable name but also assigned a value to it. This is called

## Data types

## Operators and Expressions

## Key Concepts

* Zend engine interpret PHP programs.

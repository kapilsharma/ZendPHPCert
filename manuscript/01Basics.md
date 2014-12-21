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

> <?PHP

Standard closing tags are

> ?>

As we discussed above, any code between PHP opening and closing tags is valid php script and will be parsed by Zend engine. Any other text, outside php tags will be ignored by Zend engine and sent to output as it is.

As the name suggest, standard php tags are most common and recommended. Standard tags are always available to use, regardless of php.ini settings.

### Script tags

Opening script tag

> <SCRIPT LANGUAGE="PHP">

Closing script tag

> </SCRIPT>

Like standard tags, script tags too are always available, regardless of php.ini settengs. Historically, PHP developers generally uses HTML editors. So they were added for the HTML editors which were capable to ignore script tags but could not understand PHP standard tags.

However due to long syntax, PHP developers never liked them. They are still available but generally not in use. It is not recommended to use script tags.

### Short tags

Opening short tag

> <?

closing short tag

> ?>

Although it is short form of standard PHP tags, it depends on php.ini settings. To work properly, it need

Short tag also support short form to print value of a variable as follow

> <?= $variable ?>

above code is equivalent to

```php
<?PHP
  echo $variable;
?>
```

*We will discuss more about variables in next section.*

### ASP Tags

## Variables

## Data Types

## Operators and Expressions

## Key Concepts

* Zend engine interprete PHP programs.

# Basics

Any language, like English or Hindi, consist of many words and grammer. To communicate in any language, we must know most common words and some grammer.

Similarly, a programming language also consist of words (keywords) and grammer (rules). In this chapter, we are going to learn these words and grammer of PHP. In short, we are going to learn the basics of PHP.

A decent PHP programmer must know and remember all the topics of this chapter so that (s)he never need to refer any reference for these topics while programming. These topics are so inportant for a programmer that you can expect comparatively high number of questions from this chapter.

So lets start by writing our first PHP program.

## First Script

So as usual, let's print popular 'Hello world' program.

```php
<?PHP
echo "Hello world!";
?>
```

Here line 1 is PHP opening tag, that we are going to discuss in detail in next section. It simply tell Zend Engine (software which interprete PHP programs) that we are starting code and it must be parsed.

Line 2 is actual PHP statement. Here we are commanding to print string `Hello world!`. So echo statement is used to display the output.

Line 3 is PHP closing tag. Any thing before PHP opening tag and after PHP closing tag will be ignored. Lets try another program, where we will have simple HTML page but also PHP tags with HTML to display some text from PHP.

~~~~~HTML
<HTML>
  <HEAD>
    <TITLE>Testing PHP inside HTML</TITLE>
  </HEAD>
  <BODY>
    <H1>Following line is printed by PHP</H1>
    <?PHP
      echo "Printed from PHP";
    ?>
  </BODY>
</HTML>
~~~~~

Here line 7-9 are PHP programs. Other then line 7-9, all text will be simply ignored by Zend Engine and will be sent to the output as it is. However line 7-9 will be parsed. There too, line 7 and 9 are simply PHP opening and closing tags. Real PHP code (line 8) will actually be parsed and text 'Printed from PHP' will be sent to the output.

Another important point, we must save this file with `.php` extention. So lets same this file as `hello.php`.

Now we know how PHP programs runs. So lets go through PHP basics in more details.

## PHP Tags

## Variables

## Constructs

## Data Types

## Operators and Expressions

## Constants

## Key Concepts

* Zend engine interprete PHP programs.
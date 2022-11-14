# Batch file – Programming

**Extensions:**  `.bat` or `.cmd`

**Create batch file :** Open a text file and save it as `.bat`

**How to run file?** just click on that damm file >_<

## Starting Format
```
@echo OFF

PAUSE
```
or
```
@echo off

pause
```
Dosent matter whatever way use. Because these are reserve keywords. What are reserve keywords? [Here More Info](https://en.wikipedia.org/wiki/Reserved_word)

Now, If we don’t put `@echo off` at the top of the script, it will produce an output where ‘echo’ itself will also be displayed. *Test yourself*

`Pause` is used to hold the screen until we press a key. If pause is not used, the output screen will vanish away within a blink of an eye and we won’t be able to see the output.

## Table

<a href="#comment">Comment</a>


## Comment
`::` or `rem`

```
:: This line is commented
```
or
```
REM This line also
```
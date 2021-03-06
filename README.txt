A plugin for Panic Coda which creates shortcuts for common Drupal 
code typing tasks.

Features include:
*DrupalDocBlock
*DrupalFileBlock
*FormatFunctionSugar
*Associative Array
*NestedArray

--------------------------------------------------------------------------------

*DrupalDocBlock: Create a doc block for a function.

  How to use:
  *Select a function and type Command-Option-/
    
  A Drupal code standard doc block will be created.
  Based on these standards: http://drupal.org/node/1354?no_cache=1264546172

  @return only appears if your function has a return value.

An example:

_____________
function my_function($param1, $param2) {
  return 'string';
}
_____________

Becomes:

_____________
/**
 * This function my_function  .
 *
 * @param $param1
 *   Variable.
 *
 * @param  $param2
 *   Variable.
 *
 * @return
 *   Return.
 */
function my_function($param1, $param2) {
  return 'string';
}
_____________





*DrupalFileBlock: Insert the standard block of text that goes at the
 beginning of Drupal files.

  How to use:
  *Type Command->  (Command-Option-4  (remember it by the $ - //  $Id$))

Inserts:

_____________
// $Id$

/**
 * @file
 *
 * Description of file.
 */
_____________

*FormatFunctionSugar: Enter a shorthand for a function and generate function syntax
 properly formatted for Drupal. Creates a doc block and inserts your cursor at 
 a prompt to describe your function (to promote good documentation habits.)

  How to use:

1. Type function shorthand

function functionname $variable $variable $variable : $variable
**Separate arguments by spaces, not commas.
**To add a return variable, enter a colon and then the value you want to return. (optional)

2. Select what you have typed. 

3. Enter: Command-Option-[

_____________
function modulename_taskname $astring $array : $output
_____________

Becomes:

_____________
/**
 * This function modulename_taskname .
 *
 * @param $astring
 *   Variable.
 *
 * @param $array
 *   Variable.
 *
 * @return
 *   Return.
 */

function modulename_taskname($astring, $array) {
  return $output;
}
_____________





*Associative Array

Insert the syntax for an associative array.

How to use:

Enter: Command-Option-r

Inserts:
_____________
array(
  '' => '',
  '' => '',
);

___________





*Nested Array

Insert a two level array.

How to use:

1. Select a variable
2. Enter: Command-Option-R  (Command-Option-Shift-R)


_____________
$var
_____________

Becomes:
_____________
$var = array(
    '' => '',
    '' => array(
        '' => '',
    ),     
  );
_____________

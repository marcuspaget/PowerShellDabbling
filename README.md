# PowerShellDabbling

Capture essence of PowerShell syntax for further details please see https://coding-school.com/category/windows-automation/

## Variables

$single_quoted_string = 'a '
$double_quoted_string = "a string – $x"
Write-Host $single_quote_string
Write-Host $double_quoted_string

' can enforce with [string]

## Integers
[int]$int_one = 1
$int_two = 2
$int_one + $int_two

## Arrays
[array]$arr = @(1,'str_var',5)
$arr += 'add to arr'
$array

## Hash tables
[hashtable]$htab = @{'key1' = 'value1'; 'key2' = 'value2'}
$htab

$htab.Get_Item('key1')
$htab.key1

$htab.Add('newkey',”new added variable”)

$htab.Set_Item(“key1”, “mod_val1”)
$htab.Remove('key1')

If/Then

$a = 1
if ($a -eq 1) {
Write-Host 'a equals 1'
} else {
Write-Host 'a is not equal to 1'
}

' also possible to elseif

} elseif ($a -eq 3) {

Switch

﻿$a = 1

switch ($a) {
1 {“Value 1”}
2 {“Value 2”}
3 {“Value 3”}
default {“Value exceeds threshold.”}
}

$b = “X365”

switch -wildcard ($b) {
“Z*” {“Val Z”}
“Y*” {“Val Y”}
“X*” {“Val X”}
default {“Val outside parameters.”}
}

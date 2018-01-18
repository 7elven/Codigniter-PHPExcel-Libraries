# Codigniter-PHPExcel-Libraries
Easy to use return data to array

<h1>How to use</h1>

1. load libraries in autoload
```php
   $autoload['libraries'] = array('database', 'session', 'xlsx');
```
or in your function 
```php
$this->load->library('xlsx');
```
2. send parameter
```php
list($header,$values) = $this->xlsx->convert('$filename', $first_row_of_header, $date_column);
```
<b>$filename</b> is .xlsx file ex. <b>user.xlsx</b> <br>
<b>$first_row_of_header</b> is first row of header default is <b>1</b> <br>
<b>$date_column</b> is optional it's array of column have date data ex.<b> array('E') or array('E','S') </b><br><br>
3. get value <br><br>
print_r($header); // you will get array of header value <br>
print_r($values); // you will get array of value in sheet<br><br>
4. final you will get code something like this
```php
$this->load->library('xlsx'); 
list($header, $values) = $this->xlsx->convert('test.xlsx', 2, array('E','S')); 
print_r($header); 
print_r($values); 
```

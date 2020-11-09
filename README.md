MarlinValidation

## Использование Validation()


#### **check() : Для проверки волидации.**

<h4>Принимает</h4> 

query( string $source, array $items )
1.Список параметров:source <br> 
2.Список передаваеммых данних:items <br>

<h4>Использования:</h4>

$rules = [ <br>
'email' => [ <br>
'email' => true, <br>
'required' => true, 
], <br>
'username' => [ <br>
'required' => true <br>
'min' => 4
],<br>
'password' => [<br>
'required' => true,<br>
'min' => 6,<br>
'max' => 100
],<br>
'password_again' => [<br>
'required' => true,<br>
'min' => 6,<br>
'max' => 100,<br>
'matches' => 'password'`
]<br>
];


$validation->check($_POST, $rules);



#### **Error() - Метод для получения ошибок валидации.**

<h4> Не принимает никаких параметров </h4> 

<h4>Использования:</h4>

var_dump($validation->error());

<h4>Возврашает:</h4>

Возвращает массив со всеми ошибками.

#### **passed() - Метод для получения информации о пройденной валидации.**

<h4> Не принимает никаких параметров </h4>

<h4>Использования:</h4>

if ($validation->passed()) header("Location: somewhere.php");


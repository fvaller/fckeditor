

```PHP
//para o FCKEditor funciona
include( str_replace('\\', '/' , dirname(__FILE__)) . "/fckeditor/fckeditor.php") ;


<?php editor_texto($row['descricao']); ?>


function editor_texto($conteudo){
  // Automatically calculates the editor base path based on the _samples directory.
  // This is usefull only for these samples. A real application should use something like this:
  // $oFCKeditor->BasePath = '/fckeditor/' ;	// '/fckeditor/' is the default value.
  $oFCKeditor = new FCKeditor('conteudo') ;
  $oFCKeditor->BasePath	=  'fckeditor/' ;
  $oFCKeditor->Value		= $conteudo;
  $oFCKeditor->Height		= 400;
  $oFCKeditor->Create() ;
}

```



```PHP
//para o FCKEditor funciona
include( str_replace('\\', '/' , dirname(__FILE__)) . "/fckeditor/fckeditor.php") ;


//chamar para ciar o editor
//nome do campo: conteudo
editor_texto($row['descricao']);

//funcao para criar 
function editor_texto($conteudo){
  // Automatically calculates the editor base path based on the _samples directory.
  // This is usefull only for these samples. A real application should use something like this:
  // $oFCKeditor->BasePath = '/fckeditor/' ;	// '/fckeditor/' is the default value.
  $oFCKeditor = new FCKeditor('conteudo') ; //definido o nome do campo como 'conteudo'.
  $oFCKeditor->BasePath	=  'fckeditor/' ;
  $oFCKeditor->Value		= $conteudo;
  $oFCKeditor->Height		= 400;
  $oFCKeditor->Create() ;
}

```

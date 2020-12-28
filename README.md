# Como Medir a Força de uma Senha com JavaScript / jQuery
Implemente este script super simples em seus formulários de cadastro e verifique a força da senha que o usuário digitou.

```
function verificaForcaSenha() 
{
	var numeros = /([0-9])/;
	var alfabeto = /([a-zA-Z])/;
	var chEspeciais = /([~,!,@,#,$,%,^,&,*,-,_,+,=,?,>,<])/;

	if($('#password').val().length<6) 
	{
		$('#password-status').html("<span style='color:red'>Fraco, insira no mínimo 6 caracteres</span>");
	} else {  	
		if($('#password').val().match(numeros) && $('#password').val().match(alfabeto) && $('#password').val().match(chEspeciais))
		{            
			$('#password-status').html("<span style='color:green'><b>Forte</b></span>");
		} else {
			$('#password-status').html("<span style='color:orange'>Médio, insira um caracter especial</span>");
		}
	}
}
```

## Como usar o código

Você pode ver uma descrição detalhada de como utilizar este código em seus formulários HTML lendo este artigo do Blogso - 
 [Como Medir a Força de uma Senha com JavaScript / jQuery](https://www.blogson.com.br/como-medir-a-forca-de-uma-senha-com-javascript-jquery/)


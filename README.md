# Verificar Senhas Iguais JS

Uma solução simples para quem precisa comparar se os dois campos de senha foram digitados igualmente.

1º Passo, implemente esse script no seu html.

```js
<script>
 function validarSenha(){
        NovaSenha = document.formCadastro.senha.value;
        1NovaSenha = document.formCadastro.senha1.value;
        if (NovaSenha != 1NovaSenha){ 
             $('#senhaerro').html('Erro, as senhas digitadas não estão corretas.');
             return false;
        }
        return true;
 }
</script>
```

2º Passo, crie o formulário e faça um onSubmit para retornar a função quando o formulário for chamado.

```html
<form method="post" action="cadastrar" id="formCadastro" name="formCadastro" onsubmit="return validarSenha();">
  
</form>
```

3º Passo, dentro do seu formulário insira os inputs das senhas que serão comparadas, lembrando que os nomes dos inputs tem que corresponder ao nome especificados nas variáveis do script.

```html

<input class="form-control" id="senha" name="senha" type="password" placeholder="Digite sua senha" required>

<input class="form-control" id="senha1" name="senha1" type="password"  placeholder="Confirme sua senha" required>

```

4º Insira uma div, ou um span para que retorne a mensagem de erro ao usuário caso os campos não correspondam e insira o botão para dar o  submit no formulário.

```html

<div id="senhaerro" name="senhaerro"></div>

<button type="submit" id="btnCad" onclick="validarSenha()">Cadastrar</button>

```

Um código simples e funcional, espero ter ajudado.

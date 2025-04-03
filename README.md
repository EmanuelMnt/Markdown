# Documentação de código com Markdown
## Feito por: Emanuel Monte
### 3° DS "A" | 03/04/2025

#
```Html
<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>
```
> Aqui se encontra a configuração inicial do html, como a lingua que será usada, definindo o charset e o título da página.
#
``` Html
<body>
    <h2>Calculadora de Fatorial e Verificador de Número Primo</h2>
    <label for="numero">Digite um número:</label>
    <input type="number" id="numero">
    <button onclick="calcular()">Calcular</button>
    <p id="resultado"></p>
    <script>
```
> Aqui é onde se faz o input do usuário, com a interação de um botão
#
```Javascript
        function calcularFatorial(n) {
            if (n === 0) {
                return 1;
            } else {

                return n \* calcularFatorial(n - 1);
            }
        }
```
> Esta é a função para calcular o fatorial do número inserido
#
```Javascript
        function verificarNumeroPrimo(numero) {
            if (numero <= 1) {
                return false;
            }
            for (let i = 2; i < numero; i++) {
                if (numero % i === 0) {
                    return false;
                }
            }
            return true;
        }
```
> Essa é uma função para verificar se o número inserido é primo ou não
#
```Javascript
        function calcular() {
            let numero = parseInt(document.getElementById("numero").value);
            let fatorial = calcularFatorial(numero);
            let primo = verificarNumeroPrimo(numero);
            document.getElementById("resultado").innerHTML =
                "O fatorial de " + numero + " é " + fatorial + "<br>" +
                "O número " + numero + (primo ? " é primo." : " não é primo.");
        }

    </script>
```
> Aqui é mostrado para o usuário o resultado da execução do código

</body>

</html>

# Respostas
1. O código ficou mais organizado e fácil de se analisar, ideal para devidas modificações no código.
2. Em caso de erros no código, você pode com muita mais facilidade identificar onde esteja o problema.
3. Utilizar a indentação e adicionar comentários explicativos
4. É essencial para a organização do código pois em casos de problemas não ter documentado o código, tornará muito mais difícil a manutenção.
5. Facilita a colaboração entre vários desenvolvedores, evitando redundâncias. Também ajuda na expansão do código no futuro.

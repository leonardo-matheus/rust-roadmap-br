# Rust Learning Game - 50 Exercicios Praticos

Guia completo dos 50 exercicios organizados por nivel de dificuldade.

---

## Niveis 1-15: Basico
**Temas:** Variaveis, tipos, println, operadores

---

### Nivel 1: Ola, Rust!
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    // Imprima "Ola, Rust!" na tela
    ___
}
```

**Tarefa:** Use a macro println! para imprimir a mensagem "Ola, Rust!" na tela.

**Respostas Aceitas:**
- `println!("Ola, Rust!");`
- `println!("Ola, Rust!")`
- `print!("Ola, Rust!\n");`

**Explicacao:** A macro println! e usada para imprimir texto na saida padrao com uma nova linha no final. Macros em Rust sao identificadas pelo ! apos o nome.

**Dicas:**
1. Voce precisa usar uma macro que imprime texto...
2. A macro comeca com 'print' e termina com 'ln' para adicionar nova linha...
3. Use println!("sua mensagem aqui");

**Erro Comum:** `println("Ola, Rust!");`
> Esqueceu o '!' apos println. Em Rust, println e uma macro, nao uma funcao, e macros sempre precisam do '!' para serem invocadas.

---

### Nivel 2: Minha Primeira Variavel
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    ___ nome = "Maria";
    println!("Ola, {}!", nome);
}
```

**Tarefa:** Declare uma variavel imutavel usando a palavra-chave correta.

**Respostas Aceitas:**
- `let`

**Explicacao:** Em Rust, usamos 'let' para declarar variaveis. Por padrao, variaveis sao imutaveis, o que significa que seu valor nao pode ser alterado apos a atribuicao.

**Dicas:**
1. Qual palavra-chave e usada para criar variaveis em Rust?
2. Comeca com 'l' e tem 3 letras...
3. Use 'let' para declarar variaveis.

**Erro Comum:** `var nome = "Maria";`
> Rust nao usa 'var' como JavaScript. A palavra-chave correta e 'let'.

---

### Nivel 3: Variavel Mutavel
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let ___ idade = 25;
    idade = 26;
    println!("Idade: {}", idade);
}
```

**Tarefa:** Adicione a palavra-chave que permite que a variavel seja modificada.

**Respostas Aceitas:**
- `mut`

**Explicacao:** Para tornar uma variavel mutavel em Rust, adicionamos 'mut' apos 'let'. Isso permite que o valor seja alterado posteriormente.

**Dicas:**
1. Variaveis em Rust sao imutaveis por padrao. Qual palavra torna ela mutavel?
2. A palavra e uma abreviacao de 'mutable'...
3. Use 'mut' entre 'let' e o nome da variavel.

**Erro Comum:** `let idade = 25; idade = 26;`
> Sem 'mut', a variavel e imutavel. O erro seria: 'cannot assign twice to immutable variable'.

---

### Nivel 4: Tipo Inteiro
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let quantidade: ___ = 42;
    println!("Quantidade: {}", quantidade);
}
```

**Tarefa:** Especifique o tipo inteiro de 32 bits com sinal.

**Respostas Aceitas:**
- `i32`

**Explicacao:** i32 e um inteiro de 32 bits com sinal (pode ser positivo ou negativo). E o tipo inteiro padrao em Rust quando nao especificado.

**Dicas:**
1. Inteiros com sinal comecam com 'i' em Rust...
2. 32 bits significa que o numero tem esse sufixo...
3. O tipo e 'i32'.

**Erro Comum:** `int`
> Rust nao usa 'int'. Os tipos inteiros sao i8, i16, i32, i64, i128 (com sinal) ou u8, u16, u32, u64, u128 (sem sinal).

---

### Nivel 5: Tipo Flutuante
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let pi: ___ = 3.14159;
    println!("Pi = {}", pi);
}
```

**Tarefa:** Especifique o tipo de ponto flutuante de 64 bits.

**Respostas Aceitas:**
- `f64`

**Explicacao:** f64 e um numero de ponto flutuante de 64 bits (double precision). E o tipo padrao para numeros decimais em Rust.

**Dicas:**
1. Tipos de ponto flutuante comecam com 'f'...
2. 64 bits oferece mais precisao que 32...
3. O tipo e 'f64'.

**Erro Comum:** `float`
> Rust nao usa 'float' ou 'double'. Use f32 ou f64 para numeros decimais.

---

### Nivel 6: Tipo Booleano
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let ativo: bool = ___;
    if ativo {
        println!("Sistema ativo!");
    }
}
```

**Tarefa:** Atribua o valor verdadeiro a variavel booleana.

**Respostas Aceitas:**
- `true`

**Explicacao:** Em Rust, os valores booleanos sao 'true' e 'false' (em minusculas). Diferente de outras linguagens, Rust nao aceita 1 ou 0 como booleanos.

**Dicas:**
1. Booleanos tem dois valores possiveis: verdadeiro ou falso...
2. Em ingles e minusculo...
3. Use 'true' para verdadeiro.

**Erro Comum:** `True`
> Rust usa 'true' em minusculas, nao 'True'. Rust e case-sensitive.

---

### Nivel 7: Tipo Caractere
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let letra: char = ___;
    println!("Letra: {}", letra);
}
```

**Tarefa:** Atribua o caractere 'A' a variavel. Lembre-se: caracteres usam aspas simples!

**Respostas Aceitas:**
- `'A'`

**Explicacao:** O tipo char em Rust representa um unico caractere Unicode e usa aspas simples. Strings usam aspas duplas.

**Dicas:**
1. Caracteres em Rust usam aspas simples, nao duplas...
2. E so uma letra entre aspas simples...
3. Use 'A' (com aspas simples).

**Erro Comum:** `"A"`
> Aspas duplas criam uma String (&str), nao um char. Use aspas simples para caracteres: 'A'.

---

### Nivel 8: Interpolacao Basica
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let nome = "Carlos";
    let idade = 30;
    println!("___ tem ___ anos", nome, idade);
}
```

**Tarefa:** Complete os placeholders para interpolar as variaveis.

**Respostas Aceitas:**
- `{} {}`
- `{}{}`

**Explicacao:** Em Rust, {} e um placeholder na macro println! que sera substituido pelos argumentos na ordem em que aparecem.

**Dicas:**
1. Placeholders sao representados por chaves...
2. Use um par de chaves vazio para cada variavel...
3. Use {} para cada valor a ser interpolado.

**Erro Comum:** `%s %d`
> Rust nao usa formatacao estilo C como %s ou %d. Use {} para todos os tipos basicos.

---

### Nivel 9: Operacao Aritmetica
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let a = 10;
    let b = 3;
    let soma = a ___ b;
    println!("Soma: {}", soma); // Deve imprimir 13
}
```

**Tarefa:** Use o operador correto para somar os dois numeros.

**Respostas Aceitas:**
- `+`

**Explicacao:** O operador + realiza adicao em Rust. Os operadores aritmeticos basicos sao: + (soma), - (subtracao), * (multiplicacao), / (divisao), % (resto).

**Dicas:**
1. Qual simbolo matematico representa adicao?
2. E o mesmo usado na maioria das linguagens...
3. Use o operador +

**Erro Comum:** `a.add(b)`
> Embora .add() exista via trait, para operacoes simples use o operador + diretamente.

---

### Nivel 10: Divisao Inteira
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let a: i32 = 17;
    let b: i32 = 5;
    let resultado = a ___ b;
    println!("Resultado: {}", resultado); // Deve imprimir 3
}
```

**Tarefa:** Use o operador de divisao. Note que entre inteiros, o resultado e inteiro.

**Respostas Aceitas:**
- `/`

**Explicacao:** A divisao entre inteiros em Rust resulta em um inteiro (truncado). 17 / 5 = 3 (nao 3.4). Para resultado decimal, use f64.

**Dicas:**
1. Qual simbolo representa divisao?
2. E a barra comum usada em programacao...
3. Use o operador /

**Erro Comum:** `17 / 5 esperando 3.4`
> Divisao entre inteiros sempre retorna inteiro. Para 3.4, converta para f64: 17.0 / 5.0

---

### Nivel 11: Resto da Divisao
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let numero = 17;
    let resto = numero ___ 5;
    println!("Resto: {}", resto); // Deve imprimir 2
}
```

**Tarefa:** Use o operador de modulo (resto da divisao).

**Respostas Aceitas:**
- `%`

**Explicacao:** O operador % retorna o resto da divisao inteira. 17 % 5 = 2 porque 17 = 5*3 + 2.

**Dicas:**
1. Este operador e chamado de 'modulo'...
2. E o simbolo de porcentagem...
3. Use o operador %

**Erro Comum:** `mod`
> Em Rust, 'mod' e usado para modulos (organizacao de codigo). Para resto da divisao, use %.

---

### Nivel 12: Comparacao de Igualdade
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let a = 5;
    let b = 5;
    let sao_iguais = a ___ b;
    println!("Sao iguais? {}", sao_iguais); // true
}
```

**Tarefa:** Use o operador de comparacao de igualdade.

**Respostas Aceitas:**
- `==`

**Explicacao:** O operador == compara se dois valores sao iguais e retorna um bool. Um unico = e atribuicao, nao comparacao.

**Dicas:**
1. Para comparar, nao basta um sinal de igual...
2. Voce precisa de dois sinais de igual...
3. Use == para comparacao.

**Erro Comum:** `a = b (retornando bool)`
> Um unico = e atribuicao, nao comparacao. Use == para verificar igualdade.

---

### Nivel 13: Comparacao Maior Que
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let idade = 18;
    let pode_votar = idade ___ 16;
    println!("Pode votar? {}", pode_votar); // true
}
```

**Tarefa:** Use o operador que verifica se idade e maior ou igual a 16.

**Respostas Aceitas:**
- `>=`

**Explicacao:** O operador >= verifica se o valor da esquerda e maior ou igual ao da direita. Outros operadores: >, <, <=, ==, !=

**Dicas:**
1. Precisa verificar 'maior ou igual'...
2. Combine > com =...
3. Use >= (maior ou igual).

**Erro Comum:** `=>`
> A ordem importa! E >= (maior ou igual), nao =>. O simbolo => e usado em match arms.

---

### Nivel 14: Operador Logico E
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let tem_carteira = true;
    let tem_18_anos = true;
    let pode_dirigir = tem_carteira ___ tem_18_anos;
    println!("Pode dirigir? {}", pode_dirigir);
}
```

**Tarefa:** Use o operador logico AND para verificar ambas as condicoes.

**Respostas Aceitas:**
- `&&`

**Explicacao:** O operador && (AND logico) retorna true apenas se ambos os operandos forem true. E avaliado em curto-circuito.

**Dicas:**
1. Voce precisa do operador logico 'E'...
2. Sao dois simbolos de 'e comercial'...
3. Use && para AND logico.

**Erro Comum:** `and`
> Rust nao usa 'and' como palavra-chave para logica booleana. Use &&.

---

### Nivel 15: Operador Logico OU
**Categoria:** Basico

**Codigo de Contexto:**
```rust
fn main() {
    let tem_pix = false;
    let tem_cartao = true;
    let pode_pagar = tem_pix ___ tem_cartao;
    println!("Pode pagar? {}", pode_pagar); // true
}
```

**Tarefa:** Use o operador logico OR para verificar se pelo menos uma condicao e verdadeira.

**Respostas Aceitas:**
- `||`

**Explicacao:** O operador || (OR logico) retorna true se pelo menos um dos operandos for true. Tambem usa avaliacao em curto-circuito.

**Dicas:**
1. Voce precisa do operador logico 'OU'...
2. Sao duas barras verticais...
3. Use || para OR logico.

**Erro Comum:** `or`
> Rust nao usa 'or' como palavra-chave. Use || para OR logico.

---

## Niveis 16-25: Controle de Fluxo
**Temas:** if, match, loops

---

### Nivel 16: If Simples
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let numero = 10;
    ___ numero > 5 {
        println!("Maior que 5!");
    }
}
```

**Tarefa:** Complete com a palavra-chave condicional.

**Respostas Aceitas:**
- `if`

**Explicacao:** A estrutura 'if' em Rust avalia uma condicao booleana. Diferente de outras linguagens, a condicao NAO precisa estar entre parenteses.

**Dicas:**
1. Qual palavra-chave e usada para condicionais?
2. E a mesma de outras linguagens...
3. Use 'if' antes da condicao.

**Erro Comum:** `if (numero > 5)`
> Em Rust, os parenteses ao redor da condicao sao desnecessarios e considerados ma pratica. Use: if numero > 5

---

### Nivel 17: If-Else
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let numero = 3;
    if numero > 5 {
        println!("Grande");
    } ___ {
        println!("Pequeno");
    }
}
```

**Tarefa:** Adicione a clausula para o caso alternativo.

**Respostas Aceitas:**
- `else`

**Explicacao:** O bloco 'else' e executado quando a condicao do 'if' e falsa. Em Rust, 'else' deve estar na mesma linha que a chave de fechamento do if.

**Dicas:**
1. Qual palavra indica 'caso contrario'?
2. E o complemento do 'if'...
3. Use 'else' para o caso alternativo.

**Erro Comum:** `}\nelse {`
> Em Rust, o 'else' deve estar na mesma linha que '}': '} else {', nao em linha separada.

---

### Nivel 18: If como Expressao
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let condicao = true;
    let numero = if condicao { 5 } ___ { 10 };
    println!("Numero: {}", numero);
}
```

**Tarefa:** Complete para que o if funcione como expressao que retorna um valor.

**Respostas Aceitas:**
- `else`

**Explicacao:** Em Rust, 'if' e uma expressao que retorna valor. Ambos os bracos devem retornar o mesmo tipo. Note a ausencia de ponto-e-virgula nos valores retornados.

**Dicas:**
1. O if precisa de um caso alternativo...
2. Sem else, o if nao pode retornar valor...
3. Use 'else' para completar a expressao.

**Erro Comum:** `let numero = if condicao { 5 };`
> Quando if e usado como expressao, deve ter else. Sem else, o tipo seria () quando a condicao e falsa.

---

### Nivel 19: Else If
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let nota = 75;
    if nota >= 90 {
        println!("A");
    } ___ nota >= 70 {
        println!("B");
    } else {
        println!("C");
    }
}
```

**Tarefa:** Adicione a verificacao intermediaria.

**Respostas Aceitas:**
- `else if`

**Explicacao:** Use 'else if' para verificar multiplas condicoes em sequencia. A primeira condicao verdadeira e executada, as demais sao ignoradas.

**Dicas:**
1. Voce precisa de uma combinacao de duas palavras-chave...
2. E o 'senao se'...
3. Use 'else if' para condicoes adicionais.

**Erro Comum:** `elif`
> Rust nao usa 'elif' como Python. Use 'else if' (duas palavras separadas).

---

### Nivel 20: Match Basico
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let numero = 2;
    ___ numero {
        1 => println!("Um"),
        2 => println!("Dois"),
        _ => println!("Outro"),
    }
}
```

**Tarefa:** Use a expressao de pattern matching do Rust.

**Respostas Aceitas:**
- `match`

**Explicacao:** O 'match' e uma poderosa expressao de pattern matching em Rust. Deve ser exaustivo - cobrir todos os casos possiveis. O '_' e um padrao curinga.

**Dicas:**
1. Rust tem uma expressao poderosa para comparacao de padroes...
2. Comeca com 'm' e tem 5 letras...
3. Use 'match' para pattern matching.

**Erro Comum:** `switch numero`
> Rust nao tem 'switch'. Use 'match', que e mais poderoso e seguro.

---

### Nivel 21: Match Curinga
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let dia = 5;
    match dia {
        1 => println!("Segunda"),
        7 => println!("Domingo"),
        ___ => println!("Dia util"),
    }
}
```

**Tarefa:** Adicione o padrao que captura todos os outros casos.

**Respostas Aceitas:**
- `_`

**Explicacao:** O underscore '_' e um padrao curinga em match. Ele captura qualquer valor nao coberto pelos padroes anteriores, tornando o match exaustivo.

**Dicas:**
1. Existe um caractere especial para 'qualquer coisa'...
2. E usado para ignorar valores em Rust...
3. Use '_' como padrao curinga.

**Erro Comum:** `default =>`
> Rust nao usa 'default' como em switch/case. Use '_' como padrao curinga.

---

### Nivel 22: Loop Infinito
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let mut contador = 0;
    ___ {
        contador += 1;
        if contador == 3 {
            break;
        }
        println!("Contagem: {}", contador);
    }
}
```

**Tarefa:** Use a palavra-chave para criar um loop infinito.

**Respostas Aceitas:**
- `loop`

**Explicacao:** O 'loop' cria um loop infinito que so termina com 'break'. E diferente de 'while true' pois o compilador sabe que sempre executa pelo menos uma vez.

**Dicas:**
1. Rust tem uma palavra-chave especifica para loops infinitos...
2. Tem 4 letras e significa 'repeticao'...
3. Use 'loop' para loop infinito.

**Erro Comum:** `while true`
> Embora funcione, Rust prefere 'loop' para loops infinitos. E mais idiomatico e permite 'break' com valor.

---

### Nivel 23: While Loop
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    let mut numero = 5;
    ___ numero > 0 {
        println!("{}!", numero);
        numero -= 1;
    }
    println!("Lancar!");
}
```

**Tarefa:** Use o loop condicional.

**Respostas Aceitas:**
- `while`

**Explicacao:** O 'while' executa o bloco enquanto a condicao for verdadeira. A condicao e verificada antes de cada iteracao.

**Dicas:**
1. Qual loop executa 'enquanto' uma condicao for verdadeira?
2. E a mesma palavra de outras linguagens...
3. Use 'while' seguido da condicao.

**Erro Comum:** `while (numero > 0)`
> Como no 'if', parenteses ao redor da condicao sao desnecessarios em Rust.

---

### Nivel 24: For com Range
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    ___ i in 1..4 {
        println!("Numero: {}", i);
    }
    // Imprime 1, 2, 3
}
```

**Tarefa:** Use o loop for para iterar sobre um range.

**Respostas Aceitas:**
- `for`

**Explicacao:** O 'for' em Rust itera sobre qualquer iterador. O range 1..4 gera valores de 1 ate 3 (exclusivo). Para incluir 4, use 1..=4.

**Dicas:**
1. Qual loop e usado para iterar sobre colecoes?
2. E a mesma palavra de outras linguagens...
3. Use 'for' para iterar.

**Erro Comum:** `for (i = 1; i < 4; i++)`
> Rust nao usa for no estilo C. Use 'for variavel in iterador' com ranges como 1..4.

---

### Nivel 25: Range Inclusivo
**Categoria:** Controle de Fluxo

**Codigo de Contexto:**
```rust
fn main() {
    for i in 1___5 {
        println!("{}", i);
    }
    // Deve imprimir 1, 2, 3, 4, 5
}
```

**Tarefa:** Modifique o range para incluir o numero 5.

**Respostas Aceitas:**
- `..=`

**Explicacao:** O range 1..=5 e inclusivo, gerando valores de 1 ate 5 (incluindo 5). O range 1..5 seria exclusivo (1 ate 4).

**Dicas:**
1. Ranges exclusivos usam '..', mas inclusivos precisam de algo mais...
2. Adicione um sinal de igual...
3. Use '..=' para range inclusivo.

**Erro Comum:** `1...5`
> Tres pontos '...' nao e valido. Use '..' para exclusivo ou '..=' para inclusivo.

---

## Niveis 26-35: Funcoes e Ownership
**Temas:** Funcoes, parametros, retorno, ownership, borrowing

---

### Nivel 26: Declarando Funcao
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
___ saudar() {
    println!("Ola!");
}

fn main() {
    saudar();
}
```

**Tarefa:** Use a palavra-chave para declarar uma funcao.

**Respostas Aceitas:**
- `fn`

**Explicacao:** Em Rust, funcoes sao declaradas com 'fn' seguido do nome, parametros entre parenteses e o corpo entre chaves.

**Dicas:**
1. E uma abreviacao de 'function'...
2. Tem apenas 2 letras...
3. Use 'fn' para declarar funcoes.

**Erro Comum:** `function saudar()`
> Rust usa 'fn', nao 'function' ou 'func'. E mais conciso.

---

### Nivel 27: Funcao com Parametro
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn saudar(nome___ String) {
    println!("Ola, {}!", nome);
}

fn main() {
    saudar(String::from("Maria"));
}
```

**Tarefa:** Adicione a sintaxe correta para especificar o tipo do parametro.

**Respostas Aceitas:**
- `:`

**Explicacao:** Em Rust, tipos de parametros sao obrigatorios e especificados com ':' apos o nome. Exemplo: fn func(param: Tipo)

**Dicas:**
1. Voce precisa separar o nome do tipo...
2. E um caractere de pontuacao comum em tipagem...
3. Use ':' entre o nome e o tipo.

**Erro Comum:** `fn saudar(String nome)`
> A ordem e nome: Tipo, nao Tipo nome como em Java/C. E o ':' e obrigatorio.

---

### Nivel 28: Funcao com Retorno
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn dobro(x: i32) ___ i32 {
    x * 2
}

fn main() {
    let resultado = dobro(5);
    println!("Dobro: {}", resultado);
}
```

**Tarefa:** Adicione a sintaxe que indica o tipo de retorno da funcao.

**Respostas Aceitas:**
- `->`

**Explicacao:** O tipo de retorno e especificado com -> apos os parametros. Note que a ultima expressao (sem ;) e retornada automaticamente.

**Dicas:**
1. A sintaxe de retorno usa uma 'seta'...
2. E formada por um traco e um maior-que...
3. Use '->' para indicar tipo de retorno.

**Erro Comum:** `fn dobro(x: i32): i32`
> Rust usa '->' para tipo de retorno, nao ':' como em TypeScript ou Python type hints.

---

### Nivel 29: Retorno Implicito
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn quadrado(x: i32) -> i32 {
    x * x___
}

fn main() {
    println!("Quadrado de 4: {}", quadrado(4));
}
```

**Tarefa:** A funcao deve retornar o resultado. O que NAO deve ter no final da expressao?

**Respostas Aceitas:**
- `` (vazio)

**Explicacao:** Em Rust, a ultima expressao de uma funcao (sem ponto-e-virgula) e retornada automaticamente. Adicionar ';' transformaria em statement e retornaria ().

**Dicas:**
1. Expressoes retornam valores, statements nao...
2. O ponto-e-virgula transforma expressao em statement...
3. Nao coloque ';' - deixe vazio para retorno implicito.

**Erro Comum:** `x * x;`
> Com ';', a expressao vira statement e a funcao retorna (). Remova o ';' para retorno implicito.

---

### Nivel 30: Return Explicito
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn valor_absoluto(x: i32) -> i32 {
    if x < 0 {
        ___ -x;
    }
    x
}

fn main() {
    println!("Absoluto de -5: {}", valor_absoluto(-5));
}
```

**Tarefa:** Adicione a palavra-chave para retorno antecipado.

**Respostas Aceitas:**
- `return`

**Explicacao:** Use 'return' para retornar antes do final da funcao. No final, o retorno implicito (sem return) e preferido.

**Dicas:**
1. Qual palavra-chave forca o retorno imediato?
2. E a mesma de outras linguagens...
3. Use 'return' para retorno explicito.

**Erro Comum:** `return -x (sem ponto-e-virgula)`
> Com 'return', o ponto-e-virgula e necessario pois e um statement. Sem 'return', omita o ';'.

---

### Nivel 31: Ownership Basico
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = s1___;
    println!("s2: {}", s2);
    // s1 ainda deve ser valido!
    println!("s1: {}", s1);
}
```

**Tarefa:** Clone a String para que s1 continue valido apos a atribuicao.

**Respostas Aceitas:**
- `.clone()`

**Explicacao:** Em Rust, atribuir uma String a outra variavel MOVE a ownership. Para manter s1 valido, usamos .clone() para criar uma copia profunda.

**Dicas:**
1. Voce precisa criar uma copia da String...
2. Existe um metodo para clonar valores...
3. Use .clone() para copiar dados do heap.

**Erro Comum:** `let s2 = s1; println!(s1);`
> Isso causa erro 'value borrowed after move'. String nao implementa Copy, entao a ownership e movida. Use .clone().

---

### Nivel 32: Referencia Imutavel
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn tamanho(s: ___String) -> usize {
    s.len()
}

fn main() {
    let texto = String::from("Rust");
    let tam = tamanho(&texto);
    println!("'{}' tem {} caracteres", texto, tam);
}
```

**Tarefa:** Use referencia para emprestar a String sem tomar ownership.

**Respostas Aceitas:**
- `&`

**Explicacao:** O & cria uma referencia (borrow) que permite usar o valor sem tomar ownership. A funcao recebe &String em vez de String.

**Dicas:**
1. Voce quer 'emprestar' a String, nao tomar posse...
2. Qual simbolo cria uma referencia em Rust?
3. Use '&' para criar uma referencia.

**Erro Comum:** `fn tamanho(s: String)`
> Sem &, a funcao toma ownership de texto e ele nao pode mais ser usado em main. Use &String para emprestar.

---

### Nivel 33: Referencia Mutavel
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn adicionar_exclamacao(s: &___ String) {
    s.push('!');
}

fn main() {
    let mut texto = String::from("Ola");
    adicionar_exclamacao(&mut texto);
    println!("{}", texto); // Ola!
}
```

**Tarefa:** Permita que a funcao modifique a String emprestada.

**Respostas Aceitas:**
- `mut`

**Explicacao:** Para modificar um valor emprestado, a referencia deve ser mutavel: &mut T. So pode existir uma referencia mutavel por vez.

**Dicas:**
1. Referencias imutaveis nao permitem modificacao...
2. Voce precisa de uma referencia que permite mudanca...
3. Use &mut para referencia mutavel.

**Erro Comum:** `&String mas tentando modificar`
> Referencias imutaveis (&T) nao permitem modificacao. Use &mut T e passe &mut variavel.

---

### Nivel 34: String Slice
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn primeira_palavra(s: &String) -> ___str {
    &s[..5]
}

fn main() {
    let texto = String::from("Hello World");
    let palavra = primeira_palavra(&texto);
    println!("Primeira: {}", palavra);
}
```

**Tarefa:** Use o tipo correto para uma fatia de string.

**Respostas Aceitas:**
- `&`

**Explicacao:** &str e um 'string slice' - uma referencia a parte de uma String. E mais flexivel que &String pois aceita ambos &String e &str.

**Dicas:**
1. O retorno e uma 'fatia' da string original...
2. str sozinho nao tem tamanho conhecido, precisa de referencia...
3. Use &str (referencia para string slice).

**Erro Comum:** `-> String`
> Retornar String copiaria os dados. &str e uma referencia eficiente a string original.

---

### Nivel 35: Slice de Array
**Categoria:** Funcoes e Ownership

**Codigo de Contexto:**
```rust
fn main() {
    let numeros = [1, 2, 3, 4, 5];
    let slice = &numeros[1___4];
    println!("{:?}", slice); // [2, 3, 4]
}
```

**Tarefa:** Complete a sintaxe de range para o slice.

**Respostas Aceitas:**
- `..`

**Explicacao:** Slices usam a sintaxe [inicio..fim] onde fim e exclusivo. &numeros[1..4] retorna elementos nos indices 1, 2, 3.

**Dicas:**
1. A sintaxe de range e a mesma usada em for loops...
2. Dois pontos entre inicio e fim...
3. Use '..' para criar um range.

**Erro Comum:** `&numeros[1:4]`
> Rust usa '..' para ranges, nao ':' como Python. Use &array[inicio..fim].

---

## Niveis 36-45: Structs, Enums e Collections
**Temas:** Estruturas de dados, enumeracoes, Vec, HashMap

---

### Nivel 36: Definindo Struct
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
___ Pessoa {
    nome: String,
    idade: u32,
}

fn main() {
    let p = Pessoa {
        nome: String::from("Ana"),
        idade: 25,
    };
    println!("{} tem {} anos", p.nome, p.idade);
}
```

**Tarefa:** Use a palavra-chave para definir uma estrutura.

**Respostas Aceitas:**
- `struct`

**Explicacao:** Structs sao tipos personalizados que agrupam dados relacionados. Definimos com 'struct Nome { campos }'. Campos sao acessados com '.'

**Dicas:**
1. E similar a classes em outras linguagens, mas sem metodos por padrao...
2. A palavra vem de 'structure'...
3. Use 'struct' para definir estruturas.

**Erro Comum:** `class Pessoa`
> Rust nao tem 'class'. Use 'struct' para dados e 'impl' para metodos.

---

### Nivel 37: Instanciando Struct
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
struct Ponto {
    x: i32,
    y: i32,
}

fn main() {
    let p = Ponto { x___ 10, y: 20 };
    println!("Ponto: ({}, {})", p.x, p.y);
}
```

**Tarefa:** Use a sintaxe correta para atribuir valor ao campo.

**Respostas Aceitas:**
- `:`

**Explicacao:** Ao criar instancias de struct, usamos 'campo: valor'. Se a variavel tem o mesmo nome do campo, podemos usar apenas 'campo' (field init shorthand).

**Dicas:**
1. A sintaxe e similar a definicao...
2. Campo e valor sao separados por...
3. Use ':' entre nome do campo e valor.

**Erro Comum:** `Ponto { x = 10, y = 20 }`
> Na sintaxe de struct, use ':' nao '='. O '=' e para atribuicao normal de variaveis.

---

### Nivel 38: Metodo em Struct
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
struct Retangulo {
    largura: u32,
    altura: u32,
}

___ Retangulo {
    fn area(&self) -> u32 {
        self.largura * self.altura
    }
}

fn main() {
    let r = Retangulo { largura: 10, altura: 5 };
    println!("Area: {}", r.area());
}
```

**Tarefa:** Use a palavra-chave para implementar metodos na struct.

**Respostas Aceitas:**
- `impl`

**Explicacao:** O bloco 'impl' (implementation) define metodos para um tipo. O primeiro parametro '&self' e a instancia atual (similar a 'this' em outras linguagens).

**Dicas:**
1. E uma abreviacao de 'implementation'...
2. Tem 4 letras...
3. Use 'impl' para implementar metodos.

**Erro Comum:** `struct Retangulo { fn area() }`
> Metodos nao ficam dentro da struct, mas em um bloco 'impl' separado.

---

### Nivel 39: Definindo Enum
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
___ Direcao {
    Norte,
    Sul,
    Leste,
    Oeste,
}

fn main() {
    let dir = Direcao::Norte;
    match dir {
        Direcao::Norte => println!("Indo para o Norte!"),
        _ => println!("Outra direcao"),
    }
}
```

**Tarefa:** Use a palavra-chave para definir um tipo enumerado.

**Respostas Aceitas:**
- `enum`

**Explicacao:** Enums definem um tipo com variantes fixas. Acessamos variantes com '::'. Enums em Rust podem ter dados associados (como Option e Result).

**Dicas:**
1. E a abreviacao de 'enumeration'...
2. Tem 4 letras...
3. Use 'enum' para definir enumeracoes.

**Erro Comum:** `const NORTE = 0; const SUL = 1;`
> Embora possivel, enums sao mais seguros e expressivos que constantes numericas.

---

### Nivel 40: Enum com Dados
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
enum Mensagem {
    Texto(String),
    Numero(i32),
}

fn main() {
    let m = Mensagem::Texto(String::from("Ola"));
    match m {
        Mensagem::Texto(s) ___ println!("Texto: {}", s),
        Mensagem::Numero(n) => println!("Numero: {}", n),
    }
}
```

**Tarefa:** Complete a sintaxe do braco do match.

**Respostas Aceitas:**
- `=>`

**Explicacao:** No match, cada padrao e seguido por '=>' e a expressao a executar. Enum variants podem carregar dados que sao extraidos no pattern matching.

**Dicas:**
1. E uma 'seta gorda' que separa padrao de acao...
2. Diferente de '->', usa sinal de igual...
3. Use '=>' entre padrao e expressao.

**Erro Comum:** `Mensagem::Texto(s) -> println!`
> Em match, use '=>' (fat arrow), nao '->' que e para tipos de retorno.

---

### Nivel 41: Criando Vector
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
fn main() {
    let numeros: Vec<i32> = ___![];
    println!("Vector vazio: {:?}", numeros);
}
```

**Tarefa:** Use a macro para criar um vector vazio.

**Respostas Aceitas:**
- `vec`

**Explicacao:** vec![] e uma macro que cria um Vector. Para vazio: vec![] ou Vec::new(). Com valores: vec![1, 2, 3]. Vectors sao arrays dinamicos.

**Dicas:**
1. E uma macro, entao precisa de '!'...
2. O nome e uma abreviacao de 'vector'...
3. Use 'vec!' para a macro de vector.

**Erro Comum:** `[1, 2, 3]`
> Isso cria um array fixo, nao um Vector. Use vec![1, 2, 3] para Vector dinamico.

---

### Nivel 42: Adicionando ao Vector
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
fn main() {
    let mut numeros = vec![1, 2, 3];
    numeros.___(4);
    println!("{:?}", numeros); // [1, 2, 3, 4]
}
```

**Tarefa:** Use o metodo para adicionar um elemento ao final.

**Respostas Aceitas:**
- `push`

**Explicacao:** O metodo push() adiciona um elemento ao final do Vector. O Vector deve ser mut para permitir modificacao.

**Dicas:**
1. E o mesmo nome usado em outras linguagens para adicionar ao final...
2. Comeca com 'p' e 'empurra' elementos...
3. Use 'push' para adicionar elementos.

**Erro Comum:** `numeros.add(4)`
> Rust usa 'push' nao 'add' ou 'append' para Vectors.

---

### Nivel 43: Acessando Vector
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
fn main() {
    let nums = vec![10, 20, 30];
    let segundo = nums.___(1);
    match segundo {
        Some(valor) => println!("Valor: {}", valor),
        None => println!("Indice invalido"),
    }
}
```

**Tarefa:** Use o metodo seguro para acessar por indice.

**Respostas Aceitas:**
- `get`

**Explicacao:** O metodo get() retorna Option<&T> - Some(&valor) se existir ou None se o indice for invalido. E mais seguro que nums[1] que pode causar panic.

**Dicas:**
1. Voce quer um acesso seguro que retorna Option...
2. O nome do metodo sugere 'obter'...
3. Use 'get' para acesso seguro.

**Erro Comum:** `nums[1]`
> nums[1] funciona mas causa panic se o indice for invalido. get(1) retorna Option para tratamento seguro.

---

### Nivel 44: HashMap Basico
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
use std::collections::HashMap;

fn main() {
    let mut scores = HashMap::___();
    scores.insert(String::from("Blue"), 10);
    scores.insert(String::from("Red"), 50);
    println!("{:?}", scores);
}
```

**Tarefa:** Crie um novo HashMap vazio.

**Respostas Aceitas:**
- `new`

**Explicacao:** HashMap::new() cria um mapa vazio. Diferente de Vec, nao ha macro hashmap![] na biblioteca padrao. Use insert() para adicionar pares.

**Dicas:**
1. E o construtor padrao em Rust...
2. Tres letras, metodo de criacao...
3. Use 'new' para criar instancia vazia.

**Erro Comum:** `HashMap {}`
> HashMap nao e struct com campos publicos. Use HashMap::new() ou from() para criar.

---

### Nivel 45: Iterando Vector
**Categoria:** Structs, Enums e Collections

**Codigo de Contexto:**
```rust
fn main() {
    let nums = vec![1, 2, 3, 4, 5];
    for n in nums.___() {
        println!("{}", n);
    }
    println!("Vector ainda valido: {:?}", nums);
}
```

**Tarefa:** Itere sobre referencias para manter o vector valido.

**Respostas Aceitas:**
- `iter`

**Explicacao:** iter() retorna um iterador de referencias (&T), mantendo ownership do vector. iter_mut() para &mut T, into_iter() consome o vector.

**Dicas:**
1. Voce quer um 'iterador'...
2. E a abreviacao de 'iterator'...
3. Use 'iter' para iterar por referencia.

**Erro Comum:** `for n in nums { } println!(nums)`
> 'for n in nums' consome o vector (chama into_iter). Use nums.iter() para manter ownership.

---

## Niveis 46-50: Option, Result e Traits
**Temas:** Tratamento de erros, tipos genericos, traits

---

### Nivel 46: Option Some
**Categoria:** Option, Result e Traits

**Codigo de Contexto:**
```rust
fn encontrar_par(nums: &[i32]) -> Option<i32> {
    for &n in nums {
        if n % 2 == 0 {
            return ___(n);
        }
    }
    None
}

fn main() {
    let nums = vec![1, 3, 4, 5];
    println!("Par: {:?}", encontrar_par(&nums));
}
```

**Tarefa:** Retorne o valor encontrado encapsulado em Option.

**Respostas Aceitas:**
- `Some`

**Explicacao:** Option<T> tem duas variantes: Some(T) contem um valor, None representa ausencia. E a alternativa segura a null.

**Dicas:**
1. Option tem duas variantes: uma com valor, outra sem...
2. A variante com valor comeca com 'S'...
3. Use 'Some' para encapsular o valor encontrado.

**Erro Comum:** `return n;`
> A funcao retorna Option<i32>, nao i32. Encapsule com Some(n) para indicar sucesso.

---

### Nivel 47: Unwrap com Default
**Categoria:** Option, Result e Traits

**Codigo de Contexto:**
```rust
fn main() {
    let nome: Option<&str> = None;
    let nome_final = nome.unwrap_or(___);
    println!("Nome: {}", nome_final); // Nome: Visitante
}
```

**Tarefa:** Forneca um valor padrao caso Option seja None.

**Respostas Aceitas:**
- `"Visitante"`

**Explicacao:** unwrap_or() retorna o valor de Some ou o valor padrao fornecido se for None. E mais seguro que unwrap() que causa panic.

**Dicas:**
1. Voce precisa fornecer o valor padrao como argumento...
2. E uma string literal...
3. Use "Visitante" como valor padrao.

**Erro Comum:** `nome.unwrap()`
> unwrap() em None causa panic. Use unwrap_or(default), unwrap_or_else(|| ...), ou match para seguranca.

---

### Nivel 48: Result Ok e Err
**Categoria:** Option, Result e Traits

**Codigo de Contexto:**
```rust
fn dividir(a: i32, b: i32) -> Result<i32, String> {
    if b == 0 {
        ___(String::from("Divisao por zero!"))
    } else {
        Ok(a / b)
    }
}

fn main() {
    println!("{:?}", dividir(10, 2));
    println!("{:?}", dividir(10, 0));
}
```

**Tarefa:** Retorne o erro apropriado.

**Respostas Aceitas:**
- `Err`

**Explicacao:** Result<T, E> tem duas variantes: Ok(T) para sucesso e Err(E) para erro. E usado para operacoes que podem falhar de forma recuperavel.

**Dicas:**
1. Result tem Ok para sucesso e... para erro?
2. E a abreviacao de 'Error'...
3. Use 'Err' para retornar um erro.

**Erro Comum:** `panic!("Divisao por zero")`
> panic! aborta o programa. Result permite tratamento gracioso do erro pelo chamador.

---

### Nivel 49: Operador ? para Propagacao
**Categoria:** Option, Result e Traits

**Codigo de Contexto:**
```rust
fn pode_falhar() -> Result<i32, String> {
    Err(String::from("ops"))
}

fn usar_resultado() -> Result<i32, String> {
    let valor = pode_falhar()___;
    Ok(valor * 2)
}

fn main() {
    println!("{:?}", usar_resultado());
}
```

**Tarefa:** Use o operador para propagar erros automaticamente.

**Respostas Aceitas:**
- `?`

**Explicacao:** O operador ? propaga erros automaticamente: se Result for Err, retorna imediatamente; se for Ok, extrai o valor. So funciona em funcoes que retornam Result.

**Dicas:**
1. E um operador de propagacao de erro...
2. E um unico caractere de pontuacao...
3. Use '?' apos a chamada.

**Erro Comum:** `pode_falhar().unwrap()`
> unwrap() causa panic em Err. Use '?' para propagar o erro elegantemente.

---

### Nivel 50: Implementando Trait
**Categoria:** Option, Result e Traits

**Codigo de Contexto:**
```rust
struct Ponto {
    x: i32,
    y: i32,
}

___ std::fmt::Display for Ponto {
    fn fmt(&self, f: &mut std::fmt::Formatter) -> std::fmt::Result {
        write!(f, "({}, {})", self.x, self.y)
    }
}

fn main() {
    let p = Ponto { x: 3, y: 4 };
    println!("{}", p); // (3, 4)
}
```

**Tarefa:** Use a palavra-chave para implementar um trait para o tipo.

**Respostas Aceitas:**
- `impl`

**Explicacao:** Usamos 'impl Trait for Tipo' para implementar traits. Display permite usar {} em println!. Traits sao como interfaces que definem comportamento compartilhado.

**Dicas:**
1. E a mesma palavra usada para metodos de struct...
2. Mas aqui seguida de 'TraitName for TipoName'...
3. Use 'impl' seguido do trait e 'for' tipo.

**Erro Comum:** `struct Ponto implements Display`
> Rust nao usa 'implements'. A sintaxe e 'impl Trait for Tipo { ... }'.

---

## Resumo por Categoria

| Categoria | Niveis | Conceitos |
|-----------|--------|-----------|
| Basico | 1-15 | println!, let, mut, tipos (i32, f64, bool, char), interpolacao, operadores |
| Controle de Fluxo | 16-25 | if, else, else if, match, loop, while, for, ranges |
| Funcoes e Ownership | 26-35 | fn, parametros, ->, return, clone, &, &mut, slices |
| Structs/Enums/Collections | 36-45 | struct, impl, enum, =>, Vec, push, get, HashMap, iter |
| Option/Result/Traits | 46-50 | Some, None, unwrap_or, Ok, Err, ?, impl Trait for |

---

## Dicas de Uso

1. **Progressao**: Os exercicios foram ordenados para introduzir conceitos gradualmente
2. **Respostas flexiveis**: Aceite variacoes com espacos extras
3. **Feedback**: Use as explicacoes para ensinar apos acerto ou erro
4. **Dicas progressivas**: Revele uma dica por vez, da mais vaga para mais especifica
5. **Erros comuns**: Antecipe confusoes de quem vem de outras linguagens

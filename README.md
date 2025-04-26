
# 🧭 Algoritmo de Debug para Iniciantes

  

Uma forma de pensar e organizar suas ideias quando **seu código não funciona como esperado** — sem desespero, sem chute!

Use esse passo a passo como guia mental toda vez que algo der errado.


## 🧠 Etapa 1: Modele sua solução no papel

  

Antes de escrever código, entenda o problema.

  

✏️ Pegue lápis e papel (ou seu app favorito de anotações).

+ Desenhe, rabisque, explique com palavras simples o que precisa ser feito.

  
> Se você não consegue explicar o que quer fazer, como o código vai entender?

  

🧩 Dica extra:

+ Imagine que está explicando o problema para uma criança ou para alguém que nunca viu código.
+  Use fluxogramas simples ou listas de passos.

  

  

## 📥 Etapa 2: Escreva as entradas e saídas do programa

  

Todo programa é como uma máquina: recebe algo (entrada), faz algo, e devolve um resultado (saída).

  

🔎 Pergunte-se:

- O que o programa precisa receber?

- O que ele deve devolver no final?

  

### Exemplo: Calculadora simples

-  **Entrada:** número A, operador (`+`, `-`, `*`, `/`), número B

-  **Saída:** resultado da operação entre A e B

  

🧠 Fazer isso antes de codar evita que você se perca no meio do caminho.

  

---

  

## 🛠️ Etapa 3: Esboce o que acontece entre entrada e saída

  

Agora pense: como o programa transforma entrada em saída?

  

🧱 Que blocos de ação existem?

- Precisa de repetição (loops)?
- Vai ter decisões (condições)?
- Vai usar listas ou dicionários?
- Precisa criar funções para organizar?

  

#
### Exemplo: Calcular a média de três números

1. **Entrada:** Receber três números do usuário
2. **Ação:** Somar os três números e dividir o resultado por 3
3. **Saída:** Exibir a média dos três números

### Passos no pseudocódigo:
1. Solicitar ao usuário o primeiro número
2. Solicitar ao usuário o segundo número
3. Solicitar ao usuário o terceiro número
4. Somar os três números
5. Dividir o resultado da soma por 3
6. Mostrar o valor da média

  

🎯 Faça um rascunho desses passos — até pseudocódigo vale!

---

  

## ⚠️ Etapa 4: Imagine como alguem pode querer sacanear seu codigo



Essa é a hora de treinar prever os erros mais comuns e evitar surpresas.

Diferenças na entrada, números maliciosos, ter 1 maçã e querer dar 5 maçãs; a ideia é imaginar situações que o seu codigo pode ter comportamentos incorretos; Somos brasileiros, somos bons nisso!

💭 Pergunte-se:
- E se a entrada for vazia?
- E se for um texto em vez de número?
- E se for uma operação inválida?
- E se eu tentar dividir por zero?

  

🛡️ Pensar nesses casos ajuda a escrever código mais resistente (e evita dor de cabeça depois).

## 🧪 Etapa 5: Crie (ou leia) os casos de teste

  

Agora que você entende o que o programa faz, crie exemplos reais:

  

### Exemplo:

-  **Entrada:**  `2 + 2`

-  **Esperado:**  `4`

  

💡 Tipos de teste:

- ✅ Casos normais

- 🧊 Casos-limite (zero, vazio, extremos)

- ❌ Casos errados de propósito (para ver se o programa lida bem)

  

🔍 Compare seus testes com os que o professor ou a plataforma forneceram. Faz sentido? Faltou algo?

  

---

  

## ▶️ Etapa 6: Rode o código e compare

  

Agora sim, hora de ver o programa funcionando.

  

✅ Se **a saída bateu com a esperada**: ótimo!

❌ Se **não bateu**: vem aí o… debug!

  

---

  

# 🕵️ Etapa de Debug: Investigando Erros com Calma

 
  

Debug é o processo de descobrir **por que algo não funcionou**.


Tenha em mente que você quer seguir o seguinte loop:

Hipotese → testar → observar → ajustar → repetir

Aqui vão técnicas práticas para entender e resolver erros com mais tranquilidade:


## 🔍 1. Use `print()` (ou `puts`, `console.log`, etc.)

  

Mostre na tela os valores das variáveis **em pontos estratégicos do código**.

  

```python
print(f"Entrando no loop com x = {x}")
```

🧠 Isso revela o que está acontecendo de verdade, não o que você acha que está.

  


## 🧩 2. Seccione seu código por blocos
Divida o código em partes com funções bem definidas.
  
```python
# Etapa: soma dos produtos
soma_produtos = sum(precos)
  
# Etapa: aplicação de descontos
desconto_total = calcular_descontos(cupons)  

# Etapa: resultado final
total_final = soma_produtos - desconto_total
```
📌 Isso facilita identificar onde o valor começou a sair errado.

**PS**: Uma boa prática é sempre comentar o que o código faz. Isso facilita o entendimento, tanto para você quanto para outras pessoas que possam ler o código no futuro. Comentários bem feitos ajudam a esclarecer a lógica por trás do código, tornando-o mais fácil de manter e modificar ao longo do tempo.
> ex:
```python
# Função recursiva que calcula o valor do n-ésimo termo da sequência de Fibonacci.
# A sequência de Fibonacci é definida como:
# fibonacci(0) = 0, fibonacci(1) = 1, e fibonacci(n) = fibonacci(n-1) + fibonacci(n-2) para n > 1.
valor = lambda n: n if n <= 1 else valor(n - 1) + valor(n - 2)
```
### nota dramática do autor: 
>  Quando eu escrevi o codigo, 2 pessoas sabiam como ele funcionava; Eu e Deus ... agora é só ele
>>  Eu também não sei como o codigo acima funciona xD
  
## 🔁 3. Acompanhe variáveis ao longo do tempo

Em loops ou funções complexas, imprima o valor a cada passo:
```python 
for item in carrinho:
	total += item.preco
	print(f"Somando: {item.nome} - total parcial: {total}")
```
🧭 Isso mostra se a lógica está funcionando em cada repetição.

  ## ✅ 4. Tenha um objetivo claro para cada variável

Cada variável no seu código deve ter um propósito claro.

Se você não sabe “pra que ela está ali”, talvez ela esteja atrapalhando.

  

🔎 Tente responder:
  

+ De onde essa variável vem?
+ O que ela representa?
+ O que acontece se eu remover?


## 🚨 5. Para entender o erro:

O que está?
Por ter os valores das variaveis nas etapas, voce pode se fazer perguntas para entender o que acontece:

  
> O erro foi de lógica, digitação ou fluxo?

> Quais valores a variável deveria ter?

> Quais valores a variável está mostrando?

> > O que essa diferença de valor significa?
		Não passou por um loop?

> Terminou uma conta antes do esperado?

  ## 🧰 6. Comente partes do código

Se estiver perdido, comente temporariamente trechos do código para isolar o problema.
```python 
desconto_total = calcular_descontos(cupons)
# total_final = soma_produtos - desconto_total
```  

▶️ Rode só a parte que funciona e vá desbloqueando linha por linha.

Isso ajuda a descobrir em qual trecho o problema está aparecendo.

  ## 🕸️ 7. Para erros que o script não roda:

Quando aparece uma mensagem de erro, não entre em pânico.

🧠 Pergunte-se:

+ Qual o tipo de erro? (ex: TypeError, NameError, IndexError)
+ Em qual linha aconteceu?
 + Ele menciona qual variável ou função?

  📌 Muitas vezes, o erro já te diz exatamente o que consertar — só precisa ler com atenção.


## 🗺️ 8. Volte ao plano inicial

Quando tudo parecer confuso, volte para as primeiras etapas:
```python 
Qual era o problema inicial?
Quais eram as entradas e saídas esperadas?
O que o programa deveria estar fazendo?
Quais valores a variavel deveria ter?
```
🔄 Às vezes, o problema está no caminho escolhido, não no código em si.


Debug não é só caçar erro. É testar sua teoria de como o código funciona.
>hipotese → testar → observar → ajustar → repetir

🎯 Quanto mais você pratica esse processo, mais rápido e claro ele se torna.

---

# ✅ Exemplo de aplicação do guia acima:
  

## Controle de Compras  

## 🧠 Etapa 1: Modele sua solução no papel
Antes de escrever qualquer código, precisamos entender o que o sistema deve fazer. Neste caso, queremos:

>Adicionar um item à compra.
Remover um item da compra.
Consultar o total da compra.
Listar todos os itens na compra.
  

## 📥 Etapa 2: Escreva as entradas e saídas do programa

Entradas:
```python
Nome do item (ex: "Camiseta").
Preço do item (ex: 29.90).
```
Saídas:
```python
Exibição de todos os itens na compra (nome + preço).
Cálculo do total da compra.
Confirmação ao adicionar ou remover itens.
```
  
## 🛠️ Etapa 3: Esboce o que acontece entre entrada e saída

Aqui está a ordem dos passos que o código executa:
```python
Adicionar item: Recebe o nome e preço do item e adiciona a um lista.
Remover item: Busca o item pelo nome na lista e o remove, se encontrado.
Calcular total: Soma os preços de todos os itens na lista.
Listar itens: Exibe os itens que estão na lista.
```
## ⚠️ Etapa 4: Imagine onde pode dar ruim

Vamos antecipar alguns problemas:
```python
Adicionar item: E se o preço for negativo? O que devemos fazer?

Remover item: E se o item não existir na lista? O que acontece?

Calcular total: E se a lista estiver vazia? Como mostrar o total corretamente?

Listar itens: E se não houver nenhum item na lista?
```
 ## 🧪 Etapa 5: Crie ou leia os casos de teste

Vamos pensar em alguns testes para verificar se tudo está funcionando corretamente:
```python
Adicionar um item: adicionar_item("Camiseta", 29.90)
Adicionar mais um item: adicionar_item("Calça", 49.90)

Remover um item existente: remover_item("Camiseta")

Remover um item inexistente: remover_item("Tênis")
Calcular total da compra: calcular_total()
Listar itens da compra: listar_itens()
```  

## ▶️ Etapa 6: Escreva o código e compare os testes

```python
# Lista para armazenar os itens da compra
compra = []

# Função para adicionar um item à compra
def adicionar_item(nome, preco):
    if preco <= 0:
        print("❌ Erro: Preço deve ser positivo.")
        return False
    compra.append({'nome': nome, 'preco': preco})
    print(f"✅ Item '{nome}' adicionado!")
    return True
    
# Função para remover um item da compra
def remover_item(nome):
    for item in compra:
        if item['nome'] == nome:
            compra.remove(item)
            print(f"✅ Item '{nome}' removido!")
            return True
    print(f"❌ Item '{nome}' não encontrado.")
    return False
    
# Função para calcular o total da compra
  
def calcular_total():
    total = sum(item['preco'] for item in compra)
    print(f"💳 Total da compra: R${total:.2f}" if total else "🛒 Nenhum item na lista.")
    return total
    
# Função para exibir os itens da compra
def  listar_itens():  if  not compra:  return  "🛒 Sua lista está vazia."  return  "\n".join([f"📦 {item['nome']} - R${item['preco']:.2f}"  for item in compra])
```


Agora vamos rodar os testes e comparar os resultados.
```python
# Teste 1: Adicionar item com preço inválido
adicionar_item("Item Inválido", -10)  # ❌ Erro esperado

# Teste 2: Adicionar itens válidos
adicionar_item("Camiseta", 29.90)     # ✅
adicionar_item("Calça", 49.90)        # ✅

# Teste 3: Listar itens
print(listar_itens())  # 📦 Camiseta - R$29.90 \n 📦 Calça - R$49.90

# Teste 4: Remover item inexistente
remover_item("Tênis")  # ❌ Item não encontrado

# Teste 5: Calcular total
calcular_total()       # 💳 Total: R$79.80

```
## 🕵️ Hora de debugar!
Se algo não funcionar como esperado, aqui estão algumas dicas para encontrar e corrigir o erro:

Use print(): Coloque prints em pontos chave para ver se as funções estão recebendo os parâmetros certos.


Exemplo:
```python  
  
def adicionar_item(nome, preco):
	print(f"Adicionando item: {nome} com preço {preco}")
	compra.append({'nome': nome, 'preco': preco})
```   

Verifique a lógica das funções: Se a remoção de um item não funcionar, adicione um print na parte que faz a busca para ver se o item realmente está na lista.
```python
def remover_item(nome):
	for item in compra:
		print(f"Verificando item: {item['nome']}") # Para ver se o item está sendo encontrado
		if item['nome'] == nome:
			compra.remove(item)
			return True
	return False
  ```
   
Cheque o que acontece quando a lista está vazia: Se o total estiver incorreto ou a listagem estiver falhando, verifique o comportamento quando não há itens na lista.

Leia o erro: Se o programa der um erro, olhe a mensagem com calma. O Python geralmente te diz exatamente onde o problema ocorreu, como na falta de um item ou tipo errado de dado.

# Boa sorte e bom Debugging!
__ 



## _PS: 🕵️ Não achei o erro!_
>Esse é o momento que a criança chora e a mãe não vê

Nessas horas, você tem que rever toda a sua lógica. A minha sugestão é a tecnica de debug ou depuração do  patinho companheiro <https://pt.wikipedia.org/wiki/Debug_com_Pato_de_Borracha> 

**Você:**  _"Patinho, meu código deveria calcular o total da compra, mas quando removo um item, o valor não atualiza direito. Não sei onde está o erro!"_

**Patinho:**  _"Quack! (tradução: 'Mostre-me o código e explique o que cada parte faz.')"_


### explicando linha por linha
```python
def remover_item(nome):
    for item in compra:  # Aqui eu percorro cada item na lista 'compra'
        if item['nome'] == nome:  # Se o nome do item bater com o que quero remover...
            compra.remove(item)  # ...eu removo o item da lista.
            return True  # E retorno True pra confirmar que deu certo.
    return False  # Se não achar, retorno False.
```

**Você:**  _"Patinho, essa função deveria remover um item pelo nome e retornar  `True`  se conseguir, ou  `False`  se não achar. Mas quando testo, parece que ela não remove direito. Olha só:"_
```python
adicionar_item("Camiseta", 29.90)
adicionar_item("Calça", 49.90)
remover_item("Camiseta")  # Era pra remover, mas às vezes não funciona!
```
**Patinho:**  _"Quack!"_ 
```python 
### Testando a hipoteses 
def remover_item(nome):
    print(f"Lista ANTES de remover: {compra}")  # Debug: mostra a lista antes
    for item in compra:
        if item['nome'] == nome:
            compra.remove(item)
            print(f"Lista DEPOIS de remover: {compra}")  # Debug: mostra depois
            return True
    return False
```

```terminal
Lista ANTES de remover: [{'nome': 'Camiseta', 'preco': 29.9}, {'nome': 'Calça', 'preco': 49.9}]  
Lista DEPOIS de remover: [{'nome': 'Calça', 'preco': 49.9}]  # Parece correto!
```
**Você:**  _"Patinho, olha só! A lista está sendo alterada, mas em outro lugar do código o total não atualiza. Será que o problema está na função  `calcular_total`?_

```python
def calcular_total():
    total = 0
    for item in compra:  # Percorre a lista 'compra'
        total += item['preco']  # Soma todos os preços
    return total  # Retorna o valor
 ```
```python 
remover_item("Camiseta")
print(calcular_total())  # Mostra o total atualizado?
``` 
```
49.9  # Funcionou! Então o problema não está aqui...
```

**Você (lembrando):**  _"Ah! Eu esqueci de  **atualizar o total**  na interface do usuário! O código remove o item, mas não mostra o novo total automaticamente!"_


```python
remover_item("Camiseta")  print("Total atualizado:", calcular_total())  # Agora sim!
```

**Você:** _Agora eu posso adicionar o print no final e ver o valor certo_
```python
adicionar_item("Camiseta", 29.90)
adicionar_item("Calça", 49.90)
remover_item("Camiseta")  
print("Total atualizado:", calcular_total()) # faltava essa linha
```
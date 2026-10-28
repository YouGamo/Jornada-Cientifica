import React, { useState, useEffect } from 'react';

// --- COMPONENTE DE CONCEITOS DO JAVA ---
function JavaIntro() {
  return (
    <div style={stylesJava.javaIntroBody}>
      <header style={{ display: 'flex', alignItems: 'center', gap: '15px', marginBottom: '15px' }}>
        <img 
          className="logo" 
          src="https://www.svgrepo.com/show/303388/java-4-logo.svg" 
          alt="Java Logo"
          style={stylesJava.logo} 
        />
        <h1 style={stylesJava.h1}>O que é o Java?</h1>
      </header>

      <p style={stylesJava.p}><strong>Origem:</strong> Criado nos anos 90 por James Gosling na Sun Microsystems.</p>
      <p style={stylesJava.p}>É uma linguagem de programação que funciona através de uma ferramenta JDK, que é a ponte que transforma o texto escrito por um programador num programa real que funciona no computador.</p>

      <h2 style={stylesJava.h2}>Estrutura e Regras Básicas</h2>
      <p style={stylesJava.p}>Em Java, antes de programar devemos importar as bibliotecas, neste website vamos importar:</p>
      
      <p style={stylesJava.p}><code style={stylesJava.code}>import java.io.*;</code> É uma biblioteca que diz ao Java para receber e dar resposta ao código por ti digitado.</p>
      <p style={stylesJava.p}><code style={stylesJava.code}>BufferedReader br = new BufferedReader(new InputStreamReader(System.in));</code> É uma classe pertencente à biblioteca java.io.</p>
      <p style={stylesJava.p}>Ao finalizar cada linha de código Java é obrigatório que termine sempre com ponto e vírgula <code style={stylesJava.code}>;</code> sem isso, o código terá falhas e não vai rodar.</p>
      <p style={stylesJava.p}>Todos os blocos de código funcionam como caixas fechadas: sempre que abres uma chaveta <code style={stylesJava.code}>{`{`}</code> (seja no public class, no main ou nos futuros ciclos de repetição e lógicos que verás no próximo capítulo), és obrigado a fechar com <code style={stylesJava.code}>{`}`}</code>.</p>
      <p style={stylesJava.p}>Ao atribuir um nome a uma variável, não pode ter espaçamento.</p>

      <h2 style={stylesJava.h2}>Tipos de Dados</h2>
      <p style={stylesJava.p}>Em Java temos 8 tipos de dados, entretanto neste website abordaremos 4 que são os que usaremos:</p>
      <ul style={stylesJava.ul}>
        <li style={stylesJava.li}><strong>int</strong> - Tipo de dados reservado para números inteiros.</li>
        <li style={stylesJava.li}><strong>double</strong> - Tipo de dados reservado para números decimais.</li>
        <li style={stylesJava.li}><strong>String</strong> - Tipo de dados reservado para texto.</li>
        <li style={stylesJava.li}><strong>char</strong> - Tipo de dados reservado para 1 único carácter.</li>
      </ul>

      {/* Exemplo 1: Declaração de Variáveis */}
      <div style={stylesJava.caixaExemplo}>
        <p style={stylesJava.p}><strong>Exemplo Prático: Declaração de Variáveis</strong></p>
        <p style={stylesJava.p}>Declare o tipo de dados ideal para cada variável abaixo: idade, altura, nome, sexo(M/F), numerocelular e nota.</p>
        <br />
        <p style={stylesJava.p}><strong>int idade = 15;</strong> (Porquê não usamos double? R: Porque idade não pode ser decimal);</p>
        <p style={stylesJava.p}><strong>double altura = 1.76;</strong> (Por ser um número decimal usamos o tipo de dados correspondente);</p>
        <p style={stylesJava.p}><strong>String nome = "Manuel";</strong></p>
        <p style={stylesJava.p}><strong>char sexo = 'M';</strong> (Mas porquê não disse masculino? R: Para prevenir possíveis erros e facilitar possíveis operações que envolvam este dado.);</p>
        <p style={stylesJava.p}><strong>String numerocelular = "823456789";</strong> (Porquê não usamos int? R: Pois todo dado tipo int pode sofrer operações matemáticas e um número de celular não pode sofrer alterações, é um identificador!);</p>
        <p style={stylesJava.p}><strong>double nota = 20;</strong> (Se a nota foi um número inteiro porquê atribuímos ao double? R: O double representa o conjunto de números reais em Java! E também porque as notas podem variar, podendo ou não ser decimal, no caso das notas máximas em avaliações).</p>
      </div>

      <h2 style={stylesJava.h2}>Sinais e Operadores Principais</h2>
      
      <p style={stylesJava.p}><strong>Operadores Aritméticos:</strong></p>
      <div style={stylesJava.caixaExemplo}>
        <p style={stylesJava.p}><strong>*</strong> : Multiplicação</p>
        <p style={stylesJava.p}><strong>/</strong> : Divisão (atenção: se os operandos forem inteiros, a parte fracionária é desprezada)</p>
        <p style={stylesJava.p}><strong>%</strong> : Resto da divisão inteira (módulo)</p>
        <p style={stylesJava.p}><strong>+</strong> : Adição</p>
        <p style={stylesJava.p}><strong>-</strong> : Subtração</p>
      </div>

      <p style={stylesJava.p}><strong>Operadores de Incrementação e Decrementação Unária:</strong></p>
      <div style={stylesJava.caixaExemplo}>
        <p style={stylesJava.p}><strong>++</strong> : Soma 1 ao operando (pré-incremento <code style={stylesJava.code}>++var</code> ou pós-incremento <code style={stylesJava.code}>var++</code>)</p>
        <p style={stylesJava.p}><strong>--</strong> : Subtrai 1 ao operando (pré-decremento <code style={stylesJava.code}>--var</code> ou pós-decremento <code style={stylesJava.code}>var--</code>)</p>
        <p style={stylesJava.p}><em>(Isso será melhor compreendido no capítulo de Estruturas de Controlo)</em></p>
      </div>

      <p style={stylesJava.p}><strong>Operadores de Atribuição Abreviada:</strong></p>
      <div style={stylesJava.caixaExemplo}>
        <p style={stylesJava.p}><strong>+=</strong> : Exemplo: <code style={stylesJava.code}>c += 3;</code> equivale a <code style={stylesJava.code}>c = c + 3;</code></p>
        <p style={stylesJava.p}><strong>-=</strong> : Exemplo: <code style={stylesJava.code}>d -= 4;</code> equivale a <code style={stylesJava.code}>d = d - 4;</code></p>
        <p style={stylesJava.p}><strong>*=</strong> : Exemplo: <code style={stylesJava.code}>e *= 5;</code> equivale a <code style={stylesJava.code}>e = e * 5;</code></p>
        <p style={stylesJava.p}><strong>/=</strong> : Exemplo: <code style={stylesJava.code}>f /= 3;</code> equivale a <code style={stylesJava.code}>f = f / 3;</code></p>
      </div>

      <p style={stylesJava.p}><strong>Operadores Relacionais:</strong></p>
      <div style={stylesJava.caixaExemplo}>
        <p style={stylesJava.p}><strong>&gt;</strong> : Maior que</p>
        <p style={stylesJava.p}><strong>&lt;</strong> : Menor que</p>
        <p style={stylesJava.p}><strong>&gt;=</strong> : Maior ou igual a</p>
        <p style={stylesJava.p}><strong>&lt;=</strong> : Menor ou igual a</p>
        <p style={stylesJava.p}><strong>==</strong> : Igual a</p>
        <p style={stylesJava.p}><strong>!=</strong> : Diferente de</p>
      </div>
    </div>
  );
}

const stylesJava = {
  javaIntroBody: {
    textAlign: 'left',
    color: '#2b2b2b',
    background: 'rgba(255, 255, 255, 0.6)',
    padding: '20px',
    borderRadius: '12px',
    backdropFilter: 'blur(10px)',
  },
  h1: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    fontSize: '18pt',
    margin: 0,
  },
  h2: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    marginTop: '1.5em',
    fontSize: '14pt',
  },
  logo: {
    width: '40px',
    height: '40px',
    objectFit: 'contain',
  },
  p: {
    margin: '8px 0',
    lineHeight: '1.6',
    fontSize: '11pt',
  },
  ul: {
    margin: '0.4em 0',
    paddingLeft: '1.3em',
  },
  li: {
    margin: '0.35em 0',
    fontSize: '11pt',
  },
  code: {
    fontFamily: "Consolas, 'Courier New', monospace",
    background: 'rgba(26, 54, 93, 0.09)',
    padding: '0.1em 0.4em',
    borderRadius: '4px',
    fontSize: '0.92em',
  },
  caixaExemplo: {
    background: 'rgba(255, 255, 255, 0.75)',
    backdropFilter: 'blur(10px)',
    border: '1px solid rgba(255, 255, 255, 0.6)',
    borderLeft: '5px solid #007acc',
    color: '#222',
    padding: '15px',
    margin: '15px 0',
    borderRadius: '6px',
  },
};

// --- COMPONENTE DE CONCEITOS DO PYTHON ---
function PythonIntro() {
  return (
    <div style={stylesPython.body}>
      <main style={stylesPython.main}>
        
        <h1 style={stylesPython.h1}>Estrutura e Regras Gerais em Python</h1>

        <p style={stylesPython.p}>
          Python é uma linguagem de programação de alto nível, criada por Guido van Rossum e lançada em 1991. 
          É interpretada: o código é executado linha a linha, sem passos extras de compilação.
        </p>

        <p style={stylesPython.p}>
          Enquanto em outras linguagens de programação você tem de criar toda uma estrutura básica para que realmente possa 
          começar a programar, Python já nos oferece praticamente tudo o que precisamos pré-carregado, de forma que, ao abrirmos 
          uma IDE, nossa única preocupação inicial é realmente programar.
        </p>

        <div style={stylesPython.caixaExemplo}>
          <p style={stylesPython.p}>
            <strong>IDE</strong> (Integrated Development Environment ou Ambiente de Desenvolvimento Integrado) é um software que reúne, 
            em uma única interface gráfica, todas as ferramentas essenciais para um programador criar, testar e corrigir códigos.
          </p>
        </div>

        <h2 style={stylesPython.h2}>Regras Básicas</h2>

        <ul style={stylesPython.ul}>
          <li style={stylesPython.li}>Não é preciso terminar as linhas com ponto e vírgula (<code style={stylesPython.code}>;</code>). Cada instrução ocupa uma linha.</li>
          <li style={stylesPython.li}>Os blocos de código são definidos pela <strong>indentação</strong> (o recuo da linha, normalmente 4 espaços), e não por chavetas <code style={stylesPython.code}>{`{ }`}</code>.</li>
          <li style={stylesPython.li}>Comentários começam com <code style={stylesPython.code}>#</code> e são ignorados pelo programa.</li>
          <li style={stylesPython.li}>Os nomes das variáveis não podem ter espaços (use <code style={stylesPython.code}>_</code>), não podem começar por número e diferenciam maiúsculas de minúsculas: <code style={stylesPython.code}>idade</code> e <code style={stylesPython.code}>Idade</code> são variáveis diferentes.</li>
          <li style={stylesPython.li}>É boa prática escrever os nomes das variáveis em minúsculas, como <code style={stylesPython.code}>nota_final</code>.</li>
        </ul>

        <h2 style={stylesPython.h2}>Entrada e Saída de Dados</h2>

        <div style={stylesPython.caixaExemplo}>
          <p style={stylesPython.p}><code style={stylesPython.code}>print()</code> mostra informação no ecrã.</p>
          <p style={stylesPython.p}><code style={stylesPython.code}>input()</code> lê o que o utilizador escreve.</p>
        </div>

        <pre style={stylesPython.pre}>
          <code style={stylesPython.preCode}>{`nome = input("Nome: ")
idade = int(input("Idade: "))
print("Olá,", nome, "- no próximo ano terás", idade + 1)`}</code>
        </pre>

        <div style={stylesPython.caixaNota}>
          <p style={stylesPython.p}>
            O <code style={stylesPython.code}>input()</code> devolve sempre texto. Para fazer contas com o valor lido, converta-o com <code style={stylesPython.code}>int()</code> ou <code style={stylesPython.code}>float()</code>.
          </p>
        </div>

        <h2 style={stylesPython.h2}>Tipos de Dados</h2>

        <p style={stylesPython.p}>
          O Python em si já reconhece os tipos de dados: o tipo é definido quando se atribui o valor à variável, sem precisar de o declarar. Para ver o tipo de uma variável, use <code style={stylesPython.code}>type()</code>.
        </p>

        <div style={{ ...stylesPython.caixaExemplo, overflowX: 'auto' }}>
          <table style={stylesPython.table}>
            <thead>
              <tr>
                <th style={stylesPython.th}>Tipo</th>
                <th style={stylesPython.th}>Guarda</th>
                <th style={stylesPython.th}>Exemplo</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>int</code></td>
                <td style={stylesPython.td}>Números inteiros</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>idade = 15</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>float</code></td>
                <td style={stylesPython.td}>Números decimais</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>nota = 17.5</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>str</code></td>
                <td style={stylesPython.td}>Texto</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>nome = "Manuel"</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>bool</code></td>
                <td style={stylesPython.td}>Verdadeiro ou falso</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>aprovado = True</code></td>
              </tr>
            </tbody>
          </table>
        </div>

        <p style={stylesPython.p}>
          <em>Nota: Os tipos de dados citados são os que serão usados nesta plataforma e não o seu todo.</em>
        </p>

        <div style={stylesPython.caixaExemplo}>
          <p style={stylesPython.p}>Para a variável idade, usaríamos o <strong>int</strong>.</p>
          <p style={stylesPython.p}>Para a variável nota de um teste usaríamos o <strong>float</strong>.</p>
          <p style={stylesPython.p}>Para um número de celular usaríamos o <strong>str</strong> (<code style={stylesPython.code}>"823456789"</code>), pois é um identificador e não se fazem contas com ele.</p>
        </div>

        <h2 style={stylesPython.h2}>Sinais e Operadores Principais</h2>

        <div style={{ ...stylesPython.caixaExemplo, overflowX: 'auto' }}>
          <table style={stylesPython.table}>
            <thead>
              <tr>
                <th style={stylesPython.th}>Operador</th>
                <th style={stylesPython.th}>Nome</th>
                <th style={stylesPython.th}>Exemplo</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>*</code></td>
                <td style={stylesPython.td}>Multiplicação: multiplica os valores envolvidos</td>
                <td style={stylesPython.td}>6 * 3 = 18</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>**</code></td>
                <td style={stylesPython.td}>Potenciação: eleva um valor a uma potência</td>
                <td style={stylesPython.td}>2 ** 3 = 8</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>//</code></td>
                <td style={stylesPython.td}>Divisão inteira: descarta as casas decimais (arredonda para baixo)</td>
                <td style={stylesPython.td}>9 // 2 = 4</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>/</code></td>
                <td style={stylesPython.td}>Divisão real: gera resultados decimais</td>
                <td style={stylesPython.td}>9 / 2 = 4.5</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>%</code></td>
                <td style={stylesPython.td}>Resto da divisão inteira</td>
                <td style={stylesPython.td}>55 % 7 = 6</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>+</code></td>
                <td style={stylesPython.td}>Adição</td>
                <td style={stylesPython.td}>48 + 1023 = 1071</td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>-</code></td>
                <td style={stylesPython.td}>Subtração</td>
                <td style={stylesPython.td}>178 - 24 = 154</td>
              </tr>
            </tbody>
          </table>
        </div>

        <div style={stylesPython.caixaNota}>
          <p style={stylesPython.p}>
            <strong>Ordem de prioridade:</strong> primeiro os parênteses, depois <code style={stylesPython.code}>**</code>, depois <code style={stylesPython.code}>*</code> <code style={stylesPython.code}>/</code> <code style={stylesPython.code}>//</code> <code style={stylesPython.code}>%</code>, e por fim <code style={stylesPython.code}>+</code> e <code style={stylesPython.code}>-</code>. Assim, <code style={stylesPython.code}>2 + 3 * 4</code> dá 14, e <code style={stylesPython.code}>{`(2 + 3) * 4`}</code> dá 20.
          </p>
          <p style={stylesPython.p}>
            O operador <code style={stylesPython.code}>%</code> é muito usado para saber se um número é par: se <code style={stylesPython.code}>n % 2</code> der 0, é par.
          </p>
        </div>

        <h2 style={stylesPython.h2}>Operadores de Atribuição Abreviada</h2>

        <p style={stylesPython.p}>Atualizam o valor de uma variável usando o próprio valor dela, em uma só linha.</p>

        <div style={{ ...stylesPython.caixaExemplo, overflowX: 'auto' }}>
          <table style={stylesPython.table}>
            <thead>
              <tr>
                <th style={stylesPython.th}>Operador</th>
                <th style={stylesPython.th}>Nome</th>
                <th style={stylesPython.th}>Equivale a</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>+=</code></td>
                <td style={stylesPython.td}>Adição e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x += 3</code> é igual a <code style={stylesPython.code}>x = x + 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>-=</code></td>
                <td style={stylesPython.td}>Subtração e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x -= 3</code> é igual a <code style={stylesPython.code}>x = x - 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>*=</code></td>
                <td style={stylesPython.td}>Multiplicação e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x *= 3</code> é igual a <code style={stylesPython.code}>x = x * 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>/=</code></td>
                <td style={stylesPython.td}>Divisão e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x /= 3</code> é igual a <code style={stylesPython.code}>x = x / 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>%=</code></td>
                <td style={stylesPython.td}>Módulo e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x %= 3</code> é igual a <code style={stylesPython.code}>x = x % 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>//=</code></td>
                <td style={stylesPython.td}>Divisão inteira e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x //= 3</code> é igual a <code style={stylesPython.code}>x = x // 3</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>**=</code></td>
                <td style={stylesPython.td}>Potenciação e atribuição</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>x **= 3</code> é igual a <code style={stylesPython.code}>x = x ** 3</code></td>
              </tr>
            </tbody>
          </table>
        </div>

        <div style={stylesPython.caixaNota}>
          <p style={stylesPython.p}>
            Python não tem os operadores <code style={stylesPython.code}>++</code> e <code style={stylesPython.code}>--</code> do C++ e do Java. Para somar 1, escreva <code style={stylesPython.code}>x += 1</code>.
          </p>
        </div>

        <h2 style={stylesPython.h2}>Operadores Relacionais</h2>

        <p style={stylesPython.p}>Comparam dois valores e devolvem sempre um valor <strong>bool</strong>: <code style={stylesPython.code}>True</code> ou <code style={stylesPython.code}>False</code>.</p>

        <div style={{ ...stylesPython.caixaExemplo, overflowX: 'auto' }}>
          <table style={stylesPython.table}>
            <thead>
              <tr>
                <th style={stylesPython.th}>Operador</th>
                <th style={stylesPython.th}>Significado</th>
                <th style={stylesPython.th}>Exemplo</th>
                <th style={stylesPython.th}>Resultado</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>==</code></td>
                <td style={stylesPython.td}>Igual a</td>
                <td style={stylesPython.td}>5 == 5</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>True</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>!=</code></td>
                <td style={stylesPython.td}>Diferente de</td>
                <td style={stylesPython.td}>5 != 3</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>True</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>&gt;</code></td>
                <td style={stylesPython.td}>Maior que</td>
                <td style={stylesPython.td}>2 &gt; 8</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>False</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>&lt;</code></td>
                <td style={stylesPython.td}>Menor que</td>
                <td style={stylesPython.td}>4 &lt; 7</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>True</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>&gt;=</code></td>
                <td style={stylesPython.td}>Maior ou igual a</td>
                <td style={stylesPython.td}>5 &gt;= 5</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>True</code></td>
              </tr>
              <tr>
                <td style={stylesPython.td}><code style={stylesPython.code}>&lt;=</code></td>
                <td style={stylesPython.td}>Menor ou igual a</td>
                <td style={stylesPython.td}>9 &lt;= 3</td>
                <td style={stylesPython.td}><code style={stylesPython.code}>False</code></td>
              </tr>
            </tbody>
          </table>
        </div>

        <div style={stylesPython.caixaNota}>
          <p style={stylesPython.p}>
            Não confunda: <code style={stylesPython.code}>=</code> <strong>atribui</strong> um valor a uma variável (<code style={stylesPython.code}>x = 5</code>), enquanto <code style={stylesPython.code}>==</code> <strong>compara</strong> dois valores (<code style={stylesPython.code}>x == 5</code>).
          </p>
        </div>

      </main>
    </div>
  );
}

const stylesPython = {
  body: {
    margin: 0,
    minHeight: '100vh',
    padding: '20px',
    background: 'rgba(255, 255, 255, 0.6)',
    color: '#2b2b2b',
    fontFamily: 'Arial, Helvetica, sans-serif',
    lineHeight: '1.65',
    boxSizing: 'border-box',
    borderRadius: '12px',
    backdropFilter: 'blur(10px)',
    textAlign: 'left',
  },
  main: {
    maxWidth: '820px',
    margin: '0 auto',
  },
  h1: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    fontSize: '18pt',
    lineHeight: '1.2',
    margin: '0.5em 0',
  },
  h2: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    fontSize: '14pt',
    margin: '1.8em 0 0.6em',
    paddingBottom: '0.2em',
    borderBottom: '2px solid rgba(26, 54, 93, 0.25)',
  },
  p: {
    margin: '0.6em 0',
    fontSize: '11pt',
  },
  ul: {
    margin: '0.4em 0',
    paddingLeft: '1.3em',
  },
  li: {
    margin: '0.35em 0',
    fontSize: '11pt',
  },
  code: {
    fontFamily: "Consolas, 'Courier New', monospace",
    fontSize: '0.92em',
    background: 'rgba(26, 54, 93, 0.09)',
    padding: '0.1em 0.4em',
    borderRadius: '4px',
  },
  pre: {
    background: '#1a2a44',
    color: '#f2f6fb',
    padding: '14px 16px',
    borderRadius: '8px',
    overflowX: 'auto',
    lineHeight: '1.5',
  },
  preCode: {
    background: 'none',
    padding: 0,
    color: 'inherit',
    fontFamily: "Consolas, 'Courier New', monospace",
  },
  caixaExemplo: {
    background: 'rgba(255, 255, 255, 0.75)',
    backdropFilter: 'blur(10px)',
    WebkitBackdropFilter: 'blur(10px)',
    border: '1px solid rgba(255, 255, 255, 0.6)',
    borderLeft: '5px solid #007acc',
    color: '#222',
    padding: '12px 16px',
    margin: '15px 0',
    borderRadius: '6px',
  },
  caixaNota: {
    background: 'rgba(255, 244, 214, 0.75)',
    backdropFilter: 'blur(10px)',
    WebkitBackdropFilter: 'blur(10px)',
    border: '1px solid rgba(255, 255, 255, 0.6)',
    borderLeft: '5px solid #d49a00',
    color: '#222',
    padding: '12px 16px',
    margin: '15px 0',
    borderRadius: '6px',
  },
  table: {
    width: '100%',
    borderCollapse: 'collapse',
  },
  th: {
    textAlign: 'left',
    padding: '9px 10px',
    borderBottom: '1px solid rgba(26, 54, 93, 0.15)',
    color: '#1a365d',
  },
  td: {
    textAlign: 'left',
    padding: '9px 10px',
    borderBottom: '1px solid rgba(26, 54, 93, 0.15)',
    fontSize: '11pt',
  },
};

// --- COMPONENTE DE CONCEITOS DO C++ ---
function CppIntro() {
  return (
    <div style={stylesCpp.body}>
      <h1 style={stylesCpp.h1}>Estrutura e Regras Gerais em C++</h1>
      
      <p style={stylesCpp.p}>Ao fim de cada linha de código, deve-se finalizar com ponto e vírgula (;), sem isso o código não vai correr.</p>
      <p style={stylesCpp.p}>Ao começar o código, deves importar o:</p>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>using namespace std;</code> - serve para evitar escrever o prefixo std repetidamente</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>#include &lt;iostream&gt;</code> - serve para permitir a entrada e saída de dados no seu programa em C++</p>
      </div>

      <p style={stylesCpp.p}>Ao atribuir nome à uma variável não deve haver espaçamento e é boa prática que as variáveis sejam com inicial minúscula.</p>

      <h2 style={stylesCpp.h2}>Tipos de Dados</h2>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>string</code> - Diferente de Java, usamos o string com inicial minúsculo. Serve para armazenar dados de tipo texto.</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>int</code> - Tipo de dados que serve para armazenar números inteiros.</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>double</code> - Tipo de dados que serve para armazenar números decimais.</p>
        <br />
        <p style={stylesCpp.p}><em>NOTA: Foram listados apenas os tipos de dados usados neste percurso de aprendizado.</em></p>
      </div>

      <h2 style={stylesCpp.h2}>Sinais e Operadores Principais</h2>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>*</code> : Multiplicação - (Ex: 6 * 3 = 18)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>/</code> : Divisão - (Ex: 93 / 25 = 3.72)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>%</code> : Resto da divisão inteira - (Ex: 20 % 7 = 6)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>+</code> : Adição - (Ex: 48 + 1023 = 1071)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>-</code> : Subtração - (Ex: 188 - 34 = 154)</p>
      </div>

      <h2 style={stylesCpp.h2}>Operadores de Incrementação e Decrementação Unária</h2>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>++</code> : Soma 1 ao operando (pré-incremento ++var ou pós-incremento var++)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>--</code> : Subtrai 1 ao operando (pré-decremento --var ou pós-decremento var--)</p>
        <br />
        <p style={stylesCpp.p}><em>(Isso será melhor compreendido no capítulo de Estruturas de Controlo)</em></p>
      </div>

      <h2 style={stylesCpp.h2}>Operadores de Atribuição Abreviada</h2>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>+=</code> : (Ex: c = 2 . c += 3; equivale a c = 2 + 3 = 5)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>-=</code> : (Ex: d = 5 . d -= 4; equivale a d = 5 - 4 = 1)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>*=</code> : (Ex: e = 3 . e *= 5; equivale a e = 3 * 5 = 15)</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>/=</code> : (Ex: f = 12 . f /= 3; equivale a f = 12 / 3 = 4)</p>
      </div>

      <h2 style={stylesCpp.h2}>Operadores Relacionais</h2>
      
      <div style={stylesCpp.caixaExemplo}>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>&gt;</code> : maior</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>&lt;</code> : menor</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>&gt;=</code> : maior ou igual</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>&lt;=</code> : menor ou igual</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>==</code> : igual</p>
        <p style={stylesCpp.p}><code style={stylesCpp.code}>!=</code> : diferente</p>
      </div>
    </div>
  );
}

const stylesCpp = {
  body: {
    background: 'rgba(255, 255, 255, 0.6)',
    color: '#2b2b2b',
    fontFamily: 'Arial, sans-serif',
    padding: '20px',
    borderRadius: '12px',
    backdropFilter: 'blur(10px)',
    textAlign: 'left',
  },
  h1: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    fontSize: '18pt',
  },
  h2: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    marginTop: '1.5em',
    fontSize: '14pt',
  },
  p: {
    margin: '8px 0',
    lineHeight: '1.6',
    fontSize: '11pt',
  },
  code: {
    fontFamily: "Consolas, 'Courier New', monospace",
    background: 'rgba(26, 54, 93, 0.09)',
    padding: '0.1em 0.4em',
    borderRadius: '4px',
    fontSize: '0.92em',
  },
  caixaExemplo: {
    background: 'rgba(255, 255, 255, 0.75)',
    backdropFilter: 'blur(10px)',
    WebkitBackdropFilter: 'blur(10px)',
    border: '1px solid rgba(255, 255, 255, 0.6)',
    borderLeft: '5px solid #007acc',
    color: '#222',
    padding: '15px',
    margin: '15px 0',
    borderRadius: '6px',
  },
};

// --- COMPONENTE DE CONCEITOS DO ASSEMBLY ---
function AssemblyIntro() {
  return (
    <div style={stylesAssembly.body}>
      <h1 style={stylesAssembly.h1}>O que é o Assembly?</h1>
      
      <p style={stylesAssembly.p}>
        É uma linguagem de baixo nível, muito próxima do hardware. Cada instrução corresponde a uma operação do processador.
      </p>
      <p style={stylesAssembly.p}>
        Um programa escrito em Assembly (ficheiro <code style={stylesAssembly.code}>.asm</code>) é convertido em programa executável por duas ferramentas:
      </p>
      
      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>Montador:</strong> gera o ficheiro objeto (<code style={stylesAssembly.code}>.obj</code>).</p>
        <p style={stylesAssembly.p}><strong>Linkeditor:</strong> junta outros módulos ou bibliotecas e gera o executável (<code style={stylesAssembly.code}>.exe</code>).</p>
      </div>

      <h2 style={stylesAssembly.h2}>Estrutura e Regras Gerais</h2>
      <p style={stylesAssembly.p}>
        Tal como em Java e C++, um programa em Assembly tem uma estrutura obrigatória, composta por directivas:
      </p>

      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>TITLE nome_do_programa:</strong> primeira linha, dá nome ao programa.</p>
        <p style={stylesAssembly.p}><strong>.MODEL SMALL:</strong> define o modelo de memória (código num segmento e dados noutro). Deve vir antes de qualquer segmento.</p>
        <p style={stylesAssembly.p}><strong>.STACK 100h:</strong> reserva espaço para a pilha (100h = 256 bytes).</p>
        <p style={stylesAssembly.p}><strong>.DATA:</strong> segmento de dados, onde se declaram variáveis e constantes.</p>
        <p style={stylesAssembly.p}><strong>.CODE:</strong> segmento de código, onde ficam as instruções, organizadas em procedures.</p>
        <p style={stylesAssembly.p}><strong>nome PROC ... nome ENDP:</strong> delimitam uma procedure.</p>
        <p style={stylesAssembly.p}><strong>END nome:</strong> última linha, indica a procedure principal.</p>
      </div>

      <p style={stylesAssembly.p}>
        <em>Atenção:</em> em Assembly o ponto e vírgula não termina a linha. Ele inicia um comentário (ex: <code style={stylesAssembly.code}>;funcao DOS para exibir caracter</code>).
      </p>

      <h2 style={stylesAssembly.h2}>Formato de Dados</h2>
      <p style={stylesAssembly.p}>Os números são identificados pela letra no final:</p>

      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>Binário:</strong> termina em b ou B (ex: 1110101b)</p>
        <p style={stylesAssembly.p}><strong>Decimal:</strong> sem letra, ou d/D (ex: 64223, 64223d)</p>
        <p style={stylesAssembly.p}><strong>Hexadecimal:</strong> termina em h ou H (ex: 1B4Dh)</p>
        <p style={stylesAssembly.p}>
          <em>Regras:</em> sem letra no fim, o número é considerado decimal (1110101 é decimal). Um hexadecimal tem de começar com um dígito de 0 a 9 (0FFFFh é válido, FFFFh é ilegal). Não se aceitam caracteres estranhos, como a vírgula em 1,234.
        </p>
      </div>

      <h2 style={stylesAssembly.h2}>Caracteres ASCII</h2>
      <p style={stylesAssembly.p}>
        Caracteres isolados ou strings ficam entre aspas simples ou duplas: <code style={stylesAssembly.code}>'A'</code>, <code style={stylesAssembly.code}>"A"</code>, <code style={stylesAssembly.code}>'ola, como vai'</code>.
      </p>

      <h2 style={stylesAssembly.h2}>Tipos de Dados (Declaração de Variáveis)</h2>
      <p style={stylesAssembly.p}>Em Assembly não se usa int ou String. Declara-se pelo tamanho:</p>

      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>DB:</strong> 1 byte (8 bits)</p>
        <p style={stylesAssembly.p}><strong>DW:</strong> 1 word (2 bytes, 16 bits)</p>
        <p style={stylesAssembly.p}><strong>EQU:</strong> define uma constante</p>
        <br />
        <p style={stylesAssembly.p}><strong>Exemplos:</strong></p>
        <p style={stylesAssembly.p}>VAR DB 5 (número pequeno)</p>
        <p style={stylesAssembly.p}>WORD1 DW 0A8h (hexadecimal, começa com 0)</p>
        <p style={stylesAssembly.p}>MENSAGEM DB 'Isto e uma mensagem' (texto)</p>
        <p style={stylesAssembly.p}>LF EQU 0Ah (constante)</p>
      </div>

      <h2 style={stylesAssembly.h2}>Instruções Principais</h2>
      <p style={stylesAssembly.p}>Em vez de operadores como + ou =, o Assembly usa instruções:</p>

      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>MOV destino, origem:</strong> copia um valor (equivale a =)</p>
        <p style={stylesAssembly.p}>
          <strong>INT número:</strong> interrompe o programa e passa o controlo ao DOS, que realiza a operação e devolve o controlo (INT 21h dá acesso às funções de E/S)
        </p>
      </div>

      <h2 style={stylesAssembly.h2}>Registradores Usados na Ficha</h2>
      
      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>AH:</strong> guarda o número da função DOS a executar</p>
        <p style={stylesAssembly.p}><strong>AL:</strong> recebe o código ASCII do caractere lido</p>
        <p style={stylesAssembly.p}><strong>DL:</strong> guarda o código ASCII do caractere a exibir</p>
      </div>

      <h2 style={stylesAssembly.h2}>Entrada e Saída (INT 21h)</h2>
      
      <div style={stylesAssembly.caixaExemplo}>
        <p style={stylesAssembly.p}><strong>Função 1h (AH = 1):</strong> lê um caractere do teclado, que fica em AL</p>
        <p style={stylesAssembly.p}><strong>Função 2h (AH = 2):</strong> exibe no ecrã o caractere que está em DL</p>
        <p style={stylesAssembly.p}><strong>Função 4Ch (AH = 4Ch):</strong> termina o programa e volta ao DOS</p>
      </div>
    </div>
  );
}

const stylesAssembly = {
  body: {
    background: 'rgba(255, 255, 255, 0.6)',
    color: '#2b2b2b',
    fontFamily: 'Arial, sans-serif',
    padding: '20px',
    borderRadius: '12px',
    backdropFilter: 'blur(10px)',
    textAlign: 'left',
  },
  h1: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    fontSize: '18pt',
  },
  h2: {
    fontFamily: "'Times New Roman', Times, serif",
    color: '#1a365d',
    marginTop: '1.5em',
    fontSize: '14pt',
  },
  p: {
    margin: '8px 0',
    lineHeight: '1.6',
    fontSize: '11pt',
  },
  code: {
    fontFamily: "Consolas, 'Courier New', monospace",
    background: 'rgba(26, 54, 93, 0.09)',
    padding: '0.1em 0.4em',
    borderRadius: '4px',
    fontSize: '0.92em',
  },
  caixaExemplo: {
    background: 'rgba(255, 255, 255, 0.75)',
    backdropFilter: 'blur(10px)',
    WebkitBackdropFilter: 'blur(10px)',
    border: '1px solid rgba(255, 255, 255, 0.6)',
    borderLeft: '5px solid #007acc',
    color: '#222',
    padding: '15px',
    margin: '15px 0',
    borderRadius: '6px',
  },
};

// ==========================================================
// --- PÁGINAS PRÁTICAS: Input & Output, Estruturas de Controlo e Vetores ---
// Um único componente (PaginaPratica) mostra os 12 módulos.
// O texto e o código de cada módulo estão em "conteudoPratico" (mais abaixo).
// ==========================================================

const nomesLinguagem = {
  java: 'Java',
  cpp: 'C++',
  python: 'Python',
  assembly: 'Assembly',
};

const simboloComentario = {
  java: '//',
  cpp: '//',
  python: '#',
  assembly: ';',
};

// ==========================================================
// --- LOGO DE CADA LINGUAGEM (usado em todas as páginas) ---
// Se a imagem não carregar, aparece um círculo colorido com a sigla.
// ==========================================================
const LOGOS = {
  java: 'https://www.svgrepo.com/show/303388/java-4-logo.svg',
  cpp: 'https://thumb.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1920px-ISO_C%2B%2B_Logo.svg.png',
  python: 'https://upload.wikimedia.org/wikipedia/commons/3/31/Python-logo.png',
  assembly: 'https://cdn.dribbble.com/userupload/37125886/file/original-6117f521b03664c7331283c90e82075a.png',
};
const SIGLAS_LOGO = { java: 'JAVA', cpp: 'C++', python: 'PY', assembly: 'ASM' };
const CORES_LOGO = { java: '#e76f00', cpp: '#3b82f6', python: '#22c55e', assembly: '#a855f7' };

function LogoLinguagem({ id, tamanho = 48, style }) {
  const [falhou, setFalhou] = useState(false);

  if (falhou) {
    return (
      <div
        style={{
          width: tamanho,
          height: tamanho,
          borderRadius: '50%',
          background: CORES_LOGO[id],
          color: '#ffffff',
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          fontWeight: 'bold',
          fontSize: Math.round(tamanho * 0.28),
          flexShrink: 0,
          ...style,
        }}
      >
        {SIGLAS_LOGO[id]}
      </div>
    );
  }

  return (
    <img
      src={LOGOS[id]}
      alt={`Logotipo de ${nomesLinguagem[id]}`}
      onError={() => setFalhou(true)}
      style={{ width: tamanho, height: tamanho, objectFit: 'contain', ...style }}
    />
  );
}

// Cores de cada linguagem
const temasPratica = {
  java: { destaque: '#38bdf8', borda: '#3b82f6', botao: '#3b82f6', botaoTexto: '#ffffff' },
  cpp: { destaque: '#38bdf8', borda: '#3b82f6', botao: '#3b82f6', botaoTexto: '#ffffff' },
  python: { destaque: '#4ade80', borda: '#22c55e', botao: '#22c55e', botaoTexto: '#0f172a' },
  assembly: { destaque: '#c084fc', borda: '#a855f7', botao: '#a855f7', botaoTexto: '#0f172a' },
};

// ==========================================================
// --- CORRETOR AUTOMÁTICO (corrige o código só com regras) ---
// ==========================================================
// corretor.js — corrige código só com regras. Grátis, sem internet, sem chave.
const MSG_FORA = 'Não posso responder essa mensagem, apenas respondo mensagens de código.';

// Palavras que têm de ser escritas exatamente assim (maiúsculas/minúsculas contam)
const PALAVRAS = {
  java: 'String System int public static void class if else for while do switch case break return new Scanner Math'.split(' '),
  cpp: 'string int double float bool char long void if else for while do switch case break return using namespace cout cin endl include main std'.split(' '),
  python: 'print input int float str len range def if elif else for while return import in and or not True False None'.split(' '),
};
const CORRIGE = { java: 'String', cpp: 'string' };

const INSTR2 = 'mov add sub cmp and or xor test lea xchg'.split(' ');
const INSTR1 = 'inc dec push pop mul div imul idiv neg not jmp je jne jg jl jge jle ja jb jz jnz call loop int shl shr'.split(' ');
const INSTR0 = 'ret nop hlt cld std cli sti pusha popa iret'.split(' ');
const DIRETIVAS = 'section segment ends proc endp global extern org end title assume model stack data code include db dw dd dq equ resb resw resd resq'.split(' ');

// Tira textos entre aspas e comentários, mantendo o número de linhas
function limpar(codigo, lang) {
  let c = codigo.replace(/\r/g, '');
  if (lang !== 'python' && lang !== 'assembly') c = c.replace(/\/\*[\s\S]*?\*\//g, (m) => m.replace(/[^\n]/g, ''));
  return c.split('\n').map((l) => {
    l = l.replace(/"(?:\\.|[^"\\])*"/g, '""').replace(/'(?:\\.|[^'\\])'/g, "''");
    if (lang === 'python') return l.replace(/#.*$/, '');
    if (lang === 'assembly') return l.replace(/;.*$/, '');
    return l.replace(/\/\/.*$/, '');
  });
}

function pareceCodigo(texto, lang) {
  if (lang === 'assembly') return new RegExp('^\\s*(\\w+:)?\\s*(' + [...INSTR2, ...INSTR1, ...INSTR0, ...DIRETIVAS].join('|') + ')\\b', 'im').test(texto) || /^\s*\w+:\s*$/m.test(texto);
  const kw = new RegExp('\\b(' + PALAVRAS[lang].join('|') + ')\\b', 'i');
  return kw.test(texto) || /[;{}=#]/.test(texto);
}

function precisaPontoVirgula(t, proxima) {
  if (!t || /[;{:,(]$/.test(t) || t.startsWith('#')) return false;
  if (t.startsWith('}')) return /^}\s*while\b/.test(t);
  if (/(\+\+|--)$/.test(t)) return true;
  if (/[+\-*/&|=<?]$/.test(t)) return false;                       // linha continua na seguinte
  if (/^(if|for|while|else|switch|do|try|catch|finally|class|struct|namespace|enum|interface|template)\b/.test(t) && !/^do\s*\S/.test(t)) return false;
  if (/\)$/.test(t) && proxima.startsWith('{')) return false;        // cabeçalho de função
  if (/^(public|private|protected)\b/.test(t) && !/[=]/.test(t) && /\)$/.test(t)) return false;
  return true;
}

function corrigir(codigo, lang, nExercicios = 1) {
  if (!codigo.trim()) return { vazio: true };
  if (!pareceCodigo(codigo, lang)) return { foraDeTema: true };

  const linhas = limpar(codigo, lang);
  const original = codigo.replace(/\r/g, '').split('\n');
  const erros = [];
  const add = (i, tipo, problema, correcao) => erros.push({ linha: i + 1, tipo, problema, correcao });
  let linhasDeCodigo = 0;

  linhas.forEach((l, i) => {
    const t = l.trim();
    if (!t) return;
    linhasDeCodigo++;
    const proxima = (linhas.slice(i + 1).find((x) => x.trim()) || '').trim();

    if (lang === 'assembly') {
      let s = t.replace(/^\w+:\s*/, '');
      if (!s) return;
      const [pm, ...resto] = s.split(/\s+/);
      const m = pm.toLowerCase();
      if (DIRETIVAS.includes(m) || m.startsWith('.') || m.startsWith('%') || m.startsWith('[')) return;
      if (/^(db|dw|dd|dq|equ|resb|resw|resd|resq)$/i.test(resto[0] || '')) return;   // ex.: msg db "Olá"
      const ops = resto.join(' ').split(',').map((x) => x.trim()).filter(Boolean);
      if (![...INSTR0, ...INSTR1, ...INSTR2].includes(m)) return add(i, 'instrução', `"${pm}" não é uma instrução conhecida.`, 'Confirma o nome da instrução (ex.: mov, add, sub, cmp, jmp).');
      if (INSTR2.includes(m) && (ops.length !== 2 || resto.join(' ').split(',').length !== 2)) add(i, 'operandos', `"${m}" precisa de 2 operandos separados por vírgula.`, `${m} destino, origem`);
      else if (INSTR2.includes(m) && /^(0x[0-9a-f]+|\d+)$/i.test(ops[0])) add(i, 'destino', 'O destino não pode ser um número.', `${m} registo, ${ops[0]}`);
      else if (INSTR1.includes(m) && ops.length !== 1) add(i, 'operandos', `"${m}" precisa de 1 operando.`, `${m} operando`);
      return;
    }

    // Maiúsculas/minúsculas nas palavras da linguagem
    const vistos = new Set();
    (t.match(/[A-Za-z_]\w*/g) || []).forEach((w) => {
      const certa = PALAVRAS[lang].find((p) => p.toLowerCase() === w.toLowerCase());
      if (certa && certa !== w && !vistos.has(w)) {
        vistos.add(w);
        add(i, 'maiúscula/minúscula', `"${w}" está mal escrito.`, original[i].replace(new RegExp('\\b' + w + '\\b'), certa));
      }
    });

    if (lang === 'python') {
      if (/^(if|elif|else|for|while|def|class|try|except|finally|with)\b/.test(t) && !t.includes(':')) add(i, 'dois pontos', 'Falta ":" no fim da linha.', original[i].trimEnd() + ':');
    } else if (precisaPontoVirgula(t, proxima)) {
      add(i, 'ponto e vírgula', 'Falta ";" no fim da linha.', original[i].trimEnd() + ';');
    }
  });

  if (lang !== 'assembly') {
    const todo = linhas.join('\n');
    [['(', ')', 'parênteses'], ['{', '}', 'chavetas']].forEach(([a, b, nome]) => {
      if (todo.split(a).length !== todo.split(b).length) erros.push({ linha: null, tipo: nome, problema: `Os ${nome} não estão todos fechados.`, correcao: `Confirma se cada "${a}" tem o seu "${b}".` });
    });
  }

  // Descontos: 0,5 por erro; 3 erros do mesmo tipo = 2 valores nesse tipo
  const porTipo = {};
  erros.forEach((e) => (porTipo[e.tipo] = (porTipo[e.tipo] || 0) + 1));
  let desconto = 0;
  Object.values(porTipo).forEach((n) => (desconto += n >= 3 ? 2 : n * 0.5));

  const cotacao = 20 / nExercicios;
  const nota = Math.max(0, cotacao - desconto / nExercicios);
  const comErro = new Set(erros.filter((e) => e.linha).map((e) => e.linha)).size;
  return { erros, desconto, cotacao, nota, nErros: erros.length, acertos: Math.max(0, linhasDeCodigo - comErro), repetidos: Object.keys(porTipo).filter((k) => porTipo[k] >= 3) };
}

const formatarNota = (n) => n.toFixed(2).replace('.', ',');

function criarEstilosPratica(tema) {
  return {
    body: {
      background: '#0f172a',
      color: '#fff',
      fontFamily: 'Arial, sans-serif',
      padding: '15px',
      lineHeight: '1.6',
      width: '100%',
      textAlign: 'left',
      borderRadius: '12px',
      boxSizing: 'border-box',
    },
    h1: {
      color: '#38bdf8',
      textAlign: 'center',
      fontSize: '1.5rem',
      marginTop: 0,
      marginBottom: '10px',
    },
    nota: {
      textAlign: 'center',
      fontStyle: 'italic',
      color: '#94a3b8',
      marginBottom: '20px',
    },
    h2: {
      color: '#facc15',
      fontSize: '1.2rem',
      marginTop: '30px',
      borderBottom: '2px solid #334155',
      paddingBottom: '8px',
    },
    h3: {
      color: '#38bdf8',
      marginTop: '25px',
    },
    p: {
      color: '#cbd5e1',
      margin: '6px 0',
    },
    tituloExemplo: {
      fontSize: '1.05rem',
      fontWeight: 'bold',
      color: tema.destaque,
      marginTop: '15px',
      marginBottom: '4px',
    },
    caixaExemplo: {
      background: 'rgba(255, 255, 255, 0.08)',
      backdropFilter: 'blur(8px)',
      WebkitBackdropFilter: 'blur(8px)',
      border: '1px solid rgba(255, 255, 255, 0.2)',
      color: '#fff',
      padding: '15px',
      marginTop: '12px',
      marginBottom: '15px',
      borderLeft: `4px solid ${tema.borda}`,
      borderRadius: '6px',
      overflowX: 'auto',
    },
    descricaoExemplo: {
      fontWeight: 'bold',
      color: tema.destaque,
      marginBottom: '10px',
    },
    pre: {
      margin: 0,
      fontFamily: "'Courier New', Courier, monospace",
      fontSize: '0.9rem',
      whiteSpace: 'pre-wrap',
      wordBreak: 'break-word',
      color: '#e2e8f0',
    },
    code: {
      fontFamily: 'inherit',
      color: 'inherit',
      background: 'none',
      padding: 0,
    },
    notaCodigo: {
      color: '#cbd5e1',
      fontSize: '0.9rem',
      marginTop: '-5px',
      marginBottom: '15px',
    },
    exerciciosTexto: {
      background: 'rgba(255, 255, 255, 0.05)',
      border: '1px solid rgba(255, 255, 255, 0.1)',
      padding: '15px',
      borderRadius: '6px',
      marginTop: '10px',
      marginBottom: '20px',
    },
    areaInsercao: {
      marginTop: '15px',
      display: 'flex',
      flexDirection: 'column',
      gap: '8px',
    },
    labelEditor: {
      fontSize: '0.9rem',
      color: tema.destaque,
      fontWeight: '600',
    },
    textareaCode: {
      width: '100%',
      background: '#020617',
      color: tema.destaque,
      border: '1px solid rgba(255, 255, 255, 0.2)',
      borderRadius: '6px',
      padding: '12px',
      fontFamily: "'Courier New', Courier, monospace",
      fontSize: '0.95rem',
      lineHeight: '1.4',
      resize: 'vertical',
      outline: 'none',
      boxSizing: 'border-box',
    },
    botaoSubmeter: {
      alignSelf: 'flex-start',
      backgroundColor: tema.botao,
      color: tema.botaoTexto,
      border: 'none',
      padding: '10px 18px',
      borderRadius: '6px',
      fontWeight: 'bold',
      fontSize: '0.9rem',
      cursor: 'pointer',
      transition: 'background-color 0.2s ease',
      marginTop: '5px',
    },
    resCaixa: {
      marginTop: '8px',
      borderTop: '1px solid rgba(255, 255, 255, 0.15)',
      paddingTop: '12px',
    },
    resNota: { color: '#facc15', fontSize: '1.4rem', fontWeight: 'bold' },
    resAviso: { color: '#fbbf24', margin: '8px 0' },
    resOk: { color: '#4ade80', margin: '8px 0' },
    resErro: {
      borderLeft: '4px solid #f87171',
      background: 'rgba(248, 113, 113, 0.08)',
      padding: '8px 12px',
      borderRadius: '4px',
      margin: '10px 0',
    },
    resErroTitulo: { color: '#f87171', fontWeight: 'bold' },
    resPre: {
      margin: '6px 0 0',
      fontFamily: "'Courier New', Courier, monospace",
      color: '#4ade80',
      whiteSpace: 'pre-wrap',
      wordBreak: 'break-all',
    },
  };
}

// linguagem: 'java' | 'cpp' | 'python' | 'assembly'
// modulo: 'io' | 'ciclos' | 'vetores'
// respostas / aoMudarResposta: guardados no App, para não perderes o que escreveste ao voltar atrás
function PaginaPratica({ linguagem, modulo, respostas, aoMudarResposta, aoCorrigir }) {
  const dados = conteudoPratico[linguagem][modulo];
  const estilos = criarEstilosPratica(temasPratica[linguagem]);
  const nome = nomesLinguagem[linguagem];
  const simbolo = simboloComentario[linguagem];

  // Resultado da correção de cada exercício
  const [resultados, setResultados] = useState({});

  const submeter = (id, codigo) => {
    const res = corrigir(codigo || '', linguagem, dados.exercicios.length);
    setResultados((anterior) => ({ ...anterior, [id]: res }));
    if (aoCorrigir) aoCorrigir(id, res);
  };

  const escreverCodigo = (id, valor) => {
    aoMudarResposta(id, valor);
    setResultados((anterior) => ({ ...anterior, [id]: null }));
  };

  return (
    <div style={estilos.body}>
      <h1 style={estilos.h1}>{dados.titulo}</h1>
      {dados.nota && <p style={estilos.nota}>{dados.nota}</p>}

      {/* Secções com explicação e exemplos */}
      {dados.secoes.map((secao, i) => (
        <section key={i}>
          <h2 style={estilos.h2}>{secao.titulo}</h2>
          {secao.texto && <p style={estilos.p}>{secao.texto}</p>}

          {secao.exemplos.map((ex, j) => (
            <div key={j}>
              {ex.titulo && <div style={estilos.tituloExemplo}>{ex.titulo}</div>}
              {ex.texto && <p style={estilos.p}>{ex.texto}</p>}

              <div style={estilos.caixaExemplo}>
                {ex.descricao && <div style={estilos.descricaoExemplo}>{ex.descricao}</div>}
                <pre style={estilos.pre}>
                  <code style={estilos.code}>{ex.codigo}</code>
                </pre>
              </div>

              {ex.nota && <p style={estilos.notaCodigo}>{ex.nota}</p>}
            </div>
          ))}
        </section>
      ))}

      {/* Exercícios para o utilizador resolver */}
      <section>
        <h2 style={estilos.h2}>{dados.tituloExercicios}</h2>
        {dados.textoExercicios && <p style={estilos.p}>{dados.textoExercicios}</p>}

        {dados.exercicios.map((exercicio, i) => {
          const id = `${linguagem}_${modulo}_${i}`;
          return (
            <div key={id}>
              {exercicio.grupo && <h3 style={estilos.h3}>{exercicio.grupo}</h3>}
              <div style={estilos.exerciciosTexto}>
                <p style={estilos.p}>
                  <strong>{exercicio.rotulo}:</strong> {exercicio.enunciado}
                </p>
                {exercicio.observacao && (
                  <p style={{ ...estilos.p, fontStyle: 'italic' }}>{exercicio.observacao}</p>
                )}

                <div style={estilos.areaInsercao}>
                  <label style={estilos.labelEditor}>
                    Escreve ou cola o teu código {nome} aqui:
                  </label>
                  <textarea
                    style={estilos.textareaCode}
                    placeholder={`${simbolo} Digita o teu código ${nome} aqui...`}
                    value={respostas[id] || ''}
                    onChange={(e) => escreverCodigo(id, e.target.value)}
                    rows={8}
                    spellCheck={false}
                  />
                  <button style={estilos.botaoSubmeter} onClick={() => submeter(id, respostas[id])}>
                    Submeter Código
                  </button>

                  {resultados[id] && resultados[id].vazio && (
                    <p style={estilos.resAviso}>Escreve primeiro o teu código.</p>
                  )}
                  {resultados[id] && resultados[id].foraDeTema && (
                    <p style={estilos.resAviso}>{MSG_FORA}</p>
                  )}
                  {resultados[id] && resultados[id].erros && (
                    <div style={estilos.resCaixa}>
                      <div style={estilos.resNota}>
                        Nota: {formatarNota(resultados[id].nota)} / {formatarNota(resultados[id].cotacao)}
                      </div>
                      <p style={estilos.p}>
                        Acertos: {resultados[id].acertos} linhas &nbsp;|&nbsp; Erros: {resultados[id].nErros} &nbsp;|&nbsp; Desconto: {formatarNota(resultados[id].desconto / dados.exercicios.length)}
                      </p>
                      {resultados[id].repetidos.length > 0 && (
                        <p style={estilos.resAviso}>
                          Erros repetidos 3 vezes ou mais: {resultados[id].repetidos.join(', ')} (desconto de 2 valores por tipo).
                        </p>
                      )}
                      {resultados[id].erros.length === 0 && (
                        <p style={estilos.resOk}>Sem erros encontrados. Muito bem!</p>
                      )}
                      {resultados[id].erros.map((e, k) => (
                        <div key={k} style={estilos.resErro}>
                          <div style={estilos.resErroTitulo}>
                            {e.linha ? `Linha ${e.linha}` : 'Código todo'} — {e.tipo} (−0,5)
                          </div>
                          <div style={estilos.p}>{e.problema}</div>
                          <pre style={estilos.resPre}>{e.correcao}</pre>
                        </div>
                      ))}
                    </div>
                  )}
                </div>
              </div>
            </div>
          );
        })}
      </section>
    </div>
  );
}

// ==========================================================
// --- CONTEÚDO DOS MÓDULOS ---
// ==========================================================

const conteudoPratico = {
  // ------------------------------------------------------
  // JAVA
  // ------------------------------------------------------
  java: {
    io: {
      titulo: 'Capítulo Prático: Resolução dos Exercícios',
      secoes: [
        {
          titulo: 'Exemplos Práticos Resolvidos',
          exemplos: [
            {
              titulo: 'Exemplo 1 — Estático',
              texto: 'Programa Java que declara dois números inteiros (int), calcula a sua multiplicação e mostra o resultado no ecrã.',
              codigo: `import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {

        int num1 = 5;
        int num2 = 4;
        int multiplicacao = num1 * num2;

        System.out.println("A multiplicação é: " + multiplicacao);
    }
}`,
            },
            {
              titulo: 'Exemplo 2 — Input e output',
              texto: 'Programa Java que pede ao utilizador dois números inteiros e, no final, mostra a diferença entre eles.',
              codigo: `import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {

        BufferedReader br = new BufferedReader(
            new InputStreamReader(System.in));

        int n1, n2, diferenca;

        System.out.print("Digite o primeiro número inteiro: ");
        n1 = Integer.parseInt(br.readLine());

        System.out.print("Digite o segundo número inteiro: ");
        n2 = Integer.parseInt(br.readLine());

        diferenca = n1 - n2;

        System.out.println("A diferença entre os números é: " + diferenca);
    }
}`,
            },
            {
              titulo: 'Exemplo 3 — Input e output (Papelaria)',
              texto: 'Programa que calcula o valor total a pagar por cadernos a um preço fixo de 150 meticais.',
              codigo: `import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {

        BufferedReader br = new BufferedReader(
            new InputStreamReader(System.in));

        String nome;
        int quantidade;
        double precoUnitario = 150.0;
        double valorTotal;

        System.out.print("Digite o seu nome: ");
        nome = br.readLine();

        System.out.print("Digite a quantidade de cadernos que deseja comprar: ");
        quantidade = Integer.parseInt(br.readLine());

        valorTotal = quantidade * precoUnitario;

        System.out.println("\\n--- Resumo da Compra ---");
        System.out.println("Nome do cliente: " + nome);
        System.out.println("Quantidade de cadernos: " + quantidade);
        System.out.println("Valor total a pagar: " + valorTotal + " MT");
    }
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios para Resolver',
      exercicios: [
        {
          rotulo: 'Exercício 1 — Estático',
          enunciado: 'Cria um programa Java que declare dois números inteiros (int), calcule a sua multiplicação e mostre o resultado no ecrã.',
        },
        {
          rotulo: 'Exercício 2 — Input e output',
          enunciado: 'Cria um programa Java que peça ao utilizador dois números inteiros e, no final, mostre a diferença entre eles.',
        },
        {
          rotulo: 'Exercício 3 — Input e output',
          enunciado: 'Uma papelaria vende cadernos a um preço fixo de 150 meticais cada. Cria um programa que peça ao utilizador o seu nome e a quantidade de cadernos que pretende comprar. Depois, o programa deve calcular e apresentar o nome do cliente, a quantidade comprada e o valor total a pagar.',
        },
      ],
    },

    ciclos: {
      titulo: 'Capítulo Prático: Estruturas de Controlo e Ciclos em Java',
      secoes: [
        {
          titulo: '1. Selecção Simples (if)',
          texto: 'A estrutura de selecção simples permite avaliar uma condição lógica inicial para decidir se um determinado bloco de instruções deve ou não ser executado, prosseguindo o programa normalmente após a verificação.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar se um número é maior que 10 e se a idade permite entrada num evento (maior ou igual a 18).',
              codigo: `import java.io.*;

public class SelecaoSimplesExemplo {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        int num1, idade;
        
        System.out.println("Introduza o numero: ");
        num1 = Integer.parseInt(x.readLine());
        if (num1 > 10) {
            System.out.println("Numero maior que 10: " + num1);
        }
        
        System.out.println("Introduza a idade: ");
        idade = Integer.parseInt(x.readLine());
        if (idade >= 18) {
            System.out.println("Acesso permitido.");
        }
    }
}`,
            },
          ],
        },
        {
          titulo: '2. Selecção Dupla (if-else)',
          texto: 'A estrutura de selecção dupla escolhe exatamente um entre dois blocos de instruções alternativos para executar, dependendo exclusivamente de a condição avaliada resultar em verdadeiro ou falso.',
          exemplos: [
            {
              descricao: 'Exemplo: Verificar paridade de um número e aprovação de um estudante.',
              codigo: `import java.io.*;

public class SelecaoDuplaExemplo {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        int num, nota;
        
        System.out.println("Introduza um numero inteiro: ");
        num = Integer.parseInt(x.readLine());
        if (num % 2 == 0) {
            System.out.println("O numero " + num + " e par");
        } else {
            System.out.println("O numero " + num + " e impar");
        }
        
        System.out.println("Introduza a nota do estudante: ");
        nota = Integer.parseInt(x.readLine());
        if (nota >= 10) {
            System.out.println("Estudante Aprovado");
        } else {
            System.out.println("Estudante Nao Aprovado");
        }
    }
}`,
            },
          ],
        },
        {
          titulo: '3. Selecção em Alternativa (if-else-if)',
          texto: 'A selecção em alternativa permite o encadeamento sequencial de várias condições para selecionar e executar unicamente um bloco de instruções de entre múltiplas opções possíveis.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Cálculo de função matemática com base em intervalos de A.',
              codigo: `import java.io.*;

public class SelecaoAlternativaEx1 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        double a, b, c, y;
        
        System.out.println("Intr. o valor de A: ");
        a = Double.parseDouble(x.readLine());
        System.out.println("Intr. o valor de B: ");
        b = Double.parseDouble(x.readLine());
        System.out.println("Intr. o valor de C: ");
        c = Double.parseDouble(x.readLine());
        
        if (a > 300) {
            y = a * b + c;
        } else if (a == 300) {
            y = Math.sqrt(a * b + c);
        } else {
            y = (a / c + b) * (a / c + b);
        }
        System.out.println("O valor de y = " + y);
    }
}`,
            },
            {
              descricao: 'Exemplo 2: Classificar o escalão de uma nota numérica inteira.',
              codigo: `import java.io.*;

public class SelecaoAlternativaEx2 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        int nota;
        
        System.out.println("Introduza a nota inteira (0 a 20): ");
        nota = Integer.parseInt(x.readLine());
        
        if (nota >= 16) {
            System.out.println("Escalao: Excelente");
        } else if (nota >= 14) {
            System.out.println("Escalao: Bom");
        } else if (nota >= 10) {
            System.out.println("Escalao: Suficiente");
        } else {
            System.out.println("Escalao: Insuficiente");
        }
    }
}`,
            },
          ],
        },
        {
          titulo: '4. Selecção Múltipla (switch-case)',
          texto: 'A estrutura de selecção múltipla avalia o resultado de uma expressão inteira ou de tipo caracter para direcionar de forma direta e eficiente o fluxo para o bloco case correspondente.',
          exemplos: [
            {
              descricao: 'Exemplos: Calcular área de figuras geométricas e seleção de dia da semana.',
              codigo: `import java.io.*;

public class SelecaoMultiplaExemplo {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        char letra;
        int opcao;
        double b, h, area;
        
        System.out.println("Calcular area de Rectangulo(R), Triangulo(T) ou Circulo(C)? ");
        letra = x.readLine().charAt(0);
        switch (letra) {
            case 'R': case 'r':
                System.out.print("Valor da base: ");
                b = Double.parseDouble(x.readLine());
                System.out.print("Valor da altura: ");
                h = Double.parseDouble(x.readLine());
                area = b * h;
                System.out.println("Area do rect= " + area);
                break;
            case 'T': case 't':
                System.out.print("Valor da base: ");
                b = Double.parseDouble(x.readLine());
                System.out.print("Valor da altura: ");
                h = Double.parseDouble(x.readLine());
                System.out.println("Area do triangulo= " + (b * h / 2));
                break;
            case 'C': case 'c':
                System.out.println("Introduza o valor do raio: ");
                b = Double.parseDouble(x.readLine());
                area = Math.PI * b * b;
                System.out.println("Area do circulo= " + area);
                break;
            default:
                System.out.println("Introduziu a letra errada");
                break;
        }

        System.out.println("Introduza uma opcao de 1 a 3 para o dia da semana: ");
        opcao = Integer.parseInt(x.readLine());
        switch (opcao) {
            case 1:
                System.out.println("Segunda-feira");
                break;
            case 2:
                System.out.println("Terca-feira");
                break;
            case 3:
                System.out.println("Quarta-feira");
                break;
            default:
                System.out.println("Opcao invalida");
                break;
        }
    }
}`,
            },
          ],
        },
        {
          titulo: '5. Ciclo For (for)',
          texto: 'O ciclo for é uma estrutura de repetição controlada por contador que permite executar um bloco de instruções de forma repetida um número exato e predeterminado de vezes.',
          exemplos: [
            {
              descricao: 'Exemplos: Contagem decrescente e exibição de tabuada/múltiplos.',
              codigo: `import java.io.*;

public class CicloForExemplo {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        int n, i;
        
        System.out.println("Introduza um numero inteiro para contagem inversa: ");
        n = Integer.parseInt(x.readLine());
        System.out.println("Contagem inversa:");
        for (i = n; i >= 0; i--) {
            System.out.println(i);
        }
        
        System.out.println("Introduza um numero para ver a tabuada (ate 5): ");
        n = Integer.parseInt(x.readLine());
        for (i = 1; i <= 5; i++) {
            System.out.println(n + " x " + i + " = " + (n * i));
        }
    }
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios',
      exercicios: [
        {
          rotulo: 'Exercício 1',
          enunciado: 'Faça um programa que receba um número inteiro correspondente a um ano e devolva se o ano é bissexto ou não.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Faça um programa que calcula a idade, consoante a faixa etária deve informar na saída se é criança, jovem, adulto ou idoso.',
        },
        {
          rotulo: 'Exercício 3',
          enunciado: 'Usando a estrutura de controle switch-case elabore um programa em Java que imita uma ATM, onde o usuário poderá: A – Visualizar o saldo. B – Levantar valor. C – Transferir o valor.',
          observacao: 'PS: O saldo inicial da conta é de 20,000MT, nos casos de levantamento e transferência deve-se subtrair o montante que se pretende usar para a transação.',
        },
      ],
    },

    vetores: {
      titulo: 'Vetores em Java',
      secoes: [
        {
          titulo: '1. Array Unidimensional (Vetor)',
          texto: 'Um array unidimensional, comummente conhecido como vetor, é uma estrutura de dados homogénea que armazena uma lista linear de elementos do mesmo tipo em posições consecutivas de memória, permitindo o acesso rápido aos valores através de um único índice numérico que começa em zero.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Alocação dinâmica de um vetor para armazenar notas inteiras introduzidas pelo utilizador.',
              codigo: `import java.io.*;

public class VetorExemplo1 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        
        System.out.println("Introduza o numero de notas a armazenar: ");
        int quant = Integer.parseInt(x.readLine());
        int notas[] = new int[quant];
        
        for (int i = 0; i < notas.length; i++) {
            System.out.println("Introduza a nota " + (i + 1) + ": ");
            notas[i] = Integer.parseInt(x.readLine());
        }
        
        System.out.println("Notas armazenadas com sucesso.");
    }
}`,
            },
            {
              descricao: 'Exemplo 2: Inicialização abreviada de um vetor com valores de temperaturas (double).',
              codigo: `import java.io.*;

public class VetorExemplo2 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        double temperaturas[] = {25.5, 26.0, 24.2, 28.1, 30.0};
        
        System.out.println("Temperaturas registadas:");
        for (int i = 0; i < temperaturas.length; i++) {
            System.out.println("Posicao " + i + ": " + temperaturas[i] + " graus");
        }
    }
}`,
            },
          ],
        },
        {
          titulo: '2. Array Bidimensional (Matriz)',
          texto: 'Um array bidimensional, designado por matriz, consiste numa estrutura em que cada elemento do array principal é, por sua vez, outro array, organizando os dados em linhas e colunas e exigindo dois índices para o seu acesso específico.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Declaração e alocação de uma matriz de preços (double) com 3 linhas e 2 colunas.',
              codigo: `import java.io.*;

public class MatrizExemplo1 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        double precos[][] = new double[3][2];
        
        for (int i = 0; i < precos.length; i++) {
            for (int j = 0; j < precos[0].length; j++) {
                System.out.println("Introduza o preco para a posicao [" + i + "][" + j + "]: ");
                precos[i][j] = Double.parseDouble(x.readLine());
            }
        }
        
        System.out.println("Matriz de precos preenchida com sucesso.");
    }
}`,
            },
            {
              descricao: 'Exemplo 2: Inicialização direta de uma matriz de idades (int) com 3 linhas e 2 colunas.',
              codigo: `import java.io.*;

public class MatrizExemplo2 {
    public static void main(String[] args) throws IOException {
        BufferedReader x = new BufferedReader(new InputStreamReader(System.in));
        int[][] idade = {{12, 30}, {3, 7}, {70, 26}};
        
        System.out.println("Conteudo da matriz de idades:");
        for (int i = 0; i < idade.length; i++) {
            for (int j = 0; j < idade[0].length; j++) {
                System.out.print(idade[i][j] + " ");
            }
            System.out.println();
        }
    }
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          grupo: 'Arrays Unidimensionais:',
          rotulo: 'Exercício 1',
          enunciado: 'Armazenar quaisquer valores num array de N elementos, determinar a quantidade de números negativos existentes e visualizar os elementos que ocupam as primeiras 3 posições.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Receber várias idades do teclado e visualizá-las em ordem crescente.',
        },
        {
          grupo: 'Arrays Bidimensionais:',
          rotulo: 'Exercício 3',
          enunciado: 'Preencher um array bidimensional de 3 linhas e 2 colunas com valores e visualizar o conteúdo do array no ecrã na forma de tabela.',
        },
        {
          rotulo: 'Exercício 4',
          enunciado: 'Validar o número de uma coluna escolhida pelo utilizador e calcular a soma de elementos que se encontram nessa coluna.',
        },
      ],
    },
  },

  // ------------------------------------------------------
  // C++
  // ------------------------------------------------------
  cpp: {
    io: {
      titulo: 'Capítulo Prático: Exercícios de C++',
      secoes: [
        {
          titulo: 'Exemplos Práticos Resolvidos',
          exemplos: [
            {
              titulo: 'Exemplo 1 — Estático',
              texto: 'Programa que declara dois números inteiros (int), calcula a sua multiplicação e mostra o resultado no ecrã.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int n1 = 6;
    int n2 = 7;
    int multiplicacao = n1 * n2;

    cout << "A multiplicacao e: " << multiplicacao;

    return 0;
}`,
            },
            {
              titulo: 'Exemplo 2 — Input e output',
              texto: 'Programa que pede ao utilizador dois números inteiros e, no final, mostra a diferença entre eles.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int n1, n2, diferenca;

    cout << "Digite o primeiro numero inteiro: ";
    cin >> n1;

    cout << "Digite o segundo numero inteiro: ";
    cin >> n2;

    diferenca = n1 - n2;

    cout << "A diferenca entre os numeros e: " << diferenca;

    return 0;
}`,
            },
            {
              titulo: 'Exemplo 3 — Input e output (Papelaria)',
              texto: 'Programa que pede o nome e a quantidade de cadernos (a 150 MT cada), apresentando o resumo da compra.',
              codigo: `#include <iostream>
#include <string>
using namespace std;

int main() {
    string nome;
    int quantidade;
    float precoUnitario = 150.0;
    float valorTotal;

    cout << "Digite o seu nome: ";
    cin >> nome;

    cout << "Digite a quantidade de cadernos: ";
    cin >> quantidade;

    valorTotal = quantidade * precoUnitario;

    cout << "\\n--- Resumo da Compra ---";
    cout << "\\nNome do cliente: " << nome;
    cout << "\\nQuantidade de cadernos: " << quantidade;
    cout << "\\nValor total a pagar: " << valorTotal << " MT";

    return 0;
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios para Resolver',
      exercicios: [
        {
          rotulo: 'Exercício 1 — Estático',
          enunciado: 'Cria um programa que declare dois números inteiros (int), calcule a sua multiplicação e mostre o resultado no ecrã.',
        },
        {
          rotulo: 'Exercício 2 — Input e output',
          enunciado: 'Cria um programa que peça ao utilizador dois números inteiros e, no final, mostre a diferença entre eles.',
        },
        {
          rotulo: 'Exercício 3 — Input e output',
          enunciado: 'Uma papelaria vende cadernos a um preço fixo de 150 meticais cada. Cria um programa que peça ao utilizador o seu nome e a quantidade de cadernos que pretende comprar, apresentando o nome, a quantidade e o valor total a pagar.',
        },
      ],
    },

    ciclos: {
      titulo: 'Estruturas de Controlo em C++',
      secoes: [
        {
          titulo: '1. Selecção Simples (if)',
          texto: 'A estrutura de selecção simples permite testar uma condição e executar um comando caso o resultado seja verdadeiro.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar se um número é maior que 10 e se a idade permite entrada num evento (maior ou igual a 18).',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int num, idade;
    
    cout << "Introduza um numero: ";
    cin >> num;
    if (num > 10) {
        cout << "O numero e maior que 10." << endl;
    }
    
    cout << "Introduza a idade: ";
    cin >> idade;
    if (idade >= 18) {
        cout << "Acesso permitido ao evento." << endl;
    }
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '2. Selecção Dupla (if-else)',
          texto: 'A estrutura de selecção dupla é empregue quando existem duas condições ou caminhos alternativos de execução possíveis.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar paridade de um número e aprovação de um estudante.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int num, nota;
    
    cout << "Introduza um numero inteiro: ";
    cin >> num;
    if (num % 2 == 0) {
        cout << "O numero " << num << " e par." << endl;
    } else {
        cout << "O numero " << num << " e impar." << endl;
    }
    
    cout << "Introduza a nota do estudante: ";
    cin >> nota;
    if (nota >= 10) {
        cout << "Estudante Aprovado." << endl;
    } else {
        cout << "Estudante Reprovado." << endl;
    }
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '3. Selecção em Alternativa / Encadeada (if-else-if)',
          texto: 'Permite determinar conjuntos de comandos a executar quando existem mais do que duas alternativas possíveis, encadeando múltiplos testes condicionais.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar intervalos de um número e classificar o escalão de uma nota.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int num, nota;
    
    cout << "Introduza um numero: ";
    cin >> num;
    if (num >= 0 && num <= 10) {
        cout << "O numero esta entre 0 e 10." << endl;
    } else if (num >= 11 && num <= 1000) {
        cout << "O numero esta entre 11 e 1000." << endl;
    } else if (num > 1000) {
        cout << "O numero e 1000 para frente." << endl;
    } else {
        cout << "Numero negativo." << endl;
    }
    
    cout << "Introduza a nota (0 a 20): ";
    cin >> nota;
    if (nota >= 16) {
        cout << "Escalao: Excelente" << endl;
    } else if (nota >= 14) {
        cout << "Escalao: Bom" << endl;
    } else if (nota >= 10) {
        cout << "Escalao: Suficiente" << endl;
    } else {
        cout << "Escalao: Insuficiente" << endl;
    }
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '4. Selecção Múltipla (switch)',
          texto: 'A declaração switch é uma maneira simples de fazer uma tomada de decisão com múltiplas escolhas, testando uma variável contra uma lista de constantes inteiras ou caracteres.',
          exemplos: [
            {
              descricao: 'Exemplos: Operação de calculadora básica e selecionar o dia da semana.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    char op;
    double a, b;
    int opcao;
    
    cout << "Escolha a operacao (+, -, *, /): ";
    cin >> op;
    cout << "Introduza dois valores: ";
    cin >> a >> b;
    switch (op) {
        case '+':
            cout << "Resultado: " << a + b << endl;
            break;
        case '-':
            cout << "Resultado: " << a - b << endl;
            break;
        case '*':
            cout << "Resultado: " << a * b << endl;
            break;
        case '/':
            cout << "Resultado: " << a / b << endl;
            break;
        default:
            cout << "Operacao invalida." << endl;
            break;
    }
    
    cout << "Introduza uma opcao (1 a 3): ";
    cin >> opcao;
    switch (opcao) {
        case 1:
            cout << "Segunda-feira" << endl;
            break;
        case 2:
            cout << "Terca-feira" << endl;
            break;
        case 3:
            cout << "Quarta-feira" << endl;
            break;
        default:
            cout << "Opcao invalida." << endl;
            break;
    }
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '5. Ciclo While (while)',
          texto: 'Especifica a execução de um loop onde a expressão de controle é avaliada antes de cada possível execução dos comandos.',
          exemplos: [
            {
              descricao: 'Exemplos: Ciclo que termina com 0 e contagem de 1 até 5.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int num = 1;
    while (num != 0) {
        cout << "Introduza um numero (pressione 0 para sair): ";
        cin >> num;
        cout << "Voce introduziu: " << num << endl;
    }
    cout << "Ciclo terminado." << endl;
    
    int contador = 1;
    while (contador <= 5) {
        cout << "Contador: " << contador << endl;
        contador++;
    }
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '6. Ciclo Do-While (do-while)',
          texto: 'Semelhante ao while, com a diferença fundamental de que o teste condicional é efetuado após a execução dos comandos pertencentes ao laço (garantindo pelo menos uma execução).',
          exemplos: [
            {
              descricao: 'Exemplos: Solicitar número positivo repetidamente e menu interativo simples.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int num;
    do {
        cout << "Introduza um numero positivo: ";
        cin >> num;
    } while (num <= 0);
    cout << "Numero valido introduzido: " << num << endl;
    
    int opcao;
    do {
        cout << "Menu: 1. Continuar | 0. Sair: ";
        cin >> opcao;
    } while (opcao != 0);
    cout << "Programa encerrado." << endl;
    
    return 0;
}`,
            },
          ],
        },
        {
          titulo: '7. Ciclo For (for)',
          texto: 'Utiliza-se para realizar tarefas repetitivas controladas por um valor inicial, uma condição testada e um incremento.',
          exemplos: [
            {
              descricao: 'Exemplos: Contagem decrescente e exibição de tabuada/múltiplos.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Introduza um numero para contagem inversa: ";
    cin >> n;
    for (int i = n; i >= 0; i--) {
        cout << i << endl;
    }
    
    cout << "Introduza um numero para ver a tabuada (ate 5): ";
    cin >> n;
    for (int i = 1; i <= 5; i++) {
        cout << n << " x " << i << " = " << (n * i) << endl;
    }
    
    return 0;
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios',
      textoExercicios: 'Estes três exercícios finais foram selecionados diretamente da ficha de exercícios de C++ para servir de prática autónoma:',
      exercicios: [
        {
          rotulo: 'Exercício 1',
          enunciado: 'Faça um programa que calcule a potência, sendo os dados de entrada (base e expoente) introduzidos pelo usuário.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Elabore um programa que pede os lados de um triângulo e informa se o triângulo é equilátero, isósceles ou escaleno.',
        },
        {
          rotulo: 'Exercício 3',
          enunciado: 'Faça um programa que visualiza os números múltiplos de 5 entre 50 e 100.',
        },
      ],
    },

    vetores: {
      titulo: 'Vetores em C++',
      secoes: [
        {
          titulo: '1. Array Unidimensional (Vetor)',
          texto: 'Um array unidimensional, conhecido como vector, é uma estrutura de dados que armazena um conjunto de elementos do mesmo tipo em posições consecutivas de memória, permitindo aceder de forma rápida a qualquer valor através de um índice numérico que começa em zero.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Inicialização e visualização de um array de notas inteiras utilizando índices específicos.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int notas[5] = {12, 7, 18, 11, 9};
    
    cout << "Os valores sao:\\n";
    cout << notas[0] << endl;
    cout << notas[4] << endl;
    
    system("PAUSE");
    return EXIT_SUCCESS;
}`,
            },
            {
              descricao: 'Exemplo 2: Preenchimento e percurso de um vector de tamanho dinâmico utilizando a consola e ciclos for.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Digite um valor limite\\n";
    cin >> n;
    
    int *vector = new int[n];
    cout << "Digite os elementos do vector\\n";
    for(int i = 0; i < n; i++) {
        cin >> vector[i];
    }
    
    cout << "A saida e:\\n";
    for(int i = 0; i < n; i++) {
        cout << vector[i] << " ";
    }
    cout << endl;
    
    delete[] vector;
    system("PAUSE");
    return EXIT_SUCCESS;
}`,
            },
          ],
        },
        {
          titulo: '2. Array Bidimensional (Matriz)',
          texto: 'Um array bidimensional, designado por matriz, estende o conceito de vector adicionando uma estrutura de linhas e colunas, onde cada elemento individual é endereçado por dois índices combinados (linha e coluna).',
          exemplos: [
            {
              descricao: 'Exemplo 1: Declaração e criação de uma matriz com 3 linhas e 5 colunas estáticas.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int Matriz[3][5];
    
    // Atribuicao de exemplo na primeira posicao
    Matriz[0][0] = 10;
    
    cout << "Elemento na posicao [0][0]: " << Matriz[0][0] << endl;
    
    system("PAUSE");
    return EXIT_SUCCESS;
}`,
            },
            {
              descricao: 'Exemplo 2: Percurso e visualização de uma matriz de dados estáticos com recurso a ciclos for aninhados.',
              codigo: `#include <iostream>
using namespace std;

int main() {
    int matriz[2][3] = {{1, 2, 3}, {4, 5, 6}};
    
    cout << "Conteudo da matriz 2x3:\\n";
    for(int i = 0; i < 2; i++) {
        for(int j = 0; j < 3; j++) {
            cout << matriz[i][j] << " ";
        }
        cout << endl;
    }
    
    system("PAUSE");
    return EXIT_SUCCESS;
}`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          grupo: 'Arrays Unidimensionais:',
          rotulo: 'Exercício 1',
          enunciado: 'Faça um programa que leia cinco nomes por teclado, e depois imprima esses nomes na ordem inversa em que foram digitados pelo usuário.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Fazer um programa para ler um vetor de inteiros positivos de 50 posições. Imprimir a quantidade de números pares e de múltiplos de 5.',
        },
        {
          grupo: 'Arrays Bidimensionais:',
          rotulo: 'Exercício 3',
          enunciado: 'Faça um programa para visualizar uma matriz de dimensão 2x3.',
        },
        {
          rotulo: 'Exercício 4',
          enunciado: 'Faça um programa para ler notas de 2 testes de cinco estudantes. Deverá imprimir a média de cada estudante.',
        },
      ],
    },
  },

  // ------------------------------------------------------
  // PYTHON
  // ------------------------------------------------------
  python: {
    io: {
      titulo: 'Capítulo Prático: Exercícios de Python',
      secoes: [
        {
          titulo: 'Exemplos Práticos Resolvidos',
          exemplos: [
            {
              titulo: 'Exemplo 1 — Estático',
              texto: 'Programa que declara dois números inteiros, calcula a sua multiplicação e mostra o resultado no ecrã.',
              codigo: `num1 = 8
num2 = 6

multiplicacao = num1 * num2

print("A multiplicação é:", multiplicacao)`,
            },
            {
              titulo: 'Exemplo 2 — Input e output',
              texto: 'Programa que pede ao utilizador dois números inteiros e, no final, mostra a diferença entre eles.',
              codigo: `n1 = int(input("Digite o primeiro número inteiro: "))
n2 = int(input("Digite o segundo número inteiro: "))

diferenca = n1 - n2

print("A diferença entre os números é:", diferenca)`,
            },
            {
              titulo: 'Exemplo 3 — Input e output (Papelaria)',
              texto: 'Programa que pede ao utilizador o nome e a quantidade de cadernos (a 150 MT cada), apresentando o resumo da compra.',
              codigo: `nome = input("Digite o seu nome: ")
quantidade = int(input("Digite a quantidade de cadernos: "))

preco_unitario = 150.0
valor_total = quantidade * preco_unitario

print("\\n--- Resumo da Compra ---")
print("Nome do cliente:", nome)
print("Quantidade de cadernos:", quantidade)
print("Valor total a pagar:", valor_total, "MT")`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios para Resolver',
      exercicios: [
        {
          rotulo: 'Exercício 1 — Estático',
          enunciado: 'Cria um programa que declare dois números inteiros, calcule a sua multiplicação e mostre o resultado no ecrã.',
        },
        {
          rotulo: 'Exercício 2 — Input e output',
          enunciado: 'Cria um programa que peça ao utilizador dois números inteiros e, no final, mostre a diferença entre eles.',
        },
        {
          rotulo: 'Exercício 3 — Input e output',
          enunciado: 'Uma papelaria vende cadernos a um preço fixo de 150 meticais cada. Cria um programa que peça ao utilizador o seu nome e a quantidade de cadernos que pretende comprar, apresentando o nome, a quantidade e o valor total a pagar.',
        },
      ],
    },

    // Este módulo chegou com a sintaxe partida; foi reconstruído
    ciclos: {
      titulo: 'Estruturas de Controlo em Python',
      secoes: [
        {
          titulo: '1. Selecção Simples (if)',
          texto: 'A estrutura de selecção simples permite testar uma condição lógica e executar um bloco de código específico caso o resultado seja verdadeiro.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar se um número é maior do que 10 e se a idade permite entrada num evento.',
              codigo: `num = int(input("Introduza um numero: "))
if num > 10:
    print("O numero e maior que 10.")

idade = int(input("Introduza a idade: "))
if idade >= 18:
    print("Acesso permitido ao evento.")`,
            },
          ],
        },
        {
          titulo: '2. Selecção Dupla (if-else)',
          texto: 'A estrutura de selecção dupla é utilizada quando existem duas alternativas de ação possíveis, escolhendo exatamente um de dois blocos de código consoante a condição seja verdadeira ou falsa.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar paridade de um número e aprovação de um estudante.',
              codigo: `num = int(input("Introduza um numero inteiro: "))
if num % 2 == 0:
    print(f"O numero {num} e par.")
else:
    print(f"O numero {num} e impar.")

nota = int(input("Introduza a nota do estudante: "))
if nota >= 10:
    print("Estudante Aprovado.")
else:
    print("Estudante Reprovado.")`,
            },
          ],
        },
        {
          titulo: '3. Selecção em Alternativa / Encadeada (if-elif-else)',
          texto: 'Permite definir múltiplos caminhos de execução alternativos quando existem mais do que duas condições a testar sequencialmente.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar intervalos de um número e classificar o escalão de uma nota.',
              codigo: `num = int(input("Introduza um numero: "))
if 0 <= num <= 10:
    print("O numero esta entre 0 e 10.")
elif 11 <= num <= 1000:
    print("O numero esta entre 11 e 1000.")
elif num > 1000:
    print("O numero e 1000 para frente.")
else:
    print("Numero negativo.")

nota = int(input("Introduza a nota (0 a 20): "))
if nota >= 16:
    print("Escalao: Excelente")
elif nota >= 14:
    print("Escalao: Bom")
elif nota >= 10:
    print("Escalao: Suficiente")
else:
    print("Escalao: Insuficiente")`,
            },
          ],
        },
        {
          titulo: '4. Selecção Múltipla (match-case)',
          texto: 'A estrutura de seleção múltipla em Python compara o valor de uma expressão contra vários padrões predefinidos, direcionando o fluxo de forma eficiente para o bloco correspondente.',
          exemplos: [
            {
              descricao: 'Exemplos: Operação matemática básica e selecionar o dia da semana.',
              codigo: `op = input("Escolha a operacao (+, -, *, /): ")
a = float(input("Introduza o primeiro valor: "))
b = float(input("Introduza o segundo valor: "))

match op:
    case '+':
        print(f"Resultado: {a + b}")
    case '-':
        print(f"Resultado: {a - b}")
    case '*':
        print(f"Resultado: {a * b}")
    case '/':
        print(f"Resultado: {a / b}")
    case _:
        print("Operacao invalida.")

opcao = int(input("Introduza uma opcao (1 a 3): "))
match opcao:
    case 1:
        print("Segunda-feira")
    case 2:
        print("Terca-feira")
    case 3:
        print("Quarta-feira")
    case _:
        print("Opcao invalida.")`,
            },
          ],
        },
        {
          titulo: '5. Ciclo While (while)',
          texto: 'Permite repetir a execução de um bloco de instruções enquanto uma determinada condição lógica se mantiver verdadeira.',
          exemplos: [
            {
              descricao: 'Exemplos: Ciclo que termina com 0 e contagem progressiva de 1 até 5.',
              codigo: `num = 1
while num != 0:
    num = int(input("Introduza um numero (pressione 0 para sair): "))
    print(f"Voce introduziu: {num}")
print("Ciclo terminado.")

contador = 1
while contador <= 5:
    print(f"Contador: {contador}")
    contador += 1`,
            },
          ],
        },
        {
          titulo: '6. Ciclo For (for)',
          texto: 'Utilizado em Python para percorrer iterativamente sequências de elementos (como intervalos numéricos gerados pela função range), repetindo blocos de código um número exato de vezes.',
          exemplos: [
            {
              descricao: 'Exemplos: Contagem decrescente e exibição de múltiplos (tabuada até 5).',
              codigo: `n = int(input("Introduza um numero para contagem inversa: "))
for i in range(n, -1, -1):
    print(i)

n = int(input("Introduza um numero para ver a tabuada (ate 5): "))
for i in range(1, 6):
    print(f"{n} x {i} = {n * i}")`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          rotulo: 'Exercício 1',
          enunciado: 'Faça um programa que calcule a potência, sendo os dados de entrada (base e expoente) introduzidos pelo usuário.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Elabore um programa que pede os lados de um triângulo e informa se o triângulo é equilátero, isósceles ou escaleno.',
        },
        {
          rotulo: 'Exercício 11',
          enunciado: 'Faça um programa que visualiza os números múltiplos de 5 entre 50 e 100.',
        },
      ],
    },

    vetores: {
      titulo: 'Vetores em Python',
      nota: 'Nota: Vetores são o mesmo que Arrays.',
      secoes: [
        {
          titulo: '1. Array Unidimensional (Vetor / Lista)',
          texto: 'Em Python, um array unidimensional é habitualmente representado por uma lista, consistindo numa estrutura de dados que armazena uma sequência linear de elementos, permitindo aceder de forma rápida a qualquer valor através de índices numéricos que começam em zero.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Alocação e preenchimento dinâmico de uma lista com notas inteiras introduzidas pelo utilizador.',
              codigo: `quant = int(input("Introduza o número de notas a armazenar: "))
notas = []

for i in range(quant):
    nota = int(input(f"Introduza a nota {i + 1}: "))
    notas.append(nota)

print("Notas armazenadas com sucesso:", notas)`,
            },
            {
              descricao: 'Exemplo 2: Inicialização direta de um vetor com valores de temperaturas do tipo float.',
              codigo: `temperaturas = [25.5, 26.0, 24.2, 28.1, 30.0]

print("Temperaturas registadas:")
for i in range(len(temperaturas)):
    print(f"Posição {i}: {temperaturas[i]} graus")`,
            },
          ],
        },
        {
          titulo: '2. Array Bidimensional (Matriz / Lista de Listas)',
          texto: 'Um array bidimensional, designado por matriz, é estruturado em Python sob a forma de uma lista de listas, organizando os dados de forma tabular em linhas e colunas, onde cada elemento requer dois índices para o seu acesso específico.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Criação e preenchimento de uma matriz de preços (float) com 3 linhas e 2 colunas.',
              codigo: `# Criação de uma matriz 3x2 preenchida inicialmente com zeros
precos = [[0.0, 0.0], [0.0, 0.0], [0.0, 0.0]]

for i in range(len(precos)):
    for j in range(len(precos[0])):
        precos[i][j] = float(input(f"Introduza o preço para a posição [{i}][{j}]: "))

print("Matriz de preços preenchida com sucesso.")`,
            },
            {
              descricao: 'Exemplo 2: Inicialização direta de uma matriz de idades (int) com 3 linhas e 2 colunas.',
              codigo: `idade = [[12, 30], [3, 7], [70, 26]]

print("Conteúdo da matriz de idades:")
for i in range(len(idade)):
    for j in range(len(idade[0])):
        print(idade[i][j], end=" ")
    print()`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          grupo: 'Arrays Unidimensionais:',
          rotulo: 'Exercício 1',
          enunciado: 'Armazenar quaisquer valores num array de N elementos, determinar a quantidade de números negativos existentes e visualizar os elementos que ocupam as primeiras 3 posições.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Receber várias idades do teclado e visualizá-las em ordem crescente.',
        },
        {
          grupo: 'Arrays Bidimensionais:',
          rotulo: 'Exercício 3',
          enunciado: 'Preencher um array bidimensional de 3 linhas e 2 colunas com valores e visualizar o conteúdo do array no ecrã na forma de tabela.',
        },
        {
          rotulo: 'Exercício 4',
          enunciado: 'Validar o número de uma coluna escolhida pelo utilizador e calcular a soma de elementos que se encontram nessa coluna.',
        },
      ],
    },
  },

  // ------------------------------------------------------
  // ASSEMBLY
  // ------------------------------------------------------
  assembly: {
    io: {
      titulo: 'Capítulo Prático: Exercícios de Assembly',
      secoes: [
        {
          titulo: 'Exemplos Práticos Resolvidos',
          exemplos: [
            {
              titulo: 'Exemplo 1 — Estático',
              texto: 'Programa em Assembly que declara dois números, calcula a sua multiplicação e mostra o resultado no ecrã.',
              codigo: `section .data
    num1 dd 5
    num2 dd 4
    mensagem db "A multiplicacao e: ", 0
    tamanho equ $ - mensagem

section .bss
    resultado resd 1

section .text
    global _start

_start:
    mov eax, [num1]
    imul eax, [num2]
    mov [resultado], eax

    ; Terminar o programa
    mov eax, 1
    xor ebx, ebx
    int 0x80`,
              nota: 'Nota: este primeiro exemplo calcula a multiplicação, mas ainda não apresenta o resultado no ecrã.',
            },
            {
              titulo: 'Exemplo 2 — Input e output',
              texto: 'Programa em Assembly que lê dois números introduzidos pelo utilizador e calcula a sua diferença.',
              codigo: `section .data
    mensagem1 db "Digite o primeiro numero: "
    tamanho1 equ $ - mensagem1

    mensagem2 db "Digite o segundo numero: "
    tamanho2 equ $ - mensagem2

section .bss
    n1 resb 2
    n2 resb 2

section .text
    global _start

_start:
    ; Mostrar primeira mensagem
    mov eax, 4
    mov ebx, 1
    mov ecx, mensagem1
    mov edx, tamanho1
    int 0x80

    ; Ler primeiro numero
    mov eax, 3
    mov ebx, 0
    mov ecx, n1
    mov edx, 2
    int 0x80

    ; Mostrar segunda mensagem
    mov eax, 4
    mov ebx, 1
    mov ecx, mensagem2
    mov edx, tamanho2
    int 0x80

    ; Ler segundo numero
    mov eax, 3
    mov ebx, 0
    mov ecx, n2
    mov edx, 2
    int 0x80

    ; Terminar o programa
    mov eax, 1
    xor ebx, ebx
    int 0x80`,
              nota: 'Nota: este exemplo lê os dois números, mas ainda não converte os caracteres em valores numéricos nem calcula ou apresenta a diferença.',
            },
            {
              titulo: 'Exemplo 3 — Input e output (Papelaria)',
              texto: 'Uma papelaria vende cadernos a 150 meticais cada. Programa que lê a quantidade de cadernos e calcula o valor total a pagar.',
              codigo: `section .data
    preco dd 150

section .bss
    quantidade resd 1
    total resd 1

section .text
    global _start

_start:
    ; Definir a quantidade de cadernos
    mov eax, 3
    mov ebx, 4
    ; A multiplicacao sera feita abaixo

    mov eax, [preco]
    mov ebx, 3
    imul eax, ebx
    mov [total], eax

    ; Terminar o programa
    mov eax, 1
    xor ebx, ebx
    int 0x80`,
              nota: 'Nota: este exemplo calcula o preço de três cadernos. A leitura pelo teclado e a apresentação do total ainda precisam de ser implementadas.',
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios para Resolver',
      exercicios: [
        {
          rotulo: 'Exercício 1 — Estático',
          enunciado: 'Cria um programa em Assembly que declare dois números, calcule a sua multiplicação e mostre o resultado no ecrã.',
        },
        {
          rotulo: 'Exercício 2 — Input e output',
          enunciado: 'Cria um programa em Assembly que leia dois números introduzidos pelo utilizador e calcule a sua diferença.',
        },
        {
          rotulo: 'Exercício 3 — Input e output',
          enunciado: 'Uma papelaria vende cadernos a 150 meticais cada. Cria um programa que leia a quantidade de cadernos e calcule o valor total a pagar.',
        },
      ],
    },

    ciclos: {
      titulo: 'Estruturas de Controlo em Assembly',
      secoes: [
        {
          titulo: '1. Selecção Simples (if via cmp e Saltos)',
          texto: 'Em Assembly, a seleção simples é implementada comparando valores através da instrução cmp e utilizando um salto condicional (como jle ou jne) para ignorar o bloco de código caso a condição seja falsa.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar se um número é maior do que 10 e se a idade permite entrada num evento.',
              codigo: `; Exemplo 1: Verificar se num > 10
org 100h

section .data
    num dw 15
    msg_maior db 'Numero maior que 10$', 0

section .text
start:
    mov ax, [num]
    cmp ax, 10
    jle fim_if          ; Se num <= 10, salta o bloco
    
    mov ah, 09h
    mov dx, msg_maior
    int 21h

fim_if:
    mov ax, 4C00h
    int 21h

; Exemplo 2: Verificar se idade >= 18
org 100h

section .data
    idade dw 20
    msg_acesso db 'Acesso permitido$', 0

section .text
start:
    mov ax, [idade]
    cmp ax, 18
    jl fim_if2          ; Se idade < 18, salta o bloco
    
    mov ah, 09h
    mov dx, msg_acesso
    int 21h

fim_if2:
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '2. Selecção Dupla (if-else com Saltos)',
          texto: 'A seleção dupla utiliza saltos condicionais combinados com um salto incondicional (jmp) para garantir que apenas um dos dois blocos alternativos seja executado.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar paridade de um número e aprovação de um estudante.',
              codigo: `; Exemplo 1: Par ou Ímpar
org 100h

section .data
    num dw 4
    msg_par db 'O numero e par$', 0
    msg_impar db 'O numero e impar$', 0

section .text
start:
    mov ax, [num]
    test ax, 1          ; Testa o bit menos significativo
    jnz eh_impar        ; Se diferente de zero, e impar
    
    mov ah, 09h
    mov dx, msg_par
    int 21h
    jmp fim

eh_impar:
    mov ah, 09h
    mov dx, msg_impar
    int 21h

fim:
    mov ax, 4C00h
    int 21h

; Exemplo 2: Aprovação (nota >= 10)
org 100h

section .data
    nota dw 12
    msg_aprov db 'Aprovado$', 0
    msg_reprov db 'Reprovado$', 0

section .text
start:
    mov ax, [nota]
    cmp ax, 10
    jl reprovado        ; Se nota < 10, salta para reprovado
    
    mov ah, 09h
    mov dx, msg_aprov
    int 21h
    jmp fim_processo

reprovado:
    mov ah, 09h
    mov dx, msg_reprov
    int 21h

fim_processo:
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '3. Selecção em Alternativa / Encadeada (if-else-if)',
          texto: 'Implementada através de testes condicionais encadeados em sequência, avaliando múltiplas condições e desviando o fluxo para blocos específicos.',
          exemplos: [
            {
              descricao: 'Exemplos: Verificar intervalos de um número e classificar o escalão de uma nota.',
              codigo: `; Exemplo 1: Intervalos de um número
org 100h

section .data
    num dw 500
    m1 db 'Entre 0 e 10$', 0
    m2 db 'Entre 11 e 1000$', 0
    m3 db '1000 para frente$', 0

section .text
start:
    mov ax, [num]
    cmp ax, 0
    jl fim
    cmp ax, 10
    jle faixa1
    
    cmp ax, 1000
    jle faixa2
    
    mov dx, m3
    jmp mostra

faixa1:
    mov dx, m1
    jmp mostra

faixa2:
    mov dx, m2

mostra:
    mov ah, 09h
    int 21h

fim:
    mov ax, 4C00h
    int 21h

; Exemplo 2: Escalão de nota
org 100h

section .data
    nota_val dw 15
    exc db 'Excelente$', 0
    bom db 'Bom$', 0
    suf db 'Suficiente$', 0

section .text
start:
    mov ax, [nota_val]
    cmp ax, 16
    jge e_excelente
    cmp ax, 14
    jge e_bom
    
    mov dx, suf
    jmp exibir

e_excelente:
    mov dx, exc
    jmp exibir

e_bom:
    mov dx, bom

exibir:
    mov ah, 09h
    int 21h
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '4. Selecção Múltipla (switch via Comparações Múltiplas)',
          texto: 'Em Assembly, a seleção múltipla é comummente estruturada através de sucessivas comparações (cmp) associadas a saltos condicionais correspondentes a cada opção.',
          exemplos: [
            {
              descricao: 'Exemplos: Selecionar operação aritmética e selecionar dia da semana.',
              codigo: `; Exemplo 1: Operações aritméticas
org 100h

section .data
    opcao db 2
    msg_soma db 'Operacao Soma$', 0
    msg_sub db 'Operacao Subtracao$', 0
    msg_mult db 'Operacao Multiplicacao$', 0

section .text
start:
    mov al, [opcao]
    cmp al, 1
    je op_soma
    cmp al, 2
    je op_sub
    cmp al, 3
    je op_mult
    jmp fim_switch

op_soma:
    mov dx, msg_soma
    jmp print_msg
op_sub:
    mov dx, msg_sub
    jmp print_msg
op_mult:
    mov dx, msg_mult

print_msg:
    mov ah, 09h
    int 21h

fim_switch:
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '5. Ciclo While (while em Assembly)',
          texto: 'O ciclo while avalia a condição no início de cada iteração, saltando para fora do ciclo caso a condição deixe de ser verdadeira.',
          exemplos: [
            {
              descricao: 'Exemplos: Ciclo com contador e acumulação de valores.',
              codigo: `; Exemplo 1: Decrementar até zero
org 100h

section .data
    contador dw 5

section .text
start:
inicio_while:
    mov ax, [contador]
    cmp ax, 0
    je fim_while
    
    dec word [contador]
    jmp inicio_while

fim_while:
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '6. Ciclo Do-While (do-while em Assembly)',
          texto: 'O ciclo do-while executa o bloco de código primeiro e avalia a condição de salto no final, garantindo pelo menos uma execução inicial.',
          exemplos: [
            {
              descricao: 'Exemplos: Repetir incremento até valor 3 e simulação de validação.',
              codigo: `; Exemplo 1: Incrementar até val = 3
org 100h

section .data
    val dw 0

section .text
start:
do_loop:
    inc word [val]
    
    mov ax, [val]
    cmp ax, 3
    jl do_loop

    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '7. Ciclo For (for em Assembly)',
          texto: 'Utiliza um registo contador ou variável de controlo associada a instruções de incremento e comparação para gerir um número exato de repetições.',
          exemplos: [
            {
              descricao: 'Exemplos: Contagem decrescente com jcxz e soma com registadores.',
              codigo: `; Exemplo 1: Contagem decrescente
org 100h

section .text
start:
    mov cx, 5

l_for:
    jcxz fim_for
    dec cx
    jmp l_for

fim_for:
    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          rotulo: 'Exercício 6',
          enunciado: 'Faça um programa que calcule a potência, sendo os dados de entrada (base e expoente) introduzidos pelo usuário.',
        },
        {
          rotulo: 'Exercício 7',
          enunciado: 'Elabore um programa que pede os lados de um triângulo e informa se o triângulo é equilátero, isósceles ou escaleno.',
        },
        {
          rotulo: 'Exercício 11',
          enunciado: 'Faça um programa que visualiza os números múltiplos de 5 entre 50 e 100.',
        },
      ],
    },

    vetores: {
      titulo: 'Vetores e Matrizes em Assembly',
      secoes: [
        {
          titulo: '1. Array Unidimensional (Vetor)',
          texto: 'Um array unidimensional, comummente conhecido como vetor, é uma estrutura de dados homogénea que armazena uma lista linear de elementos do mesmo tipo em posições consecutivas de memória, permitindo o acesso rápido aos valores através de um único índice numérico que começa em zero.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Declaração e percurso de um vetor de 5 elementos inteiros em Assembly para somar os seus valores.',
              codigo: `org 100h

section .data
    vetor dw 10, 20, 30, 40, 50

section .text
start:
    mov cx, 5           ; Número de elementos
    mov si, 0           ; Índice inicial em bytes
    mov ax, 0           ; Acumulador para a soma

soma_loop:
    add ax, [vetor + si]
    add si, 2           ; Avança para o próximo elemento (2 bytes por palavra)
    dec cx
    jnz soma_loop

    mov ax, 4C00h
    int 21h`,
            },
            {
              descricao: 'Exemplo 2: Acesso direto a um elemento específico de um vetor de carateres através de um índice fixo.',
              codigo: `org 100h

section .data
    notas db 14, 12, 16, 18

section .text
start:
    mov bx, notas
    mov al, [bx + 2]    ; Acede ao 3.º elemento do vetor (índice 2)

    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
        {
          titulo: '2. Array Bidimensional (Matriz)',
          texto: 'Um array bidimensional, designado por matriz, consiste numa estrutura em que cada elemento do array principal é, por sua vez, outro array, organizando os dados de forma tabular em linhas e colunas, exigindo dois índices (linha e coluna) para o seu endereçamento específico.',
          exemplos: [
            {
              descricao: 'Exemplo 1: Declaração de uma matriz 2x2 de valores inteiros e cálculo do desvio de memória para aceder a uma posição específica.',
              codigo: `org 100h

section .data
    ; Matriz 2x2: [[1, 2], [3, 4]]
    matriz dw 1, 2
           dw 3, 4

section .text
start:
    ; Aceder a matriz[1][0] (linha 1, coluna 0)
    mov si, 1           ; Linha 1
    imul si, 4          ; Linha * (2 colunas * 2 bytes por elemento)
    mov di, 0           ; Coluna 0
    shl di, 1           ; Coluna * 2 bytes
    mov ax, [matriz + si + di]

    mov ax, 4C00h
    int 21h`,
            },
            {
              descricao: 'Exemplo 2: Acesso a uma matriz de bytes 2x3 utilizando a fórmula de deslocamento linear (linha * num_colunas + coluna).',
              codigo: `org 100h

section .data
    tabela db 5, 10, 15
           db 20, 25, 30

section .text
start:
    ; Aceder a tabela[0][2] (linha 0, coluna 2) numa matriz com 3 colunas
    mov bx, tabela
    mov al, [bx + 2]    ; 0 * 3 + 2 = 2

    mov ax, 4C00h
    int 21h`,
            },
          ],
        },
      ],
      tituloExercicios: 'Exercícios Finais da Ficha',
      exercicios: [
        {
          grupo: 'Arrays Unidimensionais:',
          rotulo: 'Exercício 1',
          enunciado: 'Armazenar quaisquer valores num array de N elementos, determinar e contabilizar a quantidade de números negativos existentes.',
        },
        {
          rotulo: 'Exercício 2',
          enunciado: 'Receber várias idades do teclado e visualizá-las ordenadas por ordem crescente.',
        },
        {
          grupo: 'Arrays Bidimensionais:',
          rotulo: 'Exercício 3',
          enunciado: 'Preencher um array bidimensional de 3x2 posições com valores gerados e visualizar o conteúdo completo no ecrã sob a forma de tabela.',
        },
        {
          rotulo: 'Exercício 4',
          enunciado: 'Validar o número de uma coluna escolhida pelo utilizador e calcular a soma aritmética de todos os elementos que se encontram estritamente nessa coluna.',
        },
      ],
    },
  },
};

// ==========================================================
// --- PONTOS, NÍVEIS E MEDALHAS (a parte "jogo" do site) ---
// Cada exercício vale até 100 pontos (conforme a nota do corretor).
// Só conta o MELHOR resultado de cada exercício (não dá para "enganar" repetindo).
// ==========================================================
const CHAVE_PROGRESSO = 'aprencode_progresso_v1';
const PONTOS_POR_NIVEL = 150;
const TITULOS_NIVEL = ['Curioso', 'Aprendiz', 'Programador', 'Mestre do Código', 'Lenda'];

const MEDALHAS = [
  { id: 'primeiro', icone: '🚀', nome: 'Primeiro Passo', descricao: 'Submete o teu primeiro exercício' },
  { id: 'perfeito', icone: '🎯', nome: 'Pontaria', descricao: 'Faz um exercício sem nenhum erro' },
  { id: 'cinco', icone: '🔥', nome: 'Em Chamas', descricao: 'Submete 5 exercícios diferentes' },
  { id: 'duas', icone: '🌍', nome: 'Explorador', descricao: 'Pratica em 2 linguagens diferentes' },
  { id: 'modulo', icone: '🏆', nome: 'Módulo Completo', descricao: 'Submete todos os exercícios de um módulo' },
  { id: 'nivel3', icone: '⭐', nome: 'Estrela', descricao: 'Chega ao nível 3' },
];

function carregarProgresso() {
  try {
    const guardado = window.localStorage.getItem(CHAVE_PROGRESSO);
    if (guardado) {
      const p = JSON.parse(guardado);
      if (p && p.exercicios && Array.isArray(p.medalhas)) return p;
    }
  } catch (e) {
    // sem armazenamento: o progresso fica só enquanto a página estiver aberta
  }
  return { exercicios: {}, medalhas: [] };
}

function totalPontos(exercicios) {
  return Object.keys(exercicios).reduce((soma, id) => soma + exercicios[id], 0);
}

function calcularNivel(pontos) {
  const nivel = Math.floor(pontos / PONTOS_POR_NIVEL) + 1;
  const dentro = pontos % PONTOS_POR_NIVEL;
  return {
    nivel,
    titulo: TITULOS_NIVEL[Math.min(nivel - 1, TITULOS_NIVEL.length - 1)],
    percentagem: Math.round((dentro / PONTOS_POR_NIVEL) * 100),
    falta: PONTOS_POR_NIVEL - dentro,
  };
}

function medalhasMerecidas(exercicios) {
  const ids = Object.keys(exercicios);
  const merecidas = [];
  if (ids.length >= 1) merecidas.push('primeiro');
  if (ids.some((id) => exercicios[id] >= 100)) merecidas.push('perfeito');
  if (ids.length >= 5) merecidas.push('cinco');

  const linguagensUsadas = {};
  ids.forEach((id) => { linguagensUsadas[id.split('_')[0]] = true; });
  if (Object.keys(linguagensUsadas).length >= 2) merecidas.push('duas');

  const moduloCompleto = Object.keys(conteudoPratico).some((lang) =>
    Object.keys(conteudoPratico[lang]).some((mod) => {
      const lista = conteudoPratico[lang][mod].exercicios || [];
      return lista.length > 0 && lista.every((_, i) => exercicios[`${lang}_${mod}_${i}`] !== undefined);
    })
  );
  if (moduloCompleto) merecidas.push('modulo');

  if (calcularNivel(totalPontos(exercicios)).nivel >= 3) merecidas.push('nivel3');
  return merecidas;
}

function PainelProgresso({ progresso, escuro, aberto, aoAlternar, aoReiniciar }) {
  const total = totalPontos(progresso.exercicios);
  const n = calcularNivel(total);
  const borda = escuro ? 'rgba(255,255,255,0.15)' : 'rgba(0,0,0,0.12)';

  return (
    <div
      style={{
        width: '100%',
        boxSizing: 'border-box',
        marginBottom: '15px',
        padding: '12px 14px',
        borderRadius: '14px',
        background: escuro ? 'rgba(255,255,255,0.06)' : 'rgba(255,255,255,0.75)',
        border: `1px solid ${borda}`,
        fontFamily: 'Arial, sans-serif',
      }}
    >
      <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'center', gap: '8px' }}>
        <span style={{ fontWeight: 'bold', fontSize: '11pt' }}>⭐ Nível {n.nivel} · {n.titulo}</span>
        <span style={{ fontWeight: 'bold', fontSize: '11pt', color: escuro ? '#facc15' : '#b45309' }}>{total} pts</span>
      </div>

      <div style={{ height: '10px', borderRadius: '10px', background: escuro ? 'rgba(255,255,255,0.15)' : 'rgba(0,0,0,0.12)', margin: '10px 0 6px', overflow: 'hidden' }}>
        <div
          style={{
            width: `${n.percentagem}%`,
            height: '100%',
            borderRadius: '10px',
            background: 'linear-gradient(90deg, #f472b6, #facc15)',
            transition: 'width 0.8s ease',
          }}
        />
      </div>
      <div style={{ fontSize: '9pt', opacity: 0.8 }}>Faltam {n.falta} pts para o nível {n.nivel + 1}</div>

      <button
        onClick={aoAlternar}
        style={{
          marginTop: '10px',
          padding: '6px 12px',
          borderRadius: '20px',
          border: `1px solid ${borda}`,
          background: 'transparent',
          color: 'inherit',
          cursor: 'pointer',
          fontWeight: 'bold',
          fontSize: '9pt',
          fontFamily: 'inherit',
        }}
      >
        🏅 Medalhas ({progresso.medalhas.length}/{MEDALHAS.length}) {aberto ? '▲' : '▼'}
      </button>

      {aberto && (
        <div style={{ marginTop: '12px' }}>
          <div style={{ display: 'grid', gridTemplateColumns: 'repeat(auto-fill, minmax(130px, 1fr))', gap: '8px' }}>
            {MEDALHAS.map((m) => {
              const ganha = progresso.medalhas.includes(m.id);
              return (
                <div
                  key={m.id}
                  style={{
                    padding: '10px',
                    borderRadius: '10px',
                    textAlign: 'center',
                    border: ganha ? '1px solid #facc15' : `1px dashed ${borda}`,
                    background: ganha ? 'rgba(250, 204, 21, 0.15)' : 'transparent',
                    boxShadow: ganha ? '0 0 12px rgba(250, 204, 21, 0.35)' : 'none',
                    opacity: ganha ? 1 : 0.5,
                    filter: ganha ? 'none' : 'grayscale(1)',
                  }}
                >
                  <div style={{ fontSize: '22pt' }}>{ganha ? m.icone : '🔒'}</div>
                  <div style={{ fontWeight: 'bold', fontSize: '9pt' }}>{m.nome}</div>
                  <div style={{ fontSize: '8pt', opacity: 0.85 }}>{m.descricao}</div>
                </div>
              );
            })}
          </div>
          <button
            onClick={aoReiniciar}
            style={{ marginTop: '10px', background: 'transparent', border: 'none', color: 'inherit', opacity: 0.6, cursor: 'pointer', fontSize: '8pt', textDecoration: 'underline', fontFamily: 'inherit', padding: 0 }}
          >
            Recomeçar progresso
          </button>
        </div>
      )}
    </div>
  );
}

export default function App() {
  const [isDarkMode, setIsDarkMode] = useState(true);
  const [linguagemSelecionada, setLinguagemSelecionada] = useState(null);
  const [paginaAtiva, setPaginaAtiva] = useState('menu');

  // Código que o utilizador escreve nos exercícios (guardado aqui para não se perder ao navegar)
  const [respostas, setRespostas] = useState({});
  const mudarResposta = (id, valor) => {
    setRespostas((anterior) => ({ ...anterior, [id]: valor }));
  };

  // Pontos, níveis e medalhas
  const [progresso, setProgresso] = useState(carregarProgresso);
  const [painelAberto, setPainelAberto] = useState(false);
  const [aviso, setAviso] = useState(null);

  // Guarda o progresso no aparelho (se não for possível, continua a funcionar)
  useEffect(() => {
    try {
      window.localStorage.setItem(CHAVE_PROGRESSO, JSON.stringify(progresso));
    } catch (e) {
      // ignora
    }
  }, [progresso]);

  // O aviso desaparece sozinho ao fim de 4 segundos
  useEffect(() => {
    if (!aviso) return undefined;
    const temporizador = setTimeout(() => setAviso(null), 4000);
    return () => clearTimeout(temporizador);
  }, [aviso]);

  // Chamado sempre que um exercício é corrigido
  const registarResultado = (id, res) => {
    if (!res || !res.erros) return; // vazio ou fora de tema: não conta
    const pontos = Math.max(0, Math.min(100, Math.round((res.nota / res.cotacao) * 100)));
    const antes = progresso.exercicios[id] || 0;
    const melhor = Math.max(antes, pontos);
    const ganhos = melhor - antes;
    const exercicios = { ...progresso.exercicios, [id]: melhor };

    const novas = medalhasMerecidas(exercicios).filter((m) => !progresso.medalhas.includes(m));
    const nivelAntes = calcularNivel(totalPontos(progresso.exercicios)).nivel;
    const nivelDepois = calcularNivel(totalPontos(exercicios)).nivel;

    const linhas = [];
    if (ganhos > 0) linhas.push(`+${ganhos} pontos ✨`);
    else linhas.push(`Sem pontos novos (o teu melhor neste exercício: ${melhor}/100)`);
    novas.forEach((m) => {
      const med = MEDALHAS.find((x) => x.id === m);
      linhas.push(`${med.icone} Nova medalha: ${med.nome}!`);
    });
    if (nivelDepois > nivelAntes) linhas.push(`🎉 Subiste para o nível ${nivelDepois}!`);

    setProgresso({ exercicios, medalhas: [...progresso.medalhas, ...novas] });
    setAviso({ linhas, chave: Date.now() });
  };

  const reiniciarProgresso = () => {
    if (window.confirm('Queres mesmo apagar os teus pontos e medalhas?')) {
      setProgresso({ exercicios: {}, medalhas: [] });
    }
  };

  const currentTheme = {
    background: isDarkMode 
      ? 'linear-gradient(135deg, #1a0b2e 0%, #000000 50%, #153e75 100%)' 
      : 'linear-gradient(135deg, #d4f0fc 0%, #fef3c7 100%)',
    textColor: isDarkMode ? '#ffffff' : '#1f2937',
    cardBg: isDarkMode ? 'rgba(255, 255, 255, 0.05)' : 'rgba(255, 255, 255, 0.7)',
    cardBorder: isDarkMode ? 'rgba(255, 255, 255, 0.1)' : 'rgba(0, 0, 0, 0.1)',
  };

  const temasHistorial = {
    cpp: {
      background: 'linear-gradient(180deg, #000000df, #367cdd)',
      fontFamily: "'Courier New', Courier, monospace",
      color: '#ffffff',
      titleColor: '#3b82f6',
      logo: 'https://thumb.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1920px-ISO_C%2B%2B_Logo.svg.png',
      footerText: 'A sua jornada pelo C++ está a começar'
    },
    python: {
      background: 'linear-gradient(135deg, rgba(39, 48, 102, 0.74), rgba(222, 222, 51, 0.55))',
      fontFamily: 'Arial, sans-serif',
      color: '#ffffff',
      titleColor: '#facc15',
      logo: 'https://upload.wikimedia.org/wikipedia/commons/3/31/Python-logo.png',
      footerText: 'A história do Python'
    },
    java: {
      background: 'linear-gradient(155deg, #d37d7d, #ffffff, rgba(0, 150, 255, 0.55))',
      fontFamily: 'Arial, sans-serif',
      color: '#333333',
      titleColor: '#1e3a8a',
      logo: 'https://www.svgrepo.com/show/303388/java-4-logo.svg',
      footerText: 'A história do Java'
    },
    assembly: {
      background: 'linear-gradient(180deg, rgba(0, 0, 0, 0.87), #0f8a4a)',
      fontFamily: "'Courier New', Courier, monospace",
      color: '#ffffff',
      titleColor: '#2ee27a',
      logo: 'https://cdn.dribbble.com/userupload/37125886/file/original-6117f521b03664c7331283c90e82075a.png',
      footerText: 'A sua jornada pelo Assembly está a começar'
    }
  };

  const appStyles = {
    container: {
      background: (paginaAtiva === 'historial' && linguagemSelecionada) 
        ? temasHistorial[linguagemSelecionada].background 
        : currentTheme.background,
      minHeight: '100vh',
      color: currentTheme.textColor,
      fontFamily: "'Courier New', Courier, monospace",
      padding: '15px',
      display: 'flex',
      flexDirection: 'column',
      justifyContent: 'space-between',
      boxSizing: 'border-box',
      transition: 'all 0.5s ease',
    },
    header: {
      display: 'flex',
      justifyContent: 'space-between',
      alignItems: 'center',
      marginBottom: '20px',
      width: '100%',
    },
    brand: {
      fontFamily: 'Arial, sans-serif',
      fontSize: '14pt',
      fontWeight: 'bold',
      display: 'inline-block',
      // Gradientes adaptados e vibrantes para cada tema (nunca ficam invisíveis)
      backgroundImage: isDarkMode 
        ? 'linear-gradient(135deg, #f472b6 0%, #38bdf8 100%)' // Rosa claro e Azul ciano (destaca-se no escuro)
        : 'linear-gradient(135deg, #0284c7 0%, #7c3aed 100%)', // Azul forte e Roxo (destaca-se no claro)
      WebkitBackgroundClip: 'text',
      backgroundClip: 'text',
      WebkitTextFillColor: 'transparent',
      color: isDarkMode ? '#f472b6' : '#0284c7', // Fallback seguro
    },
    themeButton: {
      padding: '6px 12px',
      borderRadius: '20px',
      border: 'none',
      background: isDarkMode ? '#ff7e5f' : '#367cdd',
      color: '#fff',
      cursor: 'pointer',
      fontWeight: 'bold',
      fontSize: '9pt',
      fontFamily: 'inherit',
      boxShadow: '0 4px 15px rgba(0,0,0,0.2)',
    },
    content: {
      flex: 1,
      display: 'flex',
      flexDirection: 'column',
      alignItems: 'center',
      justifyContent: 'center',
      textAlign: 'center',
      width: '100%',
      maxWidth: '500px',
      margin: '0 auto',
    },
    title: {
      fontFamily: 'Arial, sans-serif',
      fontSize: '20pt',
      marginBottom: '10px',
      fontWeight: 'bold',
      color: currentTheme.textColor,
    },
    subtitle: {
      fontSize: '10pt',
      marginBottom: '30px',
      opacity: 0.8,
    },
    blockContainer: {
      display: 'flex',
      flexDirection: 'column',
      gap: '12px',
      width: '100%',
    },
    langButton: {
      display: 'flex',
      justifyContent: 'space-between',
      alignItems: 'center',
      padding: '15px 20px',
      fontSize: '13pt',
      fontWeight: 'bold',
      fontFamily: 'Arial, sans-serif',
      color: currentTheme.textColor,
      background: currentTheme.cardBg,
      border: `2px solid ${currentTheme.cardBorder}`,
      borderRadius: '12px',
      cursor: 'pointer',
      backdropFilter: 'blur(10px)',
      boxShadow: '0 8px 32px 0 rgba(0, 0, 0, 0.2)',
      width: '100%',
      transition: 'transform 0.2s ease',
    },
    animatedButton: {
      padding: '15px 20px',
      fontSize: '12pt',
      fontWeight: 'bold',
      fontFamily: 'Arial, sans-serif',
      color: currentTheme.textColor,
      background: currentTheme.cardBg,
      border: `2px solid ${currentTheme.cardBorder}`,
      borderRadius: '12px',
      cursor: 'pointer',
      backdropFilter: 'blur(10px)',
      boxShadow: '0 8px 32px 0 rgba(0, 0, 0, 0.2)',
      width: '100%',
      textAlign: 'left',
      transition: 'transform 0.2s ease',
    },
    buttonLogo: {
      width: '28px',
      height: '28px',
      objectFit: 'contain',
    },
    backButton: {
      marginBottom: '20px',
      padding: '6px 14px',
      borderRadius: '8px',
      border: 'none',
      background: '#ef4444',
      color: '#fff',
      cursor: 'pointer',
      fontWeight: 'bold',
      fontSize: '10pt',
      alignSelf: 'flex-start',
    },
    textCard: {
      background: currentTheme.cardBg,
      border: `1px solid ${currentTheme.cardBorder}`,
      padding: '20px',
      borderRadius: '12px',
      textAlign: 'left',
      lineHeight: '1.5',
      fontSize: '11pt',
      backdropFilter: 'blur(10px)',
      width: '100%',
    }
  };

  const linguagens = [
    { id: 'java', nome: 'JAVA', logo: 'https://www.svgrepo.com/show/303388/java-4-logo.svg' },
    { id: 'cpp', nome: 'C++', logo: 'https://thumb.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1920px-ISO_C%2B%2B_Logo.svg.png' },
    { id: 'python', nome: 'PYTHON', logo: 'https://upload.wikimedia.org/wikipedia/commons/3/31/Python-logo.png' },
    { id: 'assembly', nome: 'ASSEMBLY', logo: 'https://cdn.dribbble.com/userupload/37125886/file/original-6117f521b03664c7331283c90e82075a.png' }
  ];

  const historiais = {
    cpp: (
      <span>
        C++ é a linguagem de programação criada por Bjarne Stroustrup em 1979. 
        Foi originalmente criada com o nome "C com classes", uma vez que seria uma evolução da linguagem de programação C. 
        Até que em 1983 resolveu-se trocar o nome da linguagem uma vez que já não poderia mais ser considerada apenas uma extensão de linguagem C, 
        então designou-se C++ por ser uma linguagem de programação diferente!
      </span>
    ),
    python: (
      <span>
        Python é uma linguagem de programação interpretada de alto nível, conhecida por sua simplicidade, legibilidade e versatilidade. 
        Ela é usada em todos os lugares – desde aplicativos web e ferramentas de automação até ciência de dados e inteligência artificial. 
        Seja para assistir a um programa em streaming, reservar um voo ou conversar com uma IA, é provável que o Python esteja trabalhando nos bastidores. 
        Python foi criado por Guido van Rossum e lançado pela primeira vez em 20 de fevereiro de 1991. Embora a palavra "python" possa remeter à imagem de uma grande cobra, 
        o nome da linguagem na verdade vem da clássica série de comédia da BBC, Monty Python's Flying Circus.
        <br /><br />
        O que torna o Python único é que ele começou como a visão e o trabalho de uma única pessoa.
      </span>
    ),
    java: (
      <span>
        A linguagem de programação Java foi criada nos anos 90 por uma equipe de programadores
        chefiada por James Gosling, na empresa Sun Microsystems
        com o objectivo de criar uma nova linguagem de programação que pudesse ser
        executada em qualquer tipo de computador.
        Foi concebida como um computador virtual capaz de executar um
        código constituído por instruções simples. Este código é
        chamado de bytecode, pois é usado 1 byte para representar
        cada instrução.
      </span>
    ),
    assembly: (
      <span>
        Assembly é uma linguagem de programação de baixo nível, muito próxima do código máquina. 
        Em vez de escrever sequências de zeros e uns, o programador usa mnemónicos, como MOV, ADD e JMP, 
        que representam as instruções do processador. O primeiro assembler é geralmente atribuído a 
        David Wheeler, que o criou em 1949 para o computador EDSAC, na Universidade de Cambridge, 
        com o objectivo de facilitar a programação. Cada arquitectura de processador (x86, ARM, entre outras) 
        tem a sua própria linguagem Assembly, e um programa chamado assembler traduz-a para código máquina. 
        Ainda hoje é usada em sistemas embebidos, drivers e áreas onde o controlo total do hardware é essencial.
      </span>
    )
  };

  return (
    <div style={appStyles.container}>
      <style>{`
        @keyframes subirAviso {
          0% { opacity: 0; transform: translateY(30px) scale(0.9); }
          12% { opacity: 1; transform: translateY(0) scale(1.04); }
          20% { transform: translateY(0) scale(1); }
          85% { opacity: 1; transform: translateY(0) scale(1); }
          100% { opacity: 0; transform: translateY(-10px) scale(0.95); }
        }
      `}</style>

      {aviso && (
        <div style={{ position: 'fixed', left: 0, right: 0, bottom: '24px', display: 'flex', justifyContent: 'center', zIndex: 1000, pointerEvents: 'none', padding: '0 12px' }}>
          <div
            key={aviso.chave}
            style={{
              animation: 'subirAviso 4s ease forwards',
              background: 'linear-gradient(135deg, #7c3aed, #db2777)',
              color: '#ffffff',
              padding: '12px 18px',
              borderRadius: '16px',
              boxShadow: '0 8px 30px rgba(0,0,0,0.45)',
              border: '1px solid rgba(255,255,255,0.35)',
              fontFamily: 'Arial, sans-serif',
              fontWeight: 'bold',
              fontSize: '11pt',
              textAlign: 'center',
              maxWidth: '420px',
            }}
          >
            {aviso.linhas.map((linha, i) => (
              <div key={i}>{linha}</div>
            ))}
          </div>
        </div>
      )}

      <header style={appStyles.header}>
        <span style={appStyles.brand}>AprenCode</span>
        <button 
          style={appStyles.themeButton} 
          onClick={() => setIsDarkMode(!isDarkMode)}
        >
          {isDarkMode ? 'Modo Claro' : 'Modo Escuro'}
        </button>
      </header>

      <PainelProgresso
        progresso={progresso}
        escuro={isDarkMode}
        aberto={painelAberto}
        aoAlternar={() => setPainelAberto(!painelAberto)}
        aoReiniciar={reiniciarProgresso}
      />

      <main style={appStyles.content}>
        
        {/* NÍVEL 1: Menu Principal de Linguagens */}
        {!linguagemSelecionada && (
          <div style={{ width: '100%' }}>
            <h1 style={appStyles.title}>Escolha a Linguagem</h1>
            <p style={appStyles.subtitle}>Selecione a linguagem que pretende estudar.</p>
            
            <div style={appStyles.blockContainer}>
              {linguagens.map((lang) => (
                <button
                  key={lang.id}
                  style={appStyles.langButton}
                  onClick={() => {
                    setLinguagemSelecionada(lang.id);
                    setPaginaAtiva('menu');
                  }}
                >
                  <span>{lang.nome}</span>
                  <LogoLinguagem key={lang.id} id={lang.id} tamanho={28} />
                </button>
              ))}
            </div>
          </div>
        )}

        {/* NÍVEL 2: Menu Secundário */}
        {linguagemSelecionada && paginaAtiva === 'menu' && (
          <div style={{ width: '100%', display: 'flex', flexDirection: 'column', alignItems: 'center' }}>
            <button 
              style={appStyles.backButton} 
              onClick={() => setLinguagemSelecionada(null)}
            >
              ← Voltar
            </button>

            <LogoLinguagem key={linguagemSelecionada} id={linguagemSelecionada} tamanho={64} style={{ marginBottom: '10px' }} />
            <h1 style={appStyles.title}>{linguagemSelecionada.toUpperCase()}</h1>
            <p style={appStyles.subtitle}>Selecione o módulo pretendido:</p>

            <div style={appStyles.blockContainer}>
              <button style={appStyles.animatedButton} onClick={() => setPaginaAtiva('historial')}>
                Breve Historial
              </button>
              <button style={appStyles.animatedButton} onClick={() => setPaginaAtiva('conceitos')}>
                Conceitos
              </button>
              <button style={appStyles.animatedButton} onClick={() => setPaginaAtiva('io')}>
                Input & Output
              </button>
              <button style={appStyles.animatedButton} onClick={() => setPaginaAtiva('ciclos')}>
                Estruturas de Controlo
              </button>
              <button style={appStyles.animatedButton} onClick={() => setPaginaAtiva('vetores')}>
                Vetores
              </button>
            </div>
          </div>
        )}

        {/* NÍVEL 3: Páginas de Conteúdo */}
        {linguagemSelecionada && paginaAtiva !== 'menu' && (
          <div style={{ width: '100%' }}>
            <button 
              style={appStyles.backButton} 
              onClick={() => setPaginaAtiva('menu')}
            >
              ← Voltar ao Menu
            </button>

            {paginaAtiva !== 'historial' && !(paginaAtiva === 'conceitos' && linguagemSelecionada === 'java') && (
              <div style={{ display: 'flex', justifyContent: 'center', marginBottom: '15px' }}>
                <LogoLinguagem key={linguagemSelecionada} id={linguagemSelecionada} tamanho={56} />
              </div>
            )}

            {paginaAtiva === 'historial' ? (
              <div style={{
                textAlign: 'center',
                fontFamily: temasHistorial[linguagemSelecionada].fontFamily,
                color: temasHistorial[linguagemSelecionada].color,
                padding: '15px',
                borderRadius: '12px',
                background: 'rgba(0,0,0,0.2)'
              }}>
                <LogoLinguagem
                  key={linguagemSelecionada}
                  id={linguagemSelecionada}
                  tamanho={50}
                  style={{ margin: '0 auto 10px auto', display: 'block' }}
                />
                <h2 style={{ color: temasHistorial[linguagemSelecionada].titleColor, fontSize: '16pt', marginBottom: '15px' }}>
                  Breve Historial de {linguagemSelecionada.toUpperCase()}
                </h2>
                <p style={{ lineHeight: '1.6', textAlign: 'justify', fontSize: '11pt' }}>
                  {historiais[linguagemSelecionada]}
                </p>
                <footer style={{ marginTop: '20px', fontWeight: 'bold', fontSize: '10pt', color: temasHistorial[linguagemSelecionada].titleColor }}>
                  {temasHistorial[linguagemSelecionada].footerText}
                </footer>
              </div>
            ) : paginaAtiva === 'conceitos' && linguagemSelecionada === 'java' ? (
              <JavaIntro />
            ) : paginaAtiva === 'conceitos' && linguagemSelecionada === 'python' ? (
              <PythonIntro />
            ) : paginaAtiva === 'conceitos' && linguagemSelecionada === 'cpp' ? (
              <CppIntro />
            ) : paginaAtiva === 'conceitos' && linguagemSelecionada === 'assembly' ? (
              <AssemblyIntro />
            ) : ['io', 'ciclos', 'vetores'].includes(paginaAtiva) ? (
              <PaginaPratica
                linguagem={linguagemSelecionada}
                modulo={paginaAtiva}
                respostas={respostas}
                aoMudarResposta={mudarResposta}
                aoCorrigir={registarResultado}
              />
            ) : (
              <div style={appStyles.textCard}>
                <h2 style={{ color: isDarkMode ? '#ec4899' : '#0284c7', marginTop: 0, fontSize: '15pt' }}>
                  {paginaAtiva === 'conceitos' && `Conceitos Fundamentais`}
                  {paginaAtiva === 'io' && `Input & Output (Com Avaliação por IA)`}
                  {paginaAtiva === 'ciclos' && `Estruturas de Controlo (Ciclos e Condicionais)`}
                  {paginaAtiva === 'vetores' && `Vetores e Arrays`}
                </h2>
                <p>
                  {paginaAtiva === 'conceitos' && `Aborda aqui a importação de bibliotecas, regras gerais da sintaxe, para que é usada e definições base.`}
                  {paginaAtiva === 'io' && `Espaço reservado para o utilizador submeter o seu código e receber a avaliação automática da IA (nota de 0 a 20) com base nos erros e acertos.`}
                  {paginaAtiva === 'ciclos' && `Explicação detalhada com blocos de código para if/else, for, do-while e switch-case, otimizados com apoio de IA.`}
                  {paginaAtiva === 'vetores' && `Explicação de armazenamento em memória, manipulação de índices e algoritmos com vetores.`}
                </p>
              </div>
            )}
          </div>
        )}

      </main>

      <footer style={{ textAlign: 'center', fontSize: '8pt', opacity: 0.6, marginTop: '20px' }}>
        AprenCode
      </footer>
    </div>
  );
}

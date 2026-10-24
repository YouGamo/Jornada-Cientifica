import React, { useState } from 'react';

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

export default function App() {
  const [isDarkMode, setIsDarkMode] = useState(true);
  const [linguagemSelecionada, setLinguagemSelecionada] = useState(null);
  const [paginaAtiva, setPaginaAtiva] = useState('menu');

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
      background: isDarkMode 
        ? 'linear-gradient(135deg, #ec4899 0%, #3b82f6 100%)' 
        : 'linear-gradient(135deg, #0284c7 0%, #ea580c 100%)',
      WebkitBackgroundClip: 'text',
      WebkitTextFillColor: 'transparent',
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
      <header style={appStyles.header}>
        <span style={appStyles.brand}>AprenCode</span>
        <button 
          style={appStyles.themeButton} 
          onClick={() => setIsDarkMode(!isDarkMode)}
        >
          {isDarkMode ? 'Modo Claro' : 'Modo Escuro'}
        </button>
      </header>

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
                  <img src={lang.logo} alt={`Logotipo de ${lang.nome}`} style={appStyles.buttonLogo} />
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

            {paginaAtiva === 'historial' ? (
              <div style={{
                textAlign: 'center',
                fontFamily: temasHistorial[linguagemSelecionada].fontFamily,
                color: temasHistorial[linguagemSelecionada].color,
                padding: '15px',
                borderRadius: '12px',
                background: 'rgba(0,0,0,0.2)'
              }}>
                <img 
                  src={temasHistorial[linguagemSelecionada].logo} 
                  alt="Logo" 
                  style={{ width: '50px', height: '50px', objectFit: 'contain', margin: '0 auto 10px auto', display: 'block' }}
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

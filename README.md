# Emprego Já! — Documentação da planilha de cadastro

## 1. Apresentação

Este documento descreve a estrutura, os campos, as regras de preenchimento e os cuidados de utilização do arquivo `mangga_programa_emprego_ja.xlsx`, destinado ao controle do cadastro de pessoas que procuram emprego por meio do programa **Emprego Já!**, da Prefeitura de Cabo Frio.

Endereço do programa informado para esta documentação: [Emprego Já! — Prefeitura de Cabo Frio](https://www.cabofrio.rj.gov.br/empregoja).

A documentação foi elaborada a partir da leitura dos dados, das abas, das células, das validações e das configurações de proteção do arquivo fornecido. A integração da planilha com o site não foi demonstrada no arquivo nem verificada nesta análise.

> **Importante:** o arquivo analisado funciona como uma ficha individual distribuída em quatro abas de preenchimento. Não foi identificada uma base consolidada na qual cada linha represente uma pessoa. O uso para acompanhamento de vários candidatos exige um procedimento adicional de organização ou uma evolução da estrutura.

## 2. Finalidade e escopo

A ficha organiza informações em quatro grupos:

1. Dados pessoais, documentos, endereço e contatos.
2. Escolaridade e histórico de conclusão dos estudos.
3. Experiência profissional, com espaço para duas empresas.
4. Preferências de vagas, ramo de atividade e empresas de interesse.

As informações podem apoiar a consulta ao perfil dos candidatos e a identificação de oportunidades compatíveis. Essas atividades dependem da atuação da equipe: não foram encontradas fórmulas, tabelas estruturadas ou mecanismos de cruzamento automático de candidatos e vagas.

O cadastro, por si só, não constitui confirmação de encaminhamento, aprovação em processo seletivo ou contratação.

## 3. Arquivo e requisitos de utilização

| Item | Descrição |
| --- | --- |
| Arquivo documentado | `mangga_programa_emprego_ja.xlsx` |
| Formato | Pasta de trabalho Excel, extensão `.xlsx` |
| Organização | Quatro abas visíveis de formulário e uma aba auxiliar oculta |
| Área de preenchimento | Coluna `D`, nas células indicadas neste documento |
| Rótulos dos campos | Coluna `C` nas abas de formulário |
| Fórmulas | Não foram encontradas fórmulas nas células examinadas |
| Tabelas estruturadas do Excel | Não foram encontradas |
| Autofiltros | Não foram encontrados |
| Nomes definidos | Não foram encontrados |
| Vínculos externos da pasta de trabalho | Não foram identificados pela inspeção |

Utilize um editor compatível com `.xlsx`. Ao abrir o arquivo em outro aplicativo ou importá-lo para um serviço online, confira se as listas de seleção, os formatos de data, as máscaras numéricas e as proteções foram preservados. A compatibilidade com aplicativos alternativos não foi testada.

## 4. Estrutura das abas

| Aba | Visibilidade | Finalidade | Proteção de planilha |
| --- | --- | --- | --- |
| `CADASTRO` | Visível | Dados pessoais, documentos, endereço e contatos | Desativada |
| `ESCOLARIDADE` | Visível | Nível de escolaridade e informações sobre os estudos | Ativada |
| `EXPERIÊNCIA` | Visível | Histórico profissional em até duas empresas | Desativada |
| `VAGAS` | Visível | Preferências de atuação e empresas de interesse | Ativada |
| `TABELAS` | Oculta | Lista auxiliar identificada pelo cabeçalho `bancos` | Desativada |

As quatro abas de formulário possuem títulos de seção e a orientação “preencha as informações”. Em todas elas, o intervalo `C4:E4` está mesclado. A área registrada na inspeção vai até a linha 22 e a coluna `E`; isso não significa que toda essa área contenha campos ou dados.

As células de entrada documentadas abaixo estão configuradas como desbloqueadas. Nas abas com proteção ativa, isso permite seu preenchimento sem a necessidade de alterar a estrutura protegida.

> A proteção de uma aba serve principalmente para prevenir alterações na estrutura. Não deve ser tratada como controle suficiente de acesso ou de confidencialidade dos dados.

## 5. Dicionário de campos

### 5.1. Aba `CADASTRO` — Dados pessoais

| Célula | Campo | Orientação de preenchimento | Regra ou formato observado |
| --- | --- | --- | --- |
| `D6` | NOME | Informar o nome completo da pessoa candidata | Formato geral; sem validação específica identificada |
| `D7` | CPF | Informar o CPF e conferir os 11 dígitos | Máscara numérica `000.000.000-00`; sem verificação de dígitos verificadores identificada |
| `D8` | NASCIMENTO | Informar a data de nascimento como uma data válida | Formato de data `mm-dd-yy` |
| `D9` | TÍTULO DE ELEITOR | Informar o documento quando sua coleta estiver prevista no procedimento do programa | Formato geral; sem validação específica identificada |
| `D10` | CÔNJUGE | Preencher quando aplicável e necessário ao procedimento | Formato geral |
| `D11` | RUA | Informar o logradouro e os elementos do endereço previstos no procedimento | Formato geral |
| `D12` | BAIRRO | Informar o bairro, sem repetir o endereço completo da rua | Formato geral |
| `D13` | CEP | Informar o CEP e conferir os 8 dígitos | Máscara numérica `00000-000` |
| `D14` | TELEFONE | Informar DDD e número de telefone fixo, quando disponível | Máscara numérica `(00) 0000-0000` |
| `D15` | CELULAR | Informar DDD e número de celular | Máscara numérica `(00) 00000-0000` |
| `D16` | E-MAIL | Informar o endereço eletrônico de contato | Formato geral; sem validação específica de e-mail identificada |
| `D17` | GÊNERO | Selecionar uma opção disponível | Lista de seleção |
| `D18` | ESTADO CIVIL | Selecionar uma opção disponível | Lista de seleção |
| `D19` | CNH | Selecionar a categoria ou a opção de ausência de habilitação | Lista de seleção |
| `D20` | É PCD? | Selecionar a resposta informada pela pessoa candidata | Lista `SIM` ou `NÃO` |

**Opções existentes nas listas:**

- **GÊNERO:** `MASCULINO`, `FEMININO`, `OUTRO`, `PREFIRO NÃO INFORMAR`.
- **ESTADO CIVIL:** `SOLTEIRO(A)`, `CASADO(A)`, `DIVORCIADO(A)`, `VIÚVO(A)`, `VIVENDO EM RELAÇÃO ESTÁVEL`.
- **CNH:** `NÃO POSSUO`, `A`, `B`, `AB`, `C`, `D`, `ACC`.
- **É PCD?:** `SIM`, `NÃO`.

As opções acima reproduzem a configuração do arquivo. Não representam uma revisão ou ampliação das categorias existentes.

**Cuidados com documentos e contatos:**

- Uma máscara de exibição não comprova que o documento ou o telefone seja válido.
- Para os campos com máscara numérica, prefira digitar somente os dígitos e conferir a apresentação resultante.
- Identificadores como CPF, CEP e telefone não são medidas numéricas. Em uma futura base consolidada, recomenda-se armazená-los como texto, preservando zeros à esquerda.
- A data de nascimento deve ser conferida com atenção: o formato observado utiliza mês antes de dia. Recomenda-se avaliar sua padronização para `dd/mm/aaaa` no uso brasileiro.

### 5.2. Aba `ESCOLARIDADE`

| Célula | Campo | Orientação de preenchimento | Regra ou formato observado |
| --- | --- | --- | --- |
| `D6` | ESCOLARIDADE | Selecionar o nível de escolaridade informado | Lista de seleção |
| `D7` | ANO DE CONCLUSÃO | Informar o ano de conclusão, quando aplicável | Validação de número inteiro com limites configurados em `1950` e `2012`; formato `0` |
| `D8` | ESTUDOU EM ESCOLA PÚBLICA? | Selecionar a resposta informada | Lista `SIM` ou `NÃO`; formato de data aplicado à célula |
| `D9` | ESTUDOU EM UNIVERSIDADE PÚBLICA? | Selecionar a resposta informada | Lista `SIM` ou `NÃO`; formato de data aplicado à célula |

**Níveis de escolaridade disponíveis:**

- `FUNDAMENTAL INCOMPLETO`
- `FUNDAMENTAL COMPLETO`
- `MÉDIO INCOMPLETO`
- `MÉDIO COMPLETO`
- `TÉCNICO INCOMPLETO`
- `TÉCNICO COMPLETO`
- `SUPERIOR INCOMPLETO`
- `SUPERIOR COMPLETO`
- `PÓS-GRADUAÇÃO/MESTRADO/DOUTORADO`

**Ponto de atenção:** a validação do ano de conclusão contém o limite superior `2012`, que precisa ser revisado para contemplar conclusões posteriores. O comportamento dessa regra em cada aplicativo não foi testado. Não altere um ano verdadeiro para um valor incorreto apenas para contornar a validação.

Para escolaridade incompleta ou perguntas não aplicáveis, a equipe deve definir um procedimento consistente. Não foram encontradas opções explícitas `NÃO SE APLICA` nas listas dessa aba.

### 5.3. Aba `EXPERIÊNCIA`

| Célula | Campo | Orientação de preenchimento | Regra ou formato observado |
| --- | --- | --- | --- |
| `D6` | POSSUI EXPERIÊNCIA PROFISSIONAL? | Selecionar `SIM` ou `NÃO` | Lista de seleção |
| `D8` | EMPRESA 1 | Informar o nome da primeira empresa registrada | Formato numérico `0`, embora o campo seja textual |
| `D9` | FUNÇÃO/CARGO | Informar a função exercida na empresa 1 | Formato de data aplicado ao campo textual |
| `D10` | MÊS/ANO DE ENTRADA | Informar o início do vínculo com a empresa 1 | Formato `mm/yyyy` |
| `D11` | MÊS/ANO DE SAÍDA | Informar o encerramento do vínculo, quando existente | Formato `mm/yyyy` |
| `D13` | EMPRESA 2 | Informar o nome da segunda empresa registrada | Formato numérico `0`, embora o campo seja textual |
| `D14` | FUNÇÃO/CARGO | Informar a função exercida na empresa 2 | Formato de data aplicado ao campo textual |
| `D15` | MÊS/ANO DE ENTRADA | Informar o início do vínculo com a empresa 2 | Formato `mm/yyyy` |
| `D16` | MÊS/ANO DE SAÍDA | Informar o encerramento do vínculo, quando existente | Formato `mm/yyyy` |

O formulário comporta **duas experiências profissionais**. Não existe campo específico identificado para indicar vínculo atual.

**Procedimento recomendado:**

- Quando houver mais de duas experiências, adotar um critério documentado, como priorizar as mais recentes ou as mais relacionadas à vaga desejada.
- Se a pessoa não tiver experiência, selecionar `NÃO` e não inventar empresas ou períodos para preencher os espaços.
- Para vínculo em andamento, definir uma convenção para a ausência da data de saída; não inserir uma saída fictícia.
- Conferir se a saída não antecede a entrada.
- Ao utilizar datas reais do Excel para os campos de mês/ano, definir uma convenção interna para o dia armazenado. A exibição `mm/yyyy` oculta o dia, mas não elimina esse componente da data.

Há um objeto de validação associado aos intervalos `D9:D11` e `D14:D16`, mas sem tipo ou fórmulas de restrição definidos. Sua presença não deve ser interpretada como validação efetiva de cargos ou datas.

### 5.4. Aba `VAGAS`

| Célula | Campo | Orientação de preenchimento | Regra ou formato observado |
| --- | --- | --- | --- |
| `D6` | RAMO DE ATIVIDADE | Selecionar o setor desejado | Lista `COMÉRCIO`, `INDÚSTRIA`, `SERVIÇOS` |
| `D7` | FUNÇÃO | Informar a função ou ocupação desejada | Formato numérico `0`, embora o campo seja textual |
| `D8` | TEM DISPONIBILIDADE DE HORÁRIO | Selecionar a resposta informada | Lista `SIM` ou `NÃO`; formato de data aplicado à célula |
| `D9` | EMPRESA DE INTERESSE 1 | Informar a primeira empresa de interesse, quando houver | Formato numérico `0` |
| `D10` | EMPRESA DE INTERESSE 2 | Informar a segunda empresa de interesse, quando houver | Formato numérico `0` |
| `D11` | EMPRESA DE INTERESSE 3 | Informar a terceira empresa de interesse, quando houver | Formato numérico `0` |

O formulário permite registrar **um ramo de atividade, uma função e até três empresas de interesse**. Não foram identificados campos específicos para turnos, dias disponíveis, faixa salarial ou múltiplas funções desejadas.

A validação `SIM`/`NÃO` está aplicada tanto a `D8` quanto à coluna inteira `A`, no intervalo `A1:A1048576`. O alcance na coluna `A` não corresponde aos campos de entrada documentados e deve ser revisado pelo responsável técnico.

### 5.5. Aba `TABELAS`

A aba `TABELAS` está oculta e contém:

- Cabeçalho `bancos` em `A1`.
- 50 registros preenchidos abaixo do cabeçalho, até `A51`.
- Valores apresentados como códigos e nomes de instituições bancárias.

Não foi encontrada referência a essa lista nas fórmulas, nos nomes definidos ou nas regras de validação examinadas. Também não foram encontrados campos de dados bancários nas quatro abas de formulário.

Portanto, não se deve atribuir à lista uma finalidade operacional não demonstrada. Recomenda-se verificar sua origem e necessidade antes de mantê-la ou removê-la. A atualidade dos nomes e códigos bancários não foi validada nesta documentação.

## 6. Regras de validação e obrigatoriedade

As listas de seleção identificadas permitem células vazias e possuem mensagens de erro habilitadas na configuração. Isso não equivale a uma regra geral de obrigatoriedade do cadastro.

Não foi identificada uma rotina de conferência de completude, nem uma regra automatizada que impeça salvar uma ficha incompleta.

Assim:

- A equipe gestora deve definir quais campos são obrigatórios, opcionais ou condicionais.
- A existência de uma lista não garante que todos os valores já armazenados estejam corretos.
- Valores inseridos por cópia e colagem devem ser conferidos, inclusive quanto à preservação das validações e dos formatos.
- Ausência de informação não deve ser convertida automaticamente em `NÃO`.
- Dados não aplicáveis devem seguir uma convenção aprovada pela equipe, sem criar categorias incompatíveis com as listas atuais.

## 7. Fluxo recomendado de utilização

### 7.1. Preparar o cadastro

1. Manter uma cópia original controlada do modelo.
2. Antes de reutilizar o arquivo, remover os valores já preenchidos nas células de entrada, preservando rótulos, formatos e validações.
3. Utilizar uma cópia por candidato enquanto a estrutura permanecer individual.
4. Definir uma identificação interna de arquivo que não exponha CPF, telefone ou outros dados pessoais no nome.

### 7.2. Preencher a ficha

1. Completar os dados da aba `CADASTRO`.
2. Registrar as informações da aba `ESCOLARIDADE`.
3. Preencher a aba `EXPERIÊNCIA` de acordo com o histórico informado.
4. Registrar as preferências na aba `VAGAS`.
5. Usar as listas disponíveis, em vez de escrever respostas fora das categorias previstas.

### 7.3. Conferir e salvar

1. Revisar nome, documentos, data de nascimento e meios de contato.
2. Conferir a coerência das respostas de gênero, estado civil, CNH e PCD com as listas correspondentes.
3. Verificar escolaridade, ano de conclusão e aplicabilidade das perguntas.
4. Conferir cargos e períodos profissionais.
5. Validar a função desejada e as empresas de interesse com a pessoa candidata.
6. Salvar no local institucional autorizado, seguindo o procedimento de organização da equipe.

### 7.4. Atualizar e acompanhar

1. Atualizar contatos e informações profissionais quando houver confirmação de mudança.
2. Registrar a data e a responsabilidade pela atualização em um controle externo autorizado, pois esses campos não existem na ficha atual.
3. Evitar cópias concorrentes sem identificação de qual versão está vigente.
4. Se houver encaminhamento ou contratação, registrar esse acompanhamento em instrumento apropriado: a ficha não possui campos próprios para esses eventos.

## 8. Inconsistências e pontos de atenção no arquivo recebido

O arquivo contém dados preenchidos e não deve ser considerado um modelo em branco. Para evitar exposição desnecessária, esta documentação não reproduz nomes, documentos, telefones ou e-mails existentes na ficha.

| Ponto identificado | Consequência possível | Ação recomendada |
| --- | --- | --- |
| `CADASTRO!D17` contém uma resposta incompatível com a lista de gênero | Classificação incorreta do perfil | Confirmar a informação e selecionar uma categoria permitida |
| `CADASTRO!D18` contém uma resposta incompatível com a lista de estado civil | Inconsistência cadastral | Confirmar e corrigir conforme a lista |
| `CADASTRO!D19` contém uma resposta incompatível com as opções de CNH | Ausência de habilitação representada fora do padrão | Confirmar e utilizar a opção adequada, inclusive `NÃO POSSUO` quando aplicável |
| `ESCOLARIDADE!D6` contém texto que não corresponde aos níveis de escolaridade | Dado de formação inválido | Substituir pela escolaridade efetivamente informada |
| `EXPERIÊNCIA!D6` contém texto incompatível com `SIM`/`NÃO` | Histórico profissional classificado incorretamente | Confirmar se há experiência e selecionar a resposta correta |
| `CADASTRO!D12` apresenta conteúdo de endereço em vez de uma identificação clara de bairro | Dificuldade de organizar candidatos por bairro | Confirmar o bairro e corrigir o campo |
| `CADASTRO!D13` contém 9 dígitos, enquanto o CEP utiliza 8 | Endereço inconsistente | Confirmar o CEP; não cortar dígitos sem verificação |
| Limite superior `2012` na validação do ano de conclusão | Restrição indevida para formação posterior | Revisar os limites e testar o comportamento da regra |
| Formatos de data em campos de respostas e de cargos | Exibição ou interpretação inadequada de certas entradas | Padronizar campos textuais e de seleção como texto ou geral |
| Formatos numéricos em nomes de empresas e função desejada | Configuração inadequada à natureza do dado | Revisar os formatos desses campos |
| Validação `SIM`/`NÃO` aplicada à coluna inteira `A` da aba `VAGAS` | Restrição em área não destinada ao preenchimento documentado | Revisar o intervalo da validação |
| Lista bancária oculta sem utilização identificada | Conteúdo auxiliar sem propósito documentado | Verificar a necessidade antes de remover ou reutilizar |

Esses pontos são observações sobre a versão recebida, não alterações realizadas na planilha. A correção de dados pessoais deve ser feita mediante confirmação, nunca por suposição.

## 9. Privacidade e segurança da informação

A ficha reúne identificadores, contatos, endereço, data de nascimento e informações pessoais. O campo sobre PCD exige cuidado especial por poder revelar informações relacionadas à saúde ou à deficiência.

Como boas práticas de governança e de proteção de dados, alinhadas à preocupação com a LGPD, recomenda-se:

- Limitar o acesso aos profissionais que necessitem das informações para suas atribuições.
- Utilizar armazenamento institucional autorizado e controles de acesso adequados.
- Evitar publicar fichas preenchidas, anexá-las a repositórios públicos ou utilizá-las em demonstrações.
- Em treinamento e testes, usar dados fictícios claramente identificados, sem reaproveitar dados reais de candidatos.
- Compartilhar com empregadores somente as informações necessárias ao encaminhamento e conforme o procedimento institucional.
- Avaliar a necessidade de coleta de cada campo, especialmente título de eleitor, cônjuge e informações sobre deficiência.
- Definir finalidade, base legal aplicável, transparência ao titular, prazo de retenção e procedimento de descarte com as áreas responsáveis.
- Manter cópias de segurança e verificar periodicamente a possibilidade de recuperação.
- Não tratar a aba oculta ou a proteção de planilha como mecanismos de sigilo.

Este README não certifica conformidade legal e não substitui a política de proteção de dados ou os procedimentos oficiais do município.

## 10. Limitações da versão atual

Não foram identificados na estrutura examinada:

- Base de múltiplos candidatos organizada em linhas.
- Identificador único do cadastro.
- Data de cadastro ou data de atualização.
- Identificação do responsável pelo atendimento.
- Situação do candidato no atendimento.
- Registro de encaminhamentos, entrevistas e contratações.
- Controle automatizado de duplicidade de CPF.
- Validação automática de CPF, CEP ou endereço de e-mail.
- Indicadores, relatórios, painéis ou fórmulas de consolidação.
- Integração demonstrada com o formulário do site.
- Histórico de alterações ou trilha de auditoria.

A planilha pode apoiar o registro individual, mas essas ausências limitam seu uso como controle completo do atendimento e dos resultados do programa.

## 11. Melhorias sugeridas

As sugestões abaixo são propostas de evolução; **não estão implementadas no arquivo recebido**.

### 11.1. Ajustes prioritários no formulário

1. Corrigir os valores incompatíveis com as listas após confirmação com a pessoa candidata.
2. Atualizar a validação do ano de conclusão.
3. Padronizar os formatos de campos textuais e de datas.
4. Revisar o intervalo da validação na aba `VAGAS`.
5. Definir campos obrigatórios e regras para informações não aplicáveis.
6. Manter um modelo limpo, sem dados de candidatos.
7. Revisar a necessidade da aba `TABELAS`.

### 11.2. Evolução para controle de vários candidatos

Para consolidar o atendimento, recomenda-se planejar uma base em que cada pessoa tenha um identificador único e um registro principal, com campos de cadastro e atualização definidos pela equipe.

Históricos que admitem múltiplos registros, como experiências e encaminhamentos, podem ser organizados em estruturas separadas vinculadas a esse identificador. Isso evita limitar permanentemente o histórico a duas empresas ou misturar vários eventos numa única célula.

Os nomes de futuras abas e colunas devem ser definidos e aprovados antes da implantação; não são parte da estrutura atual.

### 11.3. Indicadores possíveis após estruturação

Com uma base consolidada e regras de atualização, podem ser planejadas análises de:

- Quantidade de candidatos cadastrados.
- Distribuição por bairro, escolaridade e ramo de interesse.
- Perfis com e sem experiência profissional.
- Encaminhamentos realizados.
- Entrevistas e contratações registradas.

Os indicadores de encaminhamento, entrevista e contratação dependem de informações que ainda não estão presentes nesta ficha. Nenhum resultado estatístico desses indicadores foi calculado nesta documentação.

## 12. Checklist operacional

### Antes de preencher

- [ ] Abrir uma cópia do modelo autorizado.
- [ ] Confirmar que não há dados de outro candidato nas células de entrada.
- [ ] Conferir se listas, formatos e proteções foram preservados.

### Antes de salvar

- [ ] Revisar documentos, datas e contatos.
- [ ] Confirmar rua, bairro e CEP.
- [ ] Selecionar respostas válidas nas listas.
- [ ] Conferir o ano de conclusão e eventuais restrições da validação.
- [ ] Revisar empresas, cargos e períodos profissionais.
- [ ] Conferir ramo de atividade, função e empresas de interesse.
- [ ] Não preencher informações ausentes por suposição.
- [ ] Salvar no local institucional adequado.

### Na manutenção do controle

- [ ] Manter uma versão vigente identificável de cada ficha.
- [ ] Registrar atualizações pelo procedimento autorizado.
- [ ] Revisar permissões de acesso e cópias de segurança.
- [ ] Aplicar os procedimentos institucionais de retenção e descarte.

## 13. Manutenção desta documentação

Atualize este `README.md` quando houver alterações em:

- Nomes, finalidade ou visibilidade das abas.
- Células de entrada e campos disponíveis.
- Listas e regras de validação.
- Formatos de datas, documentos ou contatos.
- Proteções e procedimentos de armazenamento.
- Fluxo de atendimento e acompanhamento.
- Integrações ou recursos de consolidação.

**Referência da documentação:** arquivo `mangga_programa_emprego_ja.xlsx` fornecido nesta conversa. A planilha original não foi modificada para a produção deste README.

## Dicionário de dados

### Acidentes

Campo | Descrição
------------ | -------------
ID_ACIDENTE | Identifica o acidente. <br> É gerado automaticamente pelo sistema com o seguinte formato: fmmaasssss, sendo: <br> f = fonte do acidente <br> mm = mês do acidente <br> aa = dois últimos dígitos do ano do acidente <br> sssss = numero sequencial gerado <br> Exemplo: R079800001
ALT_NUM | Altura numérica do acidente. Estará vazio se referencia for preenchida ou for cruzamento.
REFERENCIA | Referência do acidente. <br> (Próximo do hospital; Antes da Ponte Tal, etc.) <br> Somente será preenchido se Altura Numérica NÃO for preenchido. <br> Estará vazio se Altura Numérica for preenchida ou for cruzamento.
DATA | Data que ocorreu o acidente.
HORA | Hora que ocorreu o acidente.
COD_ACID | Código do Acidente: <br> 2 - Acidente COM vitima <br> 4 - Atropelamento
VEICULOS | Totais de Veículos Envolvidos. <br> São armazenados os totais, com um dígito para cada tipo de veículo, seguindo a seguinte sequência: <br> AMOCBXFRNVUHTJSIY <br> (Veja detalhes na tabela VEICULOS, em tipo_veiculo).
VITIMAS | Totais de Vítimas Envolvidas. <br> São armazenados os totais, com dois dígitos, sendo os dois primeiros para vítima(s) feridas(s) e os dois últimos mortos.
DISTRITO | Número do Distrito.
PRINC_A | Sempre será preenchido. <br> Conterá o código do logradouro que é o pai do acidente. <br> Caso o acidente não pertença a um corredor, será preenchido com o cadloga. <br> Caso o acidente ocorra num cruzamento, esta será a primeira componente do pai do cruzamento.
PRINC_B| Segundo código do logradouro que é o pai do acidente. <br> Será preenchida SOMENTE se o acidente ocorreu num cruzamento. Nesse caso, será a segunda componente do pai do cruzamento.<br> Se não for cruzamento complexo será preenchido com o cadlogb.
TIPO_ACIDE| CO - Colisão <br> CF - Colisão frontal <br> CT - Colisão traseira <br> CL - Colisão lateral <br> CV - Colisão Transversal <br> CP - Capotamento <br> TB - Tombamento <br> AT - Atropelamento <br> AA - Atropelamento animal <br> CH - Choque <br> QM - Queda moto/bicicleta <br>  QV - Queda veículo <br> QD - Queda ocupante dentro <br> QF - Queda ocupante fora <br> OU - Outros <br> SI - Sem informação
CADLOGA | Sempre será preenchido. Contém o código do logradouro envolvido no acidente
CADLOGB | Será preenchido SOMENTE se o local que ocorreu o acidente for um cruzamento. <br> Contém o código do segundo logradouro que compõe o cruzamento.

### Veículos

Campo | Descrição
------------ | -------------
ID_VEICULO | Identifica o veículo num determinado acidente. <br> É gerado pelo sistema e incrementado automaticamente.
TIPO_VEICU | A - AU - Auto <br> M-MO-Moto <br> O-ON-Ônibus <br> C - CA - Caminhão <br> B - BI - Bicicleta <br> X-MT-MotoTaxi <br> F - OF - Ônibus Fretado/Intermunicipal <br> R - OU - Ônibus Urbano <br> N - MC - Micro-ônibus <br> V - VA - Van <br> U-VC-Vuc <br> H - CM - Caminhonete/Caminhoneta <br>  T-CR-Carreta <br> J-JI-Jipe <br>  S-OT-Outros <br> I - SI - Sem Informação <br> Y-CO-Carroça
SEXO_COND | Sexo do Condutor: <br> M - Masculino <br> F - Feminino <br> X - Sem Informação
IDADE_COND | Idade do condutor: <br> 01 a 99 - idade em anos <br> SI - Sem Informação
CATEGORIA_ | Categoria da habilitação do condutor.
USA_CINTO_ | Indica se o condutor usa cinto de segurança ou não: <br> S-Sim <br> N-Não <br> X - Sem Informação
EST_ALCOOL | Estado de Alcoolização da Vítima: <br> AA - Alcoolizado <br> AS - Suspeita de Álcool <br> BR - Branco
ESCOLARIDADE | Escolaridade da Vitima: <br> 1 - Analfabeto <br> 2 - 1o Grau Incompleto <br> 3 - 1o Grau Completo <br> 4 - 2o Grau Incompleto <br> 5 - 2o Grau Completo <br> 6 - Superior incompleto <br> 7 - Superior Completo <br> 8 - Sem Informação
ID_ACIDENT | Identifica a qual acidente o veiculo pertence.

### Vítimas

Campo | Descrição
------------ | -------------
ID_VITIMA | Identifica a vítima num determinado acidente. <br> É gerado e incrementado automaticamente pelo sistema.
SEXO| Sexo da Vitima: <br> M - Masculino <br> F - Feminino <br> X - Sem Informação
IDADE | Idade da Vítima. <br> 01 a 99 - idade em anos <br> SI - Sem Informação
TIPO_VITIM | CD - Condutor <br> PS - Passageiro <br> PD - Pedestre <br> OU - Outros <br> SI - Sem Informação
CLASSIFICA_ | F - Ferida <br> M - Morta
TIPO_VEICU | A - AU - Auto <br> M-MO-Moto <br> O-ON-Ônibus <br> C - CA - Caminhão <br> B - BI - Bicicleta <br> X-MT-MotoTáxi <br> F - OF - Ônibus Fretado/Intermunicipal <br> R - OU - Ônibus Urbano <br> N - MC - Micro-ônibus <br> V - VA - Van <br> U-VC-Vuc <br> H - CM - Caminhonete/Caminhoneta <br> T-CR-Carreta <br> J-JI-Jipe <br>  S-OT-Outros <br> I - SI - Sem Informação <br> Y-CO-Carroça <br> EST_ALCOOL
Estado de Alcoolização da Vítima: | AA - Alcoolizado <br> AS - Suspeita de Álcool <br> BR - Branco
ESCOLARIDADE | Escolaridade da Vítima: <br> 1 - Analfabeto <br> 2 - 1o Grau Incompleto <br> 3 - 1o Grau Completo<br> 4 - 2o Grau Incompleto <br> 5 - 2o Grau Completo <br> 6 - Superior incompleto <br> 7 - Superior Completo <br> 8 - Sem Informação
ID_VEICULO | Identifica a qual veículo estava a vítima.
ID_ACIDENT | Identifica a qual acidente o veículo pertence.

### Logradouros

Como o dicionário desta tabela não foi disponibilizado pela CET, a descrição dos campos foi suposta a partir da observação dos dados.

Campo | Descrição
------------ | -------------
MAPINFO_ID | Código identifiador do [Mapinfo][mapinfo]
Rua | Nome completo do logradouro
FromLeft | Início da numeração do lado ímpar
ToLeft | Fim da numeração do lado ímpar
FromRight | Início da numeração do lado par
ToRight | Fim da numeração do lado par
tipo | Abreviação do tipo de logradouro (R - Rua, AC - Avenida, etc)
titulo | Abreviação do título do nome do logradouro (DESEM - Desembargador, PROFA - Professora, etc)
preposicao | Preposição do nome do logradouro (DO, DA, DE, etc)
codlog | Código de seis dígitos do logradouro
codseg | Vazio
codlog5 | Código de cinco dígitos do logradouro
sentido | *Não foi possível supor*
classificacao | Classificação viária do logradouro (Via local, coletora, arterial, etc)

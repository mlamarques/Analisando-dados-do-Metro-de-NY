# Projeto: Analisando dados do Metro de NY

Neste projeto, você analisa os dados do metrô de NY e descobre se mais pessoas
andam de metrô quando está chovendo, comparado com quando não está.

Você vai confrontar os dados do metrô de Nova York, usar métodos estatísticos e
dados de visualização para tirar uma conclusão interessante sobre o metrô usando
o conjunto de dados que você analisou.

### Install

O projeto requer **Python 2.7** e as sequintes bibliotecas de Python instaladas:

- [urllib](https://urllib3.readthedocs.io/en/latest/)
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)

Você também vai precisar ter instalado [Jupyter Notebook](http://ipython.org/notebook.html)

### Code

O Template code é fornecido no arquivo notebook `analyzing-subway-data-ndfdsi.ipynb`.
Nele há as orientações do projeto e o código utilizado.

### Run

Navegue até local onde o projeto `Analisando dados do Metro de NY` foi salvo em
seu computador (Local onde está esse README) e execute um dos seguinte comandos:

```bash
ipython notebook analyzing-subway-data-ndfdsi.ipynb
```  
ou

```bash
jupyter notebook analyzing-subway-data-ndfdsi.ipynb
```

Esse comando irá abrir o software Jupyter Notebook e o projeto em seu browser.

## Data

O sistema de ônibus e trens de Nova Iorque - o Metro Transit Authority -
[fornece seus dados para download](http://web.mta.info/developers/developer-data-terms.html#data)
através de  arquivos CSV. Dentre as informações disponíveisestão os **registros
semanais de dados das catracas do metrô**.

Esses registros contêm contagens cumulativas das entradas e saídas, normalmente
agrupadas em períodos de 4 horas, com dados adicionais que permitem identificar
a estação específica e a catraca correspondente a cada linha do arquivo.

### Descrição das colunas

<pre>
C/A,UNIT,SCP,STATION,LINENAME,DIVISION,DATE,TIME,DESC,ENTRIES,EXITS

C/A      = Agrupamento de catracas de que a catraca faz parte (_Control Area_)
UNIT     = Cabine de controle associada à estação onde a catraca se encontra
(_Remote Unit for a station_)
SCP      = Endereço specífico da catraca (_Subunit Channel Position_)
STATION  = Nome da estação onde a catraca se encontra
LINENAME = Código representando todas linhas que passam na estação*
DIVISION = Código representando a concessionária original da linha, antes da
prefeitura assumir a gestão   
DATE     = Representa a data (no formato MM-DD-YY) do evento de auditoria agendado
TIME     = Representa o horário (hh:mm:ss) do evento de auditoria agendado
DESc     = Descreve o tipo de evento de auditoria registrado:
           1. "REGULAR" representando um evento de auditoria padrão, em que a
           contagem é feita a cada 4 horas
           2. "RECOVR AUD" significa que o valor específico estava perdido, mas
           foi recuperado posteriormente
           3. Diversos códigos sinalizam situações em que auditorias são mais
           frequentes devido a atividades de
              planejamento ou solução de problemas.
ENTRIES  = A contagem cumulativa de entradas associadas à  catraca desde o
último registro
EXITS    = A contagem cumulativa de saídas associadas à  catraca desde o
último registro

*  Normalmente as linhas são representadas por um caractere. LINENAME 456NQR
significa que os trens 4, 5, 6, N, Q e R passam pela estação.
</pre>

## Habilidades

Esse projeto ensina habilidades em:

- Coleta de dados da internet
- Estatística aplicada e aprendizagem de máquina
- MapReduce

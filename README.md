# SERS - Dimensionamento Energético 

> Sistema de estimativa de consumo de energia residencial feito em Python para execução no terminal.

## Tecnologias

- Python
- SQLite
- Biblioteca padrão do Python
- ReportLab somente para gerar o PDF

## Estrutuar do Projeto

    sers_simples/
    ├── main.py             # ponto de entrada
    ├── banco.py            # banco de dados e funções básicas
    ├── entrada.py          # leitura de números
    ├── usuarios.py         # cadastro e login
    ├── imoveis.py          # imóveis
    ├── equipamentos.py     # equipamentos
    ├── energia.py          # consumo, solar e dimensionamento
    ├── extras.py           # relatórios, alertas e tarifas
    ├── test_sers.py        # testes automáticos
    ├── requirements.txt    # dependências do projeto
    └── README.md           # este arquivo

## Executar

```bash
python main.py
```

Para gerar PDF, caso necessário:

```bash
pip install reportlab
```

## Testes

```bash
python -m unittest test_sers.py
```

## Usuário administrador para testes

- E-mail: admin@sers.local
- Senha: admin123



## Novas funções

- Cadastro da quantidade de painéis solares por imóvel.
- Estimativa de geração mensal dos painéis.
- Testes automatizados da lógica de energia solar pelo menu e pelo `test_sers.py`.
- Geração de PDF com o histórico completo de alterações e cobranças.
- Geração de PDF com recomendação simplificada de quantidade de painéis com base no consumo mensal estimado.


## Link do quadro com as tasks no Trello
>https://trello.com/invite/b/6a7096a679644a8d7975de6c/ATTIde545b349031749e53af0b6b1ff0a812EA092AE2/sers-dimensionamento-energetico


### Premissas da recomendação solar

Para manter o projeto simples, a estimativa usa painel de 550 W, 4 horas de sol por dia e rendimento de 80%. Assim, cada painel representa aproximadamente 52,8 kWh/mês. Esses valores são apenas uma estimativa acadêmica e não substituem um dimensionamento profissional.

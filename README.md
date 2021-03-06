# CMC Transparência

Project to transform the data of "Portal da Transparência" of Câmara Munipal de Curitiba into a user-friendly and anonymously data.

This project was made with `python3` and `scrapy`.

## Dependencies

`pip install Scrapy`

## Grupo de Servidores

    [
        { id: 1, name: 'Vereadores' },
        { id: 2, name: 'Efetivos' },
        { id: 3, name: 'Comissionados' },
        { id: 4, name: 'Inativos' },
        { id: 5, name: 'Ouvidor' },
        { id: 6, name: 'Cedido para a Câmara' },
        { id: 7, name: 'Cedido pela Câmara' },
        { id: 8, name: 'Temporário' },
        { id: 9, name: 'Estagiário' },
    ]

## Running the project

    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=1 CMC_MESANO='05/2017' scrapy crawl holerite -o data/vereadores.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=2 CMC_MESANO='05/2017' scrapy crawl holerite -o data/efetivos.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=3 CMC_MESANO='05/2017' scrapy crawl holerite -o data/comissionados.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=4 CMC_MESANO='05/2017' scrapy crawl holerite -o data/inativos.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=5 CMC_MESANO='05/2017' scrapy crawl holerite -o data/ouvidor.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=6 CMC_MESANO='05/2017' scrapy crawl holerite -o data/cedido-para-camara.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=7 CMC_MESANO='05/2017' scrapy crawl holerite -o data/cedido-pela-camara.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=8 CMC_MESANO='05/2017' scrapy crawl holerite -o data/temporario.json
    CMC_CPF={CPF} CMC_SENHA={SENHA} CMC_GRUPO=9 CMC_MESANO='05/2017' scrapy crawl holerite -o data/estagiario.json

## Generating the HTML

    node javascript/generate-table.js data/vereadores.json > html/vereadores.html;
    node javascript/generate-table.js data/efetivos.json > html/efetivos.html;
    node javascript/generate-table.js data/comissionados.json > html/comissionados.html;
    node javascript/generate-table.js data/inativos.json > html/inativos.html;
    node javascript/generate-table.js data/ouvidor.json > html/ouvidor.html;
    node javascript/generate-table.js data/cedido-para-camara.json > html/cedido-para-camara.html;
    node javascript/generate-table.js data/cedido-pela-camara.json > html/cedido-pela-camara.html;
    node javascript/generate-table.js data/temporario.json > html/temporario.html;
    node javascript/generate-table.js data/estagiario.json > html/estagiario.html;

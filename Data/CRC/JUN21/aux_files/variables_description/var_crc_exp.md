﻿<meta charset="utf-8"/>

---
title: Variable Spreadsheet
title: Central Credit Responsibility Database Exposure
---


`Extraction Date`: April 2019

`Manual Date`: 25 Jun 2019


# Table of Contents

1. [Cover Sheet](#cover-sheet)

2. [Credit Exposure](#credit-exposure)

3. [Time Series](#time-series)




## Cover Sheet


+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| Variable                    | Designation                                                                                    | Scale of Measurement   | Data type              | Storage type           | Start                  | End                    |
+:============================+:===============================================================================================+:======================:+:======================:+:======================:+:======================:+:======================:+
| *tina*                      | Anonymized tax identificaton number                                                            | code                   | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *natjur*                    | Legal form                                                                                     | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *cae21*                     | Portuguese classification of Economic activities (version 2.1)                                 | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *cae3*                      | Portuguese classification of Economic activities (version 3)                                   | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *district*                  | District                                                                                       | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *municipality*              | Municipality                                                                                   | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *si*                        | Institutional sector (SEC 95)                                                                  | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *si_final*                  | Institutional sector (SEC 2010)                                                                | categorical            | discrete               | long                   | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *mindate*                   | Start date of the information                                                                  | month                  | discrete               | int                    | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| *maxdate*                   | End date of the information                                                                    | month                  | discrete               | int                    | 1999m1                 | 2018m8                |
+-----------------------------+------------------------------------------------------------------------------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+

[Return](#table-of-contents)



## Credit Exposure

+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| Name                                           | Label                                                                                          | Scale of Measurement          | Data type            | Storage type   | Start                | End        |
+:===============================================+:===============================================================================================+:==============================+:=====================+:===============+:=====================+:===========+
| *tina*                                         | Anonymized tax identification number                                                           | code                          | discrete             | long           | 1999m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *bina*                                         | Creditor identification number                                                                 | int                           | discrete             | long           | 1999m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *cina*                                         | Credit exposure identifier                                                                     | code                          | discrete             | long           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *date*                                         | Reporting date                                                                                 | month                         | discrete             | float          | 1999m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *nivelresponsabilidade*                        | Responsability level                                                                           | categorical                   | discrete             | byte           | 1999m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *tipocredito*                                  | Type of credit                                                                                 | categorical                   | discrete             | int            | 1999m1               | 2008m12    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *situacaocredito*                              | Credit situation                                                                               | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *classecreditovencido*                         | Overdue class                                                                                  | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *produto*                                      | Financial product                                                                              | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *prazooriginal*                                | Original maturity                                                                              | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *prazoresidual*                                | Residual maturity                                                                              | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *valor*                                        | Outstanding amount - in euros                                                                  | euros                         | continuous           | double         | 1999m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *moeda*                                        | Denominated  currency                                                                          | code                          | discrete             | string         | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *paisbalcaoid*                                 | Creditor´s country ISO code (Branch)                                                           | code                          | discrete             | string         | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *tipogarantia*                                 | Collateral type                                                                                | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *valorg*                                       | Collateral value                                                                               | euros                         | continuous           | double         | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+
| *caracteristicas*                              | Special characteristics                                                                        | categorical                   | discrete             | byte           | 2009m1               | 2018m8    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+-------------------------------+----------------------+----------------+----------------------+------------+


[Return](#table-of-contents)


## Time Series


+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| Variable                                                             | 1999-2008                                   | 2009-2017                                           |
+:=====================================================================+:===========================================:+:===================================================:+
| *tina*                                                               | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *bina*                                                               | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *date*                                                               | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[natjur](#legal-form)*                                              | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[cae21](#economic-activities-cae21)*                                | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[cae3](#economic-activities-cae3)*                                  | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[district](#district)*                                              | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[municipality](#municipality)*                                      | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[si](#institutional-sector-sec-95)*                                 | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[si_final](#institutional-sector-sec-2010)*                         | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *mindate*                                                            | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *maxdate*                                                            | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[nivelresponsabilidade](#responsibility-level)*                     | [✓]                                         | [✓]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[tipocredito](#type-of-credit)*                                     | [✓]                                         | [X]                                                |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[situacaocredito](#credit-situation)*                               | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[classecreditovencido](#overdue-class)*                             | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[produto](#financial-product)*                                      | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[prazooriginal](#maturity-class)*                                   | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[prazoresidual](#maturity-class)*                                   | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[moeda](#currency)*                                                 | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[paisbalcaoid](#country)*                                           | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[tipogarantia](#collateral-type)*                                   | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *valorg*                                                             | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *[caracteristicas](#special-characteristics)*                        | [X]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+
| *valor*                                                              | [✓]                                         | [✓]                                                 |
+----------------------------------------------------------------------+---------------------------------------------+-----------------------------------------------------+


\

| Legend |    |
| :---: | :------: |
| [✓] | Variable available  |
| [X] | Variable not available |

[Return](#table-of-contents)


## Legal Form

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	0	|	Todas as Naturezas	|	All Legal Forms	|
|	1	|	Pessoa Colectiva de Direito Público	|	Legal Person under Public Law 	|
|	2	|	Pessoa Colectiva Internacional	|	International Legal Person	|
|	3	|	Organismo da Administração Pública	|	Body of Public Administration	|
|	4	|	Associação de Regentes e Beneficiários	|	Regent and Beneficiary Association 	|
|	5	|	Entidade Pública Empresarial	|	Public Corporation	|
|	7	|	Empresa Municipal	|	Municipal Company	|
|	8	|	Empresa Intermunicipal	|	Intermunicipal Company	|
|	9	|	Empresa Regional	|	Regional Company	|
|	10	|	Empresa Metropolitana	|	Metropolitan Company	|
|	11	|	Fundação	|	Foundation	|
|	12	|	Entidade Empresarial Municipal	|	Municipal Business Entity	|
|	13	|	Entidade Empresarial Intermunicipal	|	Intermunicipal Business Entity	|
|	14	|	Entidade Empresarial Metropolitana	|	Metropolitan Business Entity	|
|	15	|	Sociedade Civil	|	Civil Society	|
|	16	|	Sociedade civil com personalidade jurídica	|	Civil Society with Legal Personality	|
|	17	|	Sociedade anónima europeia	|	European Public Limited Company	|
|	18	|	Sociedade em nome colectivo	|	General Partnership	|
|	19	|	Sociedade Anónima	|	Public Limited Liability Company	|
|	20	|	Sociedade em Comandita	|	Limited Partneship	|
|	21	|	Sociedade por Quotas	|	Private Limited Liability Company	|
|	22	|	Sociedade Unipessoal por Quotas	|	Sole quotaholder private limited company	|
|	23	|	Sociedade anónima desportiva	|	Public Limited Sports Company	|
|	24	|	Agrupamento Europeu de Interesse Económico Civil	|	European Economic Interest Grouping (civil)	|
|	25	|	Agrupamento Europeu de Interesse Económico	|	European Economic Interest Grouping	|
|	26	|	Agrupamento Complementar de Empresas	|	Business Group	|
|	28	|	Cooperativa de Responsabilidade Ilimitada	|	Unlimited Liability Cooperative Company	|
|	29	|	Cooperativa de Responsabilidade Limitada	|	Limited Liability Cooperative Company	|
|	30	|	Cooperativa em Comandita	|	Limited Partnership Cooperative Company	|
|	31	|	União de Cooperativas	|	Union of Cooperative	|
|	32	|	Federação de Cooperativas	|	Federation of Cooperative	|
|	33	|	Confederação de Cooperativas	|	Confederation of Cooperative	|
|	34	|	Mútua de Seguros	|	Mutual Insurance Associations	|
|	35	|	Pessoa Colectiva Religiosa	|	Religious Legal Person	|
|	36	|	Pessoa Jurídica Canónica	|	Canonical Juridical Person	|
|	37	|	Pessoa Colectiva Religiosa Não Católica	|	Non-Catholic Religious Legal Person	|
|	38	|	Pessoa Colectiva Estrangeira	|	Foreign Legal Person	|
|	39	|	Empresa Pública Estrangeira	|	Foreign Public Company	|
|	40	|	Associação Estrangeira	|	Foreign Association	|
|	41	|	Fundação Estrangeira	|	Foreign Foundation	|
|	42	|	Sociedade Civil Estrangeira	|	Foreign Civil Society	|
|	43	|	Sociedade Civil Sob Forma Comercial Estrangeira	|	Foreign Civil Society with a commercial form 	|
|	44	|	Sociedade Comercial Estrangeira	|	Foreign Commercial Society	|
|	45	|	Representação permanente	|	Permanent Representation	|
|	46	|	Empresário Individual	|	Sole Proprietorship	|
|	47	|	Comerciante Individual	|	Individual Merchant	|
|	48	|	Estabelecimento Individual de Responsabilidade Limitada	|	Sole trader entity with limited liability	|
|	49	|	Sociedade Irregular	|	Unregistered company	|
|	50	|	Representação de Pessoa Colectiva Internacional	|	Representative of International Legal Person	|
|	51	|	Entidade Equiparada a Pessoa Colectiva	|	Entity Considered Equivalent to Legal Person	|
|	52	|	Estado	|	State	|
|	53	|	Autarquia local	|	Local Authority	|
|	54	|	Outras pessoas colectivas de direito público	|	Other Legal Persons Governed by Public Law	|
|	55	|	Associação ou Fundação	|	Association or Foundation	|
|	56	|	Outras Associações	|	Other Associations	|
|	57	|	Não residentes, com estabelecimento estável	|	Non-Resident with Permanent Establishment	|
|	59	|	Outras Sociedades (IES)	|	Other corporations (IES)	|
|	60	|	Entidade Pública Municipal, Intermunicipal e Regional	|	Municipal, Intermunicipal and Regional public company	|
|	64	|	Não residentes, sem estabelecimento estável	|	Non-Resident without Permanent Establishment	|
|	65	|	Entidades que não exerçam, a título principal, actividade comercial industrial ou agrícola	|	Entities Whose Main Activity Is Not in Industrial or Agricultural Commercial Sector	|
|	68	|	Agrup. Complem. Empresas e Agrup. Europeu de Interesse Económico	|	Complementary group of companies and European economic interest group	|
|	70	|	Agrupamento Europeu de Interesse Económico Comercial	|	European Economic Interest Grouping	|
|	71	|	Cooperativa	|	Cooperative	|
|	72	|	Cooperativa de 2º grau	|	Second-level Cooperative	|
|	75	|	Pessoa Colectiva de Utilidade Pública	|	Public Utility Legal Person	|
|	76	|	Entidade Equiparada Estrangeira - Identificação	|	Foreign Equivalent Entity - Identification	|
|	77	|	Representação Permanente Não Sujeita a Registo	|	Permanent Representation Not Subject to Registration	|
|	78	|	Sucursal Financeira Exterior	|	Foreign Financial Branch	|
|	79	|	Trust	|	Trust	|
|	80	|	Pessoa colectiva em formação	|	Legal Person under Construction	|
|	81	|	Associação	|	Association	|
|	82	|	Associação de direito público	|	Association Governed by Public Law 	|
|	83	|	Associação de direito privado	|	Association Governed by Private Law 	|
|	84	|	Fundação de direito público	|	Foundation Governed by Public Law 	|
|	85	|	Fundação de direito privado	|	Foundation Governed by Private Law 	|
|	86	|	Fundos de Pensões	|	Pension Fund	|
|	87	|	Fundos de Investimento Mobiliário	|	Mutual Fund	|
|	88	|	Fundos de Investimento Imobiliário	|	Real Estate Investment Fund	|
|	89	|	Fundos de Poupança Reforma	|	Retirement Savings Fund	|
|	90	|	Fundos de Poupança Educação	|	Savings Education Fund	|
|	91	|	Fundos de Poupança Reforma/Educação	|	Savings-Retirement Education Fund	|
|	92	|	Fundos de Poupança Acções	|	Savings-shares Fund	|
|	93	|	Fundos de Capital de Risco	|	Venture Capital Funds	|
|	94	|	Fundos de Fundos	|	Funds of Funds	|
|	95	|	Não Residentes Sujeitos Retenção Fonte a Título Definitivo	|	Non-Resident Subject to Withholding Tax	|
|	96	|	Heranças Indivisas	|	Undivided Estates	|
|	97	|	Organizações Internacionais	|	International Organisations	|
|	98	|	Decreto Lei 408/87 de 31/12	|	Decree Law 408/87 of 31/12	|
|	99	|	Funcionários de Embaixadas e Consulados	|	Official of Embassies and Consulates 	|
|	100	|	Outros	|	Others	|
|	101	|	Não Residentes	|	Non-Resident	|
|	102	|	Fundos	|	Fund	|
|	103	|	Entidades Estrangeiras	|	Foreign Entity	|
|	104	|	Representações	|	Representative	|
|	105	|	Outras Sociedades	|	Other Corporations	|
|	997	|	Código inválido	|	Invalid Code	|
|	998	|	Desconhecido / Em atribuição	|	Unknown	|
|	4306	|	Organizacoes Internacionais	|	International Organizations	|
|	7192	|	Fundação	|	Foundation	|
|	7193	|	Fundação estrangeira - representação permanente	|	Foreign foundation - permanent representation	|
|	7194	|	Associação de direito privado e utilidade pública	|	Association of private law and public utility	|
|	7201	|	Pessoa coletiva religiosa (católica)	|	Religious public entity (Catholic)	|
|	7202	|	Pessoa jurídica canónica (Dec. Lei no. 19/2015)	|	Canonical legal entities (Decree Law No. 19/2015)	|



[Return](#table-of-contents)

## Economic Activities CAE21

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	1111	|	Cerealicultura	|	Growing of cereals	|
|	1112	|	Culturas agrícolas, n.e.	|	Agricultural crops, n.e.c.	|
|	1120	|	Horticultura, especialidades hortícolas e produtos de viveiro	|	Growing of vegetables, horticultural specialities and nursery products	|
|	1131	|	Fruticultura	|	Growing of fruit	|
|	1132	|	Viticultura	|	Growing of grapes	|
|	1133	|	Olivicultura	|	Growing of olive	|
|	1134	|	Culturas destinadas a preparação de bebidas e de especiarias	|	Growing of beverage and spice crops	|
|	1210	|	Bovinicultura	|	Farming of cattle, dairy farming	|
|	1220	|	Criação de gado ovino, caprino, cavalar, asinino e muar	|	Farming of sheep, goats, horses, asses, mules and hinnies	|
|	1230	|	Suinicultura	|	Raising of swine/pigs	|
|	1240	|	Avicultura	|	Raising of poultry	|
|	1251	|	Apicultura	|	Beekeeping	|
|	1252	|	Outra produção animal, n.e.	|	Raising of other animals, n.e.c.	|
|	1300	|	Produção agrícola e animal associadas	|	Growing of crops combined with farming of animals (mixed farming)	|
|	1410	|	Actividades dos serviços relacionados com a agricultura actividades de plantação e manutenção de jardins e espaços verdes	|	Agricultural service activities	|
|	1420	|	Actividades dos serviços relacionados com a produção animal, excepto serviços de veterinária	|	Support activities for animal production	|
|	1501	|	Caça e repovoamento cinegético	|	Hunting and trapping	|
|	1502	|	Actividades dos serviços relacionados com a caça e repovoamento cinegético	|	Service activities related to hunting and trapping	|
|	2011	|	Silvicultura	|	Sylviculture	|
|	2012	|	Exploração florestal	|	Logging	|
|	2020	|	Actividades dos serviços relacionados com a silvicultura e exploração florestal	|	Support services to forestry	|
|	5011	|	Pesca marítima	|	Marine fishing	|
|	5012	|	Pesca em águas interiores	|	Fishing in inland waters	|
|	5013	|	Apanha de algas e de outros produtos do mar e de águas interiores	|	Collecting seaweed and other sea and inland water products	|
|	5020	|	Aquacultura	|	Fish farming	|
|	10101	|	Extracção de hulha (inclui antracite)	|	Mining of hard coal	|
|	10102	|	Aglomeração da hulha (inclui antracite)	|	Agglomeration of hard coal (including anthracite)	|
|	10200	|	Extracção e aglomeração de linhite	|	Mining and agglomeration of lignite	|
|	10300	|	Extracção e aglomeração de turfa	|	Extraction and agglomeration of peat	|
|	11100	|	Extracção de petróleo bruto e gás natural	|	Extraction of crude petroleum and natural gas	|
|	11200	|	Actividades dos serviços relacionados com a extracção de petróleo e gás, excepto a prospecção	|	Support activities for petroleum and natural gas extraction	|
|	12000	|	Extracção e preparação de minérios de urânio e de tório	|	Mining of uranium and thorium ores	|
|	13100	|	Extracção e preparação de minérios de ferro	|	Mining of iron ores	|
|	13201	|	Extracção e preparação de minérios de cobre	|	Mining and preparation of copper ores	|
|	13202	|	Extracção e preparação de minérios de estanho	|	Mining and preparation of tin ores	|
|	13203	|	Extracção e preparação de minérios de volfrâmio	|	Mining and preparation of wolfram ores	|
|	13204	|	Extracção e preparação de minérios de metais preciosos	|	Mining and preparation of precious metal ores	|
|	13205	|	Extracção e preparação de minérios metálicos não ferrosos (excepto minérios de urânio e tório), n.e.	|	Mining and preparation of non-ferrous metal ores, except uranium and thorium ores n.e.c.	|
|	14111	|	Extracção de mármore e outras rochas carbonatadas	|	Quarrying of marble and other carbonated stones	|
|	14112	|	Extracção de granito ornamental e rochas similares	|	Quarrying of ornamental granite and similar stones	|
|	14121	|	Extracção de calcário e cré	|	Quarrying of limestone and chalk	|
|	14122	|	Extracção de gesso	|	Quarrying of gypsum	|
|	14130	|	Extracção de ardósia	|	Quarrying of slate	|
|	14210	|	Extracção de saibro, areia e pedra britada	|	Operation of gravel and sand pits	|
|	14220	|	Extracção de argilas e caulino	|	Mining of clays and kaolin	|
|	14301	|	Extracção de pirites	|	Quarrying of pyrites	|
|	14302	|	Extracção de minerais para a indústria química e para a fabricação de adubos, n.e.	|	Mining of chemical and fertilizer minerals, n.e.c.	|
|	14401	|	Extracção de sal marinho	|	Extraction of sea salt	|
|	14402	|	Extracção de sal gema	|	Extraction of rock salt	|
|	14403	|	Refinação de sal	|	Refining of salt	|
|	14501	|	Extracção de quartzo	|	Quarrying of quartz	|
|	14502	|	Extracção de feldspato	|	Quarrying of feldspar	|
|	14503	|	Extracção de diatomito	|	Quarrying of diatomite	|
|	14504	|	Extracção de outros minerais não metálicos, n.e.	|	Quarrying of other non-metallic mineral products, n.e.c.	|
|	15110	|	Abate de gado (produção de carne)	|	Processing and preserving of meat	|
|	15120	|	Abate de aves e de coelhos (produção de carne)	|	Production and preserving of poultrymeat	|
|	15130	|	Fabricação de produtos à base de carne	|	Production of meat and poultry meat products	|
|	15201	|	Preparação de produtos da pesca e da aquicultura	|	Preparation of fish and fish products	|
|	15202	|	Congelação de produtos da pesca e da aquicultura	|	Freezing of fish and fish products	|
|	15203	|	Conservação de produtos da pesca e da aquicultura em azeite e outros óleos vegetais e outros molhos	|	Preserving of fish and fish products in olive oil and other vegetable oil and other sauces	|
|	15204	|	Salga, secagem e outras actividades de transformação de produtos da pesca e aquicultura	|	Drying, salting and other fish processing and preserving	|
|	15310	|	Preparação e conservação de batatas	|	Processing and preserving of potatoes	|
|	15320	|	Fabricação de sumos de frutos e de produtos hortícolas	|	Manufacture of fruit and vegetable juice	|
|	15331	|	Congelação de frutos e de produtos hortícolas	|	Freezing of fruit and vegetables	|
|	15332	|	Secagem e desidratação de frutos e de produtos hortícolas	|	Drying and dehydration of fruit and vegetables	|
|	15333	|	Fabricação de doces, compotas, geleias e marmelada	|	Manufacture of jams, marmalades and table jellies	|
|	15334	|	Descasque e transformação de frutos de casca rija comestíveis	|	Peeling and processing of edible nuts	|
|	15335	|	Preparação e conservação de frutos e de produtos hortícolas por processos, n.e.	|	Preparation and preserving of fruit and vegetables, n.e.c.	|
|	15411	|	Produção de óleos e gorduras animais brutos	|	Manufacture of crude animal oils and fats	|
|	15412	|	Produção de azeite	|	Production of olive oil	|
|	15413	|	Produção de óleos vegetais brutos (excepto azeite)	|	Production of crude vegetable oils (except olive oil)	|
|	15420	|	Refinação de óleos e gorduras	|	Manufacture of refined oils and fats	|
|	15430	|	Fabricação de margarinas e de gorduras alimentares similares	|	Manufacture of margarine and similar edible fats	|
|	15510	|	Indústrias do leite e derivados	|	Operation of dairies and cheese making	|
|	15520	|	Fabricação de gelados e sorvetes	|	Manufacture of ice cream	|
|	15611	|	Moagem de cereais	|	Grain milling	|
|	15612	|	Descasque, branqueamento e glaciagem de arroz	|	Husking, whitening and glazing of rice	|
|	15613	|	Transformação de cereais e leguminosas, n.e.	|	Manufacture of grain mill products, n.e.c.	|
|	15620	|	Fabricação de amidos, féculas e produtos afins	|	Manufacture of starches and starch products	|
|	15710	|	Fabricação de alimentos para animais de criação	|	Manufacture of prepared feeds for farm animals	|
|	15720	|	Fabricação de alimentos para animais de estimação	|	Manufacture of prepared pet foods	|
|	15811	|	Panificação	|	Manufacture of bread	|
|	15812	|	Pastelaria	|	Manufacture of fresh pastry goods and cakes	|
|	15820	|	Fabricação de bolachas, biscoitos, tostas e pastelaria de conservação	|	Manufacture of rusks and biscuits	|
|	15830	|	Indústria do açúcar	|	Manufacture of sugar	|
|	15841	|	Fabricação de cacau e de chocolate	|	Manufacture of cocoa and chocolate	|
|	15842	|	Fabricação de produtos de confeitaria	|	Manufacture of sugar confectionery	|
|	15850	|	Fabricação de massas alimentícias, cuscuz e similares	|	Manufacture of macaroni, noodles, couscous and similar farinaceous products	|
|	15860	|	Indústria do café e do chá	|	Processing of tea and coffee	|
|	15870	|	Fabricação de condimentos e temperos	|	Manufacture of condiments and seasonings	|
|	15880	|	Fabricação de alimentos homogeneizados e dietéticos	|	Manufacture of homogenised food preparations and dietetic food	|
|	15891	|	Fabricação de fermentos, leveduras e adjuvantes para panificação e pastelaria	|	Manufacture of starters, yeast and adjuvants for breadmaking and pastry	|
|	15892	|	Fabricação de caldos, sopas e sobremesas	|	Manufacture of broths, soups and desserts	|
|	15893	|	Fabricação de outros produtos alimentares diversos, n.e.	|	Manufacture of other food products n.e.c.	|
|	15911	|	Fabricação de aguardentes preparadas	|	Manufacture of prepared spirits	|
|	15912	|	Fabricação de aguardentes não preparadas	|	Manufacture of non-prepared spirits	|
|	15913	|	Produção de licores e de outras bebidas destiladas	|	Manufacture of liqueurs and other distilled alcoholic beverages	|
|	15920	|	Fabricação de álcool etílico de fermentação	|	Manufacture of ethyl alcohol fermentation	|
|	15931	|	Produção de vinhos comuns e licorosos	|	Manufacture of ordinary and liqueur wine	|
|	15932	|	Produção de vinhos espumantes e espumosos	|	Manufacture of sparkling wine	|
|	15940	|	Fabricação de cidra e outras bebidas fermentadas de frutos	|	Manufacture of cider and other fruit wines	|
|	15950	|	Fabricação de vermutes e de outras bebidas fermentadas não destiladas	|	Manufacture of other non-distilled fermented beverages	|
|	15960	|	Fabricação de cerveja	|	Manufacture of beer	|
|	15970	|	Fabricação de malte	|	Manufacture of malt	|
|	15981	|	Engarrafamento de águas minerais naturais e de nascente	|	Bottling of natural mineral and spring waters 	|
|	15982	|	Fabricação de refrigerantes e de outras bebidas não alcoólicas, n.e.	|	Production of soft drinks and other non-alcoholic flavoured and/or sweetened waters, n.e.c.	|
|	16000	|	Indústria do tabaco	|	Manufacture of tobacco products	|
|	17110	|	Preparação e fiação de fibras do tipo algodão	|	Preparation and spinning of cotton-type fibres	|
|	17120	|	Preparação e fiação de fibras do tipo lã cardada	|	Preparation and spinning of woollen-type fibres	|
|	17130	|	Preparação e fiação de fibras do tipo lã penteada	|	Preparation and spinning of worsted-type fibres	|
|	17140	|	Preparação e fiação de fibras de tipo linho	|	Preparation and spinning of flax-type fibres	|
|	17150	|	Preparação e fiação da seda e preparação e texturização de filamentos sintéticos e artificiais	|	Throwing and preparation of silk, including from noils, and throwing and texturing of synthetic or artificial filament yarns	|
|	17160	|	Fabricação de linhas de costura	|	Manufacture of sewing threads	|
|	17170	|	Preparação e fiação de outras fibras têxteis	|	Preparation and spinning of other textile fibres	|
|	17210	|	Tecelagem de fio do tipo algodão	|	Cotton-type weaving	|
|	17220	|	Tecelagem de fio do tipo lã cardada	|	Woollen-type weaving	|
|	17230	|	Tecelagem de fio do tipo lã penteada	|	Worsted-type weaving	|
|	17240	|	Tecelagem de fio do tipo seda	|	Silk-type weaving	|
|	17250	|	Tecelagem de fio de outros têxteis	|	Other textile weaving	|
|	17301	|	Branqueamento e tingimento	|	Bleaching and dyeing	|
|	17302	|	Estampagem	|	Printing services of textile articles	|
|	17303	|	Acabamento de fios e tecidos, n.e.	|	Finishing of yarns and fabrics, n.e.c.	|
|	17400	|	Fabricação de artigos têxteis confeccionados, excepto vestuário	|	Manufacture of made-up textile articles, except apparel	|
|	17510	|	Fabricação de tapetes e carpetes	|	Manufacture of carpets and rugs	|
|	17521	|	Fabricação de cordoaria	|	Manufacture of cordage, rope and twine	|
|	17522	|	Fabricação de redes	|	Manufacture of nets	|
|	17530	|	Fabricação de não tecidos e respectivos artigos, excepto vestuário	|	Manufacture of non-wovens and articles made from non-wovens, except apparel	|
|	17541	|	Fabricação de passamanarias e sirgarias	|	Manufacture of ornamental trimmings and narrow fabrics	|
|	17542	|	Fabricação de bordados	|	Manufacture of embroidery	|
|	17543	|	Fabricação de rendas	|	Manufacture of lace	|
|	17544	|	Outras indústrias têxteis diversas, n.e.	|	Manufacture of other miscellaneous textiles, n.e.c.	|
|	17600	|	Fabricação de tecidos de malha	|	Manufacture of knitted and crocheted fabrics	|
|	17710	|	Fabricação de meias e artigos similares de malha	|	Manufacture of knitted and crocheted hosiery	|
|	17720	|	Fabricação de pulóveres, casacos e artigos similares de malha	|	Manufacture of knitted and crocheted pullovers, cardigans and similar articles	|
|	18100	|	Confecção de artigos de vestuário em couro	|	Manufacture of leather clothes	|
|	18210	|	Confecção de vestuário de trabalho e de uniformes	|	Manufacture of workwear	|
|	18221	|	Confecção de outro vestuário exterior em série	|	Manufacture of other ready-to-wear outerwear 	|
|	18222	|	Confecção de outro vestuário exterior por medida	|	Manufacture of other made-to-measure outerwear	|
|	18230	|	Confecção de vestuário interior	|	Manufacture of underwear	|
|	18240	|	Confecção de outros artigos e acessórios de vestuário, n.e.	|	Manufacture of other wearing apparel and accessories n.e.c.	|
|	18301	|	Curtimenta e acabamento de peles com pêlo	|	Tanning and dressing of fur	|
|	18302	|	Fabricação de artigos de peles com pêlo	|	Manufacture of articles of fur	|
|	19101	|	Curtimenta e acabamento de peles sem pêlo	|	Tanning and dressing of leather	|
|	19102	|	Fabricação de couro reconstituído	|	Manufacture of composition leather	|
|	19200	|	Fabricação de artigos de viagem e de uso pessoal, de marroquinaria, de correeiro e de seleiro	|	Manufacture of luggage, handbags and the like, saddlery and harness	|
|	19301	|	Fabricação de calçado	|	Manufacture of footwear	|
|	19302	|	Fabricação de componentes para calçado	|	Manufacture of parts of footwear	|
|	20101	|	Serração de madeira	|	Sawmilling of wood	|
|	20102	|	Impregnação de madeira	|	Impregnation of wood	|
|	20201	|	Fabricação de painéis de partículas de madeira	|	Manufacture of wood particle boards	|
|	20202	|	Fabricação de painéis de fibras de madeira	|	Manufacture of wood fibre boards	|
|	20203	|	Fabricação de folheados, contraplacados, lamelados e de outros painéis	|	Manufacture of veneer sheets	|
|	20301	|	Parqueteria	|	Manufacture of assembled parquet floors	|
|	20302	|	Carpintaria	|	Carpentry	|
|	20400	|	Fabricação de embalagens de madeira	|	Manufacture of wooden containers	|
|	20511	|	Fabricação de caixões mortuários em madeira	|	Manufacture of wooden coffins	|
|	20512	|	Fabricação de outras obras de madeira, n.e.	|	Manufacture of other products of wood, n.e.c.	|
|	20521	|	Fabricação de obras de cestaria e de espartaria	|	Manufacture of articles of straw and plaiting materials	|
|	20522	|	Indústria da cortiça	|	Cork industry	|
|	21110	|	Fabricação de pasta	|	Manufacture of pulp	|
|	21120	|	Fabricação de papel e de cartão (excepto canelado)	|	Manufacture of paper and paperboard	|
|	21211	|	Fabricação de papel e de cartão canelados (inclui embalagens)	|	Manufacture of corrugated paper and paperboard 	|
|	21212	|	Fabricação de outras embalagens de papel e de cartão	|	Manufacture of other containers of paper and paperboard	|
|	21220	|	Fabricação de artigos de papel para uso doméstico e sanitário	|	Manufacture of household and sanitary goods and of toilet requisites	|
|	21230	|	Fabricação de artigos de papel para papelaria	|	Manufacture of paper stationery	|
|	21240	|	Fabricação de papel de parede	|	Manufacture of wallpaper	|
|	21250	|	Fabricação de artigos de pasta de papel, de papel e de cartão, n.e.	|	Manufacture of other articles of paper and paperboard n.e.c.	|
|	22110	|	Edição de livros	|	Book publishing	|
|	22120	|	Edição de jornais	|	Publishing of newspapers	|
|	22130	|	Edição de revistas e de outras publicações periódicas	|	Publishing of journals and periodicals	|
|	22140	|	Edição de gravações de som	|	Publishing of sound recordings	|
|	22150	|	Edição, n.e.	|	Other publishing	|
|	22210	|	Impressão de jornais	|	Printing of newspapers	|
|	22220	|	Impressão, n.e.	|	Printing n.e.c.	|
|	22230	|	Encadernação	|	Bookbinding	|
|	22240	|	Actividades de preparação da impressão	|	Pre-press activities	|
|	22250	|	Actividades auxiliares relacionadas com a impressão, n.e.	|	Ancillary activities related to printing	|
|	22310	|	Reprodução de gravações de som	|	Reproduction of sound recording	|
|	22320	|	Reprodução de gravações de vídeo	|	Reproduction of video recording	|
|	22330	|	Reprodução de suportes informáticos	|	Reproduction of computer media	|
|	23100	|	Fabricação de coque	|	Manufacture of coke oven products	|
|	23200	|	Fabricação de produtos petrolíferos refinados	|	Manufacture of refined petroleum products	|
|	23300	|	Tratamento de combustível nuclear	|	Processing of nuclear fuel 	|
|	24110	|	Fabricação de gases industriais	|	Manufacture of industrial gases	|
|	24120	|	Fabricação de corantes e pigmentos	|	Manufacture of dyes and pigments	|
|	24130	|	Fabricação de outros produtos químicos inorgânicos de base	|	Manufacture of other inorganic basic chemicals	|
|	24141	|	Fabricação de resinosos e seus derivados	|	Manufacture of resin and its derivatives	|
|	24142	|	Fabricação de carvão (vegetal e animal) e produtos associados	|	Manufacture of coal (plant and animal) and related products	|
|	24143	|	Fabricação de outros produtos químicos orgânicos de base, n.e.	|	Manufacture of other organic basic chemicals, n.e.c.	|
|	24151	|	Fabricação de adubos químicos ou minerais e de compostos azotados	|	Manufacture of chemical or mineral fertilisers and nitrogen compounds	|
|	24152	|	Fabricação de adubos orgânicos e organo-minerais	|	Manufacture of organic and organic-mineral fertilisers	|
|	24160	|	Fabricação de matérias plásticas sob formas primárias	|	Manufacture of plastics in primary forms	|
|	24170	|	Fabricação de borracha sintética sob formas primárias	|	Manufacture of synthetic rubber in primary forms	|
|	24200	|	Fabricação de pesticidas e de outros produtos agroquímicos	|	Manufacture of pesticides and other agrochemical products	|
|	24301	|	Fabricação de tintas (excepto impressão), vernizes, mastiques e produtos similares	|	Manufacture of paints (except printing ink), varnishes, mastics and related products	|
|	24302	|	Fabricação de tintas de impressão	|	Manufacture of printing ink	|
|	24410	|	Fabricação de produtos farmacêuticos de base	|	Manufacture of basic pharmaceutical products	|
|	24421	|	Fabricação de medicamentos	|	Manufacture of medicaments	|
|	24422	|	Fabricação de outras preparações e de artigos farmacêuticos	|	Manufacture of other pharmaceutical preparations and pharmaceuticals	|
|	24511	|	Fabricação de sabões, detergentes e glicerina	|	Manufacture of soap, detergents and glycerol	|
|	24512	|	Fabricação de produtos de limpeza, polimento e protecção	|	Manufacture of cleaning and polishing preparations	|
|	24520	|	Fabricação de perfumes, de cosméticos e de produtos de higiene	|	Manufacture of perfumes and toilet preparations	|
|	24610	|	Fabricação de explosivos e artigos de pirotecnia	|	Manufacture of explosives	|
|	24620	|	Fabricação de colas e gelatinas	|	Manufacture of glues and gelatines	|
|	24630	|	Fabricação de óleos essenciais	|	Manufacture of essential oils	|
|	24640	|	Fabricação de produtos químicos para fotografia	|	Manufacture of photographic chemical material	|
|	24650	|	Fabricação de suportes de informação não gravados	|	Manufacture of prepared unrecorded media	|
|	24661	|	Fabricação de produtos químicos auxiliares para uso industrial	|	Manufacture of chemical products for industrial use	|
|	24662	|	Fabricação de óleos e massas lubrificantes, com exclusão da efectuada nas refinarias	|	Manufacture of lubricating oils and greases, except that made in refineries	|
|	24663	|	Fabricação de outros produtos químicos diversos, n.e.	|	Manufacture of other miscellaneous chemical products, n.e.c.	|
|	24700	|	Fabricação de fibras sintéticas ou artificiais	|	Manufacture of man-made fibres	|
|	25110	|	Fabricação de pneus e câmaras-de-ar	|	Manufacture of rubber tyres and tubes	|
|	25120	|	Reconstrução de pneus	|	Retreading and rebuilding of rubber tyres	|
|	25130	|	Fabricação de produtos de borracha, n.e.	|	Manufacture of other rubber products	|
|	25210	|	Fabricação de chapas, folhas, tubos e perfis de plástico	|	Manufacture of plastic plates, sheets, tubes and profiles	|
|	25220	|	Fabricação de embalagens de plástico	|	Manufacture of plastic packing goods	|
|	25230	|	Fabricação de artigos de plástico para a construção	|	Manufacture of builder's ware of plastic	|
|	25240	|	Fabricação de artigos de plástico, n.e.	|	Manufacture of other plastic products	|
|	26110	|	Fabricação de vidro plano	|	Manufacture of flat glass	|
|	26120	|	Moldagem e transformação de vidro plano	|	Shaping and processing of flat glass	|
|	26131	|	Fabricação de vidro de embalagem	|	Manufacture of hollow glass	|
|	26132	|	Cristalaria	|	Manufacture of crystal ware	|
|	26140	|	Fabricação de fibras de vidro	|	Manufacture of glass fibres	|
|	26150	|	Fabricação e transformação de outro vidro (inclui vidro técnico)	|	Manufacture and processing of other glass, including technical glassware	|
|	26211	|	Olaria de barro	|	Pottery	|
|	26212	|	Fabricação de artigos de uso doméstico de faiança, porcelana e grés fino	|	Manufacture of household articles made of stone- or earthenware, porcelain and china	|
|	26213	|	Fabricação de artigos de ornamentação de faiança, porcelana e grés fino	|	Manufacture of ornamental articles made of stone- or earthenware, porcelain and china	|
|	26220	|	Fabricação de artigos cerâmicos para usos sanitários	|	Manufacture of ceramic sanitary fixtures	|
|	26230	|	Fabricação de isoladores e peças isolantes em cerâmica	|	Manufacture of ceramic insulators and insulating fittings	|
|	26240	|	Fabricação de outros produtos em cerâmica para usos técnicos	|	Manufacture of other technical ceramic products	|
|	26250	|	Fabricação de outros produtos cerâmicos não refractários (excepto os destinados a construção)	|	Manufacture of other ceramic products	|
|	26260	|	Fabricação de produtos cerâmicos refractários	|	Manufacture of refractory products	|
|	26301	|	Fabricação de azulejos	|	Manufacture of ceramic tiles 	|
|	26302	|	Fabricação de ladrilhos, mosaicos e placas de cerâmica	|	Manufacture of floor flags, tiles and mosaic	|
|	26401	|	Fabricação de tijolos e telhas	|	Manufacture of bricks and tiles 	|
|	26402	|	Fabricação de abobadilhas	|	Manufacture of support or filler tiles	|
|	26403	|	Fabricação de outros produtos de barro para a construção	|	Manufacture of construction products, in baked clay	|
|	26510	|	Fabricação de cimento	|	Manufacture of cement	|
|	26521	|	Fabricação de cal hidráulica	|	Manufacture of hydraulic lime	|
|	26522	|	Fabricação de cal não hidráulica	|	Manufacture of non-hydraulic lime	|
|	26530	|	Fabricação de gesso	|	Manufacture of plaster	|
|	26610	|	Fabricação de produtos de betão para a construção	|	Manufacture of concrete products for construction purposes	|
|	26620	|	Fabricação de produtos de gesso para a construção	|	Manufacture of plaster products for construction purposes	|
|	26630	|	Fabricação de betão pronto	|	Manufacture of ready-mixed concrete	|
|	26640	|	Fabricação de argamassas	|	Manufacture of mortars	|
|	26650	|	Fabricação de produtos de fibrocimento	|	Manufacture of fibre cement	|
|	26660	|	Fabricação de outros produtos de betão, gesso, cimento e marmorite	|	Manufacture of other articles of concrete, plaster and cement	|
|	26701	|	Fabricação de artigos de mármore e de rochas similares	|	Manufacture of articles of marble and similar stone	|
|	26702	|	Fabricação de artigos em ardósia (lousa)	|	Manufacture of articles of slate	|
|	26703	|	Fabricação de artigos de granito e de rochas, n.e.	|	Manufacture of articles of granite and stones, n.e.c.	|
|	26810	|	Fabricação de produtos abrasivos	|	Production of abrasive products	|
|	26821	|	Fabricação de misturas betuminosas	|	Manufacture of bituminous mixtures	|
|	26822	|	Fabricação de outros produtos minerais não metálicos diversos, n.e.	|	Manufacture of other non-metallic mineral products, n.e.c.	|
|	27100	|	Siderurgia e fabricação de ferro-ligas	|	Manufacture of basic iron and steel and of ferro-alloys	|
|	27210	|	Fabricação de tubos de ferro fundido	|	Manufacture of cast iron tubes	|
|	27220	|	Fabricação de tubos de aço	|	Manufacture of steel tubes	|
|	27310	|	Estiragem a frio	|	Cold drawing of bars	|
|	27320	|	Laminagem a frio de arco ou banda	|	Cold rolling of narrow strip	|
|	27330	|	Perfilagem a frio	|	Cold forming or folding	|
|	27340	|	Trefilagem	|	Wire drawing	|
|	27410	|	Obtenção e primeira transformação de metais preciosos	|	Precious metals production	|
|	27420	|	Obtenção e primeira transformação de alumínio	|	Aluminium production	|
|	27430	|	Obtenção e primeira transformação de chumbo, zinco e estanho	|	Lead, zinc and tin production	|
|	27440	|	Obtenção e primeira transformação de cobre	|	Copper production	|
|	27450	|	Obtenção e primeira transformação de metais não ferrosos, n.e.	|	Other non-ferrous metal production	|
|	27510	|	Fundição de ferro fundido	|	Casting of iron	|
|	27520	|	Fundição de aço	|	Casting of steel	|
|	27530	|	Fundição de metais leves	|	Casting of light metals	|
|	27540	|	Fundição de metais não ferrosos, n.e.	|	Casting of other non-ferrous metals	|
|	28110	|	Fabricação de estruturas de construções metálicas	|	Manufacture of metal structures and parts of structures	|
|	28120	|	Fabricação de portas, janelas e elementos similares em metal	|	Manufacture of doors and windows of metal	|
|	28210	|	Fabricação de reservatórios e de recipientes metálicos	|	Manufacture of tanks, reservoirs and containers of metal	|
|	28220	|	Fabricação de caldeiras e radiadores para aquecimento central	|	Manufacture of central heating radiators and boilers	|
|	28300	|	Fabricação de geradores de vapor (excepto caldeiras para aquecimento central)	|	Manufacture of steam generators, except central heating hot water boilers	|
|	28401	|	Fabricação de produtos forjados, estampados e laminados	|	Forging, pressing, stamping and roll forming of metal	|
|	28402	|	Fabricação de produtos por pulverometalurgia	|	Powder metallurgy	|
|	28510	|	Tratamento e revestimento de metais	|	Treatment and coating of metals	|
|	28520	|	Actividades de mecânica geral	|	Machining	|
|	28610	|	Fabricação de cutelaria	|	Manufacture of cutlery	|
|	28621	|	Fabricação de ferramentas manuais	|	Manufacture of hand tools	|
|	28622	|	Fabricação de ferramentas mecânicas	|	Manufacture of mechanical tools	|
|	28623	|	Fabricação de peças sinterizadas	|	Manufacture of sintered parts	|
|	28630	|	Fabricação de fechaduras, dobradiças e de outras ferragens	|	Manufacture of locks and hinges	|
|	28710	|	Fabricação de embalagens metálicas pesadas	|	Manufacture of steel drums and similar containers	|
|	28720	|	Fabricação de embalagens metálicas ligeiras	|	Manufacture of light metal packaging 	|
|	28730	|	Fabricação de produtos de arame	|	Manufacture of wire products	|
|	28741	|	Fabricação de rebites e parafusos	|	Manufacture of fasteners and screw machine products	|
|	28742	|	Fabricação de molas	|	Manufacture of springs	|
|	28743	|	Fabricação de correntes metálicas	|	Manufacture of metal chains	|
|	28751	|	Fabricação de louça metálica e artigos de uso doméstico	|	Manufacture of metal household articles	|
|	28752	|	Fabricação de outros produtos metálicos diversos,  n.e.	|	Manufacture of other fabricated miscellaneous metal products,  n.e.c.	|
|	29110	|	Fabricação de motores e turbinas	|	Manufacture of engines and turbines, except aircraft, vehicle and cycle engines	|
|	29120	|	Fabricação de bombas e compressores	|	Manufacture of pumps and compressors	|
|	29130	|	Fabricação de torneiras e de válvulas	|	Manufacture of taps and valves	|
|	29140	|	Fabricação de rolamentos, de engrenagens e de outros órgãos de transmissão	|	Manufacture of bearings, gears, gearing and driving elements	|
|	29210	|	Fabricação de fornos e queimadores	|	Manufacture of ovens, furnaces and furnace burners	|
|	29221	|	Fabricação de ascensores e monta cargas, escadas e passadeiras rolantes	|	Manufacture of lifts, escalators and moving walkways	|
|	29222	|	Fabricação de equipamentos de elevação e de movimentação, n.e.	|	Manufacture of lifting and handling equipment, n.e.c.	|
|	29230	|	Fabricação de equipamento não doméstico para refrigeração e ventilação	|	Manufacture of non-domestic cooling and ventilation equipment	|
|	29241	|	Fabricação e reparação de máquinas de acondicionamento e de embalagem	|	Manufacture and repair of packing and wrapping machinery 	|
|	29242	|	Fabricação de balanças e de outro equipamento para pesagem	|	Manufacture of scales and other weighing machinery	|
|	29243	|	Fabricação de outras máquinas diversas de uso geral, n.e.	|	Manufacture of other general purpose machinery, n.e.c.	|
|	29310	|	Fabricação de tractores agrícolas	|	Manufacture of agricultural tractors	|
|	29320	|	Fabricação de outras máquinas para a agricultura, pecuária e silvicultura	|	Manufacture of other agricultural and forestry machinery	|
|	29410	|	Fabricação de máquinas-ferramentas portáteis com motor	|	Manufacture of power-driven hand tools	|
|	29420	|	Fabricação de outras máquinas-ferramentas para metais	|	Manufacture of other metalworking machine tools	|
|	29430	|	Fabricação de outras máquinas-ferramentas, n.e.	|	Manufacture of other machine tools	|
|	29510	|	Fabricação de máquinas para a metalurgia	|	Manufacture of machinery for metallurgy	|
|	29520	|	Fabricação de máquinas para as indústrias extractivas e para a construção	|	Manufacture of machinery for mining, quarrying and construction	|
|	29530	|	Fabricação de máquinas para as indústrias alimentares, das bebidas e do tabaco	|	Manufacture of machinery for food, beverage and tobacco processing	|
|	29540	|	Fabricação de máquinas para as indústrias têxtil, do vestuário e do couro	|	Manufacture of machinery for textile, apparel and leather production	|
|	29550	|	Fabricação de máquinas para as indústrias do papel e do cartão	|	Manufacture of machinery for paper and paperboard production	|
|	29561	|	Fabricação de máquinas para as indústrias de materiais de construção, cerâmica e vidro	|	Manufacture of machinery for construction, ceramics and glass	|
|	29562	|	Fabricação de máquinas para as indústrias da borracha e do plástico	|	Manufacture of machinery for rubber or plastics industry	|
|	29563	|	Fabricação de moldes metálicos	|	Manufacture of metal moulds	|
|	29564	|	Fabricação de outras máquinas diversas para uso específico, n.e.	|	Manufacture of other miscellaneous special purpose machinery, n.e.c.	|
|	29601	|	Fabricação de armas de caça, de desporto e defesa	|	Manufacture of hunting, sporting or protective firearms and ammunition	|
|	29602	|	Fabricação de armamento	|	Manufacture of armament	|
|	29710	|	Fabricação de electrodomésticos	|	Manufacture of electric domestic appliances	|
|	29720	|	Fabricação de aparelhos não eléctricos para uso doméstico	|	Manufacture of non-electric domestic appliances	|
|	30010	|	Fabricação de máquinas de escritório	|	Manufacture of office machinery	|
|	30020	|	Fabricação de computadores e de outro equipamento informático	|	Manufacture of computers and other information processing equipment	|
|	31100	|	Fabricação de motores, geradores e transformadores eléctricos	|	Manufacture of electric motors, generators and transformers	|
|	31201	|	Fabricação de aparelhagem e equipamento para instalações eléctricas de alta tensão	|	Manufacture of equipment for high-voltage electrical installations	|
|	31202	|	Fabricação de aparelhagem e equipamento para instalações eléctricas de baixa tensão	|	Manufacture of equipment for low-voltage electrical installations	|
|	31300	|	Fabricação de fios e cabos isolados	|	Manufacture of insulated wire and cable	|
|	31400	|	Fabricação de acumuladores e de pilhas eléctricas	|	Manufacture of accumulators, primary cells and primary batteries	|
|	31500	|	Fabricação de lâmpadas eléctricas e de outro material de iluminação	|	Manufacture of lighting equipment and electric lamps	|
|	31610	|	Fabricação de equipamento eléctrico para motores e veículos	|	Manufacture of electrical equipment for engines and vehicles n.e.c.	|
|	31620	|	Fabricação de outro equipamento eléctrico, n.e.	|	Manufacture of other electrical equipment n.e.c.	|
|	32100	|	Fabricação de componentes electrónicos	|	Manufacture of electronic components	|
|	32200	|	Fabricação de aparelhos emissores de radio e de televisão e aparelhos de telefonia e telegrafia por fios	|	Manufacture of television and radio transmitters and apparatus for line telephony and line telegraphy	|
|	32300	|	Fabricação de aparelhos receptores e material de radio e de televisão, aparelhos de gravação ou de reprodução de som e imagens e de material associado	|	Manufacture of television and radio receivers, sound or video recording or reproducing apparatus and associated goods	|
|	33101	|	Fabricação de equipamento e aparelhos medico-cirúrgicos e de electromedicina	|	Manufacture of medical and surgical equipment and electro-diagnostic apparatus	|
|	33102	|	Fabricação de material ortopédico e próteses	|	Manufacture of medical orthopaedic appliances, artificial limbs and other artificial parts of the body	|
|	33201	|	Fabricação de contadores de electricidade, gás, água e de outros líquidos	|	Manufacture of instruments for measuring electricity, gas  water and other fluid	|
|	33202	|	Fabricação de instrumentos de desenho e de cálculo	|	Manufacture of drawing, marking-out or mathematical calculating instruments	|
|	33203	|	Fabricação de instrumentos e aparelhos de medida, verificação, controlo, navegação e outros fins, n.e.	|	Manufacture of instruments and appliances for measuring, checking, testing, navigating and other purposes, n.e.c.	|
|	33300	|	Fabricação de equipamento de controlo de processos industriais	|	Manufacture of industrial process control equipment	|
|	33401	|	Fabricação de material óptico oftálmico	|	Manufacture of optical ophthalmic instruments	|
|	33402	|	Fabricação de material óptico não oftálmico	|	Manufacture of optical non-ophthalmic instruments 	|
|	33403	|	Fabricação de material fotográfico e cinematográfico	|	Manufacture of photographic and cinematographic equipment	|
|	33500	|	Fabricação de relógios e material de relojoaria	|	Manufacture of watches and clocks	|
|	34100	|	Fabricação de veículos automóveis	|	Manufacture of motor vehicles	|
|	34200	|	Fabricação de carroçarias, reboques e semi-reboques	|	Manufacture of bodies (coachwork) for motor vehicles	|
|	34300	|	Fabricação de componentes e acessórios para veículos automóveis e seus motores	|	Manufacture of parts and accessories for motor vehicles and their engines	|
|	35111	|	Construção e reparação de embarcações metálicas, excepto de recreio e desporto	|	Building and repairing of metal ships, except pleasure and sporting boats	|
|	35112	|	Construção de embarcações não metálicas, excepto de recreio e desporto	|	Building of non-metal ships, except pleasure and sporting boats	|
|	35120	|	Construção e reparação de embarcações de recreio e de desporto	|	Building and repairing of pleasure and sporting boats	|
|	35200	|	Fabricação e reparação de material circulante para caminhos de ferro	|	Manufacture of railway and tramway locomotives and rolling stock	|
|	35300	|	Fabricação de aeronaves e de veículos espaciais	|	Manufacture of aircraft and spacecraft	|
|	35410	|	Fabricação de motociclos	|	Manufacture of motorcycles	|
|	35420	|	Fabricação de bicicletas	|	Manufacture of bicycles	|
|	35430	|	Fabricação de veículos para inválidos	|	Manufacture of invalid carriages	|
|	35500	|	Fabricação de outro material de transporte, n.e.	|	Manufacture of other transport equipment n.e.c.	|
|	36110	|	Fabricação de cadeiras e assentos	|	Manufacture of chairs and seats	|
|	36120	|	Fabricação de mobiliário para escritório e comércio	|	Manufacture of office and shop furniture	|
|	36130	|	Fabricação de mobiliário de cozinha	|	Manufacture of kitchen furniture	|
|	36141	|	Fabricação de mobiliário de madeira para outros fins	|	Manufacture of wooden furniture for other purposes	|
|	36142	|	Fabricação de mobiliário metálico para outros fins	|	Manufacture of metal furniture for other purposes	|
|	36143	|	Fabricação de mobiliário de outros materiais para outros fins	|	Manufacture of furniture of other material for other purposes	|
|	36150	|	Fabricação de colchoaria	|	Manufacture of mattresses	|
|	36210	|	Cunhagem de moedas	|	Striking of coins	|
|	36221	|	Fabricação de filigranas	|	Manufacture of filigree	|
|	36222	|	Fabricação de artigos de joalharia e de outros artigos de ourivesaria	|	Manufacture of jewellery and related articles	|
|	36223	|	Trabalho de diamantes e de outras pedras preciosas ou semi-preciosas para joalharia e uso industrial	|	Working of diamonds and of other precious or semi-precious stones for jewellery and industrial use	|
|	36300	|	Fabricação de instrumentos musicais	|	Manufacture of musical instruments	|
|	36400	|	Fabricação de artigos de desporto	|	Manufacture of sports goods	|
|	36500	|	Fabricação de jogos e de brinquedos	|	Manufacture of games and toys	|
|	36610	|	Fabricação de bijuterias	|	Manufacture of imitation jewellery	|
|	36620	|	Fabricação de vassouras, escovas e pincéis	|	Manufacture of brooms and brushes	|
|	36631	|	Fabricação de linóleo e de outros revestimentos rígidos para o chão	|	Manufacture of linoleum and others hard surface floor coverings	|
|	36632	|	Fabricação de canetas, lápis e similares	|	Manufacture of pens, pencils and related articles	|
|	36633	|	Fabricação de fechos de correr, botões e similares	|	Manufacture of slide fasteners, buttons and related articles	|
|	36634	|	Fabricação de guarda-sóis e chapéus de chuva	|	Manufacture of parasols and umbrellas	|
|	36635	|	Fabricação de fósforos e outros produtos de ignição	|	Manufacture of matches and other ignition products	|
|	36636	|	Outras indústrias transformadoras diversas, n.e.	|	Other miscellaneous  manufacturing activities, n.e.c.	|
|	37100	|	Reciclagem de sucata e de desperdícios metálicos	|	Recycling of metal waste and scrap	|
|	37200	|	Reciclagem de desperdícios não metálicos	|	Recycling of non-metal waste and scrap	|
|	40110	|	Produção de electricidade	|	Production of electricity	|
|	40120	|	Transporte de electricidade	|	Transmission of electricity	|
|	40130	|	Distribuição e comércio de electricidade	|	Distribution and trade of electricity	|
|	40210	|	Produção de gás	|	Manufacture of gas	|
|	40220	|	Distribuição e comércio de combustíveis gasosos por conduta	|	Distribution and trade of gaseous fuels through mains	|
|	40301	|	Produção e distribuição de vapor e de água quente	|	Production and distribution of steam and hot water supply	|
|	40302	|	Produção de gelo	|	Production of ice	|
|	41000	|	Captação, tratamento  e distribuição de água	|	Water collection, treatment and supply	|
|	45110	|	Demolição e terraplanagens	|	Demolition and wrecking of buildings	|
|	45120	|	Perfurações e sondagens	|	Test drilling and boring	|
|	45211	|	Construção de edifícios	|	Construction of buildings 	|
|	45212	|	Construção e engenharia civil	|	Construction and civil engineering	|
|	45220	|	Construção de coberturas	|	Erection of roof covering and frames	|
|	45230	|	Construção de auto-estradas, estradas, vias férreas, aeroportos e instalações desportivas	|	Construction of motorways, roads, railways, airfields and sport facilities	|
|	45240	|	Engenharia hidráulica	|	Construction of water projects	|
|	45250	|	Outras obras especializadas de construção	|	Other construction work involving special trades	|
|	45310	|	Instalação eléctrica	|	Electrical installation	|
|	45320	|	Obras de isolamento	|	Insulation work activities	|
|	45330	|	Instalação de canalizações e de climatização	|	Plumbing, heat and air-conditioning installation	|
|	45340	|	Instalações, n.e.	|	Other building installation	|
|	45410	|	Estucagem	|	Plastering	|
|	45420	|	Montagem de trabalhos de carpintaria e de caixilharia	|	Joinery installation	|
|	45430	|	Revestimento de pavimentos e de paredes	|	Floor and wall covering	|
|	45440	|	Pintura e colocação de vidros	|	Painting and glazing	|
|	45450	|	Actividades de acabamento, n.e.	|	Other building completion	|
|	45500	|	Aluguer de equipamento de construção e de demolição, com operador	|	Renting of construction or demolition equipment with operator	|
|	50100	|	Comércio de veículos automóveis	|	Sale of motor vehicles	|
|	50200	|	Manutenção e reparação de veículos automóveis	|	Maintenance and repair of motor vehicles	|
|	50300	|	Comércio de peças e acessórios para veículos automóveis	|	Sale of motor vehicle parts and accessories	|
|	50401	|	Comércio por grosso e a retalho de motociclos, de suas peças e acessórios	|	Wholesale and retail of motorcycles and related parts and accessories	|
|	50402	|	Manutenção e reparação de motociclos, de suas peças e acessórios	|	Maintenance and repair of motorcycles and related parts and accessories	|
|	50500	|	Comércio a retalho de combustível para veículos a motor	|	Retail sale of automotive fuel	|
|	51110	|	Agentes do comércio por grosso de matérias-primas agrícolas e têxteis, animais vivos e produtos semi-acabados	|	Agents involved in the sale of agricultural raw materials, live animals, textile raw materials and semi-finished goods	|
|	51120	|	Agentes do comércio por grosso de combustíveis, minérios, metais e de produtos químicos para a indústria	|	Agents involved in the sale of fuels, ores, metals and industrial chemicals	|
|	51130	|	Agentes do comércio por grosso de madeira e materiais de construção	|	Agents involved in the sale of timber and building materials	|
|	51140	|	Agentes do comércio por grosso de máquinas, equipamento industrial, embarcações e aeronaves	|	Agents involved in the sale of machinery, industrial equipment, ships and aircraft	|
|	51150	|	Agentes do comércio por grosso de mobiliário, artigos para uso doméstico e ferragens	|	Agents involved in the sale of furniture, household goods, hardware and ironmongery	|
|	51160	|	Agentes do comércio por grosso de têxteis, vestuário, calçado e artigos de couro	|	Agents involved in the sale of textiles, clothing, fur, footwear and leather goods	|
|	51170	|	Agentes do comércio por grosso de produtos alimentares, bebidas e tabaco	|	Agents involved in the sale of food, beverages and tobacco	|
|	51180	|	Agentes especializados do comércio por grosso de produtos, n.e.	|	Agents specializing in the sale of particular products or ranges of products n.e.c.	|
|	51190	|	Agentes do comércio por grosso misto sem predominância	|	Agents involved in the sale of a variety of goods	|
|	51211	|	Comércio por grosso de cereais, sementes, leguminosas e oleaginosas	|	Wholesale of grain, seed, grain legume and oleaginous	|
|	51212	|	Comércio por grosso de alimentos para animais	|	Wholesale of animal feeds	|
|	51220	|	Comércio por grosso de flores e plantas	|	Wholesale of flowers and plants	|
|	51230	|	Comércio por grosso de animais vivos	|	Wholesale of live animals	|
|	51240	|	Comércio por grosso de peles e couro	|	Wholesale of hides, skins and leather	|
|	51250	|	Comércio por grosso de tabaco em bruto	|	Wholesale of ummanufactured tobacco	|
|	51311	|	Comércio por grosso de fruta e de produtos hortícolas, excepto batata	|	Wholesale of fruit and vegetables, except potatoes	|
|	51312	|	Comércio por grosso de batata	|	Wholesale of potatoes	|
|	51320	|	Comércio por grosso de carne e produtos à base de carne	|	Wholesale of meat and meat products	|
|	51331	|	Comércio por grosso de leite, seus derivados e ovos	|	Wholesale of dairy produce and eggs	|
|	51332	|	Comércio por grosso de azeite, óleos e gorduras alimentares	|	Wholesale of olive oil, edible oils and fats	|
|	51341	|	Comércio por grosso de bebidas alcoólicas	|	Wholesale of alcoholic beverages	|
|	51342	|	Comércio por grosso de bebidas não alcoólicas	|	Wholesale of non-alcoholic beverages	|
|	51350	|	Comércio por grosso de tabaco	|	Wholesale of tobacco products	|
|	51361	|	Comércio por grosso de açúcar	|	Wholesale of sugar	|
|	51362	|	Comércio por grosso de chocolate e de produtos de confeitaria	|	Wholesale of chocolate and sugar confectionery	|
|	51370	|	Comércio por grosso de café, chá, cacau e especiarias	|	Wholesale of coffee, tea, cocoa and spices	|
|	51381	|	Comércio por grosso de peixe, crustáceos e moluscos	|	Wholesale of fish, crustaceans and molluscs	|
|	51382	|	Comércio por grosso de outros produtos alimentares, n.e.	|	Wholesale of other food, n.e.c.	|
|	51390	|	Comércio por grosso não especializado de produtos alimentares, bebidas e tabaco	|	Non-specialised wholesale of food, beverages and tobacco	|
|	51410	|	Comércio por grosso de têxteis	|	Wholesale of textiles	|
|	51421	|	Comércio por grosso de vestuário e de acessórios	|	Wholesale of clothing and clothing accessories	|
|	51422	|	Comércio por grosso de calçado	|	Wholesale of footwear	|
|	51430	|	Comércio por grosso de electrodomésticos, aparelhos de rádio e de televisão	|	Wholesale of electrical household appliances	|
|	51441	|	Comércio por grosso de cutelaria, de louças em cerâmica e em vidro	|	Wholesale of cutlery, china and glassware	|
|	51442	|	Comércio por grosso de papeis de parede e de produtos de limpeza	|	Wholesale of wallpaper and cleaning materials	|
|	51450	|	Comércio por grosso de perfumes e de produtos de higiene	|	Wholesale of perfume and cosmetics	|
|	51460	|	Comércio por grosso de produtos farmacêuticos	|	Wholesale of pharmaceutical goods	|
|	51471	|	Comércio por grosso de artigos de papelaria	|	Wholesale of stationery	|
|	51472	|	Comércio por grosso de livros, revistas e jornais	|	Wholesale of books, magazines and newspapers	|
|	51473	|	Comércio por grosso de brinquedos, jogos e artigos de desporto	|	Wholesale of toys, games and sports goods	|
|	51474	|	Comércio por grosso de móveis e de artigos de mobiliário para uso doméstico, carpetes e revestimentos similares para o chão	|	Wholesale of furniture and household furniture goods, carpets and other similar floor coverings	|
|	51475	|	Outro comércio por grosso de bens de consumo, n.e.	|	Wholesale of other household goods, n.e.c.	|
|	51510	|	Comércio por grosso de combustíveis sólidos, líquidos,  gasosos e produtos derivados	|	Wholesale of solid, liquid and gaseous fuels and related products	|
|	51520	|	Comércio por grosso de minérios e de metais	|	Wholesale of metals and metal ores	|
|	51531	|	Comércio por grosso de madeira em bruto e de produtos derivados	|	Wholesale of wood in the rough and related products	|
|	51532	|	Comércio por grosso de materiais de construção (excepto madeira) e equipamento sanitário	|	Wholesale of construction materials (except wood) and sanitary equipment	|
|	51540	|	Comércio por grosso de ferragens, ferramentas manuais e artigos para canalizações e aquecimento	|	Wholesale of hardware, plumbing and heating equipment and supplies	|
|	51550	|	Comércio por grosso de produtos químicos	|	Wholesale of chemical products	|
|	51561	|	Comércio por grosso de fibras têxteis naturais, artificiais e sintéticas	|	Wholesale of natural and man-made textile fibres	|
|	51562	|	Comércio por grosso de cortiça em bruto	|	Wholesale of cork in the rough	|
|	51563	|	Comércio por grosso de outros bens intermédios (não agrícolas), n.e.	|	Wholesale of other (non-agricultural) intermediate products, n.e.c.	|
|	51571	|	Comércio por grosso de sucatas e de desperdícios metálicos	|	Wholesale of metal waste and scrap 	|
|	51572	|	Comércio por grosso de desperdícios têxteis, de cartão e papéis velhos	|	Wholesale of textile, cardboard and paper waste	|
|	51573	|	Comércio por grosso de desperdícios de materiais, n.e.	|	Wholesale of material waste, n.e.c.	|
|	51810	|	Comércio por grosso de máquinas-ferramentas	|	Wholesale of machine tools	|
|	51820	|	Comércio por grosso de máquinas para a indústria extractiva, construção e engenharia civil	|	Wholesale of mining, construction and civil engineering machinery	|
|	51830	|	Comércio por grosso de máquinas para a indústria têxtil, máquinas de costura e de tricotar	|	Wholesale of machinery for the textile industry and of sewing and knitting machines	|
|	51840	|	Comércio por grosso de computadores, equipamentos periféricos e programas informáticos	|	Wholesale of computers, computer peripheral equipment and software	|
|	51850	|	Comércio por grosso de outras máquinas e material de escritório	|	Wholesale of other office machinery and equipment	|
|	51860	|	Comércio por grosso de outros componentes e equipamentos electrónicos	|	Wholesale of other electronic components and equipment	|
|	51870	|	Comércio por grosso de outras máquinas e equipamentos para a indústria, comércio e navegação	|	Wholesale of other machinery for use in industry, trade and navigation	|
|	51880	|	Comércio por grosso de máquinas agrícolas e outros equipamentos agrícolas	|	Wholesale of agricultural machinery and accessories and implements, including tractors	|
|	51900	|	Comércio por grosso, n.e.	|	Other wholesale	|
|	52111	|	Comércio a retalho em supermercados e hipermercados	|	Retail sale in supermarkets and hypermarkets	|
|	52112	|	Comércio a retalho em outros estabelecimentos não especializados, com predominância de produtos alimentares, bebidas ou tabaco	|	Retail sale in others non-specialised stores with food, beverages or tobacco predominating	|
|	52120	|	Comércio a retalho em  outros estabelecimentos não especializados, sem predominância de produtos alimentares, bebidas ou tabaco	|	Other retail sale in non-specialised stores	|
|	52210	|	Comércio a retalho de fruta e de produtos hortícolas	|	Retail sale of fruit and vegetables	|
|	52220	|	Comércio a retalho de carne e de produtos a base de carne	|	Retail sale of meat and meat products	|
|	52230	|	Comércio a retalho de peixe, crustáceos e moluscos	|	Retail sale of fish, crustaceans and molluscs	|
|	52240	|	Comércio a retalho de pão, produtos de pastelaria e de confeitaria	|	Retail sale of bread, cakes, flour confectionery and sugar confectionery	|
|	52250	|	Comércio a retalho de bebidas	|	Retail sale of alcoholic and other beverages	|
|	52260	|	Comércio a retalho de tabaco	|	Retail sale of tobacco products	|
|	52271	|	Comércio a retalho de leite e de derivados	|	Retail sale of dairy produce	|
|	52272	|	Outro comércio a retalho de produtos alimentares, em estabelecimentos especializados, n.e.	|	Other retail sale of food in specialised stores, n.e.c.	|
|	52310	|	Comércio a retalho de produtos farmacêuticos (farmácias)	|	Dispensing chemists	|
|	52320	|	Comércio a retalho de artigos médicos e ortopédicos	|	Retail sale of medical and orthopaedic goods	|
|	52330	|	Comércio a retalho de produtos cosméticos e de higiene	|	Retail sale of cosmetic and toilet articles	|
|	52410	|	Comércio a retalho de têxteis	|	Retail sale of textiles	|
|	52421	|	Comércio a retalho de vestuário para adultos	|	Retail sale of adults' clothing	|
|	52422	|	Comércio a retalho de vestuário para bebes e crianças	|	Retail sale of children's and infants' clothing	|
|	52431	|	Comércio a retalho de calçado	|	Retail sale of footwear 	|
|	52432	|	Comércio a retalho de marroquinaria e artigos de viagem	|	Retail sale of handbags and luggage 	|
|	52441	|	Comércio a retalho de mobiliário e artigos de iluminação	|	Retail sale of furniture and lighting equipment 	|
|	52442	|	Comércio a retalho de louças, cutelaria e de outros artigos similares para uso doméstico	|	Retail sale of tableware, cutlery and other similar household articles 	|
|	52443	|	Comércio a retalho de têxteis para o lar	|	Retail sale of household textiles 	|
|	52444	|	Comércio a retalho de outros artigos para o lar, n.e.	|	Retail sale of other household articles, n.e.c.	|
|	52451	|	Comércio a retalho de electrodomésticos, aparelhos de radio, de televisão e vídeo	|	Retail sale of electrical household appliances and radio and television goods	|
|	52452	|	Comércio a retalho de instrumentos musicais, discos, cassetes e produtos similares	|	Retail sale of musical instruments, records and audio/visual tapes, CD, DVD and cassettes	|
|	52461	|	Comércio a retalho de ferragens e de vidro plano	|	Retail sale of hardware and flat glass 	|
|	52462	|	Comércio a retalho de tintas, vernizes e produtos similares	|	Retail sale of paints, varnishes and similar products	|
|	52463	|	Comércio a retalho de material de bricolage, equipamento sanitário, ladrilhos e materiais similares	|	Retail sale of do-it-yourself material, sanitary equipment, floor tile and similar equipment	|
|	52471	|	Comércio a retalho de livros	|	Retail sale of books 	|
|	52472	|	Comércio a retalho de artigos de papelaria, jornais e revistas	|	Retail sale of stationery, newspapers and magazines	|
|	52481	|	Comércio a retalho de máquinas e de outro material de escritório	|	Retail sale of office machinery and other equipment 	|
|	52482	|	Comércio a retalho de material óptico, fotográfico, cinematográfico e de instrumentos de precisão	|	Retail sale of photographic, optical, cinematographic and precision equipment	|
|	52483	|	Comércio a retalho de relógios e de artigos de ourivesaria	|	Retail sale of jewellery, clocks and watches	|
|	52484	|	Comércio a retalho de brinquedos e jogos	|	Retail sale of games and toys 	|
|	52485	|	Comércio a retalho de artigos de desporto, de campismo, caça e de lazer	|	Retail sale of sporting, camping, hunting and recreation equipment 	|
|	52486	|	Comércio a retalho de flores, plantas e sementes para jardim	|	Retail sale of flowers, plants and seeds 	|
|	52487	|	Comércio a retalho de combustíveis para uso doméstico	|	Retail sale of household fuel oil, bottled gas, coal and wood	|
|	52488	|	Comércio a retalho de outros produtos novos, em estabelecimentos especializados, n.e.	|	Other retail sale in specialised stores, n.e.c.	|
|	52500	|	Comércio a retalho de artigos em segunda mão em estabelecimentos	|	Retail sale of second-hand goods in stores	|
|	52610	|	Comércio a retalho por correspondência	|	Retail sale via mail order houses	|
|	52621	|	Comércio a retalho em bancas, feiras e unidades móveis de venda de produtos alimentares e bebidas	|	Retail sale via stalls and markets of food and beverages	|
|	52622	|	Comércio a retalho em bancas, feiras e unidades móveis de venda de vestuário, tecidos, calçado, malas e similares	|	Retail sale via stalls and markets of clothing, textiles, footwear, handbags and similar articles 	|
|	52623	|	Comércio a retalho em bancas, feiras e unidades móveis de venda de outros produtos não alimentares, n.e.	|	Retail sale via stalls and markets of other non-food, n.e.c.	|
|	52630	|	Comércio a retalho por outros métodos, não efectuado em estabelecimentos	|	Other non-store retail sale	|
|	52710	|	Reparação de calçado e de outros artigos de couro	|	Repair of boots, shoes and other articles of leather	|
|	52720	|	Reparação de electrodomésticos	|	Repair of electrical household goods	|
|	52730	|	Reparação de relógios e de artigos de joalharia	|	Repair of watches, clocks and jewellery	|
|	52740	|	Reparação de bens pessoais e domésticos, n.e.	|	Repair n.e.c.	|
|	55111	|	Hotéis com restaurante	|	Hotels with restaurant  	|
|	55112	|	Pensões com restaurante	|	Guest houses with restaurant	|
|	55113	|	Estalagens com restaurante	|	Inns with restaurant	|
|	55114	|	Pousadas com restaurante	|	Lodging-houses with restaurant	|
|	55115	|	Motéis com restaurante	|	Motels with restaurant	|
|	55116	|	Hotéis-Apartamentos com restaurante	|	Apartment-hotels with restaurant	|
|	55117	|	Aldeamentos turísticos com restaurante	|	Holiday villages with restaurant	|
|	55118	|	Apartamentos turísticos com restaurante	|	Holiday flats with restaurant	|
|	55119	|	Estabelecimentos hoteleiros, com restaurante, n.e.	|	Hotel and similar establishments with restaurant, n.e.c.	|
|	55121	|	Hotéis sem restaurante	|	Hotels without restaurant	|
|	55122	|	Pensões sem restaurante	|	Guest houses without restaurant	|
|	55123	|	Apartamentos turísticos sem restaurante	|	Holiday flats without restaurant	|
|	55124	|	Estabelecimentos hoteleiros, sem restaurante, n.e.	|	Hotel and similar establishments without restaurant, n.e.c.	|
|	55210	|	Pousadas de juventude e abrigos de montanha	|	Youth hostels and mountain refuges	|
|	55220	|	Campismo e caravanismo	|	Camping sites, including caravan sites	|
|	55231	|	Colónias de ferias	|	Holiday camps 	|
|	55232	|	Alojamento mobilado para turistas	|	Letting services of short-stay furnished accommodation	|
|	55233	|	Turismo no espaço rural	|	Short-stay lodging in farmhouses 	|
|	55234	|	Outros locais de alojamento de curta duração, n.e.	|	Other short-stay lodging, n.e.c.	|
|	55301	|	Restaurantes tipo tradicional	|	Traditional restaurants 	|
|	55302	|	Restaurantes com lugares ao balcão	|	Snack-bars restaurants	|
|	55303	|	Restaurantes sem serviço de mesa	|	Self-service restaurants 	|
|	55304	|	Restaurantes típicos	|	Typical restaurants 	|
|	55305	|	Restaurantes com local para dança	|	Restaurants with dance floor 	|
|	55306	|	Restaurantes, n.e.	|	Restaurants, n.e.c.	|
|	55401	|	Cafés	|	Cafés	|
|	55402	|	Cervejarias	|	Beerhouse	|
|	55403	|	Bares	|	Bars	|
|	55404	|	Casas de chá e pastelarias	|	Tea and confectionery shops	|
|	55405	|	Outros estabelecimentos de bebidas sem espectáculo	|	Other beverage establishments without entertainment	|
|	55406	|	Estabelecimentos de bebidas com espectáculo	|	Others beverages establishments, with some form of entertainment	|
|	55510	|	Cantinas	|	Canteens	|
|	55520	|	Fornecimento de refeições ao domicílio	|	Catering	|
|	60100	|	Caminhos de ferro	|	Transport via railways	|
|	60211	|	Transportes urbano e local por metropolitano, eléctrico, troleicarro e autocarro	|	Urban and suburban passenger transportation by underground, tramways and  buses	|
|	60212	|	Transporte interurbano em autocarros	|	Inter-urban passenger transportation by bus	|
|	60220	|	Transporte ocasional de passageiros em veículos ligeiros	|	Taxi operation	|
|	60230	|	Outros transportes terrestres  de passageiros	|	Other passenger land transport 	|
|	60240	|	Transportes rodoviários de mercadorias	|	Freight transport by road	|
|	60300	|	Transportes por oleodutos e gasodutos	|	Transport via pipelines	|
|	61101	|	Transporte marítimo não costeiros	|	Sea water transport 	|
|	61102	|	Transporte costeiros e locais	|	Coastal and local water transport	|
|	61200	|	Transportes por vias navegáveis interiores	|	Inland water transport	|
|	62100	|	Transportes aéreos regulares	|	Scheduled air transport	|
|	62200	|	Transportes aéreos não regulares	|	Non-scheduled air transport	|
|	62300	|	Transportes espaciais	|	Space transport	|
|	63110	|	Manuseamento de carga	|	Cargo handling	|
|	63121	|	Armazenagem frigorífica	|	Storage of frozen goods	|
|	63122	|	Armazenagem não frigorífica	|	Storage of non-frozen goods	|
|	63210	|	Outras actividades auxiliares dos transportes terrestres	|	Other supporting land transport activities	|
|	63220	|	Outras actividades auxiliares dos transportes por água	|	Other supporting water transport activities	|
|	63230	|	Outras actividades auxiliares dos transportes aéreos	|	Other supporting air transport activities	|
|	63300	|	Agências de viagens e de turismo e de outras actividades de apoio turístico	|	Activities of travel agencies and tour operators	|
|	63401	|	Organização do transporte	|	Transport organisation	|
|	63402	|	Agentes aduaneiros e similares de apoio ao transporte	|	Activities of customs clearance agents and similars	|
|	64110	|	Actividades dos correios nacionais	|	National post activities	|
|	64120	|	Actividades postais independentes dos correios nacionais	|	Courier activities other than national post activities	|
|	64200	|	Telecomunicações	|	Telecommunications	|
|	65110	|	Banco central	|	Central banking	|
|	65120	|	Outra intermediação monetária	|	Other monetary intermediation	|
|	65210	|	Locação financeira	|	Financial leasing	|
|	65221	|	Sociedades de investimentos	|	Investment companies 	|
|	65222	|	Sociedades de factoring""	|	Factoring companies	|
|	65223	|	Sociedades financeiras para aquisição de credito	|	Credit-purchase financing companies 	|
|	65224	|	Outras actividades de crédito, n.e.	|	Other credit granting n.e.c.	|
|	65230	|	Outra intermediação financeira, n.e.	|	Other financial intermediation n.e.c.	|
|	66011	|	Seguros de vida	|	Life insurance 	|
|	66012	|	Outras actividades complementares de segurança social	|	Other additional activities for social security	|
|	66020	|	Fundos de pensões e regimes profissionais complementares	|	Pension funding	|
|	66030	|	Seguros não vida	|	Non-life insurance	|
|	67110	|	Administração de mercados financeiros	|	Administration of financial markets	|
|	67120	|	Mediação na negociação e gestão de carteiras de activos	|	Security broking and fund management	|
|	67130	|	Actividades auxiliares de intermediação financeira, n.e.	|	Activities auxiliary to financial intermediation n.e.c.	|
|	67200	|	Actividades auxiliares de seguros e de fundos de pensões	|	Activities auxiliary to insurance and pension funding	|
|	70110	|	Promoção imobiliária	|	Development and selling of real estate	|
|	70120	|	Compra e venda de bens imobiliários	|	Buying and selling of own real estate	|
|	70200	|	Arrendamento de bens imobiliários	|	Renting and operating of own or leased real estate	|
|	70310	|	Mediação e avaliação imobiliária	|	Real estate agencies	|
|	70320	|	Administração de imóveis por conta de outrem	|	Management of real estate on behalf of others	|
|	71100	|	Aluguer de veículos automóveis	|	Renting and leasing of motor vehicles	|
|	71210	|	Aluguer de outro meio de transporte terrestre	|	Renting of other land transport equipment	|
|	71220	|	Aluguer de meios de transporte marítimo e fluvial	|	Renting and leasing of water transport equipment	|
|	71230	|	Aluguer de meios de transporte aéreo	|	Renting and leasing of air transport equipment	|
|	71310	|	Aluguer de máquinas e equipamentos agrícolas	|	Renting and leasing of agricultural machinery and equipment	|
|	71320	|	Aluguer de máquinas e equipamentos para a construção e engenharia civil	|	Renting and leasing of construction and civil engineering machinery and equipment	|
|	71330	|	Aluguer de máquinas e equipamentos de escritório (inclui computadores)	|	Renting and leasing of office machinery and equipment (including computers)	|
|	71340	|	Aluguer de máquinas e equipamento, n.e.	|	Renting of other machinery and equipment n.e.c.	|
|	71400	|	Aluguer de bens de uso pessoal e doméstico, n.e.	|	Renting of personal and household goods n.e.c.	|
|	72100	|	Consultoria em equipamento informático	|	Hardware consultancy	|
|	72210	|	Edição de programas informáticos	|	Software publishing	|
|	72220	|	Outras actividades de consultoria em programação informática	|	Other software consultancy and supply	|
|	72300	|	Processamento de dados	|	Data processing	|
|	72400	|	Actividades de bancos de dados e disponibilização de informação em contínuo	|	Database activities	|
|	72500	|	Manutenção e reparação de máquinas de escritório, de contabilidade e de material informático	|	Maintenance and repair of office, accounting and computing machinery	|
|	72600	|	Outras actividades conexas a informática	|	Other computer related activities	|
|	73100	|	Investigação e desenvolvimento das ciências físicas e naturais	|	Research and experimental development on natural sciences and engineering	|
|	73200	|	Investigação e desenvolvimento das ciências sociais e humanas	|	Research and experimental development on social sciences and humanities	|
|	74110	|	Actividades jurídicas	|	Legal activities	|
|	74120	|	Actividades de contabilidade e auditoria	|		|
|	74130	|	Estudos de mercado e sondagens de opinião	|	Market research and public opinion polling	|
|	74140	|	Actividades de consultoria para os negócios e a gestão	|	Management consultancy activities	|
|	74150	|	Actividades das sociedades gestoras de participações sociais	|	Activities of holding companies	|
|	74201	|	Actividades de arquitectura	|	Architectural activities 	|
|	74202	|	Actividades de engenharia e técnicas afins	|	Engineering activities and related technical consultancy	|
|	74300	|	Actividades de ensaios e análises técnicas	|	Technical testing and analysis	|
|	74401	|	Agências de publicidade	|	Advertising agencies	|
|	74402	|	Gestão de suportes publicitários	|	Management of advertising space or time 	|
|	74500	|	Selecção e colocação de pessoal	|	Labour recruitment and provision of personnel	|
|	74600	|	Actividades de investigação e segurança	|	Security and investigation activities	|
|	74700	|	Actividades de limpeza industrial	|	Industrial cleaning	|
|	74810	|	Actividades fotográficas	|	Photographic activities	|
|	74820	|	Actividades de embalagem	|	Packaging activities	|
|	74850	|	Actividades de secretariado, tradução e endereçagem	|	Secretarial and translation activities	|
|	74860	|	Actividades dos centros de chamadas	|	Activities of call centres	|
|	74871	|	Organização de feiras, exposições e de outros eventos	|	Activities of exhibition and fair organisers	|
|	74872	|	Outras actividades de serviços prestados principalmente as empresas diversas, n.e.	|	Other miscellaneous business activities, n.e.c.	|
|	75111	|	Administração central	|	Central government	|
|	75112	|	Administração regional	|	Regional government 	|
|	75113	|	Administração local	|	Local administration	|
|	75121	|	Administração pública - actividades de saúde	|	Regulation of the activities of providing health care	|
|	75122	|	Administração pública - actividades de educação	|	Regulation of the activities of providing education	|
|	75123	|	Administração Pública - actividades da cultura, desporto, recreativas, ambiente, habitação e de outras actividades sociais, excepto segurança social obrigatória	|	Activities of culture, sports, entertainment, environment, housing and other social activities, except compulsory social security	|
|	75130	|	Administração pública - actividades económicas	|	Regulation of and contribution to more efficient operation of businesses	|
|	75140	|	Actividades de apoio ao conjunto da administração pública	|	Supporting service activities for the government as a whole	|
|	75210	|	Negócios estrangeiros	|	Foreign affairs	|
|	75220	|	Actividades de defesa	|	Defence activities	|
|	75230	|	Justiça	|	Justice and judicial activities	|
|	75240	|	Segurança e ordem pública	|	Public security, law and order activities	|
|	75250	|	Actividades de protecção civil	|	Fire service activities	|
|	75300	|	Segurança social (obrigatória)	|	Compulsory social security activities	|
|	80101	|	Educação pré-escolar	|	Pre-primary education	|
|	80102	|	Ensino básico (1º  Ciclo)	|	Primary education (1st. Cycle) 	|
|	80211	|	Ensino básico (2º e 3º ciclos)	|	Basic education (2º and 3º stages)	|
|	80212	|	Ensino secundário geral	|	General secondary education	|
|	80220	|	Ensino secundário técnico e profissional	|	Technical and vocational secondary education	|
|	80300	|	Ensino superior	|	Tertiary education	|
|	80410	|	Escolas de condução e pilotagem	|	Driving school activities	|
|	80421	|	Formação profissional	|	Professional formation	|
|	80422	|	Outras actividades educativas, n.e.	|	Other education activities, n.e.c.	|
|	85110	|	Actividades dos estabelecimentos de saúde com internamento	|	Hospital activities	|
|	85120	|	Actividades de pratica clinica em ambulatório	|	Medical practice activities	|
|	85130	|	Actividades  de medicina dentária e odontologia	|	Dental practice activities	|
|	85141	|	Laboratórios de análises clínicas	|	Laboratories of clinical analyses	|
|	85142	|	Actividades de ambulâncias	|	Activities of ambulances	|
|	85143	|	Actividades de enfermagem	|	Activities of nursing 	|
|	85144	|	Centros de recolha e bancos de órgãos	|	Collection centers and organs banks	|
|	85145	|	Outras actividades de saúde humana, n.e.	|	Other human health activities n.e.c.	|
|	85200	|	Actividades veterinárias	|	Veterinary activities	|
|	85311	|	Acção social para a infância e juventude, com alojamento	|	Social assistance to children and youth, with accommodation	|
|	85312	|	Acção social para pessoas com deficiência, com alojamento	|	Social assistance to persons with some limits on ability for self-care, with accommodation	|
|	85313	|	Acção social para pessoas idosas, com alojamento	|	Social assistance to the aged, with accommodation	|
|	85314	|	Acção social com alojamento, n.e.	|	Social work activities with accommodation, n.e.c.	|
|	85321	|	Acção social para a infância e juventude, sem alojamento	|	Social assistance to children and youth, without accommodation	|
|	85322	|	Acção social para pessoas com deficiência, sem alojamento	|	Social assistance to persons with some limits on ability for self-care, without accommodation	|
|	85323	|	Acção social para pessoas idosas, sem alojamento	|	Social assistance to the aged, without accommodation	|
|	85324	|	Acção social sem alojamento, n.e.	|	Social work activities without accommodation, n.e.c.	|
|	90010	|	Recolha e tratamento de águas residuais	|	Collection and treatment of sewage	|
|	90020	|	Recolha e tratamento de outros resíduos	|	Collection and treatment of other waste	|
|	90030	|	Limpeza pública, despoluição e actividades similares	|	Sanitation, remediation and similar activities	|
|	91110	|	Organizações económicas e patronais	|	Activities of business and employers' organizations	|
|	91120	|	Organizações profissionais	|	Activities of professional organizations	|
|	91200	|	Actividades de organizações sindicais	|	Activities of trade unions	|
|	91310	|	Organizações religiosas	|	Activities of religious organizations	|
|	91320	|	Organizações políticas	|	Activities of political organizations	|
|	91331	|	Associações culturais e recreativas	|	Cultural or recreational associations 	|
|	91332	|	Associações de defesa do ambiente	|	Environmental protection associations	|
|	91333	|	Outras actividades associativas, n.e.	|	Other activities of associations, n.e.c.	|
|	92111	|	Produção de filmes e de vídeos	|	Motion picture and video production	|
|	92112	|	Actividades técnicas de pós-produção	|	Film and video post-production activities	|
|	92120	|	Distribuição de filmes e de vídeos	|	Motion picture and video distribution	|
|	92130	|	Projecção de filmes e de vídeos	|	Motion picture projection activities	|
|	92200	|	Actividades de rádio e de  televisão	|	Programming and broadcasting activities	|
|	92311	|	Actividades de teatro e musicais	|	Live theatrical presentations, concerts and opera or dance productions	|
|	92312	|	Outras actividades artísticas e literárias	|	Others artistic and literary creation	|
|	92320	|	Gestão de salas de espectáculo e actividades conexas	|	Operation of arts facilities	|
|	92330	|	Parques de diversão	|	Fair and amusement park activities	|
|	92341	|	Actividades tauromáquicas	|	Activities bullfighting	|
|	92342	|	Outras actividades de diversão e espectáculo diversas, n.e.	|	Other entertainment activities, n.e.c.	|
|	92400	|	Actividades de agências de notícias	|	News agency activities	|
|	92510	|	Actividades das bibliotecas e arquivos	|	Library and archives activities	|
|	92520	|	Actividades dos museus e conservação de locais e de monumentos históricos	|	Museums activities and preservation of historical sites and buildings	|
|	92530	|	Actividades dos jardins botânicos, zoológicos e das reservas naturais	|	Botanical and zoological gardens and nature reserves activities	|
|	92610	|	Gestão de instalações desportivas	|	Operation of sports facilities	|
|	92620	|	Outras actividades desportivas	|	Other sports activities	|
|	92710	|	Lotarias e outros jogos de aposta	|	Gambling and betting activities	|
|	92720	|	Outras actividades recreativas, n.e.	|	Other recreational activities n.e.c.	|
|	93010	|	Lavagem e limpeza a seco de têxteis e peles	|	Washing and (dry-)cleaning of textile and fur products	|
|	93021	|	Salões de cabeleireiro	|	Hairdressing 	|
|	93022	|	Institutos de beleza	|	Beauty parlours	|
|	93030	|	Actividades funerárias e conexas	|	Funeral and related activities	|
|	93041	|	Termalismo	|	Thermal establishments	|
|	93042	|	Manutenção física, n.e.	|	Physical well-being activities, n.e.c.	|
|	93050	|	Outras actividades de serviços, n.e.	|	Other service activities n.e.c.	|
|	95000	|	Actividades das famílias com empregados domésticos	|	Activities of households as employers of domestic staff	|
|	96000	|	Actividades de produção de bens pelas famílias para uso próprio	|	Undifferentiated goods-producing activities of private households for own use	|
|	97000	|	Actividades de produção de serviços pelas famílias para uso próprio	|	Undifferentiated service-producing activities of private households for own use	|
|	99000	|	Organismos internacionais e outras instituições extra-territoriais	|	Extra-territorial organizations and bodies	|



[Return](#table-of-contents)


## Economic Activities CAE3

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	1111	|	Cerealicultura (excepto arroz)	|	Growing of cereals (except rice)	|
|	1112	|	Cultura de leguminosas secas e sementes oleaginosas	|	Leguminous crops and oil seeds	|
|	1120	|	Cultura de arroz	|	Growing of rice	|
|	1130	|	Culturas de produtos hortícolas, raízes e tubérculos	|	Growing of vegetables and melons, roots and tubers	|
|	1140	|	Cultura de cana-de-açúcar	|	Growing of sugar cane	|
|	1150	|	Cultura de tabaco	|	Growing of tobacco	|
|	1160	|	Cultura de plantas têxteis	|	Growing of fibre crops	|
|	1191	|	Cultura de flores e de plantas ornamentais	|	Growing of flowers and ornamental plants	|
|	1192	|	Outras culturas temporárias, n.e.	|	Growing of other non-perennial crops, n.e.c.	|
|	1210	|	Viticultura	|	Growing of grapes	|
|	1220	|	Cultura de frutos tropicais e subtropicais	|	Growing of tropical and subtropical fruits	|
|	1230	|	Cultura de citrinos	|	Growing of citrus fruits	|
|	1240	|	Cultura de pomóideas e prunóideas	|	Growing of pome fruits and stone fruits	|
|	1251	|	Cultura de frutos de casca rija	|	Growing of nuts	|
|	1252	|	Cultura de outros frutos em árvores e arbustos	|	Growing of other tree and bush fruits 	|
|	1261	|	Olivicultura	|	Growing of olive	|
|	1262	|	Cultura de outros frutos oleaginosos	|	Growing of other oleaginous fruits	|
|	1270	|	Cultura de plantas destinadas à preparação de bebidas	|	Growing of beverage crops	|
|	1280	|	Cultura de especiarias, plantas aromáticas, medicinais e farmacêuticas	|	Growing of spices, aromatic, drug and pharmaceutical crops	|
|	1290	|	Outras culturas permanentes	|	Growing of other perennial crops	|
|	1300	|	Cultura de materiais de propagação vegetativa	|	Plant propagation	|
|	1410	|	Criação de bovinos para produção de leite	|	Raising of dairy cattle	|
|	1420	|	Criação de outros bovinos (excepto para produção de leite) e búfalos	|	Raising of other cattle and buffaloes	|
|	1430	|	Criação de equinos, asininos e muares	|	Raising of horses and other equines	|
|	1440	|	Criação de camelos e camelídeos	|	Raising of camels and camelids	|
|	1450	|	Criação de ovinos e caprinos	|	Raising of sheep and goats	|
|	1460	|	Suinicultura	|	Raising of swine/pigs	|
|	1470	|	Avicultura	|	Raising of poultry	|
|	1491	|	Apicultura	|	Beekeeping	|
|	1492	|	Cunicultura	|	Rabbit	|
|	1493	|	Criação de animais de companhia	|	Breeding company	|
|	1494	|	Outra produção animal, n.e.	|	Raising of other animals, n.e.c.	|
|	1500	|	Agricultura e produção animal combinadas	|	Mixed farming	|
|	1610	|	Actividades dos serviços relacionados com a agricultura	|	Support activities for crop production	|
|	1620	|	Actividades dos serviços relacionados com a produção animal, excepto serviços de veterinária	|	Support activities for animal production	|
|	1630	|	Preparação de produtos agrícolas para venda 	|	Post-harvest crop activities	|
|	1640	|	Preparação e tratamento de sementes para propagação	|	Seed processing for propagation	|
|	1701	|	Caça e repovoamento cinegético	|	Hunting and trapping	|
|	1702	|	Actividades dos serviços relacionados com a caça e repovoamento cinegético	|	Service activities related to hunting and trapping	|
|	2100	|	Silvicultura e outras actividades florestais	|	Silviculture and other forestry activities	|
|	2200	|	Exploração florestal	|	Logging	|
|	2300	|	Extracção de cortiça, resina e apanha de outros produtos florestais, excepto madeira	|	Gathering of wild growing non-wood products	|
|	2400	|	Actividades dos serviços relacionados com a silvicultura e exploração florestal	|	Support services to forestry	|
|	3111	|	Pesca marítima	|	Marine fishing	|
|	3112	|	Apanha de algas e de outros produtos do mar	|	Collecting seaweed and other sea products	|
|	3121	|	Pesca em águas interiores	|	Fishing in inland waters	|
|	3122	|	Apanha de produtos de águas interiores	|	Collecting inland water products	|
|	3210	|	Aquicultura em águas salgadas e salobras	|	Marine aquaculture	|
|	3220	|	Aquicultura em águas doces	|	Freshwater aquaculture	|
|	5100	|	Extracção de hulha (inclui antracite)	|	Mining of hard coal	|
|	5200	|	Extracção de lenhite	|	Mining of lignite	|
|	6100	|	Extracção de petróleo bruto	|	Extraction of crude petroleum	|
|	6200	|	Extracção de gás natural	|	Extraction of natural gas	|
|	6430	|	Trusts, fundos e  entidades financeiras similares	|	Trusts, funds and similar financial entities	|
|	7100	|	Extracção e preparação de minérios de ferro	|	Mining of iron ores	|
|	7210	|	Extracção e preparação de minérios de urânio e de tório	|	Mining of uranium and thorium ores	|
|	7290	|	Extracção e preparação de outros minérios metálicos não ferrosos	|	Mining of other non-ferrous metal ores	|
|	8111	|	Extracção de mármore e outras rochas carbonatadas	|	Quarrying of marble and other carbonated stones	|
|	8112	|	Extracção de granito ornamental e rochas similares	|	Quarrying of ornamental granite and similar stones	|
|	8113	|	Extracção de calcário e cré	|	Quarrying of limestone and chalk	|
|	8114	|	Extracção de gesso	|	Quarrying of gypsum	|
|	8115	|	Extracção de ardósia	|	Quarrying of slate	|
|	8121	|	Extracção de saibro, areia e pedra britada	|	Operation of gravel and sand pits	|
|	8122	|	Extracção de argilas e caulino	|	Mining of clays and kaolin	|
|	8910	|	Extracção de minerais para a indústria química e para a fabricação de adubos	|	Mining of chemical and fertiliser minerals	|
|	8920	|	Extracção da turfa	|	Extraction of peat	|
|	8931	|	Extracção de sal marinho	|	Extraction of sea salt	|
|	8932	|	Extracção de sal gema	|	Extraction of rock salt	|
|	8991	|	Extracção de feldspato	|	Quarrying of feldspar	|
|	8992	|	Extracção de outros minerais não metálicos, n.e.	|	Quarrying of other non-metallic mineral products, n.e.c.	|
|	9100	|	Actividades dos serviços relacionados com a extracção de petróleo e gás, excepto a prospecção	|	Support activities for petroleum and natural gas extraction	|
|	9900	|	Outras actividades dos serviços relacionados com as indústrias extractivas	|	Support activities for other mining and quarrying	|
|	10110	|	Abate de gado (produção de carne)	|	Processing and preserving of meat	|
|	10120	|	Abate de aves (produção de carne)	|	Processing and preserving of poultry meat	|
|	10130	|	Fabricação de produtos à base de carne	|	Production of meat and poultry meat products	|
|	10201	|	Preparação de produtos da pesca e da aquicultura	|	Preparation of fish and fish products	|
|	10202	|	Congelação de produtos da pesca e da aquicultura	|	Freezing of fish and fish products	|
|	10203	|	Conservação de produtos da pesca e da aquicultura em azeite e outros óleos vegetais e outros molhos	|	Preserving of fish and fish products in olive oil and other vegetable oil and other sauces	|
|	10204	|	Salga, secagem e outras actividades de transformação de produtos da pesca e aquicultura	|	Drying, salting and other fish processing and preserving	|
|	10310	|	Preparação e conservação de batatas	|	Processing and preserving of potatoes	|
|	10320	|	Fabricação de sumos de frutos e de produtos hortícolas	|	Manufacture of fruit and vegetable juice	|
|	10391	|	Congelação de frutos e de produtos hortícolas	|	Freezing of fruit and vegetables	|
|	10392	|	Secagem e desidratação de frutos e de produtos hortícolas	|	Drying and dehydration of fruit and vegetables	|
|	10393	|	Fabricação de doces, compotas, geleias e marmelada	|	Manufacture of jams, marmalades and table jellies	|
|	10394	|	Descasque e transformação de frutos de casca rija comestíveis	|	Peeling and processing of edible nuts	|
|	10395	|	Preparação e conservação de frutos e de produtos hortícolas por outros processos	|	Preparation and preserving of fruit and vegetables, n.e.c.	|
|	10411	|	Produção de óleos e gorduras animais brutos	|	Manufacture of crude animal oils and fats	|
|	10412	|	Produção de azeite	|	Production of olive oil	|
|	10413	|	Produção de óleos vegetais brutos (excepto azeite)	|	Production of crude vegetable oils (except olive oil)	|
|	10414	|	Refinação de azeite, óleos e gorduras	|	Manufacture of olive oil, refined oils and fats	|
|	10420	|	Fabricação de margarinas e de gorduras alimentares similares	|	Manufacture of margarine and similar edible fats	|
|	10510	|	Indústrias do leite e derivados	|	Operation of dairies and cheese making	|
|	10520	|	Fabricação de gelados e sorvetes	|	Manufacture of ice cream	|
|	10611	|	Moagem de cereais	|	Grain milling	|
|	10612	|	Descasque, branqueamento e outros tratamentos do arroz	|	Husking, whitening and other treatment of rice	|
|	10613	|	Transformação de cereais e leguminosas, n.e.	|	Manufacture of grain mill products, n.e.c.	|
|	10620	|	Fabricação de amidos, féculas e produtos afins	|	Manufacture of starches and starch products	|
|	10711	|	Panificação	|	Manufacture of bread	|
|	10712	|	Pastelaria	|	Manufacture of fresh pastry goods and cakes	|
|	10720	|	Fabricação de bolachas, biscoitos, tostas e pastelaria de conservação	|	Manufacture of rusks and biscuits	|
|	10730	|	Fabricação de massas alimentícias, cuscuz e similares	|	Manufacture of macaroni, noodles, couscous and similar farinaceous products	|
|	10810	|	Indústria do açúcar	|	Manufacture of sugar	|
|	10821	|	Fabricação de cacau e de chocolate	|	Manufacture of cocoa and chocolate	|
|	10822	|	Fabricação de produtos de confeitaria	|	Manufacture of sugar confectionery	|
|	10830	|	Indústria do café e do chá	|	Processing of tea and coffee	|
|	10840	|	Fabricação de condimentos e temperos	|	Manufacture of condiments and seasonings	|
|	10850	|	Fabricação de refeições e pratos pré-cozinhados	|	Manufacture of prepared meals and dishes	|
|	10860	|	Fabricação de alimentos homogeneizados e dietéticos	|	Manufacture of homogenised food preparations and dietetic food	|
|	10891	|	Fabricação de fermentos, leveduras e adjuvantes para panificação e pastelaria	|	Manufacture of starters, yeast and adjuvants for breadmaking and pastry	|
|	10892	|	Fabricação de caldos, sopas e sobremesas	|	Manufacture of broths, soups and desserts	|
|	10893	|	Fabricação de outros produtos alimentares diversos, n.e.	|	Manufacture of other miscellaneous food products n.e.c.	|
|	10911	|	Fabricação de pré-misturas	|	Manufacture of premixes	|
|	10912	|	Fabricação de alimentos para animais de criação (excepto para aquicultura)	|	Manufacture of prepared feeds for farm animals (except for aquaculture)	|
|	10913	|	Fabricação de alimentos para aquicultura	|	Manufacture of prepared feeds for aquaculture	|
|	10920	|	Fabricação de alimentos para animais de companhia	|	Manufacture of prepared pet foods	|
|	11011	|	Fabricação de aguardentes preparadas	|	Manufacture of prepared spirits	|
|	11012	|	Fabricação de aguardentes não preparadas	|	Manufacture of non-prepared spirits	|
|	11013	|	Produção de licores e de outras bebidas destiladas	|	Manufacture of liqueurs and other distilled alcoholic beverages	|
|	11021	|	Produção de vinhos comuns e licorosos	|	Manufacture of ordinary and liqueur wine	|
|	11022	|	Produção de vinhos espumantes e espumosos	|	Manufacture of sparkling wine	|
|	11030	|	Fabricação de cidra e outras bebidas fermentadas de frutos	|	Manufacture of cider and other fruit wines	|
|	11040	|	Fabricação de vermutes e de outras bebidas fermentadas não destiladas	|	Manufacture of other non-distilled fermented beverages	|
|	11050	|	Fabricação de cerveja	|	Manufacture of beer	|
|	11060	|	Fabricação de malte	|	Manufacture of malt	|
|	11071	|	Engarrafamento de águas minerais naturais e de nascente	|	Bottling of natural mineral and spring waters 	|
|	11072	|	Fabricação de refrigerantes e de outras bebidas não alcoólicas, n.e.	|	Production of soft drinks and other non-alcoholic flavoured and/or sweetened waters, n.e.c.	|
|	12000	|	Preparação de tabaco	|	Preparation of tobacco	|
|	13101	|	Preparação e fiação de fibras do tipo algodão	|	Preparation and spinning of cotton-type fibres	|
|	13102	|	Preparação e fiação de fibras do tipo lã	|	Preparation and spinning of woollen-type fibres	|
|	13103	|	Preparação e fiação da seda e preparação e texturização de filamentos sintéticos e artificiais	|	Throwing and preparation of silk, including from noils, and throwing and texturing of synthetic or artificial filament yarns	|
|	13104	|	Fabricação de linhas de costura	|	Manufacture of sewing threads	|
|	13105	|	Preparação e fiação de linho e de outras fibras têxteis	|	Preparation and spinning of flax-type fibres and other textile fibres	|
|	13201	|	Tecelagem de fio do tipo algodão	|	Cotton-type weaving	|
|	13202	|	Tecelagem de fio do tipo lã	|	Woollen-type weaving	|
|	13203	|	Tecelagem de fio do tipo seda e de outros têxteis	|	Silk-type and other textile weaving	|
|	13301	|	Branqueamento e tingimento	|	Bleaching and dyeing	|
|	13302	|	Estampagem	|	Printing services of textile articles	|
|	13303	|	Acabamento de fios,  tecidos e artigos têxteis, n.e.	|	Finishing of yarns, fabrics and textiles, n.e.c.	|
|	13910	|	Fabricação de tecidos de malha	|	Manufacture of knitted and crocheted fabrics	|
|	13920	|	Fabricação de artigos têxteis confeccionados, excepto vestuário	|	Manufacture of made-up textile articles, except apparel	|
|	13930	|	Fabricação de tapetes e carpetes	|	Manufacture of carpets and rugs	|
|	13941	|	Fabricação de cordoaria	|	Manufacture of cordage, rope and twine	|
|	13942	|	Fabricação de redes	|	Manufacture of nets	|
|	13950	|	Fabricação de não tecidos e respectivos artigos, excepto vestuário	|	Manufacture of non-wovens and articles made from non-wovens, except apparel	|
|	13961	|	Fabricação de passamanarias e sirgarias	|	Manufacture of ornamental trimmings and narrow fabrics	|
|	13962	|	Fabricação de têxteis para uso técnico e industrial, n.e.	|	Manufacture of other technical and industrial textiles, n.e.c.	|
|	13991	|	Fabricação de bordados	|	Manufacture of embroidery	|
|	13992	|	Fabricação de rendas	|	Manufacture of lace	|
|	13993	|	Fabricação de outros  têxteis diversos, n.e.	|	Manufacture of other miscellaneous textiles, n.e.c.	|
|	14110	|	Confecção de vestuário em couro	|	Manufacture of leather clothes	|
|	14120	|	Confecção de vestuário de trabalho	|	Manufacture of workwear	|
|	14131	|	Confecção de outro vestuário exterior em série	|	Manufacture of other ready-to-wear outerwear 	|
|	14132	|	Confecção de outro vestuário exterior por medida	|	Manufacture of other made-to-measure outerwear	|
|	14133	|	Actividades de acabamento de artigos de vestuário	|	Finishing activities on wear products	|
|	14140	|	Confecção de vestuário interior	|	Manufacture of underwear	|
|	14190	|	Confecção de outros artigos e acessórios de vestuário	|	Manufacture of other wearing apparel and accessories	|
|	14200	|	Fabricação de artigos de peles com pêlo	|	Manufacture of articles of fur	|
|	14310	|	Fabricação de meias e similares de malha	|	Manufacture of knitted and crocheted hosiery	|
|	14390	|	Fabricação de outro vestuário de malha	|	Manufacture of other knitted and crocheted apparel	|
|	15111	|	Curtimenta e acabamento de peles sem pêlo	|	Tanning and dressing of leather	|
|	15112	|	Fabricação de couro reconstituído	|	Manufacture of composition leather	|
|	15113	|	Curtimenta e acabamento de peles com pêlo	|	Tanning and dressing of fur	|
|	15120	|	Fabricação de artigos de viagem e de uso pessoal, de marroquinaria, de correeiro e de seleiro	|	Manufacture of luggage, handbags and the like, saddlery and harness	|
|	15201	|	Fabricação de calçado	|	Manufacture of footwear	|
|	15202	|	Fabricação de componentes para calçado	|	Manufacture of parts of footwear	|
|	16101	|	Serração de madeira	|	Sawmilling of wood	|
|	16102	|	Impregnação de madeira	|	Impregnation of wood	|
|	16211	|	Fabricação de painéis de partículas de madeira	|	Manufacture of wood particle boards	|
|	16212	|	Fabricação de painéis de fibras de madeira	|	Manufacture of wood fibre boards	|
|	16213	|	Fabricação de folheados, contraplacados, lamelados e de outros painéis	|	Manufacture of veneer sheets	|
|	16220	|	Parqueteria	|	Manufacture of assembled parquet floors	|
|	16230	|	Fabricação de outras obras de carpintaria para a construção	|	Manufacture of other builders' carpentry and joinery	|
|	16240	|	Fabricação de embalagens de madeira	|	Manufacture of wooden containers	|
|	16291	|	Fabricação de outras obras de madeira	|	Manufacture of other products of wood	|
|	16292	|	Fabricação de obras de cestaria e de espartaria	|	Manufacture of articles of straw and plaiting materials	|
|	16293	|	Indústria de preparação da cortiça	|	Cork industry	|
|	16294	|	Fabricação de rolhas de cortiça	|	Manufacture of cork	|
|	16295	|	Fabricação de outros produtos de cortiça	|	Manufacture of other articles of cork	|
|	17110	|	Fabricação de pasta	|	Manufacture of pulp	|
|	17120	|	Fabricação de papel e de cartão (excepto canelado)	|	Manufacture of paper and paperboard	|
|	17211	|	Fabricação de papel e de cartão canelados (inclui embalagens)	|	Manufacture of corrugated paper and paperboard 	|
|	17212	|	Fabricação de outras embalagens de papel e de cartão	|	Manufacture of other containers of paper and paperboard	|
|	17220	|	Fabricação de artigos de papel para uso doméstico e sanitário	|	Manufacture of household and sanitary goods and of toilet requisites	|
|	17230	|	Fabricação de artigos de papel para papelaria	|	Manufacture of paper stationery	|
|	17240	|	Fabricação de papel de parede	|	Manufacture of wallpaper	|
|	17290	|	Fabricação de outros artigos de pasta de papel, de papel e de cartão	|	Manufacture of other articles of paper and paperboard	|
|	18110	|	Impressão de jornais	|	Printing of newspapers	|
|	18120	|	Outra impressão	|	Other printing	|
|	18130	|	Actividades de preparação da impressão e de produtos media	|	Pre-press and pre-media services	|
|	18140	|	Encadernação  e actividades  relacionadas	|	Binding and related services	|
|	18200	|	Reprodução de suportes gravados	|	Reproduction of recorded media	|
|	19100	|	Fabricação de produtos de coqueria	|	Manufacture of coke oven products	|
|	19201	|	Fabricação de produtos petrolíferos refinados	|	Manufacture of refined petroleum products	|
|	19202	|	Fabricação de produtos petrolíferos a partir de resíduos	|	Manufacture of petroleum products from waste	|
|	19203	|	Fabricação de briquetes e aglomerados de hulha e lenhite	|	Manufacture of briquettes and pellets of coal and lignite	|
|	20110	|	Fabricação de gases industriais	|	Manufacture of industrial gases	|
|	20120	|	Fabricação de corantes e pigmentos	|	Manufacture of dyes and pigments	|
|	20130	|	Fabricação de outros produtos químicos inorgânicos de base	|	Manufacture of other inorganic basic chemicals	|
|	20141	|	Fabricação de resinosos e seus derivados	|	Manufacture of resin and its derivatives	|
|	20142	|	Fabricação de carvão (vegetal e animal) e produtos associados	|	Manufacture of coal (plant and animal) and related products	|
|	20143	|	Fabricação de álcool etílico de fermentação	|	Manufacture of ethyl alcohol fermentation	|
|	20144	|	Fabricação de outros produtos químicos orgânicos de base, n.e.	|	Manufacture of other organic basic chemicals, n.e.c.	|
|	20151	|	Fabricação de adubos químicos ou minerais e de compostos azotados	|	Manufacture of chemical or mineral fertilisers and nitrogen compounds	|
|	20152	|	Fabricação de adubos orgânicos e organo-minerais	|	Manufacture of organic and organic-mineral fertilisers	|
|	20160	|	Fabricação de matérias plásticas sob formas primárias	|	Manufacture of plastics in primary forms	|
|	20170	|	Fabricação de borracha sintética sob formas primárias	|	Manufacture of synthetic rubber in primary forms	|
|	20200	|	Fabricação de pesticidas e de outros produtos agroquímicos	|	Manufacture of pesticides and other agrochemical products	|
|	20301	|	Fabricação de tintas (excepto impressão), vernizes, mastiques e produtos similares	|	Manufacture of paints (except printing ink), varnishes, mastics and related products	|
|	20302	|	Fabricação de tintas de impressão	|	Manufacture of printing ink	|
|	20303	|	Fabricação de pigmentos preparados, composições vitrificáveis e afins	|	Manufacture of pigments, prepared vitrifiable and related	|
|	20411	|	Fabricação de sabões, detergentes e glicerina	|	Manufacture of soap, detergents and glycerol	|
|	20412	|	Fabricação de produtos de limpeza, polimento e protecção	|	Manufacture of cleaning and polishing preparations	|
|	20420	|	Fabricação de perfumes, de cosméticos e de produtos de higiene	|	Manufacture of perfumes and toilet preparations	|
|	20510	|	Fabricação de explosivos e artigos de pirotecnia	|	Manufacture of explosives	|
|	20520	|	Fabricação de colas	|	Manufacture of glues	|
|	20530	|	Fabricação de óleos essenciais	|	Manufacture of essential oils	|
|	20591	|	Fabricação de biodiesel	|	Manufacture of biodiesel	|
|	20592	|	Fabricação de produtos químicos auxiliares para uso industrial	|	Manufacture of chemical products for industrial use	|
|	20593	|	Fabricação de óleos e massas lubrificantes, com exclusão da efectuada nas refinarias	|	Manufacture of lubricating oils and greases, except that made in refineries	|
|	20594	|	Fabricação de outros produtos químicos diversos, n.e.	|	Manufacture of other miscellaneous chemical products, n.e.c.	|
|	20600	|	Fabricação de fibras sintéticas ou artificiais	|	Manufacture of man-made fibres	|
|	21100	|	Fabricação de produtos farmacêuticos de base	|	Manufacture of basic pharmaceutical products	|
|	21201	|	Fabricação de medicamentos	|	Manufacture of medicaments	|
|	21202	|	Fabricação de outras preparações e de artigos farmacêuticos	|	Manufacture of other pharmaceutical preparations and pharmaceuticals	|
|	22111	|	Fabricação de pneus e câmaras-de-ar	|	Manufacture of rubber tyres and tubes	|
|	22112	|	Reconstrução de pneus	|	Retreading and rebuilding of rubber tyres	|
|	22191	|	Fabricação de componentes de borracha para calçado	|	Manufacture of rubber components for footwear	|
|	22192	|	Fabricação de outros produtos de borracha, n.e.	|	Manufacture of other rubber products, n.e.c.	|
|	22210	|	Fabricação de chapas, folhas, tubos e perfis de plástico	|	Manufacture of plastic plates, sheets, tubes and profiles	|
|	22220	|	Fabricação de embalagens de plástico	|	Manufacture of plastic packing goods	|
|	22230	|	Fabricação de artigos de plástico para a construção	|	Manufacture of builder's ware of plastic	|
|	22291	|	Fabricação de componentes de plástico para calçado	|	Manufacture of plastic components for footwear	|
|	22292	|	Fabricação de outros artigos de plástico, n.e.	|	Manufacture of other plastic products, n.e.c.	|
|	23110	|	Fabricação de vidro plano	|	Manufacture of flat glass	|
|	23120	|	Moldagem e transformação de vidro plano	|	Shaping and processing of flat glass	|
|	23131	|	Fabricação de vidro de embalagem	|	Manufacture of hollow glass	|
|	23132	|	Cristalaria	|	Manufacture of crystal ware	|
|	23140	|	Fabricação de fibras de vidro	|	Manufacture of glass fibres	|
|	23190	|	Fabricação e transformação de outro vidro (inclui vidro técnico)	|	Manufacture and processing of other glass, including technical glassware	|
|	23200	|	Fabricação de produtos cerâmicos refractários	|	Manufacture of refractory products	|
|	23311	|	Fabricação de azulejos	|	Manufacture of ceramic tiles 	|
|	23312	|	Fabricação de ladrilhos, mosaicos e placas de cerâmica	|	Manufacture of floor flags, tiles and mosaic	|
|	23321	|	Fabricação de tijolos	|	Manufacture of bricks	|
|	23322	|	Fabricação de telhas	|	Manufacture of tiles 	|
|	23323	|	Fabricação de abobadilhas	|	Manufacture of support or filler tiles	|
|	23324	|	Fabricação de outros produtos cerâmicos para a construção	|	Manufacture of other clay building materials	|
|	23411	|	Olaria de barro	|	Pottery	|
|	23412	|	Fabricação de artigos de uso doméstico de faiança, porcelana e grés fino	|	Manufacture of household articles made of stone- or earthenware, porcelain and china	|
|	23413	|	Fabricação de artigos de ornamentação de faiança, porcelana e grés fino	|	Manufacture of ornamental articles made of stone- or earthenware, porcelain and china	|
|	23414	|	Actividades de decoração de artigos cerâmicos de uso doméstico e ornamental	|	Activities decoration of ceramic household and ornamental articles	|
|	23420	|	Fabricação de artigos cerâmicos para usos sanitários	|	Manufacture of ceramic sanitary fixtures	|
|	23430	|	Fabricação de isoladores e peças isolantes em cerâmica	|	Manufacture of ceramic insulators and insulating fittings	|
|	23440	|	Fabricação de outros produtos em cerâmica para usos técnicos	|	Manufacture of other technical ceramic products	|
|	23490	|	Fabricação de outros produtos cerâmicos não refractários	|	Manufacture of other ceramic products	|
|	23510	|	Fabricação de cimento	|	Manufacture of cement	|
|	23521	|	Fabricação de cal	|	Manufacture of lime 	|
|	23522	|	Fabricação de gesso	|	Manufacture of plaster	|
|	23610	|	Fabricação de produtos de betão para a construção	|	Manufacture of concrete products for construction purposes	|
|	23620	|	Fabricação de produtos de gesso para a construção	|	Manufacture of plaster products for construction purposes	|
|	23630	|	Fabricação de betão pronto	|	Manufacture of ready-mixed concrete	|
|	23640	|	Fabricação de argamassas	|	Manufacture of mortars	|
|	23650	|	Fabricação de produtos de fibrocimento	|	Manufacture of fibre cement	|
|	23690	|	Fabricação de outros produtos de betão, gesso e cimento	|	Manufacture of other articles of concrete, plaster and cement	|
|	23701	|	Fabricação de artigos de mármore e de rochas similares	|	Manufacture of articles of marble and similar stone	|
|	23702	|	Fabricação de artigos em ardósia (lousa)	|	Manufacture of articles of slate	|
|	23703	|	Fabricação de artigos de granito e de rochas, n.e.	|	Manufacture of articles of granite and stones, n.e.c.	|
|	23910	|	Fabricação de produtos abrasivos	|	Production of abrasive products	|
|	23991	|	Fabricação de misturas betuminosas	|	Manufacture of bituminous mixtures	|
|	23992	|	Fabricação de outros produtos minerais não metálicos diversos, n.e.	|	Manufacture of other non-metallic mineral products, n.e.c.	|
|	24100	|	Siderurgia e fabricação de ferro-ligas	|	Manufacture of basic iron and steel and of ferro-alloys	|
|	24200	|	Fabricação de tubos, condutas, perfis ocos e respectivos acessórios,  de aço	|	Manufacture of tubes, pipes, hollow profiles and related fittings, of steel	|
|	24310	|	Estiragem a frio	|	Cold drawing of bars	|
|	24320	|	Laminagem a frio de arco ou banda	|	Cold rolling of narrow strip	|
|	24330	|	Perfilagem a frio	|	Cold forming or folding	|
|	24340	|	Trefilagem a frio	|	Cold drawing of wire	|
|	24410	|	Obtenção e primeira transformação de metais preciosos	|	Precious metals production	|
|	24420	|	Obtenção e primeira transformação de alumínio	|	Aluminium production	|
|	24430	|	Obtenção e primeira transformação de chumbo, zinco e estanho	|	Lead, zinc and tin production	|
|	24440	|	Obtenção e primeira transformação de cobre	|	Copper production	|
|	24450	|	Obtenção e primeira transformação de outros metais não ferrosos	|	Other non-ferrous metal production	|
|	24460	|	Tratamento de combustível nuclear	|	Processing of nuclear fuel 	|
|	24510	|	Fundição de ferro fundido	|	Casting of iron	|
|	24520	|	Fundição de aço	|	Casting of steel	|
|	24530	|	Fundição de metais leves	|	Casting of light metals	|
|	24540	|	Fundição de outros metais não ferrosos	|	Casting of other non-ferrous metals	|
|	25110	|	Fabricação de estruturas de construções metálicas	|	Manufacture of metal structures and parts of structures	|
|	25120	|	Fabricação de portas, janelas e elementos similares em metal	|	Manufacture of doors and windows of metal	|
|	25210	|	Fabricação de caldeiras e radiadores para aquecimento central	|	Manufacture of central heating radiators and boilers	|
|	25290	|	Fabricação de outros reservatórios e recipientes metálicos	|	Manufacture of other tanks, reservoirs and containers of metal	|
|	25300	|	Fabricação de geradores de vapor (excepto caldeiras para aquecimento central)	|	Manufacture of steam generators, except central heating hot water boilers	|
|	25401	|	Fabricação de armas de caça, de desporto e defesa	|	Manufacture of hunting, sporting or protective firearms and ammunition	|
|	25402	|	Fabricação de armamento	|	Manufacture of armament	|
|	25501	|	Fabricação de produtos forjados, estampados e laminados	|	Forging, pressing, stamping and roll forming of metal	|
|	25502	|	Fabricação de produtos por pulverometalurgia	|	Powder metallurgy	|
|	25610	|	Tratamento e revestimento de metais	|	Treatment and coating of metals	|
|	25620	|	Actividades de mecânica geral	|	Machining	|
|	25710	|	Fabricação de cutelaria	|	Manufacture of cutlery	|
|	25720	|	Fabricação de fechaduras, dobradiças e de outras ferragens	|	Manufacture of locks and hinges	|
|	25731	|	Fabricação de ferramentas manuais	|	Manufacture of hand tools	|
|	25732	|	Fabricação de ferramentas mecânicas	|	Manufacture of mechanical tools	|
|	25733	|	Fabricação de peças sinterizadas	|	Manufacture of sintered parts	|
|	25734	|	Fabricação de moldes metálicos	|	Manufacture of metal moulds	|
|	25910	|	Fabricação de embalagens metálicas pesadas	|	Manufacture of steel drums and similar containers	|
|	25920	|	Fabricação de embalagens metálicas ligeiras	|	Manufacture of light metal packaging 	|
|	25931	|	Fabricação de produtos de arame	|	Manufacture of wire products	|
|	25932	|	Fabricação de molas	|	Manufacture of springs	|
|	25933	|	Fabricação de correntes metálicas	|	Manufacture of metal chains	|
|	25940	|	Fabricação de rebites, parafusos e porcas	|	Manufacture of fasteners and screw machine products	|
|	25991	|	Fabricação de louça metálica e artigos de uso doméstico	|	Manufacture of metal household articles	|
|	25992	|	Fabricação de outros produtos metálicos diversos,  n.e.	|	Manufacture of other fabricated miscellaneous metal products,  n.e.c.	|
|	26110	|	Fabricação de componentes electrónicos	|	Manufacture of electronic components	|
|	26120	|	Fabricação de placas de circuitos electrónicos	|	Manufacture of loaded electronic boards	|
|	26200	|	Fabricação de computadores e de equipamento periférico	|	Manufacture of computers and peripheral equipment	|
|	26300	|	Fabricação de aparelhos e equipamentos para comunicações	|	Manufacture of communication equipment	|
|	26400	|	Fabricação de receptores  de rádio e de televisão e bens de consumo similares	|	Manufacture of consumer electronics	|
|	26511	|	Fabricação de contadores de electricidade, gás, água e de outros líquidos	|	Manufacture of instruments for measuring electricity, gas  water and other fluid	|
|	26512	|	Fabricação de instrumentos e aparelhos de medida, verificação, navegação e outros fins, n.e.	|	Manufacture of instruments and appliances for measuring, checking, testing, navigating and other purposes, n.e.c.	|
|	26520	|	Fabricação de relógios e material de relojoaria	|	Manufacture of watches and clocks	|
|	26600	|	Fabricação de equipamentos de radiação, electromedicina e electroterapêutico	|	Manufacture of irradiation, electromedical and electrotherapeutic equipment	|
|	26701	|	Fabricação de instrumentos e equipamentos ópticos não oftálmicos	|	Manufacture of optical non-ophthalmic instruments 	|
|	26702	|	Fabricação de material fotográfico e cinematográfico	|	Manufacture of photographic and cinematographic equipment	|
|	26800	|	Fabricação de suportes de informação magnéticos e ópticos	|	Manufacture of magnetic and optical media	|
|	27110	|	Fabricação de motores, geradores e transformadores eléctricos	|	Manufacture of electric motors, generators and transformers	|
|	27121	|	Fabricação de material de distribuição e controlo para instalações eléctricas de alta tensão	|	Manufacture of electricity distribution and control apparatus for high-voltage electrical installations	|
|	27122	|	Fabricação de material de distribuição e controlo para instalações eléctricas de baixa tensão	|	Manufacture of electricity distribution and control apparatus for low-voltage electrical installations	|
|	27200	|	Fabricação de acumuladores e pilhas	|	Manufacture of batteries and accumulators	|
|	27310	|	Fabricação de cabos de fibra óptica	|	Manufacture of fibre optic cables	|
|	27320	|	Fabricação de outros fios e cabos eléctricos e electrónicos	|	Manufacture of other electronic and electric wires and cables	|
|	27330	|	Fabricação de dispositivos e acessórios para instalações eléctricas de baixa tensão	|	Manufacture of wiring devices	|
|	27400	|	Fabricação de lâmpadas eléctricas e de outro equipamento de iluminação	|	Manufacture of electric lighting equipment	|
|	27510	|	Fabricação de electrodomésticos	|	Manufacture of electric domestic appliances	|
|	27520	|	Fabricação de aparelhos não eléctricos para uso doméstico	|	Manufacture of non-electric domestic appliances	|
|	27900	|	Fabricação de outro equipamento eléctrico	|	Manufacture of other electrical equipment	|
|	28110	|	Fabricação de motores e turbinas, excepto motores para aeronaves, automóveis e motociclos	|	Manufacture of engines and turbines, except aircraft, vehicle and cycle engines	|
|	28120	|	Fabricação de equipamento hidráulico e pneumático	|	Manufacture of fluid power equipment	|
|	28130	|	Fabricação de outras bombas e compressores	|	Manufacture of other pumps and compressors	|
|	28140	|	Fabricação de  outras torneiras e válvulas	|	Manufacture of other taps and valves	|
|	28150	|	Fabricação de rolamentos, de engrenagens e de outros órgãos de transmissão	|	Manufacture of bearings, gears, gearing and driving elements	|
|	28210	|	Fabricação de fornos e queimadores	|	Manufacture of ovens, furnaces and furnace burners	|
|	28221	|	Fabricação de ascensores e monta cargas, escadas e passadeiras rolantes	|	Manufacture of lifts, escalators and moving walkways	|
|	28222	|	Fabricação de equipamentos de elevação e de movimentação, n.e.	|	Manufacture of lifting and handling equipment, n.e.c.	|
|	28230	|	Fabricação de máquinas e equipamento de escritório, excepto computadores e equipamento periférico	|	Manufacture of office machinery and equipment (except computers and peripheral equipment)	|
|	28240	|	Fabricação de máquinas-ferramentas portáteis com motor	|	Manufacture of power-driven hand tools	|
|	28250	|	Fabricação de equipamento não doméstico para refrigeração e ventilação	|	Manufacture of non-domestic cooling and ventilation equipment	|
|	28291	|	Fabricação de máquinas de acondicionamento e de embalagem	|	Manufacture of packing and wrapping machinery 	|
|	28292	|	Fabricação de balanças e de outro equipamento para pesagem	|	Manufacture of scales and other weighing machinery	|
|	28293	|	Fabricação de outras máquinas diversas de uso geral, n.e.	|	Manufacture of other general purpose machinery, n.e.c.	|
|	28300	|	Fabricação de máquinas e de tractores para a agricultura, pecuária e silvicultura	|	Manufacture of agricultural and forestry machinery	|
|	28410	|	Fabricação de máquinas-ferramentas para metais	|	Manufacture of metal forming machinery	|
|	28490	|	Fabricação de outras máquinas-ferramentas, n.e.	|	Manufacture of other machine tools	|
|	28910	|	Fabricação de máquinas para a metalurgia	|	Manufacture of machinery for metallurgy	|
|	28920	|	Fabricação de máquinas para as indústrias extractivas e para a construção	|	Manufacture of machinery for mining, quarrying and construction	|
|	28930	|	Fabricação de máquinas para as indústrias alimentares, das bebidas e do tabaco	|	Manufacture of machinery for food, beverage and tobacco processing	|
|	28940	|	Fabricação de máquinas para as indústrias têxtil, do vestuário e do couro	|	Manufacture of machinery for textile, apparel and leather production	|
|	28950	|	Fabricação de máquinas para as indústrias do papel e do cartão	|	Manufacture of machinery for paper and paperboard production	|
|	28960	|	Fabricação de máquinas para as indústrias do plástico e da borracha	|	Manufacture of plastics and rubber machinery	|
|	28991	|	Fabricação de máquinas para as indústrias de materiais de construção, cerâmica e vidro	|	Manufacture of machinery for construction, ceramics and glass	|
|	28992	|	Fabricação de outras máquinas diversas para uso específico, n.e.	|	Manufacture of other miscellaneous special purpose machinery, n.e.c.	|
|	29100	|	Fabricação de veículos automóveis	|	Manufacture of motor vehicles	|
|	29200	|	Fabricação de carroçarias, reboques e semi-reboques	|	Manufacture of bodies (coachwork) for motor vehicles	|
|	29310	|	Fabricação de equipamento eléctrico e electrónico para veículos automóveis	|	Manufacture of electrical and electronic equipment for motor vehicles	|
|	29320	|	Fabricação de outros componentes e acessórios para veículos automóveis	|	Manufacture of other parts and accessories for motor vehicles	|
|	30111	|	Construção de embarcações metálicas e estruturas flutuantes, excepto de recreio e desporto	|	Building of metal ships, except pleasure and sporting boats	|
|	30112	|	Construção de embarcações não metálicas, excepto de recreio e desporto	|	Building of non-metal ships, except pleasure and sporting boats	|
|	30120	|	Construção de embarcações de recreio e de desporto	|	Building of pleasure and sporting boats	|
|	30200	|	Fabricação de material circulante para caminhos-de-ferro	|	Manufacture of railway locomotives and rolling stock	|
|	30300	|	Fabricação de aeronaves, de veículos espaciais e equipamento relacionado	|	Manufacture of air and spacecraft and related machinery	|
|	30400	|	Fabricação de veículos militares de combate	|	Manufacture of military fighting vehicles	|
|	30910	|	Fabricação de motociclos	|	Manufacture of motorcycles	|
|	30920	|	Fabricação de bicicletas e veículos para inválidos	|	Manufacture of bicycles and invalid carriages	|
|	30990	|	Fabricação de outro equipamento de transporte, n.e.	|	Manufacture of other transport equipment n.e.c.	|
|	31010	|	Fabricação de mobiliário para escritório e comércio	|	Manufacture of office and shop furniture	|
|	31020	|	Fabricação de mobiliário de cozinha	|	Manufacture of kitchen furniture	|
|	31030	|	Fabricação de colchoaria	|	Manufacture of mattresses	|
|	31091	|	Fabricação de mobiliário de madeira para outros fins	|	Manufacture of wooden furniture for other purposes	|
|	31092	|	Fabricação de mobiliário metálico para outros fins	|	Manufacture of metal furniture for other purposes	|
|	31093	|	Fabricação de mobiliário de outros materiais para outros fins	|	Manufacture of furniture of other material for other purposes	|
|	31094	|	Actividades de acabamento de mobiliário	|	Completion and finishing of furniture	|
|	32110	|	Cunhagem de moedas	|	Striking of coins	|
|	32121	|	Fabricação de filigranas	|	Manufacture of filigree	|
|	32122	|	Fabricação de artigos de joalharia e de outros artigos de ourivesaria	|	Manufacture of jewellery and related articles, n.c.e	|
|	32123	|	Trabalho de diamantes e de outras pedras preciosas ou semi-preciosas para joalharia e uso industrial	|	Working of diamonds and of other precious or semi-precious stones for jewellery and industrial use	|
|	32130	|	Fabricação de bijutarias	|	Manufacture of imitation jewellery and related articles	|
|	32200	|	Fabricação de instrumentos musicais	|	Manufacture of musical instruments	|
|	32300	|	Fabricação de artigos de desporto	|	Manufacture of sports goods	|
|	32400	|	Fabricação de jogos e de brinquedos	|	Manufacture of games and toys	|
|	32501	|	Fabricação de material óptico oftálmico	|	Manufacture of optical ophthalmic instruments	|
|	32502	|	Fabricação de material ortopédico e próteses e de instrumentos médico-cirúrgicos	|	Manufacture of orthopaedic appliances and prosthesis and medical and surgical equipment	|
|	32910	|	Fabricação de vassouras, escovas e pincéis	|	Manufacture of brooms and brushes	|
|	32991	|	Fabricação de canetas, lápis e similares	|	Manufacture of pens, pencils and related articles	|
|	32992	|	Fabricação de fechos de correr, botões e similares	|	Manufacture of slide fasteners, buttons and related articles	|
|	32993	|	Fabricação de guarda-sóis e chapéus de chuva	|	Manufacture of parasols and umbrellas	|
|	32994	|	Fabricação de equipamento de protecção e segurança	|	Manufacture of equipment for safety and security	|
|	32995	|	Fabricação de caixões mortuários em madeira	|	Manufacture of wooden coffins	|
|	32996	|	Outras indústrias transformadoras diversas, n.e.	|	Other miscellaneous manufacturing activities, n.e.c.	|
|	33110	|	Reparação e manutenção  de produtos metálicos (excepto máquinas e equipamento)	|	Repair of fabricated metal products	|
|	33120	|	Reparação e  manutenção de máquinas e equipamentos	|	Repair of machinery	|
|	33130	|	Reparação e manutenção de equipamento electrónico e óptico	|	Repair of electronic and optical equipment	|
|	33140	|	Reparação e manutenção de equipamento eléctrico	|	Repair of electrical equipment	|
|	33150	|	Reparação e manutenção de embarcações	|	Repair and maintenance of ships and boats	|
|	33160	|	Reparação e manutenção de aeronaves e de veículos espaciais	|	Repair and maintenance of aircraft and spacecraft	|
|	33170	|	Reparação e manutenção de outro equipamento de transporte	|	Repair and maintenance of other transport equipment	|
|	33190	|	Reparação e manutenção de outro equipamento	|	Repair of other equipment	|
|	33200	|	Instalação de máquinas e de equipamentos industriais	|	Installation of industrial machinery and equipment	|
|	35111	|	Produção de electricidade de origem hídrica	|	Production of electricity from water	|
|	35112	|	Produção de electricidade de origem térmica	|	Production of electricity from thermal sources	|
|	35113	|	Produção de electricidade de origem eólica, geotérmica, solar e de origem, n.e.	|	Production of electricity from wind, geothermal, solar and origin nec	|
|	35120	|	Transporte de electricidade	|	Transmission of electricity	|
|	35130	|	Distribuição de electricidade	|	Distribution of electricity	|
|	35140	|	Comércio de electricidade	|	Trade of electricity	|
|	35210	|	Produção de gás	|	Manufacture of gas	|
|	35220	|	Distribuição de combustíveis gasosos por condutas	|	Distribution of gaseous fuels through mains	|
|	35230	|	Comércio de gás por condutas	|	Trade of gas through mains	|
|	35301	|	Produção e distribuição de vapor,  água quente e fria  e ar frio por conduta	|	Production and distribution of steam, hot and cold water and cold air by conduct	|
|	35302	|	Produção de gelo	|	Production of ice	|
|	36001	|	Captação e tratamento de água	|	Water collection and treatment	|
|	36002	|	Distribuição de água	|	Distribution of water	|
|	37001	|	Recolha e drenagem de águas residuais	|	Collection and drainage of sewage	|
|	37002	|	Tratamento de águas residuais	|	Wastewater	|
|	38111	|	Recolha de resíduos inertes	|	Collection of inert waste	|
|	38112	|	Recolha de outros resíduos não perigosos	|	Collection of other non-hazardous waste	|
|	38120	|	Recolha de resíduos perigosos	|	Collection of hazardous waste	|
|	38211	|	Tratamento e eliminação de resíduos inertes	|	Treatment and disposal of inert waste	|
|	38212	|	Tratamento e eliminação de outros resíduos não perigosos	|	Treatment and disposal of other non-hazardous waste	|
|	38220	|	Tratamento e eliminação de resíduos perigosos	|	Treatment and disposal of hazardous waste	|
|	38311	|	Desmantelamento de veículos automóveis, em fim de vida	|	Dismantling of vehicles at the end of life	|
|	38312	|	Desmantelamento de equipamentos eléctricos e electrónicos, em fim de vida	|	Dismantling of electrical and electronic equipment at the end of life	|
|	38313	|	Desmantelamento de outros equipamentos e bens, em fim de vida	|	Dismantling of equipment and other assets at the end of life	|
|	38321	|	Valorização de resíduos metálicos	|	Recovery of scrap metal	|
|	38322	|	Valorização de resíduos não metálicos	|	Recovery of non-metallic material	|
|	39000	|	Descontaminação e actividades similares	|	Remediation activities and other waste management services	|
|	41100	|	Promoção imobiliária (desenvolvimento de projectos de edifícios)	|	Development of building projects	|
|	41200	|	Construção de edifícios (residenciais e não residenciais)	|	Construction of residential and non-residential buildings	|
|	42110	|	Construção de estradas e pistas de aeroportos	|	Construction of roads and motorways	|
|	42120	|	Construção de vias férreas	|	Construction of railways and underground railways	|
|	42130	|	Construção de pontes e túneis	|	Construction of bridges and tunnels	|
|	42210	|	Construção de redes de transporte de águas, de esgotos e de outros fluídos	|	Construction of utility projects for fluids	|
|	42220	|	Construção de redes de transporte e distribuição de electricidade e redes de telecomunicações	|	Construction of utility projects for electricity and telecommunications	|
|	42910	|	Engenharia hidráulica	|	Construction of water projects	|
|	42990	|	Construção de outras obras de engenharia civil, n.e.	|	Construction of other civil engineering projects n.e.c.	|
|	43110	|	Demolição	|	Demolition	|
|	43120	|	Preparação dos locais de construção	|	Site preparation	|
|	43130	|	Perfurações e sondagens	|	Test drilling and boring	|
|	43210	|	Instalação eléctrica	|	Electrical installation	|
|	43221	|	Instalação de canalizações	|	Installation of plumbling 	|
|	43222	|	Instalação de climatização	|	Installation of conditioning air	|
|	43290	|	Outras instalações em construções	|	Other construction installation	|
|	43310	|	Estucagem	|	Plastering	|
|	43320	|	Montagem de trabalhos de carpintaria e de caixilharia	|	Joinery installation	|
|	43330	|	Revestimento de pavimentos e de paredes	|	Floor and wall covering	|
|	43340	|	Pintura e colocação de vidros	|	Painting and glazing	|
|	43390	|	Outras actividades de acabamento em edifícios	|	Other building completion and finishing	|
|	43910	|	Actividades de colocação de coberturas	|	Roofing activities	|
|	43991	|	Aluguer de equipamento de construção e de demolição, com operador	|	Renting of construction or demolition equipment with operator	|
|	43992	|	Outras actividades  especializadas de construção diversas, n.e.	|	Other miscellaneous specialised construction activities n.e.c.	|
|	45110	|	Comércio de veículos automóveis ligeiros	|	Sale of cars and light motor vehicles	|
|	45190	|	Comércio de outros veículos automóveis	|	Sale of other motor vehicles	|
|	45200	|	Manutenção e reparação de veículos automóveis	|	Maintenance and repair of motor vehicles	|
|	45310	|	Comércio por grosso de peças e acessórios para veículos automóveis	|	Wholesale trade of motor vehicle parts and accessories	|
|	45320	|	Comércio a retalho de peças e acessórios para veículos automóveis	|	Retail trade of motor vehicle parts and accessories	|
|	45401	|	Comércio por grosso e a retalho de motociclos, de suas peças e acessórios	|	Wholesale and retail of motorcycles and related parts and accessories	|
|	45402	|	Manutenção e reparação de motociclos, de suas peças e acessórios	|	Maintenance and repair of motorcycles and related parts and accessories	|
|	46110	|	Agentes do comércio por grosso de matérias-primas agrícolas e têxteis, animais vivos e produtos semi-acabados	|	Agents involved in the sale of agricultural raw materials, live animals, textile raw materials and semi-finished goods	|
|	46120	|	Agentes do comércio por grosso de combustíveis, minérios, metais e de produtos químicos para a indústria	|	Agents involved in the sale of fuels, ores, metals and industrial chemicals	|
|	46130	|	Agentes do comércio por grosso de madeira e materiais de construção	|	Agents involved in the sale of timber and building materials	|
|	46140	|	Agentes do comércio por grosso de máquinas, equipamento industrial, embarcações e aeronaves	|	Agents involved in the sale of machinery, industrial equipment, ships and aircraft	|
|	46150	|	Agentes do comércio por grosso de mobiliário, artigos para uso doméstico e ferragens	|	Agents involved in the sale of furniture, household goods, hardware and ironmongery	|
|	46160	|	Agentes do comércio por grosso de têxteis, vestuário, calçado e artigos de couro	|	Agents involved in the sale of textiles, clothing, fur, footwear and leather goods	|
|	46170	|	Agentes do comércio por grosso de produtos alimentares, bebidas e tabaco	|	Agents involved in the sale of food, beverages and tobacco	|
|	46180	|	Agentes especializados do comércio por grosso de outros produtos	|	Agents specialised in the sale of other particular products	|
|	46190	|	Agentes do comércio por grosso misto sem predominância	|	Agents involved in the sale of a variety of goods	|
|	46211	|	Comércio por grosso de alimentos para animais	|	Wholesale of animal feeds	|
|	46212	|	Comércio por grosso de tabaco em bruto	|	Wholesale of ummanufactured tobacco	|
|	46213	|	Comércio por grosso de cortiça em bruto	|	Wholesale of cork in the rough	|
|	46214	|	Comércio por grosso de cereais, sementes, leguminosas, oleaginosas e outras matérias-primas agrícolas	|	Wholesale of grain, seed, grain legume, oleaginous and other agricultural raw materials	|
|	46220	|	Comércio por grosso de flores e plantas	|	Wholesale of flowers and plants	|
|	46230	|	Comércio por grosso de animais vivos	|	Wholesale of live animals	|
|	46240	|	Comércio por grosso de peles e couro	|	Wholesale of hides, skins and leather	|
|	46311	|	Comércio por grosso de fruta e de produtos hortícolas, excepto batata	|	Wholesale of fruit and vegetables, except potatoes	|
|	46312	|	Comércio por grosso de batata	|	Wholesale of potatoes	|
|	46320	|	Comércio por grosso de carne e produtos à base de carne	|	Wholesale of meat and meat products	|
|	46331	|	Comércio por grosso de leite, seus derivados e ovos	|	Wholesale of dairy produce and eggs	|
|	46332	|	Comércio por grosso de azeite, óleos e gorduras alimentares	|	Wholesale of olive oil, edible oils and fats	|
|	46341	|	Comércio por grosso de bebidas alcoólicas	|	Wholesale of alcoholic beverages	|
|	46342	|	Comércio por grosso de bebidas não alcoólicas	|	Wholesale of non-alcoholic beverages	|
|	46350	|	Comércio por grosso de tabaco	|	Wholesale of tobacco products	|
|	46361	|	Comércio por grosso de açúcar	|	Wholesale of sugar	|
|	46362	|	Comércio por grosso de chocolate e de produtos de confeitaria	|	Wholesale of chocolate and sugar confectionery	|
|	46370	|	Comércio por grosso de café, chá, cacau e especiarias	|	Wholesale of coffee, tea, cocoa and spices	|
|	46381	|	Comércio por grosso de peixe, crustáceos e moluscos	|	Wholesale of fish, crustaceans and molluscs	|
|	46382	|	Comércio por grosso de outros produtos alimentares, n.e.	|	Wholesale of other food, n.e.c.	|
|	46390	|	Comércio por grosso não especializado de produtos alimentares, bebidas e tabaco	|	Non-specialised wholesale of food, beverages and tobacco	|
|	46410	|	Comércio por grosso de têxteis	|	Wholesale of textiles	|
|	46421	|	Comércio por grosso de vestuário e de acessórios	|	Wholesale of clothing and clothing accessories	|
|	46422	|	Comércio por grosso de calçado	|	Wholesale of footwear	|
|	46430	|	Comércio por grosso de electrodomésticos, aparelhos de rádio e de televisão	|	Wholesale of electrical household appliances	|
|	46441	|	Comércio por grosso de louças em cerâmica e em vidro	|	Wholesale of china and glassware 	|
|	46442	|	Comércio por grosso de produtos de limpeza	|	Wholesale of cleaning materials	|
|	46450	|	Comércio por grosso de perfumes e de produtos de higiene	|	Wholesale of perfume and cosmetics	|
|	46460	|	Comércio por grosso de produtos farmacêuticos	|	Wholesale of pharmaceutical goods	|
|	46470	|	Comércio por grosso de móveis para uso doméstico, carpetes,  tapetes  e artigos de iluminação	|	Wholesale of furniture, carpets and lighting equipment	|
|	46480	|	Comércio por grosso de relógios e de artigos de ourivesaria e joalharia	|	Wholesale of watches and jewellery	|
|	46491	|	Comércio por grosso de artigos de papelaria	|	Wholesale of stationery	|
|	46492	|	Comércio por grosso de livros, revistas e jornais	|	Wholesale of books, magazines and newspapers	|
|	46493	|	Comércio por grosso de brinquedos, jogos e artigos de desporto	|	Wholesale of toys, games and sports goods	|
|	46494	|	Outro comércio por grosso de bens de consumo, n.e.	|	Wholesale of other household goods, n.e.c.	|
|	46510	|	Comércio por grosso de computadores, equipamentos periféricos e programas informáticos	|	Wholesale of computers, computer peripheral equipment and software	|
|	46520	|	Comércio por grosso de  equipamentos  electrónicos,  de telecomunicações e suas partes	|	Wholesale of electronic and telecommunications equipment and parts	|
|	46610	|	Comércio por grosso de máquinas e equipamentos, agrícolas	|	Wholesale of agricultural machinery, equipment and supplies	|
|	46620	|	Comércio por grosso de máquinas-ferramentas	|	Wholesale of machine tools	|
|	46630	|	Comércio por grosso de máquinas para a indústria extractiva, construção e engenharia civil	|	Wholesale of mining, construction and civil engineering machinery	|
|	46640	|	Comércio por grosso de máquinas para a indústria têxtil, máquinas de costura e de tricotar	|	Wholesale of machinery for the textile industry and of sewing and knitting machines	|
|	46650	|	Comércio por grosso de mobiliário de escritório	|	Wholesale of office furniture	|
|	46660	|	Comércio por grosso de outras máquinas e material de escritório	|	Wholesale of other office machinery and equipment	|
|	46690	|	Comércio por grosso de outras máquinas e equipamentos	|	Wholesale of other machinery and equipment	|
|	46711	|	Comércio por grosso de produtos petrolíferos	|	Wholesale of petroleum products 	|
|	46712	|	Comércio por grosso de combustíveis sólidos, líquidos e gasosos, não derivados do petróleo	|	Wholesale of solid, liquid and gaseous fuels and products not related to petroleum	|
|	46720	|	Comércio por grosso de minérios e de metais	|	Wholesale of metals and metal ores	|
|	46731	|	Comércio por grosso de madeira em bruto e de produtos derivados	|	Wholesale of wood in the rough and related products	|
|	46732	|	Comércio por grosso de materiais de construção (excepto madeira) e equipamento sanitário	|	Wholesale of construction materials (except wood) and sanitary equipment	|
|	46740	|	Comércio por grosso de ferragens, ferramentas manuais e artigos para canalizações e aquecimento	|	Wholesale of hardware, plumbing and heating equipment and supplies	|
|	46750	|	Comércio por grosso de produtos químicos	|	Wholesale of chemical products	|
|	46761	|	Comércio por grosso de fibras têxteis naturais, artificiais e sintéticas	|	Wholesale of natural and man-made textile fibres	|
|	46762	|	Comércio por grosso de outros bens intermédios, n.e.	|	Wholesale of other intermediate products n.e.c.	|
|	46771	|	Comércio por grosso de sucatas e de desperdícios metálicos	|	Wholesale of metal waste and scrap 	|
|	46772	|	Comércio por grosso de desperdícios têxteis, de cartão e papéis velhos	|	Wholesale of textile, cardboard and paper waste	|
|	46773	|	Comércio por grosso de desperdícios de materiais, n.e.	|	Wholesale of material waste, n.e.c.	|
|	46900	|	Comércio por grosso não especializado	|	Non-specialised wholesale trade	|
|	47111	|	Comércio a retalho em supermercados e hipermercados	|	Retail sale in supermarkets and hypermarkets	|
|	47112	|	Comércio a retalho em outros estabelecimentos não especializados, com predominância de produtos alimentares, bebidas ou tabaco	|	Retail sale in others non-specialised stores with food, beverages or tobacco predominating	|
|	47191	|	Comércio a retalho não especializado, sem predominância de produtos alimentares, bebidas ou tabaco, em grandes armazéns e similares	|	Non-specialised retail sale in big stores and similar with food, beverages or tobacco not predominating  	|
|	47192	|	Comércio a retalho em  outros estabelecimentos não especializados, sem predominância de produtos alimentares, bebidas ou tabaco	|	Other retail sale in non-specialised stores	|
|	47210	|	Comércio a retalho de frutas e produtos hortícolas, em estabelecimentos especializados	|	Retail sale of fruit and vegetables in specialised stores	|
|	47220	|	Comércio a retalho de carne e produtos à base de carne, em estabelecimentos especializados	|	Retail sale of meat and meat products in specialised stores	|
|	47230	|	Comércio a retalho de peixe, crustáceos e moluscos, em estabelecimentos especializados	|	Retail sale of fish, crustaceans and molluscs in specialised stores	|
|	47240	|	Comércio a retalho de pão, de produtos de pastelaria e de confeitaria, em estabelecimentos especializados	|	Retail sale of bread, cakes, flour confectionery and sugar confectionery in specialised stores	|
|	47250	|	Comércio a retalho de bebidas, em estabelecimentos especializados	|	Retail sale of beverages in specialised stores	|
|	47260	|	Comércio a retalho de tabaco, em estabelecimentos especializados	|	Retail sale of tobacco products in specialised stores	|
|	47291	|	Comércio a retalho de leite e de derivados, em estabelecimentos especializados	|	Retail sale of dairy produce in specialised stores	|
|	47292	|	Comércio a retalho de produtos alimentares, naturais e dietéticos, em estabelecimentos especializados	|	Retail sale of food, natural and dietary in specialized stores	|
|	47293	|	Outro comércio a retalho de produtos alimentares, em estabelecimentos especializados, n.e.	|	Other retail sale of food in specialised stores, n.e.c.	|
|	47300	|	Comércio a retalho de combustível para veículos a motor, em estabelecimentos especializados	|	Retail sale of automotive fuel in specialised stores	|
|	47410	|	Comércio a retalho de computadores, unidades periféricas e programas informáticos, em estabelecimentos especializados	|	Retail sale of computers, peripheral units and software in specialised stores	|
|	47420	|	Comércio a retalho de equipamento de telecomunicações, em estabelecimentos especializados	|	Retail sale of telecommunications equipment in specialised stores	|
|	47430	|	Comércio a retalho de equipamento audiovisual, em estabelecimentos especializados	|	Retail sale of audio and video equipment in specialised stores	|
|	47510	|	Comércio a retalho de têxteis, em estabelecimentos especializados	|	Retail sale of textiles in specialised stores	|
|	47521	|	Comércio a retalho de ferragens e de vidro plano, em estabelecimentos especializados	|	Retail sale of hardware and flat glass in specialised stores	|
|	47522	|	Comércio a retalho de tintas, vernizes e produtos similares, em estabelecimentos especializados	|	Retail sale of paints, varnishes and similar products in specialised stores	|
|	47523	|	Comércio a retalho de material de bricolage, equipamento sanitário, ladrilhos e materiais similares, em estabelecimentos especializados	|	Retail sale of do-it-yourself material, sanitary equipment, floor tile and similar equipment in specialised stores	|
|	47530	|	Comércio a retalho de carpetes, tapetes, cortinados e  revestimentos  para paredes e pavimentos, em estabelecimentos especializados	|	Retail sale of carpets, rugs, wall and floor coverings in specialised stores	|
|	47540	|	Comércio a retalho de electrodomésticos, em estabelecimentos especializados	|	Retail sale of electrical household appliances in specialised stores	|
|	47591	|	Comércio a retalho de mobiliário e artigos de iluminação, em estabelecimentos especializados	|	Retail sale of furniture, lighting equipment and household articles in specialised stores	|
|	47592	|	Comércio a retalho de louças, cutelaria e de outros artigos similares para uso doméstico, em estabelecimentos especializados	|	Retail sale of tableware, cutlery and other similar household articles in specialised stores	|
|	47593	|	Comércio a retalho de outros artigos para o lar, n.e., em estabelecimentos especializados	|	Retail sale of other household articles in specialised stores, n.e.c.	|
|	47610	|	Comércio a retalho de livros, em estabelecimentos especializados	|	Retail sale of books in specialised stores	|
|	47620	|	Comércio a retalho de jornais, revistas e artigos de papelaria, em estabelecimentos especializados	|	Retail sale of newspapers and stationery in specialised stores	|
|	47630	|	Comércio a retalho de  discos, CD, DVD, cassetes e similares, em estabelecimentos especializados	|	Retail sale of music and video recordings in specialised stores	|
|	47640	|	Comércio a retalho de artigos de desporto, de campismo e lazer, em estabelecimentos especializados	|	Retail sale of sporting equipment in specialised stores	|
|	47650	|	Comércio a retalho de jogos e brinquedos, em estabelecimentos especializados	|	Retail sale of games and toys in specialised stores	|
|	47711	|	Comércio a retalho de vestuário para adultos, em estabelecimentos especializados	|	Retail sale of adults? clothing in specialised stores	|
|	47712	|	Comércio a retalho de vestuário para bebés e crianças, em estabelecimentos especializados	|	Retail sale of children?s and infants? clothing in specialised stores	|
|	47721	|	Comércio a retalho de calçado, em estabelecimentos especializados	|	Retail sale of footwear in specialised stores 	|
|	47722	|	Comércio a retalho de marroquinaria e artigos de viagem, em estabelecimentos especializados	|	Retail sale of handbags and luggage in specialised stores	|
|	47730	|	Comércio a retalho de produtos farmacêuticos, em estabelecimentos especializados	|	Dispensing chemist in specialised stores	|
|	47740	|	Comércio a retalho de produtos médicos e ortopédicos, em estabelecimentos especializados	|	Retail sale of medical and orthopaedic goods in specialised stores	|
|	47750	|	Comércio a retalho de produtos cosméticos e de higiene, em estabelecimentos especializados	|	Retail sale of cosmetic and toilet articles in specialised stores	|
|	47761	|	Comércio a retalho de flores, plantas, sementes e  fertilizantes, em estabelecimentos especializados	|	Retail sale of flowers, plants, seeds and fertilisers in specialised stores	|
|	47762	|	Comércio a retalho de animais de companhia e respectivos alimentos, em estabelecimentos especializados	|	Retail sale of pet animals and pet food in specialised stores	|
|	47770	|	Comércio a retalho de relógios e de artigos de ourivesaria e joalharia, em estabelecimentos especializados	|	Retail sale of watches and jewellery in specialised stores	|
|	47781	|	Comércio a retalho de máquinas e de outro material de escritório, em estabelecimentos especializados	|	Retail sale of office machinery and other equipment  in specialised stores	|
|	47782	|	Comércio a retalho de material óptico, fotográfico, cinematográfico e de instrumentos de precisão, em estabelecimentos especializados	|	Retail sale of photographic, optical, cinematographic and precision equipment in specialised stores	|
|	47783	|	Comércio a retalho de combustíveis para uso doméstico, em estabelecimentos especializados	|	Retail sale of household fuel oil, bottled gas, coal and wood in specialised stores	|
|	47784	|	Comércio a retalho de outros produtos novos, em estabelecimentos especializados, n.e.	|	Other retail sale in specialised stores, n.e.c.	|
|	47790	|	Comércio a retalho de artigos em segunda mão, em estabelecimentos especializados	|	Retail sale of second-hand goods in stores	|
|	47810	|	Comércio a retalho em bancas, feiras e unidades móveis de venda, de produtos alimentares, bebidas e tabaco	|	Retail sale via stalls and markets of food, beverages and tobacco products	|
|	47820	|	Comércio a retalho em bancas, feiras e unidades móveis de venda, de têxteis, vestuário, calçado, malas e similares	|	Retail sale via stalls and markets of textiles, clothing and footwear	|
|	47890	|	Comércio a retalho em bancas, feiras e unidades móveis de venda, de outros produtos	|	Retail sale via stalls and markets of other goods	|
|	47910	|	Comércio a retalho por correspondência ou via Internet	|	Retail sale via mail order houses or via Internet	|
|	47990	|	Comércio a retalho por outros métodos, não efectuado em estabelecimentos, bancas, feiras ou unidades móveis de venda	|	Other retail sale not in stores, stalls or markets	|
|	49100	|	Transporte interurbano  de passageiros por caminho-de-ferro	|	Passenger rail transport, interurban	|
|	49200	|	Transporte de mercadorias por caminho-de-ferro	|	Freight rail transport	|
|	49310	|	Transportes terrestres, urbanos e suburbanos, de passageiros	|	Urban and suburban passenger land transport	|
|	49320	|	Transporte ocasional de passageiros em veículos ligeiros	|	Taxi operation	|
|	49391	|	Transporte interurbano em autocarros	|	Inter-urban passenger transportation by bus	|
|	49392	|	Outros transportes terrestres de passageiros diversos, n.e	|	Other miscellaneous land passenger transport, n.e.c.	|
|	49410	|	Transportes rodoviários de mercadorias	|	Freight transport by road	|
|	49420	|	Actividades de mudanças, por via rodoviária	|	Removal services	|
|	49500	|	Transportes por oleodutos ou gasodutos 	|	Transport via pipeline	|
|	50101	|	Transportes marítimos não costeiros de passageiros	|	Sea passenger water transport 	|
|	50102	|	Transportes costeiros e locais de passageiros	|	Coastal and local passenger water transport	|
|	50200	|	Transportes marítimos de mercadorias 	|	Sea and coastal freight water transport	|
|	50300	|	Transportes de passageiros por vias navegáveis interiores	|	Inland passenger water transport	|
|	50400	|	Transportes de mercadorias por vias navegáveis interiores	|	Inland freight water transport	|
|	51100	|	Transportes aéreos de passageiros	|	Passenger air transport	|
|	51210	|	Transportes aéreos de mercadorias	|	Freight air transport	|
|	51220	|	Transportes espaciais	|	Space transport	|
|	52101	|	Armazenagem frigorífica	|	Storage of frozen goods	|
|	52102	|	Armazenagem não frigorífica	|	Storage of non-frozen goods	|
|	52211	|	Gestão de infra-estruturas dos transportes terrestres	|	Management of the infraestructure for land transportation	|
|	52212	|	Assistência a veículos na estrada	|	Assistance activities to vehicles on the road	|
|	52213	|	Outras actividades auxiliares dos transportes terrestres	|	Other supporting land transport activities	|
|	52220	|	Actividades auxiliares dos transportes por água	|	Service activities incidental to water transportation	|
|	52230	|	Actividades auxiliares dos transportes aéreos	|	Service activities incidental to air transportation	|
|	52240	|	Manuseamento de carga	|	Cargo handling	|
|	52291	|	Organização do transporte	|	Transport organisation	|
|	52292	|	Agentes aduaneiros e similares de apoio ao transporte	|	Activities of customs clearance agents and similars	|
|	53100	|	Actividades postais sujeitas a obrigações do serviço universal	|	Postal activities under universal service obligation	|
|	53200	|	Outras actividades postais e de courier	|	Other postal and courier activities	|
|	55111	|	Hotéis com restaurante	|	Hotels with restaurant  	|
|	55112	|	Pensões com restaurante	|	Guest houses with restaurant	|
|	55113	|	Estalagens com restaurante	|	Inns with restaurant	|
|	55114	|	Pousadas com restaurante	|	Lodging-houses with restaurant	|
|	55115	|	Motéis com restaurante	|	Motels with restaurant	|
|	55116	|	Hotéis-Apartamentos com restaurante	|	Apartment-hotels with restaurant	|
|	55117	|	Aldeamentos turísticos com restaurante	|	Holiday villages with restaurant	|
|	55118	|	Apartamentos turísticos com restaurante	|	Holiday flats with restaurant	|
|	55119	|	Outros estabelecimentos hoteleiros com restaurante	|	Hotel and similar establishments with restaurant, n.e.c.	|
|	55121	|	Hotéis sem restaurante	|	Hotels without restaurant	|
|	55122	|	Pensões sem restaurante	|	Guest houses without restaurant	|
|	55123	|	Apartamentos turísticos sem restaurante	|	Holiday flats without restaurant	|
|	55124	|	Outros estabelecimentos hoteleiros sem restaurante	|	Hotel and similar establishments without restaurant, n.e.c.	|
|	55201	|	Alojamento mobilado para turistas	|	Letting services of short-stay furnished accommodation	|
|	55202	|	Turismo no espaço rural	|	Short-stay lodging in farmhouses 	|
|	55203	|	Colónias e campos de férias 	|	Holiday camps 	|
|	55204	|	Outros locais de alojamento de curta duração	|	Other short-stay lodging, n.e.c.	|
|	55300	|	Parques de campismo e de caravanismo	|	Camping grounds, recreational vehicle parks and trailer parks	|
|	55900	|	Outros locais de alojamento	|	Other accommodation	|
|	56101	|	Restaurantes tipo tradicional	|	Traditional restaurants 	|
|	56102	|	Restaurantes com lugares ao balcão	|	Snack-bars restaurants	|
|	56103	|	Restaurantes sem serviço de mesa	|	Self-service restaurants 	|
|	56104	|	Restaurantes típicos	|	Typical restaurants 	|
|	56105	|	Restaurantes com espaço de dança	|	Restaurants with dance floor 	|
|	56106	|	Confecção de refeições prontas a levar para casa	|	Confection of ready meals for take-away	|
|	56107	|	Restaurantes, n.e. (inclui actividades de restauração em meios móveis)	|	Restaurants and mobile food service activities n.e.c.	|
|	56210	|	Fornecimento de refeições para eventos 	|	Event catering activities	|
|	56290	|	Outras actividades de serviço  de refeições	|	Other food service activities	|
|	56301	|	Cafés	|	Cafés	|
|	56302	|	Bares	|	Bars	|
|	56303	|	Pastelarias e casas de chá	|	Pastries and tea houses	|
|	56304	|	Outros estabelecimentos de bebidas sem espectáculo	|	Other beverage establishments without entertainment	|
|	56305	|	Estabelecimentos de bebidas com espaço de dança 	|	Beverage establishments with room to dance	|
|	58110	|	Edição de livros	|	Book publishing	|
|	58120	|	Edição de listas  destinadas a consulta	|	Publishing of directories and mailing lists	|
|	58130	|	Edição de jornais	|	Publishing of newspapers	|
|	58140	|	Edição de revistas e de outras publicações periódicas	|	Publishing of journals and periodicals	|
|	58190	|	Outras actividades de edição	|	Other publishing activities	|
|	58210	|	Edição de jogos de computador	|	Publishing of computer games	|
|	58290	|	Edição de outros programas informáticos	|	Other software publishing	|
|	59110	|	Produção de filmes, de vídeos e de programas de televisão	|	Motion picture, video and television programme production activities	|
|	59120	|	Actividades técnicas de pós-produção para filmes, vídeos e programas de televisão	|	Motion picture, video and television programme post-production activities	|
|	59130	|	Distribuição de filmes, de vídeos e de programas de televisão	|	Motion picture, video and television programme distribution activities	|
|	59140	|	Projecção de filmes e de vídeos	|	Motion picture projection activities	|
|	59200	|	Actividades de gravação de som e edição de música	|	Sound recording and music publishing activities	|
|	60100	|	Actividades de rádio	|	Radio broadcasting	|
|	60200	|	Actividades de  televisão	|	Television programming and broadcasting activities	|
|	61100	|	Actividades de telecomunicações por fio	|	Wired telecommunications activities	|
|	61200	|	Actividades de telecomunicações sem fio	|	Wireless telecommunications activities	|
|	61300	|	Actividades de telecomunicações por satélite	|	Satellite telecommunications activities	|
|	61900	|	Outras actividades de telecomunicações	|	Other telecommunications activities	|
|	62010	|	Actividades de programação informática	|	Computer programming activities	|
|	62020	|	Actividades de consultoria em informática	|	Computer consultancy activities	|
|	62030	|	Gestão e exploração de equipamento informático	|	Computer facilities management activities	|
|	62090	|	Outras actividades  relacionadas com as tecnologias da informação e informática	|	Other information technology and computer service activities	|
|	63110	|	Actividades de processamento de dados, domiciliação de informação e actividades relacionadas	|	Data processing, hosting and related activities	|
|	63120	|	Portais Web	|	Web portals	|
|	63910	|	Actividades de agências de notícias	|	News agency activities	|
|	63990	|	Outras actividades dos serviços de informação, n.e.	|	Other information service activities n.e.c.	|
|	64110	|	Banco central	|	Central banking	|
|	64190	|	Outra intermediação monetária	|	Other monetary intermediation	|
|	64201	|	Actividades das sociedades gestoras de participações sociais financeiras	|	Activities of holding financial companies	|
|	64202	|	Actividades das sociedades gestoras de participações sociais não financeiras	|	Activities of holding non-financial companies	|
|	64300	|	Trusts, fundos e  entidades financeiras similares	|	Trusts, funds and similar financial entities	|
|	64910	|	Actividades de locação financeira	|	Financial leasing	|
|	64921	|	Actividades das instituições financeiras de crédito	|	Activities of credit institutions	|
|	64922	|	Actividades das sociedades financeiras para aquisições a crédito	|	Credit-purchase financing companies 	|
|	64923	|	Outras actividades de crédito, n.e.	|	Other credit granting n.e.c.	|
|	64991	|	Actividades de factoring	|	Factoring	|
|	64992	|	Outras actividades de serviços financeiros diversos , n.e.,excepto seguros e fundos de pensões	|	Other miscellaneous financial service activities, except insurance and pension funding n.e.c.	|
|	65111	|	Seguros de vida	|	Life insurance	|
|	65112	|	Outras actividades complementares de segurança social	|	Other additional activities for social security	|
|	65120	|	Seguros não vida	|	Non-life insurance	|
|	65200	|	Resseguros	|	Reinsurance	|
|	65300	|	Fundos de pensões e regimes profissionais complementares	|	Pension funding	|
|	66110	|	Administração de mercados financeiros	|	Administration of financial markets	|
|	66120	|	Actividades de negociação por conta de terceiros em valores mobiliários e outros instrumentos financeiros	|	Security and commodity contracts brokerage	|
|	66190	|	Outras actividades auxiliares de serviços financeiros, excepto seguros e fundos de pensões	|	Other activities auxiliary to financial services, except insurance and pension funding	|
|	66210	|	Actividades de avaliação de riscos e danos	|	Risk and damage evaluation	|
|	66220	|	Actividades de mediadores de seguros	|	Activities of insurance agents and brokers	|
|	66290	|	Outras actividades auxiliares de seguros e fundos de pensões	|	Other activities auxiliary to insurance and pension funding	|
|	66300	|	Actividades de gestão de fundos	|	Fund management activities	|
|	68100	|	Compra e venda de bens imobiliários	|	Buying and selling of own real estate	|
|	68200	|	Arrendamento de bens imobiliários	|	Renting and operating of own or leased real estate	|
|	68311	|	Actividades de mediação imobiliária	|	Activities of real estate mediation	|
|	68312	|	Actividades de angariação imobiliária	|	Raising real estate activities	|
|	68313	|	Actividades de avaliação imobiliária	|	Activities of real estate evaluation	|
|	68321	|	Administração de imóveis por conta de outrem	|	Management of real estate on behalf of others	|
|	68322	|	Administração de condomínios	|	Condominium management	|
|	69101	|	Actividades jurídicas	|	Legal activities	|
|	69102	|	Actividades dos cartórios notariais	|	Activities of notaries	|
|	69200	|	Actividades de contabilidade e auditoria	|		|
|	70100	|	Actividades das sedes sociais	|	Activities of head offices	|
|	70210	|	Actividades de relações públicas e comunicação	|	Public relations and communication activities	|
|	70220	|	Outras actividades de consultoria para os negócios e a gestão	|	Business and other management consultancy activities	|
|	71110	|	Actividades de arquitectura	|	Architectural activities 	|
|	71120	|	Actividades de engenharia e técnicas afins	|	Engineering activities and related technical consultancy	|
|	71200	|	Actividades de ensaios e análises técnicas	|	Technical testing and analysis	|
|	72110	|	Investigação e desenvolvimento em biotecnologia	|	Research and experimental development on biotechnology	|
|	72190	|	Outra investigação e desenvolvimento das ciências físicas e naturais	|	Other research and experimental development on natural sciences and engineering	|
|	72200	|	Investigação e desenvolvimento das ciências sociais e humanas	|	Research and experimental development on social sciences and humanities	|
|	73110	|	Agências de publicidade	|	Advertising agencies	|
|	73120	|	Actividades de representação nos meios de comunicação	|	Media representation	|
|	73200	|	Estudos de mercado e sondagens de opinião	|	Market research and public opinion polling	|
|	74100	|	Actividades de design	|	Specialised design activities	|
|	74200	|	Actividades fotográficas	|	Photographic activities	|
|	74300	|	Actividades de tradução e interpretação	|	Translation and interpretation activities	|
|	74900	|	Outras actividades de consultoria, científicas, técnicas e similares, n.e.	|	Other professional, scientific and technical activities n.e.c.	|
|	75000	|	Actividades veterinárias	|	Veterinary activities	|
|	77110	|	Aluguer de veículos automóveis ligeiros	|	Renting and leasing of cars and light motor vehicles	|
|	77120	|	Aluguer de veículos automóveis pesados	|	Renting and leasing of trucks	|
|	77210	|	Aluguer de bens  recreativos e desportivos	|	Renting and leasing of recreational and sports goods	|
|	77220	|	Aluguer de videocassetes e discos	|	Renting of video tapes and disks	|
|	77290	|	Aluguer de outros bens de uso pessoal e doméstico	|	Renting and leasing of other personal and household goods	|
|	77310	|	Aluguer de máquinas e equipamentos agrícolas	|	Renting and leasing of agricultural machinery and equipment	|
|	77320	|	Aluguer de máquinas e equipamentos para a construção e engenharia civil	|	Renting and leasing of construction and civil engineering machinery and equipment	|
|	77330	|	Aluguer de máquinas e equipamentos de escritório (inclui computadores)	|	Renting and leasing of office machinery and equipment (including computers)	|
|	77340	|	Aluguer de meios de transporte marítimo e fluvial	|	Renting and leasing of water transport equipment	|
|	77350	|	Aluguer de meios de transporte aéreo	|	Renting and leasing of air transport equipment	|
|	77390	|	Aluguer de outras máquinas e equipamentos, n.e.	|	Renting and leasing of other machinery, equipment and tangible goods n.e.c.	|
|	77400	|	Locação de propriedade intelectual e produtos similares, excepto direitos de autor	|	Leasing of intellectual property and similar products, except copyrighted works	|
|	78100	|	Actividades das empresas de selecção e colocação de pessoal	|	Activities of employment placement agencies	|
|	78200	|	Actividades das empresas de trabalho temporário	|	Temporary employment agency activities	|
|	78300	|	Outro fornecimento de recursos humanos	|	Other human resources provision	|
|	79110	|	Actividades das agências de viagem	|	Travel agency activities	|
|	79120	|	Actividades dos operadores turísticos	|	Tour operator activities	|
|	79900	|	Outros serviços de reservas e actividades relacionadas	|	Other reservation service and related activities	|
|	80100	|	Actividades de  segurança privada	|	Private security activities	|
|	80200	|	Actividades  relacionadas com sistemas de segurança	|	Security systems service activities	|
|	80300	|	Actividades de investigação	|	Investigation activities	|
|	81100	|	Actividades combinadas de apoio aos  edifícios	|	Combined facilities support activities	|
|	81210	|	Actividades de limpeza geral em edifícios	|	General cleaning of buildings	|
|	81220	|	Outras actividades de limpeza em edifícios e em equipamentos industriais	|	Other building and industrial cleaning activities	|
|	81291	|	Actividades de desinfecção, desratização e similares	|	Activities disinfection, rodent control and similar	|
|	81292	|	Outras actividades de limpeza, n.e.	|	Other cleaning activities n.e.c.	|
|	81300	|	Actividades de plantação e manutenção de jardins	|	Landscape service activities	|
|	82110	|	Actividades  combinadas de serviços administrativos	|	Combined office administrative service activities	|
|	82190	|	Execução de fotocópias, preparação de documentos e outras actividades especializadas de apoio administrativo	|	Photocopying, document preparation and other specialised office support activities	|
|	82200	|	Actividades dos centros de chamadas	|	Activities of call centres	|
|	82300	|	Organização de feiras, congressos e outros eventos similares	|	Organisation of conventions and trade shows	|
|	82910	|	Actividades de cobranças e avaliação de crédito	|	Activities of collection agencies and credit bureaus	|
|	82921	|	Engarrafamento de gases	|	Filling gas	|
|	82922	|	Outras actividades de embalagem	|	Other packaging activities	|
|	82990	|	Outras actividades de serviços de apoio prestados às empresas, n.e.	|	Other business support service activities n.e.c.	|
|	84111	|	Administração central	|	Central government	|
|	84112	|	Administração Regional Autónoma	|	Autonomous Regional administration	|
|	84113	|	Administração local	|	Local administration	|
|	84114	|	Actividades de apoio à administração pública	|	Support activities to the public administration	|
|	84121	|	Administração pública - actividades de saúde	|	Regulation of the activities of providing health care	|
|	84122	|	Administração pública - actividades de educação	|	Regulation of the activities of providing education	|
|	84123	|	Administração Pública - actividades da cultura, desporto, recreativas, ambiente, habitação e de outras actividades sociais, excepto segurança social obrigatória	|	Activities of culture, sports, entertainment, environment, housing and other social activities, except compulsory social security	|
|	84130	|	Administração pública - actividades económicas	|	Regulation of and contribution to more efficient operation of businesses	|
|	84210	|	Negócios estrangeiros	|	Foreign affairs	|
|	84220	|	Actividades de defesa	|	Defence activities	|
|	84230	|	Actividades de justiça	|	Justice and judicial activities	|
|	84240	|	Actividades de segurança e ordem pública	|	Public order and safety activities	|
|	84250	|	Actividades de protecção civil	|	Fire service activities	|
|	84300	|	Actividades de segurança social obrigatória	|	Compulsory social security activities	|
|	85100	|	Educação pré-escolar	|	Pre-primary education	|
|	85201	|	Ensino básico (1º  Ciclo)	|	Primary education (1st. Cycle) 	|
|	85202	|	Ensino básico (2º Ciclo)	|	Primary education (2nd. Cycle)	|
|	85310	|	Ensinos básico (3º Ciclo) e secundário geral	|	General secondary education 	|
|	85320	|	Ensinos secundário tecnológico, artístico  e profissional	|	Technical and vocational secondary education 	|
|	85410	|	Ensino pós-secundário não superior	|	Post-secondary non-tertiary education	|
|	85420	|	Ensino superior	|	Tertiary education	|
|	85510	|	Ensinos desportivo e recreativo	|	Sports and recreation education	|
|	85520	|	Ensino de actividades culturais	|	Cultural education	|
|	85530	|	Escolas de condução e pilotagem	|	Driving school activities	|
|	85591	|	Formação profissional	|	Professional formation	|
|	85592	|	Escolas de línguas	|	Schools of languages	|
|	85593	|	Outras actividades educativas, n.e.	|	Other education activities, n.e.c.	|
|	85600	|	Actividades de serviços de apoio à educação	|	Educational support activities	|
|	86100	|	Actividades dos estabelecimentos de saúde com internamento	|	Hospital activities	|
|	86210	|	Actividades de prática médica de clínica geral, em ambulatório	|	General medical practice activities	|
|	86220	|	Actividades de prática médica de clínica especializada, em ambulatório	|	Specialist medical practice activities	|
|	86230	|	Actividades  de medicina dentária e odontologia	|	Dental practice activities	|
|	86901	|	Laboratórios de análises clínicas	|	Laboratories of clinical analyses	|
|	86902	|	Actividades de ambulâncias	|	Activities of ambulances	|
|	86903	|	Actividades de enfermagem	|	Activities of nursing 	|
|	86904	|	Centros de recolha e bancos de órgãos	|	Collection centers and organs banks	|
|	86905	|	Actividades termais	|	Thermal activities	|
|	86906	|	Outras actividades de saúde humana, n.e.	|	Other human health activities n.e.c.	|
|	87100	|	Actividades dos estabelecimentos de cuidados continuados integrados,  com alojamento	|	Residential nursing care activities	|
|	87200	|	Actividades dos estabelecimentos para pessoas com  doença do foro mental e do abuso de drogas, com alojamento	|	Residential care activities for mental retardation, mental health and substance abuse	|
|	87301	|	Actividades de apoio social para pessoas idosas, com alojamento	|	Residential care activities for the elderly	|
|	87302	|	Actividades de apoio social para pessoas com deficiência, com alojamento	|	Residential care activities for disabled	|
|	87901	|	Actividades de apoio social para crianças e jovens, com alojamento	|	Residential care activities for children and young	|
|	87902	|	Actividades de apoio social com alojamento, n.e.	|	Other residential care activities n.e.c.	|
|	88101	|	Actividades de apoio social para pessoas idosas, sem alojamento	|	Social work activities without accommodation for the elderly 	|
|	88102	|	Actividades de apoio social para pessoas com deficiência, sem alojamento	|	Social work activities without accommodation for disabled	|
|	88910	|	Actividades de cuidados  para crianças, sem alojamento	|	Child day-care activities	|
|	88990	|	Outras actividades de apoio social sem alojamento, n.e.	|	Other social work activities without accommodation n.e.c.	|
|	90010	|	Actividades das artes do espectáculo	|	Performing arts	|
|	90020	|	Actividades de apoio às artes do espectáculo	|	Support activities to performing arts	|
|	90030	|	Criação artística e literária	|	Artistic creation	|
|	90040	|	Exploração de salas de espectáculos e actividades conexas	|	Operation of arts facilities	|
|	91011	|	Actividades das bibliotecas	|	Library activities	|
|	91012	|	Actividades dos arquivos	|	Archives activities	|
|	91020	|	Actividades dos museus	|	Museums activities	|
|	91030	|	Actividades dos sítios e  monumentos históricos	|	Operation of historical sites and buildings and similar visitor attractions	|
|	91041	|	Actividades dos jardins  zoológicos, botânicos e aquários	|	Botanical and zoological gardens activities	|
|	91042	|	Actividade dos parques e reservas naturais 	|	Parks and nature reserves activities	|
|	92000	|	Lotarias e outros jogos de aposta	|	Gambling and betting activities	|
|	93110	|	Gestão de instalações desportivas	|	Operation of sports facilities	|
|	93120	|	Actividades dos clubes desportivos	|	Activities of sports clubs	|
|	93130	|	Actividades de ginásio  (fitness)	|	Fitness facilities	|
|	93191	|	Organismos reguladores das actividades desportivas	|	Regulatory bodies of sport	|
|	93192	|	Outras actividades desportivas, n.e.	|	Other sports activities n.e.c.	|
|	93210	|	Actividades dos  parques de diversão e temáticos	|	Activities of amusement parks and theme parks	|
|	93291	|	Actividades tauromáquicas	|	Activities bullfighting	|
|	93292	|	Actividades dos portos de recreio (marinas)	|	Activities of recreation ports (marinas)	|
|	93293	|	Organização de actividades de animação turística	|	Organization of recreational tourism activities	|
|	93294	|	Outras actividades de diversão e recreativas, n.e.	|	Other amusement and recreation activities n.e.c.	|
|	93295	|	Outras atividades de diversão itinerantes (Lei n.º 66/2018, de 3 de dezembro)	|	Other itinerant amusement and recreational activities (Law No 66/2018, of 3 December)	|
|	94110	|	Actividades de organizações económicas e patronais	|	Activities of business and employers membership organisations	|
|	94120	|	Actividades de organizações profissionais	|	Activities of professional membership organisations	|
|	94200	|	Actividades de organizações sindicais	|	Activities of trade unions	|
|	94910	|	Actividades de organizações religiosas	|	Activities of religious organisations	|
|	94920	|	Actividades de organizações políticas	|	Activities of political organisations	|
|	94991	|	Associações culturais e recreativas	|	Cultural or recreational associations 	|
|	94992	|	Associações de defesa do ambiente	|	Environmental protection associations	|
|	94993	|	Associações de juventude e de estudantes	|	Youth and student associations	|
|	94994	|	Associações de pais e encarregados de educação	|	Associations of parents and guardians	|
|	94995	|	Outras actividades associativas, n.e.	|	Other activities of associations, n.e.c.	|
|	95110	|	Reparação  de computadores e de equipamento periférico	|	Repair of computers and peripheral equipment	|
|	95120	|	Reparação de equipamento de comunicação	|	Repair of communication equipment	|
|	95210	|	Reparação   de televisores e de outros bens de consumo similares	|	Repair of consumer electronics	|
|	95220	|	Reparação de electrodomésticos e de outros equipamentos de uso doméstico e para jardim	|	Repair of household appliances and home and garden equipment	|
|	95230	|	Reparação de calçado e de artigos de couro	|	Repair of footwear and leather goods	|
|	95240	|	Reparação de mobiliário e similares, de uso doméstico	|	Repair of furniture and home furnishings	|
|	95250	|	Reparação de relógios e de artigos de joalharia	|	Repair of watches, clocks and jewellery	|
|	95290	|	Reparação de outros bens de uso pessoal e doméstico	|	Repair of other personal and household goods	|
|	96010	|	Lavagem e limpeza a seco de têxteis e peles	|	Washing and (dry-)cleaning of textile and fur products	|
|	96021	|	Salões de cabeleireiro	|	Hairdressing 	|
|	96022	|	Institutos de beleza	|	Beauty parlours	|
|	96030	|	Actividades funerárias e conexas	|	Funeral and related activities	|
|	96040	|	Actividades de bem-estar físico	|	Physical well-being activities	|
|	96091	|	Actividades de tatuagem e similares	|	Activities of tattooing and similar	|
|	96092	|	Actividades dos serviços para animais de companhia	|	Service activities for pets	|
|	96093	|	Outras actividades de serviços pessoais diversas, n.e.	|	Other personal miscellaneous service activities n.e.c.	|
|	97000	|	Actividades das famílias empregadoras de pessoal doméstico	|	Activities of households as employers of domestic personnel	|
|	98100	|	Actividades de produção de bens pelas famílias para uso próprio	|	Undifferentiated goods-producing activities of private households for own use	|
|	98200	|	Actividades de produção de serviços pelas famílias para uso próprio	|	Undifferentiated service-producing activities of private households for own use	|
|	99000	|	Actividades dos organismos internacionais e outras instituições extra-territoriais	|	Activities of extraterritorial organizations and bodies	|


[Return](#table-of-contents)


## District

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	1	|	Aveiro	|	Aveiro	|
|	2	|	Beja	|	Beja	|
|	3	|	Braga	|	Braga	|
|	4	|	Bragança	|	Bragança	|
|	5	|	Castelo Branco	|	Castelo Branco	|
|	6	|	Coimbra	|	Coimbra	|
|	7	|	Évora	|	Évora	|
|	8	|	Faro	|	Faro	|
|	9	|	Guarda	|	Guarda	|
|	10	|	Leiria	|	Leiria	|
|	11	|	Lisboa	|	Lisboa	|
|	12	|	Portalegre	|	Portalegre	|
|	13	|	Porto	|	Porto	|
|	14	|	Santarém	|	Santarém	|
|	15	|	Setúbal	|	Setúbal	|
|	16	|	Viana do Castelo	|	Viana do Castelo	|
|	17	|	Vila Real	|	Vila Real	|
|	18	|	Viseu	|	Viseu	|
|	19	|	Angra do Heroísm	|	Angra do Heroísm	|
|	20	|	Horta	|	Horta	|
|	21	|	Ponta Delgada	|	Ponta Delgada	|
|	22	|	Funchal	|	Funchal	|
|	31	|	Ilha da Madeira	|	Ilha da Madeira	|
|	32	|	Ilha de Porto Santo	|	Ilha de Porto Santo	|
|	41	|	Ilha de Santa Maria	|	Ilha de Santa Maria	|
|	42	|	Ilha de São Miguel	|	Ilha de São Miguel	|
|	43	|	Ilha Terceira	|	Ilha Terceira	|
|	44	|	Ilha Graciosa	|	Ilha Graciosa	|
|	45	|	Ilha de São Jorge	|	Ilha de São Jorge	|
|	46	|	Ilha do Pico	|	Ilha do Pico	|
|	47	|	Ilha do Faial	|	Ilha do Faial	|
|	48	|	Ilha das Flores	|	Ilha das Flores	|
|	49	|	Ilha do Corvo	|	Ilha do Corvo	|
|	88	|	Estrangeiro	|	Foreign	|
|	97	|	Desconhecido	|	Unknown	|
|	98	|	Não especificado	|	Not specified	|
|	99	|	Não aplicável	|	Not applicable	|
|	3999	|	Off-shore de Madeira	|	Off-shore de Madeira	|
|	4999	|	Off-shore dos Açores	|	Off-shore dos Açores	|


[Return](#table-of-contents)


## Municipality

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	101	|	Águeda	|	Águeda	|
|	102	|	Albergaria-a-Velha	|	Albergaria-a-Velha	|
|	103	|	Anadia	|	Anadia	|
|	104	|	Arouca	|	Arouca	|
|	105	|	Aveiro	|	Aveiro	|
|	106	|	Castelo de Paiva	|	Castelo de Paiva	|
|	107	|	Espinho	|	Espinho	|
|	108	|	Estarreja	|	Estarreja	|
|	109	|	Santa Maria da Feira	|	Santa Maria da Feira	|
|	110	|	Ílhavo	|	Ílhavo	|
|	111	|	Mealhada	|	Mealhada	|
|	112	|	Murtosa	|	Murtosa	|
|	113	|	Oliveira de Azeméis	|	Oliveira de Azeméis	|
|	114	|	Oliveira do Bairro	|	Oliveira do Bairro	|
|	115	|	Ovar	|	Ovar	|
|	116	|	São João da Madeira	|	São João da Madeira	|
|	117	|	Sever do Vouga	|	Sever do Vouga	|
|	118	|	Vagos	|	Vagos	|
|	119	|	Vale de Cambra	|	Vale de Cambra	|
|	201	|	Aljustrel	|	Aljustrel	|
|	202	|	Almodôvar	|	Almodôvar	|
|	203	|	Alvito	|	Alvito	|
|	204	|	Barrancos	|	Barrancos	|
|	205	|	Beja	|	Beja	|
|	206	|	Castro Verde	|	Castro Verde	|
|	207	|	Cuba	|	Cuba	|
|	208	|	Ferreira do Alentejo	|	Ferreira do Alentejo	|
|	209	|	Mértola	|	Mértola	|
|	210	|	Moura	|	Moura	|
|	211	|	Odemira	|	Odemira	|
|	212	|	Ourique	|	Ourique	|
|	213	|	Serpa	|	Serpa	|
|	214	|	Vidigueira	|	Vidigueira	|
|	301	|	Amares	|	Amares	|
|	302	|	Barcelos	|	Barcelos	|
|	303	|	Braga	|	Braga	|
|	304	|	Cabeceiras de Basto	|	Cabeceiras de Basto	|
|	305	|	Celorico de Basto	|	Celorico de Basto	|
|	306	|	Esposende	|	Esposende	|
|	307	|	Fafe	|	Fafe	|
|	308	|	Guimarães	|	Guimarães	|
|	309	|	Póvoa de Lanhoso	|	Póvoa de Lanhoso	|
|	310	|	Terras de Bouro	|	Terras de Bouro	|
|	311	|	Vieira do Minho	|	Vieira do Minho	|
|	312	|	Vila Nova de Famalicão	|	Vila Nova de Famalicão	|
|	313	|	Vila Verde	|	Vila Verde	|
|	314	|	Vizela	|	Vizela	|
|	401	|	Alfândega da Fé	|	Alfândega da Fé	|
|	402	|	Bragança	|	Bragança	|
|	403	|	Carrazeda de Ansiães	|	Carrazeda de Ansiães	|
|	404	|	Freixo de Espada à Cinta	|	Freixo de Espada à Cinta	|
|	405	|	Macedo de Cavaleiros	|	Macedo de Cavaleiros	|
|	406	|	Miranda do Douro	|	Miranda do Douro	|
|	407	|	Mirandela	|	Mirandela	|
|	408	|	Mogadouro	|	Mogadouro	|
|	409	|	Torre de Moncorvo	|	Torre de Moncorvo	|
|	410	|	Vila Flor	|	Vila Flor	|
|	411	|	Vimioso	|	Vimioso	|
|	412	|	Vinhais	|	Vinhais	|
|	501	|	Belmonte	|	Belmonte	|
|	502	|	Castelo Branco	|	Castelo Branco	|
|	503	|	Covilhã	|	Covilhã	|
|	504	|	Fundão	|	Fundão	|
|	505	|	Idanha-a-Nova	|	Idanha-a-Nova	|
|	506	|	Oleiros	|	Oleiros	|
|	507	|	Penamacor	|	Penamacor	|
|	508	|	Proença-a-Nova	|	Proença-a-Nova	|
|	509	|	Sertã	|	Sertã	|
|	510	|	Vila de Rei	|	Vila de Rei	|
|	511	|	Vila Velha de Ródão	|	Vila Velha de Ródão	|
|	601	|	Arganil	|	Arganil	|
|	602	|	Cantanhede	|	Cantanhede	|
|	603	|	Coimbra	|	Coimbra	|
|	604	|	Condeixa-a-Nova	|	Condeixa-a-Nova	|
|	605	|	Figueira da Foz	|	Figueira da Foz	|
|	606	|	Góis	|	Góis	|
|	607	|	Lousã	|	Lousã	|
|	608	|	Mira	|	Mira	|
|	609	|	Miranda do Corvo	|	Miranda do Corvo	|
|	610	|	Montemor-o-Velho	|	Montemor-o-Velho	|
|	611	|	Oliveira do Hospital	|	Oliveira do Hospital	|
|	612	|	Pampilhosa da Serra	|	Pampilhosa da Serra	|
|	613	|	Penacova	|	Penacova	|
|	614	|	Penela	|	Penela	|
|	615	|	Soure	|	Soure	|
|	616	|	Tábua	|	Tábua	|
|	617	|	Vila Nova de Poiares	|	Vila Nova de Poiares	|
|	701	|	Alandroal	|	Alandroal	|
|	702	|	Arraiolos	|	Arraiolos	|
|	703	|	Borba	|	Borba	|
|	704	|	Estremoz	|	Estremoz	|
|	705	|	Évora	|	Évora	|
|	706	|	Montemor-o-Novo	|	Montemor-o-Novo	|
|	707	|	Mora	|	Mora	|
|	708	|	Mourão	|	Mourão	|
|	709	|	Portel	|	Portel	|
|	710	|	Redondo	|	Redondo	|
|	711	|	Reguengos de Monsaraz	|	Reguengos de Monsaraz	|
|	712	|	Vendas Novas	|	Vendas Novas	|
|	713	|	Viana do Alentejo	|	Viana do Alentejo	|
|	714	|	Vila Viçosa	|	Vila Viçosa	|
|	801	|	Albufeira	|	Albufeira	|
|	802	|	Alcoutim	|	Alcoutim	|
|	803	|	Aljezur	|	Aljezur	|
|	804	|	Castro Marim	|	Castro Marim	|
|	805	|	Faro	|	Faro	|
|	806	|	Lagoa	|	Lagoa	|
|	807	|	Lagos	|	Lagos	|
|	808	|	Loulé	|	Loulé	|
|	809	|	Monchique	|	Monchique	|
|	810	|	Olhão	|	Olhão	|
|	811	|	Portimão	|	Portimão	|
|	812	|	São Brás de Alportel	|	São Brás de Alportel	|
|	813	|	Silves	|	Silves	|
|	814	|	Tavira	|	Tavira	|
|	815	|	Vila do Bispo	|	Vila do Bispo	|
|	816	|	Vila Real de Santo António	|	Vila Real de Santo António	|
|	901	|	Aguiar da Beira	|	Aguiar da Beira	|
|	902	|	Almeida	|	Almeida	|
|	903	|	Celorico da Beira	|	Celorico da Beira	|
|	904	|	Figueira de Castelo Rodrigo	|	Figueira de Castelo Rodrigo	|
|	905	|	Fornos de Algodres	|	Fornos de Algodres	|
|	906	|	Gouveia	|	Gouveia	|
|	907	|	Guarda	|	Guarda	|
|	908	|	Manteigas	|	Manteigas	|
|	909	|	Mêda	|	Mêda	|
|	910	|	Pinhel	|	Pinhel	|
|	911	|	Sabugal	|	Sabugal	|
|	912	|	Seia	|	Seia	|
|	913	|	Trancoso	|	Trancoso	|
|	914	|	Vila Nova de Foz Côa	|	Vila Nova de Foz Côa	|
|	1001	|	Alcobaça	|	Alcobaça	|
|	1002	|	Alvaiázere	|	Alvaiázere	|
|	1003	|	Ansião	|	Ansião	|
|	1004	|	Batalha	|	Batalha	|
|	1005	|	Bombarral	|	Bombarral	|
|	1006	|	Caldas da Rainha	|	Caldas da Rainha	|
|	1007	|	Castanheira de Pêra	|	Castanheira de Pêra	|
|	1008	|	Figueiró dos Vinhos	|	Figueiró dos Vinhos	|
|	1009	|	Leiria	|	Leiria	|
|	1010	|	Marinha Grande	|	Marinha Grande	|
|	1011	|	Nazaré	|	Nazaré	|
|	1012	|	Óbidos	|	Óbidos	|
|	1013	|	Pedrógão Grande	|	Pedrógão Grande	|
|	1014	|	Peniche	|	Peniche	|
|	1015	|	Pombal	|	Pombal	|
|	1016	|	Porto de Mós	|	Porto de Mós	|
|	1101	|	Alenquer	|	Alenquer	|
|	1102	|	Arruda dos Vinhos	|	Arruda dos Vinhos	|
|	1103	|	Azambuja	|	Azambuja	|
|	1104	|	Cadaval	|	Cadaval	|
|	1105	|	Cascais	|	Cascais	|
|	1106	|	Lisboa	|	Lisboa	|
|	1107	|	Loures	|	Loures	|
|	1108	|	Lourinhã	|	Lourinhã	|
|	1109	|	Mafra	|	Mafra	|
|	1110	|	Oeiras	|	Oeiras	|
|	1111	|	Sintra	|	Sintra	|
|	1112	|	Sobral de Monte Agraço	|	Sobral de Monte Agraço	|
|	1113	|	Torres Vedras	|	Torres Vedras	|
|	1114	|	Vila Franca de Xira	|	Vila Franca de Xira	|
|	1115	|	Amadora	|	Amadora	|
|	1116	|	Odivelas	|	Odivelas	|
|	1201	|	Alter do Chão	|	Alter do Chão	|
|	1202	|	Arronches	|	Arronches	|
|	1203	|	Avis	|	Avis	|
|	1204	|	Campo Maior	|	Campo Maior	|
|	1205	|	Castelo de Vide	|	Castelo de Vide	|
|	1206	|	Crato	|	Crato	|
|	1207	|	Elvas	|	Elvas	|
|	1208	|	Fronteira	|	Fronteira	|
|	1209	|	Gavião	|	Gavião	|
|	1210	|	Marvão	|	Marvão	|
|	1211	|	Monforte	|	Monforte	|
|	1212	|	Nisa	|	Nisa	|
|	1213	|	Ponte de Sor	|	Ponte de Sor	|
|	1214	|	Portalegre	|	Portalegre	|
|	1215	|	Sousel	|	Sousel	|
|	1301	|	Amarante	|	Amarante	|
|	1302	|	Baião	|	Baião	|
|	1303	|	Felgueiras	|	Felgueiras	|
|	1304	|	Gondomar	|	Gondomar	|
|	1305	|	Lousada	|	Lousada	|
|	1306	|	Maia	|	Maia	|
|	1307	|	Marco de Canaveses	|	Marco de Canaveses	|
|	1308	|	Matosinhos	|	Matosinhos	|
|	1309	|	Paços de Ferreira	|	Paços de Ferreira	|
|	1310	|	Paredes	|	Paredes	|
|	1311	|	Penafiel	|	Penafiel	|
|	1312	|	Porto	|	Porto	|
|	1313	|	Póvoa de Varzim	|	Póvoa de Varzim	|
|	1314	|	Santo Tirso	|	Santo Tirso	|
|	1315	|	Valongo	|	Valongo	|
|	1316	|	Vila do Conde	|	Vila do Conde	|
|	1317	|	Vila Nova de Gaia	|	Vila Nova de Gaia	|
|	1318	|	Trofa	|	Trofa	|
|	1401	|	Abrantes	|	Abrantes	|
|	1402	|	Alcanena	|	Alcanena	|
|	1403	|	Almeirim	|	Almeirim	|
|	1404	|	Alpiarça	|	Alpiarça	|
|	1405	|	Benavente	|	Benavente	|
|	1406	|	Cartaxo	|	Cartaxo	|
|	1407	|	Chamusca	|	Chamusca	|
|	1408	|	Constância	|	Constância	|
|	1409	|	Coruche	|	Coruche	|
|	1410	|	Entroncamento	|	Entroncamento	|
|	1411	|	Ferreira do Zêzere	|	Ferreira do Zêzere	|
|	1412	|	Golegã	|	Golegã	|
|	1413	|	Mação	|	Mação	|
|	1414	|	Rio Maior	|	Rio Maior	|
|	1415	|	Salvaterra de Magos	|	Salvaterra de Magos	|
|	1416	|	Santarém	|	Santarém	|
|	1417	|	Sardoal	|	Sardoal	|
|	1418	|	Tomar	|	Tomar	|
|	1419	|	Torres Novas	|	Torres Novas	|
|	1420	|	Vila Nova da Barquinha	|	Vila Nova da Barquinha	|
|	1421	|	Ourém	|	Ourém	|
|	1501	|	Alcácer do Sal	|	Alcácer do Sal	|
|	1502	|	Alcochete	|	Alcochete	|
|	1503	|	Almada	|	Almada	|
|	1504	|	Barreiro	|	Barreiro	|
|	1505	|	Grândola	|	Grândola	|
|	1506	|	Moita	|	Moita	|
|	1507	|	Montijo	|	Montijo	|
|	1508	|	Palmela	|	Palmela	|
|	1509	|	Santiago do Cacém	|	Santiago do Cacém	|
|	1510	|	Seixal	|	Seixal	|
|	1511	|	Sesimbra	|	Sesimbra	|
|	1512	|	Setúbal	|	Setúbal	|
|	1513	|	Sines	|	Sines	|
|	1601	|	Arcos de Valdevez	|	Arcos de Valdevez	|
|	1602	|	Caminha	|	Caminha	|
|	1603	|	Melgaço	|	Melgaço	|
|	1604	|	Monção	|	Monção	|
|	1605	|	Paredes de Coura	|	Paredes de Coura	|
|	1606	|	Ponte da Barca	|	Ponte da Barca	|
|	1607	|	Ponte de Lima	|	Ponte de Lima	|
|	1608	|	Valença	|	Valença	|
|	1609	|	Viana do Castelo	|	Viana do Castelo	|
|	1610	|	Vila Nova de Cerveira	|	Vila Nova de Cerveira	|
|	1701	|	Alijó	|	Alijó	|
|	1702	|	Boticas	|	Boticas	|
|	1703	|	Chaves	|	Chaves	|
|	1704	|	Mesão Frio	|	Mesão Frio	|
|	1705	|	Mondim de Basto	|	Mondim de Basto	|
|	1706	|	Montalegre	|	Montalegre	|
|	1707	|	Murça	|	Murça	|
|	1708	|	Peso da Régua	|	Peso da Régua	|
|	1709	|	Ribeira de Pena	|	Ribeira de Pena	|
|	1710	|	Sabrosa	|	Sabrosa	|
|	1711	|	Santa Marta de Penaguião	|	Santa Marta de Penaguião	|
|	1712	|	Valpaços	|	Valpaços	|
|	1713	|	Vila Pouca de Aguiar	|	Vila Pouca de Aguiar	|
|	1714	|	Vila Real	|	Vila Real	|
|	1801	|	Armamar	|	Armamar	|
|	1802	|	Carregal do Sal	|	Carregal do Sal	|
|	1803	|	Castro Daire	|	Castro Daire	|
|	1804	|	Cinfães	|	Cinfães	|
|	1805	|	Lamego	|	Lamego	|
|	1806	|	Mangualde	|	Mangualde	|
|	1807	|	Moimenta da Beira	|	Moimenta da Beira	|
|	1808	|	Mortágua	|	Mortágua	|
|	1809	|	Nelas	|	Nelas	|
|	1810	|	Oliveira de Frades	|	Oliveira de Frades	|
|	1811	|	Penalva do Castelo	|	Penalva do Castelo	|
|	1812	|	Penedono	|	Penedono	|
|	1813	|	Resende	|	Resende	|
|	1814	|	Santa Comba Dão	|	Santa Comba Dão	|
|	1815	|	São João da Pesqueira	|	São João da Pesqueira	|
|	1816	|	São Pedro do Sul	|	São Pedro do Sul	|
|	1817	|	Sátão	|	Sátão	|
|	1818	|	Sernancelhe	|	Sernancelhe	|
|	1819	|	Tabuaço	|	Tabuaço	|
|	1820	|	Tarouca	|	Tarouca	|
|	1821	|	Tondela	|	Tondela	|
|	1822	|	Vila Nova de Paiva	|	Vila Nova de Paiva	|
|	1823	|	Viseu	|	Viseu	|
|	1824	|	Vouzela	|	Vouzela	|
|	1901	|	Angra do Heroísmo	|	Angra do Heroísmo	|
|	1902	|	Calheta	|	Calheta	|
|	1903	|	Santa Cruz da Graciosa	|	Santa Cruz da Graciosa	|
|	1904	|	Velas	|	Velas	|
|	1905	|	Vila Praia da Vitoria	|	Vila Praia da Vitoria	|
|	2001	|	Corvo	|	Corvo	|
|	2002	|	Horta	|	Horta	|
|	2003	|	Lajes das Flores	|	Lajes das Flores	|
|	2004	|	Lajes do Pico	|	Lajes do Pico	|
|	2005	|	Madalena	|	Madalena	|
|	2006	|	Santa Cruz das Flores	|	Santa Cruz das Flores	|
|	2007	|	São Roque do Pico	|	São Roque do Pico	|
|	2101	|	Lagoa	|	Lagoa	|
|	2102	|	Nordeste	|	Nordeste	|
|	2103	|	Ponta Delgada	|	Ponta Delgada	|
|	2104	|	Povoação	|	Povoação	|
|	2105	|	Ribeira Grande	|	Ribeira Grande	|
|	2106	|	Vila Franca de Campo	|	Vila Franca de Campo	|
|	2107	|	Vila do Porto	|	Vila do Porto	|
|	2201	|	Calheta	|	Calheta	|
|	2202	|	Câmara de Lobos	|	Câmara de Lobos	|
|	2203	|	Funchal	|	Funchal	|
|	2204	|	Machico	|	Machico	|
|	2205	|	Ponta do Sol	|	Ponta do Sol	|
|	2206	|	Porto Moniz	|	Porto Moniz	|
|	2207	|	Porto Santo	|	Porto Santo	|
|	2208	|	Ribeira Brava	|	Ribeira Brava	|
|	2209	|	Santa Cruz	|	Santa Cruz	|
|	2210	|	Santana	|	Santana	|
|	2211	|	São Vicente	|	São Vicente	|
|	998	|	Não Especificado	|	Not specified	|
|	997	|	Desconhecido	|	Unknown	|


[Return](#table-of-contents)



## Institutional Sector SEC 95

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	-99999998	|	Não specificado	|	Not specified	|
|	317000196	|	Sector Residente	|	Resident sector	|
|	317000247	|	Sociedades e fundos de titularização de crédito	|	Credit securitization companies and funds	|
|	317000210	|	Particulares, incluindo emigrantes	|	Households, including emigrants	|
|	317000003	|	Sector financeiro	|	Financial sector	|
|	317000007	|	Instituições financeiras monetárias	|	Monetary financial institutions	|
|	317000075	|	Auxiliares de seguros	|	Insurance ancillary workers	|
|	317000011	|	Banco de Portugal	|	Banco de Portugal	|
|	317000015	|	Outras instituições financeiras monetárias	|	Other monetary financial institutions	|
|	317000018	|	Tipo 1	|	Type 1	|
|	317000020	|	Fundos do mercado monetário	|	Money Market Funds	|
|	317000025	|	Tipo 2	|	Type 2	|
|	317000027	|	Bancos	|	Banks	|
|	317000212	|	Bancos centrais da União Monetária e outras IFM	|	National central banks of monetary union countries and other MFIs	|
|	317000029	|	Caixas de crédito agrícola mútuo	|	Mutual agricultural credit banks	|
|	317000220	|	Autoridades Monetárias	|	Monetary Authorities	|
|	317000035	|	Instituições financeiras não monetárias	|	Non-monetary financial institutions	|
|	317000032	|	Caixas económicas	|	Savings banks	|
|	317000039	|	Outros intermediários financeiros e auxiliares financeiros	|	Other Financial Intermediaries and Financial Auxiliaries	|
|	317000237	|	Contrapartes centrais	|	Central counterparties	|
|	317000043	|	Outros Intermediários Financeiros	|	Financial Intermediaries, except Insurance Corporations and Pension Funds	|
|	317000244	|	Contrapartes centrais	|	Central counterparties	|
|	317000236	|	Dos quais Instituições financeiras monetárias do Sector público	|	Public monetary financial institutions 	|
|	317000248	|	Dos quais Instituições financeiras não monetárias do Sector público	|	Public non-monetary financial institutions 	|
|	317000243	|	Dos quais Não Residentes do Sector público	|	Non-residents of the public sector	|
|	317000240	|	Dos quais Outros intermediários financeiros e auxiliares financeiros do Sector público	|	Other financial intermediaries and financial auxiliaries of the public sector	|
|	317000241	|	Dos quais Sociedades de seguros e fundos de pensões do Sector público	|	Insurance companies and pension funds of the public sector 	|
|	317000242	|	Dos quais Sociedades não financeiras do Sector público	|	Non-finanical companies of the public sector	|
|	317000252	|	Empresários em nome individual residentes na União Monetária	|	Individual entrepreneurs residing in Monetary Union	|
|	317000141	|	Famílias - Outros	|	Households - others	|
|	317000103	|	Fundos autónomos	|	Autonomous funds	|
|	317000222	|	Fundos e sociedades Especiais de Investimento	|	Special Investment Funds	|
|	317000056	|	Fundos e sociedades de investimento imobiliário	|	Real Estate Mutual Funds	|
|	317000057	|	Sociedades de capital de risco	|	Risk Capital Companies	|
|	317000058	|	Sociedades de factoring	|	Factoring Companies	|
|	317000059	|	Sociedades de locação financeira	|	Leasing Companies	|
|	317000060	|	Sociedades financeiras de corretagem	|	Dealers	|
|	317000061	|	Sociedades financeiras para aquisições a crédito	|	Credit-Purchase Financing Companies	|
|	317000062	|	Sociedades gestoras de participações sociais (do sector financeiro)	|	Financial Holding Companies	|
|	317000055	|	Fundos de Capital de Risco e FRIE	|	Venture capital funds and FRIE	|
|	317000064	|	Sociedades de desenvolvimento regional	|	Regional Development Companies	|
|	317000246	|	Fundos de titularização de créditos	|	Credit securitization funds	|
|	317000066	|	Sociedades de investimento	|	Investment Companies	|
|	317000067	|	Sociedades emitentes ou gestoras de cartões de crédito	|	Credit Card Issuing or Managing Companies	|
|	317000048	|	Fundos e sociedades de acções	|	Equity funds	|
|	317000069	|	Sociedades de titularização de créditos	|	Securitization Companies	|
|	317000219	|	Fundos de titularização de créditos	|	Securitisation Funds	|
|	317000218	|	Sociedades de garantia mútua	|	Mutual Guarantee Societies	|
|	317000217	|	Instituições financeiras de crédito	|	Credit Financial Institutions	|
|	317000070	|	Auxiliares Financeiros	|	Financial Auxiliaries	|
|	317000074	|	Agências de câmbios	|	Exchange Offices	|
|	317000053	|	Fundos e sociedades de fundos	|	Fund of funds	|
|	317000076	|	Sociedades corretoras	|	Brokers	|
|	317000077	|	Sociedades gestoras de fundos de investimento	|	Investment Fund Managing Companies	|
|	317000047	|	Fundos e sociedades de investimento mobiliário, excepto fundos do mercado monetário	|	Investment funds other than money market funds	|
|	317000049	|	Fundos e sociedades de obrigações	|	bond funds	|
|	317000080	|	Sociedades gestoras de fundos de titularização de créditos	|	Securitization Fund Managing Companies	|
|	317000081	|	Sociedades gestoras de fundos de pensões	|	Pension Funds Managing Companies	|
|	317000082	|	Sociedades gestoras de patrimónios	|	Wealth Managing Companies	|
|	317000083	|	Auxiliares Financeiros - Outros	|	Other Financial Auxiliaries	|
|	317000084	|	Sociedades administradoras de compras em grupo	|	Group-Purchase Managing Companies	|
|	317000085	|	Sociedades mediadoras do mercado monetário e do mercado de câmbios	|	Foreign-Exchange and Money-Market Mediating Companies	|
|	317000052	|	Fundos e sociedades de poupança em acções	|	Share account savings funds	|
|	317000087	|	Sociedades de seguros e fundos de pensões	|	Insurance corporations and pension funds	|
|	317000051	|	Fundos e sociedades de poupança reforma	|	Retirement savings funds	|
|	317000091	|	Sociedades de seguros	|	Insurance Corporations	|
|	317000092	|	Fundos de pensões	|	Pension Funds	|
|	317000093	|	Administrações públicas	|	General government	|
|	317000050	|	Fundos e sociedades de tesouraria	|	Treasury funds	|
|	317000097	|	Administração central	|	Central government	|
|	317000101	|	Estado	|	State	|
|	317000102	|	Fundos e serviços autónomos	|	Autonomous funds and services	|
|	317000054	|	Fundos e sociedades mistos	|	Mixed funds	|
|	317000229	|	Instituições sem fins lucrativos ao serviço das sociedades não financeiras privadas	|	Non-profit institutions serving private non-financial corporations	|
|	317000105	|	Administrações públicas, excepto administração central	|	General government, except central government	|
|	317000107	|	Administração regional	|	Regional government	|
|	317000108	|	Administração regional - Açores	|	Regional government - Azores	|
|	317000109	|	Administração regional - Madeira	|	Regional government - Madeira	|
|	317000111	|	Administração local	|	Local government	|
|	317000112	|	Administração local - Continente	|	Local government - Mainland	|
|	317000113	|	Administração local - Açores	|	Local government- Azores	|
|	317000114	|	Administração local - Madeira	|	Local government - Madeira	|
|	317000118	|	Fundos de segurança social	|	Social security funds	|
|	317000122	|	Sector não financeiro, excepto administrações públicas	|	Non-financial sector, except general government	|
|	317000125	|	Sociedades não financeiras	|	Non-financial corporations	|
|	317000231	|	Instituições sem fins lucrativos ao serviço das sociedades não financeiras sob controlo estrangeiro	|	Foreign-controlled non-profit institutions serving non-financial corporations	|
|	317000063	|	Intermediários financeiros - Outros	|	Other financial intermediaries	|
|	317000024	|	Outras instituições	|	Other institutions	|
|	317000034	|	Outras instituições	|	Other institutions	|
|	317000021	|	Outras instituições com relação de domínio	|	Other institutions - with a domain relation	|
|	317000030	|	Outras instituições com relação de domínio	|	Other institutions - with a domain relation	|
|	317000022	|	Outras instituições sem relação de domínio	|	Other institutions - without a domain relation	|
|	317000031	|	Outras instituições sem relação de domínio	|	Other institutions - without a domain relation	|
|	317000130	|	Particulares, excluindo emigrantes	|	Households, excluding emigrants	|
|	317000135	|	Famílias	|	Households	|
|	317000139	|	Famílias - Empregadores e trabalhadores por conta própria	|	Sole proprietors/ unincorporated partnerships	|
|	317000086	|	Outros auxiliares financeiros	|	Other financial auxiliaries	|
|	317000143	|	Instituições sem fins lucrativos ao serviço das famílias	|	Non-Profit Institutions serving households	|
|	317000147	|	Emigrantes	|	Emigrants	|
|	317000221	|	Outros sectores	|	Other Sectors	|
|	317000197	|	Sector Não Residente	|	Non-Resident Sector	|
|	317000068	|	Outros intermediários financeiros	|	Other financial intermediaries	|
|	317000227	|	Quase-sociedades não financeiras públicas (Outras entidades)	|	Public non-financial quasi-corporations (other entities)	|
|	317000211	|	Sede e sucursais da própria instituição	|	Other MFIs - Departments abroad	|
|	317000213	|	Outras instituições com relação de domínio	|	Other MFI's - With a domain relation, excluding departments abroad	|
|	317000214	|	Outras instituições sem relação de domínio	|	Other MFI's - Without a domain relation	|
|	317000004	|	Sector financeiro	|	Financial sector	|
|	317000008	|	Instituições financeiras monetárias	|	Monetary financial institutions	|
|	317000012	|	Bancos centrais	|	Central banks	|
|	317000016	|	Outras instituições financeiras monetárias	|	Other monetary financial institutions	|
|	317000250	|	Sector público residente	|	Resident public sector	|
|	317000215	|	Sector residente e não residente, excepto Bancos Centrais da União Monetária e outras IFM	|	Resident and non-resident sector, except central banks in the Monetary Union and other MFIs	|
|	317000023	|	Sede e sucursais da própria instituição	|	Headquarters and branches	|
|	317000033	|	Sede e sucursais da própria instituição	|	Headquarters and branches	|
|	317000104	|	Serviços autónomos	|	Autonomous services	|
|	317000065	|	Sociedades de fomento empresarial	|	Business development companies	|
|	317000245	|	Sociedades de titularização de créditos	|	Credit securitization companies	|
|	317000251	|	Sociedades e fundos de titularização de crédito não residentes	|	Non-resident credit securitization companies and funds	|
|	317000079	|	Sociedades gestoras de fundos de investimento imobiliário	|	Real estate investment funds management companies 	|
|	317000078	|	Sociedades gestoras de fundos de investimento mobiliário	|	Securities investment fund management companies	|
|	317000036	|	Instituições financeiras não monetárias	|	Non-monetary financial institutions	|
|	317000040	|	Outros intermediários financeiros e auxiliares financeiros	|	Non-monetary financial institutions, except insurance corporations and pension funds	|
|	317000044	|	Intermediários financeiros	|	Financial Intermediaries, except Insurance Corporations and Pension Funds	|
|	317000228	|	Sociedades não financeiras privadas	|	Pivate non-financial companies	|
|	317000225	|	Sociedades não financeiras públicas	|	Public non-financial companies	|
|	317000226	|	Sociedades não financeiras públicas participadas maioritariamente pelo sector público (Empresas públicas)	|	Public non-financial corporations mainly owned by the public sector (Public companies)	|
|	317000071	|	Auxiliares financeiros	|	Financial Auxiliaries	|
|	317000088	|	Sociedades de seguros e fundos de pensões	|	Insurance corporations and pension funds	|
|	317000094	|	Administrações públicas	|	General government	|
|	317000098	|	Administração central	|	Central government	|
|	317000106	|	Administrações públicas, excepto administração central	|	General government, except central government	|
|	317000110	|	Administração regional	|	Regional Government	|
|	317000115	|	Administração local	|	Local Government	|
|	317000119	|	Fundos de segurança social	|	Social Security Funds	|
|	317000123	|	Sector não financeiro, excepto administrações públicas	|	Non-financial sector, except general government	|
|	317000126	|	Sociedades não financeiras	|	Non-financial corporations	|
|	317000131	|	Particulares	|	Individuals	|
|	317000136	|	Famílias	|	Households	|
|	317000140	|	Famílias - Empregadores e trabalhadores por conta própria	|	Households - Sole proprietors/ unincorporated partnerships	|
|	317000142	|	Famílias - Outros	|	Households - others	|
|	317000144	|	Instituições sem fins lucrativos ao serviço das famílias	|	Non-Profit Institutions serving households	|
|	317000164	|	Não Sectorizado	|	Non-specified sector	|
|	317000230	|	Sociedades não financeiras sob controlo estrangeiro	|	Foreign-controlled non-finanical companies	|
|	317000019	|	Tipo 1	|	Type 1	|
|	317000124	|	Sector não financeiro (excepto administrações públicas) residente na União Monetária	|	Non-Financial sector, except General Government, residents at the Monetary Union	|
|	317000127	|	Empresas não financeiras, residentes na União Monetária	|	Non-financial Corporations, residents at the Monetary Union	|
|	317000132	|	Particulares, residentes na União Monetária	|	Households and non-profit institutions serving households, residents at the Monetary Union	|
|	317000026	|	Tipo 2	|	Type 2	|
|	317000223	|	Sector privado não monetário	|	Non monetary private sector	|
|	317000224	|	Sector não monetário	|	Non monetary sector	|
|	317000257	|	Todos os Sectores	|	All sectors	|
|	317000256	|	Outros Sectores Institucionais	|	Other institutional sectors	|
|	-99999997	|	[ Desconhecido ]	|	Unknown	|
|	-99999999	|	[ Não Aplicável ]	|	Not applicable	|

[Return](#table-of-contents)


## Institutional Sector SEC 2010

| Code |	Designação | Designation |
| :---: | :----- | :----- |
|	-99999998	|	Não Especificado	|	Non-specified	|
|	348500001	|	Total da Economia	|	Total Economy	|
|	348500002	|	Sociedades não financeiras	|	Non-financial corporations	|
|	348500003	|	Sociedades não financeiras públicas	|	Public non-financial corporations	|
|	348500006	|	Sociedades não financeiras da Administração Central - Empresas	|	Non-financial corporations of the general government - Companies	|
|	348500007	|	Sociedades não financeiras da Administração Central - Outras Entidades	|	Non-financial corporations of the general government - Other entities	|
|	348500010	|	Sociedades não financeiras da Administração Regional dos Açores - Empresas	|	Non-financial corporations of the regional government of Azores - Companies	|
|	348500011	|	Sociedades não financeiras da Administração Regional dos Açores - Outras Entidades	|	Non-financial corporations of the regional government of Azores - Other entities	|
|	348500008	|	Sociedades não financeiras da Administração Regional da Madeira - Empresas	|	Non-financial corporations of the regional government of Madeira - Companies	|
|	348500009	|	Sociedades não financeiras da Administração Regional da Madeira - Outras Entidades	|	Non-financial corporations of the regional government of Madeira - Other entities	|
|	348500012	|	Sociedades não financeiras da Administração Local do Continente - Empresas	|	Non-financial corporations of the local government of the Mainland - Companies	|
|	348500013	|	Sociedades não financeiras daAdministração Local do Continente - Outras Entidades	|	Non-financial corporations of the local government of the Mainland - Other entities	|
|	348500014	|	Sociedades não financeiras da Administração Local dos Açores - Empresas	|	Non-financial corporations of the local government of the Azores - Companies	|
|	348500015	|	Sociedades não financeiras da Administração Local dos Açores - Outras Entidades	|	Non-financial corporations of the local government of the Azores - Other entities	|
|	348500016	|	Sociedades não financeiras da Administração Local da Madeira - Empresas	|	Non-financial corporations of the local government of the Madeira - Companies	|
|	348500017	|	Sociedades não financeiras da Administração Local da Madeira - Outras Entidades	|	Non-financial corporations of the local government of the Madeira - Other entities	|
|	348500004	|	Sociedades não financeiras privadas	|	Private non-financial corporations	|
|	348500005	|	Sociedades não financeiras sob controlo estrangeiro	|	Foreign controlled non-financial corporations	|
|	348500018	|	Sociedades financeiras	|	Financial corporations	|
|	348500019	|	Banco central	|	Central bank	|
|	348500290	|	Instituições financeiras monetárias	|	Monetary financial institutions	|
|	348500020	|	Entidades depositárias exceto o banco central	|	Deposit-taking corporations except the Central bank	|
|	348500021	|	Entidades depositárias públicas exceto o banco central	|	Public deposit-taking corporations except the Central bank	|
|	348500022	|	Bancos públicos	|	Public banks	|
|	348500023	|	Caixas de crédito agrícola mútuo públicas	|	Public mutual agriculture credit banks	|
|	348500024	|	Caixas económicas públicas	|	Public savings banks	|
|	348500025	|	Instituições de moeda electrónica públicas	|	Public electronic money institutions	|
|	348500026	|	Entidades depositárias privadas	|	Private deposit-taking corporations	|
|	348500027	|	Bancos privados	|	Private banks	|
|	348500028	|	Caixas de crédito agrícola mútuo privadas	|	Private mutual agriculture credit banks	|
|	348500029	|	Caixas económicas privadas	|	Private savings banks	|
|	348500030	|	Instituições de moeda electrónica privadas	|	Private electronic money institutions	|
|	348500031	|	Entidades depositárias sob controlo estrangeiro	|	Foreign controlled deposit-taking corporations	|
|	348500032	|	Bancos sob controlo estrangeiro	|	Foreign controlled banks	|
|	348500033	|	Caixas de crédito agrícola mútuo sob controlo estrangeiro	|	Foreign controlled mutual agriculture credit banks	|
|	348500034	|	Caixas Económicas sob controlo estrangeiro	|	Foreign controlled savings banks	|
|	348500035	|	Instituições de moeda electrónica sob controlo estrangeiro	|	Foreign controlled electronic money institutions	|
|	348500291	|	Outras instituições financeiras monetárias	|	Other Monetary financial institutions	|
|	348500036	|	Fundos do mercado monetário (FMM)	|	Money market funds (MMF)	|
|	348500037	|	Fundos do mercado monetário (FMM) públicos	|	Public money market funds	|
|	348500038	|	Fundos do mercado monetário (FMM) privados	|	Private money market funds	|
|	348500039	|	Fundos do mercado monetário (FMM) sob controlo estrangeiro	|	Foreign controlled money market funds	|
|	348500040	|	Fundos de investimento exceto FMM	|	Investment funds except MMF	|
|	348500041	|	Fundos de investimento públicos exceto FMM	|	Public investment funds except MMF	|
|	348500042	|	Fundos de investimento mobiliários públicos	|	Public securities investment funds	|
|	348500043	|	Fundos de investimento imobiliários públicos	|	Public real estate investment funds	|
|	348500294	|	Fundos de investimento capital de risco públicos	|	Public venture capital investment funds	|
|	348500044	|	Fundos de investimento privados exceto FMM	|	Private investment funds except MMF	|
|	348500045	|	Fundos de investimento mobiliários privados	|	Private securities investment funds	|
|	348500046	|	Fundos de investimento imobiliários privados	|	Private real estate investment funds	|
|	348500295	|	Fundos de investimento de capital de risco privados	|	Private venture capital investment funds	|
|	348500047	|	Fundos de investimento sob controlo estrangeiro exceto FMM	|	Foreign controlled investment funds except MMF	|
|	348500048	|	Fundos de investimento mobiliários sob controlo estrangeiro	|	Foreign controlled securities investment funds	|
|	348500049	|	Fundos de investimento imobiliários sob controlo estrangeiro	|	Foreign controlled real estate investment funds	|
|	348500296	|	Fundos de investimento de capital de risco sob controlo estrangeiro	|	Foreign controlled venture capital investment funds	|
|	348500293	|	Instituições financeiras não monetárias exceto SSFP	|	Non-monetary financial institutions except insurance corporations and pension funds	|
|	348500292	|	Instituições financeiras não monetárias	|	Non-monetary financial institutions	|
|	348500050	|	Outros intermediários financeiros exceto sociedades de seguros e fundos de pensões	|	Other financial intermediaries except insurance corporations and pension funds	|
|	348500051	|	Outros intermediários financeiros públicos exceto sociedades de seguros e fundos de pensões	|	Other public financial intermediaries except insurance corporations and pension funds	|
|	348500052	|	Contrapartes centrais públicas	|	Public central counterparty clearing houses	|
|	348500053	|	Sociedades de capital de risco públicas	|	Public venture capital corporations	|
|	348500054	|	Sociedades de factoring públicas	|	Public factoring corporations	|
|	348500055	|	Sociedades de locação financeira públicas	|	Public financial leasing corporations	|
|	348500056	|	Sociedades financeiras de corretagem públicas	|	Public financial dealers	|
|	348500057	|	Sociedades financeiras para aquisições a Crédito públicas	|	Public credit-purchase financing corporations	|
|	348500058	|	Sociedades de desenvolvimento regional públicas	|	Public regional development corporations	|
|	348500059	|	Sociedades de fomento empresarial públicas	|	Public business development corporations	|
|	348500060	|	Sociedades de investimento públicas	|	Public investment corporations	|
|	348500061	|	Sociedades emitentes ou gestoras de cartões de crédito públicas	|	Public credit card issuing and managing corporations	|
|	348500062	|	Sociedades de titularização de créditos públicas	|	Public credit securitization corporations	|
|	348500063	|	Sociedades de garantia mútua públicas	|	Public mutual garantee corporations	|
|	348500064	|	Instituições financeiras de crédito públicas	|	Public financial credit institutions	|
|	348500065	|	Fundos de titularização de créditos públicos	|	Public credit securitization funds	|
|	348500067	|	Outros intermediários financeiros públicas	|	Other public financial intermediaries	|
|	348500068	|	Outros intermediários financeiros privados exceto sociedades de seguros e fundos de pensões	|	Other Private financial intermediaries except insurance corporations and pension funds	|
|	348500069	|	Contrapartes centrais privadas	|	Private central counterparty clearing houses	|
|	348500070	|	Sociedades de capital de risco privadas	|	Private venture capital corporations	|
|	348500071	|	Sociedades de factoring privadas	|	Private factoring corporations	|
|	348500072	|	Sociedades de locação financeira privadas	|	Private financial leasing corporations	|
|	348500073	|	Sociedades financeiras de corretagem privadas	|	Private financial dealers	|
|	348500074	|	Sociedades financeiras para aquisições a crédito privadas	|	Private credit-purchase financing corporations	|
|	348500075	|	Sociedades de desenvolvimento regional privadas	|	Private regional development corporations	|
|	348500076	|	Sociedades de fomento empresarial privadas	|	Private business development corporations	|
|	348500077	|	Sociedades de investimento privadas	|	Private investment corporations	|
|	348500078	|	Sociedades emitentes ou gestoras de cartões de crédito privadas	|	Private credit card issuing and managing corporations	|
|	348500079	|	Sociedades de titularização de créditos privadas	|	Private credit securitization corporations	|
|	348500080	|	Sociedades de garantia mútua privadas	|	Private mutual garantee corporations	|
|	348500081	|	Instituições financeiras de crédito privadas	|	Private financial credit institutions	|
|	348500082	|	Fundos de titularização de créditos privados	|	Private credit securitization funds	|
|	348500084	|	Outros intermediários financeiros privados	|	Other private financial intermediaries	|
|	348500085	|	Outros intermediários financeiros sob controlo estrangeiro exceto sociedades de seguros e fundos de pensões	|	Other Foreign controlled financial intermediaries except insurance corporations and pension funds	|
|	348500086	|	Contrapartes centrais sob controlo estrangeiro	|	Foreign controlled central counterparty clearing houses	|
|	348500087	|	Sociedades de capital de risco sob controlo estrangeiro	|	Foreign controlled venture capital corporations	|
|	348500088	|	Sociedades de factoring sob controlo estrangeiro	|	Foreign controlled factoring corporations	|
|	348500089	|	Sociedades de locação financeira sob controlo estrangeiro	|	Foreign controlled financial leasing corporations	|
|	348500090	|	Sociedades financeiras de corretagem sob controlo estrangeiro	|	Foreign controlled financial dealers	|
|	348500091	|	Sociedades financeiras para aquisições a crédito sob controlo estrangeiro	|	Foreign controlled credit-purchase financing corporations	|
|	348500092	|	Sociedades de desenvolvimento regional sob controlo estrangeiro	|	Foreign controlled regional development corporations	|
|	348500093	|	Sociedades de fomento empresarial sob controlo estrangeiro	|	Foreign controlled business development corporations	|
|	348500094	|	Sociedades de investimento sob controlo estrangeiro	|	Foreign controlled investment corporations	|
|	348500095	|	Sociedades emitentes ou gestoras de cartões de crédito sob controlo estrangeiro	|	Foreign controlled credit card issuing and managing corporations	|
|	348500096	|	Sociedades de titularização de créditos sob controlo estrangeiro	|	Foreign controlled credit securitization corporations	|
|	348500097	|	Sociedades de garantia mútua sob controlo estrangeiro	|	Foreign controlled mutual garantee corporations	|
|	348500098	|	Instituições financeiras de crédito sob controlo estrangeiro	|	Foreign controlled financial credit institutions	|
|	348500099	|	Fundos de titularização de créditos sob controlo estrangeiro	|	Foreign controlled credit securitization funds	|
|	348500101	|	Outros intermediários financeiros sob controlo estrangeiro	|	Other foreign controlled financial intermediaries	|
|	348500297	|	Outros Intermediários financeiros exceto SSFP, auxiliares financeiros e instituições financeiras cativas e prestamistas	|	Other financial intermediaries except ICPF, financial auxiliaries and captive financial institutions and money lenders	|
|	348500102	|	Auxiliares financeiros	|	Financial auxiliaries	|
|	348500103	|	Auxiliares financeiros públicos	|	Public financial auxiliaries	|
|	348500104	|	Auxiliares de seguros públicos	|	Public insurance auxiliaries	|
|	348500105	|	Agencias de câmbios públicas	|	Public exchange offices	|
|	348500106	|	Sociedades corretoras públicas	|	Public brokers	|
|	348500107	|	Sociedades gestoras de fundos de investimento públicas	|	Public Investment funds management corporations	|
|	348500108	|	Sociedades gestoras de fundos de titularização de créditos públicas	|	Public credit securitization funds management corporations	|
|	348500109	|	Sociedades gestoras de fundos de pensões públicas	|	Public pension funds management corporations	|
|	348500110	|	Sociedades gestoras de patrimónios públicas	|	Public wealth management corporations	|
|	348500111	|	Sociedades administradoras de compras em grupo públicas	|	Public group-purchase management corporations	|
|	348500112	|	Sociedades mediadoras do mercado monetário e do mercado de câmbios públicas	|	Public foreign exchange and money market mediating corporations	|
|	348500298	|	Sedes sociais de sociedades financeiras públicas	|	Public financial head offices	|
|	348500066	|	Instituições de pagamentos públicas	|	Public payment institutions	|
|	348500113	|	Outros auxiliares financeiros  públicos	|	Other public  financial auxiliaries	|
|	348500114	|	Auxiliares financeiros privados	|	Private financial auxiliaries	|
|	348500115	|	Auxiliares de seguros privadas	|	Private insurance auxiliaries	|
|	348500116	|	Agências de câmbios privadas	|	Private exchange offices	|
|	348500117	|	Sociedades corretoras privadas	|	Private brokers	|
|	348500118	|	Sociedades gestoras de fundos de investimento privadas	|	Private Investment funds management corporations	|
|	348500119	|	Sociedades gestoras de fundos de titularização de créditos privadas	|	Private credit securitization funds management corporations	|
|	348500120	|	Sociedades gestoras de fundos de pensões privadas	|	Private pension funds management corporations	|
|	348500121	|	Sociedades gestoras de patrimónios privadas	|	Private wealth management corporations	|
|	348500122	|	Sociedades administradoras de compras em grupo privadas	|	Private group-purchase management corporations	|
|	348500123	|	Sociedades mediadoras do mercado monetário e do mercado de câmbios privadas	|	Private foreign exchange and money market mediating corporations	|
|	348500299	|	Sedes sociais de sociedades financeiras privadas	|	Private financial head offices	|
|	348500083	|	Instituições de pagamentos privadas	|	Private payment institutions	|
|	348500124	|	Outros auxiliares financeiros  privadas	|	Other private  financial auxiliaries	|
|	348500125	|	Auxiliares financeiros sob controlo estrangeiro	|	Foreign controlled financial auxiliaries	|
|	348500126	|	Auxiliares de seguros sob controlo estrangeiro	|	Foreign controlled insurance auxiliaries	|
|	348500127	|	Agencias de câmbios sob controlo estrangeiro	|	Foreign controlled exchange offices	|
|	348500128	|	Sociedades corretoras sob controlo estrangeiro	|	Foreign controlled brokers	|
|	348500129	|	Sociedades gestoras de fundos de investimento sob controlo estrangeiro	|	Foreign controlled Investment funds management corporations	|
|	348500130	|	Sociedades gestoras de fundos de titularização de créditos sob controlo estrangeiro	|	Foreign controlled credit securitization funds management corporations	|
|	348500131	|	Sociedades gestoras de fundos de pensões sob controlo estrangeiro	|	Foreign controlled pension funds management corporations	|
|	348500132	|	Sociedades gestoras de patrimónios sob controlo estrangeiro	|	Foreign controlled wealth management corporations	|
|	348500133	|	Sociedades administradoras de compras em grupo sob controlo estrangeiro	|	Foreign controlled group-purchase management corporations	|
|	348500134	|	Sociedades mediadoras do mercado monetário e do mercado de câmbios sob controlo estrangeiro	|	Foreign controlled foreign exchange and money market mediating corporations	|
|	348500300	|	Sedes sociais de sociedades financeiras sob controlo estrangeiro	|	Foreign controlled financial head offices	|
|	348500100	|	Instituições de pagamentos sob controlo estrangeiro	|	Foreign controlled payment institutions	|
|	348500135	|	Outros auxiliares financeiros  sob controlo estrangeiro	|	Other foreign controlled  financial auxiliaries	|
|	348500136	|	Instituições financeiras cativas e prestamistas	|	Captive financial institutions and money lenders	|
|	348500137	|	Instituições financeiras cativas e prestamistas públicas	|	Public captive financial institutions and money lenders	|
|	348500301	|	Holdings financeiras públicas	|	Public financial holding corporations	|
|	348500302	|	Holdings não financeiras públicas	|	Public non-financial holding corporations	|
|	348500303	|	Prestamistas públicos	|	Public money lenders	|
|	348500304	|	Trusts e outras atividades similares públicos	|	Public trusts and other similar activities	|
|	348500305	|	Sociedades de finalidade especial que obtêm financiamento para empresas-mãe, públicas	|	Public special purpose entities obtaining financing for parent company	|
|	348500306	|	Outras Intituições financeiras cativas e prestamistas públicas	|	Other public captive financial institutions and money lenders	|
|	348500138	|	Instituições financeiras cativas e prestamistas privadas	|	Private captive financial institutions and money lenders	|
|	348500307	|	Holdings financeiras privadas	|	Private financial holding corporations	|
|	348500308	|	Holdings não financeiras privadas	|	Private non-financial holding corporations	|
|	348500309	|	Prestamistas privados	|	Private money lenders	|
|	348500310	|	Trusts e outras atividades similares privadas	|	Private trusts and other similar activities	|
|	348500311	|	Sociedades de finalidade especial  que obtêm financiamento para empresa-mãe, privadas	|	Private special purpose entities obtaining financing for parent company	|
|	348500312	|	Outras Intituições financeiras cativas e prestamistas privadas	|	Other public captive financial institutions and money lenders	|
|	348500139	|	Instituições financeiras cativas e prestamistas sob controlo estrangeiro	|	Foreign controlled captive financial institutions and money lenders	|
|	348500313	|	Holdings financeiras sob controlo estrangeiro	|	Foreign controlled financial holding corporations	|
|	348500314	|	Holdings não financeiras sob controlo estrangeiro	|	Foreign controlled non-financial holding corporations	|
|	348500315	|	Prestamistas sob controlo estrangeiro	|	Foreign controlled money lenders	|
|	348500316	|	Trusts e outras atividades similares sob controlo estrangeiro	|	Foreign controlled trusts and other similar activities	|
|	348500317	|	Sociedades de finalidade especial que obtêm financiamento para empresa-mãe, sob controlo estrangeiro	|	Foreign controlled special purpose entities obtaining financing for parent company	|
|	348500318	|	Outras Intituições financeiras cativas e prestamistas sob controlo estrangeiro	|	Other public captive financial institutions and money lenders	|
|	348500140	|	Sociedades de seguros	|	Insurance corporations	|
|	348500141	|	Sociedades de seguros públicas	|	Public insurance corporations	|
|	348500320	|	Companhias de seguros públicas	|	Public insurance companies	|
|	348500321	|	Associações de socorros mútuos públicas	|	Public mutual aid associations	|
|	348500142	|	Sociedades de seguros privadas	|	Private insurance corporations	|
|	348500322	|	Companhias de seguros privadas	|	Private insurance companies	|
|	348500323	|	Associações de socorros mútuos privadas	|	Private mutual aid associations	|
|	348500143	|	Sociedades de seguros sob controlo estrangeiro	|	Foreign controlled insurance corporations	|
|	348500324	|	Companhias de seguros sob controlo estrangeiro	|	Foreign controlled insurance companies	|
|	348500325	|	Associações de socorros mútuos sob controlo estrangeiro	|	Foreign controlled mutual aid associations	|
|	348500319	|	Sociedades de seguros e fundos de pensões (SSFP)	|	Insurance corporations and pension funds (ICPF)	|
|	348500144	|	Fundos de Pensões	|	Pension funds	|
|	348500145	|	Fundos de Pensões públicos	|	Public pension funds	|
|	348500146	|	Fundos de Pensões privados	|	Private pension funds	|
|	348500147	|	Fundos de Pensões sob controlo estrangeiro	|	Foreign controlled pension funds	|
|	348500148	|	Administrações públicas	|	General government	|
|	348500149	|	Administração Central (exceto fundos de segurança social)	|	Central government (excluding social security funds)	|
|	348500151	|	Estado	|	State	|
|	348500152	|	Serviços e fundos autónomos da administração central	|	Autonomous services and funds of the central government	|
|	348500150	|	Empresas públicas da administração central	|	Public corporations of the central government	|
|	348500153	|	Instituições sem fim lucrativo da administração central	|	Non-profit institutions of the central government	|
|	348500154	|	Administração regional	|	Regional government	|
|	348500163	|	Administração regional dos Açores	|	Regional government of Azores	|
|	348500167	|	Orgãos do governo regional dos Açores	|	Bodies of the regional government of Azores	|
|	348500165	|	Serviços e fundos autónomos da administração regional dos Açores	|	Autonomous services and funds of the regional  government of Azores	|
|	348500164	|	Empresas públicas da administração regional dos Açores	|	Public corporations of the regional government of Azores	|
|	348500166	|	Instituições sem fim lucrativo da administração regional dos Açores	|	Non-profit institutions of the regional government of Azores	|
|	348500168	|	Administração regional da Madeira	|	Regional government of Madeira	|
|	348500172	|	Orgãos do governo regional da Madeira	|	Bodies of the regional government of Madeira	|
|	348500170	|	Serviços e fundos autónomoss da administração regional da Madeira	|	Autonomous services and funds of the regional  government of Madeira	|
|	348500169	|	Empresas públicas da administração regional da Madeira	|	Public corporations of the regional government of Madeira	|
|	348500171	|	Instituições sem fim lucrativo da administração regional da Madeira	|	Non-profit institutions of the regional government of Madeira	|
|	348500326	|	Administração regional e local	|	Regional and local government	|
|	348500155	|	Administracão local	|	Local government	|
|	348500331	|	Administração local do continente	|	Local government of the mainland	|
|	348500335	|	Distritos do Continente	|	Districts of the mainland	|
|	348500336	|	Municípios do Continente	|	Municipalities of the mainland	|
|	348500337	|	Freguesias do Continente	|	Parishes of the mainland	|
|	348500338	|	Serviços autónomos da Administração local do Continente	|	Autonomous services of the local  government of the mainland	|
|	348500173	|	Empresas públicas da Administração local do Continente	|	Public corporations of the local government of the mainland	|
|	348500174	|	Instituições sem fim lucrativo da Administração local do Continente	|	Non-profit institutions of the local government of the mainland	|
|	348500332	|	Administração local dos Açores	|	Local government of Azores	|
|	348500339	|	Distritos dos Açores	|	Districts of Azores	|
|	348500340	|	Municípios dos Açores	|	Municipalities of Azores	|
|	348500341	|	Freguesias dos Açores	|	Parishes of Azores	|
|	348500342	|	Serviços autónomos da administração Local dos Açores	|	Autonomous services of the local  government of Azores	|
|	348500175	|	Empresas públicas da administração local dos Açores	|	Public corporations of the local government of Azores	|
|	348500176	|	Instituições sem fim lucrativo da administração Local dos Açores	|	Non-profit institutions of the local government of Azores	|
|	348500333	|	Administração local da Madeira	|	Local government of Madeira	|
|	348500343	|	Distritos da Madeira	|	Districts of Madeira	|
|	348500344	|	Municípios da Madeira	|	Municipalities of Madeira	|
|	348500345	|	Freguesias da Madeira	|	Parishes of Madeira	|
|	348500346	|	Serviços autónomos da administração local da Madeira	|	Autonomous services of the local  government of Madeira	|
|	348500177	|	Empresas públicas da administração local da Madeira	|	Public corporations of the local government of Madeira	|
|	348500178	|	Instituições sem fim lucrativo da administração local da Madeira	|	Non-profit institutions of the local government of Madeira	|
|	348500162	|	Fundos da Segurança Social	|	Social security funds	|
|	348500179	|	Famílias	|	Households	|
|	348500180	|	Empregadores	|	Employers	|
|	348500181	|	Trabalhadores por conta própria	|	Own-account workers	|
|	348500182	|	Empregados	|	Employees	|
|	348500183	|	Famílias com recursos provenientes de rendimentos de propriedade e transferências	|	Households receiving property and transfer income	|
|	348500184	|	Famílias com recursos provenientes de rendimentos de propriedade	|	Households receiving property income	|
|	348500185	|	Famílias com recursos provenientes de pensões	|	Households receiving pensions	|
|	348500186	|	Famílias com recursos provenientes de outras transferencias	|	Households receiving other transfers	|
|	348500327	|	Particulares	|	Households and NPISH	|
|	348500187	|	Instituições sem fim lucrativo ao servico das famílias	|	Non-profit institutions serving households (NPISH)	|
|	348500188	|	Instituições sem fim lucrativo ao servico das famílias, privadas	|	Private non-profit institutions serving households	|
|	348500189	|	Instituições sem fim lucrativo ao servico das famílias, sob controlo estrangeiro	|	Foreign controlled non-profit institutions serving households	|
|	348500190	|	Resto do Mundo (Outros países que não Portugal)	|	Rest of the world	|
|	348500277	|	Sociedades não financeiras não residentes	|	Non-resident non-financial corporations	|
|	348500193	|	Sociedades não financeiras residentes em países da União Europeia que não União Monetária	|	Non-financial corporations resident in countries of the European Union outside the Monetary Union	|
|	348500192	|	Sociedades não financeiras residentes em países da União Monetária	|	Non-financial corporations resident in countries of the Monetary Union	|
|	348500191	|	Sociedades não financeiras residentes em países fora da União Europeia	|	Non-financial corporations resident outside the European Union	|
|	348500278	|	Sociedades financeiras não residentes	|	Non-resident financial corporations	|
|	348500328	|	Bancos centrais não residentes	|	Non-resident Central Banks	|
|	348500198	|	Bancos centrais de países da União Europeia que não União Monetária	|	Central banks of countries of the European Union outside the Monetary Union	|
|	348500197	|	Bancos centrais de países da União Monetária	|	Central banks of countries in the Monetary Union	|
|	348500199	|	Bancos centrais de países fora da União Europeia	|	Central banks of countries not belonging the European Union	|
|	348500349	|	Administração local de países da União monetária	|	Local administration of monetary union countries	|
|	348500279	|	Entidades depositárias, exceto o banco central, não residentes	|	Non-resident deposit-taking corporations except the Central bank	|
|	348500201	|	Entidades depositárias, exceto o banco central, residentes em países da União Europeia que não União Monetária	|	Deposit-taking corporations, except the Central bank, resident in countries of the European Union outside the Monetary Union	|
|	348500200	|	Entidades depositárias, exceto o banco central, residentes em países da União Monetária	|	Deposit-taking corporations, except the Central bank, resident in countries of the Monetary Union	|
|	348500202	|	Entidades depositárias, exceto o banco central, residentes em países fora da União Europeia	|	Deposit-taking corporations, except the Central bank, resident outside the European Union	|
|	348500280	|	Fundos do mercado monetário (FMM) não residentes	|	Non-resident money market funds	|
|	348500204	|	Fundos do mercado monetário (FMM) residentes em países da União Europeia que não União Monetária	|	Money market funds resident in countries of the European Union outside the Monetary Union	|
|	348500203	|	Fundos do mercado monetário (FMM) residentes em países da União Monetária	|	Money market funds resident in countries of the Monetary Union	|
|	348500205	|	Fundos do mercado monetário (FMM) residentes em países fora da União Europeia	|	Money market funds resident outside the European Union	|
|	348500281	|	Fundos de investimento, exceto FMM, não residentes	|	Non-resident investment funds	|
|	348500207	|	Fundos de investimento, exceto FMM, residentes em países da União Europeia que não União Monetária	|	Investment funds resident in countries of the European Union outside the Monetary Union	|
|	348500206	|	Fundos de investimento, exceto FMM, residentes em países da União Monetária	|	Investment funds resident in countries of the Monetary Union	|
|	348500208	|	Fundos de investimento, exceto FMM, residentes em países fora da União Europeia	|	Investment funds resident outside the European Union	|
|	348500282	|	Outros intermediários financeiros, exceto SSFP, não residentes	|	Other non-resident financial intermediaries except ICPF	|
|	348500210	|	Outros intermediários financeiros, exceto SSFP, residentes em países da União Europeia que não União Monetária	|	Other financial intermediaries, except ICPF, resident in countries of the European Union outside the Monetary Union	|
|	348500209	|	Outros intermediários financeiros, exceto SSFP, residentes em países da União Monetária	|	Other financial intermediaries, except ICPF, resident in countries of the Monetary Union	|
|	348500211	|	Outros intermediários financeiros, exceto SSFP, residentes em países fora da União Europeia	|	Other financial intermediaries, except ICPF, resident outside the European Union	|
|	348500283	|	Auxiliares financeiros não residentes	|	Non-resident financial auxiliaries	|
|	348500213	|	Auxiliares financeiros residentes em países da União Europeia que não União Monetária	|	Financial auxiliaries resident in countries of the European Union outside the Monetary Union	|
|	348500212	|	Auxiliares financeiros  residentes em países da União Monetária	|	Financial auxiliaries resident in countries of the Monetary Union	|
|	348500214	|	Auxiliares financeiros residentes em países fora da União Europeia	|	Financial auxiliaries resident outside the European Union	|
|	348500329	|	Instituições financeiras cativas e prestamistas não residentes	|	Non-resident captive financial institutions and money lenders	|
|	348500243	|	Instituições financeiras cativas e prestamistas residentes em países da União Europeia que não União Monetária	|	Captive financial institutions and money lenders resident in countries of the European Union outside the Monetary Union	|
|	348500242	|	Instituições financeiras cativas e prestamistas residentes em países da União Monetária	|	Captive financial institutions and money lenders resident in countries of the Monetary Union	|
|	348500244	|	Instituições financeiras cativas e prestamistas residentes em países fora da União Europeia	|	Captive financial institutions and money lenders resident outside the European Union	|
|	348500284	|	Sociedades de seguros não residentes	|	Non-resident insurance corporations	|
|	348500216	|	Sociedades de seguros residentes em países da União Europeia que não União Monetária	|	Insurance corporations resident in countries of the European Union outside the Monetary Union	|
|	348500215	|	Sociedades de seguros residentes em países da União Monetária	|	Insurance corporations resident in countries of the Monetary Union	|
|	348500217	|	Sociedades de seguros residentes em países fora da União Europeia	|	Insurance corporations resident outside the European Union	|
|	348500285	|	Fundos de Pensões não residentes	|	Non-resident pension funds	|
|	348500219	|	Fundos de Pensões residentes em países da União Europeia que não União Monetária	|	Pension funds resident in countries of the European Union outside the Monetary Union	|
|	348500218	|	Fundos de Pensões residentes em países da União Monetária	|	Pension funds resident in countries of the Monetary Union	|
|	348500220	|	Fundos de Pensões residentes em países fora da União Europeia	|	Pension funds resident outside the European Union	|
|	348500286	|	Administrações públicas não residentes	|	Non-resident general government	|
|	348500222	|	Administrações públicas de países da União Europeia que não União Monetária	|	General government of European Union countries outside the Monetary Union	|
|	348500221	|	Administrações públicas de países da União Monetária	|	General government of Monetary Union countries	|
|	348500223	|	Administrações públicas de países de fora da União Europeia	|	General government of countries outside the European Union	|
|	348500347	|	Administração central de países da União monetária	|	Central administration of monetary union countries	|
|	348500348	|	Administração regional de países da União monetária	|	Regional administration of monetary union countries	|
|	348500350	|	Fundos da segurança social de países da União monetária	|	Social security funds of monetary union countries	|
|	348500287	|	Famílias não residentes	|	Non-resident households	|
|	348500225	|	Famílias residentes em países da União Europeia que não União Monetária	|	Households resident in EU countries outside the Monetary Union	|
|	348500224	|	Famílias residentes em países da União Monetária	|	Households resident in countries of the Monetary Union	|
|	348500226	|	Famílias residentes em países fora da União Europeia	|	Households resident in countries outside the European Union	|
|	348500228	|	Emigrantes residentes em países da UE que não União Monetária	|	Emigrants resident in EU countries outside the Monetary Union	|
|	348500227	|	Emigrantes residentes em países da União Monetária	|	Emigrants resident in countries of the Monetary Union	|
|	348500229	|	Emigrantes residentes em países fora da União Europeia	|	Emigrants resident outside the European Union	|
|	348500330	|	Outras famílias residentes em países da UE que não União Monetária	|	Other households resident in EU countries outside the Monetary Union	|
|	348500288	|	Outras famílias residentes em países da União Monetária	|	Other households resident in countries of the Monetary Union	|
|	348500158	|	Outras famílias residentes em países fora da União Europeia	|	Other households resident in countries outside the European Union	|
|	348500289	|	Instituições sem fim lucrativo ao serviço das famílias, não residentes	|	Non-resident non-profit institutions serving households (NPISH)	|
|	348500231	|	Instituições sem fim lucrativo ao serviço das famílias, residentes em países da União Europeia que não União Monetária	|	NPISH resident in countries of the European Union outside the Monetary Union	|
|	348500230	|	Instituições sem fim lucrativo ao serviço das famílias, residentes em países da União Monetária	|	NPISH resident in countries of the Monetary Union	|
|	348500232	|	Instituições sem fim lucrativo ao serviço das famílias, residentes em países fora da União Europeia	|	NPISH resident outside the European Union	|
|	348500235	|	Organizações internacionais europeias	|	European international organizations	|
|	348500236	|	Organizações internacionais não europeias	|	Non-european international organizations	|
|	348500233	|	Organizações internacionais não financeiras europeias	|	European non-financial  international organizations	|
|	348500234	|	Organizações internacionais não financeiras não europeias	|	Non-european non-financial international organizations	|
|	348500237	|	Organizações internacionais financeiras europeias	|	European financial international organizations	|
|	348500238	|	Organizações internacionais financeiras não Europeias	|	Non-european financial international organizations	|
|	348500239	|	Banco Central Europeu	|	European Central Bank	|
|	348500240	|	Outras organizações financeiras europeias	|	Other european international financial organizations	|


[Return](#table-of-contents)

## Responsibility Level

**Version October, 1995**

+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                     | Designation                                                                                    |
+:===============================================+:===============================================================================================+:===============================================================================================+
| 1                                              | Crédito individual                                                                             | Individual credit                                                                              |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 11                                             | Crédito individual - poupança-emigrante – aquisição de prédios                                 | Individual credit - savings-emigrant - acquisition of buildings                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 12                                             | Crédito individual - poupança-emigrante - outras actividades                                   | Individual credit - savings-emigrant - other activities                                        |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 13                                             | Crédito individual - poupança-emigrante - prédios+outras actividades                           | Individual credit - savings-emigrant - buildings + other activ.                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 14                                             | Crédito individual - poupança-crédito– aquisição de prédios                                    | Individual credit - savings-credit - acquisition of buildings                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 15                                             | Crédito individual - poupança-crédito - outras actividades                                     | Individual credit - savings-credit - other activities                                          |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 16                                             | Crédito individual - poupança-crédito - prédios+outras actividades                             | Individual credit - savings-credit - buildings + other activ.                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 2                                              | Conta conjunta (crédito a mais do que um beneficiário) - primeiro mutuário                     | Joint credit (credit more than one beneficiary) - 1ºdebtor                                     |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 21                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - aquisição de prédios                      | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                               |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 22                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - outras actividades                        | Joint credit 1ºdebtor. - saving-emigrant - other activities                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 23                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - Prédios e outras actividades              | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activ.                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 24                                             | Crédito conjunto, 1º mutuário - poupança-crédito - aquisição de prédios                        | Joint credit 1ºdebtor. - saving-credit - acquisition buildings                                 |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 25                                             | Crédito conjunto, 1º mutuário - poupança-crédito - outras actividades                          | Joint credit 1ºdebtor. - saving-credit - other activities                                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 26                                             | Crédito conjunto, 1º mutuário - poupança-crédito - Prédios e outras actividades                | Joint credit 1ºdebtor. - saving-credit - buildings + other activ.                              |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 3                                              | Conta conjunta (crédito a mais do que um beneficiário) - restantes mutuários                   | Joint credit (credit more than one beneficiary) - remaining debtors                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 31                                             | Conta conj. Rest.mut. - poupança-emigrante - aquisição prédios                                 | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 32                                             | Conta conj. Rest.mut. - poupança-emigrante - outras actividades                                | Joint credit - remaining debtors - saving-emigrant - other activities                          |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 33                                             | Conta conj. Rest.mut. - poupança-emigrante - prédios + outras activ.                           | Joint credit - remaining debtors - savings-emigrant - buildings+ other activ.                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 34                                             | Conta conj. Rest.mut. - poupança-crédito - aquisição prédios                                   | Joint credit- remaining debtors - saving-credit - acquisition buildings                        |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 35                                             | Conta conj. Rest.mut. - poupança-crédito - outras actividades                                  | Joint credit - remaining debtors - saving-credit - other activities                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 36                                             | Conta conj. Rest.mut. - poupança-crédito - prédios + outras activ.                             | Joint credit - remaining debtors - savings-credit - buildings+ other activ.                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+


**Version October, 1996**

+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                     | Designation                                                                                    |
+:===============================================+:===============================================================================================+:===============================================================================================+
| 1                                              | Crédito individual                                                                             | Individual credit                                                                              |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 11                                             | Crédito individual - poupança-emigrante – aquisição de prédios                                 | Individual credit - savings-emigrant - acquisition of buildings                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 12                                             | Crédito individual - poupança-emigrante - outras actividades                                   | Individual credit - savings-emigrant - other activities                                        |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 13                                             | Crédito individual - poupança-emigrante - prédios+outras actividades                           | Individual credit - savings-emigrant - buildings + other activ.                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 2                                              | Conta conjunta (crédito a mais do que um beneficiário) - primeiro mutuário                     | Joint credit (credit more than one beneficiary) - 1ºdebtor                                     |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 21                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - aquisição de prédios                      | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                               |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 22                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - outras actividades                        | Joint credit 1ºdebtor. - saving-emigrant - other activities                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 23                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - Prédios e outras actividades              | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activ.                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 3                                              | Conta conjunta (crédito a mais do que um beneficiário) - restantes mutuários                   | Joint credit (credit more than one beneficiary) - remaining debtors                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 31                                             | Conta conj. Rest.mut. - poupança-emigrante - aquisição prédios                                 | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 32                                             | Conta conj. Rest.mut. - poupança-emigrante - outras actividades                                | Joint credit - remaining debtors - saving-emigrant - other activities                          |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 33                                             | Conta conj. Rest.mut. - poupança-emigrante - prédios + outras activ.                           | Joint credit - remaining debtors - savings-emigrant - buildings+ other activ.                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+


**Version November, 2001**

+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                     | Designation                                                                                    |
+:===============================================+:===============================================================================================+:===============================================================================================+
| 1                                              | Crédito individual                                                                             | Individual credit                                                                              |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 11                                             | Crédito individual - poupança-emigrante – aquisição de prédios                                 | Individual credit - savings-emigrant - acquisition of buildings                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 12                                             | Crédito individual - poupança-emigrante - outras actividades                                   | Individual credit - savings-emigrant - other activities                                        |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 13                                             | Crédito individual - poupança-emigrante - prédios+outras actividades                           | Individual credit - savings-emigrant - buildings + other activ.                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 14                                             | Crédito individual – crédito cedido em operações de titularização                              | Individual credit - credit due to operations of securitization                                 |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 2                                              | Conta conjunta (crédito a mais do que um beneficiário) - primeiro mutuário                     | Joint credit (credit more than one beneficiary) - 1ºdebtor                                     |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 21                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - aquisição de prédios                      | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                               |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 22                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - outras actividades                        | Joint credit 1ºdebtor. - saving-emigrant - other activities                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 23                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - Prédios e outras actividades              | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activ.                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 24                                             | Crédito conjunto, 1º mutuário - crédito cedido em operações de titularização                   | Joint credit 1ºdebtor. - credit due to operations of securitization                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 3                                              | Conta conjunta (crédito a mais do que um beneficiário) - restantes mutuários                   | Joint credit (credit more than one beneficiary) - remaining debtors                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 31                                             | Conta conj. Rest.mut. - poupança-emigrante - aquisição prédios                                 | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 32                                             | Conta conj. Rest.mut. - poupança-emigrante - outras actividades                                | Joint credit - remaining debtors - saving-emigrant - other activities                          |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 33                                             | Conta conj. Rest.mut. - poupança-emigrante - prédios + outras activ.                           | Joint credit - remaining debtors - savings-emigrant - buildings+ other activ.                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
| 34                                             | Conta conj. Rest.mut. - crédito cedido em operações de titularização                           | Joint credit - remaining debtors - credit due to operations of securitization                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+


**Version October, 2006**

+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                             | Designation                                                                                          |
+:===============================================+:=======================================================================================================+:=====================================================================================================+
| 1                                              | Crédito individual                                                                                     | Individual credit                                                                                    |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 11                                             | Crédito individual - poupança-emigrante – aquisição de prédios                                         | Individual credit - savings-emigrant - acquisition of buildings                                      |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 12                                             | Crédito individual - poupança-emigrante - outras actividades                                           | Individual credit - savings-emigrant - other activities                                              |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 13                                             | Crédito individual - poupança-emigrante - prédios+outras actividades                                   | Individual credit - savings-emigrant - buildings + other activ.                                      |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 14                                             | Crédito individual -  crédito cedido em operações de titularização                                     | Individual credit - credit due to operations of securitization                                       |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 15                                             | Crédito individual - afecto a obrigações hipotecárias ou obrigações sobre o sector público             | Individual credit -  mortgage-backed obligations or obligations in the public sector                 |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 2                                              | Conta conjunta (crédito a mais do que um beneficiário) - primeiro mutuário                             | Joint credit (credit more than one beneficiary) - 1ºdebtor                                           |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 21                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - aquisição de prédios                              | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 22                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - outras actividades                                | Joint credit 1ºdebtor. - saving-emigrant - other activities                                          |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 23                                             | Crédito conjunto, 1º mutuário - poupança-emigrante - Prédios e outras actividades                      | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activ.                                  |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 24                                             | Crédito conjunto, 1º mutuário - crédito cedido em operações de titularização                           | Joint credit 1ºdebtor. - credit due to operations of securitization                                  |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 25                                             | Crédito conjunto, 1º mutuário -  afecto a obrigações hipotecárias ou obrigações sobre o sector público | Joint credit 1ºdebtor. -  mortgage-backed obligations or obligations in the public sector            |
+------------------------------------------------+-----------------------------------------------------------------------------------------------+--------+------------------------------------------------------------------------------------------------------+
| 3                                              | Conta conjunta (crédito a mais do que um beneficiário) - restantes mutuários                           | Joint credit (credit more than one beneficiary) - remaining debtors                                  |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 31                                             | Conta conj. Rest.mut. - poupança-emigrante - aquisição prédios                                         | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                            |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 32                                             | Conta conj. Rest.mut. - poupança-emigrante - outras actividades                                        | Joint credit - remaining debtors - saving-emigrant - other activities                                |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 33                                             | Conta conj. Rest.mut. - poupança-emigrante - prédios + outras activ.                                   | Joint credit - remaining debtors - savings-emigrant - buildings+ other activ.                        |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 34                                             | Conta conj. Rest.mut. - crédito cedido em operações de titularização                                   | Joint credit - remaining debtors - credit due to operations of securitization                        |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 35                                             | Conta conj. Rest.mut. -  afecto a obrigações hipotecárias ou obrigações sobre o sector público         | Joint credit - remaining debtors –  mortgage-backed obligations or obligations in the public sector  |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 4                                              | Crédito conjunto comunicado por centrais estrangeiras                                                  | Joint credit – communicated via foreign channels                                                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+


**Version January, 2009**

+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                             | Designation                                                                                          |
+:===============================================+:=======================================================================================================+:=====================================================================================================+
| 1                                              | Crédito individual                                                                                     | Individual credit                                                                                    |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 2                                              | Crédito conjunto – 1.º mutuário                                                                        | Joint credit – 1.º debtor                                                                            |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 3                                              | Crédito conjunto – outros mutuários                                                                    | Joint credit – remaining debtors                                                                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 4                                              | Avalista ou fiador – individual                                                                        | Individual guarantor                                                                                 |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+
| 5                                              | Avalista ou fiador – conjunto                                                                          | Joint guarantor                                                                                      |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------+

[Return](#table-of-contents)



## Type of Credit

+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                                                                           | Designation                                                                                                                                       |
+:===============================================+:=====================================================================================================================================================+:==================================================================================================================================================+
| 1                                              | Responsabiidades comerciais                                                                                                                          | Commercial                                                                                                                                        |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 2                                              | Responsabilidades de financiamento por desconto                                                                                                      | Discount funding                                                                                                                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 3                                              | Outras responsabilidades de financiamento a curto prazo                                                                                              | Other short term funding                                                                                                                          |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 4                                              | Responsabilidades de financiamento a médio e longo prazos                                                                                            | Medium and Long term funding                                                                                                                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 5                                              | Outras responsabilidades                                                                                                                             | Other responsibilities                                                                                                                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 6                                              | Responsabilidades extrapatrimoniais, excepto garantias classificadas nos tipos 11 e 12                                                               | Off balance sheet liabilities (potential indebtedness)                                                                                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 7                                              | Responsabilidades de crédito em mora                                                                                                                 | Overdue Credit (non-performing loans)                                                                                                             |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 8                                              | Responsabilidades de crédito em contencioso                                                                                                          | Credit in litigation                                                                                                                              |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 9                                              | Créditos abatidos ao activo                                                                                                                          | Written-off credit                                                                                                                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 10                                             | Créditos renegociados                                                                                                                                | Renegotiated credit                                                                                                                               |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 11                                             | Garantias prestadas por entidades participantes para assegurar o cumprimento de operações de crédito concedido por outras entidades participantes    | Guarantees provided by participating entities to ensure the compliance of credit operations that are granted by other participating entities      |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 12                                             | Fianças e avales                                                                                                                                     | Guarantees or sureties                                                                                                                            |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 13                                             | Responsabilidades de crédito efectivas comunicadas por centrais estrangeiras                                                                         | Effective credit communicated by foreign banks                                                                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 14                                             | Responsabilidades de crédito potencial comunicadas por centrais estrangeiras                                                                         | Potential credit communicated by foreign banks                                                                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+

[Return](#table-of-contents)


## Credit Situation

+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                                                                           | Designation                                                                                                                                       |
+:===============================================+:=====================================================================================================================================================+:==================================================================================================================================================+
| 1                                              | Crédito efectivo em situação regular                                                                                                                 | Regular credit                                                                                                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 2                                              | Crédito potencial                                                                                                                                    | Potential credit                                                                                                                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 3                                              | Crédito vencido                                                                                                                                      | Overdue credit                                                                                                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 4                                              | Crédito abatido ao activo                                                                                                                            | Written-off credit                                                                                                                                |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 5                                              | Crédito renegociado                                                                                                                                  | Renegotiated credit                                                                                                                               |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 6                                              | Crédito vencido em litígio judicial                                                                                                                  | Overdue credit in litigation                                                                                                                      |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+
| 7                                              | Crédito abatido ao ativo em litígio judicial                                                                                                         | Written-off credit in litigation                                                                                                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------+


[Return](#table-of-contents)


## Overdue Class

+------------------------------------------------+---------------------------------------------+------------------------------------+
| Code                                           | Designação                                  | Designation                        |
+:===============================================+:============================================+:===================================+
| 1                                              | Até 1 mês                                   | Up to 1 month                      |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 2                                              | Mais de 1 até 2 meses                       | From 1 to 2 months                 |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 3                                              | Mais de 1 até 2 meses                       | From 2 to 3 months                 |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 4                                              | Mais de 3 até 6 meses                       | From 3 to 6 months                 |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 5                                              | Mais de 6 até 9 meses                       | From 6 to 9 months                 |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 6                                              | Mais de 9 até 12 meses                      | From 9 to 12 months                |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 7                                              | Mais de 12 até 15 meses                     | From 12 to 15 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 8                                              | Mais de 15 até 18 meses                     | From 15 to 18 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 9                                              | Mais de 18 até 24 meses                     | From 18 to 24 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 10                                             | Mais de 24 até 30 meses                     | From 24 to 30 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 11                                             | Mais de 30 até 36 meses                     | From 30 to 36 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 12                                             | Mais de 36 até 48 meses                     | From 36 to 48 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 13                                             | Mais de 48 até 60 meses                     | From 48 to 60 months               |
+------------------------------------------------+---------------------------------------------+------------------------------------+
| 14                                             | Mais de 60 meses                            | More than 60 months                |
+------------------------------------------------+---------------------------------------------+------------------------------------+

[Return](#table-of-contents)


## Financial Product

+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| Code                                           | Designação                                                                               | Designation                                                        |
+:===============================================+:=========================================================================================+:===================================================================+
| 1                                              | Desconto e outros créditos titulados por efeitos                                         | Discount and other credits secured by effects                      |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 2                                              | Créditos em conta corrente                                                               | Current account (credit lines)                                     |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 3                                              | Descobertos em depósitos à ordem                                                         | Overdrafts on deposit accounts                                     |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 4                                              | Factoring com recurso                                                                    | Recourse factoring                                                 |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 5                                              | Factoring sem recurso                                                                    | None-recourse factoring                                            |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 6                                              | Leasing imobiliário                                                                      | Real estate leasing                                                |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 7                                              | Leasing mobiliário                                                                       | Non-real estate leasing                                            |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 8                                              | Financiamentos à actividade empresarial ou equiparada                                    | Financing to the corporate activity or equivalent                  |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 9                                              | Cartão de crédito                                                                        | Credit card                                                        |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 10                                             | Crédito à habitação                                                                      | Mortgage credit                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 11                                             | Crédito ao consumo                                                                       | Consumer credit                                                    |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 12                                             | Crédito automóvel                                                                        | Automobile credit                                                  |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 13                                             | Outros créditos                                                                          | Other credit                                                       |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 14                                             | Avales e garantias bancárias prestadas a favor de outras instituições participantes      | Bank Guarantees from other participating institutions              |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+
| 15                                             | Outros avales e garantias bancárias prestadas                                            | Other bank guarantees                                              |
+------------------------------------------------+------------------------------------------------------------------------------------------+--------------------------------------------------------------------+

[Return](#table-of-contents)


## Maturity Class

**Version January, 2009**

+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| Code                                           | Designação                                      | Designation                                       |
+:===============================================+:================================================+:==================================================+
| 1                                              | Indeterminado                                   | Undefined                                         |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 2                                              | Até 90 dias                                     | Up to 90 days                                     |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 3                                              | Mais de 90 até 180 dias                         | From 90 days to 180 days                          |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 4                                              | Mais de 180 dias até 1 ano                      | From 180 days to 1 year                           |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 5                                              | Mais de 1 até 5 anos                            | From  1  to 5 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 6                                              | Mais de 5 até 10 anos                           | From  5  to 10 years                              |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 7                                              | Mais de 10 até 20 anos                          | From  10  to 20 years                             |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 8                                              | Mais de 20 até 25 anos                          | From 20 to 25 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 9                                              | Mais de 25 até 30 anos                          | From 25 to 30 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 10                                             | Mais de 30 anos                                 | Over 30 years                                     |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+


**Version December, 2013**


+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| Code                                           | Designação                                      | Designation                                       |
+:===============================================+:================================================+:==================================================+
| 1                                              | Indeterminado                                   | Undefined                                         |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 2                                              | Até 90 dias                                     | Up to 90 days                                     |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 3                                              | Mais de 90 até 180 dias                         | From 90 days to 180 days                          |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 4                                              | Mais de 180 dias até 1 ano                      | From 180 days to 1 year                           |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 51                                             | Mais de 1 até 2 anos                            | From  1  to 2 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 52                                             | Mais de 2 até 3 anos                            | From  2  to 3 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 53                                             | Mais de 3 até 4 anos                            | From  3  to 4 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 54                                             | Mais de 4 até 5 anos                            | From  4  to 5 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 61                                             | Mais de 5 até 6 anos                            | From  5  to 6 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 62                                             | Mais de 6 até 7 anos                            | From  6  to 7 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 63                                             | Mais de 7 até 8 anos                            | From  7  to 8 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 64                                             | Mais de 8 até 9 anos                            | From  8  to 9 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 65                                             | Mais de 9 até 10 anos                           | From  9  to 10 years                              |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 71                                             | Mais de 10 até 15 anos                          | From  10  to 15 years                             |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 72                                             | Mais de 15 até 20 anos                          | From  15  to 20 years                             |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 8                                              | Mais de 20 até 25 anos                          | From 20 to 25 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 9                                              | Mais de 25 até 30 anos                          | From 25 to 30 years                               |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+
| 10                                             | Mais de 30 anos                                 | Over 30 years                                     |
+------------------------------------------------+-------------------------------------------------+---------------------------------------------------+




[Return](#table-of-contents)

## Collateral Type

**Version January, 2009**

+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| Code                                           | Designação                                                              | Designation                                                            |
+:===============================================+:========================================================================+:=======================================================================+
| 1                                              | Colateral real hipotecário                                              | Real collateral mortgage                                               |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| 2                                              | Colateral real - não hipotecário                                        | Real collateral - not mortgaged                                        |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| 3                                              | Colateral financeiro                                                    | Financial Collateral                                                   |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| 4                                              | Garantia pessoal – prestada por uma empresa ou particular               | Personal guarantee - Provided by firm or individual                    |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| 5                                              | Garantia pessoal – prestada pelo Estado ou instituição financeira       | Personal guarantee - Granted by the State or financial institution     |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+
| 6 	                                           | Outras garantias	                                                   | Other guarantees                                                       |
+------------------------------------------------+-------------------------------------------------------------------------+------------------------------------------------------------------------+


**Version June, 2014**


+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| Code                                           | Designação                                                                                                         | Designation                                                                                             |
+:===============================================+:===================================================================================================================+:========================================================================================================+
| 1                                              | Colateral real hipotecário                                                                                         | Real collateral mortgage                                                                                |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 2                                              | Colateral real - não hipotecário                                                                                   | Real collateral - not mortgaged                                                                         |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 31                                             | Colateral financeiro – Depósitos                                                                                   | Financial Collateral - deposits                                                                         |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 32                                             | Colateral financeiro – Dívida pública portuguesa                                                                   | Financial Collateral – Portuguese public debt                                                           |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 33                                             | Colateral financeiro – Dívida pública de não residentes e organizações multilaterais de desenvolviment             | Financial Collateral – Public debt of non-residents and multinational organizations                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 34                                             | Colateral financeiro – Dívida de outras entidades                                                                  | Financial Collateral – Debt of other entities                                                           |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 35                                             | Colateral financeiro – Ações e outras participações financeiras cotadas                                            | Financial Collateral – Stocks and other participations in listed companies                              |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 36                                             | Colateral financeiro – Ações e outras participações financeiras não cotadas                                        | Financial Collateral – Stocks and other participations in unlisted companies                            |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 39                                             | Colateral financeiro – Outros instrumentos	                                                                       | Financial Collateral – Other instruments                                                                |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 4                                              | Garantia pessoal – prestada por uma empresa ou particular                                                          | Personal guarantee - Provided by firm or individual                                                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 51                                             | Garantia pessoal – Prestada pelo Estado Português                                                                  | Personal guarantee - Granted by the Portuguese State                                                    |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 52                                             | Garantia pessoal – Prestada por outros Estados ou por organizações multilaterais de desenvolvimento                | Personal guarantee - Granted by other governments or by multinational organizations                     |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 53                                             | Garantia pessoal – Prestada por instituições financeiras                                                           | Personal guarantee - Granted by financial institutions                                                  |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+
| 6                                              | Outras garantias                                                                                                   | Other guarantees                                                                                        |
+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------+



[Return](#table-of-contents)


## Special Characteristics

|Code |  Designação  |  Designation  |
|:--------|:---------------|:---------------|
| 1	                                             | Crédito cedido em operação de titularização não desreconhecida com a intervenção de um veículo financeiro residente                                                      | Credit conceded in a recognized securitization operation with the intervention of a resident financial vehicle               |
| 2	                                             | Crédito cedido em operação de titularização não desreconhecida com a intervenção de um veículo financeiro não residente	                                                | Credit conceded in a recognized securitization operation with the intervention of a nonresident financial vehicle            |
| 3	                                             | Crédito cedido em operação de titularização desreconhecida com a intervenção de um veículo financeiro residente	                                                        | Credit conceded in an unrecognized securitization operation with the intervention of a resident financial vehicle            |
| 4                                              | Crédito cedido em operação de titularização desreconhecida com a intervenção de um veículo financeiro não residente                                                      | Credit conceded in an unrecognized securitization operation with the intervention of a nonresident financial vehicle         |
| 5	                                             | Crédito sindicado                                                                                                                                                        | Syndicated loan                                                                                                              |
| 6	                                             | Crédito afeto a obrigações hipotecárias	                                                                                                                                | Mortgage-backed loan                                                                                                         |
| 7	                                             | Crédito afeto a obrigações sobre o sector público                                                     	                                                                  | Public loan                                                                                                                  |
| 8	                                             | Crédito associado a contas poupança-emigrante para aquisição de prédios	                                                                                                | Credit associated with emigrant´s savings accounts for purchasing buildings                                                  |
| 9	                                             | Crédito associado a contas poupança-emigrante para outras finalidades	                                                                                                  | Credit associated with emigrant´s savings accounts for other purposes                                                        |
| 10                                             | Crédito para proteção de habitação própria permanente (Dec. Lei 103/2009)	                                                                                              | Credit for protecting permanent housing property (Decree-Law103/2009)                                                        |
| 11                                             | Empréstimo entregue como garantia para as operações de crédito do Eurosistema (Instrução 7/2012)	                                                                        | Loan extended as collateral for credit operations in Eurosystem (Instruction N.º 7/2012)                                     |
| 12                                             | Empréstimo caracterizado com código de identificação (IEB)	                                                                                                              | Loan featured with identification code (IEB) (Instruction N.º 7/2012)                                                        |
| 13                                             | Crédito reestruturado por dificuldades financeiras do cliente (Instrução 18/2012)	                                                                                      | Credit restructured for customers in financial difficulties (Instruction 18/2012))                                           |
| 14                                             | Crédito em risco (Instrução 16/2004)	                                                                                                                                    | Credit at risk (Instruction 16/2004)                                                                                         |
| 15                                             | Crédito integrado num Procedimento Extrajudicial de Regularização de Situações de Incumprimento (PERSI) (DL 227/2012) ou num Regime Extraordinário (Lei 58/2012)	        | Credit in an out-of-course renegotiation procedure (PERSI) (Decree-Law No. 227/2012) or in a Special Regime (Law 58/2012)    |


[Return](#table-of-contents)


## Country

|Code |  Designation  |
|:--------|:---------------|
ABW	|	Aruba	|
AFG	|	Afghanistan	|
AGO	|	Angola	|
AIA	|	Anguilla	|
ALA	|	Aland Islands	|
ALB	|	Albania	|
AND	|	Andorra	|
ANT	|	Netherlands Antilles	|
ARE	|	United Arab Emirates	|
ARG	|	Argentina	|
ARM	|	Armenia	|
ASM	|	American Samoa	|
ATA	|	Antarctica	|
ATF	|	South territories of France	|
ATG	|	Antigua and Barbuda	|
AUS	|	Australia	|
AUT	|	Austria	|
AZE	|	Azerbaijan	|
BDI	|	Burundi	|
BEL	|	Belgium	|
BEN	|	Benin	|
BFA	|	Burkina Faso	|
BGD	|	Bangladesh	|
BGR	|	Bulgaria	|
BHR	|	Bahrain	|
BHS	|	Bahamas	|
BIH	|	Bosnia Herzegovina	|
BLM	|	St. Bartholomew	|
BLR	|	Belarus	|
BLZ	|	Belize	|
BMU	|	Bermuda	|
BOL	|	Bolivia	|
BRA	|	Brazil	|
BRB	|	Barbados	|
BRN	|	Brunei	|
BTN	|	Bhutan	|
BVT	|	Bouvet Island (Norway Territory)	|
BWA	|	Botswana	|
CAF	|	Central African Republic	|
CAN	|	Canada	|
CCK	|	Cocos	|
CHE	|	Switzerland	|
CHL	|	Chile	|
CHN	|	China	|
CIV	|	Costa do Marfim	|
CMR	|	Cameroon	|
COD	|	Democratic Republic of Congo (former Zaire)	|
COG	|	Congo	|
COK	|	Cook Islands	|
COL	|	Colombia	|
COM	|	Comoros	|
CPV	|	Cape Verde	|
CRI	|	Costa Rica	|
CUB	|	Cuba	|
CUW	|	Curacao	|
CXR	|	Christmas island	|
CYM	|	Cayman Islands	|
CYP	|	Cyprus	|
CZE	|	Czech republic	|
DEU	|	Germany	|
DJI	|	Djibouti	|
DMA	|	dominica	|
DNK	|	Denmark	|
DOM	|	Dominican Republic	|
DZA	|	Algeria	|
ECU	|	Ecuador	|
EGY	|	Egypt	|
ERI	|	Eritrea	|
ESH	|	Western Sahara (former Spanish Sahara)	|
ESP	|	Spain	|
EST	|	Estonia	|
ETH	|	Ethiopia	|
FIN	|	Finland	|
FJI	|	Fiji	|
FLK	|	Falkland Islands (Malvinas)	|
FRA	|	France	|
FRO	|	Faroes Islands	|
FSM	|	Micronesia	|
GAB	|	Gabon	|
GBR	|	Great Britain (United Kingdom, UK)	|
GEO	|	Georgia	|
GGY	|	Guernsey	|
GHA	|	Ghana	|
GIB	|	Gibraltar	|
GIN	|	Guinea	|
GLP	|	Guadeloupe	|
GMB	|	Gambia	|
GNB	|	Guinea Bissau	|
GNQ	|	Equatorial Guinea	|
GRC	|	Greece	|
GRD	|	Grenade	|
GRL	|	Greenland	|
GTM	|	Guatemala	|
GUF	|	French Guiana	|
GUM	|	Guam (US Territory)	|
GUY	|	Guiana	|
HKG	|	Hong Kong	|
HMD	|	Heard and McDonald Islands (territory of Australia)	|
HND	|	Honduras	|
HRV	|	Croatia (Hrvatska)	|
HTI	|	Haiti	|
HUN	|	Hungary	|
IDN	|	Indonesia	|
IMN	|	Isle of Man	|
IND	|	India	|
IOT	|	Territory British Indian Ocean	|
IRL	|	Ireland	|
IRN	|	Will	|
IRQ	|	Iraq	|
ISL	|	Iceland	|
ISR	|	Israel	|
ITA	|	Italy	|
JAM	|	Jamaica	|
JEY	|	jersey	|
JOR	|	Jordan	|
JPN	|	Japan	|
KAZ	|	Kazakhstan	|
KEN	|	Kenya	|
KGZ	|	Kyrgyzstan	|
KHM	|	Cambodia	|
KIR	|	Kiribati	|
KNA	|	Saint Kitts and Nevis	|
KOR	|	South Korea	|
KWT	|	Kuwait	|
LAO	|	Laos	|
LBN	|	Lebanon	|
LBR	|	Liberia	|
LBY	|	Libya	|
LCA	|	Saint Lucia	|
LIE	|	Liechtenstein	|
LKA	|	Sri Lanka	|
LSO	|	Lesotho	|
LTU	|	Lithuania	|
LUX	|	Luxembourg	|
LVA	|	Latvia	|
MAC	|	Macao	|
MAF	|	St. Martin	|
MAR	|	Morocco	|
MCO	|	Monaco	|
MDA	|	Moldova	|
MDG	|	Madagascar	|
MDV	|	Maldives	|
MEX	|	Mexico	|
MHL	|	Marshall Islands	|
MKD	|	Macedonia (Republic Yugoslav)	|
MLI	|	Mali	|
MLT	|	Malta	|
MMR	|	Myanmar (former Burma)	|
MNE	|	Montenegro	|
MNG	|	Mongolia	|
MNP	|	Northern Mariana Islands	|
MOZ	|	Mozambique	|
MRT	|	Mauritania	|
MSR	|	montserrat	|
MTQ	|	Martinique	|
MUS	|	Mauritius	|
MWI	|	Malawi	|
MYS	|	Malaysia	|
MYT	|	Mayotte	|
NAM	|	Namibia	|
NCL	|	New Caledonia	|
NER	|	Niger	|
NFK	|	Norfolk Islands	|
NGA	|	Nigeria	|
NIC	|	Nicaragua	|
NIU	|	Niue	|
NLD	|	Netherlands	|
NOR	|	Norway	|
NPL	|	Nepal	|
NRU	|	Nauru	|
NZL	|	New Zealand	|
OMN	|	Oman	|
PAK	|	Pakistan	|
PAN	|	Panama	|
PCN	|	Pitcairn island	|
PER	|	Peru	|
PHL	|	Philippines	|
PLW	|	Palau	|
PNG	|	Papua New Guinea	|
POL	|	Poland	|
PRI	|	Puerto Rico	|
PRK	|	North Korea	|
PRT	|	Portugal	|
PRY	|	Paraguay	|
PSE	|	Occupied Palestinian Territories	|
PYF	|	French Polynesian	|
QAT	|	Qatar	|
REU	|	Reunion island	|
ROU	|	Romania	|
RUS	|	Russian Federation	|
RWA	|	Rwanda	|
SAU	|	Saudi Arabia	|
SDN	|	Sudan	|
SEN	|	Senegal	|
SGP	|	Singapore	|
SGS	|	South Georgia and the South Sandwich Islands	|
SHN	|	Saint Helen	|
SJM	|	Svalbard and Jan Mayen Islands	|
SLB	|	Solomon Islands	|
SLE	|	Sierra Leone	|
SLV	|	El Salvador	|
SMR	|	San Marino	|
SOM	|	Somalia	|
SPM	|	St. Pierre and Miquelon	|
SRB	|	Serbia	|
STP	|	Sao Tome and Principe	|
SUR	|	Suriname	|
SVK	|	Slovakia	|
SVN	|	Slovenia	|
SWE	|	Sweden	|
SWZ	|	Swaziland	|
SYC	|	Seychelles	|
SYR	|	Syria	|
TCA	|	Turks and Caicos Islands	|
TCD	|	Chad	|
TGO	|	Togo	|
THA	|	Thailand	|
TJK	|	Tajikistan	|
TKL	|	Tokelau Islands	|
TKM	|	Turkmenistan	|
TLS	|	East Timor (former East Timor)	|
TON	|	Tonga	|
TTO	|	Trinidad and Tobago	|
TUN	|	Tunisia	|
TUR	|	Turkey	|
TUV	|	Tuvalu	|
TWN	|	Taiwan	|
TZA	|	Tanzania	|
UGA	|	Uganda	|
UKR	|	Ukraine	|
UMI	|	US Outlying Islands	|
URY	|	Uruguay	|
USA	|	U.S	|
UZB	|	Uzbekistan	|
VAT	|	Vatican	|
VCT	|	Saint Vincent and the Grenadines	|
VEN	|	Venezuela	|
VGB	|	Virgin Islands (England)	|
VIR	|	Virgin Islands (United States)	|
VNM	|	Vietnam	|
VUT	|	Vanuatu	|
WLF	|	Wallis and Futuna Islands	|
WSM	|	Western Samoa	|
YEM	|	Yemen	|
ZAF	|	South Africa	|
ZMB	|	Zambia	|
ZWE	|	Zimbabwe	|


[Return](#table-of-contents)


## Currency

|Code |  Designation  |
|:--------|:---------------|
AED	|	UAE Dirham	|
ALL	|	Lek	|
AMD	|	Armenian Dram	|
ANG	|	Netherlands Antillean Guilder	|
AOA	|	Kwanza	|
ARS	|	Argentine Peso	|
AUD	|	Australian Dollar	|
AWG	|	Aruban Florin	|
AZN	|	Azerbaijan Manat	|
BAM	|	Convertible Mark	|
BBD	|	Barbados Dollar	|
BDT	|	Taka	|
BGN	|	Bulgarian Lev	|
BHD	|	Bahraini Dinar	|
BIF	|	Burundi Franc	|
BMD	|	Bermudian Dollar	|
BND	|	Brunei Dollar	|
BOB	|	Boliviano	|
BOV	|	Mvdol	|
BRL	|	Brazilian Real	|
BSD	|	Bahamian Dollar	|
BTN	|	Ngultrum	|
BWP	|	Pula	|
BYN	|	Belarusian Ruble	|
BZD	|	Belize Dollar	|
CAD	|	Canadian Dollar	|
CDF	|	Congolese Franc	|
CHE	|	WIR Euro	|
CHF	|	Swiss Franc	|
CHW	|	WIR Franc	|
CLF	|	Unidad de Fomento	|
CLP	|	Chilean Peso	|
CNY	|	Yuan Renminbi	|
COP	|	Colombian Peso	|
COU	|	Unidad de Valor Real	|
CRC	|	Costa Rican Colon	|
CUC	|	Peso Convertible	|
CUP	|	Cuban Peso	|
CVE	|	Cabo Verde Escudo	|
CZK	|	Czech Koruna	|
DJF	|	Djibouti Franc	|
DKK	|	Danish Krone	|
DOP	|	Dominican Peso	|
DZD	|	Algerian Dinar	|
EGP	|	Egyptian Pound	|
ERN	|	Nakfa	|
ETB	|	Ethiopian Birr	|
EUR	|	Euro	|
FJD	|	Fiji Dollar	|
FKP	|	Falkland Islands Pound	|
GBP	|	Pound Sterling	|
GEL	|	Lari	|
GHS	|	Ghana Cedi	|
GIP	|	Gibraltar Pound	|
GMD	|	Dalasi	|
GNF	|	Guinean Franc	|
GTQ	|	Quetzal	|
GYD	|	Guyana Dollar	|
HKD	|	Hong Kong Dollar	|
HNL	|	Lempira	|
HRK	|	Kuna	|
HTG	|	Gourde	|
HUF	|	Forint	|
IDR	|	Rupiah	|
ILS	|	New Israeli Sheqel	|
INR	|	Indian Rupee	|
IQD	|	Iraqi Dinar	|
IRR	|	Iranian Rial	|
ISK	|	Iceland Krona	|
JMD	|	Jamaican Dollar	|
JOD	|	Jordanian Dinar	|
JPY	|	Yen	|
KES	|	Kenyan Shilling	|
KGS	|	Som	|
KHR	|	Riel	|
KMF	|	Comorian Franc 	|
KPW	|	North Korean Won	|
KRW	|	Won	|
KWD	|	Kuwaiti Dinar	|
KYD	|	Cayman Islands Dollar	|
KZT	|	Tenge	|
LAK	|	Lao Kip	|
LBP	|	Lebanese Pound	|
LKR	|	Sri Lanka Rupee	|
LRD	|	Liberian Dollar	|
LSL	|	Loti	|
LYD	|	Libyan Dinar	|
MAD	|	Moroccan Dirham	|
MDL	|	Moldovan Leu	|
MGA	|	Malagasy Ariary	|
MKD	|	Denar	|
MMK	|	Kyat	|
MNT	|	Tugrik	|
MOP	|	Pataca	|
MRU	|	Ouguiya	|
MUR	|	Mauritius Rupee	|
MVR	|	Rufiyaa	|
MWK	|	Malawi Kwacha	|
MXN	|	Mexican Peso	|
MXV	|	Mexican Unidad de Inversion (UDI)	|
MYR	|	Malaysian Ringgit	|
MZN	|	Mozambique Metical	|
NAD	|	Namibia Dollar	|
NGN	|	Naira	|
NIO	|	Cordoba Oro	|
NOK	|	Norwegian Krone	|
NPR	|	Nepalese Rupee	|
NZD	|	New Zealand Dollar	|
OMR	|	Rial Omani	|
PAB	|	Balboa	|
PEN	|	Sol	|
PGK	|	Kina	|
PHP	|	Philippine Peso	|
PKR	|	Pakistan Rupee	|
PLN	|	Zloty	|
PYG	|	Guarani	|
QAR	|	Qatari Rial	|
RON	|	Romanian Leu	|
RSD	|	Serbian Dinar	|
RUB	|	Russian Ruble	|
RWF	|	Rwanda Franc	|
SAR	|	Saudi Riyal	|
SBD	|	Solomon Islands Dollar	|
SCR	|	Seychelles Rupee	|
SDG	|	Sudanese Pound	|
SEK	|	Swedish Krona	|
SGD	|	Singapore Dollar	|
SHP	|	Saint Helena Pound	|
SLL	|	Leone	|
SOS	|	Somali Shilling	|
SRD	|	Surinam Dollar	|
SSP	|	South Sudanese Pound	|
STN	|	Dobra	|
SVC	|	El Salvador Colon	|
SYP	|	Syrian Pound	|
SZL	|	Lilangeni	|
THB	|	Baht	|
TJS	|	Somoni	|
TMT	|	Turkmenistan New Manat	|
TND	|	Tunisian Dinar	|
TOP	|	Pa’anga	|
TRY	|	Turkish Lira	|
TTD	|	Trinidad and Tobago Dollar	|
TWD	|	New Taiwan Dollar	|
TZS	|	Tanzanian Shilling	|
UAH	|	Hryvnia	|
UGX	|	Uganda Shilling	|
USD	|	US Dollar	|
UYU	|	Peso Uruguayo	|
UYW	|	Unidad Previsional	|
UZS	|	Uzbekistan Sum	|
VES	|	Bolívar Soberano	|
VND	|	Dong	|
VUV	|	Vatu	|
WST	|	Tala	|
XAF	|	CFA Franc BEAC	|
XCD	|	East Caribbean Dollar	|
XOF	|	CFA Franc BCEAO	|
XPF	|	CFP Franc	|
XSU	|	Sucre	|
XUA	|	ADB Unit of Account	|
YER	|	Yemeni Rial	|
ZAR	|	Rand	|
ZMW	|	Zambian Kwacha	|
ZWL	|	Zimbabwe Dollar	|

Versão 1.0.9

-bug de não atualizar corrigido. (o legal que ele nasceu quando eu resolvi os bugs anteriors, mas tudo bem)

Versão 1.0.8

-BUGS CORRIGIDOS

Versão 1.0.7
- Ao clicar no preparar banco, ele pergunta se voce deseja truncar ou não a cadpar2

Versão 1.0.6
- Adicionado um novo botão para usuarios REC
-  Comandos sql executados por esse botão
( 

INSERT INTO {usuarioSelecionado}.CADCAR (CCCODCAR, CCNOMCAR, CCTIPACE, CCALTPED02) VALUES (COALESCE((SELECT MAX(CCCODCAR) + 1 FROM {usuarioSelecionado}.CADCAR),1),'CARGOTESTE','2','N');

INSERT INTO {usuarioSelecionado}.CADUSRCODUSR,NOMUSR,CODCAR,SENUSR,FONE,ENDER,BAIRRO,CIDADE,UF,CEP,CPF,RG,FECHADIA,TEMPO,LIBSU01,LIBSU02,LIBSU03,LIBSU04,LIBSU05,LIBSU06,LIBSU07,LIBSU08,LIBSU09,LIBSU10,LIBSU11,LIBSU12,LIBSU13,LIBSU14,LIBSU15,LIBSU16,LIBSU17,LIBSU18,LIBSU19,LIBSU20,FONE2,LIBSU21,LIBSU23,LIBSU24,LIBSU25,LIBSU26,LIBSU27,FONE3,LIBSU28,ESCOLARIDADE,VEICULO_MODELO,VEICULO_ANO,VEICULO_PLACA,CNH_NUM,CNH_CAT,CNH_VCTO,TE_NUM,TE_ZONA,TE_SECAO,TE_EMIS,CTPS_NUM,CTPS_SERIE,CTPS_UF,CTPS_EMIS,CC_BANCO,CC_AGENCIA,CC_TITULAR,CC_CONTA,CR_NUM,CC_TIPO,CR_SERIE,CR_CAT,CR_EMIS,CONTATO1,FONECONT1,CONTATO2,ORGAO,FONECONT2,DTNASC,DTADM,DTDEM,TIPOUSR,LIBCARGA,LIBBALC,LIBENTRG,EMAIL,LIBSU30,LIBSU31,LIBSU32,LIBSU33,VER_LSEP,VER_CONF,VER_VOL,VER_EMI,VER_LFIN,LIBSU38,ACEDS_SA,LIBSU39,LIBSU40,LIBSU41,TEM_AVISO_SONORO,LIBSU42,LIBSU90,LIBSU37,LIBSU36,LIBSU35,LIBSU34,LIBSU29,ATIVO_SN,LIBSU43,LIBSU44,LIBSU45) values ('999900','    USUARIO TESTE',(select cccodcar from {usuarioSelecionado}.cadcar where ccnomcar like '%CARGOTESTE'),'Kabcde',null,null,null,null,null,null,null,null,'N',null,'N','N','N','N','N','N','N','N','N','N','N','N','N','N','N','N','N','N','N','N',null,'N','N','N','N','N','N',null,'N',null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,'N',null,null,null,null,null,null,null,null,null,null,null,'1',null,null,null,null,'N','N','N','N','S','S','S','S','S','N','N','N','N','N','N','N','N','N','N','N','N','N','S','N','N','N');

INSERT INTO {usuarioSelecionado}.lotpro (lpcodpro, lplote, lpqtd,lpcodemp,lpcontrole) SELECT pdcodpro, 'loteTeste', 9999,1, {usuarioSelecionado}.CTRL_LOTPRO.NEXTVAL FROM {usuarioSelecionado}.cadpro WHERE pdstatus <> 8;

truncate table {usuarioSelecionado}.cadpar2;
)
- Principal função e preparar um novo banco de dados para utilização

Versão 1.0.5

- O criar tabelas agora esta presente na aba principal da aplicação.
- O botão a qual o criar tabelas era usando antes recebera reformulação de função.
- O sistema esta de forma geral mais estavel.
- Adicionado de patch notes.

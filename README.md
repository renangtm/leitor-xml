# leitor de xml

Algoritmo pequeno de utilização simples, que converte uma String XML em formato JSON para facilitar sua manipulação,

Exemplo de utilização
<code>

var xml = '\<?xml version="1.0" encoding="UTF-8"?\>
\<nfeProc xmlns="http://www.portalfiscal.inf.br/nfe" versao="4.00"\>
\<NFe\>
\<det nItem="1"\>
\<xnome\>
teste
\</xnome\>
\</det\>
\<det nItem="2"\>
\<xnome\>
teste
\</xnome\>
\</det\>
\<det nItem="2"\>
\<xnome\>
teste
\</xnome\>
\</det\>
\</NFe\>
\</xml\>'

var json = xmlToJson(xml,0);

alert(json.version); // mostra 1.0

alert(json.nfeProc.xmlns); // mostra http://www.portalfiscal.inf.br/nfe

alert(json.NFe.det[0].nItem); // mostra 1

alert(json.NFe.det[0].xnome); // mostra teste

</code>

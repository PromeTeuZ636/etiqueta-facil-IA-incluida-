# Etiqueta Fácil

Editor de etiquetas baseado no modelo enviado: código de barras à esquerda; nome do produto, dois códigos e validade à direita.

## Abrir no VS Code

1. Extraia o ZIP.
2. No VS Code, use **Arquivo → Abrir Pasta** e selecione `etiqueta-facil`.
3. Abra `index.html` no navegador. Não precisa instalar Node.js, npm ou banco de dados.
4. Opcionalmente, use um servidor de desenvolvimento da sua preferência para atualizar a página durante a edição.

## Arquivos

- `index.html`: campos e estrutura da tela.
- `style.css`: aparência, adaptação ao celular e estilos de impressão.
- `app.js`: prévia, código EAN-13, validação, armazenamento local e impressão.
- `referencia.jpg`: imagem do modelo original exibida na seção de referência.

## Usar

Preencha os campos, confira a prévia e escolha tamanho, quantidade e papel. Clique em **Imprimir / salvar PDF**. O PDF é salvo pela janela de impressão do navegador.

Na impressão, use escala de 100%, desative cabeçalhos e rodapés e confira o tamanho do papel. Faça uma impressão de teste para validar as medidas e a leitura do código de barras na impressora do cliente.

O tamanho inicial é 100 × 25 mm, ajustável. Os nomes dos dois códigos à direita são provisórios. A fonte aproxima o modelo; não reproduz exatamente a fonte da foto.

Os últimos dados preenchidos ficam no armazenamento local do navegador. Não existe cadastro, servidor ou compartilhamento dos campos entre computadores. O funcionamento pode variar ao abrir diretamente por `file://`; um servidor local ou hospedagem oferece um endereço estável para o armazenamento.

## Colocar no GitHub

Crie um repositório vazio na sua conta. No terminal do VS Code, dentro desta pasta, execute os comandos abaixo, substituindo `SEU_USUARIO` e o nome do repositório pela URL real:

```bash
git init
git add .
git commit -m "Adiciona editor de etiquetas"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/etiqueta-facil.git
git push -u origin main
```

O Git precisa estar instalado e a autenticação no GitHub deve ser feita com sua própria conta. Nenhuma credencial está incluída neste projeto.

Se preferir, envie os arquivos pela interface do GitHub. Mantenha `index.html`, `style.css`, `app.js` e `referencia.jpg` juntos na raiz do repositório.

Enviar o código ao GitHub e disponibilizar o programa como site são etapas distintas. Este projeto é estático e pode ser hospedado em um serviço que publique HTML, CSS e JavaScript, como GitHub Pages. A hospedagem deste ZIP é independente da versão de teste criada na conversa.

## Conferências realizadas

- Verificação de sintaxe JavaScript.
- Validação do EAN-13 do exemplo e rejeição de dígito verificador inválido.
- Conferência da prévia e dos campos no navegador.
- Geração de 12 etiquetas em duas páginas A4 no tamanho inicial.

Não foi realizada uma impressão física ou leitura com scanner.

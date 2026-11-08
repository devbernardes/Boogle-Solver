# Boggle Solver PWA — protótipo 0.1

## Incluído
- PWA com manifest, ícone vetorial e service worker.
- Importação de screenshot.
- OCR por Tesseract.js em português, processando cada uma das 25 casas separadamente.
- Ajuste manual do retângulo de recorte.
- Grade 5×5 editável.
- Dicionário pt_BR VERO/Hunspell baixado sob demanda do repositório LibreOffice.
- Busca DFS com Trie, sem reutilizar casas e considerando 8 vizinhos.
- Exibição do caminho de cada palavra.

## Limitações importantes
- OCR ainda precisa ser calibrado com screenshots reais; revise as letras antes da busca.
- O dicionário Hunspell contém entradas-base e marcações de afixos. Esta versão remove as marcações, mas ainda não expande todas as flexões gramaticais; pode perder palavras flexionadas.
- O dicionário e o OCR precisam ser baixados na primeira execução. O app-shell fica em cache pelo service worker; recursos externos podem exigir rede na primeira utilização.
- A validação ortográfica não garante que toda palavra seja aceita pelo Boggle Party.
- O recorte padrão é aproximado; ajuste Topo/Altura/Esquerda/Largura se necessário.
- A instalação como PWA exige hospedagem HTTPS.

## Fontes
Dicionário pt_BR VERO/LibreOffice: https://github.com/LibreOffice/dictionaries/tree/master/pt_BR
OCR Tesseract.js v5: https://github.com/naptha/tesseract.js

## Publicação
Ative GitHub Pages nas configurações do repositório, usando a branch main e a pasta /(root). Depois abra a URL Pages no Chrome Android e escolha “Instalar app” ou “Adicionar à tela inicial”.
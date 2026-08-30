# Camera Project — detector facial didático

Aplicação web didática para fins exclusivamente educacionais. O projeto demonstra como acessar a câmera pelo navegador, detectar faces em tempo real e capturar uma imagem com as marcações encontradas.

> **Aviso:** este projeto não identifica pessoas, não realiza reconhecimento facial e não deve ser usado para vigilância, controle de acesso ou decisões sobre indivíduos. O processamento ocorre no navegador e nenhuma foto é enviada ou armazenada em servidor.

## Funcionalidades

- Visualização da câmera em tempo real.
- Detecção simultânea de múltiplas faces.
- Caixa delimitadora e nível de confiança para cada face.
- Contador de faces detectadas.
- Captura da imagem com as marcações.
- Download da captura em PNG.
- Interface responsiva para computador e celular.

## Tecnologias

- HTML, CSS e JavaScript.
- Node.js para servidor local e build.
- face-api.js com o modelo Tiny Face Detector.
- API `getUserMedia` do navegador.

## Requisitos

- Node.js 18 ou superior.
- npm.
- Navegador moderno com acesso à câmera.
- Câmera integrada ou conectada ao dispositivo.

## Configuração passo a passo

1. Clone o repositório e entre na pasta:

   ```bash
   git clone https://github.com/w3aewander/camera-project.git
   cd camera-project
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Inicie o servidor:

   ```bash
   npm start
   ```

4. Abra no navegador:

   ```text
   http://localhost:8000
   ```

5. Clique em **Ligar câmera** e permita o acesso quando o navegador solicitar.

6. Posicione uma ou mais faces diante da câmera. As caixas azuis, a confiança e o contador serão atualizados automaticamente.

7. Clique no botão circular para capturar uma foto. Use **Baixar foto** para salvar o PNG.

8. Clique em **Desligar** para encerrar o acesso à câmera.

## Scripts

| Comando | Descrição |
| --- | --- |
| `npm start` | Inicia o servidor na porta 8000. |
| `npm run dev` | Inicia o mesmo servidor para desenvolvimento. |
| `npm run build` | Gera a versão publicável na pasta `dist/`. |

É possível alterar temporariamente a porta:

```bash
PORT=9000 npm start
```

## Build de produção

Execute:

```bash
npm run build
```

Sirva o conteúdo da pasta `dist/` em uma origem HTTPS. Por segurança, navegadores normalmente permitem câmera apenas em `localhost` ou HTTPS.

## Estrutura principal

```text
camera-project/
├── models/          # Pesos locais do detector facial
├── scripts/
│   ├── build.js     # Geração da pasta dist
│   └── serve.js     # Servidor HTTP local
├── src/
│   ├── app.js       # Câmera, detecção e captura
│   └── style.css    # Interface responsiva
├── index.html
└── package.json
```

## Privacidade e limitações

- A detecção é executada localmente no navegador.
- O projeto detecta a presença de faces, mas não reconhece identidades.
- Iluminação, distância, ângulo e desempenho do dispositivo afetam os resultados.
- A porcentagem exibida representa a confiança estimada do detector, não a identidade de alguém.
- Solicite consentimento antes de apontar a câmera para outras pessoas.
- Use somente como exemplo de estudo e aprendizado.

## Licença e uso

Material demonstrativo destinado a estudo de desenvolvimento web e visão computacional. Antes de reutilizar em outro contexto, avalie requisitos legais, éticos, de privacidade e de consentimento aplicáveis.

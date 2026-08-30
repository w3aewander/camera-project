# Camera Project â€” detector facial didÃ¡tico

AplicaÃ§Ã£o web didÃ¡tica para fins exclusivamente educacionais. O projeto demonstra como acessar a cÃ¢mera pelo navegador, detectar faces em tempo real e capturar uma imagem com as marcaÃ§Ãµes encontradas.

> **Aviso:** este projeto nÃ£o identifica pessoas, nÃ£o realiza reconhecimento facial e nÃ£o deve ser usado para vigilÃ¢ncia, controle de acesso ou decisÃµes sobre indivÃ­duos. O processamento ocorre no navegador e nenhuma foto Ã© enviada ou armazenada em servidor.

## Funcionalidades

- VisualizaÃ§Ã£o da cÃ¢mera em tempo real.
- DetecÃ§Ã£o simultÃ¢nea de mÃºltiplas faces.
- Caixa delimitadora e nÃ­vel de confianÃ§a para cada face.
- Contador de faces detectadas.
- Captura da imagem com as marcaÃ§Ãµes.
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
- Navegador moderno com acesso Ã  cÃ¢mera.
- CÃ¢mera integrada ou conectada ao dispositivo.

## ConfiguraÃ§Ã£o passo a passo

1. Clone o repositÃ³rio e entre na pasta:

   ```bash
   git clone https://github.com/w3aewander/camera-project.git
   cd camera-project
   ```

2. Instale as dependÃªncias:

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

5. Clique em **Ligar cÃ¢mera** e permita o acesso quando o navegador solicitar.

6. Posicione uma ou mais faces diante da cÃ¢mera. As caixas azuis, a confianÃ§a e o contador serÃ£o atualizados automaticamente.

7. Clique no botÃ£o circular para capturar uma foto. Use **Baixar foto** para salvar o PNG.

8. Clique em **Desligar** para encerrar o acesso Ã  cÃ¢mera.

## Scripts

| Comando | DescriÃ§Ã£o |
| --- | --- |
| `npm start` | Inicia o servidor na porta 8000. |
| `npm run dev` | Inicia o mesmo servidor para desenvolvimento. |
| `npm run build` | Gera a versÃ£o publicÃ¡vel na pasta `dist/`. |

Ã‰ possÃ­vel alterar temporariamente a porta:

```bash
PORT=9000 npm start
```

## Build de produÃ§Ã£o

Execute:

```bash
npm run build
```

Sirva o conteÃºdo da pasta `dist/` em uma origem HTTPS. Por seguranÃ§a, navegadores normalmente permitem cÃ¢mera apenas em `localhost` ou HTTPS.

## Estrutura principal

```text
camera-project/
â”œâ”€â”€ models/          # Pesos locais do detector facial
â”œâ”€â”€ scripts/
â”‚   â”œâ”€â”€ build.js     # GeraÃ§Ã£o da pasta dist
â”‚   â””â”€â”€ serve.js     # Servidor HTTP local
â”œâ”€â”€ src/
â”‚   â”œâ”€â”€ app.js       # CÃ¢mera, detecÃ§Ã£o e captura
â”‚   â””â”€â”€ style.css    # Interface responsiva
â”œâ”€â”€ index.html
â””â”€â”€ package.json
```

## Privacidade e limitaÃ§Ãµes

- A detecÃ§Ã£o Ã© executada localmente no navegador.
- O projeto detecta a presenÃ§a de faces, mas nÃ£o reconhece identidades.
- IluminaÃ§Ã£o, distÃ¢ncia, Ã¢ngulo e desempenho do dispositivo afetam os resultados.
- A porcentagem exibida representa a confianÃ§a estimada do detector, nÃ£o a identidade de alguÃ©m.
- Solicite consentimento antes de apontar a cÃ¢mera para outras pessoas.
- Use somente como exemplo de estudo e aprendizado.

## LicenÃ§a e uso

Material demonstrativo destinado a estudo de desenvolvimento web e visÃ£o computacional. Antes de reutilizar em outro contexto, avalie requisitos legais, Ã©ticos, de privacidade e de consentimento aplicÃ¡veis.


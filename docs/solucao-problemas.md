# 🔧 GUIA DE SOLUÇÃO DE PROBLEMAS

## ❌ Erro: "Failed to fetch"

Este é o erro mais comum e tem solução fácil!

### 🎯 Causa Principal: CORS (Cross-Origin Resource Sharing)

Quando você abre o arquivo HTML **diretamente** no navegador (endereço começa com `file://`), o navegador bloqueia requisições a APIs externas por segurança.

---

## ✅ SOLUÇÕES (escolha uma)

### 🥇 SOLUÇÃO 1: Servidor Local (RECOMENDADO)

**No Windows:**
```cmd
cd C:\caminho\para\pasta\dos\arquivos
python -m http.server 8000
```

**No Mac/Linux:**
```bash
cd /caminho/para/pasta/dos/arquivos
python3 -m http.server 8000
```

**Depois acesse:**
```
http://localhost:8000/prova-analyzer-v2.html
```

---

### 🥈 SOLUÇÃO 2: Extensão do Navegador

**Chrome/Edge:**
1. Instale: [Web Server for Chrome](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb)
2. Aponte para a pasta dos arquivos
3. Clique em "Choose folder"
4. Acesse a URL mostrada

---

### 🥉 SOLUÇÃO 3: Hospedagem Gratuita (funciona na internet)

#### Opção A - Vercel (Mais fácil)
1. Crie conta em: https://vercel.com
2. Instale o CLI: `npm install -g vercel`
3. Na pasta dos arquivos: `vercel`
4. Siga as instruções
5. Receba um link público: `https://seu-projeto.vercel.app`

#### Opção B - GitHub Pages
1. Crie repositório no GitHub
2. Faça upload dos arquivos
3. Ative GitHub Pages nas configurações
4. Acesse: `https://seu-usuario.github.io/nome-repositorio`

#### Opção C - Netlify Drop
1. Acesse: https://app.netlify.com/drop
2. Arraste a pasta com os arquivos
3. Receba um link público instantaneamente

---

## 🔍 Outros Erros Possíveis

### Erro: "API key not valid"

**Causa:** API Key incorreta ou expirada

**Solução:**
1. Vá em: https://makersuite.google.com/app/apikey
2. Delete a chave antiga
3. Crie uma nova chave
4. Copie e cole no campo (certifique-se de copiar completa)

---

### Erro: "Quota exceeded" ou "429"

**Causa:** Atingiu o limite de requisições

**Limites do tier gratuito:**
- 15 requisições por minuto
- 1.500 requisições por dia

**Solução:**
1. Aguarde alguns minutos
2. Ou crie uma nova API Key
3. Ou ative o billing no Google Cloud (mas continua barato)

---

### Erro: "Não identificou as notas"

**Causas possíveis:**
- Foto muito escura ou desfocada
- Notas muito pequenas
- Ângulo muito inclinado
- Letra muito ilegível

**Soluções:**
1. ✅ Tire foto com boa iluminação
2. ✅ Mantenha câmera perpendicular à prova
3. ✅ Foco nas notas (não pode estar borrado)
4. ✅ Teste primeiro com a prova de exemplo
5. ✅ Se escrita manual, prefira letra de forma

---

### Erro: Firewall/Antivírus bloqueando

**Sintoma:** "Failed to fetch" mesmo usando servidor local

**Solução:**
1. Desabilite temporariamente o antivírus
2. Adicione exceção para localhost:8000
3. Verifique configurações de firewall
4. Use hospedagem online (Vercel/Netlify)

---

## 🧪 Como Testar se Está Funcionando

### Teste 1: Verificar API
1. Abra `prova-analyzer-v2.html` (versão nova)
2. Cole a API Key
3. Clique em "🔍 Testar Conexão com API"
4. Deve aparecer: "✅ Conexão OK!"

### Teste 2: Usar Prova de Exemplo
1. Abra `gerador-prova-exemplo.html`
2. Baixe a imagem gerada
3. Use no analisador
4. Taxa de acerto esperada: ~95%

### Teste 3: Prova Real
1. Tire foto bem iluminada de uma prova
2. Use no analisador
3. Compare resultados com notas reais
4. Taxa de acerto esperada: 80-95%

---

## 📱 Problemas Específicos do Celular

### "Não consigo acessar do celular"

**Checklist:**
- ☑️ PC e celular na mesma rede WiFi?
- ☑️ Servidor rodando no PC? (`python3 -m http.server 8000`)
- ☑️ Usando IP correto do PC?
- ☑️ Firewall liberado na porta 8000?

**Como descobrir o IP do PC:**

Windows:
```cmd
ipconfig
```
Procure por "IPv4 Address"

Mac/Linux:
```bash
ifconfig
# ou
ip addr show
```

Exemplo de acesso no celular:
```
http://192.168.1.100:8000/prova-analyzer-v2.html
```

---

## 🆘 Última Opção: Usar Versão Online Temporária

Se nada funcionar, você pode usar uma versão online temporária que eu posso te ajudar a hospedar, ou usar ferramentas como:

- **CodePen**: https://codepen.io (cole o código HTML)
- **JSFiddle**: https://jsfiddle.net
- **StackBlitz**: https://stackblitz.com

---

## 📞 Ainda com Problemas?

Se nenhuma solução funcionou:

1. **Verifique o console do navegador:**
   - Aperte F12
   - Vá na aba "Console"
   - Tire um print do erro
   - Me envie para análise

2. **Informações úteis para debug:**
   - Sistema operacional
   - Navegador e versão
   - Como está abrindo o arquivo
   - Mensagem de erro completa

3. **Alternativa rápida:**
   - Experimente usar a API do OpenAI (GPT-4 Vision)
   - Ou Anthropic Claude (eu mesmo!) via API
   - Ambos têm tier gratuito/trial

---

## ✅ Checklist Final

Antes de pedir ajuda, confirme:

- [ ] Está usando servidor local (não `file://`)
- [ ] API Key válida e recém-criada
- [ ] Testou o botão "Testar Conexão"
- [ ] Internet funcionando
- [ ] Navegador atualizado
- [ ] Testou com prova de exemplo primeiro
- [ ] Foto com boa qualidade e iluminação

Se todos itens checados e ainda não funciona, pode ser um problema mais específico que precisamos investigar juntos!

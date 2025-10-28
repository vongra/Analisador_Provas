# 🚀 GUIA RÁPIDO - COMEÇAR EM 5 MINUTOS

## Passo 1: Obter API Key (2 minutos)

1. Abra: https://makersuite.google.com/app/apikey
2. Faça login com Google
3. Clique em "Create API Key"
4. Copie a chave

## Passo 2: Gerar Prova de Teste (1 minuto)

1. Abra `gerador-prova-exemplo.html` no navegador
2. Clique em "Baixar como Imagem"
3. Salve a imagem

## Passo 3: Testar o Analisador (2 minutos)

1. Abra `prova-analyzer.html` no navegador
2. Cole a API Key no campo
3. Carregue a imagem da prova
4. Clique em "Analisar Prova com IA"
5. Veja os resultados!

## 📱 Para Usar no Celular

### Opção Fácil:
1. No PC, na pasta dos arquivos, execute:
   ```bash
   python3 -m http.server 8000
   ```

2. Descubra o IP do seu PC:
   - Windows: `ipconfig` no cmd
   - Mac/Linux: `ifconfig` ou `ip addr`

3. No celular (mesma rede WiFi), acesse:
   ```
   http://SEU-IP:8000/prova-analyzer.html
   ```
   Exemplo: `http://192.168.1.100:8000/prova-analyzer.html`

### Opção para Internet:
1. Crie conta gratuita em https://vercel.com
2. Faça upload dos arquivos
3. Acesse de qualquer lugar!

## ❓ Problemas Comuns

**"Erro na API do Gemini"**
- Verifique se copiou a API Key completa
- Certifique-se de ter ativado a API no Google AI Studio

**"Não identificou as notas"**
- Tente com imagem mais clara e perpendicular
- Certifique-se que as notas estão visíveis
- Teste com a prova de exemplo primeiro

**"Não abre no celular"**
- PC e celular precisam estar na mesma rede WiFi
- Verifique se o firewall não está bloqueando a porta 8000

## 💡 Próximos Testes

Depois de validar com a prova de exemplo:

1. Teste com provas reais escaneadas
2. Teste com fotos de celular
3. Teste com diferentes tipos de letra
4. Avalie a taxa de acerto

## 📊 O Que Observar

- ✅ Taxa de acerto na identificação
- ✅ Tempo de processamento
- ✅ Qualidade mínima da foto necessária
- ✅ Facilidade de uso para professores

## 🎯 Decisão Final

Após os testes, você poderá decidir:

**Se precisão > 85%**: 
- ✅ Viável para MVP
- Use API em produção inicialmente
- Economize tempo e recursos

**Se precisão < 85%**:
- Considere pré-processamento de imagem
- Teste outros modelos (GPT-4 Vision)
- Ou adicione validação manual

---

**Tempo total estimado**: 5-10 minutos para primeiro teste completo!

Boa sorte com seu projeto! 🎉

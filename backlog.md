# Mercapp  
## Backlog do Produto Priorizado (Detalhado com Tarefas)  
---

## **Sprint 1: Definição do Produto e Estrutura Básica**  
**Objetivo:** Estabelecer a base do aplicativo, incluindo a arquitetura, design inicial, fluxo de navegação e funcionalidades essenciais.

### **US01: Criação do Protótipo no Figma**  
`Como equipe de design, eu quero criar um protótipo do aplicativo no Figma, para validar a experiência do usuário antes do desenvolvimento.`   

**Tarefas:**  
1. Criar wireframes das telas principais (Home, Login, Lista de Produtos, Carrinho).  
2. Definir fluxo de navegação entre telas.  
3. Validar protótipo com usuários internos (equipe de desenvolvimento).  
4. Ajustar design com base em feedbacks.  

**Critérios de Aceitação:**  
- Protótipo interativo no Figma com pelo menos 5 telas principais.  
- Fluxo de navegação aprovado pela equipe.  

### **US02: Cadastro de Usuário**  
`Como cliente, eu quero me cadastrar no aplicativo usando meu e-mail ou número de telefone, para acessar funcionalidades personalizadas.`  

**Tarefas:**  
1. Desenvolver tela de cadastro com campos: e-mail, senha e telefone.  
2. Implementar validação de e-mail e senha (mínimo 6 caracteres).  
3. Integrar API de verificação por SMS (ex: Twilio).  
4. Criar banco de dados para armazenar usuários.  

**Critérios de Aceitação:**  
- Usuário pode se cadastrar com e-mail + senha ou telefone + SMS.  
- Dados salvos no banco de dados com criptografia de senha.  

### **US03: Listagem de Produtos**  
`Como cliente, eu quero visualizar a lista de produtos disponíveis no supermercado, para escolher o que desejo comprar.`  

**Tarefas:**  
1. Criar interface de lista de produtos por categoria.  
2. Integrar API de busca por nome.  
3. Desenvolver cards de produtos com imagem, nome e preço.  

**Critérios de Aceitação:**  
- Lista exibe produtos organizados por categorias.  
- Busca retorna resultados em tempo real.  

### **US04: Cadastro de Produtos (Admin)**  
`Como administrador, eu quero cadastrar produtos no sistema, para mantê-los atualizados no aplicativo.`  

**Tarefas:**  
1. Criar painel administrativo (CRUD de produtos).  
2. Implementar upload de imagens para produtos.  
3. Validar campos obrigatórios (nome, preço, categoria).  

**Critérios de Aceitação:**  
- Admin pode adicionar/editar/excluir produtos.  
- Campos inválidos exibem mensagens de erro.  

---

## **Sprint 2: Funcionalidades de Compra e Navegação**  
**Objetivo:** Implementar carrinho, filtros e checkout.  

### **US05: Adicionar Produtos ao Carrinho**  
`Como cliente, eu quero adicionar produtos ao carrinho de compras, para finalizar minha compra posteriormente`  

**Tarefas:**  
1. Adicionar botão "Comprar" em cada produto.  
2. Desenvolver tela de carrinho com lista de itens e total.  
3. Salvar carrinho localmente (AsyncStorage/SQLite).  

**Critérios de Aceitação:**  
- Itens persistem no carrinho mesmo após fechar o app.  

### **US06: Filtros e Ordenação**  
`Como cliente, eu quero filtrar produtos por categoria, preço ou promoções, para encontrar o que preciso mais rapidamente.`  
**Tarefas:**  
1. Implementar dropdown de filtros (categoria, preço).  
2. Adicionar botões de ordenação (preço crescente/decrescente).  

**Critérios de Aceitação:**  
- Filtros aplicados em tempo real.  

### **US07: Finalização de Compra**  
`Como cliente, eu quero finalizar minha compra com opções de pagamento e entrega, para receber meus produtos em casa.`  

**Tarefas:**  
1. Integrar gateways de pagamento (PIX, cartão).  
2. Desenvolver tela de confirmação de pedido.  

**Critérios de Aceitação:**  
- Usuário recebe e-mail de confirmação após compra.  

---

## **Sprint 3: Personalização e Relacionamento**  
**Objetivo:** Adicionar notificações, avaliações e fidelidade.  

### **US08: Notificações Personalizadas**  
`Como cliente, eu quero receber notificações sobre promoções e ofertas personalizadas, para economizar em minhas compras.`  

**Tarefas:**  
1. Desenvolver sistema de tags baseado em histórico de compras
2. Criar templates de notificações para promoções
3. Implementar disparo automático de notificações

**Critérios de Aceitação:**  
- Notificações são recebidas em dispositivos Android e iOS.  
- Usuários com histórico de compras recebem ofertas relevantes (ex: cliente de cervejas recebe promoção de drinks).  
- Taxa de abertura de notificações acima de 20% (métrica pós-lançamento).  

---

### **US09: Avaliação do Aplicativo**  
`Como cliente, eu quero avaliar o aplicativo após a efetuação de um pedido.`  

**Tarefas:**  
1. Desenvolver modal de avaliação
2. Armazenar avaliações no banco de dados: Coletar nota, comentário, ID do pedido e ID do usuário.  
3. Dashboard de feedbacks (Admin): Exibir métricas de avaliação (média, tendências) no painel administrativo.  
4. Redirecionar usuários que derem 4+ estrelas para avaliar na Play Store/App Store.  

**Critérios de Aceitação:**  
- Modal aparece apenas uma vez por pedido concluído.  
- Avaliações são salvas e podem ser filtradas por período no painel admin.  
- Se nota ≤ 2, sistema abre formulário para detalhar problemas (ex: "O que não funcionou?").  

---

## **Sprint 4: Integrações e Plano de Marketing**  
**Objetivo:** Finalizar integrações técnicas e preparar campanhas de lançamento.  

---

### **US10: Integração com Estoque**  
`Como administrador, eu quero integrar o aplicativo com o sistema de estoque do supermercado, para garantir que os produtos estejam sempre atualizados.`  

**Tarefas:**  
1. Desenvolver API de integração com o sistema de estoque existente  
2. Implementar atualização automática de estoque  
3. Criar sistema de notificação para reposição    

**Critérios de Aceitação:**  
- Atualização de estoque refletida no app em até 5 minutos  
- Painel administrativo com alertas de estoque crítico (<5 unidades)  
- Taxa de erro na integração < 0.1% em testes de carga  

---

### **US11: Relatórios de Vendas**  
`Como administrador, eu quero visualizar relatórios de vendas e desempenho do aplicativo.`  

**Tarefas:**  
1. Desenvolver dashboard analítico  
2. Implementar filtros avançados  
3. Criar funcionalidade de exportação  

**Critérios de Aceitação:**  
- Dados atualizados em tempo real com no máximo 1 minuto de delay  
- Sistema suporta geração de relatórios com 50k+ registros  
- Exportação em PDF mantém formatação profissional  

---

### **US12: Campanhas Promocionais**  
`Como equipe de marketing, eu quero criar campanhas promocionais no aplicativo.`  

**Tarefas:**  
1. Desenvolver editor de campanhas  
   - Upload de banners  
   - Configuração de datas e descontos  
2. Implementar sistema de cupons   
3. Criar painel de performance  
   - Taxa de conversão por campanha  
   - ROI estimado  

**Critérios de Aceitação:**  
- Campanhas podem ser publicadas em até 15 minutos  
- Cupons com limites de uso funcionam corretamente  
- Métricas atualizadas a cada 30 minutos  

---

## **Sprint 5: Lançamento e Ajustes Finais**  
**Objetivo:** Publicar aplicativo e executar plano de marketing.  

---

### **US14: Publicação nas Lojas**  
`Como administrador, eu quero publicar o aplicativo nas lojas oficiais.`  

**Tarefas:**  
1. Preparar assets para publicação na App Store e Play Store  
2. Configurar builds finais  
   - Versão Android (APK/AAB)  
   - Versão iOS (IPA)  
3. Submeter para aprovação  

**Critérios de Aceitação:**  
- Aprovado nas lojas em até 72h (Google Play) e 7 dias (App Store)  
- Notas médias acima de 4.2 estrelas na primeira semana  
----

### **US15: Plano de Lançamento**  
`Como equipe de marketing, eu quero executar o plano de lançamento.`  

**Tarefas:**  
1. Campanha de pré-lançamento  
2. Estratégia pós-lançamento    
3. Monitoramento de resultados    

---

### **US16: Feedback Pós-Lançamento**  
`Como cliente, eu quero enviar feedback sobre minha experiência.`  

**Tarefas:**  
1. Implementar formulário de avaliação  
2. Criar sistema de priorização      

---
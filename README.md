# Loja de variedades

Protótipo React/Vite de loja comercial multicategorias, com busca, filtros, ordenação, carrinho demonstrativo e cupons.

## Funcionalidades

- Catálogo de eletrônicos, casa, beleza, acessórios e presentes
- Botões e fotos de produtos iniciam um pedido no WhatsApp com mensagem codificada
- Carrinho demonstrativo com quantidades e cupons
- Temas e cores personalizáveis; imagem de fundo apenas por upload; alternância entre modo claro/escuro
- Até cinco fotos por produto, adicionadas pelo computador e navegáveis por miniaturas na vitrine; imagens existentes podem ser mantidas ao editar
- Vitrine inicial simplificada; detalhes, opções de compra e carrinho são exibidos em telas próprias
- Upload da foto da identidade da loja, com otimização local no navegador
- Atalho visível “Área da equipe” na home, com painel demonstrativo de login
- Criação e gerenciamento de logins da equipe pelo administrador, com permissões para identidade da loja, cupons, redes sociais e produtos
- Edição do nome e da foto da loja pela Área da equipe; imagens enviadas são otimizadas e salvas neste navegador
- Criação, pausa, ativação e remoção de cupons percentuais pela Área da equipe
- Configuração dos links de Instagram, Facebook, TikTok e YouTube, exibidos no cabeçalho e no rodapé da loja
- Tela de abertura animada e transições na vitrine, nos produtos e nas telas de compra
- Layout adaptado para celular; animações respeitam a preferência por movimento reduzido

## Executar

```bash
npm install
npm run dev
```

## Publicação

O GitHub Actions publica esta loja no GitHub Pages a cada atualização da branch `main`:

https://neysidi40-debug.github.io/variedades/

A Área da equipe está em `/admin/`. O acesso é demonstrativo e não protege informações em uma página pública.

## Acesso administrativo demonstrativo

Use o atalho **Área da equipe** no cabeçalho da home ou acesse `/admin`. Entre com o login `admin` e a senha padrão `zoo2026`. Para trocar a senha da conta principal localmente, configure `VITE_ADMIN_PASSWORD` e reinicie o Vite. A conta principal pode criar logins, selecionar as áreas permitidas e pausar, ativar ou remover os acessos da equipe. Cada login criado precisa de pelo menos uma permissão e uma senha de seis caracteres ou mais.

Este é somente um protótipo: os logins e permissões ficam no `localStorage` deste navegador e não são sincronizados entre dispositivos. As senhas de equipe são armazenadas como hashes locais, mas a autenticação e as permissões são controladas pelo frontend e podem ser contornadas; não use dados reais nem considere o painel seguro para produção. Um sistema real precisa validar identidade e autorização no servidor.

## Build e limitações

```bash
npm run build
```

LocalStorage não sincroniza entre dispositivos. Cupons, contas da equipe e checkout são demonstrativos, sem pagamento real; os cupons aceitam descontos percentuais de 1% a 100%. Redes sociais e catálogo são salvos neste navegador. O WhatsApp usa `+55 81 98976-9880`; as imagens do catálogo são URLs externas HTTPS.

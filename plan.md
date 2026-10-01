# Plano de implementação — PARIRA JUSI

## Escopo
Landing page institucional de uma página para apresentar a PARIRA JUSI, empresa do ramo de geradores de energia. O site será em português do Brasil, com foco em geração de leads para orçamento e conteúdo setorial profissional sem inventar dados empresariais específicos.

## Arquitetura e entrega
- Site estático, adequado ao conteúdo público e à indexação.
- Vite + HTML/CSS/JavaScript modular e leve; sem backend, login, banco ou dependências de UI pesadas.
- O output de publicação será `dist/`, gerado pelo comando `npm run build`.
- Uma única rota pública `/`, com `public/manus-routes.json` declarando a rota.
- Assets versionados na pasta `public/assets`; HTML sem cache compartilhado agressivo e assets estáticos com cache longo quando publicados.

## Experiência e conteúdo
1. Header fixo com wordmark, navegação por âncora e CTA de orçamento.
2. Hero com proposta "Energia para o seu próximo movimento", CTAs WhatsApp/formulário e visual técnico de gerador/rotor.
3. Faixa de benefícios: continuidade, segurança operacional, suporte técnico e dimensionamento.
4. Soluções com cards para locação, venda/fornecimento e manutenção — tratadas como oferta ajustável.
5. Seção institucional curta, sem histórico ou certificações inventadas.
6. Aplicações editáveis: obras, indústria, eventos, agronegócio e operações críticas.
7. Processo em quatro passos: entender, dimensionar, instalar, acompanhar.
8. CTA final e formulário de orçamento com campos de nome, empresa, telefone, cidade, necessidade e mensagem. O envio mostra feedback local e deixa o contato provisório claramente marcado.
9. Rodapé com dados de contato provisórios e aviso de personalização.

## Design e assets
- Seguir `ideas.md`: Pulso Industrial, navy, azul elétrico e lime, tipografia Space Grotesk/Inter/IBM Plex Mono.
- Criar logo específico para o projeto e aplicar no header e favicon.
- Criar um hero visual original com gerador industrial e rotor abstrato, sem texto embutido, para evitar aparência de banco de imagens.
- Responsividade em desktop, tablet e celular; respeitar `prefers-reduced-motion`.

## SEO e acessibilidade
- HTML com conteúdo significativo, título, meta description, Open Graph e Twitter Card.
- H1 único, hierarquia H2/H3, `lang=pt-BR`, labels de formulário, foco visível e contraste alto.
- Canonical/og:url não serão inventados enquanto a URL pública definitiva não estiver disponível.
- `robots.txt` e `sitemap.xml` podem ser adicionados quando o domínio público for definido; o gateway gerenciado atende defaults na ausência desses arquivos.

## Verificação
- Instalar dependências com pnpm e executar `npm run build`/`pnpm build`.
- Iniciar servidor no listener configurado pelo Webdev e verificar HTTP 200 para `/` e `/manus-routes.json`.
- Inspecionar código e checar que todos os CTAs apontam para âncoras/WhatsApp provisório, os campos provisórios estão sinalizados e não há promessa factual não confirmada.

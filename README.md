# Kit Redes Sociais

Kit enxuto de 24 skills para marketing em redes sociais, com foco em Instagram e TikTok.
É uma curadoria de seis pacotes de código aberto, sem vínculo com ferramentas pagas. Cada
função tem uma skill dedicada, e a skill geral `social` complementa as dedicadas.

## O que tem aqui

| Função | Skill | Origem |
|---|---|---|
| Sistema de ideias e banco de pautas | `idea-generation-and-ideation` | Frank Heijdenrijk |
| Pilares de conteúdo | `content-pillars` | Frank Heijdenrijk |
| Tendências do momento | `trend-jacking` | Frank Heijdenrijk |
| Datas e sazonalidade | `seasonal-and-moment-marketing` | Frank Heijdenrijk |
| Desmontar um post viral | `viral-reverse-engineering` | Frank Heijdenrijk |
| Ganchos | `hook-writer` | Frank Heijdenrijk |
| Roteiro de TikTok | `tiktok-script` | Frank Heijdenrijk |
| Crescimento no TikTok | `tiktok-growth` | Frank Heijdenrijk |
| Carrossel | `carousel-writer` | Frank Heijdenrijk |
| Roteiro de Reels com nota de gancho | `ig-reel` | Jake Schincariol (adaptação PT-BR) |
| Pesquisa do que funciona no nicho | `ig-viral` | Jake Schincariol (adaptação PT-BR) |
| Plano da semana no Instagram | `ig-plan` | Jake Schincariol (adaptação PT-BR) |
| Auditoria do que já foi postado | `ig-audit` | Jake Schincariol (adaptação PT-BR) |
| Legenda | `ig-caption` | Jake Schincariol (adaptação PT-BR) |
| Tirar a cara de IA do texto | `ig-human` | Jake Schincariol (adaptação PT-BR) |
| Hashtags | `ig-hashtag-strategist` | Serge Bulaev |
| Perfil do Instagram | `ig-profile-optimizer` | Serge Bulaev |
| Matriz de conteúdo (pilares x formatos) | `content-matrix` | Charlie Hills |
| Notícias do nicho na semana | `niche-research` | Charlie Hills |
| Visão geral de redes sociais (LinkedIn, X, Facebook, calendário, reaproveitamento, engajamento, análise) | `social` | Corey Haines |
| Copy de páginas e ofertas | `copywriting` | Corey Haines |
| Psicologia aplicada ao marketing | `marketing-psychology` | Corey Haines |
| Criativos de anúncio | `ad-creative` | Corey Haines |
| Comunidades de WhatsApp | `whatsapp-community` | kit-510-ptbr (kursku/skills) |

## O que foi alterado em relação aos originais

- Removidas as menções ao agendador pago WoopSocial nas skills de Frank Heijdenrijk
  (trocadas por "a ferramenta de agendamento do usuário" ou por analytics nativo).
- Removida a seção "Tool Integrations" de `ad-creative`, que apontava para o registro de
  ferramentas e parceiros do repositório original, e o guia que comparava geradores de
  imagem, vídeo e voz.
- `social`: removidos o trecho que indicava agendadores (um deles do mantenedor do pacote)
  e os dados de Telegram atribuídos ao produto de um colaborador. Descrição reescrita e nota
  de precedência adicionada para ela complementar as skills dedicadas.
- `social`: três números que contradiziam as skills dedicadas foram alinhados a elas:
  frequência no Instagram (segue `ig-plan`), frequência no TikTok (segue `tiktok-growth`)
  e duração de Reels (segue `ig-reel`).
- Removidas as pastas de avaliação (`evals`) e de testes, que não são usadas em tempo de uso.
- `ig-hashtag-strategist`: as duas referências compartilhadas do pacote original foram
  copiadas para dentro da skill.
- `ad-creative`: a referência `meta-decision-system.md`, que os arquivos dela citam e que
  morava em outra skill do pacote original, foi copiada para dentro da skill.
- `content-matrix` e `whatsapp-community`: descrição reescrita para a skill ser acionada
  no momento certo.
- Nota adicionada no topo das skills de Frank Heijdenrijk avisando que algumas skills
  irmãs citadas não fazem parte do kit.

O conteúdo das instruções não foi reescrito além disso.

## Limitações conhecidas

- A maior parte das skills está em inglês. Elas respondem em português quando o pedido
  vem em português. As seis `ig-*` de Reels, pesquisa, plano, auditoria, legenda e
  humanizador já estão em português do Brasil.
- As skills `ig-*` guardam voz, swipe file, histórico e plano em `~/.claude/instagram/`.
  Isso persiste no Claude Code. No app, sem uma pasta conectada, vale só para a conversa.
- `ig-reel`, `ig-viral`, `ig-caption` e `ig-human` usam scripts Python locais, só com a
  biblioteca padrão e sem acesso à rede.
- `ig-viral` pesquisa com o navegador do próprio usuário, em ritmo humano. Não usa API.
- `whatsapp-community` vem de um catálogo com cara de conteúdo gerado em lote; trate os
  números de referência dela como ponto de partida, não como dado verificado.

## Instalação em outros dispositivos

**Claude Code (terminal):** com acesso de leitura a este repositório privado configurado no git do
dispositivo, rode:

```
/plugin marketplace add ericescolastico/kit-redes-sociais
/plugin install kit-redes-sociais@kit-redes-sociais
```

**App do Claude:** clone o repositório, gere o arquivo do plugin e abra-o numa conversa para
aceitar a instalação:

```
git clone https://github.com/ericescolastico/kit-redes-sociais.git
cd kit-redes-sociais
zip -r ../kit-redes-sociais.plugin . -x ".git/*" -x "*.DS_Store"
```

## Como atualizar

1. Edite as skills em `skills/`.
2. Suba o número da versão em `.claude-plugin/plugin.json` e em `.claude-plugin/marketplace.json`.
3. Anote a mudança em `CHANGELOG.md` e faça o commit.

## Licenças

Todas as origens são MIT. Os textos de licença estão em `licenses/` e os créditos
detalhados em `NOTICE.md`.

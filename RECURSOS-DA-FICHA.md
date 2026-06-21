# Ficha de Personagem — D&D 2024 / Aliança de Heróis
### Resumo completo de recursos (features)

*Grupo Pró=RPG · documento gerado em 2026-06-21*

Aplicativo de **ficha de personagem em arquivo único** (HTML), que abre direto no navegador, **sem instalar nada**, calcula tudo sozinho e salva automaticamente. Cobre o **D&D 2024 (Livro do Jogador)** somado ao homebrew **Aliança de Heróis** e ao **Suplemento AdH** do Grupo Pró=RPG.

🌐 **No ar:** https://jsimaoneto.github.io/Ficha-ProRPG/

---

## 1. Visão geral

- **Arquivo único** (`.html`, ~240 KB) — funciona offline, basta abrir no navegador.
- **Salvamento automático** no próprio navegador (localStorage) a cada alteração.
- **Três páginas** prontas para impressão: (1) ficha principal, (2) Talentos · Qualidades · Defeitos, (3) descrições e habilidades.
- **Responsivo** — adaptado para celular e tablet (toque).
- **Identidade visual Pró=RPG / Aliança de Heróis**: papel pergaminho, vermelho (#7a1f1f) + dourado (#a8862b), fonte serifada, brasão com o logo real Pró=RPG, e um **medalhão/emblema por classe**.

---

## 2. Conteúdo de jogo embutido

| Categoria | Quantidade | Observações |
|---|---:|---|
| **Classes** | **18** | 12 oficiais do D&D 2024 + 2 do Aliança (★) + 4 do Suplemento (✦) |
| Classes conjuradoras | 8 | cálculo de conjuração automático |
| **Espécies** | 10 | |
| **Antecedentes** | 16 | |
| **Atributos** | 6 | FOR · DES · CON · INT · SAB · CAR |
| **Perícias** | 18 | |
| **Talentos D&D 2024** | 75 | Origem (10) · Geral (43) · Estilo de Luta (10) · Dádiva Épica (12) |
| **Talentos de Nível Zero** (Aliança) | 24 | escolhidos na criação |
| **Qualidades** (Aliança) | 25 | custam pontos |
| **Defeitos** (Aliança) | 27 | concedem pontos |
| **Habilidades de Classe escolhíveis** | 92 (4 grupos) | Caçador de Demônios, Homem do Oeste, Faz Tudo, Fantasma |
| **Habilidades automáticas por nível** | — | Assassino do Credo, Espectro + 5 trilhas/subclasses |
| **Itens mágicos** | 5 raridades | Comuns · Incomuns · Raros · Muito Raros · Lendários |
| **Maestrias de armas** | 8 | D&D 2024 |
| **Armas / Armaduras** | 38 / 13 | em ordem alfabética |
| **Descrições de itens** | 358 | base do painel "Descrição dos Itens Escolhidos" |

### Classes incluídas
**Oficiais (D&D 2024):** Bárbaro, Bardo, Bruxo, Clérigo, Druida, Feiticeiro, Guardião, Guerreiro, Ladino, Mago, Monge, Paladino.
**Aliança de Heróis (★):** Assassino do Credo, Caçador de Demônios.
**Suplemento AdH (✦):** Homem do Oeste (d10), Faz Tudo (d8), Espectro (usa o PV do corpo possuído), Fantasma (d10).

> Subclasses homebrew aparecem marcadas com **★** nas listas.

---

## 3. Cálculos automáticos

A ficha calcula sozinha, em tempo real:

- **Modificadores** dos seis atributos.
- **Bônus de Proficiência** pelo nível total de personagem.
- **Salvaguardas** (com proficiência marcável) + bônus de itens.
- **Perícias** (com proficiência e especialização) + bônus por atributo e por perícia.
- **Percepção Passiva**, **Iniciativa**, **Classe de Armadura**.
- **Dados de Vida** (somando por classe na multiclasse).
- **Conjuração**: atributo, CD de magia e bônus de ataque mágico; **nível de conjurador** multiclasse (incluindo Cavaleiro Místico e Trapaceiro Arcano com 1/3).

---

## 4. Progressão de nível e multiclasse

- **Níveis 0 a 20.** O **Nível 0 (Criação)** deixa os atributos editáveis; ao escolher a 1ª classe, vai ao Nível 1 e trava os atributos (a partir daí mudam só por Aumento de Habilidade).
- **Até 3 classes** (multiclasse), com checagem dos **pré-requisitos** do Livro do Jogador 2024.
- **Subir nível com escolha de classe:** ao clicar em "▲ Subir nível" com multiclasse, você **escolhe em qual classe** aplicar o nível.
- **Soma correta entre classes**, mesmo subindo fora de ordem (ex.: Paladino → Guerreiro → Paladino). Há um histórico interno da ordem dos níveis.
- **Descer nível** remove o **último nível efetivamente ganho** (na classe certa) e desfaz as escolhas feitas naquele nível.
- **Painel resumo** mostra "Níveis por classe" e os Dados de Vida totais.

---

## 5. Aumento de Habilidade (ASI)

- Avisa nos níveis certos **de cada classe** (inclusive tabelas próprias de Guerreiro e Ladino).
- A cada Aumento, escolha: **+2 em atributos** (com setas ▲▼, máx. 20) **ou** um **Talento**.
- O **talento escolhido entra nos cálculos** da ficha (bônus e vantagens aplicados), com botão **"+ Adicionar"** e confirmação ✓.
- A lista de talentos do ASI já respeita todas as regras de escolha (abaixo).

---

## 6. Regras de escolha (travas inteligentes)

Implementadas para impedir combinações inválidas:

- **Talentos só na criação:** o seletor de talentos da página 2 só funciona nos **Níveis 0–1** (Talentos de Nível Zero + Talento de Origem). Do Nível 2 em diante, talento novo vem **só pelo painel Aumento de Habilidade** (ao subir de nível).
- **Sem repetição:** um talento/item **não pode ser escolhido mais de uma vez** — exceto os que dizem isso na própria descrição (ex.: *Habilidoso*, *Aumento no Valor de Atributo*, *Iniciado em Magia*). Itens já escolhidos **somem das opções**.
- **Validade por nível:** Talentos **Gerais** só a partir do **4º nível**; **Dádivas Épicas** só do **19º**; **Origem · Estilo de Luta · Nível Zero** sempre disponíveis.
- **Habilidades de Classe filtradas:** o seletor mostra **apenas grupos das classes presentes** na ficha e **conforme o nível** (ex.: Caçador de Demônios a partir do 4º, Homem do Oeste do 3º).
- **Subclasse a partir do 3º nível:** o campo de Subclasse (da classe principal **e** de cada classe de multiclasse) só **destrava no 3º nível daquela classe**; classes sem subclasse avisam isso.

---

## 7. Recursos próprios de classe e emblemas

- **Trackers de recursos por classe** (atual / máximo) para as 18 classes — ex.: Mana, Sangue-Frio, Fúrias, Energia/Engenho, Fragmentos de Alma, Foco etc.
- **Emblema/medalhão por classe** (19 desenhos SVG), exibido no painel de Características quando a classe é selecionada. O **Paladino** usa o logo real Pró=RPG.

---

## 8. Bônus automáticos e vantagens/desvantagens

- **Mapa de bônus (47 entradas):** ao escolher certos itens, a ficha aplica sozinha os efeitos numéricos — Iniciativa, CA, Percepção Passiva, PV por nível, testes por atributo, perícia ou salvaguarda.
- **Vantagem/Desvantagem:** quando o efeito é vantagem/desvantagem, perícias afetadas recebem os marcadores **▲ / ▼**; os demais aparecem no painel **"Vantagens & Desvantagens ativas"**, com o **motivo** de cada marca.
- **Penalidade de armadura:** armaduras médias/pesadas indicadas aplicam desvantagem em Furtividade automaticamente.
- **Contador de pontos** de Qualidades × Defeitos (defeitos dão pontos, qualidades gastam).
- **Bônus Personalizados:** 5 linhas livres para somar qualquer modificador onde você quiser.

---

## 9. Salvamento, compartilhamento e impressão

- **Salvamento automático** (localStorage) — cada pessoa guarda a própria ficha no seu navegador.
- **💾 Exportar / Importar JSON** — backup e transferência da ficha em arquivo.
- **🔗 Link da ficha** — gera uma URL com a ficha preenchida embutida (funciona depois de publicada; cai para JSON se for muito grande).
- **🖨️ Salvar como PDF** — via impressão do navegador, com layout próprio para papel.
- **📖 Descrição dos Itens Escolhidos** — painel ao fim da página 3 que resume cada Talento, Habilidade de Classe, Qualidade e Defeito selecionado, além das habilidades automáticas por nível.

---

## 10. Como usar e publicar

- **Uso local:** basta dar duplo-clique no arquivo `Ficha-DnD-AliancaDeHerois.html`.
- **Online (já publicado):** GitHub Pages em https://jsimaoneto.github.io/Ficha-ProRPG/ — site estático, sem servidor; cada visitante mantém os próprios dados.
- **Compartilhar com jogadores:** envie o link do site; para mandar uma ficha específica já preenchida, use o botão "🔗 Link da ficha".

---

## 11. Qualidade / testes automatizados

O projeto tem **testes automatizados** (Node.js + jsdom) que validam as regras a cada alteração:

- `tests/syntax-check.js` — valida a sintaxe do JavaScript da ficha.
- `tests/run-tests.js` — repetibilidade, validade por nível, ocultação de escolhidos, subclasse no 3º nível, soma de multiclasse.
- `tests/check-multiclass-sub.js` — subclasse aparecendo corretamente nas classes de multiclasse.
- `tests/check-talent-gate.js` — talentos só na criação / via Aumento de Habilidade.

Última execução: **todos os testes passando** (25/25 · 13/13 · 20/20).

---

## 12. Como estender (para manutenção futura)

- **Novos bônus:** acrescente uma entrada ao mapa `BONUS`, com a chave igual ao nome do item.
- **Novas descrições:** acrescente ao mapa `DESC`.
- **Novas habilidades escolhíveis:** acrescente ao `HAB_CLASSE` (o rótulo do grupo define classe e nível mínimo); automáticas vão em `HAB_AUTO_CLASSE` / `HAB_AUTO_SUB`.
- **Novos talentos de Nível Zero:** acrescente ao array `TALENTOS_NZ`.
- **Recursos/Emblemas de classe:** mapas `RECURSOS` e `EMBLEMAS`.

> Ao editar, lembre-se de **copiar o HTML principal para `site/index.html`** antes de publicar.

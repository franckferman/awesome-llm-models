# All-in-One (généraux / reasoning / agents)

* **DeepSeek-R1**
  Modèle reasoning **SOTA** : excellent pour planification/logique longue, proche GPT-o3 en perf.
* **GPT-OSS**
  Open-weights by OpenAI, pensé pour reasoning/agents. Bon compromis perf/transparence.
* **Llama 3.1 (8B/70B/405B)**
  Backbone open robuste, très bon tool-use, reste une base standard pour RAG/agents.
* **DeepSeek-V3.1**
  Hybride reasoning (thinking/non-thinking). Modèle **2025**, plus flexible que R1 mais encore jeune.
* **DeepSeek-V3 (MoE 671B, 37B actifs)**
  Rapport coût/perf intéressant grâce à MoE, mais tuning encore inégal selon tâches.
* **DeepSeek-V2.5**
  Polyvalent (général + code), solide mais commence à dater face aux V3.
* **DeepSeek-V2**
  Ancien mais stable, reste fiable pour usages généraux sans edge cases.
* **FireFunction-V2**
  Llama3 optimisé function calling, pensé pour orchestration d’agents (GPT-4o-like).
* **Goliath (2x Llama2-70B merge)**
  Monstre expérimental. Intéressant pour recherche mais peu optimisé prod.
* **OpenChat**
  Très bon chat général, certains benchs le placent > ChatGPT en QA.
* **Llama 4 (16x17B / 128x17B)**
  Multimodal Meta, génération texte + vision. Grosse capacité mais lourd à servir.
* **Gemma 3 (Google)**
  Bon compromis vitesse/qualité, vision incluse, solide choix prod en 2025.
* **Gemma v1/v2**
  Versions précédentes (2B-27B). Toujours viables pour edge ou usage frugal.
* **Qwen 3**
  Dense+MoE, multilingue costaud, très propre en tool-use.  
* **Llama 3.2 (1B/3B)**
  Versions mini pour edge/mobile. Perf correcte malgré taille.
* **OpenThinker**
  Distilled de DeepSeek-R1, plus léger, pratique pour reasoning embarqué.

---

# Reasoning spécialisés

* **Magistral (24B)**
  Modèle reasoning compact, pensé pour efficacité. Bon compromis perf/latence, utile pour CoT solide sans passer sur des monstres 70B+.

* **Phi-4-Reasoning (14B)**
  Très compétitif sur logique pure et mathématique. Léger, rapide, souvent benchmarké proche de modèles 10x plus gros en tasks de raisonnement.

* **Cogito (hybride DeepSeek + Qwen + LLaMA)**
  Fusion multi-sources orientée reasoning hybride. Objectif = combiner la rigueur de DeepSeek avec la fluidité multilingue de Qwen. Intéressant pour expérimentation et tâches cross-domaine.

* **QwQ (Qwen, 32B)**
  Spécialisé chaînes de pensée longues (CoT). Plus lourd que Magistral/Phi mais meilleur pour raisonnement narratif ou multi-étapes complexes.

---

# Développement / Code

* **CodeUp (Llama2-based)**
  Ancien mais robuste. Très bon en génération de code généraliste, modèle **simple, stable et peu coûteux**.

* **DeepCoder (14B)**
  Open 14B, niveau proche **GPT-o3-mini** pour dev. Solide sur algorithmes et tâches coding classiques. Bon rapport taille/perf, utile pour labs perso.

* **Devstral (24B)**  
  Spécialisé **coding agents** : fort en function calling, orchestration multi-outils, workflows complexes. Plus intéressant pour intégration que pour du pur codegen.

* **CodeGemma (2B / 7B)**
  Léger et efficace pour **FIM** (fill-in-the-middle), complétion rapide, petits projets. Idéal pour edge/dev embarqué, mais limité sur gros projets.

* **StarCoder2 (3B / 7B / 15B)**
  Multi-langages, réputé **fiabilité et cohérence**. Très bon sur Python, C, JS. Version 15B = sweet spot pour équilibre qualité/latence.

* **CodeLlama / Phind-CodeLlama**
  Basé sur Llama. Code général, avec variantes optimisées pour **completion vs instruct**. Bonne base open, mais moins pointue que Qwen/DeepSeek récents.

* **Qwen3-Coder (30B / 480B)**
  **Le plus performant open pour code & agents** en 2025. Version 30B déjà redoutable, 480B = niveau quasi GPT-4o en orchestration et code complexe.

* **DeepSeek-Coder-V2 (MoE)**
  MoE (mixture-of-experts) → **GPT-4-Turbo level en code**. Excellent en qualité, tool-use, raisonnement sur projets complexes. Plus lourd à servir mais top choix SOTA.

---

# Uncensored / permissifs

* **EverythingLM (Llama2, 16k contexte)**
  Version uncensored de Llama2 avec **long contexte (16k)**. Stable, simple à servir, mais reste limité par les perfs natives de Llama2.

* **WizardLM-Uncensored (13B)**
  Dérivé Llama, tuning permissif. Compact, efficace pour expérimenter prompts "sans filtre". Bon compromis poids/flexibilité.

* **Llama2-Uncensored (George Sung + Jarrad Hope)**
  Un des premiers forks uncensored sérieux. Base Llama2 brute, utile comme **brique de recherche** ou comportement très direct.

* **Wizard-Vicuna-Uncensored (7B / 13B / 30B)**
  Héritage Vicuna, uncensored. Versions légères adaptées à l’edge (7B/13B), la 30B offrant plus de cohérence. Style plus conversationnel que WizardLM pur.

* **Dolphin-Mixtral / Dolphin-Llama3**
  Option très populaire : uncensored **+ bonne qualité codegen**. Plus polyvalent (chat + code), intéressant pour éviter d’empiler plusieurs modèles.

---

# Math / Sciences

* **Mathstral (7B)** ➗  
  Compact et optimisé pour raisonnement scientifique. Modèle **léger mais spécialisé** en mathématiques, bon pour usage local/edge.

* **Opencoder**
  Polyvalent code + math. Pas uniquement dédié au calcul mais pratique pour un modèle **mixte dev + raisonnement quantitatif**.

* **Qwen2-Math (7B / 72B)**
  **SOTA en raisonnement mathématique**.  
  - 7B = très efficace, cost/perf optimal.  
  - 72B = lourd mais imbattable en logique formelle, théorèmes, résolution pas-à-pas.  
  Référence actuelle pour math avancé.

* **Wizard-Math (7B / 13B / 70B)**
  Dérivé Wizard, tuning dédié mathématiques. Bonne base pour **générateur d’explications pas-à-pas**. Plus accessible que Qwen2-Math, mais un cran en dessous en pure performance.

---

# Chat / réduction hallucination

* **Alfred (40B)**
  Conçu pour **réduire les hallucinations** et offrir un style de réponse plus fiable.  
  Bon pour **QA, support, knowledge bases** → là où la stabilité et la cohérence priment sur la créativité.

* **Reflection (70B)**
  Tuning avancé pour **détection et correction d’erreurs** dans ses propres sorties.  
  Plus lourd, mais utile pour **workflows critiques** (validation de code, explications techniques, RAG où pour éviter les dérapages).

---

# Cas spécifiques

* **Command-R7B-Arabic (7B)**
  Modèle compact spécialisé arabe, particulièrement adapté aux **contextes sociaux, culturels et SE**. Léger, pratique pour RAG/agents ciblés Middle East.

* **Aya (Cohere, multilingue 23 langues)**
  Alternative solide aux Llama/Qwen, pensé pour **vraie diversité linguistique** (23 langues couvertes). Bon choix pour modèle **universel mais pas trop lourd**.

* **Yi / Yi-Coder**
  Bilingue chinois-anglais avec en plus de bonnes perfs en **coding**. Pertinent besoin à cheval entre **multilingue asiatique + dev**.

---

# Embeddings / RAG

* **Nomic-Embed-Text**
  Surpasse OpenAI ada-002 / text-embedding-3-small.  
  Points forts : **long contexte**, open, bon pour projets RAG à coût réduit.

* **BGE-M3**
  Multi-lingual + multi-granularité (phrase, passage, document).  
  Référence pour **RAG multilingue** et tasks nécessitant flexibilité de granularité.

* **MXBAI-Embed-Large**
  **SOTA embeddings** open. Très haut niveau de qualité sémantique, mais plus coûteux.  
  Idéal pour **recherche avancée, prod exigeante**.

* **Snowflake-Arctic-Embed2**
  Embeddings **multilingues pro**, orientés entreprise.  
  Bon choix pour environnements corporate, notamment si besoin de couverture linguistique large avec robustesse.

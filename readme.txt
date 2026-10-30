# FutSal - AP 🏆

**FutSal - AP** é uma aplicação web avançada desenvolvida para treinadores e analistas de futsal criarem, gravarem, editarem e gerirem jogadas táticas interativas, com sincronização em tempo real com uma base de dados na cloud.

---

## 🚀 Principais Funcionalidades

* **Simulador de Campo Interativo:** Quadra de futsal dimensionada com arrastamento (*drag & drop*) fluido de jogadores (Equipa Principal e Equipa Oponente) e da bola.
* **Gravação e Reprodução Temporal:** Registo quadro a quadro (*frames*) dos movimentos táticos, permitindo reprodução dinâmica e navegação por linha temporal (*timeline slider*).
* **Gestão Hierárquica de Tipos e Subtipos:** Categorização avançada de jogadas (Ataque, Defesa, Transições, Esquemas Táticos) com formações específicas (`1*3*1`, `Individual`, `Cantos`, etc.) e suporte para adição de novas categorias personalizadas.
* **Modo de Desenho de Setas Táticas:** Ferramenta interativa para desenhar setas de passe/movimento diretamente no campo, associadas ao frame exato da linha temporal.
* **Painel de Observações e Notas Táticas:** Inserção de apontamentos e notas textuais que são renderizadas dinamicamente tanto na interface como na exportação.
* **Exportação de Vídeo:** Capacidade de exportar a simulação gravada diretamente para formato de vídeo (`.mp4` / `.webm`) através da API `MediaRecorder`.
* **Persistência com Supabase:** Operações CRUD completas (Criar, Ler, Atualizar e Apagar) ligadas a uma base de dados PostgreSQL na cloud.
* **Personalização de Equipas:** Edição livre de rótulos, números e posições dos atletas em campo.

---

## 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5 Canvas, JavaScript (ES6+), Tailwind CSS (via CDN)
* **Backend / Base de Dados:** Supabase (PostgreSQL)
* **Multimédia:** `MediaRecorder` / `captureStream` para exportação de vídeo em tempo real.

---

## 📂 Estrutura do Projeto

O projeto está concentrado num único ficheiro modular (*Single-Page Application*):
* `index.html` — Contém toda a estrutura UI em Tailwind CSS, a lógica de renderização do `Canvas`, a máquina de estados da simulação e os conectores assíncronos do Supabase.

---

## ⚙️ Configuração e Instalação

1. Clona o repositório ou descarrega o ficheiro `index.html`.
2. Certifica-te de que tens as credenciais do **Supabase** configuradas nas constantes globais do script:
   ```javascript
   const SUPABASE_URL = 'SUA_SUPABASE_URL';
   const SUPABASE_ANON_KEY = 'SUA_SUPABASE_ANON_KEY';
<style>
:root {
  --primary: #00d9ff;
  --accent: #ff006e;
  --dark: #0a0e27;
  --light: #f0f4ff;
  --success: #00ff88;
  --warning: #ffb800;
}

.header-hero {
  background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0d1b2a 100%);
  border-bottom: 3px solid #00d9ff;
  padding: 3rem 0;
  margin: -1rem -1rem 2rem -1rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.header-hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: radial-gradient(circle at 20% 50%, rgba(0, 217, 255, 0.1) 0%, transparent 50%),
              radial-gradient(circle at 80% 80%, rgba(255, 0, 110, 0.05) 0%, transparent 50%);
  pointer-events: none;
}

.header-hero h1 {
  font-size: 3em;
  font-weight: 900;
  color: #00d9ff;
  margin: 0;
  text-shadow: 0 0 30px rgba(0, 217, 255, 0.3);
  animation: glow 3s ease-in-out infinite;
  position: relative;
  z-index: 1;
}

@keyframes glow {
  0%, 100% { text-shadow: 0 0 20px rgba(0, 217, 255, 0.3), 0 0 40px rgba(0, 217, 255, 0.1); }
  50% { text-shadow: 0 0 30px rgba(0, 217, 255, 0.5), 0 0 60px rgba(0, 217, 255, 0.2); }
}

.tagline {
  color: #ff006e;
  font-size: 1.3em;
  font-weight: 600;
  margin: 0.5rem 0;
  font-style: italic;
  position: relative;
  z-index: 1;
}

.quote-block {
  background: rgba(0, 217, 255, 0.05);
  border-left: 4px solid #00d9ff;
  padding: 1.5rem;
  margin: 2rem 0;
  border-radius: 0 8px 8px 0;
  font-style: italic;
  color: #00d9ff;
  font-size: 1.1em;
  line-height: 1.6;
}

.project-card {
  background: linear-gradient(135deg, rgba(26, 31, 58, 0.8) 0%, rgba(13, 27, 42, 0.9) 100%);
  border: 2px solid #00d9ff;
  border-radius: 12px;
  padding: 1.8rem;
  margin: 1.5rem 0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 217, 255, 0.1), transparent);
  transition: left 0.5s ease;
}

.project-card:hover {
  border-color: #ff006e;
  box-shadow: 0 0 20px rgba(0, 217, 255, 0.3), inset 0 0 20px rgba(0, 217, 255, 0.05);
  transform: translateY(-3px);
}

.project-card:hover::before {
  left: 100%;
}

.project-title {
  font-size: 1.4em;
  font-weight: 700;
  color: #00d9ff;
  margin: 0 0 0.5rem 0;
  text-decoration: none;
}

.project-desc {
  color: #b0b9d4;
  line-height: 1.6;
  margin: 0.5rem 0 1rem 0;
}

.tech-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-top: 1rem;
}

.tag {
  background: rgba(0, 217, 255, 0.1);
  color: #00d9ff;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85em;
  font-weight: 600;
  border: 1px solid rgba(0, 217, 255, 0.3);
  transition: all 0.2s ease;
}

.tag:hover {
  background: rgba(0, 217, 255, 0.2);
  border-color: #00d9ff;
}

.accent-tag {
  background: rgba(255, 0, 110, 0.1);
  color: #ff006e;
  border-color: rgba(255, 0, 110, 0.3);
}

.accent-tag:hover {
  background: rgba(255, 0, 110, 0.2);
  border-color: #ff006e;
}

.section-header {
  font-size: 1.8em;
  font-weight: 800;
  color: #00d9ff;
  margin: 2.5rem 0 1.5rem 0;
  padding-bottom: 0.8rem;
  border-bottom: 2px solid rgba(0, 217, 255, 0.3);
  position: relative;
}

.section-header::before {
  content: '';
  display: inline-block;
  width: 8px;
  height: 8px;
  background: #ff006e;
  border-radius: 50%;
  margin-right: 0.8rem;
  vertical-align: middle;
}

.tech-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  margin: 1.5rem 0;
}

.tech-category {
  background: rgba(0, 217, 255, 0.05);
  border: 1px solid rgba(0, 217, 255, 0.2);
  border-radius: 8px;
  padding: 1.2rem;
  transition: all 0.3s ease;
}

.tech-category:hover {
  background: rgba(0, 217, 255, 0.1);
  border-color: #00d9ff;
  box-shadow: 0 0 15px rgba(0, 217, 255, 0.1);
}

.tech-category-title {
  font-weight: 700;
  color: #ff006e;
  margin: 0 0 0.8rem 0;
  font-size: 0.95em;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.tech-category-content {
  color: #b0b9d4;
  font-size: 0.95em;
  line-height: 1.6;
}

.philosophy-list {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0;
}

.philosophy-list li {
  padding: 0.8rem 0;
  color: #b0b9d4;
  border-bottom: 1px solid rgba(0, 217, 255, 0.1);
  display: flex;
  align-items: center;
  transition: all 0.2s ease;
}

.philosophy-list li:hover {
  color: #00d9ff;
  padding-left: 0.5rem;
}

.philosophy-list li::before {
  content: '→';
  color: #ff006e;
  margin-right: 0.8rem;
  font-weight: bold;
}

.learning-highlight {
  background: linear-gradient(135deg, rgba(0, 217, 255, 0.1) 0%, rgba(255, 0, 110, 0.05) 100%);
  border: 2px solid #00d9ff;
  border-radius: 8px;
  padding: 1.5rem;
  margin: 2rem 0;
  color: #b0b9d4;
  line-height: 1.8;
  position: relative;
}

.learning-highlight::before {
  content: '🧪';
  font-size: 2em;
  position: absolute;
  top: 1rem;
  right: 1rem;
  opacity: 0.3;
}

.stats-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1rem;
  margin: 1.5rem 0;
}

.stat {
  background: rgba(0, 217, 255, 0.05);
  border: 1px solid rgba(0, 217, 255, 0.2);
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
  transition: all 0.3s ease;
}

.stat:hover {
  background: rgba(0, 217, 255, 0.1);
  border-color: #00d9ff;
  transform: scale(1.05);
}

.stat-number {
  font-size: 1.8em;
  font-weight: 900;
  color: #00d9ff;
}

.stat-label {
  font-size: 0.85em;
  color: #7a8fb4;
  margin-top: 0.3rem;
}

.cta-section {
  background: linear-gradient(135deg, rgba(0, 217, 255, 0.1) 0%, rgba(255, 0, 110, 0.05) 100%);
  border: 2px solid #ff006e;
  border-radius: 12px;
  padding: 2rem;
  margin: 2.5rem 0;
  text-align: center;
}

.cta-text {
  color: #b0b9d4;
  font-size: 1.1em;
  line-height: 1.8;
  margin: 1rem 0;
}

.footer-text {
  text-align: center;
  color: #7a8fb4;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(0, 217, 255, 0.2);
  font-style: italic;
}

body {
  background: #0a0e27;
  color: #b0b9d4;
}

a {
  color: #00d9ff;
  text-decoration: none;
  transition: color 0.2s ease;
}

a:hover {
  color: #ff006e;
}
</style>

<div class="header-hero">
  <h1>🚀 Matheus Buniotto</h1>
  <p class="tagline">Builder | Learning by Doing | Always Experimenting</p>
</div>

<div class="quote-block">
"The best way to understand something is to build it. The best way to build something is to just start."
</div>

## 🎯 What I Do

I build **AI-powered systems, integrations, and tools**—usually trying something new in the process. Go, Python, TypeScript. Agents, APIs, data pipelines. If it needs to be built, I'm interested.

Right now obsessed with:
- 🤖 **AI Agents** — Building intelligent systems that actually do useful things
- 🔗 **Integrations** — Connecting disparate systems with elegant APIs
- 📊 **Data & Analysis** — Finding insights in the noise
- 🛠️ **Developer Tools** — Making other builders' lives easier

## 🔥 Flagship Projects

<div class="project-card">
  <a href="https://github.com/matheusbuniotto/go-google-mcp" class="project-title">go-google-mcp</a>
  <p class="project-desc">Model Context Protocol (MCP) server for Google Workspace. Secure CRUD operations for Drive, Gmail, Calendar, Sheets, Docs, Tasks, and People via AI agents. Built in Go because speed matters when your agents are calling your APIs.</p>
  <div class="tech-tags">
    <span class="tag">golang</span>
    <span class="tag accent-tag">mcp</span>
    <span class="tag">google-workspace</span>
    <span class="tag accent-tag">ai-agent</span>
    <span class="tag">integration</span>
    <span class="tag">llm</span>
  </div>
</div>

<div class="project-card">
  <a href="https://github.com/matheusbuniotto/goAgent" class="project-title">goAgent</a>
  <p class="project-desc">Bare-bone AI Agent Framework in Go. A lean, focused implementation showing how to build agents with tool-use capabilities. No bloat. Just the essential patterns you need to understand agent architecture.</p>
  <div class="tech-tags">
    <span class="tag">golang</span>
    <span class="tag accent-tag">ai-agent</span>
    <span class="tag">agent-framework</span>
    <span class="tag">tool-use</span>
    <span class="tag">llm</span>
  </div>
</div>

<div class="project-card">
  <a href="https://github.com/matheusbuniotto/openwebui-tools" class="project-title">openwebui-tools</a>
  <p class="project-desc">WebUI Tool Integration Framework. Extending OpenWebUI with custom integrations and tools. Making AI interfaces more powerful and connected to your systems.</p>
  <div class="tech-tags">
    <span class="tag">python</span>
    <span class="tag">webui</span>
    <span class="tag accent-tag">tools</span>
    <span class="tag">integration</span>
    <span class="tag">plugin</span>
  </div>
</div>

<div class="project-card">
  <a href="https://github.com/matheusbuniotto/datathon-mlops-rh-ia" class="project-title">datathon-mlops-rh-ia</a>
  <p class="project-desc">MLOps Datathon: HR & AI. Real-world datathon project combining ML operations with human resources analytics. Practical end-to-end ML pipeline in a competitive setting.</p>
  <div class="tech-tags">
    <span class="tag">python</span>
    <span class="tag accent-tag">mlops</span>
    <span class="tag">machine-learning</span>
    <span class="tag">datathon</span>
    <span class="tag">data-science</span>
  </div>
</div>

## 🛠️ Tech Stack

<div class="tech-grid">
  <div class="tech-category">
    <div class="tech-category-title">Languages</div>
    <div class="tech-category-content">Go • Python • TypeScript • Shell • HCL</div>
  </div>
  <div class="tech-category">
    <div class="tech-category-title">AI/ML</div>
    <div class="tech-category-content">LangGraph • Agents • RAG • LSTM • Vector DBs</div>
  </div>
  <div class="tech-category">
    <div class="tech-category-title">DevOps</div>
    <div class="tech-category-content">Terraform • LocalStack • AWS • Docker</div>
  </div>
  <div class="tech-category">
    <div class="tech-category-title">Data</div>
    <div class="tech-category-content">Pandas • Jupyter • dbt • Analytics Eng</div>
  </div>
  <div class="tech-category">
    <div class="tech-category-title">APIs</div>
    <div class="tech-category-content">REST • GraphQL • MCP • gRPC</div>
  </div>
  <div class="tech-category">
    <div class="tech-category-title">Web</div>
    <div class="tech-category-content">React • FastAPI • Node.js</div>
  </div>
</div>

## 🧠 How I Work

<ul class="philosophy-list">
  <li><strong>See a problem</strong> → Wonder how to solve it</li>
  <li><strong>Build a prototype</strong> → Get hands dirty immediately</li>
  <li><strong>Break it</strong> → Learn from the failures</li>
  <li><strong>Iterate</strong> → Ship something useful</li>
  <li><strong>Repeat</strong> → Always trying something new</li>
</ul>

I'm not a "plan everything then execute" person. I'm a **"start with a clear goal, adapt as you learn"** builder.

## 🎨 Fun Facts

- 🐹 Obsessed with building **CLI tools**—terminals are my canvas
- 📚 Self-directed learner—each project is a learning lab
- 🔄 Believe in **continuous experimentation**
- 🌍 Working across **Go, Python, TypeScript** ecosystems
- ⚡ Speed and clarity matter—in code and thinking
- 🤝 Love integrating systems that weren't meant to talk to each other

## 🧪 Learning & Exploration

<div class="learning-highlight">
A lot of my projects are just for <strong>learning and fun</strong>. I believe in shipping experimental work, diving into new tools, and seeing what sticks. Some repos are prototypes, some are learning labs, some turn into production systems. That's the builder way—you never know what'll spark the next big thing until you try it.
</div>

## 📊 GitHub Stats

<div class="stats-container">
  <div class="stat">
    <div class="stat-number">14</div>
    <div class="stat-label">Active Projects</div>
  </div>
  <div class="stat">
    <div class="stat-number">3</div>
    <div class="stat-label">Core Languages</div>
  </div>
  <div class="stat">
    <div class="stat-number">∞</div>
    <div class="stat-label">Curiosity Level</div>
  </div>
  <div class="stat">
    <div class="stat-number">Today</div>
    <div class="stat-label">Latest Build</div>
  </div>
</div>

## 🌐 What's Next?

<div class="cta-section">
  <p class="cta-text">Curious about what I'm building? Check out the projects above or reach out. I'm always down to discuss architecture, debug weird problems, collaborate on interesting projects, or just talk about building, shipping, and iterating.</p>
</div>

<div class="footer-text">
Built with curiosity and shipped with enthusiasm ✨
</div>

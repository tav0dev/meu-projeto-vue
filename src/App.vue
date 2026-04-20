<template>
  <div class="app">
    <!-- NAVBAR -->
    <nav class="navbar" :class="{ scrolled: isScrolled }">
      <div class="container navbar-inner">
        <a href="#inicio" class="navbar-brand">
          <span class="brand-icon">★</span>
          <div class="brand-text">
            <span class="brand-name">RUBEM GONZALEZ</span>
            <span class="brand-subtitle">Deputado Estadual</span>
          </div>
        </a>
        <button class="mobile-toggle" @click="mobileOpen = !mobileOpen" :class="{ active: mobileOpen }">
          <span></span><span></span><span></span>
        </button>
        <ul class="nav-links" :class="{ open: mobileOpen }">
          <li><a href="#inicio" @click="mobileOpen = false">Início</a></li>
          <li><a href="#sobre" @click="mobileOpen = false">Sobre</a></li>
          <li><a href="#bandeiras" @click="mobileOpen = false">Bandeiras</a></li>
          <li><a href="#conquistas" @click="mobileOpen = false">Conquistas</a></li>
          <li><a href="#galeria" @click="mobileOpen = false">Galeria</a></li>
          <li><a href="#contato" @click="mobileOpen = false" class="nav-cta">Fale Comigo</a></li>
        </ul>
      </div>
    </nav>

    <!-- HERO SECTION -->
    <section id="inicio" class="hero">
      <div class="hero-bg">
        <img src="/hero.jpg" alt="Brasil" class="hero-bg-img" />
        <div class="hero-overlay"></div>
      </div>
      <div class="hero-particles">
        <div v-for="n in 20" :key="n" class="particle" :style="particleStyle(n)"></div>
      </div>
      <div class="container hero-content">
        <div class="hero-text">
          <div class="hero-badge animate-hero">
            <span class="badge-star">★</span> Deputado Estadual
          </div>
          <h1 class="hero-title animate-hero delay-1">
            <span class="hero-name">RUBEM</span>
            <span class="hero-surname">GONZALEZ</span>
          </h1>
          <p class="hero-slogan animate-hero delay-2">
            O melhor deputado estadual do Brasil.<br/>
            <strong>Nacionalista, patriota e comprometido com o povo.</strong>
          </p>
          <div class="hero-actions animate-hero delay-3">
            <a href="#bandeiras" class="btn btn-primary">
              <span>Conheça Minhas Bandeiras</span>
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M7 17l9.2-9.2M17 17V7H7"/>
              </svg>
            </a>
            <a href="#contato" class="btn btn-outline">Fale Comigo</a>
          </div>
          <div class="hero-stats animate-hero delay-4">
            <div class="stat-item">
              <span class="stat-number" ref="stat1">{{ animatedStats.projetos }}</span>
              <span class="stat-label">Projetos de Lei</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat-item">
              <span class="stat-number">{{ animatedStats.familias }}k+</span>
              <span class="stat-label">Famílias Beneficiadas</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat-item">
              <span class="stat-number">{{ animatedStats.presenca }}%</span>
              <span class="stat-label">De Presença</span>
            </div>
          </div>
        </div>
        <div class="hero-image animate-hero delay-2">
          <div class="hero-image-frame">
            <img src="/images.jpg" alt="Deputado Rubem Gonzalez" />
            <div class="hero-image-glow"></div>
          </div>
          <div class="hero-image-badge">
            <span class="badge-number">#1</span>
            <span class="badge-text">Melhor Deputado</span>
          </div>
        </div>
      </div>
      <div class="hero-scroll-indicator">
        <span>Role para baixo</span>
        <div class="scroll-arrow">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 5v14M5 12l7 7 7-7"/>
          </svg>
        </div>
      </div>
    </section>

    <!-- FAIXA VERDE E AMARELA -->
    <div class="brazil-stripe">
      <div class="stripe-content">
        <span v-for="n in 8" :key="n">★ ORDEM E PROGRESSO ★ BRASIL ACIMA DE TUDO</span>
      </div>
    </div>

    <!-- SOBRE -->
    <section id="sobre" class="sobre">
      <div class="container">
        <div class="sobre-grid">
          <div class="sobre-image animate-on-scroll">
            <div class="sobre-image-wrapper">
              <img src="/FSiMmkxJtKv9AWF0.jpg" alt="Rubem Gonzalez em entrevista" />
              <div class="sobre-image-accent"></div>
            </div>
            <div class="experience-badge">
              <span class="exp-number">15+</span>
              <span class="exp-text">Anos de<br/>Política</span>
            </div>
          </div>
          <div class="sobre-content animate-on-scroll">
            <span class="section-tag">Conheça o Deputado</span>
            <h2 class="section-title">Um Líder Que Nasceu<br/><span class="highlight">Para Servir o Povo</span></h2>
            <p class="sobre-text">
              Rubem Gonzalez é mais do que um político — é um <strong>patriota dedicado</strong> 
              que acordou cedo todos os dias da sua vida para lutar pelo povo brasileiro. 
              Nascido e criado no interior do Brasil, conhece de perto as dificuldades 
              e necessidades da população.
            </p>
            <p class="sobre-text">
              Como <strong>deputado estadual nacionalista</strong>, Rubem defende uma política de 
              valorização do cidadão brasileiro, priorizando a segurança pública, a educação 
              de qualidade e o desenvolvimento econômico sustentável. É reconhecido como 
              <strong>o melhor deputado estadual</strong> do país por sua atuação incansável 
              e resultados concretos.
            </p>
            <div class="sobre-values">
              <div class="value-item">
                <div class="value-icon">🇧🇷</div>
                <div>
                  <h4>Nacionalismo</h4>
                  <p>Brasil e seus cidadãos em primeiro lugar, sempre.</p>
                </div>
              </div>
              <div class="value-item">
                <div class="value-icon">⚖️</div>
                <div>
                  <h4>Justiça</h4>
                  <p>Igualdade e transparência em cada decisão.</p>
                </div>
              </div>
              <div class="value-item">
                <div class="value-icon">💪</div>
                <div>
                  <h4>Coragem</h4>
                  <p>Enfrentar o sistema para defender o povo.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- BANDEIRAS -->
    <section id="bandeiras" class="bandeiras">
      <div class="bandeiras-bg"></div>
      <div class="container">
        <div class="section-header animate-on-scroll">
          <span class="section-tag light">Nossas Bandeiras</span>
          <h2 class="section-title light">As Causas que<br/><span class="highlight-gold">Movem Nossa Luta</span></h2>
          <p class="section-desc">Conheça as principais bandeiras que norteiam o mandato do Deputado Rubem Gonzalez.</p>
        </div>
        <div class="bandeiras-grid">
          <div v-for="(bandeira, i) in bandeiras" :key="i" 
               class="bandeira-card animate-on-scroll"
               :style="{ animationDelay: i * 0.1 + 's' }">
            <div class="bandeira-icon">{{ bandeira.icon }}</div>
            <div class="bandeira-number">0{{ i + 1 }}</div>
            <h3>{{ bandeira.titulo }}</h3>
            <p>{{ bandeira.desc }}</p>
            <div class="bandeira-line"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONQUISTAS -->
    <section id="conquistas" class="conquistas">
      <div class="container">
        <div class="section-header animate-on-scroll">
          <span class="section-tag">Resultados Reais</span>
          <h2 class="section-title">Conquistas que<br/><span class="highlight">Falam por Si</span></h2>
        </div>
        <div class="timeline">
          <div v-for="(conquista, i) in conquistas" :key="i" 
               class="timeline-item animate-on-scroll"
               :class="i % 2 === 0 ? 'left' : 'right'">
            <div class="timeline-content">
              <span class="timeline-year">{{ conquista.ano }}</span>
              <h3>{{ conquista.titulo }}</h3>
              <p>{{ conquista.desc }}</p>
            </div>
            <div class="timeline-dot"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- CITAÇÃO -->
    <section class="citacao">
      <div class="citacao-bg"></div>
      <div class="container">
        <div class="citacao-content animate-on-scroll">
          <div class="citacao-aspas">"</div>
          <blockquote>
            Minha missão é simples: servir o povo brasileiro com honra, 
            coragem e verdade. Não estou aqui pelo poder — estou aqui 
            pela nossa pátria.
          </blockquote>
          <div class="citacao-author">
            <div class="citacao-line"></div>
            <div>
              <strong>Rubem Gonzalez</strong>
              <span>Deputado Estadual</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- GALERIA -->
    <section id="galeria" class="galeria">
      <div class="container">
        <div class="section-header animate-on-scroll">
          <span class="section-tag">Em Ação</span>
          <h2 class="section-title">Galeria de<br/><span class="highlight">Atuação</span></h2>
        </div>
        <div class="galeria-grid">
          <div class="galeria-item large animate-on-scroll">
            <img src="/FSiMmkxJtKv9AWF0.jpg" alt="Rubem em entrevista" />
            <div class="galeria-overlay">
              <span>Comício em praça pública</span>
            </div>
          </div>
          <div class="galeria-item animate-on-scroll">
            <img src="/hero.jpg" alt="Rubem Gonzalez - Rubão" />
            <div class="galeria-overlay">
              <span>Nosso estado, nosso orgulho</span>
            </div>
          </div>
          <div class="galeria-item animate-on-scroll">
            <img src="/images.jpg" alt="Retrato do deputado" />
            <div class="galeria-overlay">
              <span>Foto oficial do mandato</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA NEWSLETTER -->
    <section class="newsletter">
      <div class="container">
        <div class="newsletter-card animate-on-scroll">
          <div class="newsletter-content">
            <h2>Junte-se à Nossa Causa</h2>
            <p>Receba atualizações sobre os projetos e ações do mandato do Deputado Rubem Gonzalez.</p>
          </div>
          <form class="newsletter-form" @submit.prevent="submitEmail">
            <div class="input-group">
              <input type="email" v-model="email" placeholder="Seu melhor e-mail" required />
              <button type="submit" class="btn btn-primary">
                <span>Inscrever-se</span>
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M5 12h14M12 5l7 7-7 7"/>
                </svg>
              </button>
            </div>
            <p v-if="emailSent" class="success-msg">✓ Inscrição realizada com sucesso!</p>
          </form>
        </div>
      </div>
    </section>

    <!-- CONTATO -->
    <section id="contato" class="contato">
      <div class="contato-bg"></div>
      <div class="container">
        <div class="contato-grid">
          <div class="contato-info animate-on-scroll">
            <span class="section-tag light">Entre em Contato</span>
            <h2 class="section-title light">Fale Diretamente<br/><span class="highlight-gold">Com o Deputado</span></h2>
            <p class="contato-desc">
              Sua voz importa! Entre em contato com o gabinete do Deputado 
              Rubem Gonzalez e participe ativamente da política do nosso estado.
            </p>
            <div class="contato-items">
              <div class="contato-item">
                <div class="contato-icon">📍</div>
                <div>
                  <h4>Gabinete</h4>
                  <p>Assembleia Legislativa, Sala 301<br/>Brasília - DF</p>
                </div>
              </div>
              <div class="contato-item">
                <div class="contato-icon">📞</div>
                <div>
                  <h4>Telefone</h4>
                  <p>(61) 3215-0000</p>
                </div>
              </div>
              <div class="contato-item">
                <div class="contato-icon">✉️</div>
                <div>
                  <h4>E-mail</h4>
                  <p>contato@rubemgonzalez.com.br</p>
                </div>
              </div>
              <div class="contato-item">
                <div class="contato-icon">🕐</div>
                <div>
                  <h4>Atendimento</h4>
                  <p>Segunda a Sexta, 8h às 18h</p>
                </div>
              </div>
            </div>
            <div class="social-links">
              <a href="#" class="social-link" aria-label="Instagram">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
              </a>
              <a href="#" class="social-link" aria-label="Facebook">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
              </a>
              <a href="#" class="social-link" aria-label="Twitter/X">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
              </a>
              <a href="#" class="social-link" aria-label="YouTube">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M23.498 6.186a3.016 3.016 0 00-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 00.502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 002.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 002.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
              </a>
            </div>
          </div>
          <div class="contato-form-wrapper animate-on-scroll">
            <form class="contato-form" @submit.prevent="submitContact">
              <h3>Envie sua Mensagem</h3>
              <div class="form-group">
                <label for="nome">Nome completo</label>
                <input type="text" id="nome" v-model="form.nome" placeholder="Seu nome" required />
              </div>
              <div class="form-row">
                <div class="form-group">
                  <label for="email-contato">E-mail</label>
                  <input type="email" id="email-contato" v-model="form.email" placeholder="seu@email.com" required />
                </div>
                <div class="form-group">
                  <label for="telefone">Telefone</label>
                  <input type="tel" id="telefone" v-model="form.telefone" placeholder="(00) 00000-0000" />
                </div>
              </div>
              <div class="form-group">
                <label for="assunto">Assunto</label>
                <select id="assunto" v-model="form.assunto">
                  <option value="">Selecione um assunto</option>
                  <option value="denuncia">Denúncia</option>
                  <option value="sugestao">Sugestão</option>
                  <option value="apoio">Apoio ao Mandato</option>
                  <option value="imprensa">Imprensa</option>
                  <option value="outro">Outro</option>
                </select>
              </div>
              <div class="form-group">
                <label for="mensagem">Mensagem</label>
                <textarea id="mensagem" v-model="form.mensagem" rows="4" placeholder="Escreva sua mensagem..." required></textarea>
              </div>
              <button type="submit" class="btn btn-primary full-width">
                <span>Enviar Mensagem</span>
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M22 2L11 13M22 2l-7 20-4-9-9-4 20-7z"/>
                </svg>
              </button>
              <p v-if="contactSent" class="success-msg">✓ Mensagem enviada! Responderemos em breve.</p>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
      <div class="footer-top">
        <div class="container footer-grid">
          <div class="footer-brand">
            <div class="footer-logo">
              <span class="brand-icon">★</span>
              <div>
                <span class="brand-name">RUBEM GONZALEZ</span>
                <span class="brand-subtitle">Deputado Estadual</span>
              </div>
            </div>
            <p>Trabalhando incansavelmente por um Brasil mais forte, justo e soberano. Nacionalismo com responsabilidade.</p>
          </div>
          <div class="footer-links-col">
            <h4>Navegação</h4>
            <ul>
              <li><a href="#inicio">Início</a></li>
              <li><a href="#sobre">Sobre</a></li>
              <li><a href="#bandeiras">Bandeiras</a></li>
              <li><a href="#conquistas">Conquistas</a></li>
              <li><a href="#contato">Contato</a></li>
            </ul>
          </div>
          <div class="footer-links-col">
            <h4>Transparência</h4>
            <ul>
              <li><a href="#">Prestação de Contas</a></li>
              <li><a href="#">Projetos de Lei</a></li>
              <li><a href="#">Agenda Pública</a></li>
              <li><a href="#">Relatórios</a></li>
            </ul>
          </div>
          <div class="footer-links-col">
            <h4>Legal</h4>
            <ul>
              <li><a href="#">Política de Privacidade</a></li>
              <li><a href="#">Termos de Uso</a></li>
              <li><a href="#">LGPD</a></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="container footer-bottom-inner">
          <p>© 2026 Rubem Gonzalez — Todos os direitos reservados.</p>
          <p class="footer-motto">🇧🇷 Pátria Amada Brasil</p>
        </div>
      </div>
    </footer>

    <!-- BACK TO TOP -->
    <button class="back-to-top" :class="{ visible: isScrolled }" @click="scrollToTop" aria-label="Voltar ao topo">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <path d="M12 19V5M5 12l7-7 7 7"/>
      </svg>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref, reactive, onMounted, onUnmounted } from 'vue'

// --- State ---
const isScrolled = ref(false)
const mobileOpen = ref(false)
const email = ref('')
const emailSent = ref(false)
const contactSent = ref(false)

const form = reactive({
  nome: '',
  email: '',
  telefone: '',
  assunto: '',
  mensagem: ''
})

const animatedStats = reactive({
  projetos: 0,
  familias: 0,
  presenca: 0
})

const bandeiras = [
  { icon: '🛡️', titulo: 'Segurança Pública', desc: 'Tolerância zero com a criminalidade. Mais investimento em forças policiais, armamento e inteligência para proteger cada cidadão.' },
  { icon: '📚', titulo: 'Educação Patriótica', desc: 'Escolas que formam cidadãos orgulhosos da sua nação, com ensino de qualidade, valores cívicos e respeito à história do Brasil.' },
  { icon: '🏥', titulo: 'Saúde para Todos', desc: 'Hospitais equipados, postos de saúde funcionando e atendimento digno para todos os brasileiros que precisam.' },
  { icon: '🌾', titulo: 'Agronegócio Forte', desc: 'Apoio total ao produtor rural brasileiro, o verdadeiro herói que alimenta a nação e gera riqueza para o país.' },
  { icon: '👨‍👩‍👧‍👦', titulo: 'Família Brasileira', desc: 'Políticas públicas que fortalecem e protegem a família — a base fundamental da sociedade brasileira.' },
  { icon: '💼', titulo: 'Geração de Emprego', desc: 'Menos burocracia, menos impostos e mais oportunidades para o trabalhador e o empreendedor brasileiro.' },
]

const conquistas = [
  { ano: '2024', titulo: 'Lei de Proteção ao Patrimônio Cultural', desc: 'Aprovação de projeto que garante a preservação dos monumentos históricos e símbolos nacionais em todo o estado.' },
  { ano: '2023', titulo: '50 Escolas Revitalizadas', desc: 'Programa de revitalização que reformou mais de 50 escolas públicas, beneficiando 30 mil alunos.' },
  { ano: '2023', titulo: 'Programa Segurança Total', desc: 'Implementação do programa que reduziu a criminalidade em 35% nas regiões mais vulneráveis.' },
  { ano: '2022', titulo: 'Apoio ao Agro', desc: 'Criação do fundo estadual de apoio aos pequenos produtores rurais, beneficiando mais de 5 mil famílias.' },
]

// --- Particle animation ---
function particleStyle(n: number) {
  const size = Math.random() * 4 + 2
  return {
    width: size + 'px',
    height: size + 'px',
    left: Math.random() * 100 + '%',
    top: Math.random() * 100 + '%',
    animationDelay: Math.random() * 5 + 's',
    animationDuration: (Math.random() * 10 + 10) + 's'
  }
}

// --- Scroll handler ---
function handleScroll() {
  isScrolled.value = window.scrollY > 80

  // Animate elements on scroll
  const elements = document.querySelectorAll('.animate-on-scroll')
  elements.forEach(el => {
    const rect = el.getBoundingClientRect()
    if (rect.top < window.innerHeight - 100) {
      el.classList.add('visible')
    }
  })
}

// --- Stats counter ---
function animateStats() {
  const targets = { projetos: 147, familias: 85, presenca: 98 }
  const duration = 2000
  const steps = 60
  const interval = duration / steps
  let step = 0

  const timer = setInterval(() => {
    step++
    const progress = step / steps
    const eased = 1 - Math.pow(1 - progress, 3)
    animatedStats.projetos = Math.round(targets.projetos * eased)
    animatedStats.familias = Math.round(targets.familias * eased)
    animatedStats.presenca = Math.round(targets.presenca * eased)
    if (step >= steps) clearInterval(timer)
  }, interval)
}

// --- Scroll to top ---
function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}

// --- Form handlers ---
function submitEmail() {
  emailSent.value = true
  email.value = ''
  setTimeout(() => { emailSent.value = false }, 4000)
}

function submitContact() {
  contactSent.value = true
  form.nome = ''
  form.email = ''
  form.telefone = ''
  form.assunto = ''
  form.mensagem = ''
  setTimeout(() => { contactSent.value = false }, 4000)
}

// --- Lifecycle ---
onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  handleScroll()
  setTimeout(animateStats, 500)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
/* =============================================
   NAVBAR
   ============================================= */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 20px 0;
  transition: var(--transition-smooth);
}

.navbar.scrolled {
  background: rgba(0, 10, 30, 0.95);
  backdrop-filter: blur(20px);
  padding: 12px 0;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
}

.navbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.navbar-brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.brand-icon {
  font-size: 28px;
  color: var(--amarelo-brasil);
  filter: drop-shadow(0 0 10px rgba(255, 223, 0, 0.5));
}

.brand-text {
  display: flex;
  flex-direction: column;
}

.brand-name {
  font-family: var(--font-accent);
  font-size: 1.4rem;
  color: var(--branco);
  letter-spacing: 3px;
  line-height: 1;
}

.brand-subtitle {
  font-size: 0.65rem;
  color: var(--amarelo-brasil);
  text-transform: uppercase;
  letter-spacing: 4px;
  font-weight: 500;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 8px;
}

.nav-links a {
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.88rem;
  font-weight: 500;
  padding: 8px 16px;
  border-radius: 8px;
  transition: var(--transition-fast);
}

.nav-links a:hover {
  color: var(--branco);
  background: rgba(255, 255, 255, 0.1);
}

.nav-cta {
  background: linear-gradient(135deg, var(--verde-brasil), var(--verde-escuro)) !important;
  color: var(--branco) !important;
  padding: 10px 24px !important;
  border-radius: 50px !important;
  font-weight: 600 !important;
}

.nav-cta:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 156, 59, 0.4);
  background: linear-gradient(135deg, var(--verde-claro), var(--verde-brasil)) !important;
}

/* Mobile Toggle */
.mobile-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 8px;
  z-index: 1001;
}

.mobile-toggle span {
  width: 25px;
  height: 2px;
  background: var(--branco);
  border-radius: 2px;
  transition: var(--transition-fast);
}

.mobile-toggle.active span:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.mobile-toggle.active span:nth-child(2) {
  opacity: 0;
}

.mobile-toggle.active span:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
}

/* =============================================
   HERO SECTION
   ============================================= */
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.hero-bg-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    135deg,
    rgba(0, 10, 40, 0.92) 0%,
    rgba(0, 39, 118, 0.85) 40%,
    rgba(0, 20, 60, 0.88) 100%
  );
}

/* Particles */
.hero-particles {
  position: absolute;
  inset: 0;
  z-index: 1;
  pointer-events: none;
}

.particle {
  position: absolute;
  background: var(--amarelo-brasil);
  border-radius: 50%;
  opacity: 0.3;
  animation: float linear infinite;
}

/* Hero Content */
.hero-content {
  position: relative;
  z-index: 2;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  padding-top: 100px;
  padding-bottom: 60px;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255, 223, 0, 0.15);
  border: 1px solid rgba(255, 223, 0, 0.3);
  padding: 8px 20px;
  border-radius: 50px;
  color: var(--amarelo-brasil);
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 24px;
}

.badge-star {
  font-size: 1.1rem;
  animation: pulse-glow 2s infinite;
}

.hero-title {
  font-family: var(--font-display);
  line-height: 1;
  margin-bottom: 24px;
}

.hero-name {
  display: block;
  font-size: 4.5rem;
  font-weight: 700;
  color: var(--branco);
  letter-spacing: 2px;
}

.hero-surname {
  display: block;
  font-size: 5.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, var(--amarelo-brasil), var(--amarelo-dourado));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  letter-spacing: 4px;
}

.hero-slogan {
  font-size: 1.15rem;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.8;
  margin-bottom: 32px;
  max-width: 500px;
}

.hero-slogan strong {
  color: var(--branco);
}

/* Buttons */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 14px 32px;
  border-radius: 50px;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition-smooth);
  border: none;
  font-family: var(--font-body);
}

.btn-primary {
  background: linear-gradient(135deg, var(--verde-brasil), var(--verde-escuro));
  color: var(--branco);
  box-shadow: 0 4px 20px rgba(0, 156, 59, 0.3);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 35px rgba(0, 156, 59, 0.5);
}

.btn-outline {
  background: transparent;
  color: var(--branco);
  border: 2px solid rgba(255, 255, 255, 0.3);
}

.btn-outline:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: var(--branco);
  transform: translateY(-3px);
}

.hero-actions {
  display: flex;
  gap: 16px;
  margin-bottom: 48px;
  flex-wrap: wrap;
}

/* Hero Stats */
.hero-stats {
  display: flex;
  align-items: center;
  gap: 32px;
  padding: 24px 32px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 20px;
  backdrop-filter: blur(10px);
}

.stat-item {
  text-align: center;
}

.stat-number {
  display: block;
  font-family: var(--font-accent);
  font-size: 2.2rem;
  color: var(--amarelo-brasil);
  line-height: 1;
}

.stat-label {
  font-size: 0.75rem;
  color: rgba(255, 255, 255, 0.6);
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-top: 4px;
}

.stat-divider {
  width: 1px;
  height: 40px;
  background: rgba(255, 255, 255, 0.15);
}

/* Hero Image */
.hero-image {
  display: flex;
  justify-content: center;
  position: relative;
}

.hero-image-frame {
  position: relative;
  width: 420px;
  height: 500px;
  border-radius: 30px;
  overflow: hidden;
  border: 3px solid rgba(255, 223, 0, 0.3);
}

.hero-image-frame img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-image-glow {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(0, 39, 118, 0.6) 0%, transparent 50%);
}

.hero-image-badge {
  position: absolute;
  bottom: 30px;
  right: -20px;
  background: linear-gradient(135deg, var(--amarelo-brasil), var(--amarelo-dourado));
  padding: 16px 24px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
  animation: float 3s ease-in-out infinite;
}

.badge-number {
  display: block;
  font-family: var(--font-accent);
  font-size: 2rem;
  color: var(--azul-brasil);
  line-height: 1;
}

.badge-text {
  font-size: 0.7rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 2px;
  color: var(--azul-brasil);
}

/* Hero Scroll Indicator */
.hero-scroll-indicator {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.75rem;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.scroll-arrow {
  animation: float 2s ease-in-out infinite;
}

/* Hero Animations */
.animate-hero {
  animation: fadeInUp 0.8s ease forwards;
  opacity: 0;
}

.delay-1 { animation-delay: 0.2s; }
.delay-2 { animation-delay: 0.4s; }
.delay-3 { animation-delay: 0.6s; }
.delay-4 { animation-delay: 0.8s; }

/* =============================================
   BRAZIL STRIPE
   ============================================= */
.brazil-stripe {
  background: linear-gradient(135deg, var(--verde-brasil), var(--verde-escuro));
  padding: 16px 0;
  overflow: hidden;
}

.stripe-content {
  display: flex;
  gap: 40px;
  white-space: nowrap;
  animation: shimmer 20s linear infinite;
  font-family: var(--font-accent);
  font-size: 1.1rem;
  color: var(--amarelo-brasil);
  letter-spacing: 6px;
}

/* =============================================
   SECTION COMMON
   ============================================= */
.section-tag {
  display: inline-block;
  font-size: 0.8rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 4px;
  color: var(--verde-brasil);
  margin-bottom: 16px;
}

.section-tag.light {
  color: var(--amarelo-brasil);
}

.section-title {
  font-family: var(--font-display);
  font-size: 3rem;
  font-weight: 800;
  color: var(--preto);
  line-height: 1.2;
  margin-bottom: 20px;
}

.section-title.light {
  color: var(--branco);
}

.highlight {
  color: var(--verde-brasil);
}

.highlight-gold {
  color: var(--amarelo-brasil);
}

.section-header {
  text-align: center;
  margin-bottom: 64px;
}

.section-desc {
  font-size: 1.05rem;
  color: rgba(255, 255, 255, 0.7);
  max-width: 600px;
  margin: 0 auto;
}

/* =============================================
   SOBRE
   ============================================= */
.sobre {
  padding: 120px 0;
  background: var(--cinza-claro);
}

.sobre-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 80px;
  align-items: center;
}

.sobre-image-wrapper {
  position: relative;
  border-radius: 24px;
  overflow: hidden;
  box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
}

.sobre-image-wrapper img {
  width: 100%;
  height: 450px;
  object-fit: cover;
}

.sobre-image-accent {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 5px;
  background: linear-gradient(90deg, var(--verde-brasil), var(--amarelo-brasil), var(--azul-brasil));
}

.sobre-image {
  position: relative;
}

.experience-badge {
  position: absolute;
  bottom: -20px;
  right: 30px;
  background: linear-gradient(135deg, var(--azul-brasil), var(--azul-profundo));
  padding: 20px 28px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 10px 40px rgba(0, 39, 118, 0.4);
  color: var(--branco);
}

.exp-number {
  display: block;
  font-family: var(--font-accent);
  font-size: 2.8rem;
  line-height: 1;
  color: var(--amarelo-brasil);
}

.exp-text {
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  opacity: 0.9;
}

.sobre-text {
  font-size: 1.05rem;
  color: var(--cinza-escuro);
  margin-bottom: 20px;
  line-height: 1.8;
}

.sobre-values {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-top: 32px;
}

.value-item {
  display: flex;
  align-items: flex-start;
  gap: 16px;
  padding: 20px;
  background: var(--branco);
  border-radius: 16px;
  transition: var(--transition-smooth);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
}

.value-item:hover {
  transform: translateX(8px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
}

.value-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.value-item h4 {
  font-family: var(--font-display);
  font-size: 1.1rem;
  color: var(--azul-brasil);
  margin-bottom: 4px;
}

.value-item p {
  font-size: 0.9rem;
  color: var(--cinza-medio);
  line-height: 1.5;
}

/* =============================================
   BANDEIRAS
   ============================================= */
.bandeiras {
  position: relative;
  padding: 120px 0;
  overflow: hidden;
}

.bandeiras-bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--azul-profundo) 0%, var(--azul-brasil) 50%, #001040 100%);
}

.bandeiras .container {
  position: relative;
  z-index: 1;
}

.bandeiras-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.bandeira-card {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 24px;
  padding: 40px 32px;
  transition: var(--transition-smooth);
  position: relative;
  overflow: hidden;
}

.bandeira-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--verde-brasil), var(--amarelo-brasil));
  transform: scaleX(0);
  transition: var(--transition-smooth);
}

.bandeira-card:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-8px);
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
}

.bandeira-card:hover::before {
  transform: scaleX(1);
}

.bandeira-icon {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.bandeira-number {
  position: absolute;
  top: 20px;
  right: 24px;
  font-family: var(--font-accent);
  font-size: 1.5rem;
  color: rgba(255, 223, 0, 0.15);
}

.bandeira-card h3 {
  font-family: var(--font-display);
  font-size: 1.3rem;
  color: var(--branco);
  margin-bottom: 12px;
}

.bandeira-card p {
  font-size: 0.92rem;
  color: rgba(255, 255, 255, 0.6);
  line-height: 1.7;
}

.bandeira-line {
  width: 40px;
  height: 3px;
  background: var(--verde-brasil);
  border-radius: 2px;
  margin-top: 20px;
  transition: var(--transition-smooth);
}

.bandeira-card:hover .bandeira-line {
  width: 80px;
  background: linear-gradient(90deg, var(--verde-brasil), var(--amarelo-brasil));
}

/* =============================================
   CONQUISTAS / TIMELINE
   ============================================= */
.conquistas {
  padding: 120px 0;
  background: var(--branco);
}

.timeline {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
}

.timeline::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  width: 3px;
  height: 100%;
  background: linear-gradient(to bottom, var(--verde-brasil), var(--amarelo-brasil), var(--azul-brasil));
  transform: translateX(-50%);
  border-radius: 2px;
}

.timeline-item {
  display: flex;
  align-items: center;
  margin-bottom: 48px;
  position: relative;
}

.timeline-item.left {
  justify-content: flex-start;
  padding-right: calc(50% + 40px);
}

.timeline-item.right {
  justify-content: flex-end;
  padding-left: calc(50% + 40px);
}

.timeline-content {
  background: var(--cinza-claro);
  padding: 28px 32px;
  border-radius: 20px;
  transition: var(--transition-smooth);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.timeline-content:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 35px rgba(0, 0, 0, 0.1);
}

.timeline-year {
  display: inline-block;
  font-family: var(--font-accent);
  font-size: 1.3rem;
  color: var(--verde-brasil);
  letter-spacing: 2px;
  margin-bottom: 8px;
}

.timeline-content h3 {
  font-family: var(--font-display);
  font-size: 1.2rem;
  color: var(--azul-brasil);
  margin-bottom: 8px;
}

.timeline-content p {
  font-size: 0.92rem;
  color: var(--cinza-medio);
  line-height: 1.6;
}

.timeline-dot {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 18px;
  height: 18px;
  background: var(--verde-brasil);
  border: 4px solid var(--branco);
  border-radius: 50%;
  box-shadow: 0 0 0 4px rgba(0, 156, 59, 0.2);
  z-index: 1;
}

/* =============================================
   CITAÇÃO
   ============================================= */
.citacao {
  position: relative;
  padding: 100px 0;
  overflow: hidden;
}

.citacao-bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--verde-escuro), var(--verde-brasil));
}

.citacao-content {
  position: relative;
  z-index: 1;
  text-align: center;
  max-width: 800px;
  margin: 0 auto;
}

.citacao-aspas {
  font-family: var(--font-display);
  font-size: 8rem;
  color: rgba(255, 223, 0, 0.3);
  line-height: 0.5;
  margin-bottom: 20px;
}

blockquote {
  font-family: var(--font-display);
  font-size: 1.8rem;
  font-weight: 600;
  color: var(--branco);
  line-height: 1.6;
  font-style: italic;
  margin-bottom: 32px;
}

.citacao-author {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}

.citacao-line {
  width: 50px;
  height: 2px;
  background: var(--amarelo-brasil);
}

.citacao-author strong {
  display: block;
  color: var(--amarelo-brasil);
  font-size: 1.05rem;
}

.citacao-author span {
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.85rem;
}

/* =============================================
   GALERIA
   ============================================= */
.galeria {
  padding: 120px 0;
  background: var(--cinza-claro);
}

.galeria-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  grid-template-rows: auto auto;
  gap: 20px;
}

.galeria-item {
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  cursor: pointer;
}

.galeria-item.large {
  grid-row: span 2;
}

.galeria-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: var(--transition-smooth);
  min-height: 250px;
}

.galeria-item:hover img {
  transform: scale(1.05);
}

.galeria-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(0, 10, 40, 0.8) 0%, transparent 60%);
  display: flex;
  align-items: flex-end;
  padding: 24px;
  opacity: 0;
  transition: var(--transition-smooth);
}

.galeria-item:hover .galeria-overlay {
  opacity: 1;
}

.galeria-overlay span {
  color: var(--branco);
  font-weight: 600;
  font-size: 1rem;
}

/* =============================================
   NEWSLETTER
   ============================================= */
.newsletter {
  padding: 80px 0;
  background: var(--branco);
}

.newsletter-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  padding: 60px;
  background: linear-gradient(135deg, var(--azul-profundo), var(--azul-brasil));
  border-radius: 30px;
  box-shadow: 0 20px 60px rgba(0, 39, 118, 0.3);
}

.newsletter-content h2 {
  font-family: var(--font-display);
  font-size: 2rem;
  color: var(--branco);
  margin-bottom: 8px;
}

.newsletter-content p {
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.95rem;
  max-width: 400px;
}

.newsletter-form {
  flex-shrink: 0;
}

.input-group {
  display: flex;
  gap: 12px;
}

.input-group input {
  padding: 14px 24px;
  border: 2px solid rgba(255, 255, 255, 0.2);
  border-radius: 50px;
  background: rgba(255, 255, 255, 0.1);
  color: var(--branco);
  font-size: 0.95rem;
  font-family: var(--font-body);
  width: 280px;
  transition: var(--transition-fast);
}

.input-group input::placeholder {
  color: rgba(255, 255, 255, 0.5);
}

.input-group input:focus {
  outline: none;
  border-color: var(--amarelo-brasil);
  background: rgba(255, 255, 255, 0.15);
}

.success-msg {
  color: var(--verde-claro);
  font-size: 0.85rem;
  margin-top: 12px;
  font-weight: 500;
}

/* =============================================
   CONTATO
   ============================================= */
.contato {
  position: relative;
  padding: 120px 0;
  overflow: hidden;
}

.contato-bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--azul-profundo), #000a1e);
}

.contato .container {
  position: relative;
  z-index: 1;
}

.contato-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: flex-start;
}

.contato-desc {
  color: rgba(255, 255, 255, 0.7);
  font-size: 1.05rem;
  margin-bottom: 40px;
  line-height: 1.8;
}

.contato-items {
  display: flex;
  flex-direction: column;
  gap: 24px;
  margin-bottom: 40px;
}

.contato-item {
  display: flex;
  align-items: flex-start;
  gap: 16px;
}

.contato-icon {
  font-size: 1.5rem;
  flex-shrink: 0;
  width: 50px;
  height: 50px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.contato-item h4 {
  color: var(--branco);
  font-size: 1rem;
  margin-bottom: 4px;
}

.contato-item p {
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.9rem;
  line-height: 1.5;
}

.social-links {
  display: flex;
  gap: 12px;
}

.social-link {
  width: 48px;
  height: 48px;
  border-radius: 14px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--branco);
  transition: var(--transition-smooth);
}

.social-link:hover {
  background: var(--verde-brasil);
  border-color: var(--verde-brasil);
  transform: translateY(-4px);
}

/* Contato Form */
.contato-form-wrapper {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 28px;
  padding: 44px;
  backdrop-filter: blur(20px);
}

.contato-form h3 {
  font-family: var(--font-display);
  font-size: 1.5rem;
  color: var(--branco);
  margin-bottom: 28px;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.85rem;
  font-weight: 500;
  margin-bottom: 8px;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 14px 20px;
  background: rgba(255, 255, 255, 0.08);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 14px;
  color: var(--branco);
  font-size: 0.95rem;
  font-family: var(--font-body);
  transition: var(--transition-fast);
}

.form-group select {
  appearance: none;
  cursor: pointer;
}

.form-group select option {
  background: var(--azul-profundo);
  color: var(--branco);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: rgba(255, 255, 255, 0.4);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--verde-brasil);
  background: rgba(255, 255, 255, 0.12);
}

.form-group textarea {
  resize: vertical;
  min-height: 100px;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.full-width {
  width: 100%;
  justify-content: center;
}

/* =============================================
   FOOTER
   ============================================= */
.footer {
  background: var(--preto);
}

.footer-top {
  padding: 80px 0 60px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr 1fr;
  gap: 48px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 20px;
}

.footer-logo .brand-icon {
  font-size: 24px;
}

.footer-logo .brand-name {
  font-family: var(--font-accent);
  font-size: 1.2rem;
  color: var(--branco);
  letter-spacing: 3px;
  display: block;
}

.footer-logo .brand-subtitle {
  font-size: 0.6rem;
}

.footer-brand p {
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.9rem;
  line-height: 1.7;
}

.footer-links-col h4 {
  color: var(--branco);
  font-size: 0.95rem;
  font-weight: 600;
  margin-bottom: 20px;
}

.footer-links-col li {
  margin-bottom: 12px;
}

.footer-links-col a {
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.88rem;
  transition: var(--transition-fast);
}

.footer-links-col a:hover {
  color: var(--verde-claro);
  padding-left: 4px;
}

.footer-bottom {
  padding: 24px 0;
}

.footer-bottom-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-bottom p {
  color: rgba(255, 255, 255, 0.4);
  font-size: 0.85rem;
}

.footer-motto {
  font-weight: 600;
  color: var(--amarelo-brasil) !important;
}

/* =============================================
   BACK TO TOP
   ============================================= */
.back-to-top {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 50px;
  height: 50px;
  border-radius: 16px;
  background: linear-gradient(135deg, var(--verde-brasil), var(--verde-escuro));
  color: var(--branco);
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transform: translateY(20px);
  transition: var(--transition-smooth);
  box-shadow: 0 8px 25px rgba(0, 156, 59, 0.3);
  z-index: 999;
}

.back-to-top.visible {
  opacity: 1;
  transform: translateY(0);
}

.back-to-top:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 35px rgba(0, 156, 59, 0.5);
}

/* =============================================
   RESPONSIVE
   ============================================= */
@media (max-width: 1024px) {
  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .hero-text {
    order: 2;
  }

  .hero-image {
    order: 1;
  }

  .hero-slogan {
    margin: 0 auto 32px;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-stats {
    justify-content: center;
  }

  .hero-name { font-size: 3.5rem; }
  .hero-surname { font-size: 4rem; }

  .sobre-grid {
    grid-template-columns: 1fr;
    gap: 48px;
  }

  .bandeiras-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .contato-grid {
    grid-template-columns: 1fr;
  }

  .newsletter-card {
    flex-direction: column;
    text-align: center;
  }

  .newsletter-content p {
    margin: 0 auto;
  }

  .footer-grid {
    grid-template-columns: 1fr 1fr;
    gap: 36px;
  }

  .galeria-grid {
    grid-template-columns: 1fr;
  }

  .galeria-item.large {
    grid-row: span 1;
  }
}

@media (max-width: 768px) {
  .mobile-toggle {
    display: flex;
  }

  .nav-links {
    position: fixed;
    top: 0;
    right: -100%;
    width: 280px;
    height: 100vh;
    background: rgba(0, 10, 40, 0.98);
    backdrop-filter: blur(20px);
    flex-direction: column;
    justify-content: center;
    gap: 4px;
    padding: 32px;
    transition: var(--transition-smooth);
  }

  .nav-links.open {
    right: 0;
  }

  .nav-links a {
    font-size: 1.1rem;
    padding: 14px 20px;
    width: 100%;
    text-align: center;
  }

  .hero-name { font-size: 2.5rem; }
  .hero-surname { font-size: 3rem; }

  .hero-image-frame {
    width: 300px;
    height: 380px;
  }

  .hero-stats {
    flex-direction: column;
    gap: 20px;
    padding: 20px;
  }

  .stat-divider {
    width: 60px;
    height: 1px;
  }

  .section-title {
    font-size: 2.2rem;
  }

  .bandeiras-grid {
    grid-template-columns: 1fr;
  }

  .timeline::before {
    left: 20px;
  }

  .timeline-item.left,
  .timeline-item.right {
    padding-left: 60px;
    padding-right: 0;
    justify-content: flex-start;
  }

  .timeline-dot {
    left: 20px;
    transform: translateX(-50%);
  }

  blockquote {
    font-size: 1.3rem;
  }

  .input-group {
    flex-direction: column;
  }

  .input-group input {
    width: 100%;
  }

  .newsletter-card {
    padding: 36px 28px;
  }

  .contato-form-wrapper {
    padding: 28px;
  }

  .form-row {
    grid-template-columns: 1fr;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    gap: 32px;
  }

  .footer-bottom-inner {
    flex-direction: column;
    gap: 12px;
    text-align: center;
  }
}
</style>

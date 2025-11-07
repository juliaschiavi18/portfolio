# Portfólio de Desenvolvedora Full-Stack com Foco em Cybersecurity

Um portfólio moderno e responsivo construído com React (JSX) e Tailwind CSS, apresentando projetos de cybersecurity, habilidades em segurança de aplicações e informações de contato. O site oferece suporte completo a modo escuro (rosa escuro) e claro (cinza claro).

## Características Principais

**Navegação e Roteamento**
- Menu de navegação responsivo com suporte a dispositivos móveis
- Roteamento de página única (SPA) utilizando a biblioteca Wouter
- Navegação suave entre diferentes seções do portfólio

**Modo Tema**
- Toggle de tema claro/escuro com persistência em localStorage
- Paleta de cores personalizada: cinza claro para modo claro e rosa escuro para modo escuro
- Transições suaves entre temas

**Seção de Projetos**
- Grade responsiva de projetos com imagens
- Busca em tempo real por título, descrição ou tecnologias
- Filtro por categoria (Cybersecurity, Web Application)
- Cards de projeto com informações detalhadas, tecnologias utilizadas e links para projeto ao vivo e repositório GitHub

**Formulário de Contato**
- Formulário completo com validação de campos
- Validação de email
- Notificações de sucesso/erro usando Sonner toast
- Suporte a acessibilidade com labels e aria-labels

**Seções Adicionais**
- Hero section com chamada para ação focada em cybersecurity
- Seção de especialidades (Segurança de Aplicações, Teste de Penetração, Análise de Ameaças, etc.)
- Página sobre com experiência profissional e certificações
- Footer com links sociais e informações de contato

## Stack Tecnológico

| Tecnologia | Versão | Propósito |
|-----------|--------|----------|
| React | 19 | Framework JavaScript para UI |
| JSX | - | Sintaxe para componentes React |
| Tailwind CSS | 4 | Framework CSS utilitário |
| Wouter | - | Roteamento leve para SPA |
| Lucide React | - | Ícones SVG |
| Sonner | - | Notificações toast |
| Vite | 5 | Build tool e dev server |

## Estrutura do Projeto

```
portfolio-cybersecurity/
├── src/
│   ├── components/          # Componentes reutilizáveis
│   │   ├── Header.jsx
│   │   ├── Footer.jsx
│   │   └── ProjectCard.jsx
│   ├── contexts/            # React contexts
│   │   └── ThemeContext.jsx
│   ├── data/                # Dados estáticos
│   │   └── projects.js
│   ├── pages/               # Páginas/rotas
│   │   ├── Home.jsx
│   │   ├── Projects.jsx
│   │   ├── About.jsx
│   │   ├── Contact.jsx
│   │   └── NotFound.jsx
│   ├── App.jsx              # Componente raiz com rotas
│   ├── main.jsx             # Entry point
│   └── index.css            # Estilos globais e temas
├── public/                  # Arquivos estáticos
├── index.html
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
├── package.json
├── .gitignore
├── todo.md
└── README.md
```

## Páginas e Rotas

| Rota | Página | Descrição |
|------|--------|-----------|
| `/` | Home | Página inicial com hero section, especialidades e projetos em destaque |
| `/projects` | Projetos | Galeria completa de projetos com busca e filtro |
| `/about` | Sobre | Informações pessoais, habilidades, experiência e certificações |
| `/contact` | Contato | Formulário de contato e informações de comunicação |
| `/404` | Não Encontrado | Página de erro para rotas inexistentes |

## Funcionalidades de Busca e Filtro

A página de projetos oferece duas formas de filtrar projetos:

**Busca por Texto**
- Busca em tempo real por título do projeto
- Busca na descrição do projeto
- Busca por tecnologias utilizadas
- Atualização instantânea dos resultados

**Filtro por Categoria**
- Todos os Projetos
- Cybersecurity
- Web Application

Os filtros funcionam em conjunto, permitindo combinações como "buscar por 'Python' na categoria 'Cybersecurity'".

## Formulário de Contato

O formulário de contato inclui:

- Campo de nome (obrigatório)
- Campo de email com validação (obrigatório)
- Campo de assunto (obrigatório)
- Campo de mensagem (obrigatório)
- Validação de todos os campos antes do envio
- Mensagem de sucesso ao enviar
- Mensagem de erro em caso de falha

## Acessibilidade

O projeto segue as melhores práticas de acessibilidade:

- Todos os elementos interativos possuem labels apropriados
- Uso de aria-labels para ícones e botões
- Atributo alt em todas as imagens
- Navegação por teclado completa
- Contraste de cores adequado em ambos os temas
- Suporte a leitores de tela

## Responsividade

O portfólio é totalmente responsivo e funciona perfeitamente em:

- Dispositivos móveis (320px e acima)
- Tablets (768px e acima)
- Desktops (1024px e acima)
- Telas grandes (1280px e acima)

Utiliza breakpoints do Tailwind CSS para adaptar o layout em diferentes tamanhos de tela.

## Paleta de Cores

### Modo Claro (Light)
- Fundo: Cinza muito claro
- Texto: Cinza escuro
- Primária: Roxo/Azul (cinza claro)
- Acentos: Variações de cinza

### Modo Escuro (Dark)
- Fundo: Preto/Cinza muito escuro
- Texto: Branco/Cinza claro
- Primária: Rosa escuro
- Acentos: Variações de rosa

## Como Usar

### Instalação

```bash
# Instalar dependências com pnpm (recomendado)
pnpm install

# Ou com npm
npm install --legacy-peer-deps
```

### Desenvolvimento

```bash
# Iniciar servidor de desenvolvimento
pnpm dev
# ou
npm run dev
```

O servidor estará disponível em `http://localhost:3000`.

### Build para Produção

```bash
# Criar build otimizado
pnpm build
# ou
npm run build
```

### Preview do Build

```bash
# Visualizar build de produção localmente
pnpm preview
# ou
npm preview
```

## Personalização

### Adicionar Novos Projetos

Para adicionar novos projetos, edite o arquivo `src/data/projects.js`:

```javascript
{
  id: '9',
  title: 'Seu Projeto',
  description: 'Descrição do projeto',
  image: 'URL da imagem',
  category: 'Cybersecurity',
  technologies: ['Python', 'Machine Learning'],
  liveUrl: 'https://seu-projeto.com',
  githubUrl: 'https://github.com/usuario/projeto',
}
```

### Personalizar Cores

As cores são definidas em `src/index.css` usando variáveis CSS. Modifique os valores OKLCH para alterar a paleta de cores:

```css
:root {
  /* Modo claro */
  --primary: oklch(0.65 0.15 280);
  /* ... outras cores */
}

.dark {
  /* Modo escuro */
  --primary: oklch(0.55 0.2 330);
  /* ... outras cores */
}
```

### Adicionar Novas Páginas

Para adicionar uma nova página:

1. Crie um novo arquivo em `src/pages/NovaPagina.jsx`
2. Implemente o componente da página
3. Adicione a rota em `src/App.jsx`
4. Atualize o menu em `src/components/Header.jsx`

## SEO

O portfólio inclui otimizações básicas de SEO:

- Títulos semânticos (h1, h2, h3)
- Atributos alt em todas as imagens
- Meta tags apropriadas
- Estrutura HTML semântica
- Navegação clara e lógica

## Performance

O projeto utiliza as seguintes técnicas para otimizar performance:

- Lazy loading de imagens
- Otimização de bundle com Vite
- Code splitting automático
- Componentes React otimizados
- CSS utilitário (Tailwind) para reduzir tamanho do CSS

## Navegadores Suportados

O portfólio funciona em todos os navegadores modernos:

- Chrome (últimas 2 versões)
- Firefox (últimas 2 versões)
- Safari (últimas 2 versões)
- Edge (últimas 2 versões)

## Contribuindo

Para contribuir com melhorias:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Contato

Para dúvidas ou sugestões sobre o portfólio, entre em contato através do formulário de contato no site ou pelos links de redes sociais no footer.

---

**Desenvolvido com ❤️ usando React (JSX) e Tailwind CSS**

**Temática:** Desenvolvedora Full-Stack Apaixonada por Cybersecurity
# portfolio

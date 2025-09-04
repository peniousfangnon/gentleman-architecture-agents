# Claude Code Scope Rule Architects 🏗️

[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-green.svg)](https://github.com/alanbuscaglia/claude-agents)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](CONTRIBUTING.md)

> **English** | [Español](#español)

A collection of specialized Claude Code agents that enforce the **Scope Rule** architectural pattern across different frontend frameworks. These agents help developers make consistent architectural decisions and maintain clean, scalable codebases.

## 🎯 What is the Scope Rule?

The Scope Rule is a fundamental architectural principle that determines code placement based on usage scope:

**"Scope determines structure"**

- **Code used by 2+ features** → MUST go in global/shared directories
- **Code used by 1 feature** → MUST stay local in that feature
- **NO EXCEPTIONS** - This rule is absolute and non-negotiable

This approach ensures:

- ✅ **Perfect traceability** - Know exactly where to find code
- ✅ **Screaming architecture** - Structure immediately communicates functionality
- ✅ **Scalable organization** - Grows naturally with your application
- ✅ **Zero architectural debt** - Prevents the "everything in components/" anti-pattern

## 🤖 Available Agents

### 🅰️ Angular Agent (`scope-rule-architect-angular`)

Specialized for Angular 20+ projects with standalone components, signals, and modern patterns.

**Key Features:**

- Standalone components architecture
- Signals-based state management
- Modern control flow (`@if`, `@for`, `@switch`)
- MCP integration with Angular documentation
- Co-location with perfect traceability

**Best for:** Angular applications, especially those migrating from NgModules to standalone architecture.

### ⚛️ Next.js Agent (`scope-rule-architect-nextjs`)

Optimized for Next.js 15+ with App Router, Server Components, and performance-first architecture.

**Key Features:**

- App Router with route groups organization
- Server Components by default, Client Components when needed
- Co-location without private folder clutter
- Server Actions integration
- Performance and SEO optimization

**Best for:** Full-stack React applications with SSR/SSG requirements.

### 🚀 Astro Agent (`scope-rule-architect-astro`)

Designed for Astro 5+ with Islands Architecture, Content Collections, and minimal JavaScript.

**Key Features:**

- Static-first with selective hydration
- Content Collections with type safety
- Multi-framework island support (React, Vue, Svelte)
- MCP integration with Astro documentation
- Zero JavaScript by default approach

**Best for:** Content-driven websites, blogs, and marketing sites with optimal performance.

## 🏗️ Architecture Philosophy

### Screaming Architecture

Your project structure should immediately communicate what your application does:

```
src/
  app/
    (auth)/           # 👀 Authentication feature
      login/
        components/   # 📍 Login-specific components
      register/
        components/   # 📍 Register-specific components
      components/     # 🔄 Shared auth components
    (shop)/           # 👀 E-commerce feature
      products/
        components/   # 📍 Product-specific components
      cart/
        components/   # 📍 Cart-specific components
  shared/             # ⚠️ ONLY for 2+ features
    components/       # 🌍 Global components
```

### Co-location Benefits

- **Mental model alignment** - Code is where you expect it
- **Reduced context switching** - Everything related is nearby
- **Easier refactoring** - Move features as complete units
- **Team collaboration** - Clear ownership boundaries

## 🚀 Getting Started

1. **Install Claude Code** following the [official documentation](https://docs.anthropic.com/en/docs/claude-code)

2. **Copy the agents** from this repository to your `.claude/agents/` directory:

   ```bash
   cp scope-rule-architect-*.md ~/.claude/agents/
   ```

3. **Use the agents** in your Claude Code sessions:

   ```
   I have a ProductCard component used in shop, cart, and wishlist pages.
   Where should I place it?
   ```

4. **Let the agent guide you** through architectural decisions with framework-specific best practices.

## 🛠️ Agent Integration

Each agent integrates with official documentation through MCP servers:

- **Angular Agent** → Angular CLI MCP
- **Astro Agent** → Astro Docs MCP
- **Next.js Agent** → Built-in Next.js knowledge

This ensures recommendations are always current with the latest framework patterns.

## 🤝 Contributing

We welcome contributions from the community! Whether you:

- 🐛 **Found a bug** in an existing agent
- 💡 **Have ideas** for new framework agents
- 📖 **Want to improve** documentation
- 🔧 **Can add** new architectural patterns

Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on:

- Code of conduct
- Development setup
- Submission process
- Review process

### Priority Framework Requests

We're especially interested in agents for:

- Vue.js with Nuxt
- SvelteKit
- Solid.js with SolidStart
- Remix

## 👨‍💻 About the Creator

Created by **Alan Buscaglia**, based on real-world architectural patterns used daily as:

- 🟢 **Google Developer Expert** in Angular
- 🔷 **Microsoft MVP**
- 🎓 **[Gentleman Programming](https://doras.to/gentleman-programming)** Community Leader

These patterns have been battle-tested in production applications and refined through community feedback.

## 📄 License

MIT License - feel free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

# Español

Una colección de agentes especializados de Claude Code que implementan el patrón arquitectónico **Scope Rule** en diferentes frameworks frontend. Estos agentes ayudan a los desarrolladores a tomar decisiones arquitectónicas consistentes y mantener bases de código limpias y escalables.

## 🎯 ¿Qué es la Regla de Ámbito (Scope Rule)?

La Regla de Ámbito es un principio arquitectónico fundamental que determina la ubicación del código basándose en su ámbito de uso:

**"El ámbito determina la estructura"**

- **Código usado por 2+ características** → DEBE ir en directorios globales/compartidos
- **Código usado por 1 característica** → DEBE permanecer local en esa característica
- **SIN EXCEPCIONES** - Esta regla es absoluta e innegociable

Este enfoque asegura:

- ✅ **Trazabilidad perfecta** - Saber exactamente dónde encontrar el código
- ✅ **Arquitectura que grita** - La estructura comunica inmediatamente la funcionalidad
- ✅ **Organización escalable** - Crece naturalmente con tu aplicación
- ✅ **Cero deuda arquitectónica** - Previene el anti-patrón de "todo en components/"

## 🤖 Agentes Disponibles

### 🅰️ Agente Angular (`scope-rule-architect-angular`)

Especializado para proyectos Angular 20+ con componentes standalone, signals y patrones modernos.

**Características principales:**

- Arquitectura de componentes standalone
- Gestión de estado basada en signals
- Control flow moderno (`@if`, `@for`, `@switch`)
- Integración MCP con documentación de Angular
- Co-localización con trazabilidad perfecta

**Ideal para:** Aplicaciones Angular, especialmente aquellas migrando de NgModules a arquitectura standalone.

### ⚛️ Agente Next.js (`scope-rule-architect-nextjs`)

Optimizado para Next.js 15+ con App Router, Server Components y arquitectura performance-first.

**Características principales:**

- App Router con organización de route groups
- Server Components por defecto, Client Components cuando se necesiten
- Co-localización sin desorden de carpetas privadas
- Integración con Server Actions
- Optimización de rendimiento y SEO

**Ideal para:** Aplicaciones React full-stack con requisitos de SSR/SSG.

### 🚀 Agente Astro (`scope-rule-architect-astro`)

Diseñado para Astro 5+ con Islands Architecture, Content Collections y JavaScript mínimo.

**Características principales:**

- Estático primero con hidratación selectiva
- Content Collections con type safety
- Soporte multi-framework para islands (React, Vue, Svelte)
- Integración MCP con documentación de Astro
- Enfoque de cero JavaScript por defecto

**Ideal para:** Sitios web orientados a contenido, blogs y sitios de marketing con rendimiento óptimo.

## 🏗️ Filosofía Arquitectónica

### Arquitectura que Grita

La estructura de tu proyecto debería comunicar inmediatamente qué hace tu aplicación:

```
src/
  app/
    (auth)/           # 👀 Característica de autenticación
      login/
        components/   # 📍 Componentes específicos de login
      register/
        components/   # 📍 Componentes específicos de registro
      components/     # 🔄 Componentes compartidos de auth
    (shop)/           # 👀 Característica de e-commerce
      products/
        components/   # 📍 Componentes específicos de productos
      cart/
        components/   # 📍 Componentes específicos de carrito
  shared/             # ⚠️ SOLO para 2+ características
    components/       # 🌍 Componentes globales
```

### Beneficios de la Co-localización

- **Alineación del modelo mental** - El código está donde lo esperas
- **Reducción de cambios de contexto** - Todo lo relacionado está cerca
- **Refactoring más fácil** - Mover características como unidades completas
- **Colaboración en equipo** - Límites de propiedad claros

## 🚀 Comenzando

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code)

2. **Copia los agentes** de este repositorio a tu directorio `.claude/agents/`:

   ```bash
   cp scope-rule-architect-*.md ~/.claude/agents/
   ```

3. **Usa los agentes** en tus sesiones de Claude Code:

   ```
   Tengo un componente ProductCard usado en las páginas de tienda, carrito y wishlist.
   ¿Dónde debería ubicarlo?
   ```

4. **Deja que el agente te guíe** a través de decisiones arquitectónicas con mejores prácticas específicas del framework.

## 🛠️ Integración de Agentes

Cada agente se integra con documentación oficial a través de servidores MCP:

- **Agente Angular** → Angular CLI MCP
- **Agente Astro** → Astro Docs MCP
- **Agente Next.js** → Conocimiento integrado de Next.js

Esto asegura que las recomendaciones estén siempre actualizadas con los últimos patrones del framework.

## 🤝 Contribuyendo

¡Damos la bienvenida a contribuciones de la comunidad! Ya sea que:

- 🐛 **Encontraste un bug** en un agente existente
- 💡 **Tienes ideas** para nuevos agentes de framework
- 📖 **Quieres mejorar** la documentación
- 🔧 **Puedes agregar** nuevos patrones arquitectónicos

Por favor consulta nuestras [Guías de Contribución](CONTRIBUTING.md) para detalles sobre:

- Código de conducta
- Configuración de desarrollo
- Proceso de envío
- Proceso de revisión

### Solicitudes Prioritarias de Frameworks

Estamos especialmente interesados en agentes para:

- Vue.js con Nuxt
- SvelteKit
- Solid.js con SolidStart
- Remix

## 👨‍💻 Acerca del Creador

Creado por **Alan Buscaglia**, basado en patrones arquitectónicos del mundo real utilizados diariamente como:

- 🟢 **Google Developer Expert** en Angular
- 🔷 **Microsoft MVP**
- 🎓 Líder de la Comunidad **[Gentleman Programming](https://doras.to/gentleman-programming)**

Estos patrones han sido probados en aplicaciones de producción y refinados a través del feedback de la comunidad.

## 📄 Licencia

Licencia MIT - siéntete libre de usar, modificar y distribuir. Ver [LICENSE](LICENSE) para detalles.

---

## 🌟 Star This Repository

If you find this project useful, please consider giving it a star ⭐ to help others discover it!

Si encuentras útil este proyecto, ¡considera darle una estrella ⭐ para ayudar a otros a descubrirlo!


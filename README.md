<h1 align="center">John Mugabe</h1>

<p align="center">
  <b>Full-Stack Engineer · Platform &amp; Product</b> · Harare, Zimbabwe<br>
  Building event ticketing and payment infrastructure for Africa, by Africa.
</p>

<p align="center">
  <a href="mailto:jonesmugabe08@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-jonesmugabe08%40gmail.com-D14836?logo=gmail&logoColor=white"></a>
  <a href="https://linkedin.com/in/johnmugabe"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-johnmugabe-0A66C2?logo=linkedin&logoColor=white"></a>
  <a href="https://johnmugabe.online"><img alt="Website" src="https://img.shields.io/badge/Portfolio-mystrikingly-111111?logo=googlechrome&logoColor=white"></a>
  <a href="https://github.com/67even"><img alt="67even" src="https://img.shields.io/badge/Open%20source-67even-FF3131?logo=github&logoColor=white"></a>
  <img alt="Open to work" src="https://img.shields.io/badge/Open%20to-work%20%26%20collaboration-2EA043">
</p>

---

```php
<?php

declare(strict_types=1);

/**
 * John Mugabe - Full-Stack Developer
 *
 * 11 years shipping production web platforms, from Laravel monoliths to
 * multi-app TypeScript monorepos. Currently building 263tickets Discover:
 * a multi-sided event ticketing platform for Africa, by Africa, with native
 * mobile-money rails, WhatsApp-first ticket delivery, and inventory that
 * survives an arena on-sale.
 *
 * Clean code, tested behaviour, correctness under load, and money that
 * always adds up.
 *
 * @author  John Mugabe <jonesmugabe08@gmail.com>
 * @see     https://github.com/johnmugabe
 * @see     https://github.com/67even
 * @see     https://johnmugabe.online
 */
final readonly class AboutMe
{
    public function __construct(
        public string $name = 'John Mugabe',
        public string $title = 'Full-Stack Developer · Platform & Product',
        public string $location = 'Harare, Zimbabwe',
        public string $timezone = 'Africa/Harare',
        public int $yearsOfExperience = 11,
        public string $currentFocus = 'Payments integrity, inventory at scale, and AI-augmented delivery',
        public string $philosophy = 'Clean code, tested behaviour, delighted users',
        public bool $openToWork = true,
        public bool $openToCollaboration = true,
    ) {
    }

    /** @return array<string, string> */
    public function contact(): array
    {
        return [
            'email'      => 'jonesmugabe08@gmail.com',
            'linkedin'   => 'linkedin.com/in/johnmugabe',
            'github'     => 'github.com/johnmugabe',
            'openSource' => 'github.com/67even',
            'portfolio'  => 'johnmugabe.mystrikingly.com',
        ];
    }

    /** @return list<array{role: string, company: string, website: string}> */
    public function experience(): array
    {
        return [
            ['role' => 'Co-Founder & CTO',          'company' => 'Innfuture Technologies', 'website' => 'https://www.innfuture.co.zw'],
            ['role' => 'Lead Platform Architect', 'company' => '263tickets',             'website' => 'https://www.263tickets.co.zw'],
        ];
    }

    /** @return list<string> */
    public function recentlyShipped(): array
    {
        return [
            'Zimbabwe payments cutover: EcoCash, InnBucks and ZimSwitch on a custodial ledger',
            'Closed three inventory leaks with Redis hold-restoration sweeps',
            'Apple & Google Wallet pass pipeline, with revocable device tokens',
            'Gated livestreaming: signed HLS, access codes, device binding',
            'Enterprise WhatsApp management: consent, STOP semantics, broadcasts, inbox',
            'Admin control plane: RBAC, tamper-evident audit trail, emergency kill switches',
            'Buyer account hub: wallet, refund requests, DSAR export, payment methods',
            'Four coexisting design-token systems across web, organiser, admin and mobile',
            'Open-source developer guides and Claude skills for Paynow and EcoCash (github.com/67even)',
        ];
    }

    /** @return list<array{name: string, description: string, stack: list<string>, features: list<string>}> */
    public function currentProjects(): array
    {
        return [
            [
                'name'        => '263tickets Discover',
                'description' => 'Event ticketing for Africa, by Africa: organisers, attendees, venues and partners',
                'stack'       => ['Next.js', 'NestJS', 'Drizzle', 'PostgreSQL', 'Redis', 'Temporal', 'Typesense', 'Expo'],
                'features'    => [
                    'Native mobile-money rails on a custodial ledger',
                    'Oversell-proof inventory holds under on-sale load',
                    'WhatsApp-first ticket delivery with a consent ledger',
                    'Apple & Google Wallet passes with live updates',
                    'Gated livestreaming over signed HLS',
                    'Offline-capable door scanning',
                ],
            ],
            [
                'name'        => 'E-commerce Platform',
                'description' => 'Scalable e-commerce solution with a microservices architecture',
                'stack'       => ['Laravel', 'Vue.js', 'MySQL', 'Redis'],
                'features'    => ['Microservices', 'Real-time Analytics', 'Payment Integration'],
            ],
        ];
    }

    /** @return array<string, string> Zimbabwean payment rails, documented for other developers */
    public function openSource(): array
    {
        return [
            'ecocash-instant-payment-api' => 'EcoCash Instant Payment (EIP) guide, tested clients in 5 languages, and a Claude skill',
            'paynow-integration-skill'    => 'Paynow checkout integration guide and Claude skill',
            'paynow-billpay-skill'        => 'Paynow bill payments guide and Claude skill',
            'InnBucks Merchant API Developer Guide'  => 'Integrate InnBucks: generate a payment code, show it with its QR code and deep link, confirm payment and go live.',
        ];
    }

    /** @return array<string, list<string>> */
    public function platformEngineering(): array
    {
        return [
            'Inventory at Scale' => ['Atomic Redis Lua Holds', 'TTL + Heartbeat Extension', 'Cache Pre-warming', 'k6 On-Sale Rehearsals'],
            'Durable Workflows'  => ['Temporal', 'Idempotent Activities', 'continueAsNew Fan-out', 'Reconciliation Sweeps'],
            'Realtime'           => ['Soketi (Pusher protocol)', 'Scoped Channels', 'Live Availability Push'],
            'Architecture'       => ['Modular Monolith', 'Bounded Contexts', 'Boundary Lint Gates', 'Domain-Event Outbox'],
            'Reliability'        => ['Idempotency Keys', 'Poll-Reconciliation over Webhooks', 'Process-Safety Nets', 'Graceful Degradation'],
        ];
    }

    /** @return array<string, list<string>> */
    public function fintech(): array
    {
        return [
            'Payment Rails'   => ['EcoCash', 'InnBucks', 'ZimSwitch', 'Paynow', 'Custodial Ledger'],
            'Money Modelling' => ['Integer Minor Units', 'ISO 4217 Currency Codes', 'Multi-currency (USD / ZiG / ZAR)', 'Never Floats'],
            'Integrity'       => ['Signature-verified Webhooks', 'Enquiry-endpoint Reconciliation', 'Double-entry Ledgers', 'Dispute-grade Audit Trails'],
            'Compliance'      => ['PCI SAQ-A Scope', 'Hosted / Tokenised Card Flows', 'No PAN or CVV Ever Stored'],
        ];
    }

    /** @return array<string, list<string>> */
    public function backend(): array
    {
        return [
            'PHP 8.x'         => ['Laravel', 'Symfony', 'Livewire'],
            'TypeScript/Node' => ['NestJS', 'Node.js 22', 'Fastify', 'Zod-validated Boundaries'],
            'Databases'       => ['PostgreSQL', 'MySQL', 'Redis', 'Typesense', 'pgvector', 'Elasticsearch'],
            'Data Access'     => ['Drizzle ORM', 'Eloquent', 'Query Tuning', 'Forward-only Migrations'],
            'APIs'            => ['REST (versioned)', 'OpenAPI Contracts', 'GraphQL', 'WebSocket Services'],
            'Async & Jobs'    => ['Temporal Workflows', 'Queue Systems', 'Scheduled Reconciliation', 'Outbox Events'],
        ];
    }

    /** @return array<string, list<string>> */
    public function frontend(): array
    {
        return [
            'JavaScript'              => ['React 19', 'Next.js App Router / RSC', 'TypeScript', 'Vue.js 3', 'Alpine.js'],
            'State & Forms'           => ['TanStack Query', 'React Hook Form', 'Zod', 'Server Actions'],
            'Styling'                 => ['Tailwind CSS v4', 'Design Tokens', 'shadcn/ui on Radix', 'SASS/SCSS'],
            'Motion'                  => ['Motion', 'GSAP', 'Lenis', 'Lottie / Rive', 'prefers-reduced-motion'],
            'Mobile'                  => ['Expo', 'React Native', 'NativeWind', 'Offline-first SQLite'],
            'Build Tools'             => ['Turborepo', 'Turbopack', 'Vite', 'pnpm Workspaces', 'Biome'],
            'Progressive Enhancement' => ['PWAs', 'Offline-first', 'Performance Budgeting'],
        ];
    }

    /** @return array<string, list<string>> */
    public function design(): array
    {
        return [
            'Tools'          => ['Figma', 'Adobe XD', 'Sketch'],
            'User Research'  => ['User Personas', 'Journey Mapping', 'Usability Testing'],
            'Design Systems' => ['Multi-brand Token Architectures', 'Component Libraries', 'Automated Token Linting'],
            'Accessibility'  => ['WCAG 2.1', 'Screen Readers', 'Keyboard Navigation'],
        ];
    }

    /** @return array<string, list<string>> */
    public function ai(): array
    {
        return [
            'Tooling'    => ['Vercel AI SDK', 'Claude (Opus / Sonnet / Haiku)', 'Claude Skills', 'Structured Output via Zod', 'Prompt Caching'],
            'Surfaces'   => ['Semantic Discovery & Re-ranking', 'Content Generation', 'Moderation Triage', 'Fraud Scoring', 'Pricing Suggestions'],
            'Retrieval'  => ['pgvector', 'Embedding Pipelines', 'Hybrid Search with Typesense'],
            'Guardrails' => ['Per-request Spend Caps', 'Human-in-the-loop Gates', 'Explainable Recommendations', 'Full Decision Audit'],
        ];
    }

    /** @return array<string, list<string>> */
    public function security(): array
    {
        return [
            'AuthN / AuthZ'   => ['Clerk', 'JWT Verification', 'RBAC as Policy Code', 'Two-Admin Approval on High-Risk Actions'],
            'Data Protection' => ['Column-level PII Encryption (KMS)', 'Log Redaction', 'Secret Scanning', 'Rate Limiting & Anti-bot'],
            'Auditability'    => ['Append-only Audit Log', 'Merkle-chained Tamper Evidence', 'Impersonation Tracing'],
            'Privacy Law'     => ['GDPR', 'POPIA', 'Zimbabwe Cyber & Data Protection Act', 'DSAR Export + Erasure'],
        ];
    }

    /** @return array<string, list<string>> */
    public function devOps(): array
    {
        return [
            'Containers'    => ['Docker', 'Docker Compose', 'Kubernetes'],
            'Cloud'         => ['Vercel', 'Railway', 'Cloudflare (R2 / WAF / Stream)', 'AWS', 'DigitalOcean', 'Forge & Envoyer'],
            'CI/CD'         => ['GitHub Actions', 'Pre-commit Gates', 'Preview Deploys', 'Feature-flagged Dark Launches'],
            'Observability' => ['OpenTelemetry', 'Grafana Cloud (Loki / Tempo / Mimir)', 'Sentry', 'SLO-based Alerting'],
        ];
    }

    /** @return array<string, list<string>> */
    public function principles(): array
    {
        return [
            'Code Quality'          => ['Test-Driven Development', 'Clean Architecture', 'SOLID', 'Design Patterns'],
            'Collaboration'         => ['Agile', 'Code Reviews', 'Architecture Decision Records', 'Docs Shipped in the Same PR'],
            'User Focus'            => ['User-Centred Design', 'Performance First', 'Progressive Enhancement', 'Continuous Feedback'],
            'AI-Augmented Delivery' => ['Agentic Workflows with Claude Code', 'Multi-agent Adversarial Audits', 'Spec-driven Implementation', 'Human Review Before Merge'],
        ];
    }

    /** @return list<string> */
    public function education(): array
    {
        return [
            'Information Technology (HND)',
            'UI/UX Certified',
            'Full-Stack Web Development Certified',
            'X-Platform Mobile Development Certified',
            'Google Skillshop Certified',
        ];
    }

    /** @return list<array{name: string, description: string, stack: list<string>, url?: string}> */
    public function sideProjects(): array
    {
        return [
            [
                'name'        => 'iZambezi CSS',
                'description' => 'Custom CSS framework for rapid UI development',
                'url'         => 'https://izambezi.vercel.app',
                'stack'       => ['CSS', 'SCSS', 'JavaScript'],
            ],
            [
                'name'        => 'GasFlow',
                'description' => 'Point-of-sale SaaS for LPG retail: stock, cylinders and cash reconciliation',
                'stack'       => ['Laravel', 'Livewire', 'PostgreSQL'],
            ],
        ];
    }
}

echo (new AboutMe())->openToCollaboration ? "Let's build something. 👋" : '';
```

---

### Open source

Developer guides for Zimbabwean payment rails, each with tested code, a documentation site and an installable Claude skill.

| Repository | What it is |
|:---|:---|
| [**ecocash-instant-payment-api**](https://github.com/67even/ecocash-instant-payment-api) · [docs](https://67even.github.io/ecocash-instant-payment-api/) | EcoCash Instant Payment (EIP) API: sandbox to go-live, clients in PHP, Node.js, Python, Java and C#, and a Claude skill |
| [**paynow-integration-skill**](https://github.com/67even/paynow-integration-skill) · [docs](https://67even.github.io/paynow-integration-skill/) | Paynow checkout integration guide and Claude skill |
| [**paynow-billpay-skill**](https://github.com/67even/paynow-billpay-skill) · [docs](https://67even.github.io/paynow-billpay-skill/) | Paynow bill payments guide and Claude skill |
| [**innbucks-merchant-api-integration**](https://github.com/67even/innbucks-merchant-api-integration) · [docs](https://67even.github.io/innbucks-merchant-api-integration/) | InnBucks merchant API developer guide and Claude skill |

### Side projects

- [**iZambezi CSS**](https://izambezi.vercel.app): a custom CSS framework for rapid UI development

<p align="center"><sub>Harare, Zimbabwe · Africa/Harare (UTC+2) · <a href="mailto:jonesmugabe08@gmail.com">jonesmugabe08@gmail.com</a></sub></p>

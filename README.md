# Hey, I am ME!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/johnmugabe)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat-square&logo=gmail)](mailto:jonesmugabe@innfuture.co.zw)

## ReadME and don't forget to get in touch :)

```php

<?php

declare(strict_types=1);

/**
 * John Mugabe - Full-Stack Engineer
 *
 * 8+ years shipping production web platforms — from Laravel monoliths to
 * multi-app TypeScript monorepos. Currently building 263tickets Discover:
 * a multi-sided event ticketing platform for Africa, by Africa — native
 * mobile-money rails, WhatsApp-first ticket delivery, and inventory that
 * survives an arena on-sale.
 *
 * Passionate about clean code, TDD, correctness under load, and money
 * that always adds up.
 *
 * @author  John Mugabe <jonesmugabe08@gmail.com>
 * @see     https://github.com/johnmugabe
 * @see     https://johnmugabe.mystrikingly.com
 */
final readonly class AboutMe
{
    public function __construct(
        public string $name = 'John Mugabe',
        public string $title = 'Full-Stack Engineer · Platform & Product',
        public string $location = 'Harare, Zimbabwe',
        public string $timezone = 'Africa/Harare',
        public int $yearsOfExperience = 8,
        public string $currentFocus = 'Payments integrity, inventory at scale, and AI-augmented delivery',
        public string $philosophy = 'Clean code, tested behaviour, delighted users',
        public bool $openToWork = true,
        public bool $openToCollaboration = true,
    ) {
    }

    public function contact(): array
    {
        return [
            'email'     => 'jonesmugabe08@gmail.com',
            'linkedin'  => 'linkedin.com/in/johnmugabe',
            'github'    => 'github.com/johnmugabe',
            'portfolio' => 'johnmugabe.mystrikingly.com',
        ];
    }

    public function certifications(): array
    {
        return [
            'UI/UX Certified',
            'Front-End Development',
            'Mobile Development',
        ];
    }

    public function backendSkills(): array
    {
        return [
            'PHP 8.x'         => ['Laravel', 'Symfony', 'Livewire'],
            'TypeScript/Node' => ['NestJS', 'Node.js 22', 'Fastify', 'Zod-validated boundaries'],
            'Databases'       => ['PostgreSQL', 'MySQL', 'Redis', 'Typesense', 'pgvector', 'Elasticsearch'],
            'Data Access'     => ['Drizzle ORM', 'Eloquent', 'Query tuning', 'Forward-only migrations'],
            'API Development' => ['REST (versioned)', 'OpenAPI contracts', 'GraphQL', 'WebSocket Services'],
            'Async & Jobs'    => ['Temporal Workflows', 'Queue Systems', 'Scheduled Reconciliation', 'Outbox Events'],
        ];
    }

    public function frontendSkills(): array
    {
        return [
            'JavaScript'              => ['React 19', 'Next.js App Router / RSC', 'TypeScript', 'Vue.js 3', 'Alpine.js'],
            'State & Forms'           => ['TanStack Query', 'React Hook Form', 'Zod', 'Server Actions'],
            'Styling'                 => ['Tailwind CSS v4', 'Design Tokens', 'shadcn/ui on Radix', 'SASS/SCSS'],
            'Motion'                  => ['Motion', 'GSAP', 'Lenis', 'Lottie/Rive', 'prefers-reduced-motion'],
            'Mobile'                  => ['Expo', 'React Native', 'NativeWind', 'Offline-First SQLite'],
            'Build Tools'             => ['Turborepo', 'Turbopack', 'Vite', 'pnpm Workspaces', 'Biome'],
            'Progressive Enhancement' => ['PWAs', 'Offline-First', 'Performance Budgeting'],
        ];
    }

    public function designSkills(): array
    {
        return [
            'Design Tools'   => ['Figma', 'Adobe XD', 'Sketch'],
            'User Research'  => ['User Personas', 'Journey Mapping', 'Usability Testing'],
            'Design Systems' => ['Multi-brand Token Architectures', 'Component Libraries', 'Automated Token Linting'],
            'Accessibility'  => ['WCAG 2.1', 'Screen Readers', 'Keyboard Navigation'],
        ];
    }

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

    public function fintechSkills(): array
    {
        return [
            'Payment Rails'   => ['EcoCash', 'InnBucks', 'ZimSwitch', 'Custodial Ledger'],
            'Money Modelling' => ['Integer Minor Units', 'ISO 4217 Currency Codes', 'Multi-currency (USD/ZiG/ZAR)', 'Never Floats'],
            'Integrity'       => ['Signature-verified Webhooks', 'Enquiry-endpoint Reconciliation', 'Double-entry Ledgers', 'Dispute-grade Audit Trails'],
            'Compliance'      => ['PCI SAQ-A Scope', 'Hosted/Tokenised Card Flows', 'No PAN or CVV Ever Stored'],
        ];
    }

    public function aiEngineering(): array
    {
        return [
            'Tooling'      => ['Vercel AI SDK', 'Claude (Opus / Sonnet / Haiku)', 'Structured Output via Zod', 'Prompt Caching'],
            'Surfaces'     => ['Semantic Discovery & Re-ranking', 'Content Generation', 'Moderation Triage', 'Fraud Scoring', 'Pricing Suggestions'],
            'Retrieval'    => ['pgvector', 'Embedding Pipelines', 'Hybrid Search with Typesense'],
            'Guardrails'   => ['Per-request Spend Caps', 'Human-in-the-loop Gates', 'Explainable Recommendations', 'Full Decision Audit'],
        ];
    }

    public function securityAndCompliance(): array
    {
        return [
            'AuthN / AuthZ'   => ['Clerk', 'JWT Verification', 'RBAC as Policy Code', 'Two-Admin Approval on High-Risk Actions'],
            'Data Protection' => ['Column-level PII Encryption (KMS)', 'Log Redaction', 'Secret Scanning', 'Rate Limiting & Anti-bot'],
            'Auditability'    => ['Append-only Audit Log', 'Merkle-chained Tamper Evidence', 'Impersonation Tracing'],
            'Privacy Law'     => ['GDPR', 'POPIA', 'Zimbabwe Cyber & Data Protection Act', 'DSAR Export + Erasure'],
        ];
    }

    public function devOpsSkills(): array
    {
        return [
            'Containers'      => ['Docker', 'Docker Compose', 'Kubernetes'],
            'Cloud Platforms' => ['Vercel', 'Railway', 'Cloudflare (R2 / WAF / Stream)', 'AWS', 'DigitalOcean', 'Forge & Envoyer'],
            'CI/CD'           => ['GitHub Actions', 'Pre-commit Gates', 'Preview Deploys', 'Feature-flagged Dark Launches'],
            'Observability'   => ['OpenTelemetry', 'Grafana Cloud (Loki / Tempo / Mimir)', 'Sentry', 'SLO-based Alerting'],
        ];
    }

    public function developmentPrinciples(): array
    {
        return [
            'Code Quality'           => ['Test-Driven Development', 'Clean Architecture', 'SOLID Principles', 'Design Patterns'],
            'Collaboration'          => ['Agile Methodology', 'Code Reviews', 'Architecture Decision Records', 'Docs Shipped in the Same PR'],
            'User Focus'             => ['User-Centered Design', 'Performance First', 'Progressive Enhancement', 'Continuous Feedback'],
            'AI-Augmented Delivery'  => ['Agentic Workflows with Claude Code', 'Multi-agent Adversarial Audits', 'Spec-driven Implementation', 'Human Review Before Merge'],
        ];
    }

    public function experience(): array
    {
        return [
            [
                'role'    => 'Systems Developer',
                'company' => '263tickets',
                'website' => 'https://263tickets.com',
                'work'    => 'Multi-sided event ticketing platform — marketplace, organiser console, admin control plane, and two mobile apps over a shared API',
                'stack'   => ['Next.js', 'NestJS', 'TypeScript', 'PostgreSQL', 'Redis', 'Temporal', 'Expo'],
            ],
            [
                'role'    => 'Front-End Developer',
                'company' => 'startupAZ',
                'website' => 'https://www.suaz.co.uk/',
            ],
        ];
    }

    public function currentProjects(): array
    {
        return [
            [
                'name'        => '263tickets Discover',
                'description' => 'Event ticketing platform for Africa, by Africa — built for organisers, attendees, venues and partners',
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
                'description' => 'Scalable e-commerce solution with microservices architecture',
                'stack'       => ['Laravel', 'Vue.js', 'MySQL', 'Redis'],
                'features'    => ['Microservices', 'Real-time Analytics', 'Payment Integration'],
            ],
        ];
    }

    public function recentlyShipped(): array
    {
        return [
            'Zimbabwe payments cutover — EcoCash, InnBucks and ZimSwitch on a custodial ledger',
            'Closed three inventory leaks with Redis hold-restoration sweeps',
            'Apple & Google Wallet pass pipeline, with revocable device tokens',
            'Gated livestreaming — signed HLS, access codes, device binding',
            'Enterprise WhatsApp management — consent, STOP semantics, broadcasts, inbox',
            'Admin control plane — RBAC, tamper-evident audit trail, emergency kill switches',
            'Buyer account hub — wallet, refund requests, DSAR export, payment methods',
            'Four coexisting design-token systems across web, organiser, admin and mobile',
        ];
    }

    public function hobbyProjects(): array
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
                'description' => 'Point-of-sale SaaS for LPG retail — stock, cylinders, and cash reconciliation',
                'stack'       => ['Laravel', 'Livewire', 'PostgreSQL'],
            ],
        ];
    }
}

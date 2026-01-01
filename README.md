# Hey, I am John Mugabe!

[![Website](https://img.shields.io/badge/Website-Portfolio-blue?style=flat-square&logo=google-chrome)](https://johnmugabe.mystrikingly.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/johnmugabe)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/johnmugabe8)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat-square&logo=gmail)](mailto:jonesmugabe08@gmail.com)

## A Little About Me In Source Code

```php

<?php

declare(strict_types=1);

namespace App\Resume;

/**
 * Availability status for collaboration and employment opportunities.
 */
enum AvailabilityStatus: string
{
    case OPEN_TO_OPPORTUNITIES = 'open_to_opportunities';
    case EMPLOYED_NOT_LOOKING = 'employed_not_looking';
    case FREELANCE_AVAILABLE = 'freelance_available';

    public function allowsCollaboration(): bool
    {
        return match ($this) {
            self::OPEN_TO_OPPORTUNITIES, self::FREELANCE_AVAILABLE => true,
            self::EMPLOYED_NOT_LOOKING => false,
        };
    }
}

/**
 * Skill category classification.
 */
enum SkillCategory: string
{
    case BACKEND_ARCHITECTURE = 'backend_architecture';
    case FRONTEND_ENGINEERING = 'frontend_engineering';
    case UI_UX_DESIGN = 'ui_ux_design';
    case DEVOPS_INFRASTRUCTURE = 'devops_infrastructure';
}

/**
 * Immutable value object representing a geographic location.
 */
final readonly class Location
{
    public function __construct(
        public string $city,
        public string $country,
        public string $timezone = 'UTC',
    ) {}

    public function __toString(): string
    {
        return "{$this->city}, {$this->country}";
    }

    public function toArray(): array
    {
        return [
            'city' => $this->city,
            'country' => $this->country,
            'timezone' => $this->timezone,
        ];
    }
}

/**
 * Immutable value object representing contact information.
 */
final readonly class ContactInfo
{
    public function __construct(
        public string $email,
        public string $linkedin,
        public string $github,
        public string $portfolio,
    ) {}

    public function toArray(): array
    {
        return get_object_vars($this);
    }

    public function getEmailLink(): string
    {
        return "mailto:{$this->email}";
    }

    public function getLinkedInUrl(): string
    {
        return "https://{$this->linkedin}";
    }

    public function getGitHubUrl(): string
    {
        return "https://{$this->github}";
    }
}

/**
 * Immutable value object representing a project.
 */
final readonly class Project
{
    /**
     * @param  array<int, string>  $stack
     * @param  array<int, string>  $features
     */
    public function __construct(
        public string $name,
        public string $description = '',
        public ?string $url = null,
        public array $stack = [],
        public array $features = [],
    ) {}

    public function toArray(): array
    {
        return [
            'name' => $this->name,
            'description' => $this->description,
            'url' => $this->url,
            'stack' => $this->stack,
            'features' => $this->features,
        ];
    }
}

/**
 * Base developer class with common functionality.
 */
abstract class Developer
{
    abstract public function getTechnicalSkills(): array;
    abstract public function getDevelopmentPrinciples(): array;
    abstract public function getContactInfo(): ContactInfo;
}

/**
 * Contract interfaces for skill domains.
 */
interface BackendTechnologiesInterface
{
    public function getTechnicalSkills(): array;
}

interface FrontendTechnologiesInterface
{
    public function getTechnicalSkills(): array;
}

interface DesignExpertiseInterface
{
    public function getTechnicalSkills(): array;
}

interface DevOpsToolsInterface
{
    public function getTechnicalSkills(): array;
}

interface DevelopmentPrinciplesInterface
{
    public function getDevelopmentPrinciples(): array;
}

/**
 * Professional profile for a seasoned Full-Stack Developer.
 *
 * Represents 8+ years of experience building scalable web applications
 * within the Laravel ecosystem. Emphasizes clean code, TDD practices,
 * and continuous exploration of emerging technologies.
 *
 * @author  John Mugabe <jonesmugabe08@gmail.com>
 * @license MIT
 * @version 2.0.0
 *
 * @see https://github.com/johnmugabe
 * @see https://johnmugabe.mystrikingly.com
 */
final readonly class AboutMe extends Developer implements
    BackendTechnologiesInterface,
    FrontendTechnologiesInterface,
    DesignExpertiseInterface,
    DevOpsToolsInterface,
    DevelopmentPrinciplesInterface
{
    private const string CURRENT_FOCUS = 'Building scalable web applications with exceptional UX';
    private const string DEVELOPMENT_PHILOSOPHY = 'Clean code, tested features, and delighted users';
    private const int YEARS_OF_EXPERIENCE = 8;

    /**
     * @param  array<int, string>  $certifications
     */
    public function __construct(
        private string $name = 'John Mugabe',
        private string $title = 'Full-Stack PHP Developer',
        private Location $location = new Location(
            city: 'Harare',
            country: 'Zimbabwe',
            timezone: 'Africa/Harare'
        ),
        private array $certifications = [
            'UI/UX Certified',
            'Front-End Development',
            'Mobile Development',
        ],
        private AvailabilityStatus $availability = AvailabilityStatus::OPEN_TO_OPPORTUNITIES,
    ) {}

    // =========================================================================
    // GETTERS
    // =========================================================================

    public function getName(): string
    {
        return $this->name;
    }

    public function getTitle(): string
    {
        return $this->title;
    }

    public function getLocation(): Location
    {
        return $this->location;
    }

    /**
     * @return array<int, string>
     */
    public function getCertifications(): array
    {
        return $this->certifications;
    }

    public function getYearsOfExperience(): int
    {
        return self::YEARS_OF_EXPERIENCE;
    }

    public function getCurrentFocus(): string
    {
        return self::CURRENT_FOCUS;
    }

    public function getDevelopmentPhilosophy(): string
    {
        return self::DEVELOPMENT_PHILOSOPHY;
    }

    // =========================================================================
    // TECHNICAL SKILLS
    // =========================================================================

    /**
     * Retrieve comprehensive technical skills organized by domain.
     *
     * @return array<string, array<string, array<int, string>>>
     */
    public function getTechnicalSkills(): array
    {
        return [
            SkillCategory::BACKEND_ARCHITECTURE->value => [
                'PHP 8.x' => ['Laravel', 'Symfony', 'Livewire'],
                'Databases' => ['MySQL', 'PostgreSQL', 'Redis', 'Elasticsearch'],
                'API Development' => ['REST', 'GraphQL', 'WebSocket Services'],
                'Performance' => ['Caching Strategies', 'Queue Systems', 'Load Optimization'],
            ],

            SkillCategory::FRONTEND_ENGINEERING->value => [
                'JavaScript' => ['Vue.js 3', 'React', 'TypeScript', 'Alpine.js'],
                'Styling' => ['Tailwind CSS', 'SASS/SCSS', 'CSS-in-JS', 'Bootstrap'],
                'Build Tools' => ['Vite', 'Webpack', 'Laravel Mix'],
                'Progressive Enhancement' => ['PWAs', 'Offline-First', 'Performance Budgeting'],
            ],

            SkillCategory::UI_UX_DESIGN->value => [
                'Design Tools' => ['Figma', 'Adobe XD', 'Sketch'],
                'User Research' => ['User Personas', 'Journey Mapping', 'Usability Testing'],
                'Design Systems' => ['Component Libraries', 'Style Guides', 'Design Tokens'],
                'Accessibility' => ['WCAG 2.1', 'Screen Readers', 'Keyboard Navigation'],
            ],

            SkillCategory::DEVOPS_INFRASTRUCTURE->value => [
                'Containers' => ['Docker', 'Docker Compose', 'Kubernetes'],
                'Cloud Platforms' => ['AWS', 'DigitalOcean', 'Forge & Envoyer'],
                'CI/CD' => ['GitHub Actions', 'GitLab CI', 'Automated Testing'],
                'Monitoring' => ['Application Logging', 'Performance Metrics', 'Error Tracking'],
            ],
        ];
    }

    /**
     * Get skills for a specific category.
     *
     * @return array<string, array<int, string>>|null
     */
    public function getSkillsByCategory(SkillCategory $category): ?array
    {
        return $this->getTechnicalSkills()[$category->value] ?? null;
    }

    // =========================================================================
    // DEVELOPMENT PRINCIPLES
    // =========================================================================

    /**
     * Retrieve core development principles and methodologies.
     *
     * @return array<string, array<int, string>>
     */
    public function getDevelopmentPrinciples(): array
    {
        return [
            'code_quality' => [
                'Test-Driven Development',
                'Clean Architecture',
                'SOLID Principles',
                'Design Patterns',
            ],
            'collaboration' => [
                'Agile Methodology',
                'Code Reviews',
                'Pair Programming',
                'Technical Documentation',
            ],
            'user_focus' => [
                'User-Centered Design',
                'Performance First',
                'Progressive Enhancement',
                'Continuous Feedback',
            ],
        ];
    }

    // =========================================================================
    // PROJECTS
    // =========================================================================

    /**
     * Retrieve personal and hobby projects.
     *
     * @return iterable<string, Project>
     */
    public function getHobbyProjects(): iterable
    {
        yield 'iZambezi CSS' => new Project(
            name: 'iZambezi CSS',
            description: 'Custom CSS framework for rapid UI development',
            url: 'https://izambezi.vercel.app',
            stack: ['CSS', 'SCSS', 'JavaScript'],
        );
    }

    /**
     * Retrieve currently active projects.
     *
     * @return iterable<string, Project>
     */
    public function getCurrentProjects(): iterable
    {
        yield 'E-commerce Platform' => new Project(
            name: 'E-commerce Platform',
            description: 'Scalable e-commerce solution with microservices architecture',
            stack: ['Laravel', 'Vue.js', 'MySQL', 'Redis'],
            features: ['Microservices', 'Real-time Analytics', 'Payment Integration'],
        );

        yield '263tickets Internal Applications' => new Project(
            name: '263tickets Internal Applications',
            description: 'Internal ticketing and management systems',
            stack: ['Livewire', 'Alpine.js', 'PostgreSQL', 'AWS'],
            features: ['Multi-tenancy', 'API-first', 'Automated Deployment'],
        );
    }

    /**
     * Retrieve notable professional work experience.
     *
     * @return iterable<int, array{role: string, company: string, website: string}>
     */
    public function getNotableWorks(): iterable
    {
        yield [
            'role' => 'Front-End Developer',
            'company' => 'startupAZ',
            'website' => 'https://www.suaz.co.uk/',
        ];

        yield [
            'role' => 'Systems Developer',
            'company' => '263tickets',
            'website' => 'https://263tickets.com',
        ];
    }

    // =========================================================================
    // AVAILABILITY
    // =========================================================================

    /**
     * Check availability for collaboration opportunities.
     */
    public function isAvailableForCollaboration(): bool
    {
        return $this->availability->allowsCollaboration();
    }

    /**
     * Check availability for full-time opportunities.
     */
    public function isOpenToWork(): bool
    {
        return $this->availability === AvailabilityStatus::OPEN_TO_OPPORTUNITIES;
    }

    /**
     * Get current availability status.
     */
    public function getAvailabilityStatus(): AvailabilityStatus
    {
        return $this->availability;
    }

    // =========================================================================
    // CONTACT
    // =========================================================================

    /**
     * Retrieve all contact methods.
     */
    public function getContactInfo(): ContactInfo
    {
        return new ContactInfo(
            email: 'jonesmugabe08@gmail.com',
            linkedin: 'linkedin.com/in/johnmugabe',
            github: 'github.com/johnmugabe',
            portfolio: 'johnmugabe.mystrikingly.com',
        );
    }

    // =========================================================================
    // SERIALIZATION
    // =========================================================================

    /**
     * Convert the profile to an array representation.
     *
     * @return array<string, mixed>
     */
    public function toArray(): array
    {
        return [
            'name' => $this->name,
            'title' => $this->title,
            'location' => $this->location->toArray(),
            'years_of_experience' => self::YEARS_OF_EXPERIENCE,
            'certifications' => $this->certifications,
            'current_focus' => self::CURRENT_FOCUS,
            'philosophy' => self::DEVELOPMENT_PHILOSOPHY,
            'skills' => $this->getTechnicalSkills(),
            'principles' => $this->getDevelopmentPrinciples(),
            'contact' => $this->getContactInfo()->toArray(),
            'availability' => [
                'open_to_work' => $this->isOpenToWork(),
                'open_to_collaboration' => $this->isAvailableForCollaboration(),
                'status' => $this->availability->value,
            ],
        ];
    }

    /**
     * Convert to JSON representation.
     */
    public function toJson(int $flags = JSON_PRETTY_PRINT): string
    {
        return json_encode($this->toArray(), $flags | JSON_THROW_ON_ERROR);
    }
}

# Hey, I am John Mugabe!

[![Website](https://img.shields.io/badge/Website-Portfolio-blue?style=flat-square&logo=google-chrome)](https://johnmugabe.mystrikingly.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/johnmugabe)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/johnmugabe8)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat-square&logo=gmail)](mailto:jonesmugabe08@gmail.com)

## A Little About Me In Source Code

```php

<?php

declare(strict_types=1);

/**
 * John Mugabe - Full-Stack PHP Developer
 * 
 * 8+ years building scalable web applications in the Laravel ecosystem.
 * Passionate about clean code, TDD, and exceptional user experiences.
 *
 * @author  John Mugabe <jonesmugabe08@gmail.com>
 * @see     https://github.com/johnmugabe
 * @see     https://johnmugabe.mystrikingly.com
 */
final readonly class AboutMe
{
    public string $name = 'John Mugabe';
    public string $title = 'Full-Stack PHP Developer';
    public string $location = 'Harare, Zimbabwe';
    public string $timezone = 'Africa/Harare';
    public int $yearsOfExperience = 8;
    public string $currentFocus = 'Building scalable web applications with exceptional UX';
    public string $philosophy = 'Clean code, tested features, and delighted users';
    public bool $openToWork = true;
    public bool $openToCollaboration = true;

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
            'Databases'       => ['MySQL', 'PostgreSQL', 'Redis', 'Elasticsearch'],
            'API Development' => ['REST', 'GraphQL', 'WebSocket Services'],
            'Performance'     => ['Caching Strategies', 'Queue Systems', 'Load Optimization'],
        ];
    }

    public function frontendSkills(): array
    {
        return [
            'JavaScript'              => ['Vue.js 3', 'React', 'TypeScript', 'Alpine.js'],
            'Styling'                 => ['Tailwind CSS', 'SASS/SCSS', 'CSS-in-JS', 'Bootstrap'],
            'Build Tools'             => ['Vite', 'Webpack', 'Laravel Mix'],
            'Progressive Enhancement' => ['PWAs', 'Offline-First', 'Performance Budgeting'],
        ];
    }

    public function designSkills(): array
    {
        return [
            'Design Tools'   => ['Figma', 'Adobe XD', 'Sketch'],
            'User Research'  => ['User Personas', 'Journey Mapping', 'Usability Testing'],
            'Design Systems' => ['Component Libraries', 'Style Guides', 'Design Tokens'],
            'Accessibility'  => ['WCAG 2.1', 'Screen Readers', 'Keyboard Navigation'],
        ];
    }

    public function devOpsSkills(): array
    {
        return [
            'Containers'       => ['Docker', 'Docker Compose', 'Kubernetes'],
            'Cloud Platforms'  => ['AWS', 'DigitalOcean', 'Forge & Envoyer'],
            'CI/CD'            => ['GitHub Actions', 'GitLab CI', 'Automated Testing'],
            'Monitoring'       => ['Application Logging', 'Performance Metrics', 'Error Tracking'],
        ];
    }

    public function developmentPrinciples(): array
    {
        return [
            'Code Quality'  => ['Test-Driven Development', 'Clean Architecture', 'SOLID Principles', 'Design Patterns'],
            'Collaboration' => ['Agile Methodology', 'Code Reviews', 'Pair Programming', 'Technical Documentation'],
            'User Focus'    => ['User-Centered Design', 'Performance First', 'Progressive Enhancement', 'Continuous Feedback'],
        ];
    }

    public function experience(): array
    {
        return [
            [
                'role'    => 'Systems Developer',
                'company' => '263tickets',
                'website' => 'https://263tickets.com',
                'work'    => 'Internal ticketing and management systems with multi-tenancy, API-first architecture, and automated deployment',
                'stack'   => ['Livewire', 'Alpine.js', 'PostgreSQL', 'AWS'],
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
                'name'        => 'E-commerce Platform',
                'description' => 'Scalable e-commerce solution with microservices architecture',
                'stack'       => ['Laravel', 'Vue.js', 'MySQL', 'Redis'],
                'features'    => ['Microservices', 'Real-time Analytics', 'Payment Integration'],
            ],
            [
                'name'        => '263tickets Internal Applications',
                'description' => 'Internal ticketing and management systems',
                'stack'       => ['Livewire', 'Alpine.js', 'PostgreSQL', 'AWS'],
                'features'    => ['Multi-tenancy', 'API-first', 'Automated Deployment'],
            ],
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
        ];
    }
}

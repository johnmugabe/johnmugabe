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
    
    use App\Skills\{
        Backend,
        Frontend,
        DesignExpertise,
        DevOps,
        DevelopmentPrinciples
    };
    
    /**
     * Seasoned Full-Stack Developer with 8+ years experience building scallable web applications using
     * Laravel ecosystem. Passionate about clean code, TDD and exploring nw technologies.
     * 
     * @author John Mugabe
     * @license MIT
     * @version 1.0
     */
    final class AboutMe extends Developer implements 
        BackendTechnologies,
        FrontendTechnologies, 
        DesignExpertise,
        DevOpsTools,
        DevelopmentPrinciples
    {
        private const string CURRENT_FOCUS = 'Building scalable web applications with exceptional UX';
        private const string DEVELOPMENT_PHILOSOPHY = 'Clean code, tested features, and delighted users';
        
        public function __construct(
            private string $name = 'John Mugabe',
            private string $title = 'Full-Stack PHP Developer',
            private Location $location = new Location('Harare, Zimbabwe'),
            private array $certifications = ['UI/UX Certified', 'Front-End Development', 'Mobile Development']
        ) {}
        
        public function getTechnicalSkills(): array
        {
            return [
                'backend_architecture' => [
                    'PHP 8.x' => ['Laravel', 'Symfony', 'Livewire'],
                    'Databases' => ['MySQL', 'PostgreSQL', 'Redis', 'Elasticsearch'],
                    'API_Development' => ['REST', 'GraphQL', 'WebSocket Services'],
                    'Performance' => ['Caching Strategies', 'Queue Systems', 'Load Optimization']
                ],
                
                'frontend_engineering' => [
                    'JavaScript' => ['Vue.js 3', 'React', 'TypeScript', 'Alpine.js'],
                    'Styling' => ['Tailwind CSS', 'SASS/SCSS', 'CSS-in-JS', 'Bootstrap'],
                    'Build_Tools' => ['Vite', 'Webpack', 'Laravel Mix'],
                    'Progressive_Enhancement' => ['PWAs', 'Offline-First', 'Performance Budgeting']
                ],
                
                'ui_ux_design' => [
                    'Design_Tools' => ['Figma', 'Adobe XD', 'Sketch'],
                    'User_Research' => ['User Personas', 'Journey Mapping', 'Usability Testing'],
                    'Design_Systems' => ['Component Libraries', 'Style Guides', 'Design Tokens'],
                    'Accessibility' => ['WCAG 2.1', 'Screen Readers', 'Keyboard Navigation']
                ],
                
                'devops_infrastructure' => [
                    'Containers' => ['Docker', 'Docker Compose', 'Kubernetes'],
                    'Cloud_Platforms' => ['AWS', 'DigitalOcean', 'Forge & Envoyer'],
                    'CI_CD' => ['GitHub Actions', 'GitLab CI', 'Automated Testing'],
                    'Monitoring' => ['Application Logging', 'Performance Metrics', 'Error Tracking']
                ]
            ];
        }
        
        public function getDevelopmentPrinciples(): array
        {
            return [
                'code_quality' => [
                    'Test-Driven Development',
                    'Clean Architecture',
                    'SOLID Principles',
                    'Design Patterns'
                ],
                'collaboration' => [
                    'Agile Methodology',
                    'Code Reviews',
                    'Pair Programming',
                    'Technical Documentation'
                ],
                'user_focus' => [
                    'User-Centered Design',
                    'Performance First',
                    'Progressive Enhancement',
                    'Continuous Feedback'
                ]
            ];
        }

        public function hobbyprojects(): iterable
        {
            yield 'iZambezi CSS' => [
                'website' => 'https://izambezi.vercel.app'
            ];
            
            yield 'Systems Developer' => [
                'company' => '263tickets',
                'website' => 'https://263tickets.com'
            ];
        }
        
        public function getCurrentProjects(): iterable
        {
            yield 'E-commerce Platform' => [
                'stack' => ['Laravel', 'Vue.js', 'MySQL', 'Redis'],
                'features' => ['Microservices', 'Real-time Analytics', 'Payment Integration']
            ];
            
            yield '263tickets Internal Applications' => [
                'stack' => ['Livewire', 'Alpine.js', 'PostgreSQL', 'AWS'],
                'features' => ['Multi-tenancy', 'API-first', 'Automated Deployment']
            ];
        }

        public function otherNotableWorks(): iterable
        {
            yield 'Front-End Development => [
                'company' => 'startupAZ,
                'website' => 'https://www.suaz.co.uk/'
            ];
            
            yield 'Systems Developer' => [
                'company' => '263tickets',
                'website' => 'https://263tickets.com'
            ];
        }
        
        public function isAvailableForCollaboration(): bool
        {
            return true;
        }
        
        public function getContactMethods(): array
        {
            return [
                'email' => 'jonesmugabe08@gmail.com',
                'linkedin' => 'linkedin.com/in/johnmugabe',
                'github' => 'github.com/johnmugabe',
                'portfolio' => 'johnmugabe.mystrikingly.com'
            ];
        }
        
    }

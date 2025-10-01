# Hello, I'm John Mugabe!

[![Website](https://img.shields.io/badge/Website-YourPortfolio-blue?style=flat-square&logo=google-chrome)](https://johnmugabe.mystrikingly.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/johnmugabe)
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/johnmugabe8)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat-square&logo=gmail)](mailto:jonesmugabe08@gmail.com)

## A Little About Me

```php
<?php

class AboutMe extends Developer
{
    public string $name = "John Mugabe";
    public string $title = "Full-Stack PHP Developer";
    public string $currentFocus = "Build it solid, make it stunning, and for the love of all that is holy, ensure the "Submit" button doesn't break the space-time continuum. Let's create something amazing that won't keep you up at night.";
    public string $location = "[Harare, Zimbabwe]";
    
    public function getSkills(): array
    {
        return [
        'backend' => ['PHP 8.x', 'Laravel', 'Livewire', 'Eloquent ORM', 'API Development (REST, GraphQL)','MySQL', 'PostgreSQL', 'Redis', 'Queues & Jobs', 'WebSockets', 'Payment Integration'],
        'frontend' => ['JavaScript (ES6+)', 'TypeScript', 'Vue.js 3', 'React', 'Alpine.js', 'Tailwind CSS', 'Bootstrap', 'HTML5/CSS3', 'SASS/SCSS', 'Webpack', 'Vite'],
        'ui_ux_design' => ['User Experience (UX) Design', 'User Interface (UI) Design', 'Figma', 'Adobe XD', 'Prototyping', 'Wireframing', 'Design Systems', 'Responsive Design', 'Mobile-First Approach', 'Accessibility   (a11y)'],
    'devops_cloud' => [
        'Docker',
        'AWS (EC2, S3, RDS)',
        'Forge & Envoyer',
        'CI/CD Pipelines',
        'Nginx',
        'Linux Server Administration',
        'GitHub Actions',
        'Shell Scripting',
        'Monitoring & Logging'
    ],
    'tools_workflow' => [
        'Git & GitHub',
        'VS Code',
        'PHPStorm',
        'Composer',
        'NPM/Yarn',
        'Postman',
        'Telescope',
        'Debugbar'
    ],
    'testing_quality' => [
        'PHPUnit',
        'Pest',
        'Test-Driven Development (TDD)',
        'Feature & Unit Testing',
        'Browser Testing',
        'Code Quality Tools',
        'Performance Optimization'
    ],
    'methodologies' => [
        'Agile/Scrum',
        'Git Flow',
        'API-First Development',
        'Mobile-First Development',
        'Progressive Enhancement'
    ]
];
    }
    
    public function sayHello(): string
    {
        return "Thanks for stopping by my GitHub! 👋";
    }
}

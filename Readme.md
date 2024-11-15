### <img src="https://miro.medium.com/v2/resize:fit:1000/format:webp/1*Gbi_XNOkPFbWkIkJC7LnBQ.gif" width="50"> Hello I'm Mirsaidov Umed 
```php

<?php

namespace MirsaidovUmed;

interface ProfileDisplayInterface
{
    public function displayProfile(): string;
}

class Programmer
{
    private array $info;

    public function __construct(array $info)
    {
        $this->info = $info;
    }

    public function getInfo(): array
    {
        return $this->info;
    }
}

class ProgrammerProfileDisplay implements ProfileDisplayInterface
{
    private Programmer $programmer;

    public function __construct(Programmer $programmer)
    {
        $this->programmer = $programmer;
    }

    public function displayProfile(): string
    {
        $info = $this->programmer->getInfo();
        $profile = "Programmer since high school (11th grade).\n";
        $profile .= "Backend developer with experience in PHP and Golang.\n";

        if (!empty($info['projects'])) {
            $profile .= "Projects:\n";
            foreach ($info['projects'] as $project) {
                $profile .= "- {$project}\n";
            }
        }

        if (!empty($info['skills'])) {
            $profile .= "Skills:\n";
            foreach ($info['skills'] as $skill) {
                $profile .= "- {$skill}\n";
            }
        }
        return $profile;
    }
}

$programmer = new Programmer([
    'projects' => ['CloudStorage', 'SUP', 'UrlShortener'],
    'skills' => ['PHP', 'Golang', 'MySQL', 'Postgres', 'Laravel', 'Symfony']
]);

$profileDisplay = new ProgrammerProfileDisplay($programmer);
echo $profileDisplay->displayProfile();
```

### :hammer_and_wrench: Languages and Tools :
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/go/go-original-wordmark.svg" title="Go" alt="Golang" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/php/php-original.svg" title="php" alt="php" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/laravel/laravel-line-wordmark.svg" title="laravel" alt="laravel" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/symfony/symfony-original-wordmark.svg" title="symfony" alt="symfony" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/wordpress/wordpress-original.svg" title="WordPress" alt="WordPress" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/composer/composer-original.svg" title="composer" alt="composer" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/vscode/vscode-original.svg" title="VScode" alt="VScode" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/phpstorm/phpstorm-original.svg" title="PHPStorm",alt="PHPStorm" width="40" height="40"/>&nbsp; 
  <img src="https://github.com/devicons/devicon/blob/master/icons/goland/goland-original.svg" title="Goland" alt="Goland" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postgresql/postgresql-original.svg" title="PostgreSQL" alt="PostgreSQL" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL" alt="MySQL " width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postman/postman-original.svg" title="Postman" alt="Postman" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original-wordmark.svg" title="github" alt="github" width="40" height="40"/>&nbsp;
</div>

### Top Languages :
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MirsaidovUmed&langs_count=8&theme=tokyonight)

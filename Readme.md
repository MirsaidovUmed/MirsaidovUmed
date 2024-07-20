### <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExZXZidGxtczZvZXF6YTVrOWxoZ3JtbWJzbGQ1Zmo0eGs3NDc2ZjhmeSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/QAsHga1AB6dIGUsui6/giphy.webp" width="50"> Hello I'm Mirsaidov Umed 
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
    'projects' => ['FileHosting', 'SUP', 'UrlShortener'],
    'skills' => ['PHP', 'Golang', 'MySQL', 'Postgres', 'Laravel']
]);

$profileDisplay = new ProgrammerProfileDisplay($programmer);
echo $profileDisplay->displayProfile();
```

### :hammer_and_wrench: Languages and Tools :
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/go/go-original-wordmark.svg" title="Go" alt="Golang" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/goland/goland-original.svg" title="Goland" alt="Goland" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postgresql/postgresql-original.svg" title="PostgreSQL" alt="PostgreSQL" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postman/postman-original.svg" title="Postman" alt="Postman" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL" alt="MySQL " width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/php/php-original.svg" title="php" alt="php" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/composer/composer-original.svg" title="composer" alt="composer" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original-wordmark.svg" title="github" alt="github" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/vscode/vscode-original.svg" title="VScode" alt="VScode" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/jetbrains/jetbrains-original.svg" title="jetbrains" alt="jetbrains" width="40" height="40"/>&nbsp;
    <img src="https://github.com/devicons/devicon/blob/master/icons/laravel/laravel-line-wordmark.svg" title="laravel" alt="laravel" width="40" height="40"/>&nbsp;
</div>

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MirsaidovUmed&langs_count=8&theme=tokyonight)

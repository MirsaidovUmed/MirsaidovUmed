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

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs?username=MirsaidovUmed&hide=html&show_icons=true&locale=en&theme=tokyonight)

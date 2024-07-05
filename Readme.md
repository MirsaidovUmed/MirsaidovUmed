### <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExZXZidGxtczZvZXF6YTVrOWxoZ3JtbWJzbGQ1Zmo0eGs3NDc2ZjhmeSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/QAsHga1AB6dIGUsui6/giphy.webp&ct=s" width="50"
Hello I'm Mirsaidov Umed 

```php

<?php



namespace MirsaidovUmed;



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



    public function displayProfile(): string

    {

        $profile = "Programmer since high school (11th grade).\n";

        $profile .= "Backend developer with experience in PHP and Golang.\n";



        if (!empty($this->info['projects'])) {

            $profile .= "Projects:\n";

            foreach ($this->info['projects'] as $project) {

                $profile .= "- {$project}\n";

            }

        }



        if (!empty($this->info['skills'])) {

            $profile .= "Skills:\n";

            foreach ($this->info['skills'] as $skill) {

                $profile .= "- {$skill}\n";

            }

        }



        return $profile;

    }

}



$programmer = new Programmer([

    'projects' => ['FileHosting', 'SUP', 'UrlShotener'],

    'skills' => ['PHP', 'Golang', 'MySQL', 'Postgres', 'Laravel']

]);



echo $programmer->displayProfile();

```

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs?username-MirsaidovUmed&hide=html&show_icons=true&locale=en&theme=tokyonight)
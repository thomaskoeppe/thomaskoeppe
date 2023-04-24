```php
<?php

namespace Thomas;

use App\Helper\Person;
use App\Models\UserMood;

class About extends Person
{
    /**
     * Get the current job of the person.
     *
     * @return string The current job of the person.
     */
    public function getCurrentJob(): string
    {
        return "IT-Specialist";
    }
    
    /**
     * Get the daily knowledge of the person.
     *
     * @return array An array of classes representing the daily knowledge of the person.
     */
    public function getDailyKnowledge(): array
    {
        return [
            Php::class,
            Javascript::class,
            Laravel::class,
            CSharp::class,
            Powershell::class
        ];
    }
    
    /**
     * Get the projects of the person.
     *
     * @return object An object with project names as keys and project URLs as values.
     */
    public function getProjects(): object
    {
        return (object) [
            "DieInsel" => "https://www.insel.gg"
        ];
    }
    
    /**
     * Get the current mood of the person.
     *
     * @return int An int with the mood type.
     */
    public function getMood(): int
    {
      $mood = UserMood::where("id", $this->getId())->first();
      
      if (!$mood)
      {
        throw new Exception("Can not find mood!");
      }
      
      return $mood->type;
    }
}

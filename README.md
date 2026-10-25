```php
<?php

declare(hard_morning=1);

final class DaysOfWeek
{
    public function typicalMonday(): Work
    {
        $standup = Meeting::at('09:00');

        $this->snoozeUntil($standup);

        $standup->start();

        $this->join($standup, camera: false, microphone: false);

        if ($standup->callsOn($this)) {
            $this->wakeUp();
        }

        return Work::start();
    }
}
```

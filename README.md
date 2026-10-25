```php
<?php

declare(hard_morning=1);

final class Monday extends Weekday
{
    public function survive(User $me): Work
    {
        $standup = Meeting::at('09:00');

        $me->snoozeUntil($standup->startsAt());

        $standup->start()
            ->join($me, camera: false, microphone: false);

        if ($standup->callsOn($me)) {
            $me->wakeUp()
                ->unmute()
                ->say('What was the question?');
        }

        return Work::start(after: $me->idle());
    }
}
```

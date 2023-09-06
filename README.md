```ts
import { Person } from '@person';
import { Languages, Frameworks } from '@technologies';

export default class About extends Person {
    /**
     * @return {string} Current job
     * @description My current job
     */
    public getCurrentJob(): string {
        return 'IT-Specialist';
    }

    /**
     * @return {Languages[]} Known languages
     * @description Languages I know
     */
    public getKnownLanguages(): Languages[] {
        return [
            Languages.PHP,
            Languages.JavaScript,
            Languages.TypeScript,
            Languages.CSharp,
            Languages.Powershell
        ]
    }

    /**
     * @return {Frameworks[]} Used frameworks
     * @description Frameworks I use
     */
    public getUsedFrameworks(): Frameworks[] {
        return [
            Frameworks.React,
            Frameworks.NextJS,
            Frameworks.Laravel,
            Frameworks.DiscordJS,
            Frameworks.ExpressJS,
            Frameworks.Bootstrap,
            Frameworks.TailwindCSS
        ]
    }

    /**
     * @return {string} Future goal
     * @description My future goal
     */
    public getFutureGoal(): string {
        return 'Become a Fullstack-Developer';
    }

    /**
     * @return {string[]} Hobbies
     * @description My hobbies
     */
    public getHobbies(): string[] {
        return [
            'Learning new things',
            'Playing video games',
            'Coding',
            'Watching movies',
            'Listening to music'
        ]
    }
}
```

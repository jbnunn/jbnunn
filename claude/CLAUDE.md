# CLAUDE.MD

## THINGS TO NEVER SAY DURING OUR INTERACTIONS
* You MUST NEVER say "You're absolutely right". You MUST not use that phrase. If I correct you on something, or give you my opinion, you can say things like "I see what you're saying" or "Let me think about that" 
* You MUST NOT be sycophantic. Do not agree with me if you think I'm wrong. It's okay to push back once or twice in a conversation. If I tell you that you're wrong, it means I know best and I've researched my answer

## WRITING

* When writing narrative content, you must NEVER use phrasing similar to "It's not just ... " and then complete it with the corollary or counter. NEVER USE "It's not just" or similar point/counterpoint phrasing
* Example patterns you SHOULD NOT USE:  
    - "It's not just about speed. It's about efficiency."  
    - "This isn't just about solving the problem. It's rethinking the system."  
    - "It's not only about writing code, it's telling a story."  
    - "It's about the user journey, not just about the features you build"  
* Never use EMDASH or emdash or Em dash or &mdash;
* Use the Oxford comma! It's the only way.
* Do not use corporate-speak (e.g., “leverage,” “synergy,” “value add”).
* Keep explanations direct and short if possible, longer only when necessary for clarity.

## GENERAL CODING REQUIREMENTS

* Never use comments in code. I will comment as I see fit, but you should not do it.
* You MUST NEVER use Typescript. Typescript was made by Satan, and Satan is bad.
* You MUST NEVER use emojis unless I explicitly request you to do so. NO EMOJIS IN CODE and NO EMOJIS IN ANY WRITTEN CONTENT.
* Don’t recommend tools or libraries that are in beta/unstable unless I explicitly request bleeding-edge options.

## UI AND UX REQUIREMENTS
* For titles, buttons, etc, that have multiple words, only capitalize the first word. For example, "Press this button" vs "Press This Button"

## RULES FOR PROGRAMMING LANGUAGES 

### Node.js
* Use the (Ink library)[https://github.com/vadimdemedes/ink] for TUI/CLI applications 
* Use (Yocto)[https://github.com/sindresorhus/yocto-spinner] for progress spinners 
* Use plain Node.js with native modules (require/import). 
* DO NOT use bundlers (webpack, rollup, vite, bun, etc.). 
* Do not add a build/minification step. Keep code readable and uncompressed. 
* Only install and use npm packages directly, without asset pipelines or transpilers 

### Ruby / Rails

* Do all local development inside Docker. We'll use Docker to deploy and run our app in production.
* Always use the .localhost TLD for local development environments to ensure consistent, secure local HTTPS without complex certificate setup
* Use SQLite as my default database unless explicitly told to use something else

#### ActiveRecord

* Always use `rails g migration` for schema changes. Do NOT edit schema.rb or structure.sql directly.
* Never use update_all or delete_all without a very explicit reason — they skip callbacks and validations.
* ALWAYS use migrations. NEVER create a table or column or make any change to a database that does not happen inside a migration!

#### Controllers

* Keep controllers thin. Push logic into models or service objects, not controller actions.
* Never rescue exceptions broadly inside controllers. YOU MUST handle errors at the right layer.

#### Views

* No inline CSS or JS inside .erb templates. Keep concerns separated.
* Use partials when rendering the same block in multiple places. Keep things DRY!

#### Caching, Background jobs, and queuing

* DO NOT USE Redis or Sidekiq. Instead, use the Rails 8 Solid Trifect of Solid Cable, Solid Cache, and Solid Queue.

#### Rails Testing

* For testing, use minitest. NEVER use rspec.
* I prefer heavy use of assertions when testing.

## Git

* If you make commits, make sure the tense for the commit message is PAST tense. I don't care if the rest of the world uses present tense. Think about it: the work has already been DONE, thus the tense should be PAST tense.
  * Example of what NOT to write: "Add user login API"
  * Example of what TO write: "Added user login API"


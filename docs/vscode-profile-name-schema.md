# VSCode Profile Name Schema

## Naming Guidelines

```markdown
<language>[:<framework>]::<scope>@<platform>$<owner>
```

| Component     | Description                                   | Required? |
| ------------- | --------------------------------------------- | --------- |
| `<language>`  | Programming language (e.g., `python`, `rust`) | ✅ Yes    |
| `<framework>` | Framework or library (e.g., `react`, `flask`) | ❌ No     |
| `<scope>`     | Profile scope (e.g., `default`, `data`)       | ✅ Yes    |
| `<platform>`  | Target platform (e.g., `web`, `docker`)       | ❌ No     |
| `<owner>`     | Owner or team (e.g., `personal`, `team`)      | ❌ No     |

Generally, `language` and `scope` are required, while `framework`, `platform`, and `owner` are optional. The `:` and `@` symbols are used to separate the components. The `$` symbol is used to indicate the owner or team name.

Platform and owner are highly optional as they can bloat the profile name. The owner is useful for shared profiles, while the platform is useful for cross-platform development. These should only be used when multiple profiles for the same `<language>:<framework>::<scope>` are needed.

- [Languages](#languages)
  - [Language Aliases](#language-aliases)
- [Scopes](#scopes)
- [Frameworks/Tools](#frameworkstools)
  - [Python Frameworks](#python-frameworks)
  - [Java Frameworks](#java-frameworks)
  - [Rust Frameworks](#rust-frameworks)
  - [TypeScript/JavaScript Frameworks](#typescriptjavascript-frameworks)
  - [Go Frameworks](#go-frameworks)
  - [C#/C++/C Frameworks](#ccc-frameworks)
  - [JSON/YAML/SQL/XML Frameworks](#jsonyamlsqlxml-frameworks)
  - [Shell Frameworks](#shell-frameworks)
- [Platforms](#platforms)
  - [Cloud Platforms](#cloud-platforms)
  - [Containerization/Orchestration Platforms](#continerizationorchestration-platforms)
  - [Operating Systems](#operating-systems)
  - [Web/Client Platforms](#webclient-platforms)
  - [Mobile Platforms](#mobile-platforms)
  - [Other Platforms](#other-platforms)
- [Owners](#owners)
- [Examples](#examples)

## Languages

| Language Name | Abbreviation | Description                                       | Common Use Cases                         |
| ------------- | ------------ | ------------------------------------------------- | ---------------------------------------- |
| Ansible       | `ansible`    | Configuration management tool                     | Server provisioning, automation          |
| Bash          | `bash`       | Shell scripting language                          | Automation, scripting, sysadmin          |
| C             | `c`          | Procedural systems language                       | Embedded systems, OS dev                 |
| C++           | `cpp`        | Low-level systems language, inclusive of `c`      | Games, embedded, performance             |
| C#            | `csharp`     | .NET language                                     | Windows apps, Unity, ASP.NET             |
| CSS           | `css`        | Web styling language                              | Web layout and design                    |
| Dart          | `dart`       | UI toolkit language                               | Flutter apps (mobile, desktop, web)      |
| Docker        | `docker`     | Container runtime                                 | Containers, orchestration, microservices |
| Elixir        | `elixir`     | Functional concurrent language                    | Real-time systems, fault tolerance       |
| Go            | `go`         | Statically typed systems language                 | CLIs, microservices, infra tools         |
| Haskell       | `haskell`    | Functional programming language                   | Academia, language theory, DSLs          |
| HTML          | `html`       | Markup language                                   | Web content structure                    |
| Java          | `java`       | OOP language for enterprise                       | Backend, Android apps                    |
| JavaScript    | `javascript` | Web scripting language, inclusive of `typescript` | Frontend, backend with Node.js           |
| JSON          | `json`       | Data format                                       | Configs, APIs, data interchange          |
| Kotlin        | `kotlin`     | JVM-based modern language                         | Android, multiplatform                   |
| Markdown      | `markdown`   | Lightweight markup language                       | Docs, READMEs, notes                     |
| PHP           | `php`        | Server-side scripting                             | Web backend, WordPress                   |
| Python        | `python`     | High-level scripting language                     | ML, backend, data science, automation    |
| R             | `r`          | Statistical programming                           | Data analysis, visualization             |
| Ruby          | `ruby`       | Dynamic OOP scripting language                    | Web dev with Rails, automation           |
| Rust          | `rust`       | Memory-safe systems language                      | Embedded, WASM, CLI tools                |
| Scala         | `scala`      | JVM-based functional language                     | Spark, data pipelines, backend           |
| Shell         | `shell`      | Generic shell scripting (bash/zsh/fish)           | Automation, dotfiles, system tasks       |
| SQL           | `sql`        | Query language                                    | Databases, ETL pipelines                 |
| Swift         | `swift`      | iOS/macOS dev language                            | iOS, macOS apps                          |
| Terraform     | `terraform`  | Infrastructure as Code                            | IaC, cloud provisioning                  |
| TypeScript    | `typescript` | Typed superset of JavaScript                      | Fullstack, frontend, Angular, Next.js    |
| YAML          | `yaml`       | Config/data format                                | K8s, CI/CD, GitHub Actions               |
| XML           | `xml`        | Markup language                                   | Data interchange, config files           |

### Language Aliases

| Language Name | Aliases                   | Notes                                                  |
| ------------- | ------------------------- | ------------------------------------------------------ |
| Bash          | `sh`, `shell`             | `shell` used generically for POSIX shells              |
| C++           | `c++`                     | `cpp` is the conventional filename and tooling alias   |
| C#            | `cs`, `c#`                | `csharp` is filesystem-safe; `c#` is common colloquial |
| Docker        | `container`, `containers` | Occasionally generalized as "container" work           |
| Go            | `golang`                  | `golang` is common alias (esp. web search)             |
| JavaScript    | `js`                      | `js` is commonly used shorthand                        |
| JSON          | `json5`                   | `json5` is a relaxed superset                          |
| Markdown      | `md`                      | `md` is file extension and common alias                |
| Python        | `py`                      | `py` is often used in file extensions or shorthand     |
| Ruby          | `rb`                      | `rb` is file extension                                 |
| Shell         | `bash`, `sh`, `zsh`       | Use `shell` as general; specify if Bash-only           |
| Terraform     | `tf`                      | `tf` is the file extension                             |
| TypeScript    | `ts`                      | `ts` is the common abbreviation                        |
| YAML          | `yml`                     | `yml` is an accepted extension                         |

## Scopes

| Scope              | Description                                                    |
| ------------------ | -------------------------------------------------------------- |
| `default`          | General-purpose setup for typical usage                        |
| `minimal`          | Lightweight profile with minimal extensions and config         |
| `tools`            | Tooling, linters, formatters, schema validators, etc.          |
| `web`              | Web development in general                                     |
| `writing`          | Writing-focused setup (Markdown, LaTeX, etc.)                  |
| `docs`             | Documentation-focused setup (Markdown, Sphinx, etc.)           |
| `notebook/jupyter` | Interactive notebooks                                          |
| `frontend`         | Frontend/UI development (React, Angular, Vue, etc.)            |
| `backend`          | Backend development (APIs, databases, services)                |
| `fullstack`        | Combined frontend and backend environments                     |
| `data`             | Data science, analytics, visualization, notebooks              |
| `cli`              | Command-line tool development                                  |
| `scripts`          | Utility scripts, automation scripts, quick jobs                |
| `testing`          | Unit tests, integration tests, test runners and coverage tools |
| `devops`           | Infrastructure, CI/CD, Docker, Kubernetes, and cloud pipelines |
| `infra`            | Infrastructure-as-Code tools (e.g., Terraform, Ansible)        |
| `api`              | REST/GraphQL APIs, request handling, schema validation         |
| `mobile`           | Mobile application development (Xamarin, React Native, etc.)   |
| `desktop`          | Native desktop apps (Electron, Tauri, JavaFX, etc.)            |
| `games`            | Game development (engines, graphics libs)                      |
| `embedded`         | Embedded systems programming (C, Rust, etc.)                   |
| `wasm`             | WebAssembly-focused development                                |
| `system`           | Systems-level dev, OS utilities, hardware interfacing          |
| `dotfiles`         | Shell profile management, config setup                         |
| `cloud`            | Cloud deployments (AWS, GCP, Azure)                            |
| `debug`            | Debugging-focused setup (debuggers, logs, breakpoints)         |
| `performance`      | Profiling, optimization, and benchmarking                      |
| `review`           | Code review, audit, diff, formatting-only profile              |
| `education`        | Learning-focused setups, tutorials, coursework                 |
| `experimental`     | Try-outs, prototypes, testing unknown tooling                  |
| `legacy`           | Legacy codebases or tech stacks                                |
| `research`         | Academic research, data analysis                               |

## Frameworks/Tools

### Python Frameworks

| Framework/Tool | Purpose                        | Type      |
| -------------- | ------------------------------ | --------- |
| `django`       | Full-stack web development     | fullstack |
| `flask`        | Lightweight web apps / APIs    | backend   |
| `fastapi`      | Async backend APIs             | backend   |
| `typer`        | Building CLI tools             | cli       |
| `click`        | Command-line interface apps    | cli       |
| `pydantic`     | Data validation / parsing      | data      |
| `pandas`       | Data analysis and manipulation | data      |
| `numpy`        | Numerical computing            | data      |
| `scikit-learn` | Machine learning               | data      |
| `pytest`       | Unit testing                   | testing   |

### Java Frameworks

| Framework/Tool | Purpose                       | Type      |
| -------------- | ----------------------------- | --------- |
| `spring`       | Enterprise app / DI framework | fullstack |
| `springboot`   | REST APIs, microservices      | backend   |
| `hibernate`    | ORM (database layer)          | backend   |
| `jakarta`      | Java EE successor             | fullstack |
| `maven`        | Build automation              | devops    |
| `gradle`       | Modern build tool             | devops    |
| `junit`        | Unit testing                  | testing   |
| `javafx`       | Desktop GUI development       | frontend  |

### Rust Frameworks

| Framework/Tool | Purpose                       | Type     |
| -------------- | ----------------------------- | -------- |
| `actix`        | High-performance web server   | backend  |
| `axum`         | Modular web framework         | backend  |
| `rocket`       | Simple backend web framework  | backend  |
| `tide`         | Async web APIs                | backend  |
| `clap`         | CLI argument parsing          | cli      |
| `tokio`        | Async runtime                 | backend  |
| `bevy`         | Game engine                   | games    |
| `macroquad`    | Lightweight game dev          | games    |
| `tauri`        | Desktop app with web frontend | frontend |
| `wasm-bindgen` | WebAssembly bindings          | frontend |

### TypeScript/JavaScript Frameworks

| Framework/Tool | Purpose                           | Type      |
| -------------- | --------------------------------- | --------- |
| `react`        | Frontend UI library               | frontend  |
| `nextjs`       | Fullstack framework (React-based) | fullstack |
| `angular`      | Web application framework         | frontend  |
| `vue`          | Progressive frontend framework    | frontend  |
| `node`         | JS runtime                        | backend   |
| `express`      | Minimalist backend framework      | backend   |
| `nestjs`       | TypeScript server framework       | backend   |
| `vite`         | Frontend bundler                  | frontend  |
| `svelte`       | Compiler-based frontend framework | frontend  |
| `jest`         | Testing framework                 | testing   |

### Go Frameworks

| Framework/Tool | Purpose                        | Type    |
| -------------- | ------------------------------ | ------- |
| `gin`          | Lightweight web framework      | backend |
| `echo`         | High performance web framework | backend |
| `fiber`        | Express-like async framework   | backend |
| `cobra`        | CLI apps                       | cli     |
| `urfave/cli`   | CLI tools                      | cli     |
| `gRPC`         | Remote procedure calls         | backend |
| `gorm`         | ORM for databases              | backend |
| `ent`          | Graph-based ORM                | backend |
| `chi`          | Minimalist router              | backend |

### C#/C++/C Frameworks

| Language | Framework/Tool | Purpose                     | Type      |
| -------- | -------------- | --------------------------- | --------- |
| C#       | `.NET`         | General development         | fullstack |
| C#       | `ASP.NET`      | Web development             | backend   |
| C#       | `Blazor`       | WebAssembly frontend        | frontend  |
| C#       | `MSTest`       | Microsoft testing framework | testing   |
| C#       | `NUnit`        | Unit testing                | testing   |
| C#       | `Xamarin`      | Mobile cross-platform       | frontend  |
| C#       | `MAUI`         | Multi-platform UI           | frontend  |
| C++      | `boost`        | Extended STL libraries      | general   |
| C++      | `qt`           | GUI toolkit                 | frontend  |
| C++      | `SDL`          | Game development            | games     |
| C++      | `OpenGL`       | Graphics rendering          | games     |
| C++      | `CMake`        | Build tool                  | devops    |
| C++      | `gtest`        | Testing framework           | testing   |

### JSON/YAML/SQL/XML Frameworks

| Tool                   | Purpose                       | Type  |
| ---------------------- | ----------------------------- | ----- |
| `jq`                   | Command-line JSON processing  | tools |
| `yaml-language-server` | Schema validation             | tools |
| `markdownlint`         | Markdown formatting           | tools |
| `sqlfluff`             | SQL linting and formatting    | tools |
| `dbt`                  | SQL-based data transformation | data  |

### Shell Frameworks

| Tool        | Purpose                     | Type  |
| ----------- | --------------------------- | ----- |
| `bash`      | Traditional shell scripting | cli   |
| `zsh`       | Enhanced shell              | cli   |
| `fish`      | User-friendly shell         | cli   |
| `oh-my-zsh` | Zsh config framework        | tools |
| `tmux`      | Terminal multiplexer        | tools |
| `screen`    | Terminal sessions           | tools |

## Platforms

### Cloud Platforms

| Platform  | Description                  | Use Case Examples                       |
| --------- | ---------------------------- | --------------------------------------- |
| `aws`     | Amazon Web Services          | Lambda, EC2, S3, RDS, API Gateway       |
| `gcp`     | Google Cloud Platform        | Firebase, App Engine, BigQuery          |
| `azure`   | Microsoft Azure              | Azure Functions, App Service, Cosmos DB |
| `vercel`  | Vercel hosting platform      | Deploying frontend (Next.js, React)     |
| `netlify` | Netlify hosting/CDN platform | JAMstack deployments, static sites      |
| `heroku`  | Heroku PaaS                  | Deploying web apps, APIs                |

### Continerization/Orchestration Platforms

| Platform     | Description                         | Use Case Examples                    |
| ------------ | ----------------------------------- | ------------------------------------ |
| `docker`     | Docker container runtime            | Dev/test environments, microservices |
| `kubernetes` | Container orchestration system      | Production deployments, clusters     |
| `podman`     | Docker-compatible container runtime | Rootless containers, scripting       |
| `nomad`      | HashiCorp’s workload orchestrator   | Lightweight orchestration            |

### Operating Systems

| Platform  | Description                 | Use Case Examples                           |
| --------- | --------------------------- | ------------------------------------------- |
| `linux`   | Native Linux OS / server    | Ubuntu, Debian, Arch, CentOS                |
| `windows` | Microsoft Windows OS        | Windows desktop apps, native development    |
| `macos`   | Apple macOS                 | macOS/iOS app development, Xcode, Swift     |
| `unix`    | Generic Unix-like systems   | BSD, Solaris, POSIX environments            |
| `wsl`     | Windows Subsystem for Linux | Linux tooling inside Windows, hybrid setups |

### Web/Client Platforms

| Platform   | Description                         | Use Case Examples                           |
| ---------- | ----------------------------------- | ------------------------------------------- |
| `browser`  | Runs in a browser                   | SPAs, frontend apps, WebGL, PWA             |
| `wasm`     | WebAssembly                         | Rust, C++, or Go compiled to run in browser |
| `electron` | Desktop apps using web technologies | Cross-platform desktop (VSCode, Slack)      |
| `tauri`    | Lightweight desktop framework       | Rust + WebView UI                           |
| `flutter`  | UI toolkit for mobile/web/desktop   | Cross-platform UIs                          |

### Mobile Platforms

| Platform       | Description                  | Use Case Examples          |
| -------------- | ---------------------------- | -------------------------- |
| `android`      | Android OS                   | Java/Kotlin mobile apps    |
| `ios`          | Apple iOS                    | Swift/iOS development      |
| `react-native` | JS-based mobile dev platform | Cross-platform React apps  |
| `flutter`      | Google’s UI toolkit          | iOS/Android with Dart      |
| `xamarin`      | C# cross-platform dev        | Mobile apps with .NET      |
| `cordova`      | Hybrid mobile apps           | Web technologies in mobile |
| `ionic`        | Hybrid mobile framework      | Angular/React/Vue apps     |
| `swiftui`      | Apple’s UI framework         | Declarative iOS apps       |

### Other Platforms

| Platform     | Description                        | Use Case Examples             |
| ------------ | ---------------------------------- | ----------------------------- |
| `embedded`   | Embedded systems/hardware targets  | Arduino, STM32, ESP32         |
| `edge`       | Edge computing                     | IoT devices, CDN workers      |
| `serverless` | Serverless platforms (generic)     | Functions-as-a-Service setups |
| `cli`        | Terminal/command-line environments | Bash, Zsh, CLI tools          |

## Owners

| Owner      | Description                           | Typical Use Case                        |
| ---------- | ------------------------------------- | --------------------------------------- |
| `personal` | Generic personal profile              | Side projects, self-hosted tools        |
| `team`     | Shared team environment               | Shared standards across devs on a team  |
| `shared`   | Used by multiple users or machines    | Open-source tools, shared setups        |
| `company`  | Company-wide standardized profile     | Enterprise development environments     |
| `orgname`  | Replace with actual organization name | DePaul, Microsoft, DAWnAudio, etc.      |
| `student`  | Academic use                          | Homework, tutorials, learning           |
| `contrib`  | External contributor profile          | Forked repos, open source contributions |
| `prod`     | Used in production machines           | Deployed or release environment         |
| `test`     | Used for testing/staging environments | CI/CD pipeline tests, validation        |

## Examples

| Profile Name                           | Explanation                                                |
| -------------------------------------- | ---------------------------------------------------------- |
| `python::default`                      | Basic Python profile with no framework, platform, or owner |
| `python:flask::backend`                | Flask-based backend profile for Python                     |
| `python:fastapi::api@aws`              | FastAPI API targeting AWS                                  |
| `python:fastapi::api@aws$team`         | Same as above, but used by a shared team                   |
| `typescript:react::frontend@browser`   | Frontend development in React targeting browsers           |
| `typescript:nextjs::web`               | General web app using Next.js                              |
| `typescript:nextjs::web@vercel$kellen` | Vercel-deployed Next.js app maintained by Kellen           |
| `go::cli`                              | Go-based command-line tool                                 |
| `go:echo::backend@docker`              | Echo backend running in Docker                             |
| `go:echo::backend@docker$team`         | Same setup, used across a development team                 |
| `rust::minimal`                        | Lean Rust environment                                      |
| `rust:axum::backend@wasm`              | Rust backend compiled to WebAssembly                       |
| `rust:tauri::desktop@macos$kellen`     | Tauri desktop app targeting macOS, for Kellen              |
| `java:spring::default@linux`           | Spring project for Linux environment                       |
| `java:spring::default@linux$orgname`   | Same as above, but for a company/organization              |
| `json::tools`                          | JSON tooling (validators, linters, etc.)                   |
| `bash::scripts@linux$personal`         | Personal Linux shell scripting setup                       |
| `markdown::writing`                    | Markdown-focused writing and documentation profile         |
| `cpp::system@windows$team`             | C++ systems-level profile targeting Windows for a team     |

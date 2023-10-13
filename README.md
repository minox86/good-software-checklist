# Good Software Checklist and Best Practices
The following is a checklist of best practices to develop and maintain good modern software. This list does not pretend to be complete, exhaustive or definitive, but should be considered as an evolving document to which anyone can **contribute** (please do), sending a pull request.

The backbone of this list was drafted within [TwinLogix s.r.l.](https://www.twinlogix.com/) in order to promote the use of good software development and management practices and standardize them across projects. For many practices, thid parties tools, services or products are also recommended to help with proper application. Feel free to supplement and evolve these lists.

## Version Control

- Use a **VCS**
  - [`GIT`](https://git-scm.com/)
- Use a **branch naming convention**
  - [`main`, `stage`, `develop`, `feature`, `bugfix`, `hotfix` or `test`](https://dev.to/varbsan/a-simplified-convention-for-naming-branches-and-commits-in-git-il4)
- Use **conventional commits**
  - [`feat`, `fix`, `chore`, `refactor`, `doc`, `test`](https://www.conventionalcommits.org/)
- **Protect** your production **branch**
- Adopt and combine **workflows**
  - [`GitFlow`](https://dev.to/the_previ/a-practical-introduction-to-git-flow-5420)
  - [`GitHub flow`](https://docs.github.com/en/get-started/quickstart/github-flow)
  - [`Rebase and squash`](https://matt-rickard.com/squash-merge-or-rebase) insted of merge
- Use **[release tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)**
- Organize projects using **[monorepo](https://monorepo.tools/)**
- Use **[git hooks](https://git-scm.com/docs/githooks)** to add pre-commit checks
  - [`Husky`](https://typicode.github.io/husky/)
- Setup a **bot for dependency updates**
  - [`Renovate`](https://www.mend.io/renovate/)  

## IDE

- Use an **IDE**
  - [`Visul Studio Code`](https://code.visualstudio.com/)
- Use a generative AI **copilot**
  - [`GitHub Copilot`](https://github.com/features/copilot)
- Use a **secure coding** plugin
  - [`Snyk`](https://snyk.io/platform/ide-plugins/)
- Use a **linter** plugin
  - [`ESlint`](https://eslint.org/)
  - [`SonarLint from SonarSource`](https://www.sonarsource.com/products/sonarlint/features/)
- Use a **prettier** plugin
  - [`Prettier`](https://prettier.io/)

## Architecture

- Follow the [**SOLID principles**](https://www.baeldung.com/solid-principles)
- Use a [**Clean Architecture**](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- **Decouple**, avoiding or breaking dependencies
- Use [**Architecture Decision Records (ADRs)**](https://adr.github.io/)
- Avoid monoliths, design [**microservices**](https://microservices.io/) or [**modular monoliths**](https://files.gotocon.com/uploads/slides/conference_12/515/original/gotoberlin2018-modular-monoliths.pdf)
- Produce and consume **APIs**
- Make it **observable**
  - [`Open Telemetry`](https://opentelemetry.io/)
  - [`ELK Stack`](https://www.elastic.co/elastic-stack)
- Use the [**CQRS pattern**](https://martinfowler.com/bliki/CQRS.html)
- Use the [**Transactional Outbox pattern**](https://microservices.io/patterns/data/transactional-outbox.html)
- Use [**Change data capture**](https://www.confluent.io/learn/change-data-capture) to implement the Transactional Outbox pattern
- Always implement **health checks**
- **Embrace standards** whenever you find them

## Development

### General

- Follow the [**KISS principle**](https://www.interaction-design.org/literature/topics/keep-it-simple-stupid)
- Follow [**DRY (Don't Repeat Yourself) Principle**](https://www.baeldung.com/cs/dry-software-design-principle)
- Produce [**Clean Code**](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
- Practice [**Domain Driven Design**](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215)
- Practice [**Test Driven Development**](https://www.agileway.it/test-driven-development-tdd/)
- Do [**regression tests**](https://katalon.com/resources-center/blog/regression-testing)
- Use [IDE helpers](#IDE) for linting, formatting and check your code
- Use **meaningful** variable and function **names**
- Keep **functions** and methods **short**
- Add only **meaningful comments** on your code
- Add **scripts** to compile, build, start, debug, test and releasing your project
- Try to be [**functional**](https://vimeo.com/97514630)

### Database

- Choose the right database ([**SQL vs NoSQL**](https://www.coursera.org/articles/nosql-vs-sql)) 
- Use **proper datatypes**
- Follow a **naming convention**
- Use **indexes**
- Continuously optimize performance through **indexes tuning**
- Plan and test a **backup strategy**
- Follow [**OWASP Security Principles**](https://owasp.org/www-project-developer-guide/draft/04-foundations/03-security-principles.html)
- Use [**up and down migrations**](http://vaidehijoshi.github.io/blog/2015/05/19/the-secret-life-of-your-database-part-1-migrations/)
  - [`migrate-mongo`](https://github.com/seppevs/migrate-mongo)

### Back-end

- Produce only **APIs** with an automatic **specification**
  - [`OpenAPI`](https://www.openapis.org/)
  - [`GraphQL`](https://graphql.org/)
  - [`gRPC`](https://grpc.io/)
- Produce and consume **events** with a standard **specification**
  - [`Cloud Events`](https://cloudevents.io/) 
- Secure your APIs with **JWT tokens**
- Use [**OAuth 2.0**](https://oauth.net/2/) authorization protocol
- Use **caching**
  - [`Redis`](https://redis.io/)
- Upload and download files with **presigned URLs**
  - [`S3 presigned URLs`](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html)

### Front-end
- Use a **typed language**
  - [`TypeScript`](https://www.typescriptlang.org/)
- Enforce [**end to end type safing**](https://sabinadams.hashnode.dev/end-to-end-type-safety-what-why-and-how)
- **Minify and compress** your bundle
- Use a **bundler tool**
  - [`Turbo`](https://turbo.build/)
  - [`Nx`](https://nx.dev/)
- Use **browser caching**
- Use a **Content Delivery Network (CDN)**
  - [`AWS CloudFront`](https://aws.amazon.com/it/cloudfront/)
- Use **pagination or infinite scroll**
- Use [**debounce/ throttle**](https://webdesign.tutsplus.com/javascript-debounce-and-throttle--cms-36783t)
- Use [**lazy loading**](https://www.codemotion.com/magazine/backend/how-to-boost-performance-with-lazy-loading/)
- Use **captcha**
- Use **appropriate image formats** (e.g., SVG, WebP)
- Use **end to end testing** for critical paths
  - [Playwright](https://playwright.dev/)
- Define a [**manifest**](https://web.dev/articles/add-manifest?hl=it) for your app
 
### Mobile
- 

## Infrastructure

- Develop **Infrastructore as a Code**
  - [`Terraform`](https://www.terraform.io/)
- Have **at least two environments**: test and production
- Use **GitOps**
  - [`Terraform Cloud`](https://developer.hashicorp.com/terraform/cloud-docs)
  - [`GitLab CI`](https://docs.gitlab.com/ee/ci/)
  - [`GitHub Actions`](https://github.com/features/actions)
- Save **secrets in a secure storage**
  - [`AWS Systems Manager Parameter Store`](https://aws.amazon.com/it/systems-manager/)
  - [`Vault by HashiCorp`](https://www.vaultproject.io/) 
- Store the **infrastructure state** in the cloud
  - [`Terraform Cloud`](https://developer.hashicorp.com/terraform/cloud-docs)
  - [`AWS S3`](https://aws.amazon.com/it/s3/)
- **Modularize infastructure** for reuse
- Design for **scalability**
  - [`Kubernetes`](https://kubernetes.io/)
  - [`AWS ECS`](https://aws.amazon.com/it/ecs/)
- Design for **security**
  - [`AWS WAF`](https://aws.amazon.com/it/waf/)
- Design for **availability**
- Design for **reliability**
- Design for **disaster recovery**
- Design for **auto healing**
- Monitor [**DORA metrics**](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)
- Do **load tests**
  - [`k6`](https://k6.io/)

## DevOps

- Run applications in **containers**
  - [`Docker`](https://www.docker.com/)
- Use **caches** to speed up the pipeline
- Configure a **build step**
- Use a **CI/CD** tool
  - [`AWS Code Pipeline`](https://aws.amazon.com/it/codepipeline/)
  - [`GitLab CI`](https://docs.gitlab.com/ee/ci/)
  - [`GitHub Actions`](https://github.com/features/actions)
- Configure a **testing step** in your pipeline
- Configure a **coverage step** in your pipeline
  - [`Codecov`](https://about.codecov.io/)  
- Configure a **security check step** in your pipeline
  - [`Snyk`](https://docs.snyk.io/integrations/snyk-ci-cd-integrations)
- Configure a **code quality check step** in your pipeline
  - [`ESlint`](https://eslint.org/)
  - [`SonarLint from SonarSource`](https://www.sonarsource.com/products/sonarlint/features/)
- Configure a **deploy step**
- Use [**blue green deployment**](https://docs.aws.amazon.com/whitepapers/latest/overview-deployment-options/bluegreen-deployments.html)


# Glossary — Clean Code

**Abstract Factory (ABF)** — pattern used to bury a `switch`/construction in one place so polymorphic objects are produced without repeating the switch.
**Active Record** — a data structure (DTO) with navigation methods like `save`/`find`; keep business logic out of it.
**Adapter** — bridges the API you wish you had and the one a vendor gives you; isolates the single point of change at a boundary.
**AOP (Aspect-Oriented Programming)** — modularizes cross-cutting concerns (persistence, security, transactions).
**Boy Scout Rule** — leave the code cleaner than you found it, on every check-in.
**BUILD-OPERATE-CHECK** — readable three-part structure of a clean test.
**Code smell** — a surface symptom (after Fowler) signaling a deeper design problem.
**Code-sense** — the trained ability to perceive messes and know the maneuvers to fix them.
**Cohesion** — degree to which a class's methods use its instance variables; high cohesion = small, focused classes.
**Command Query Separation** — a function either does something or answers something, never both.
**Cross-cutting concern** — functionality (logging, security) that spans many modules; modularize via aspects.
**Dependency Injection (DI)** — supplying an object's dependencies from outside rather than constructing them internally; a form of Inversion of Control.
**Dependency Inversion Principle (DIP)** — depend on abstractions, not concretions.
**DRY (Don't Repeat Yourself)** — eliminate duplication; "the root of all evil in software" (G5).
**DTO (Data Transfer Object)** — class of public data + no behavior; ideal at boundaries.
**F.I.R.S.T.** — clean tests are Fast, Independent, Repeatable, Self-Validating, Timely.
**Feature Envy** — a method more interested in another class's data than its own (G14).
**Hybrid** — half object, half data structure; worst of both — avoid.
**Inversion of Control (IoC)** — move secondary responsibilities (like construction) out of an object to an authoritative mechanism.
**Law of Demeter** — talk only to immediate friends: `this`, your fields, your parameters, objects you create; don't navigate through strangers (G36).
**LeBlanc's Law** — "Later equals never."
**Learning Test** — a test written to explore/verify a third-party API; doubles as an upgrade regression test.
**Newspaper Metaphor** — a source file should read top-down like an article: headline first, details below.
**Open-Closed Principle (OCP)** — open for extension, closed for modification.
**POJO (Plain Old Java Object)** — a simple object free of framework entanglement; enables testable architecture.
**Polymorphism over switch** — prefer dispatching on type via polymorphism to repeated switch/if-else (G23).
**Single Responsibility Principle (SRP)** — a class/module has exactly one reason to change.
**Special Case Pattern** — an object that encapsulates exceptional behavior so clients avoid null-checks/try-catch.
**Stepdown Rule** — every function is followed by those one level of abstraction below it.
**Successive Refinement** — reaching clean code through many small, test-protected improvements.
**Template Method** — pattern to remove higher-level duplication by hoisting the common algorithm to a base class.
**Test-Driven Development (TDD)** — write a failing test before the production code that passes it; see the Three Laws.
**Three Laws of TDD** — (1) no production code without a failing test; (2) write no more test than fails; (3) write no more code than passes.
**Train wreck** — chained calls through object internals (`a.getB().getC().getD()`); a Demeter violation.
**Vertical distance** — related concepts should sit close together in a file.

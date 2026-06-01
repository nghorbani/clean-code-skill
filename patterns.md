# Patterns & Techniques — Clean Code

## Express Intent in Code, Not Comments
**When**: about to write an explanatory comment.
**How**: extract the condition/expression into a well-named function or variable (`if (employee.isEligibleForFullBenefits())`).
**Trade-offs**: more named units; pays off because names don't rot the way comments do.

## Extract Till You Drop (Small Functions)
**When**: a function does more than one thing or mixes abstraction levels.
**How**: extract sub-steps into functions named for *what* they do until each does one thing; apply the Stepdown Rule so the file reads top-down.
**Trade-offs**: many small functions; navigation relies on good names + IDE.

## Replace Switch with Polymorphism (Abstract Factory)
**When**: a switch/if-else dispatches on a type code and tends to recur.
**How**: bury one switch in a factory that returns polymorphic subclasses; add new types by adding classes (OCP), not editing the switch.
**Trade-offs**: more classes; eliminates repeated, error-prone branching (G23).

## Wrap Third-Party APIs
**When**: a foreign type (e.g. `Map`) or library would otherwise spread through the codebase.
**How**: encapsulate it in a class exposing only the operations you need; convert its exceptions to yours.
**Trade-offs**: a thin wrapper layer; gains testability and one-place migration.

## Learning Tests
**When**: adopting or upgrading a third-party library.
**How**: write tests exercising the API as you intend to use it; keep them as regression guards against library changes.
**Trade-offs**: upfront test code you'd informally write anyway; catches breaking upgrades for free.

## Code to the Interface You Wish You Had
**When**: depending on code that doesn't exist yet (another team's API).
**How**: define your ideal interface, implement against it, adapt to reality later with an Adapter.
**Trade-offs**: an adapter to write later; keeps your design clean and testable now.

## Exceptions over Return Codes; Special Case Object
**When**: error handling clutters the happy path, or you'd return/check null.
**How**: throw unchecked exceptions with context; for "nothing"/edge cases return a Special Case object or empty collection — never null.
**Trade-offs**: must define exception/special-case types; logic stays clean and NPE-free.

## Separate Construction from Use (DI / Separation of Main)
**When**: objects build their own dependencies (lazy-init, `new` in business logic).
**How**: move construction to `main`/factories/DI container; pass fully-built collaborators in; depend on abstractions (DIP).
**Trade-offs**: a wiring layer; yields testable, flexible, swappable components.

## Four Rules of Simple Design (drive emergent design)
**When**: continuously, as you add features.
**How**: ensure (1) all tests pass, (2) no duplication, (3) intent is expressed, (4) fewest classes/methods — in that priority.
**Trade-offs**: requires test discipline; design emerges instead of being over-planned.

## Successive Refinement under Tests
**When**: code starts sliding toward a mess.
**How**: **stop adding features**; refactor in tiny steps with the test suite green before continuing.
**Trade-offs**: short-term feature pause; avoids the unrecoverable mess.

## Concurrency Defenses
**When**: introducing threads.
**How**: isolate concurrency code (SRP); limit & protect shared mutable data; prefer copies/thread-confinement; use `java.util.concurrent`; break one deadlock condition by lock-ordering.
**Trade-offs**: added structure/overhead; intermittent bugs become tractable.

## Build a Domain-Specific Testing Language
**When**: tests are verbose and hard to read.
**How**: extract helpers (`assertResponseIs(...)`, builders) so tests read at the domain level; one concept per test.
**Trade-offs**: a small test API to maintain; far more readable, durable tests.

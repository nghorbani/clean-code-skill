# Clean Code — Cheatsheet

## The One Rule
**Leave it cleaner than you found it** (Boy Scout Rule). The only way to go fast is to keep the code clean.

## Naming (N1–N7)
- Intention-revealing · no disinformation · meaningful distinctions · pronounceable · searchable.
- Classes = nouns; methods = verbs. One word per concept.
- Name length ∝ scope. No encodings (Hungarian, `m_`, `I`-prefix).

## Functions (F1–F4)
- **Small**, then smaller. **Do one thing.** One level of abstraction.
- Args: 0 > 1 > 2 > 3. No flag args. No output args.
- Command **or** query, not both. Exceptions, not error codes. DRY.

## Comments (C1–C5)
- A comment = a failure to express in code. Best comment = the one you didn't need.
- **Delete commented-out code now.** No journal/noise/redundant comments — VCS remembers.

## Formatting
- Read top-down (newspaper). Blank lines separate concepts; related code stays close.
- Declare variables near use. **Adopt one team style; automate it.**

## Objects vs Data
- Objects: hide data, expose behavior → easy new *types*. Data structures: expose data → easy new *functions*.
- Don't make hybrids. Obey Law of Demeter (no train wrecks). Tell, don't ask.

## Error Handling
- Unchecked exceptions with context. Wrap third-party APIs.
- **Never return null. Never pass null.** Use Special Case objects.

## Boundaries
- Wrap foreign types. Write learning tests. Code to the interface you wish you had + Adapter.

## Tests (T1–T9)
- **Three Laws of TDD**: failing test first → minimal test → minimal code.
- **F.I.R.S.T.**: Fast, Independent, Repeatable, Self-Validating, Timely.
- One concept per test. Keep tests as clean as production code. Use a coverage tool.

## Classes
- Small = few responsibilities. **SRP**: one reason to change. High cohesion.
- **OCP** (extend, don't modify) · **DIP** (depend on abstractions).

## Systems
- Separate construction from use. Inject dependencies. Grow architecture incrementally. Defer decisions to the last responsible moment.

## Emergence — Simple Design, in priority order
1. Runs all the tests  2. No duplication  3. Expresses intent  4. Fewest classes/methods

## Concurrency
- Decouples *what* from *when*. Isolate concurrency code (SRP). Limit & protect shared data; prefer copies.
- Deadlock needs all four: Mutual Exclusion, Lock & Wait, No Preemption, Circular Wait — break one.
- Treat every intermittent failure as a threading bug; jiggle to expose.

## Smell Codes
**C** Comments · **E** Environment · **F** Functions · **G** General (G1–G36) · **J** Java · **N** Names · **T** Tests.
Most messes reduce to **G5 Duplication** and **G6 Wrong Level of Abstraction**.

## Definition of Done
It **works** (tested) **and** it's **right** (clean). Working alone is not done.

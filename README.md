# Evaluation Playbook for AI Assistants and Agents

**Evaluation is a steering system, not a scorecard added at the end.**

A sophisticated metric over the wrong population answers the wrong question
precisely. This playbook is about the things that go wrong *before* the metric —
the dataset that does not represent the work, the oracle that cannot see the
evidence, the judge that has never been validated, and the run that reported a
clean number over half a sample.

📖 **[Read the playbook](https://amandachan-ai.github.io/evaluation-playbook/)**

---

## What it covers

| | |
|---|---|
| **North star** | A priority order for where to look first: representativeness → oracle validity → judge validity → task success → consistency → operations |
| **Three archetypes** | Text-transformation assistant, conversation assistant, cross-context agent — described as *evaluation problems*, not products |
| **Controlled comparison** | Pre-register before generating, compare the same cases, keep measurement layers separate |
| **Validating the judge** | Discriminative power, headroom counted in cases, construct validity, and why rationales are not evidence |
| **Run integrity** | Silent failure, and why a count of identifiers is not a count of work |
| **Shipping evidence chain** | Config exists → run completes → causal result → change lands → feature enables → gate enforces → user impact |
| **Failure library** | Ten failure patterns with the preventive rule for each |
| **Minimum Definition of Done** | Nine checks before an evaluation is allowed to decide anything |

## Three things it argues that are easy to get wrong

**A judge that passes everything has told you nothing.** Check saturation and
headroom before trusting any comparison made with it, and report the number of
cases that *could* still improve rather than a mean and a standard deviation.

**Ask what score the judge gives to a correct decision to do almost nothing.**
A judge can follow its rubric perfectly and still reward the wrong product
behavior. Abstaining, asking for clarification, and making only the change that
was requested are correct outcomes, and a rubric that punishes them is measuring
something other than quality.

**A number that a failure can also produce is not a check.** If failed trials
keep their identifiers, counting identifiers reports a complete run with missing
outputs. Verify the property you actually care about — successful output IDs,
terminal state, artifact hashes, grader coverage, error denominators.

## Scope

The playbook is provider-neutral and deliberately generic. It describes
evaluation problems and the methods that address them; it contains no private
product names, internal architecture, identifiers, experiment values, or
artifact inventories.

## License

MIT — use it, adapt it, argue with it.

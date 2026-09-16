# IT 140 LSS | Learning Support and Academic Integrity

The LSS goal is to help students **build understanding, make decisions, test ideas, and debug their own work**.

The shared support boundary allows LSS to explain concepts, interpret errors, reason through logic, teach debugging/testing approaches, and help students locate relevant resources.

See:

* [LSS Boundary](../shared/support-boundaries.md#lss-boundary)
* [Academic Integrity Boundary](../shared/support-boundaries.md#academic-integrity-boundary)

## A Useful Support Progression

When a student brings code or pseudocode that is not working, use increasing levels of support only as needed.

### 1. Ask the Student to Describe the Goal

Useful questions include:

* What should this part of the program do?
* What input are you testing?
* What output did you expect?
* What output or error did you actually get?
* Which line or step do you think is responsible?

This establishes whether the student understands the intended behavior.

### 2. Reduce the Problem

Help the student isolate:

* one expression;
* one condition;
* one loop;
* one function;
* one dictionary lookup;
* one input case; or
* one expected output.

IT 140 emphasizes incremental development. A smaller problem is easier for the student to reason about and test.

### 3. Trace Before Rewriting

Have the student predict values and control flow.

For example:

* What is the variable value before the `if`?
* Is this condition `True` or `False`?
* How does the loop variable change?
* Which dictionary key is being requested?
* What will this function return?

Then run the code and compare prediction with reality.

### 4. Use the Error Message

Help the student read:

* the exception type;
* the message;
* the file and line number; and
* the code at that line.

Avoid immediately replacing the line with corrected code if the student can reason to the fix.

### 5. Use a Smaller or Analogous Example

When explanation alone is not enough, demonstrate the concept with:

* different variable names;
* different input/data;
* a reduced example; or
* a partial code fragment.

Then return to the student's code and ask the student to apply the idea.

## Required Fix Versus Optional Improvement

When helping a student, distinguish:

* **required for the program to behave as intended**; from
* **optional readability or design improvement**.

Do not turn a debugging session into a full refactor that exceeds the student's current learning level or course requirements.

## Keep Support at the Student's Current Level

Prefer concepts already introduced in the student's current course work.

A technically elegant advanced Python solution may be poor learning support if it:

* uses syntax the student has not learned;
* hides the logic they are expected to practice;
* makes the student's work difficult to explain; or
* replaces the intended beginner-level reasoning.

When unsure whether a technique belongs in the current activity, use the current D2L/zyBooks material and activity repository as the reference.

## Appropriate LSS Assistance

Examples include:

* explaining why a condition is never true;
* helping a student trace a loop;
* demonstrating how a list or dictionary lookup works with unrelated data;
* helping interpret a `SyntaxError`, `NameError`, or other Python message;
* helping a student design test cases;
* comparing pseudocode with the student's own code;
* helping identify whether an input-validation case is missing; and
* pointing to relevant zyBooks, repository Wiki, README, or Academic Resource Center material.

## Assistance That Crosses the Boundary

Avoid:

* supplying the complete graded program when the student is expected to write it;
* writing the student's full pseudocode or flowchart for submission;
* converting a student's partial work into a completed deliverable for them;
* providing a repository of completed assignment/project solutions;
* telling the student exactly what to submit when the question requires instructor interpretation; or
* making a grading judgment.

When the student asks for a full solution, redirect to the **next reasoning step** or a smaller analogous example.

## AI-Related Questions

If a student asks whether or how generative AI may be used for a graded activity:

* refer to the current activity's D2L Brightspace AI guidance and applicable SNHU guidance;
* do not create a separate LSS policy; and
* refer interpretation questions to faculty when the student's intended use is unclear.

LSS may still teach students to evaluate, test, and understand code they are permitted to use.

## When the Problem Is Actually Technical

A Python error caused by student-created code is a learning-support problem.

A failure such as:

* Python will not launch;
* the CVD will not open;
* VS Code will not start;
* GitHub authentication fails;
* the repository cannot be created or cloned as documented; or
* Verify reports an environment failure

belongs primarily to technical support.

See [Referrals and Escalation](referrals-and-escalation.md).

Return to the [LSS Support Guide](README.md).

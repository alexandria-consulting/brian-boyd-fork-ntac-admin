# NIEMOpen NTAC Token Use Policy

Version 0.1, discussion draft for the group's first meeting, arranged by stage and by role.

All policy provisions and templates below are proposals for the group to adopt, change
or reject; none has been agreed.

The proposed policy covers everyone who spends tokens from the NTAC budget, every agent
that spends them on that person's behalf, everything produced with them, and every
NIEMOpen repository or NTAC work item that the work touches. Section 7 sets out the
proposed coverage of work that the NTAC budget does not pay for.

The OASIS Open Project rules, the NIEMOpen governance documents, the Contributor License
Agreement, the Code of Conduct, each repository's license and the provider's terms come
first; where this policy conflicts with them, they win.

## Proposed approach at a glance

1. No one uses NTAC tokens without a recorded grant.
2. The current quota is noted at the very beginning of the work, whenever it refreshes
   during the work, and directly after work is completed or otherwise stopped.
3. Every token spent is attributable to a person, a project and a unit of work or review
   round, in a record kept in GitHub.
4. Work is planned; the plan is adversarially reviewed until it converges; the plan is
   implemented unit by unit; each unit is checked in; substantial work is adversarially
   reviewed until it converges; the plan is closed as implemented.
5. The person, not the agent, is accountable for everything that reaches the project.
6. Credentials are personal, unshared, never committed, and revoked when the grant ends.
7. The policy names no provider. The provider in use, and how its own limits,
   notifications and usage reports are set up, are recorded in one manifest file
   (section 10), chosen against stated requirements and reviewed on a regular cadence
   (section 9).

## 1. Words

- **Provider**: a vendor whose model service the NTAC buys tokens from. "The provider"
  means the provider the manifest names for the account and period in question.
- **Manifest**: the file in the NTAC admin repository that records the provider in use and
  how its account is set up (section 10).
- **Token**: the unit in which the provider meters use of its model service, whatever it
  calls that unit.
- **Budget**: the pool of tokens the NTAC holds.
- **Grant**: a recorded permission for one person to spend up to a stated amount on one
  project for a stated period.
- **Credential**: the key or account through which an agent spends tokens.
- **Quota**: the tokens the provider shows as available on a credential at a given moment.
  A **refresh** is the provider restoring or raising that quota, for example at the start
  of a billing period. Where the provider shows no quota for a credential, use the
  remaining spend limit set for it instead, for every quota note.
- **Coding agent**: software that uses an AI model to read, write, run and test code,
  specifications or documents under a person's direction.
- **Holder**: the person named in a grant.
- **Project**: a NIEMOpen repository, or a named NTAC work item together with the
  repository that receives its work.
- **Plan**: the written statement of a piece of work: its goal, scope, units, acceptance
  checks and open questions.
- **Unit of work**: a focused change with an acceptance check, completable in one pass.
- **Checked in**: committed and pushed to the project repository, or submitted there as a
  pull request, by that repository's rules. Merging is the maintainers' business, not part
  of checking in. A unit that changes no repository, such as research, is checked in when
  its result is recorded in the plan.
- **Adversarial review**: a review whose brief is to refute the work: to find a failure
  scenario, a false claim or a broken contract. A finding that names such a thing is a
  defect; what would be better but is not wrong is an enhancement.
- **Reviewer**: a person other than the author, or an agent the author runs in a fresh
  session that carries nothing of the author's working context and reads only the plan
  or the repository at the stated commit. You may run the reviewing agent yourself.
- **Converged**: a review round that finds nothing at medium severity or above. Findings
  carry one of four severities: critical, high, medium, low.
- **Substantial work**: a milestone the plan names, or any unit that changes a
  specification, a conformance rule, a model artifact or a release.
- **Register**: the grant issues and the usage ledger, kept in GitHub (section 5).

## 2. Who does what

- **The NTAC** owns this policy and changes it by its ordinary decision process.
- **The co-chairs** administer it: they decide grant requests, amendments and exceptions,
  suspend and revoke grants, and may delegate day-to-day administration to the steward.
  Nobody takes part in a decision about their own grant: a co-chair's grant is decided by
  the other co-chair, or by the NTAC if there is a single chair; the steward's grant is
  decided by the co-chairs.
- **The token steward**, a person the co-chairs name, holds the NTAC's provider
  account, keeps the manifest current, runs the vendor review (section 9), issues and
  revokes credentials, keeps the register, records closures,
  suspensions and revocations, reconciles the ledger against the provider's usage report,
  and reports to the NTAC. For
  the steward's own grant, a co-chair does the reconciling and the recording.
- **The holder** is the contributor of record, requests the grant, spends the tokens,
  keeps the ledger current, follows section 4, and answers to the NTAC for the work and
  for the consumption. Everything the CLA says about a contribution applies to agent
  output exactly as to the holder's own work; "the agent wrote it" is no defence. Whoever holds the contract with the provider
  answers to the provider for the account as a whole.
- **A sponsor** is an NTAC member who sponsors a non-member's request and answers to the
  NTAC for that person's compliance.
- **Maintainers** review and merge pull requests by each repository's own rules, which
  this policy does not change. They review agent-assisted work by the same standard as any
  other, may ask whether and how an agent was used, and may decline work that does not meet
  the repository's standard, whoever or whatever produced it.
- **The agent** acts only under the holder's direction. It never certifies the CLA or any
  statement of origin. After the holder has reviewed the work, the agent may perform the
  push or open the pull request.

## 3. The life of a grant

### 3.1 Who may ask

Anyone who has signed the Individual CLA (and whose employer has signed the Entity CLA
where that applies), is not under a Code of Conduct sanction, and is an NTAC member or
sponsored by one.

### 3.2 States and moves

A grant is requested, active, exhausted, suspended or closed.

**Requested.** You open a grant issue in the register (template A) giving your name and
GitHub login, your sponsor if you have one, the project (for a work item, also the
repository that receives the work), the goal, the amount, the period, and your
acknowledgment of this policy.

**Active.** The co-chairs approve, reduce or decline the request by agreement and record
the decision on the issue; a grant under a size the co-chairs delegate may be approved by
the steward. If nothing is decided within ten days, you may bring the request to the next
NTAC meeting, which decides by lazy consensus.

**Exhausted.** When the amount runs out, spending stops until an amendment for more tokens
is approved or the grant is closed. Directly after stopping, note the current quota on the
grant issue, with the quota at the beginning of the work and any refreshes.

**Suspended.** The co-chairs may suspend an active or exhausted grant on non-compliance
(section 6). The credential is revoked at once, and the grant still counts as held. The
co-chairs may lift the suspension; the steward then issues a new credential.

**Closed.** A grant closes when its period ends, when you and a co-chair agree that its
purpose is met, or when the co-chairs revoke it. After 60 days without ledger activity,
the grant is reviewed with you and may be closed by the co-chairs. The steward records
the closure on the grant issue.

More tokens or more time is an amendment on the same issue, decided by whoever decided
the grant. An amendment that takes a steward-approved grant over the delegated size goes
to the co-chairs. Nobody extends their own grant. Another project is a new request, not
an amendment.

You hold one grant per project at a time and may hold grants on several projects. A
grant cannot be transferred.

### 3.3 The credential

The steward issues one credential per grant from the NTAC's account with the provider the
manifest names. The grant issue names the credential's identifier and its provider, never
the credential itself. When the provider changes, credentials are reissued as section 9.4
sets out.

The credential is yours alone: never shared, lent, or used by anyone else, and never
committed to a repository, pasted into an issue, message or chat, or stored under version
control. Keep it in the environment or a secret store, with local environment files out
of version control. Use it only as the provider's terms allow; do not substitute a
personal subscription's credential for it, and do not use it for anything outside the
grant. Have it replaced every 90 days by asking the steward, and the replacement noted on
the grant issue, which then names the new credential's identifier. Report exposure or
suspected compromise to the steward at once; the credential is revoked and replaced, and
the event is noted on the issue.

The steward revokes the credential when the grant closes, is suspended or is revoked.

### 3.4 What the tokens may be spent on

The work named in the grant, on the grant's project: code, specifications, model
artifacts, conformance rules, tests, tooling, documentation; analysis or research in
direct service of that work, recorded as a unit; and adversarial review of another
holder's work on the same project, recorded under your own grant.

Not: anything outside the grant's project or purpose, including personal, employer or
commercial purposes; transferring, lending or pooling tokens or credentials, or routing
consumption through another credential to get around a grant's amount; giving an agent
material you may not disclose (third-party confidential material, personal data, anything
under a non-disclosure agreement); sending the project anything you have not reviewed, whether a commit, pull request,
issue, comment or message; or leaving an agent running with no active unit of work.

## 4. How the work goes

Written for the holder, in order.

### 4.1 Note the quota and write the plan

At the very beginning of the work, note the current quota on the credential in the plan.
Whenever the quota refreshes during the work, note when it happened and the quota after it.

Before any tokens go on implementation, write the plan in the project repository, or in
the NTAC admin repository beside the register, and link it from the grant issue. Writing
the plan, or taking over a plan that continues under your grant, is the grant's first unit
of work.

The plan states the goal, the scope, and the units of work with an acceptance check each,
and sizes the work as a count of units with the breakdown that makes the count checkable.
The plan also includes the declined list (what was considered and left out, and why),
the known unknowns with who resolves each, and the plan's blind spots. Plans give no time
estimates. Template C is an outline.

### 4.2 Have the plan reviewed

The plan is adversarially reviewed before implementation, by a reviewer (section 1)
reading it at a stated commit. Each finding carries a severity, and a finding at medium
or above says what wrong outcome it produces and how. Fix each finding, add it to the plan
as a named unit, or record why it is declined; nothing is dropped silently, and a fix that
breaks something the plan must allow is the next round's finding. Rounds continue until
the review converges (section 1); rounds and findings are recorded with the plan.

### 4.3 Implement the plan as written

When a unit's acceptance check passes, check it in; a unit may take several commits.
Each commit names its plan, unit and grant in trailers (template D), and its message
records the decisions taken.

If a deviation turns out to be necessary, record it in the plan as an amendment, with its
evidence, before implementing it. If the amendment changes the goal, the scope or a unit's
acceptance check, the plan goes back through review; units the amendment does not touch
may continue meanwhile, and a unit it touches, even one already implemented, waits for the
re-review before it is checked in. Work the plan does not ask for is proposed as an
amendment or declined, not added.

### 4.4 Record each unit

When a unit is checked in, write its ledger row (section 5) before the next unit is
checked in. A row counts as written when it is committed to the register or submitted
to it as a pull request.

A review round that consumed tokens gets a row of its own, under the grant whose credential
ran it; tokens spent on a unit after its row exists, such as a fix after a review round,
get a further row.

### 4.5 Have substantial work reviewed

Substantial work (section 1) is adversarially reviewed to convergence before it counts as
done. The reviewer reads the repository at a stated commit and runs what can be run. Each
finding becomes a failing case, a test or an acceptance check before it is fixed, and the
fix is checked in under the unit it corrects.

### 4.6 Close the plan

The plan is marked implemented when every unit is checked in and every review that 4.5
required has converged. Directly after the work is completed, note the current quota, and
record on the grant issue the plan's total consumption, the quota noted at the beginning,
every refresh noted during the work, and the quota at the end. A plan may continue under a
later grant; each row names the grant that paid, and each grant's share of the total goes
on its own issue.

### 4.7 Keep the person in charge

Direct the agent, read and understand its output, and submit the work under your own
name. Nothing reaches the project unreviewed by you. Use only tools whose terms do not
restrict the use of their output in a way that conflicts with the repository's license or
the OASIS IPR rules. Third-party material an agent reproduces is handled like any other
third-party material: disclosed, licensed compatibly, or removed; where a tool can flag
output that resembles public code, turn that on. A commit whose content was materially
generated by an agent carries a trailer naming the tool and model (template D); light
help, such as wording and formatting, needs none.

## 5. The record

The register lives in the NTAC admin repository: one GitHub issue per grant, which
carries the request, the decision, amendments, incidents, credential replacements,
exceptions, the plan's location, the plan's total and quota notes, and the closure; and
one ledger file with a row per unit of work, review round or fix (template B). The
register is public, as the OASIS rules require of project tools; nothing goes into it
that the writer may not disclose.

A ledger row holds the date, holder, grant, project, plan, the unit or round or fix, the
amount consumed as the provider's usage view shows it, the commits or pull request that
checked the unit in, and a note if the unit was abandoned or is incomplete. A mistaken row
is corrected by a further row that names the row it corrects and carries the full
corrected values; the total counts the correction and not the row it corrects. Rows are
not edited; nothing is removed from the register.

Before each NTAC meeting, the steward reconciles the ledger against the usage report of
the provider the manifest named for each credential and period, resolves any difference with the holder, and notes
the outcome on the grant issue.

At each regular NTAC meeting, the steward reports tokens consumed and remaining, in total
and per grant; grants opened and closed; and incidents. The report goes where NTAC meeting
outcomes are posted. The co-chairs may at any time ask a holder to account for consumption
against the ledger.

## 6. When something goes wrong

Unrecorded consumption, a shared or exposed credential, use outside the grant, and work
that bypasses section 4 are raised with the holder by the steward, or by a co-chair if the
steward is the holder. The co-chairs may suspend the grant, revoke it, and decline future
requests. Conduct matters follow the Code of Conduct process.

If a grant closes, is suspended or is revoked while a unit is in progress, that unit's
row is written, marked incomplete, before the closure, suspension or revocation is
recorded: by the holder, or by whoever records it, from the provider's usage report, with
a note on the issue. Directly after the work stops, the current quota is noted on the
grant issue in the same way, with the quota noted at the beginning and any refreshes.

An exception to a clause is requested on the grant issue, or on an issue in the register
for work that has no grant, naming the clause, the reason, the scope and the end date.
The co-chairs decide and record the decision on the issue, nobody deciding on their own
grant.

## 7. Work the NTAC budget does not pay for

Sections 4 and 2's rules for the holder, maintainers and the agent also apply to
agent-assisted contributions to NTAC repositories that the NTAC budget does not pay for,
whether the contributor, their employer or nobody pays. For that work the contributor is
the holder, and the steps that depend on a grant, a credential, the ledger or the quota do
not apply. An exception for such work is requested on an issue in the register.

## 8. Keeping the policy current

The policy lives in the NTAC admin repository, and its history is the repository's
history. It is reviewed once a year and whenever the token source, the provider or the
provider's terms change, and against any guidelines OASIS adopts on token use or agent-assisted
contributions.

## 9. Choosing the provider

Model services change quickly, in capability, price, terms and reliability, and the NTAC
should not be tied to one of them. This policy therefore names no provider. Everything
specific to a provider lives in the manifest (section 10), and the provider is chosen
against the requirements below and reviewed on a regular cadence.

### 9.1 Use the provider's own controls

Where the provider's team or organization plan already does something this policy needs,
such as spend limits per member or workspace, quota notifications, usage reports or
credential revocation, the NTAC uses that feature and records how it is set up in the
manifest. It does not build its own tool to do the same job. Tooling the NTAC does build,
for example a hook that writes quota notes for a holder, is a project of its own under a
grant, and must work with more than one provider or be easy to replace.

### 9.2 Requirements

A provider qualifies only if it meets every one of these.

1. **Terms.** Its terms allow use for open standards work, and do not restrict the use of
   output in a way that conflicts with the repository's license or the OASIS IPR rules
   (section 4.7).
2. **Data.** Its terms state how prompts and output are retained and whether they are used
   for training. The NTAC can choose a setting under which project material is not used
   for training.
3. **Team account.** The NTAC holds one account, under the steward, and can issue a
   separate credential to each holder within it.
4. **Limits.** The steward can set and change a spend or token limit for each credential,
   or for a workspace or group that holds it, in the provider's own console.
5. **Notifications.** The provider can notify the holder, the steward, or both when a
   limit is approached or reached.
6. **Usage reports.** The steward can get usage for each credential and period from the
   provider, in a form that can be reconciled against the ledger (section 5).
7. **Revocation.** The steward can revoke any single credential at once without
   affecting the others.
8. **Agents.** The service can be used from the coding agents that holders use,
   and those agents support hooks or an equivalent that can read the quota at the start
   and end of a unit of work (sections 4.1 and 4.6).
9. **Billing.** It can be paid for in the way the NTAC's funding source requires.

### 9.3 Weighing qualified providers

Among providers that qualify, the review weighs:

- cost for a representative unit of work, measured on the same plan with each provider
  rather than read from a price list;
- model capability for the NTAC's work, which is specifications, model artifacts,
  conformance rules, tooling and review;
- reliability and availability over the period under review;
- the effort and disruption a switch would cost holders mid-plan.

### 9.4 The vendor review

The steward runs a vendor review on the cadence the manifest states (proposed: monthly,
before the start of the provider's billing period), and whenever a provider's terms
change in a way that affects a requirement in 9.2.

1. The steward opens a review issue in the register. It lists the current provider and
   any candidates, checks each against 9.2, gives the facts for 9.3, and reports problems
   holders have recorded since the last review.
2. Holders with an active grant may comment and vote for a provider. The vote advises the
   co-chairs and does not bind them.
3. The co-chairs decide whether to keep the provider or switch, and record the decision
   and its reasons on the issue. If nothing is decided before the review date, the
   current provider stays.
4. A switch takes effect at the start of a billing period. Before it does, each holder
   notes the quota on their grant issue and writes the row for any unit in progress,
   marked incomplete if it is not checked in. The steward then revokes the old
   credentials, issues new ones from the new provider, notes them on each grant issue,
   and updates the manifest in the same change that records the decision.
5. Grants carry over a switch. Because providers meter differently, a grant's amount
   should be stated in currency, or restated in currency at the switch, so that the
   remainder is clear.

The NTAC may hold accounts with more than one provider at once, for example to keep a
fallback when the main provider is unreliable. The manifest then lists each one, and each
grant issue names the provider its credential belongs to.

## 10. The provider manifest

The manifest is a single file in the NTAC admin repository, beside the register (proposed
path: `token-policy/manifest.yaml`). It records the parts of how the NTAC uses tokens that
change when the provider changes, so that switching provider means changing the manifest,
not the policy. Template E is an outline.

The manifest records:

- the policy version it applies to;
- each provider in use, with the plan or tier, the account holder and the billing period;
- the unit the provider meters in, and how that converts to currency for the ledger;
- the workspaces or groups and their limits, and the default limit for a new grant;
- the notification thresholds the provider is set to, and who receives each;
- where the steward gets the usage report, and in what form;
- the coding agents and models approved for use with each provider (the names used in
  `Assisted-by` trailers, template D);
- the hooks or settings holders should use to note the quota at the start and end of
  work;
- the credential replacement interval (section 3.3);
- the vendor review cadence and the date of the next review.

Rules for the manifest:

- **No secrets.** It never holds a credential, a key or an account password, only names,
  identifiers and settings.
- **One owner.** The steward keeps it current. Each change is a pull request reviewed by a
  co-chair, and a change of provider links the review issue that decided it (9.4).
- **Readable by agents.** It is plain, structured text, so a holder's agent can read the
  policy and the manifest at the start of a plan and follow both without being told
  provider details by hand.
- **The policy wins.** Where the manifest and this policy disagree, the policy applies and
  the manifest is corrected.

## Templates

### A. Grant issue

```
Title: Token grant request: <holder> / <project>

Holder (name, GitHub login):
Sponsor (NTAC member, if the holder is not one):
Project (repository, or work item and the repository that receives its work):
Goal (one sentence):
Amount (tokens or currency):
Period (start, end):
Plan location (once written):
I have read the NTAC Token Use Policy and will keep the ledger current: yes

--- for the co-chairs / steward ---
Decision (approved / reduced to <amount> / declined), by whom:
Grant identifier:
Credential identifier (never the credential):
Quota noted at the very beginning of the work:
Quota refreshes during the work (when, and the quota after each):
Plan closed (date, total consumed, quota noted directly after completion or stop):
Closure (date, reason, total consumed):
```

### B. Ledger rows

Each row records: the date; the holder; the grant; the project; the plan (repository and
path); the unit, review round or fix; the amount consumed, as the provider's usage view
shows it; the commits or pull request that checked the unit in; and a note where one is
needed, such as abandoned, incomplete, or which earlier row this one corrects.

Four rows of one grant, as examples:

- 20 November, login, G-007, niem-naming-design-rules, plan PLANS/ndr-literals.md, unit
  U3, 1.84 M consumed, checked in as a1b2c3d and e4f5a6b.
- 21 November, the same holder, grant, project and plan, review round 2, 0.31 M consumed.
- 22 November, the same, unit U4, 0.40 M consumed, not checked in; note: abandoned,
  continued as U7.
- 23 November, the same, unit U3, 1.80 M consumed, checked in as a1b2c3d and e4f5a6b;
  note: corrects the row of 20 November, where the amount was misread as 1.84 M.

The quota notes go on the grant issue, for example: 42.0 M at the start on 20 November;
refreshed to 50.0 M on 22 November; 47.9 M directly after completion on 25 November.

### C. Plan outline

```
# <Plan title>
Goal: <one sentence>
Grant(s): <identifiers>
Repository: <name>
Quota at the very beginning of the work: <amount, date>
Quota refreshes during the work: <when, and the quota after each>

Scope: what is in
Declined list: what was considered and left out, and why
Units: a table of unit, change, acceptance check, depends on; the total count
Known unknowns: each with how it will be resolved and who decides
Blind spots: what the plan does not examine, and what happens if something is found there
Review log: round, reviewer, commit reviewed, findings by severity, what was done
Amendments: what changed, the evidence, who approved, which round re-reviewed it
Status: planned | converged | implementing (unit k of n) | amended, in re-review | implemented
```

### D. Commit trailers

- `Unit: <plan> / U<k>` and `Grant: G-<nnn>` on each commit of a unit.
- `Assisted-by: <tool>:<model>` when the content was materially generated by an agent.

### E. Provider manifest

```yaml
# token-policy/manifest.yaml
policy_version: "0.1"
steward: "<GitHub login>"

providers:
  - name: "<provider>"
    plan: "<team or organization plan, tier>"
    account_holder: "<who holds the contract with the provider>"
    billing_period: "monthly, starting on day <n>"
    metering_unit: "<the provider's unit>"
    currency_conversion: "<how units convert to currency for the ledger>"
    data_settings: "<retention, and that training on inputs is off>"
    workspaces:
      - name: "<workspace or group>"
        limit: "<amount per billing period>"
    default_grant_limit: "<amount>"
    notifications:
      - at: "75% of limit"
        to: [holder]
      - at: "100% of limit"
        to: [holder, steward]
    usage_report: "<where the steward gets it, and the format>"
    approved_agents:
      - tool: "<coding agent>"
        models: ["<model>"]
    quota_hooks: "<the hook or setting holders use to note the quota>"

credential_replacement_days: 90

vendor_review:
  cadence: "monthly, before the billing period starts"
  next_review: "<date>"
  last_decision: "<link to the review issue>"
```

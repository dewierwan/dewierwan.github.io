---
name: access-check
description: Finds content about an incoming person in shared chat and knowledge spaces and recommends what to restrict first. Use when adding a new hire or advisor, or checking before you add someone.
---

# Check before granting access

Use this workflow before adding a new hire, advisor, contractor or collaborator to a shared chat workspace, a knowledge base, or both. It answers one question: **once they join, could they read anything about themselves that should not be visible to them?** It then recommends what to restrict, move or redact before you grant access.

## Quick version

- List every way the person might be written about: full name, surname alone, first name, nicknames, likely misspellings and their chat handle.
- Write down exactly what they will be able to see: which channels, spaces and shared databases. Everything else is out of scope.
- Search each visible space yourself for every name variant. Paste the relevant hits (with their location and link) into your assistant. Include whole threads, not just the first message.
- Ask the assistant to rate each hit: **▲ Hide** (fix before they join), **◆ Consider** (your call), **○ Fine** (checked, harmless). Flag anything they would find hurtful, misleading or awkward, or that reveals plans about them they do not know about.
- Ask for a short report that leads with the count of ▲ and ◆ items and whether anything blocks access today, with one linked item per finding.
- Change nothing until you have decided. After fixing, search again to confirm nothing visible remains.

## 1. Set the scope and gather inputs

Look only for content that mentions the incoming person directly. Ignore other sensitive material, however interesting, unless it is about them.

Run this only if you are authorized to manage access to these systems, such as a workspace admin or the person's sponsor, and search only the systems the person is about to join. Quote only the line needed to judge a finding; for health, family or other personal-life details, name the category (for example "mentions a family matter") instead of repeating it. Send the report only to the requester, never to a shared space.

| Input | Why it matters |
|---|---|
| Full name, nicknames, likely misspellings | Catches mentions that exact-name search misses |
| Chat user ID or handle, if they already have one | Catches tagged mentions |
| A disambiguator, such as current or past employers | Rules out people with the same name |
| Which private channels and restricted spaces they will join | Defines what they can actually see |

If the requester says "standard team-member access", assume every public channel and every open knowledge-base space, with no private channels.

## 2. Identify the person

1. Look up the person in the user directory of each system.
2. Many first names are shared. Keep the disambiguator handy and drop namesakes as you go.
3. List the spelling variants you will search (for example a surname with swapped vowels or a missing letter).

## 3. Map what they will and will not see

This decides what counts as exposed. Skip what they cannot see, but say what you skipped.

- **Usually not visible:** direct messages and group messages they are not in; private channels they will not join; the requester's personal or private spaces and databases (if the requester excludes them); pages in another user's private section.
- **Usually visible:** public channels; private channels they will join; every page in shared spaces and shared databases, including meeting notes, hiring, strategy, projects and archives.

Rules for unclear cases:

- **Keep a list of the requester's private locations.** Ask which databases or folders are private to them, and recognize search hits by the location path shown. Private locations get renamed, so record former names too, and treat a hit under any of them as not visible.
- **Search tools often cannot see page-level permissions.** A page may be restricted while still sitting in a shared database, and search returns it anyway. Treat every page in a shared space as visible unless the requester confirms it is restricted. Then move it to the skipped list as "restricted, confirmed by requester".
- **Pages with no parent location** (for example auto-generated meeting notes) are often private to their creator. Treat them as not visible unless they show explicit sharing or the requester says otherwise.
- **System-generated user profile pages** usually carry no content. Skip them. An access error on them is expected and not worth reporting.

## 4. Search the chat workspace

Cover every channel you are allowed to search:

- Full name, surname alone, and each misspelling, newest first. Page through results until they stop being about the person.
- First name alone, to catch casual mentions. Skim for context and drop namesakes.
- Their user ID as a keyword, to catch tagged mentions.
- Any announcement about adding them. Read the full thread, since colleagues may have replied with concerns.

For each relevant hit, record the channel type and a permanent link. Read the full thread around any hit that has replies. Direct messages are not visible to the person, but list them with links in the skipped section so the requester knows they were seen.

## 5. Search the knowledge base

1. Search the full name, each misspelling, and the name combined with their main employers or role. Ask for a large page of results.
2. If the requester's private space is excluded, run the same search limited to that space. Hits that appear only there are out of scope.
3. Open every remaining hit that mentions the person beyond a passing name-drop. Read the full text and check its location against your visibility map.
4. Check structured properties as well as body text: hiring status fields, pipeline stages, contact-relationship fields, and similar.
5. If a page fails to open, report it with its link and ask the requester to check it by hand.

## 6. Judge each mention

Flag a mention when the person would plausibly feel hurt, misled or awkward reading it, or when it reveals plans about them that they do not know about.

**Flag:**

- Candid assessments: doubts about their skills, commitment or results.
- Hiring, offer, compensation or persuasion strategy aimed at them, including records marking them as a lost or declined candidate.
- Other people's plans for them that they may not know about.
- Reference feedback, gossip, or health, family or personal-life details.
- Colleagues' doubts about what they contribute.

**Do not flag:**

- Neutral mentions: event replies, being tagged on a link, a field recording who introduced them.
- Praise and accurate bios.
- Their own advice recorded in meeting notes. **Exception:** if those notes include their candid remarks about third parties, mention this once. They may not expect those remarks to sit in a team-wide space.

Rate every finding with a word and a symbol, never colour alone:

| Rating | Meaning |
|---|---|
| **▲ Hide** | Restrict, move or redact before they join |
| **◆ Consider** | Mild; the requester decides |
| **○ Fine** | Checked and harmless; listed briefly for completeness |

## 7. Report

Lead with the answer: the number of ▲ and ◆ items, and whether anything blocks granting access today. Then list one item per finding:

- Bold rating, then the page or message label as a short hyperlink (for example `[#announcements, 4 Oct](link)`), never a bare URL
- Where it lives, and whether the person would see it
- The exact line that matters (or the category, for sensitive personal details)
- Recommended fix: restrict the page, move it to a private space, or redact one line

Every item gets its own working link, including **○ Fine** items and skipped direct messages. The requester will check each one, so an item without a link is not useful. Close with failed fetches and the list of what was skipped as not visible.

**Invented example.** Before adding Jordan Vale, a fictional advisor from the fictional Maple Street Studio:

> **1 ▲, 1 ◆. One item blocks access today.**
>
> - **▲ Hide** [Hiring pipeline: Jordan Vale](link). Hiring space, visible. Status field "Declined, revisit later"; note: "unsure about follow-through." Fix: restrict the page.
> - **◆ Consider** [Advisory board planning](link). Strategy space, visible. "Jordan might push for equity; hold firm." Fix: redact the line.
> - **○ Fine** [#announcements, 4 Oct](link). Welcome post, all positive replies.
>
> Skipped as not visible: 2 direct messages ([1](link), [2](link)); 1 page in a private meeting database ([link](link)).

## 8. Make changes

Do not change permissions, move pages or edit content without explicit approval. Moving or redacting someone else's page is a material change, so confirm with its owner where appropriate. Prefer restricting access over deleting, and do not delete or alter records under a retention duty, a legal hold, or the person's legal right to access data about them; if unsure, flag it for the right owner. After approval, make the edits, then re-run the searches to confirm nothing visible remains.

## Common failure modes

- Searching only the exact name and missing misspellings, nicknames or tagged IDs.
- Confusing a namesake with the person.
- Assuming a page is private because search cannot show its permissions.
- Missing a private location because it was renamed, or reporting it as exposed.
- Reading only the first message and missing a critical reply in the thread.
- Missing sensitive content stored in page properties rather than body text.
- Acting on findings before approval.

## Optional extras

- **Parallel searches.** With an agent connected to your chat and knowledge tools, run all name variants at once and ask for detailed results so each hit comes back with a permanent link.
- **Scoped exclusion search.** If your knowledge tool can limit search to one space, use it to separate hits in the requester's private space from hits in shared spaces, instead of guessing from titles.
- **Reusable location list.** Keep a short note of private locations (current and former names), shared databases and typical access bundles, so each check starts from an accurate visibility map.
- **Re-check routine.** After fixes, have the agent re-run the same saved queries and report only items still marked ▲ or ◆.

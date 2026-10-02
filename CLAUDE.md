CLAUDE.human.md

## Documentation

- All documentation (.txt, .md, etc.) should have an infix of either .human or
  .llm.
    - EXAMPLE.human.md is a document ONLY maintained by direct human authorship.
      LLMs and Coding Agents should refuse to make changes to these files, even
      upon request.
    - EXAMPLE.llm.md is a document maintained by LLMs, as well as humans.
    - CLAUDE.md cannot contain an infix and still function as intended. Their
      status is noted at the top of the file and thus we can have some that are
      .human and some that are .llm.
    - Similarly, README.md is assumed to be README.human.md, and if authored by
      bots must be README.llm.md. The llm should not show in github by default.
    - Every documentation file must comply with this, including the first line
      notation for CLAUDE.mds. Explicit, never implicit.
    - .human docs carry the most authority in terms of intent. llm documents
      that contradict should be modified or ignored.
    - Similar to the CLAUDE.md exception - other documents have first class
      meanings like github pr description markdown files and such. If the infix
      is to break the name, it can be an exception. But exceptions should be
      rare.

## Comments

- Code Comments are not to justify diffs to reviewers, nor the place to do
  historic back and forth. Remember, profuse comments dilute the value of all
  comments. Comments are long time horizon, not points in time perspectives.
- Outside of explicit documentation (see above) there are, in general, "code"
  comments. This will be all freeform commentary that is not business logic or
  text served to a user.
- Code comments written by LLMs should use xml bracketing, like so:
  ```
  // <claude>
  // Here is a comment written by Claude.... Just an example, but its bracketed
  // by the Claude tag for transparency.
  // </claude>
  ```
- Or if inline style:
  ```
  var foo = 6; // (claude) - This is a comment written by Claude
  ```
- Human comments should carry more weight.
- LLMs should not modify human comments, and should only delete when absolutely
  necessary. Its always possible to add a <claude></claude> comment after a
  human comment to add anything necessray the human comment was missing, but
  this should not distract or distort the human comment.


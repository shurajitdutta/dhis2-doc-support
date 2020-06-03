# Suggested workflow to contribute to area specific documentation

The following sequence diagram, drawn using mermaid.js illustrates in a simplified way how collaborators should contribute to a specific area documentation such as DHIS2 COVID19 Documentation or DHIS2 Android App.

We haven't found a way to display mermaid.js diagrams in Github yet, therefore we are using the [mermaid.js Live Editor](https://mermaid-js.github.io/mermaid-live-editor/) to generate an image a putting it in the documentation.

Feel free to copy the code below and paste it in the [mermaid.js Live Editor](https://mermaid-js.github.io/mermaid-live-editor/) to try it out.

```mermaid
sequenceDiagram
    autonumber
    participant A as docs.dhis2.org
    participant B as Area specific documentation Repo
    participant C as Contributor Repo
    participant D as Contributor's Machine
    participant E as Transifex
    Note over B: Contributor wants to contribute
    alt fork
      B->>C: creates a fork
    else create a new repo
      B->>C: creates a repo from template
    end
    C->>D: clones the repo
    loop repeats for each commit
      Note over D: Contributor starts to contribute
      activate D
        D->>D: creates a branch
        D->>D: creates or edits a document
      deactivate D
      Note over D: Contributor wants to share
      D->>D: stages the contribution
      D->>C: pushes the contribution
      C->>C: merges to master branch
      C->>B: create a Pull request to merge
      opt when identified
        A->>A: create an issue for publication
      end
    end
    opt when identified
      alt if kept as a standalone documentation project
        B->>E: updates related project for translation
      else if integrated to docs.dhis2.org
        A->>E: updates related project for translation
      end
      E->>E: translates strings
      alt if kept as a standalone documentation project
        E-->>B: pulls translated strings
      else if integrated to docs.dhis2.org
        E-->>A: pulls translated strings
      end
    end
```

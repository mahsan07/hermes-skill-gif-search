# How Gif Search Works

Search and download GIFs from Tenor through a controlled command-line workflow.

![Detailed systems blueprint for Gif Search](../assets/system-blueprint.png)

## Stages

### 1. Convert intent into concise search terms

**Primary surface:** `Search phrase`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 2. Query Tenor with a bounded result count

**Primary surface:** `Tenor search endpoint`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 3. Inspect previews dimensions and source links

**Primary surface:** `Relevance and content filter`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 4. Filter irrelevant or unsafe results

**Primary surface:** `Preview candidates`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 5. Download only the selected asset

**Primary surface:** `Downloaded GIF`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 6. Report attribution and local path

**Primary surface:** `Downloaded GIF`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.

## Failure handling

- **Authorization failure:** do not probe credentials or broaden access; report the missing authority.
- **Target ambiguity:** stop before mutation and request the minimum identifying information.
- **Tool or service failure:** retain error evidence, retry only safe transient failures, and cap retries.
- **Verification failure:** classify the run as incomplete even when the preceding operation returned success.

## Completion evidence

The handoff should contain the original request, inspection state, preview or plan, exact execution result, direct verification, and a final receipt naming limitations and withheld actions.

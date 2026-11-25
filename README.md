# Summary annotation pilot

Annotation tool for the pilot study on evaluating summaries of research papers (HPLT 4.0, TurkuNLP collaboration).

**Open the tool:** https://anilkus.github.io/summary-annotation-pilot/

- The summary and the source paper are shown side by side, with a search box for the paper
- Rubric: grammatical correctness, self-contained, coherence, conciseness, coverage (yes/no questions, labels computed automatically)
- Texts are in random order and their sources are hidden
- Progress is saved in your browser. **Export JSON** saves your annotations to a file, **Import annotations** loads that file back (e.g. on another computer)

The page comes with the Turkish pilot set built in (10 papers, 40 texts).

## Loading another set of papers and summaries

Use **Load data** and pick a JSON file, or put the file in this repo and share a link like
`https://anilkus.github.io/summary-annotation-pilot/?data=english_pilot.json`.
Annotations for each set are stored separately. **Use built-in data** switches back to the Turkish set.

Format:

```json
{
  "name": "english-pilot",
  "papers": { "1": "full text of paper 1", "2": "full text of paper 2" },
  "items": [
    { "item_id": "T01", "paper_no": 1, "text": "a summary of paper 1" },
    { "item_id": "T02", "paper_no": 2, "text": "a summary of paper 2" }
  ]
}
```

`name` and `item_id` are optional. Keep the mapping from item to source model in a separate file so annotators don't see it.

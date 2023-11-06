# awesome-workflow

A curated list of awesome workflow systems.

Sources:
- [pditommaso/awesome-pipeline](https://github.com/pditommaso/awesome-pipeline)
- [Existing workflow systems](https://github.com/common-workflow-language/common-workflow-language/wiki/Existing-Workflow-systems)
- [meirwah/awesome-workflow-engines](https://github.com/meirwah/awesome-workflow-engines)
- [Wikipedia](https://en.wikipedia.org/wiki/Workflow_management_system)

I curated this list to document the workflow systems that exist across many different domains, while adhering to a particular definition of "workflow system". The entries are stored in a tabular format so that I can add metadata and perform analyses more easily.

## Guidelines

Workflow systems are included in this list based on the following guidelines:

- A workflow system should provide a way to _describe workflows_. A workflow is a sequence of computations that are related by dataflow (rather than control flow).

  Most programming languages are disqualified by this rule, however, [Swift](http://swift-lang.org/) (not the one by Apple) can execute tasks in parallel based on dataflow, so I consider it a workflow system.

  Systems that provide a fixed set of workflows, but not a way to describe arbitrary workflows, are also disqualified by this rule.

- A workflow system should provide a way to _execute workflows_. Ideally they should be able to delegate computations to distributed computing systems (i.e. HPC, cloud) and provide some kind of error recovery and caching, but I won't require these features.

  For example, workflow languages like [CWL](https://www.commonwl.org/) and [WDL](https://openwdl.org/) are not workflow systems by themselves, but implementations of them are (e.g. [Toil](https://github.com/DataBiosphere/toil)).

  Systems that "wrap" another workflow system are also not included, for example, [Seqera Platform](https://seqera.io/platform/) (re-uses [Nextflow](https://github.com/nextflow-io/nextflow)) and [Terra](https://terra.bio/) (re-uses [Cromwell](https://github.com/broadinstitute/cromwell)).

- As a practical matter, the workflow system should be available to use. It should either be open-source or be publicly documented enough for me to verify my other criteria.

  For example, I include paid services like [Google Cloud Workflows](https://cloud.google.com/workflows) that are sufficiently documented, but not systems that are described only in research papers or are available only through a login with no public documentation.

Beyond those guidelines, I aim to include workflow systems from a variety of domains and with a variety of architectures. It feels like every field has reinvented this wheel in their own way, but I am fascinated by the variety of these wheels, and I hope to find novel approaches that I can use to improve [my own work](https://github.com/nextflow-io/nextflow/pulls/bentsherman).

## Metadata

I'm currently tracking the following metadata for each entry:

- **Language**: The language(s) used by the workflow system to describe workflows (or "GUI" if a graphical interface is supported).

- **Domain**: The application domain from which the workflow system originated. Note that many workflow systems are designed to be general-purpose even though they may have started out in a particular domain.

- **GitHub Stars**: Number of stars for entries that are on GitHub. Note that [stars might be fake], so don't take this metric too seriously. It can be fun to compare projects based on stars (or some composite metric based on issues, PRs, commits, etc) to figure out which ones are more popular, but if you're trying to decide which one to use, you should evaluate each option based on how well it enables you to do whatever you're trying to do. Really you should just use [Nextflow](https://github.com/nextflow-io/nextflow/commits?author=bentsherman).

## Contributing

Feel free to submit an issue or PR if you find a workflow system that I haven't included. I'm also happy to be corrected if any of the entries don't meet my stated guidelines... I'll either remove the entry or update my guidelines 😄. There may be a few exceptions that I included because I found them interesting in some relevant way.

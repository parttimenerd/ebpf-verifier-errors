# A Collection of eBPF Verifier Errors

eBPF verifier errors can be cryptic and are often hard to understand.
So how can we help new developers when they encounter them?
Let's collect verifier error messages, their code context, 
and how they can be resolved.
This collection can then be searched by others and used
as a data source for tooling.

The errors are collected in the form of 
[issues](https://github.com/parttimenerd/ebpf-verifier-errors/issues) to this
repository.

Please consider submitting your verifier errors today.

## How to submit?

Just [create an issue with the "New Verifier Error" issue template](https://github.com/parttimenerd/ebpf-verifier-errors/issues/new?assignees=&labels=submisson&projects=&template=new-verifier-error.md):

[![image](https://github.com/user-attachments/assets/fd5c9585-640b-41ac-85f1-33bad87b9475)](https://github.com/parttimenerd/ebpf-verifier-errors/issues/new?assignees=&labels=submisson&projects=&template=new-verifier-error.md)

### How to get all issues?

You can use the following bash script to obtain
all currently available issues:

```sh
curl -s "https://api.github.com/repos/parttimenerd/ebpf-verifier-errors/issues?labels=submission" \
     | jq -r '.[] | "\(.title)\n\(.body)\n-----"'
```

If you experience rate-limiting issues, try using a personal GitHub token:

```sh
curl -s -H "Authorization: token your_github_token_here" \
         "https://api.github.com/repos/parttimenerd/ebpf-verifier-errors/issues?labels=submission" \
     | jq -r '.[] | "\(.title)\n\(.body)\n-----"'
```

## Contribute
To contribute to the repository other than submitting
verifier issues, please open a [GitHub Discussion](https://github.com/parttimenerd/ebpf-verifier-errors/discussions)
or a [pull request](https://github.com/parttimenerd/ebpf-verifier-errors/pulls).
We're happy for any issues template improvements or additions
of tools that use the data.

## License
GPLv2, this also includes the GitHub issues

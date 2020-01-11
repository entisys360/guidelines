# Styleguide
> Organization-wide coding, style and configuration guidelines

## Guidelines

- 2 spaces for indentation

- Insert newlines between modules

```shell
modules:
  - name: module-one
    sources:
      - type: archive
        url: 'https://example.org'
 
  - name: module-two
    sources:
      - type: archive
        url: 'https://example.org'

  - name: module-three
    sources:
      - type: archive
        url: 'https://example.org'
```

- Always indent child elements

```shell
# GOOD:
modules:
  - name: foo
    sources:
      - type: bar

# BAD:
modules:
- name: foo
  sources:
  - type: bar
```

- Do not align values

Aligning values means you have to have automated tooling to sanely format it and 
many simple changes result in full file modifications making diffs harder to 
review, revert, or otherwise manage.

```shell
# BAD:
id:           org.example.Foo   
modules:
  - name:     foo
    sources:
      - type: git
```


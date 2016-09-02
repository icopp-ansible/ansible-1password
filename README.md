# ansible-1password

Install 1Password via the Mac App Store or Homebrew. Does nothing on non-macOS platforms.

## Role Variables

* `prefer_mas_over_homebrew`: Defaults to `false`.

## Dependencies

* [icopp.mas-cli](https://github.com/icopp/ansible-mas-cli) (included as repository dependency), but only if `prefer_mas_over_homebrew` is `true`.
* [icopp.homebrew](https://github.com/icopp/ansible-homebrew) (included as repository dependency), but only if `prefer_mas_over_homebrew` is `false`.

## Example Playbook

```
  - hosts: all
    roles:
      - role: icopp.1password
```

```
  - hosts: all
    roles:
      - role: icopp.1password
        prefer_mas_over_homebrew: true
```

## License

MIT

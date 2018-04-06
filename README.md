# trellis-backup-during-deploy

[![GitHub tag](https://img.shields.io/github/tag/ItinerisLtd/trellis-backup-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-backup-during-deploy/tags)
[![license](https://img.shields.io/github/license/ItinerisLtd/trellis-backup-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-backup-during-deploy/blob/master/LICENSE)


Backup WordPress database during [Trellis](https://github.com/roots/trellis) deploys.

## Requirements

- Trellis [9dfddfd](https://github.com/roots/trellis/commit/9dfddfd0d5f7d10886d2f434c02d3bd23edb8684) or later
- Ansible v2.4 or later


## Installation

Add this role to `requirements.yml`:

```yaml
# requirements.yml
- src: git+https://github.com/ItinerisLtd/trellis-backup-during-deploy.git
  version: master # Check for latest version!
```

Add this role to the [`deploy_initialize_after` hook](https://roots.io/trellis/docs/deploys/#hooks):
```yaml
# group_vars/all/deploy-hooks.yml
# Learn more on https://roots.io/trellis/docs/deploys/#hooks
deploy_initialize_after:
  - "{{ playbook_dir }}/vendor/roles/trellis-backup-during-deploy/tasks/main.yml"
```


## Author Information

[trellis-backup-during-deploy](https://github.com/ItinerisLtd/trellis-backup-during-deploy) is a [Itineris Limited](https://www.itineris.co.uk/) project created by [Tang Rufus](https://typist.tech).

Special thanks to [the Roots team](https://roots.io/about/) whose [Trellis](https://github.com/roots/trellis) make this project possible.

Full list of contributors can be found [here](https://github.com/ItinerisLtd/trellis-backup-during-deploy/graphs/contributors).

## Feedback

**Please provide feedback!** We want to make this library useful in as many projects as possible.
Please submit an [issue](https://github.com/ItinerisLtd/trellis-backup-during-deploy/issues/new) and point out what you do and don't like, or fork the project and make suggestions.
**No issue is too small.**

## Change log

Please see [CHANGELOG](./CHANGELOG.md) for more information on what has changed recently.

## License

[trellis-backup-during-deploy](https://github.com/ItinerisLtd/trellis-backup-during-deploy) is released under the [MIT License](https://opensource.org/licenses/MIT).

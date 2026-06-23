<div align="center">

# ClassCharts API · Python

### An unofficial Python client for the ClassCharts student API.

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyPI](https://img.shields.io/pypi/v/classcharts?style=for-the-badge)

</div>

> ⚠️ **Unofficial.** This project is not affiliated with, endorsed by, or supported by ClassCharts / Edukey. It talks to the same endpoints the website uses, which can change at any time. Use it for your own data only.

## Install

```bash
pip install classcharts
```

It uses [`requests`](https://pypi.org/project/requests/), but the package doesn't declare it as a dependency yet — install it alongside:

```bash
pip install requests
```

## Usage

```python
from classcharts.clients import StudentClient

client = StudentClient("YOUR_STUDENT_CODE", "2000-01-01")  # date of birth: YYYY-MM-DD
client.login()

# the session keeps itself alive and refreshes automatically
```

`StudentClient` logs in with the same **student code + date of birth** you'd use on the ClassCharts student site, and refreshes its session in the background.

## Status

This is an **early (`0.0.1`)** release — the student login flow works; higher-level helpers are still being built out.

### Clients
- [x] Student client
- [ ] Parent client
- [ ] Automatic re-login after session timeout

### Data helpers
Convenience wrappers for these are planned but not all implemented yet:

- [ ] Announcements
- [ ] Homework & homework statuses
- [ ] Behaviour points
- [ ] Rewards
- [ ] Student information
- [ ] Timetable (lessons & day timetable)

> A Java version of this library also exists: [classcharts-api-java](https://github.com/duzos/classcharts-api-java).

## Links

- [PyPI](https://pypi.org/project/classcharts/)
- [GitHub](https://github.com/duzos/classcharts-api-python)

## Credits

By [Duzo](https://duzo.is-a.dev/).

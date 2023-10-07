# AD3 Tutorials

This is a repository containing tutorial materials for AD3 discoveries and apps.

## Directory structure

```
./
  README.md
  apps/
    _short_description/  # short description of every AD3 app in a single Markdown file
      {en,ko}.json       # each key shall be the app's development name (dev_name) defined in backend server
    {dev_name}/          # collection of files required for AD3 app
                         # Note. dev_name is the app's development name defined in backend server.
      {en,ko}/
        README.md        # help page
        submission.json  # (optional) displayable strings in submission page
  examples/              # example files linked by README.md above
                         # Note. No file shall be here.
  legals/
    {en,ko}.md           # mandatory legal notice for third party software use in front/back-end servers
  terms/
    privacy-policy/      # 개인정보 보호정책
      {version}/         # a version of x.yy format where x is major and yy is minor
        {en,ko}.md
    terms-of-service/    # 서비스 약관
      {version}/         # a version of x.yy format where x is major and yy is minor
        {en,ko}.md
  videos/                # video files linked by frontend server
                         # Note. No file shall be here.
```

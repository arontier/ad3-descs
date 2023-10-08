# AD3 Tutorials

This is a repository containing tutorial materials for AD3 discoveries and apps.

## Directory structure

```
./
  README.md
  apps/
    _metadata_all_at_once_/  # metadata of every AD3 app in a single Markdown file
      {en,ko}.json           # Note. Each key shall be the app's development name (dev_name) defined in backend server.
    {dev_name}/              # collection of files for AD3 app used in frontend server
                             # Note. dev_name is the app's development name defined in backend server.
      {en,ko}/
        README.md            # help page used in frontend server
        submission.json      # (optional) displayable strings in submission page used in frontend server
  examples/                  # example files linked by README.md above
                             # Note. No file shall be here. (They can be too big for GitHub.)
  legals/
    {en,ko}.md               # mandatory legal notice for third party software used in front/back-end servers
  terms/
    privacy-policy/          # 개인정보 보호정책
      {version}/             # a version of format x.yy where x is major and yy is minor
        {en,ko}.md
    terms-of-service/        # 서비스 약관
      {version}/             # a version of format x.yy where x is major and yy is minor
        {en,ko}.md
  videos/                    # video files linked by frontend server
                             # Note. No file shall be here. (They can be too big for GitHub.)
```

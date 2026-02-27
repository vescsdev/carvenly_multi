# carvenly

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Learn Flutter](https://docs.flutter.dev/get-started/learn-flutter)
- [Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Flutter learning resources](https://docs.flutter.dev/reference/learning-resources)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## iOS Launch Workflow (VS Code)

If VS Code stays on `Flutter: Launching...` for iOS simulator runs, do this once
after Flutter SDK updates (or after clearing caches):

```bash
flutter precache --ios
flutter pub get
```

Then run:

```bash
flutter run -d ios
```

This avoids first-run iOS artifact downloads from happening during VS Code launch.

## Mac + Windows Git Sync Workflow

Use GitHub as the single source of truth for both machines.

1. Start from latest shared branch:

```bash
git checkout master
git pull --ff-only
```

2. Create a feature branch for each task:

```bash
git checkout -b feat/<short-task-name>
```

3. Commit and push often:

```bash
git add .
git commit -m "<message>"
git push -u origin feat/<short-task-name>
```

4. Open a PR and merge into `master`.
5. On the other machine, pull `master` before continuing work.

Conflict handling:

```bash
git fetch origin
git rebase origin/master
```

Use `git push --force-with-lease` only for your feature branch after rebase. Never force-push `master`.

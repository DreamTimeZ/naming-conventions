# File Naming Conventions

## Table of Contents

- [File Naming Conventions](#file-naming-conventions)
  - [Table of Contents](#table-of-contents)
  - [📘 Naming Pattern Reference](#-naming-pattern-reference)
    - [Core Elements](#core-elements)
    - [Additional Document Elements](#additional-document-elements)
    - [Additional Elements (for all but for Document)](#additional-elements-for-all-but-for-document)
    - [Additional Data Elements](#additional-data-elements)
    - [Additional Script Elements](#additional-script-elements)
    - [Additional Image Elements](#additional-image-elements)
    - [Additional Audio Elements](#additional-audio-elements)
    - [Additional Video Elements](#additional-video-elements)
    - [Additional Folder Elements](#additional-folder-elements)
  - [Document Files](#document-files)
  - [Text-Based Files](#text-based-files)
    - [Plain Text Files](#plain-text-files)
  - [Data \& Configuration Files](#data--configuration-files)
    - [Data Files](#data-files)
    - [Configuration Files](#configuration-files)
  - [Archive Files](#archive-files)
  - [Script \& Programming Files](#script--programming-files)
    - [Shell Scripts](#shell-scripts)
    - [Batch Scripts](#batch-scripts)
    - [PowerShell](#powershell)
    - [Programming Languages](#programming-languages)
      - [snake\_case](#snake_case)
      - [camelCase](#camelcase)
      - [PascalCase](#pascalcase)
      - [kebab-case](#kebab-case)
  - [Media Files](#media-files)
    - [Image Files](#image-files)
    - [Audio Files](#audio-files)
    - [Video Files](#video-files)
  - [Folder Naming](#folder-naming)
    - [Cross-Platform Folder Naming Conventions](#cross-platform-folder-naming-conventions)

## 📘 Naming Pattern Reference

### Core Elements

| Element                                  | Req. | Format / Examples                                                                                             | Description                                                                                                                                                                                  |
| ---------------------------------------- | ---- | ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Date`, `date`                           | ✅    | `YYYY-MM-DD`, `YYYY-MM`, `YYYY`<br>`YYYY-MM-DD-YYYY-MM-DD`, `YYYY-YYYY`<br>`YYYY-MM-DD-ongoing`, `until-YYYY` | Date or date range in [ISO 8601](https://de.wikipedia.org/wiki/ISO_8601) format. Choose precision based on context. Avoid special characters; use only `A-Z`, `0-9`, `_`, and `-` in ranges. |
| `[Version]`, `[version]`                 | ⬜    | `v1`, `v2.3`, `v10.01`                                                                                        | Version number. Use when tracking iterations, drafts, or formal releases. Use **kebab-case**.                                                                                                |
| `[Status]`, `[status]`                   | ⬜    | `draft`, `final`, `signed`, `archived`, `encrypted`, `backup`, `legacy`                                       | Document workflow or approval state. Often paired with `Version`. Use **lowercase**.                                                                                                         |
| `[Language]`, `[language]`               | ⬜    | `en`, `de`, `fr`                                                                                              | [ISO 639-1 language code](https://de.wikipedia.org/wiki/Liste_der_ISO-639-Sprachcodes) - Set 1. Use **lowercase**.                                                                           |
| `[Confidentiality]`, `[confidentiality]` | ⬜    | `internal`, `confidential`, `public`                                                                          | Indicates visibility or access level. Required for sensitive documents. Use **lowercase**.                                                                                                   |
| `env`                                    | ⬜    | `dev`, `test`, `prod`, `local`, `stage`, `qa`, `mock`, `training`, `inference`, `demo`, `ci`                  | Environment the data relates to. Use **lowercase**.                                                                                                                                          |

> ✅ `Element` = required  ⬜ `[Element]` = optional
> Only these dates, versions, statuses, confidentialities and envs are allowed.
> All languages on [ISO 639-1 language code](https://de.wikipedia.org/wiki/Liste_der_ISO-639-Sprachcodes) Set 1 are allowed.
> Element can be lowercase or capitalized for consistency and to avoid confusion.
> Delimiter only need to between elements. If there is no other element the delimiter must not be used.
> **The elements must not contains fixed words from other elements.**

### Additional Document Elements

| Element    | Req. | Format / Examples                             | Description                                                                                                                                                                                                                                                |
| ---------- | ---- | --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Subject`  | ✅    | `Project_Plan`, `Q4_Report`, `Annual_Summary` | Central topic, title, or focus of the document. Should summarize the content clearly and concisely. Examples: document title, meeting name, project code, deliverable, report type, presentation focus, or research theme. Use **Capitalized_Snake_Case**. |
| `[Author]` | ⬜    | `Firstname`, `Surname`, `Firstname_Surname`   | Creator or responsible person. Use initials or full name for traceability. Use **Capitalized_Snake_Case**.                                                                                                                                                 |

### Additional Elements (for all but for Document)

| Element   | Req. | Format / Examples                            | Description                                                                                                      |
| --------- | ---- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `subject` | ✅    | `meeting-notes`, `api-reference`, `ml-ideas` | Short, descriptive topic, description or title. Use lowercase and hyphens (-) as separators. Use **kebab-case**. |

### Additional Data Elements

| Element | Req. | Format / Examples                                                                                                  | Description                             |
| ------- | ---- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------- |
| `type`  | ⬜    | `schema`, `dump`, `export`, `import`, `migration`, `snapshot`, `seed`, `backup`, `dataset`, `etl`, `log`, `config` | Nature of file/data. Use **lowercase**. |

> Only these types are allowed.

### Additional Script Elements

| Element  | Req. | Format / Examples                             | Description                                                                                                                                                                                                                                                                                       |
| -------- | ---- | --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `prefix` | ⬜    | `01`, `02`, `10`, `55`, `99`, `XX`            | Optional numeric prefix for ordering shell scripts, especially in init/setup flows. Common in Unix systems to determine execution order.                                                                                                                                                          |
| `Verb`   | ✅    | `Get`, `Set`, `Install`, `Deploy`, `Backup`   | For PowerShell scripts, use an approved verb from the [PowerShell approved verb list](https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands?view=powershell-7.5) to describe the action. Use **capitalized words** (e.g. `Add`). |
| `os`     | ⬜    | `linux`, `macos`, `windows`, `cross`, `other` | Target operating system or compatibility. Use **lowercase**.                                                                                                                                                                                                                                      |

> Only these prefix, os formats are allowed.
> All [PowerShell approved verbs](https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands?view=powershell-7.5) on this offical microsoft documentation are allowed.

### Additional Image Elements

| Element       | Req. | Format / Examples                                                | Description                                                                                                                                         |
| ------------- | ---- | ---------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `figure`      | ⬜    | `figX`, `figXX`, `figXXX`                                        | Use **lowercase**.                                                                                                                                  |
| `contributor` | ⬜    | `john-doe`, `maria-smith`, `artist-a`, `contributor01`, `anon-b` | General-purpose identifier for the person involved in creation or performance (e.g., speaker, presenter, artist, photographer). Use **kebab-case**. |
| `type`        | ⬜    | `photo`, `icon`, `banner`, `scan`, `diagram`                     | Useful for organizing visuals by purpose or source. Use **lowercase**.                                                                              |
| `resolution`  | ⬜    | `2160p`, `3840x2160`, `retina`, `2k`, `4k`, `8k`                 | Denote size or target quality. Helpful when maintaining multiple sizes. Use **lowercase**.                                                          |

> Only these figure formats are allowed.
> The type and the resolut elements are not checked for these specific ones because there are too many and new ones are coming up.

### Additional Audio Elements

| Element     | Req. | Format / Examples                                                 | Description                                                        |
| ----------- | ---- | ----------------------------------------------------------------- | ------------------------------------------------------------------ |
| `type`      | ⬜    | `recording`, `music`, `narration`, `effect`, `ambient`, `dataset` | Describes the purpose or category of the audio. Use **lowercase**. |
| `frequency` | ⬜    | `8k`, `16k`, `22k`, `44k`, `44.1k`, `48k`, `96k`                  | Sample rate in kilohertz (kHz). Use **lowercase** without `Hz`.    |
| `quality`   | ⬜    | `raw`, `normalized`, `compressed`, `lossless`, `proxy`            | Describes audio fidelity or processing state. Use **lowercase**.   |

> For contributor see [Additional Image Elements - contributor](#additional-image-elements).

### Additional Video Elements

| Element | Req. | Format / Examples                                                                   | Description         |
| ------- | ---- | ----------------------------------------------------------------------------------- | ------------------- |
| `type`  | ⬜    | `recording`, `interview`, `presentation`, `screencast`, `vlog`, `youtube`, `b-roll` | Use **kebab-case**. |

> For resolution see [Additional Image Elements - resolution](#additional-image-elements).
> For quality see [Additional Audio Elements - quality](#additional-audio-elements).
> For contributor see [Additional Image Elements - contributor](#additional-image-elements).

### Additional Folder Elements

> For prefix see [Additional Script Elements - prefix](#additional-script-elements)

## Document Files

- `Date_Subject_[Author]_[Version]_[Status]_[Language]_[Confidentiality].ext`

| Type       | Extension | Examples                                                                                                          |
| ---------- | --------- | ----------------------------------------------------------------------------------------------------------------- |
| PDF        | `.pdf`    | `2023-06-30_Annual_Report_v1_final_en_internal.pdf`<br>`2024-01-15_User_Manual.pdf`                               |
| Word       | `.docx`   | `2016-01-04_ProjectA_Meeting_Notes_Smith_v2_draft_en.docx`<br>`2025-03-12_Meeting_Minutes.docx`                   |
| Excel      | `.xlsx`   | `2022-10-05_Budget_Spreadsheet_MM_v1_final_en_confidential.xlsx`<br>`2023-04-20_Financial_Projections.xlsx`       |
| PowerPoint | `.pptx`   | `2022-11-02_Alice_Smith_Influence_Strategies_v2_final_en.pptx`<br>`2023-07-01_Quarterly_Results_v1_draft_en.pptx` |
| RTF        | `.rtf`    | `2023-01-15_Project_Requirements_Bob_v1_draft_en_internal.rtf`<br>`2024-02-05_Meeting_Notes.rtf`                  |

## Text-Based Files

### Plain Text Files

- `[date]-subject-[version]-[status].ext`
- **kebab-case**
- **Exceptions:** Uppercase for special files like `README`, `COPYING`, `LICENSE`, etc.

| Type     | Extension | Examples                                                                     |
| -------- | --------- | ---------------------------------------------------------------------------- |
| Text     | `.txt`    | `2025-05-18-project-description-v1.txt`, `ml-ideas.txt`                      |
| Markdown | `.md`     | `2025-05-api-reference-v2.md`, `2025-03-project-notes-final.md`, `README.md` |

## Data & Configuration Files

### Data Files

- **IMPORTANT:** The subject must be in **snake_case**.
- `[date]_subject_[type]_[env]_[version]_[status]_[confidentiality].ext`
- **snake_case** but the `date`

| Type     | Extension        | Examples                                                                                                                |
| -------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------- |
| CSV      | `.csv`           | `2025-05-18_survey_responses_export_prod_v2_final_internal.csv`, `2024-12_sales_backup_dev_v1_draft.csv`                |
| Database | `.db`, `.sqlite` | `2025-04-30_user_database_snapshot_prod_v3_encrypted_confidential.db`, `2025-05-01_app_data_seed_local_v1_final.sqlite` |

### Configuration Files

- Whether to use `-` or `_` depends on the environment.
  - yaml, ini consistent with the rest.
  - **But I like to stick with `-`.**
- `[date]-subject-[env]-[version]-[status].ext`
- **kebab-case**
- **Exceptions:** `compose.yaml`, `env.local`, `config_prod.py`, etc.

| Type     | Extension | Examples                                                                   |
| -------- | --------- | -------------------------------------------------------------------------- |
| XML      | `.xml`    | `app-settings-prod-v1-final.xml`, `2023-01-15-database-schema-prod-v3.xml` |
| JSON     | `.json`   | `api-config-dev-v2.json`, `2025-05-18-user-data-prod-v1-final.json`        |
| YAML/YML | `.yaml`   | `app-config-production.yaml`, `2025-05-01-deploy-config-stage-v2.yaml`     |
| INI      | `.ini`    | `postgresql-dev-v1.ini`, `2024-12-30-server-config-prod-final.ini`         |
| TOML     | `.toml`   | `config-local-v1.toml`, `tool-settings-stage-v2-final.toml`                |
| CONF     | `.conf`   | `nginx-prod.conf`, `redis-local-v1.conf`                                   |

## Archive Files

- `[date]-subject-[env]-[version]-[status]-[confidentiality].ext`
- **kebab-case**

| Type    | Extension  | Examples                                                                                 |
| ------- | ---------- | ---------------------------------------------------------------------------------------- |
| ZIP     | `.zip`     | `2025-05-18-project-backup-prod-v2-final.zip`, `2024-12-logs-qa-archived.zip`            |
| TAR.GZ  | `.tar.gz`  | `2025-01-01-website-export-stage-v1-internal.tar.gz`, `2023-11-analytics-data.tar.gz`    |
| 7-Zip   | `.7z`      | `2025-05-database-snapshot-prod-v3.7z`, `2024-07-user-exports-test-draft.7z`             |
| RAR     | `.rar`     | `2023-09-30-legacy-archive-confidential.rar`, `2022-06-15-compressed-documents-prod.rar` |
| TAR.BZ2 | `.tar.bz2` | `2023-03-15-log-archive-prod-v1.tar.bz2`, `2022-12-10-source-files-dev.tar.bz2`          |

## Script & Programming Files

### Shell Scripts

- `[prefix]-subject-[env]-[os]-[version]-[status].ext`
  - os: e.g. `linux`, `macos`, `cross`
- **kebab-case**

| Type         | Extension     | Examples                                                                    |
| ------------ | ------------- | --------------------------------------------------------------------------- |
| Shell Script | `.sh`, `.zsh` | `01-init-linux.sh`, `10-deploy-backend-prod-cross-v2.sh`, `zsh-aliases.zsh` |

### Batch Scripts

- `subject-[env]-[version]-[status].ext`
- **kebab-case**

| Type       | Extension | Examples                                                          |
| ---------- | --------- | ----------------------------------------------------------------- |
| Batch File | `.bat`    | `backup-prod-v1.bat`, `reset-env-final.bat`, `install-driver.bat` |
| CMD File   | `.cmd`    | `start-server.cmd`, `clean-cache-prod.cmd`                        |

### PowerShell

- **IMPORTANT:** `Subject` must be in `PascalCase`
- `Verb-Subject.ext`
- **Verb-Noun** both in **PascalCase**

| Type              | Extension | Examples                                                   |
| ----------------- | --------- | ---------------------------------------------------------- |
| PowerShell Script | `.ps1`    | `Check-SystemStatus.ps1`, `Install-ModuleDependencies.ps1` |
| PowerShell Module | `.psm1`   | `Update-NetworkConfig.psm1`, `Start-WebServer.psm1`        |

### Programming Languages

#### snake_case

- `subject.ext`

| Language | Extension | Examples                              |
| -------- | --------- | ------------------------------------- |
| Python   | `.py`     | `data_processor.py`, `load_config.py` |
| Ruby     | `.rb`     | `user_auth.rb`, `email_service.rb`    |
| Elixir   | `.ex`     | `user_repo.ex`, `email_client.ex`     |
| Rust     | `.rs`     | `data_model.rs`, `http_server.rs`     |

#### camelCase

- `subject.ext`

| Language    | Extension | Examples                |
| ----------- | --------- | ----------------------- |
| JavaScript  | `.js`     | `dataProcessor.js`      |
| TypeScript  | `.ts`     | `userService.ts`        |
| Java (vars) | `.java`   | `camelCaseExample.java` |
| C# (vars)   | `.cs`     | `dataProcessor.cs`      |

#### PascalCase

- `subject.ext`

| Language   | Extension | Examples                           |
| ---------- | --------- | ---------------------------------- |
| C#         | `.cs`     | `UserManager.cs`, `AppConfig.cs`   |
| Java       | `.java`   | `UserService.java`, `MainApp.java` |
| TypeScript | `.tsx`    | `UserCard.tsx`, `LoginForm.tsx`    |

#### kebab-case

- `subject.ext`

| Language / Type  | Extension    | Examples                                     |
| ---------------- | ------------ | -------------------------------------------- |
| JavaScript (web) | `.js`, `.ts` | `user-service.js`, `data-utils.ts`           |
| HTML             | `.html`      | `user-profile.html`, `account-settings.html` |
| CSS              | `.css`       | `main-styles.css`, `login-page.css`          |
| SCSS             | `.scss`      | `dashboard-layout.scss`                      |
| JSON             | `.json`      | `project-config.json`, `users-list.json`     |

## Media Files

### Image Files

- `[figure]-[date]-subject-[contributor]-[type]-[resolution]-[version].ext`
- **kebab-case**

| Type | Extension | Examples                                                                                        |
| ---- | --------- | ----------------------------------------------------------------------------------------------- |
| PNG  | `.png`    | `fig02-2025-05-18-logo-dark-theme-icon-512x512-v1.png`, `quarterly-sales-chart.png`             |
| JPG  | `.jpg`    | `fig1-2024-08-12-family-picnic-photo-4k-v1.jpg`, `2023-smith-family-spring-1920x1080.jpg`       |
| GIF  | `.gif`    | `2025-03-01-loading-animation-256x256-v1.gif`, `2024-12-data-flow-diagram-animated-480p-v2.gif` |
| SVG  | `.svg`    | `2025-05-project-logo-icon-retina-v3.svg`, `icon-download-vector-v1.svg`                        |

### Audio Files

- `[date]-subject-[contributor]-[type]-[frequency]-[quality]-[version]-[status]-[language].ext`
- **kebab-case**

| Type | Extension | Examples                                                                                                                          |
| ---- | --------- | --------------------------------------------------------------------------------------------------------------------------------- |
| MP3  | `.mp3`    | `2025-05-18-interview-john-doe-narration-44k-compressed-v1-final-en.mp3`, `2024-12-keynote-speech-48k-normalized-v2-final-en.mp3` |
| WAV  | `.wav`    | `2025-04-30-nature-forest-recording-48k-raw-v1-draft-en.wav`, `2023-11-12-lab-session-recording-44k-processed-v3-final-en.wav`    |
| FLAC | `.flac`   | `2025-01-01-speech-dataset-commands-16k-raw-v1-final-en.flac`, `2024-10-ambient-office-noise-48k-lossless-v2-final-en.flac`       |
| OGG  | `.ogg`    | `2025-03-10-ui-click-effect-22k-compressed-v1-final.ogg`, `alert-notification-48k-lossless-v2-final.ogg`                          |
| M4A  | `.m4a`    | `2025-02-15-podcast-episode-07-narration-44.1k-compressed-v1-final-en.m4a`, `voice-memo-16k-raw-v1-draft-en.m4a`                  |

### Video Files

- `[date]-subject-[contributor]-[type]-[resolution]-[quality]-[version]-[status]-[language].ext`
- **kebab-case**

| Type | Extension | Examples                                                                                                                       |
| ---- | --------- | ------------------------------------------------------------------------------------------------------------------------------ |
| MP4  | `.mp4`    | `2025-05-18-lab-procedure-tutorial-recording-1080p-edited-v1-final-en.mp4`, `2024-12-experiment-demo-720p-raw-v1-draft-en.mp4` |
| MOV  | `.mov`    | `2025-04-b-roll-lab-setup-4k-raw-v1.mov`, `2024-11-interview-session-1-1080p-edited-v2-final-en.mov`                           |
| MKV  | `.mkv`    | `conference2025-session-3-presentation-720p-compressed-v1-final-en.mkv`, `projectx-overview-1080p-final.mkv`                   |
| WEBM | `.webm`   | `screencast-installation-guide-1080p-edited-v1-final-en.webm`, `2023-ui-demo-walkthrough-720p-final-en.webm`                   |
| AVI  | `.avi`    | `legacy-training-recording-480p-final-en.avi`, `2022-05-field-capture-raw-720p-v1-draft.avi`                                   |

## Folder Naming

### Cross-Platform Folder Naming Conventions

Based on scientific research and institutional best practices for naming folders across Windows, macOS, and Linux:

- `[date]-subject`
- `[prefix]-subject`
- `[prefix]-[date]-subject`
- **kebab-case**

| Pattern            | Examples                                        | Use Case                                             |
| ------------------ | ----------------------------------------------- | ---------------------------------------------------- |
| `[date]-subject`   | `2025-05-18-interview-data`                     | Date-based sorting, e.g. logs, snapshots, recordings |
|                    | `2024-12-01-lab-results`                        | Daily/weekly structured data or research exports     |
| `[prefix]-subject` | `01-project-proposal`                           | Enforced order in workflows or onboarding steps      |
|                    | `10-experiment-results`                         | Ordered batch folders (e.g., steps in a pipeline)    |
| Combined           | `01-2025-05-18-lab-recordings`                  | When both chronological and step order matter        |
| General project    | `data-cleaning`, `model-training`, `audio-sync` | Standard project or component folders                |

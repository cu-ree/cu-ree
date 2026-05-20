# AI Portfolio Workspace

AI를 활용한 실무형 개발 포트폴리오를 장기 운영하기 위한 개인 작업공간입니다.

이 루트 저장소는 개별 포트폴리오 프로젝트의 소스 저장소가 아니라, 프로젝트 관리, 실험, 문서, 템플릿, 에셋을 정리하는 운영 허브입니다. GitHub 업로드 대상은 기본적으로 `projects/<project-name>` 단위의 독립 repository입니다.

## Workspace Structure

```text
AI_Portfolio/
  projects/      # GitHub 업로드 대상 포트폴리오 프로젝트
  experiments/   # AI workflow, API, image generation, routing 실험
  docs/          # 구조, 비용, workflow, troubleshooting, business model 문서
  assets/        # 공통 screenshots, gifs, videos
  templates/     # README, FastAPI, React, env, GitHub 템플릿
  archive/       # 오래된 프로젝트, 실패한 실험, 임시 보관
  scripts/       # 작업공간 자동화 스크립트
```

## Operating Rules

- `projects/` 아래의 각 폴더는 독립 프로젝트로 간주합니다.
- 프로젝트별 GitHub repository를 분리합니다.
- 실험 코드는 `experiments/`에서 검증한 뒤 필요한 것만 `projects/`로 승격합니다.
- 각 프로젝트는 반드시 `README.md`, `docs/`, `assets/screenshots/`, `devlog/`를 포함합니다.
- API key, `.env`, DB dump, 대용량 영상 원본은 Git에 올리지 않습니다.
- README는 결과물 중심으로 작성하되, 문제 정의와 구현 판단을 함께 남깁니다.

## Project Creation

PowerShell에서 새 프로젝트를 만들 때:

```powershell
.\scripts\new-project.ps1 -Name cad-bim-analyzer -Description "CAD/BIM 파일 분석 자동화 프로젝트" -InitGit
```

생성 위치:

```text
projects/cad-bim-analyzer/
```

## GitHub Strategy

기본 전략은 프로젝트별 repository 분리입니다.

```text
projects/cad-bim-analyzer      -> github.com/<user>/cad-bim-analyzer
projects/ai-office-simulation  -> github.com/<user>/ai-office-simulation
projects/ai-content-automation -> github.com/<user>/ai-content-automation
```

루트 작업공간은 개인 관리용으로 두거나, 필요하면 private repository로만 관리합니다.

## Documentation Index

- [Workspace Structure](docs/architecture/workspace-structure.md)
- [Project Lifecycle](docs/workflows/project-lifecycle.md)
- [Portfolio Management](docs/workflows/portfolio-management.md)
- [Devlog Policy](docs/workflows/devlog-policy.md)
- [Extension Roadmap](docs/architecture/extension-roadmap.md)
- [GitHub Profile Branding Strategy](docs/branding/github-profile-strategy.md)
- [Project Description Examples](docs/branding/project-description-examples.md)
- [GitHub Repository Strategy](docs/github/repository-strategy.md)
- [API Cost Tracking](docs/api-costs/README.md)
- [Troubleshooting](docs/troubleshooting/README.md)
- [Business Model Notes](docs/business-model/README.md)

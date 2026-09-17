# AVA Mother Standard frontend comparison

This application uses the production 5pay frontend values as shared AVA tokens. The
medical workflow keeps its own content and business logic, while the outer shell and
common controls use the same sizing system.

| Frontend rule | 5pay production value | medicalclaims value |
| --- | ---: | ---: |
| Header height | `56px` | `--ava-header-height: 56px` |
| App identity alignment | Header leading / left | `.app-header-leading` / left |
| Content max-width | `920px` | `--ava-shell-max: 920px` |
| Page horizontal padding | `20px` | `--ava-page-padding: 20px` |
| Card padding | `24px` | `--ava-card-padding: 24px` |
| Card gap | `20px` | `--ava-card-gap: 20px` |
| Card radius | `14px` | `--ava-card-radius: 14px` |
| Card border | `1px solid #e2e8f0` | `1px solid #e2e8f0` |
| Card shadow | `0 4px 16px rgba(15,23,42,.06)` | `0 4px 16px rgba(15,23,42,.06)` |
| Heading size / line-height | `22px / 1.4` | `--ava-heading-size: 22px / 1.4` |
| Body size / line-height | `14px / 1.6` | `--ava-body-size: 14px / 1.6` |
| Input / select height | `44px` | `--ava-control-height: 44px` |
| Primary button height | `46px` | `--ava-button-height: 46px` |
| Responsive breakpoint | `700px` | `@media (max-width: 700px)` |
| Mobile page padding | `12px` | `12px` |
| Mobile card padding | `18px 16px` | `18px 16px` |

## Responsive behaviour

- **Desktop and iPad landscape:** the header and content share the same centred
  `920px` rail. The app identity remains in the leading (left) group.
- **iPad portrait:** the fluid rail fills the available viewport while retaining
  the standard `20px` edge spacing.
- **Mobile portrait:** at `700px` the shell changes to `12px` page spacing and
  `18px 16px` card spacing; at `480px`, header utilities and navigation controls
  wrap instead of overflowing.
- **Return navigation:** `← 返回 AVA` remains the first control in the standard
  leading header group and links to the AVA Platform root.

No calculation, persistence, cloud mapping, role, case/document, admin, manifest,
or navigation-flow logic is changed by the token alignment.

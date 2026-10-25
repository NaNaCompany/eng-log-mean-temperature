# 로그평균 온도차 계산기

열교환기 양 끝의 양의 온도차로 LMTD 계산

- Plan ID: E078
- App: https://nanalab.kr/eng-log-mean-temperature/
- Repository: https://github.com/NaNaCompany/eng-log-mean-temperature
- Formula: `ΔT_lm = (ΔT₁−ΔT₂)/ln(ΔT₁/ΔT₂)`
- Output: 로그평균 온도차 ΔT_lm

## Model

ΔT₁,ΔT₂>0. 온도 역전이 없는 열교환기 단부 차이를 입력한다. 두 차이가 같으면 극한값인 동일 온도차를 반환한다. 전열량·보정계수·열교환기 형상 해석은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `14.4269504088896`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.

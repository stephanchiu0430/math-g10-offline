# Math Prep — Grade 10 Math (Taiwan 高一 level)

An offline-capable web app for short daily practice of every core Grade 10 math skill in Taiwan's 108 curriculum, plus the middle-school foundations those skills rest on. Same engine as the vocabulary and math-fact apps: spaced repetition, daily sessions, XP and streaks, a parent report, and progress stored on the device.

## Coverage

| Unit | 課綱 | Semester | Skills |
| --- | --- | --- | --- |
| Middle-school foundations | 國中先備 | before 高一 | linear equations, 2×2 systems, quadratics by factoring, Pythagorean theorem, exponent rules |
| Numbers & expressions | 數與式 | 高一上 | absolute value, simplifying radicals, rationalizing, multiplication formulas, division points |
| Lines & circles | 直線與圓 | 高一上 | slope, line equations, parallel/perpendicular, point-to-line distance, circle equations, line–circle position |
| Polynomial functions | 多項式函數 | 高一上 | remainder theorem, factor theorem, vertex of a quadratic, quadratic and polynomial inequalities, roots and coefficients |
| Sequences & series | 數列與級數 | 高一下 | arithmetic and geometric sequences and series, Σ notation, recursive sequences |
| Data analysis | 數據分析 | 高一下 | mean and median, standard deviation, linear transformations, regression line |
| Counting | 排列組合 | 高一下 | permutations, combinations, repeated letters, together/apart, grid paths, binomial theorem |
| Probability | 機率 | 高一下 | two dice, drawing without replacement, "at least one", expected value |

42 skills in total. Every question is generated fresh, so a skill can't be passed by remembering one answer.

## How it works

- **Unit checks first.** One question per skill. Right answers are marked known (and still reviewed a week later); everything else enters daily practice. The Stats tab lists every gap a check found and whether it has since been mastered.
- **New skill = idea + worked example + two tries.** Each new skill opens with the key formula and a fully worked example, then two practice problems.
- **Wrong answers teach.** The full solution and the key idea are shown, then a similar problem is asked right away (ungraded), and the skill returns tomorrow.
- **Spaced review**: 1 → 3 → 7 → 14 → 30 days, a new problem each time. Mastered from box 4.
- **Typed answers** — integers, fractions such as −3/4, or decimals — on an on-screen keypad. Equivalent forms are accepted (6/8 = 3/4 = 0.75).
- **Done for today** when reviews due and new skills both reach zero.

## Scope

The app drills the core calculation behind each topic. Taiwanese exams also ask multi-step and proof-style questions; once a unit is mastered here, a 高一 textbook or 學測-style problem set is the right next step for that unit.

## Files, deployment, updates, parent report

Same as the other apps:

- `index.html` (whole app), `sw.js` (offline + auto-update), `manifest.json` and icons, `apps-script.gs` (optional parent report).
- Deploy to GitHub Pages from the repository root. Don't commit `.env`; add it to `.gitignore`.
- **Change `VERSION` at the top of `sw.js` on every release.** The installed version shows at the bottom of Setup.
- Progress lives in `localStorage`. On iOS, deleting the home-screen icon deletes its progress — use **Setup → Export progress** first. Every parent-report row also includes a backup code.
- Parent report: paste `apps-script.gs` into a Google Sheet's Apps Script, deploy as a web app (Execute as *Me*, access *Anyone*), and paste the `/exec` URL into **Setup → Parent report** on the student's device. Keep the URL private.

# Audit

Dated log of editorial passes and verification runs. Newest first.
See docs/writing-pipeline.md §7 and docs/refresh-pipeline.md.

## 2026-06-07 — research-pipeline formalization + fact-check + gate to built

Scope: bring the paper to PIATRA research-pipeline parity. Retro-document the
deep research and fact-check into brief.md / research.md / sources.md; clear the
one refs flag; run the gates; set status to built. No new claims beyond what is
verified.

Changes:
  - Fact-check (web-verified against publisher / PubMed / DOI). Three errors
    corrected in PAPER.md:
      - De Wolff & van IJzendoorn (1997): sensitivity-security is r = .22 (30
        studies, N=1,666); the 66-study / N=4,176 figure is the full
        all-antecedents meta, not sensitivity alone. §4 rewritten.
      - Ritchie & Tucker-Drob (2018): "persists across the lifespan" softened to
        "showed little sign of fading with age"; added 142 effect sizes / 42
        datasets / three quasi-experimental designs. §11.
      - Csibra & Gergely (2009): "pointing" removed from the ostensive-cue list
        (pointing is referential, not ostensive). §6.
    Minor: Johnson et al. (1991) full title; Onishi & Baillargeon (2005) title
    is a question, initials K. H.; neonatal-imitation hedge now cites Davis et
    al. (2021) for heterogeneity and notes the null is contested (Meltzoff et
    al. 2018); BEIP claims split (cognition+timing -> Nelson et al. 2007;
    memory/EF -> Bos et al. 2009; EEG -> Vanderwert et al. 2010).
  - Bibliography expanded 31 -> 60, each addition integrated into prose where it
    does work (verified non-decorative by `papers refs` 0 unused). Added among
    others: primary Vygotsky (1978, 1987); Wood, Bruner & Ross (1976);
    Friston (2010); Clark (2013); Atzil et al. (2018); Fonagy et al. (2002);
    Trevarthen & Aitken (2001); Liszkowski et al. (2004); Tomasello, Kruger &
    Ratner (1993); Tennie, Call & Tomasello (2009); Boyd & Richerson (1985);
    Lewis & Brooks-Gunn (1979); Rochat (2003); Lewis et al. (1989); Lyons et al.
    (2007); Horner & Whiten (2005); Curtiss (1977); Sonuga-Barke et al. (2017);
    Greenough et al. (1987); Johnson et al. (1991); Cooper & Aslin (1990);
    Vouloumanos & Werker (2007); Mehler et al. (1988); Onishi & Baillargeon
    (2005); Davis et al. (2021); Meltzoff et al. (2018).
  - Removed the earlier cross-references to other PIATRA papers (per request);
    the historical-stratification point is now anchored to Mauss (1985) instead.
  - refs fix: the combined "(Vygotsky, 1978, 1987)" hid the 1987 year from the
    parser (flagged unused). §10 now cites Vygotsky (1978) for internalization
    and Vygotsky (1987) for egocentric->inner speech separately; both engage the
    text. `unused` cleared.
  - Created research-pipeline artifacts at repo root: brief.md (synthesis;
    cornerstone list), research.md (findings tiered T1-T4 by section), sources.md
    (60 entries mirroring `## References`, one provenance line each).
  - metadata.yaml: status draft -> built.

Verification:
  - voice: 0 errors, 12 review-candidates (all load-bearing contrasts:
    nativism-vs-environmentalism, IQ-vs-scaffolding, one-algorithm-two-niches,
    runtime-metaphor limit; kept deliberately).
  - refs: 60 in-text keys, 60 bib entries, 0 missing, 0 unused.
  - claims: claims_target none (synthesis) — manual only, no reconciliation.
  - build: clean, 23 pages, 0 missing-character warnings. ~9,600 words.
  - check => PASS (metadata OK, build OK, voice OK, refs OK, claims advisory).
  - web-sync not run: paper is built, not published.

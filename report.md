## Part A — Characterising the series

This analysis characterises the Faroe Bank Channel (FBC) overflow volume
transport — the dense overflow of cold, deep water from the Nordic Seas into the
North Atlantic across the FBC sill (~61.5°N, 8.2°W) — distributed by AMOCatlas as
the single scalar series `TRANS_FBC` (Sv). I chose it as a long, regularly
sampled, single-variable record with strong intrinsic variability, well suited to
spectral characterisation, and because the overflow limb is a distinct,
dynamically interesting component of the AMOC.

The record spans 1995-11-14 to 2024-05-18 (≈28.6 years) on a regular daily grid
(sampling interval 1 day, confirmed by a unique forward difference of 1.0 day),
giving 10,414 samples. Of these, 573 (5.5%) are missing. The gaps are not
isolated days but 28 discrete outages — 26 longer than a week, the longest 28
days — consistent with mooring servicing. I fill the interior gaps by linear
interpolation to preserve the regular grid the FFT-based estimates in Part B
require. This is a documented compromise: interpolating across multi-week blocks
acts as a local low-pass, muting genuine high-frequency variance within those
windows and adding minor spurious low-frequency structure. At 5.5% of the record,
spread over nearly three decades and averaged over many Welch segments, the effect
is small but non-zero, and I flag it rather than conceal it.

The transport has mean 2.20 Sv and standard deviation 0.59 Sv (sample std,
`ddof=1`), consistent with the long-quoted ~2 Sv FBC overflow strength; the
near-equal median (2.17 Sv) indicates only mild asymmetry. Values range from 0.50
to 4.86 Sv (range 4.36 Sv). The distribution is unimodal and approximately
Gaussian with a slight positive skew — a longer tail toward strong-overflow events,
visible as occasional excursions above ~4 Sv — while the series otherwise
fluctuates around a stable ~2.2 Sv mean with no apparent long-term trend.
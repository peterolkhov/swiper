# Swiper virtual.removeSlide index ordering

Run `python3 -m http.server 8000 --bind 127.0.0.1` in this directory and open http://127.0.0.1:8000. No package install or external request is needed.

Both fresh carousels start with A,B,C,D,E,F and request removal of B and D. Passing [1,3] leaves A,C,E,F; passing [3,1] incorrectly leaves A,C,D,F, deleting E instead of D.

The included browser bundle contains unchanged Swiper Core/Virtual/Manipulation source pinned to82cb393aaf3793c92bd31ae23006215c813ab984 (master/package14.4.0) plus a small public-API harness. The exact HTML and bundle were exercised in Chromium153 on macOS. Both virtual cache modes reproduce; this page displays the cached case. No stable npm release or other browser is claimed.

This reproduction is isolated from the eventual production-fix branch. MIT source license is included.

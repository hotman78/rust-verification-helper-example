---
data:
  attributes: {}
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 64, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/rust.py\"\
    , line 77, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: pub mod union_find;
  dependsOn:
  - src/union_find/union_find.rs
  extendedDependsOn:
  - icon: ':heavy_check_mark:'
    path: src/union_find/union_find.rs
    title: src/union_find/union_find.rs
  extendedRequiredBy: []
  extendedVerifiedWith:
  - icon: ':heavy_check_mark:'
    path: src/union_find_yosupo_test.rs
    title: src/union_find_yosupo_test.rs
  - icon: ':heavy_check_mark:'
    path: src/union_find_aoj_test.rs
    title: src/union_find_aoj_test.rs
  isVerificationFile: false
  path: src/union_find/mod.rs
  requiredBy: []
  timestamp: '2020-09-12 11:31:32+09:00'
  verificationStatus: LIBRARY_ALL_AC
  verificationStatusIcon: ':heavy_check_mark:'
  verifiedWith:
  - src/union_find_yosupo_test.rs
  - src/union_find_aoj_test.rs
documentation_of: src/union_find/mod.rs
layout: document
redirect_from:
- /library/src/union_find/mod.rs
- /library/src/union_find/mod.rs.html
title: src/union_find/mod.rs
---

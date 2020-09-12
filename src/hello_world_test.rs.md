---
data:
  attributes:
    PROBLEM: https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/1/ITP1_1_A
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 64, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/rust.py\"\
    , line 77, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "//verify-helper: PROBLEM https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/1/ITP1_1_A\n\
    mod hello_world;\nuse hello_world::hello_world;\n\nfn main(){\n    hello_world();\n\
    }"
  dependsOn:
  - src/hello_world.rs
  extendedDependsOn:
  - icon: ':heavy_check_mark:'
    path: src/hello_world.rs
    title: src/hello_world.rs
  extendedRequiredBy: []
  extendedVerifiedWith: []
  isVerificationFile: true
  path: src/hello_world_test.rs
  requiredBy: []
  timestamp: '2020-09-12 11:31:32+09:00'
  verificationStatus: TEST_ACCEPTED
  verificationStatusIcon: ':heavy_check_mark:'
  verifiedWith: []
documentation_of: src/hello_world_test.rs
layout: document
redirect_from:
- /verify/src/hello_world_test.rs
- /verify/src/hello_world_test.rs.html
title: src/hello_world_test.rs
---

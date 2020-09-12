---
data:
  attributes:
    PROBLEM: https://judge.yosupo.jp/problem/unionfind
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 64, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/rust.py\"\
    , line 77, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "// verify-helper: PROBLEM https://judge.yosupo.jp/problem/unionfind\n#![allow(dead_code)]\n\
    mod union_find;\nuse union_find::union_find::UnionFind;\n\nuse std::io::*;\nuse\
    \ std::str::FromStr;\n\nfn read<T: FromStr>() -> T {\n    let stdin = stdin();\n\
    \    let stdin = stdin.lock();\n    let token: String = stdin\n        .bytes()\n\
    \        .map(|c| c.expect(\"failed to read char\") as char) \n        .skip_while(|c|\
    \ c.is_whitespace())\n        .take_while(|c| !c.is_whitespace())\n        .collect();\n\
    \    token.parse().ok().expect(\"failed to parse token\")\n}\n\nfn main(){\n \
    \   let n:usize=read();\n    let q:usize=read();\n    let mut uf=UnionFind::new(n);\n\
    \    for _i in 0..q{\n        let c:usize=read();\n        let s:usize=read();\n\
    \        let t:usize=read();\n        if c==0{\n            uf.merge(s,t);\n \
    \       }else{\n            println!(\"{}\",if uf.same(s,t){1}else{0});\n    \
    \    }\n    }\n}\n\n"
  dependsOn:
  - src/union_find/union_find.rs
  - src/union_find/mod.rs
  extendedDependsOn:
  - icon: ':heavy_check_mark:'
    path: src/union_find/union_find.rs
    title: src/union_find/union_find.rs
  - icon: ':heavy_check_mark:'
    path: src/union_find/mod.rs
    title: src/union_find/mod.rs
  extendedRequiredBy: []
  extendedVerifiedWith: []
  isVerificationFile: true
  path: src/union_find_yosupo_test.rs
  requiredBy: []
  timestamp: '2020-09-12 11:31:32+09:00'
  verificationStatus: TEST_ACCEPTED
  verificationStatusIcon: ':heavy_check_mark:'
  verifiedWith: []
documentation_of: src/union_find_yosupo_test.rs
layout: document
redirect_from:
- /verify/src/union_find_yosupo_test.rs
- /verify/src/union_find_yosupo_test.rs.html
title: src/union_find_yosupo_test.rs
---

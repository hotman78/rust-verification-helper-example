---
data:
  attributes: {}
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 64, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/rust.py\"\
    , line 77, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "/// Implement (union by size) + (path compression)\n/// Reference:\n/// Zvi\
    \ Galil and Giuseppe F. Italiano,\n/// Data structures and algorithms for disjoint\
    \ set union problems\npub struct UnionFind {\n    n: usize,\n    // root node:\
    \ -1 * component size\n    // otherwise: parent\n    parent_or_size: Vec<i32>,\n\
    }\n\nimpl UnionFind {\n    // 0 <= size <= 10^8 is constrained.\n    pub fn new(size:\
    \ usize) -> Self {\n        Self {\n            n: size,\n            parent_or_size:\
    \ vec![-1; size],\n        }\n    }\n    pub fn merge(&mut self, a: usize, b:\
    \ usize) -> usize {\n        assert!(a < self.n);\n        assert!(b < self.n);\n\
    \        let (mut x, mut y) = (self.leader(a), self.leader(b));\n        if x\
    \ == y {\n            return x;\n        }\n        if -self.parent_or_size[x]\
    \ < -self.parent_or_size[y] {\n            std::mem::swap(&mut x, &mut y);\n \
    \       }\n        self.parent_or_size[x] += self.parent_or_size[y];\n       \
    \ self.parent_or_size[y] = x as i32;\n        x\n    }\n\n    pub fn same(&mut\
    \ self, a: usize, b: usize) -> bool {\n        assert!(a < self.n);\n        assert!(b\
    \ < self.n);\n        self.leader(a) == self.leader(b)\n    }\n    pub fn leader(&mut\
    \ self, a: usize) -> usize {\n        assert!(a < self.n);\n        if self.parent_or_size[a]\
    \ < 0 {\n            return a;\n        }\n        self.parent_or_size[a] = self.leader(self.parent_or_size[a]\
    \ as usize) as i32;\n        self.parent_or_size[a] as usize\n    }\n    pub fn\
    \ size(&mut self, a: usize) -> usize {\n        assert!(a < self.n);\n       \
    \ let x = self.leader(a);\n        -self.parent_or_size[x] as usize\n    }\n \
    \   pub fn groups(&mut self) -> Vec<Vec<usize>> {\n        let mut leader_buf\
    \ = vec![0; self.n];\n        let mut group_size = vec![0; self.n];\n        for\
    \ i in 0..self.n {\n            leader_buf[i] = self.leader(i);\n            group_size[leader_buf[i]]\
    \ += 1;\n        }\n        let mut result = vec![Vec::new(); self.n];\n     \
    \   for i in 0..self.n {\n            result[i].reserve(group_size[i]);\n    \
    \    }\n        for i in 0..self.n {\n            result[leader_buf[i]].push(i);\n\
    \        }\n        result\n            .into_iter()\n            .filter(|x|\
    \ !x.is_empty())\n            .collect::<Vec<Vec<usize>>>()\n    }\n}\n\n#[cfg(test)]\n\
    mod tests {\n    use super::*;\n\n    #[test]\n    fn dsu_works() {\n        let\
    \ mut d = UnionFind::new(4);\n        d.merge(0, 1);\n        assert_eq!(d.same(0,\
    \ 1), true);\n        d.merge(1, 2);\n        assert_eq!(d.same(0, 2), true);\n\
    \        assert_eq!(d.size(0), 3);\n        assert_eq!(d.same(0, 3), false);\n\
    \        assert_eq!(d.groups(), vec![vec![0, 1, 2], vec![3]]);\n    }\n}\n"
  dependsOn: []
  extendedDependsOn: []
  extendedRequiredBy:
  - icon: ':heavy_check_mark:'
    path: src/union_find/mod.rs
    title: src/union_find/mod.rs
  extendedVerifiedWith:
  - icon: ':heavy_check_mark:'
    path: src/union_find_yosupo_test.rs
    title: src/union_find_yosupo_test.rs
  - icon: ':heavy_check_mark:'
    path: src/union_find_aoj_test.rs
    title: src/union_find_aoj_test.rs
  isVerificationFile: false
  path: src/union_find/union_find.rs
  requiredBy:
  - src/union_find/mod.rs
  timestamp: '2020-09-12 11:31:32+09:00'
  verificationStatus: LIBRARY_ALL_AC
  verificationStatusIcon: ':heavy_check_mark:'
  verifiedWith:
  - src/union_find_yosupo_test.rs
  - src/union_find_aoj_test.rs
documentation_of: src/union_find/union_find.rs
layout: document
redirect_from:
- /library/src/union_find/union_find.rs
- /library/src/union_find/union_find.rs.html
title: src/union_find/union_find.rs
---

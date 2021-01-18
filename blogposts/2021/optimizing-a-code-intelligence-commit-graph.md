---
title: "Optimizing a code intelligence commit graph"
author: Eric Fritz
authorUrl: https://eric-fritz.com
publishDate: 2021-01-18T18:00-07:00
tags: [blog]
slug: optimizing-a-code-intel-commit-graph
heroImage: https://sourcegraphstatic.com/blog/lsif-go/lsif-go-improvements.png
published: true
---

# Genesis

- [RFC 32 IMPLEMENTED: Nearest commit queries](https://docs.google.com/document/d/16g_S9ViSgsCvwJqbpeo734WwHPem6Fpl40dpdaRaXdQ)
- [LSIF: Track and determine closest commit #5691](https://github.com/sourcegraph/sourcegraph/pull/5691)

# Performance Improvements

- [LSIF: add indexes to speed up finding the nearest-commit #5946](https://github.com/sourcegraph/sourcegraph/pull/5946)
- [LSIF: Better fix for quadratic query #5984](https://github.com/sourcegraph/sourcegraph/pull/5984)
- [LSIF: fix quadratic SQL query #5980](https://github.com/sourcegraph/sourcegraph/pull/5980)

# New Techniques

- [RFC 186 IMPLEMENTED: Scalable nearest commit queries](https://docs.google.com/document/d/1NiAQG4muTljgk8qirYs2aN5Zt3lfk4lgwNqOm9WOH4s)
- [Implement better nearest commit queries #12098](https://github.com/sourcegraph/sourcegraph/issues/12098)
- [codeintel: Determine nearest upload efficiently in query path #14581](https://github.com/sourcegraph/sourcegraph/pull/14581)

# Takes too long, too much memory to calculate graph

- [LSIF Go Indexing fails after 3.17 > 3.21 upgrade #16030](https://github.com/sourcegraph/sourcegraph/issues/16030)
- [codeintel: Reduce memory when calculating commit graph #16086](https://github.com/sourcegraph/sourcegraph/pull/16086)
- [codeintel: Limit size of commit graph #16140](https://github.com/sourcegraph/sourcegraph/pull/16140)
- [codeintel: Topologically sort commits in gitserver #16270](https://github.com/sourcegraph/sourcegraph/pull/16270)
- [codeintel: Optimize commit graph #16368](https://github.com/sourcegraph/sourcegraph/pull/16368)

# Now too much data in database

- [Uber: LSIF Indexing fails in 3.22.1 #156](https://github.com/sourcegraph/customer/issues/156)
- [codeintel: Optimize nearest upload operations #16636](https://github.com/sourcegraph/sourcegraph/pull/16636)
- [codeintel: Refrain from using git log --all in directed path #16733](https://github.com/sourcegraph/sourcegraph/pull/16733)
- [code-intel: pass hex byte encoded commit hash to query #16558](https://github.com/sourcegraph/sourcegraph/pull/16558)

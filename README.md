# EQEmu-Docs-Browser
View web site here: http://tfsg.dyndns.org/EQEmu-Docs/

Built a 2-file standalone browser for the EQEmu docs tree:

- index.html (18 KB)
- data.js (2.7 MB)

Open index.html by double-clicking — it runs from file:// with no server, no build step, and no network access so it will run locally from a downloads folder if so choose. I verified zero external references (0 http/https srcs or hrefs); the only resource is the local data.js.

Embedded data:
- 301 tables / 4,152 columns with types, nullability, ordinal position, and descriptions
- 887 foreign-key relationships with cardinality
- 638 documentation pages, ~2.0M characters of searchable prose
- 48 schema categories

Four views, all driven by one search box:
- Everything — landing dashboard with category list
- Schema — table cards with column details and per-table relationships
- Documentation — all pages, filterable by top-level section
- Relationships — all 887 foreign keys, filterable by category

Search covers table names, column names, column descriptions, foreign keys, and full doc text, with match highlighting. Relationship and table references are click-through deep links (#t=table_name), so a foreign key jumps straight to that table's definition.

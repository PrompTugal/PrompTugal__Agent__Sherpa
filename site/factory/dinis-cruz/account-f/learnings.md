# Learnings

From the role's first weeks (history/board/team/sherpa/debriefs/):
- A page is only as current as its own "last checked" line (ST1, 11 Nov).
- On a day that changes, check every way in for the same fact, first screen first.
- A full-page screenshot can catch an animation or a streaming loop mid-way: use waitUntil 'load', not 'networkidle', on pages with a live loop.
- A message sent to a superseded inbox is lost to the role: confirm the current inbox before sending.
- Findings are ranked, each has an owner, and is re-measured; none is narrated as fixed until measured.

From this session (26 Nov):
- The container has no ssh-keygen: apt-get install -y openssh-client (after apt-get update) gives it.
- add_repo may be refused by the classifier until Dinis says yes in the session; attach, then one clone with a long timeout, then a bounded fetch (--depth) for history; the full history was 9,166 commits.

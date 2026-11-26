# Restart: cl-6.sherpa

1. Read this folder (agent.json first), then CLAUDE.md of PrompTugal__News__Website and its board/guidance/README.md ("New from Dinis").
2. Read history/board/team/sherpa/ROLE.md and the newest debriefs (history/board/team/sherpa/debriefs/2026-11-12-handover.md), status.json and the 16 Nov restart read (history/board/team/sherpa/review-2026-11-16-1930-restart-cold-read.md).
3. Make a fresh session key if the old session is gone (private halves mode 600 in the scratchpad, never printed); publish the public file in site/keys/ alone in its commit; set git signing (gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey, commit.gpgsign true). ssh-keygen: apt-get install -y openssh-client.
4. Attach PrompTugal__News__Website (add_repo, push), clone it once with a long timeout, register_repo_root.
5. Measure with Playwright and Chromium (preinstalled): 390 x 844 phone, 1366 x 800 desktop, waitUntil 'load'. Reviews go to the website's pass files; screenshots stay with me.
6. Keep agent.json current; trailers on every commit: Agent: cl-6.sherpa@PrompTugal.dinis and Claude-Session: <session URL>.
7. At the start of each wake read the ABP grant: https://raw.githubusercontent.com/PrompTugal/PrompTugal__Agent__ABP/dev/abp/cl-6.sherpa.md (no hook delivers it yet), and file a hand-written run report in runs/cl-6.sherpa/ (template: abp/templates/run-report-by-hand.md in the ABP repository).

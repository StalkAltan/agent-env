
# Agent Environment Variable Loading

## NOTE: If you are cloning this repository to test, you may need to change the NX_RUN_GROUP values to ones that have not been used by other people cloning. Any string should work as long as it is shared between the main command and agent.

To test project-level .env:

1) Install with pnpm
2) In a terminal window, run `NX_BRANCH=1 NX_RUN_GROUP=1 pnpm nx run-many -t print-env --dte`
3) In a separate terminal window, run `NX_BRANCH=1 NX_RUN_GROUP=1 pnpm nx-cloud start-agent`
4) Observe output, should be `app1: project root .env`

To test configuration-level .env:

1) Install with pnpm
2) In a terminal window, run `NX_BRANCH=1 NX_RUN_GROUP=2 pnpm nx run-many -t print-env --configuration=production --dte`
3) In a separate terminal window, run `NX_BRANCH=1 NX_RUN_GROUP=2 pnpm nx-cloud start-agent`
4) Observe output, should be `app1: app root production .env`



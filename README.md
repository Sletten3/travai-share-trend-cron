# TravAi share-trend scheduler

Calls `https://trav-innsamling.vercel.app/api/cron/share-trend` every 5 minutes via GitHub Actions.

Each run is a **single** HTTP poll (no multi-hour loop). A long loop plus a shared concurrency queue previously delayed new kicks and created sampling gaps.

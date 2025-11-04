# SoundScape - Adversarial Analysis (V1)

**Authors**: Vedha Avali (vavali), Leha Choppara (lehac), Nathan Lee (nzlee)

## EXECUTIVE SUMMARY
Ambitious crowdsourced audio mapping platform attempting to build global sound database with sophisticated ML pipelines, gamification, and multi-layered QC in 4-5 weeks. While conceptually novel and well-documented, technical scope severely overambitious for timeline, and reliance on intrinsic motivation without concrete worker testing is critical risk.

## VERDICT: WEAK GO - Needs Scope Reduction

**Main Issue**: Massive scope creep - cross-platform mobile/web apps, ML-based audio processing (SNR, MFCC, chroma embeddings), worker queues, PyTorch clustering, Mapbox integration. This is 6-12 month funded startup scope, not 5-week student project.

**Critical Flaws**:
- Scope 3-4x too large (10+ features, each week-long)
- Zero budget for acquisition ($0.00/task with 150+ submissions needed)
- Vague recruitment (same "social media campaigns" magic thinking)
- Audio-specific complexity underestimated (signal processing, perceptual hashing, MFCC embeddings)
- Untested motivation (why would people record sounds for badges?)
- Cold start ignored (empty map = no value)

**Strengths**:
- Genuine novelty (acoustic dimension is differentiated)
- Specific success metrics with numbers
- Honest ethical considerations
- Framework awareness (Octalysis cited)
- Good faith steel-man effort
- Thoughtful aggregation strategy

**Rating**: C+ crowdsourcing (understands theory, execution questionable), D+ technical feasibility

**Most Critical Change**: Cut scope by 70% immediately. Simple web form (not mobile) to upload MP3 + location + tags. MapBox showing pins. Manual QC by team (not ML). 30-50 clips around campus. Kill: ML pipeline, sophisticated QC, gamification backend, mobile app, worker queues, acoustic features.

**Predicted Outcome**: Weeks 1-2 infrastructure setup, week 3 realize audio processing harder than expected, week 4 no users, recruit friends, week 5 polish demo. Show functional map with 25-40 clips mostly around campus. Grade: depends on execution of reduced scope.

# Loopify

## Team Members
- James Baker (bakj@seas.upenn.edu)
- Jasper Zhu (jzhu25@sas.upenn.edu)
- Chanya Thanglerdsumpan (chanyat@seas.upenn.edu)
- Avi Upadhyayula (aviu@sas.upenn.edu)
- Namita Sajai (namitas@seas.upenn.edu)
- Angie Cao (angiecao@seas.upenn.edu)

## Project Resources
- **Video Presentation**: https://drive.google.com/file/d/1QBJYsUSHxUdOgEjlalDMsAToayKIugxp/view
- **Website**: Functional platform with Spotify integration
- **Report**: 296852809_Loopify.pdf

## Project Synopsis
Loopify is a music discovery platform that helps users find songs matching specific "vibes" or moods. Unlike traditional recommendation systems, it combines crowdsourcing with AI to create thematically coherent playlists. Users vote on whether songs belong to specific vibe categories, and the aggregated votes create consensus-based playlists that better capture nuanced emotions and contexts than algorithmic recommendations alone.

## How It Uses the Crowd
The crowd contributes through:
- **Song Categorization**: Voting yes/no/unsure on whether songs match specific vibes
- **Vibe Definition**: Community consensus on what constitutes each playlist mood
- **Quality Assessment**: Crowd validates song-vibe associations
- **Playlist Curation**: Aggregated votes determine final playlist composition
- **Human Insight**: Provides assessments impossible to automate

## Strengths
- **Addresses Real Need**: Solves actual problem with poor music recommendations
- **Self-Sustaining Incentives**: Users contribute to benefit from better playlists
- **Excellent Proof-of-Concept**: Smooth Spotify integration and user experience
- **Strong Analysis**: 
  - Interesting comparison with GPT-generated playlists
  - Found crowd includes multiple songs per artist vs AI's varied approach
  - Identified crowd better at common emotions, weaker at nuanced vibes
- **Technical Excellence**: Well-integrated APIs and smooth prototype
- **Valuable Data**: Creates human-curated music categorizations impossible to automate

## Weaknesses
- **Technical Implementation Issues**:
  - No user accounts or persistent identities
  - WorkerID refreshes on each page load
  - Can't distinguish 100 users with 1 vote from 1 user with 100 votes
  - No ability to edit votes or track malicious users
- **Limited Functionality**:
  - Can't create new vibes
  - No song contribution mechanism
  - Cold start problem not addressed
- **UI Limitations**: Some brittleness expected given timeline
- **Demographic Blindness**: No user profiles means can't detect taste differences

## Course Concept Alignment
The project demonstrates:
- **High understanding** of incentives, crowd value, and aggregation
- **Adequate understanding** of ethics, skills, quality control, and scaling
- Excellent grasp of using crowds for subjective judgments
- Strong practical application of course concepts

## Recommendations for Improvement
1. **Implement User Accounts**:
   - Persistent user identities
   - Track contribution history
   - Enable vote editing
   - Detect and remove malicious users
2. **Enhance Quality Control**:
   - Associate ratings with profiles
   - Implement reputation systems
   - Add minimum vote thresholds
   - Weight votes by user reliability
3. **Expand Functionality**:
   - Allow users to create new vibes
   - Enable song submissions
   - Add playlist sharing features
   - Implement collaborative filtering
4. **Improve Aggregation**:
   - Provide details on voting algorithms
   - Explain tie-breaking mechanisms
   - Document song ordering logic
   - Add transparency to aggregation process
5. **Address Scaling**:
   - Solve cold start with seed data
   - Implement vibe discovery mechanisms
   - Add demographic segmentation
   - Create personalized recommendations
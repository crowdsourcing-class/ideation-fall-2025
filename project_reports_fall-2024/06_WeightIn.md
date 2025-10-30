# WeightIn

## Team Members
- Sydney Simon (sydsimon@sas.upenn.edu)
- Aarti Bhamidipati (aartib@seas.upenn.edu)
- Nicholas Molina (ngmolina@seas.upenn.edu)
- Brian Lu (brilu100@seas.upenn.edu)
- Henry Casper (hcasper@seas.upenn.edu)
- Michael Wallison (mwalli@seas.upenn.edu)

## Project Resources
- **Video Presentation**: https://www.youtube.com/watch?v=f2Br3uVawEo
- **Website**: Live deployment with custom frontend/backend
- **Report**: 296739762_WeightIn.pdf

## Project Synopsis
WeightIn is a platform for anonymous users to post and respond to polls, positioned as a tool to help address indecisiveness through the wisdom of the crowd. The platform features real-time aggregation and visualization of poll results, displayed immediately after users submit their responses. It aims to provide meaningful crowd-sourced opinions on various topics.

## How It Uses the Crowd
The crowd contributes through:
- **Poll Creation**: Users submit questions for community input
- **Response Collection**: Anonymous voting on polls
- **Real-time Aggregation**: Immediate display of aggregated results
- **Content Categorization**: Polls organized into 6 categories (Academic, Career Guidance, etc.)
- **Quality Filtering**: Community-driven content moderation

## Strengths
- **Technical Excellence**: 
  - Significant engineering effort with well-organized codebase
  - Nice web interface with responsive design
  - Real-time result visualization as incentive
  - Professional frontend/backend implementation
- **Quality Control**: Good implementation using Perspective API for toxic content filtering
- **Clear Documentation**: Comprehensive report with detailed development process
- **Cost Analysis**: Thorough scalability analysis with AWS service projections
- **Category Analysis**: Insightful breakdown of content into 6 categories

## Weaknesses
- **Lack of Differentiation**: Fails to distinguish from existing platforms (Reddit polls, Yik Yak, Sidechat)
- **Unclear Value Proposition**: 
  - Claims of enhanced anonymity not substantiated vs Reddit
  - "Meaningful questions" focus not enforced or encouraged
- **Limited Innovation**: Essentially recreates existing poll functionality
- **Simulated Crowd**: Used simulated data rather than real crowd engagement
- **No Incentive Comparison**: Didn't explore different incentive mechanisms
- **Missing ML Components**: No machine learning models implemented

## Course Concept Alignment
The project demonstrates:
- **High understanding** of crowd dynamics, ethics, quality control, aggregation, and scaling
- **Adequate understanding** of incentives and overall crowdsourcing concepts
- Good technical implementation but limited crowdsourcing innovation
- Strong connection to course material in analysis sections

## Recommendations for Improvement
1. **Strengthen Differentiation**:
   - Develop unique features beyond basic polling
   - Create specialized use cases (e.g., decision-making for specific domains)
   - Add AI-powered insights or recommendations
2. **Enhance Incentives**:
   - Implement reputation system
   - Add gamification elements
   - Create achievement badges
3. **Improve Content Quality**:
   - Develop mechanisms to encourage meaningful questions
   - Add expert verification for certain categories
   - Implement topic-specific moderation
4. **Add Innovation**:
   - Integrate machine learning for poll recommendations
   - Create predictive models for poll outcomes
   - Add sentiment analysis
5. **Address Edge Cases**:
   - Handle the 0.0 agreement rate in philosophical debates
   - Clarify user vs system categorization process
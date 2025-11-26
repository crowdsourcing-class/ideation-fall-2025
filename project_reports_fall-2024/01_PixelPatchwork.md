# PixelPatchwork

## Team Members
- John Majernik (johnmaj@seas.upenn.edu)
- Jason Figueroa (jasonfig@seas.upenn.edu)
- Via Liu (bangchel@sas.upenn.edu)
- Dan Kim (dankim1@seas.upenn.edu)
- Ryan Zhou (ryanzh@seas.upenn.edu)

## Project Resources
- **Video Presentation**: https://drive.google.com/file/d/16jjDGjSW1skFFihlSFL2iqCjEpGfvOBN/view
- **Website**: https://pixelspatchwork-1.onrender.com/ (Note: functionality may be discontinued)
- **Report**: 296850446_PixelPatchwork.pdf

## Project Synopsis
PixelPatchwork is a collaborative image editing tool that allows users to make small updates to a seed image via AI generation with prompting and in-filling. The platform displays one seed image each day, collects several alternate images and votes, and then moves the best-voted alternate on to be the seed image the next day. It combines AI and human creativity in an iterative crowdsourcing process similar to 99designs or Threadless.

## How It Uses the Crowd
The crowd contributes to PixelPatchwork in multiple ways:
- **Creative Input**: Users select parts of images to mask out and provide prompts for AI-generated refinements
- **Voting Mechanism**: Community members upvote/downvote submissions to determine the best daily image
- **Iterative Processing**: Each day's winning image becomes the next day's seed, creating collaborative evolution
- **Dual Crowd Sources**: The project collected input from both MTurk workers and classmates

## Strengths
- **Technical Innovation**: Nice integration of AI and human creativity with a well-designed interface that allows users to clear sections, enter prompts, and see AI-generated results
- **User Experience**: Clear and easy-to-use UI with intuitive masking and prompting capabilities
- **Community Engagement**: Good implementation of voting system and daily image progression to encourage repeat visits
- **Visual Communication**: Strong visual project that effectively illustrated its creative potential
- **Technical Execution**: Significant engineering effort in setting up custom canvas and API integrations

## Weaknesses
- **Limited Scale**: Only one image available at a time severely limits user engagement and project potential
- **Weak Analysis**: Analysis was limited due to single initial image, preventing meaningful comparison of iterative vs parallel processing
- **Missed Opportunities**: 
  - Incentive schemes could have been gamified rather than relying on paid/mandatory participation
  - Lack of thematic focus led to random evolution (camping photo to unicorns/rainbows)
  - No clear goal or coherent theme to guide creative direction
- **Quality Control Issues**: Random Forest model for predicting winning images was ineffective (always predicted false)
- **Sustainability**: Website functionality was discontinued after project completion, likely due to API costs
- **Ethics Oversight**: Insufficient consideration of potential harm from toxic content submissions

## Course Concept Alignment
The project demonstrates:
- **High understanding** of crowd collaboration and aggregation concepts
- **Adequate understanding** of incentives, ethics, skills, and quality control
- **Inadequate understanding** of proper incentive design beyond payment/requirement
- Strong connection to iterative and parallel processing topics covered in class

## Recommendations for Improvement
1. Implement multiple simultaneous canvases with different seed images
2. Add thematic constraints or goals (e.g., "underwater wildlife," "more dogs!")
3. Develop sustainable incentive mechanisms beyond payment
4. Improve quality control with better ML models and content moderation
5. Consider long-term sustainability of API costs and platform maintenance
6. Add features for personalized creativity and individual artistic expression
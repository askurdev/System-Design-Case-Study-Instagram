# System-Design-Case-Study-Instagram

Overview : Instagram is an American photo and video sharing social networking service owned by Meta Platforms. Instagram a widely popular photo and video-sharing social networking platform, has grown exponentially and now boasts 300 million monthly active users .To ensure optimal performance, scalability, and reliability robust system architecture must be designed to handle the platform’s massive user base support key operations. This case study focuses on designing system for two major operations: user authentication and media content delivery.

Functional Requirements : 
Some of the functional requirements of the Instagram design are:

User Posting: User should be able create and publish posts, consisting of a status update and an optional image or video attachment. User should have the ability to edit their post content before publishing.
Timeline Generation: A personalized timeline should be generated for each upon login, displaying posts from users they follow. The Timeline should be sorted chronology or based on relevance.
Interactions with Posts: Users must be able to like posts. Users should be able to leave comments on posts. Posts can have multiple comments and users should be able to delete their own comments.
Follow/Unfollow: Users have the ability to follow and follow other users. There should be a notification system to alert user about new folders.
Profile Management : Users should be able to view and edit their profiles, including profile picture and bio.Users can view profiles of other users

Non-Functional Requirements : 
Some of the Non-Functional requirements of the Instagram design are :

** Performance**

Response Time: The system should respond to user actions within a maximum of 2 seconds to provide a seamless and responsive user experience.

Scalability: The Platform should be designed to handle an increasing number of users and posts ensuring performance remains stale under growing user.

Reliability:

Availability: The system should have a minimum uptime of 99.9% to ensure user can and interact with the platform consistently.

Fault Tolerance: the application should be designed to handle server failures gracefully, ensuring minimul disruption to user experience.

Security:

Data Encryption: All user data, including passwords and personal information, should be encrypted during transmission and storage to maintain user privacy.

Access Control: Implement robust access controls to ensure that users can only access and modify their own data and administrators have appropriate privileges

Usability

User Interface Consistency: Maintain a consistent and intuitive user interface across platform feature and devices to enhance user satisfaction and usability.

Accessibility: The platform should be designed to be accessible to users with disabilities, complying with relevant accessibility standards.

Scalability:

Load Handling: The system should be able to handle a scalable number of concurrent users, ensuring that performance does not degrade as user activity increases.

Database Scalability: The database architecture should be scalable to accommodate a growing volume of volume of data without compromising performance

Media Content Delivery system
Objective efficiently delivers media content (image and video) to 300 million users with low latency.

Design Consideration:

Content Distribution network (CDN):

Integrate with a global CDN to cache and distribute media content closer to users, reducing latency.
Leverage CDN capabilities for dynamic content caching and edge computing.

Media Server Clusters:

Deploy cluster of media servers to handle the high volume of media content requests.
Implement load balancing to evenly distribute content requests across media servers.

Adaptive bitrates Streaming:

Implement adaptive bitrates streaming for videos to optimize playback based on user’s network conditions.
Transcode media files into multiple resolutions and bitrates for efficient delivery.

Caching and Prefetching:

Implement content caching mechanisms to reduce server load and improve response times.
Utilize prefetching algorithms to predict and load content that users are likely to access.

Estimates:

Let’s say, we have —

No of photos uploaded by each user/month = 3

No of active users/month = 300 million

Size of each Image & Video: 10 MB

Total = 300⁷  10  3 = 8.37 PB of storage is what we need every month

Storage space (for photos) needed for 10 years:

8.37  12  10 = 1004.4 PB

Media content Requests per Seconds: 50,000 request per second.
CDN cache Hit Ration: 90%
Latency Target: 100 milliseconds.

User APIs
Below will the APIs that will be needed

Create a POST with a photo or a video
Comment on a POST
Comment on a Comment itself
Like a Post
Like a Comment
Fetch the timeline.

Conclusion
Designing scalable systems for instagram’300 million monthly active users involves careful consideration of load balancing, redundancy, security measures, and efficient content delivery. The proposed Solutions for user authentication and media content delivery aim to provide a seamless and secure user experience while ensuring.


Check out my Notion case studies 🔗 Instagram-Case Study of System Design

#SystemDesign #Instagram #SoftwareArchitecture #FullStackDeveloper #CDN #Microservices #WebDevelopment

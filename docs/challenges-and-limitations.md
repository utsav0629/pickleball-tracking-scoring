# Challenges and Limitations

## 1. Overview

This project explored the feasibility of applying computer vision to pickleball video analysis. During research and experimentation, several technical challenges were identified that would need to be addressed before a reliable, complete tracking and scoring system could be developed.

## 2. Small and Fast-Moving Ball

A pickleball may occupy only a small number of pixels in a video frame. Rapid movement can also cause motion blur or make the ball difficult to distinguish from the background.

**Potential improvement:** Use a more diverse dataset, review image resolution, and evaluate detection performance across different ball positions and movement conditions.

## 3. Occlusion

Players, paddles, or other objects can temporarily hide the ball. This can make detection unreliable and complicate tracking across consecutive frames.

**Potential improvement:** Investigate tracking methods that can handle temporary loss of detection and evaluate them using representative gameplay footage.

## 4. Background and Lighting Variation

Court colors, shadows, reflections, camera angles, and lighting conditions may affect the appearance of objects in video footage.

**Potential improvement:** Include varied conditions in the dataset and test the model on footage that differs from the training images.

## 5. Player Identification

Detecting a person in a frame is not the same as reliably identifying an active player throughout a rally. A complete system would need to distinguish players from spectators and maintain consistent identities across frames.

**Potential improvement:** Explore object tracking, court-region filtering, and identity association techniques.

## 6. Detection Versus Tracking

Object detection produces predictions for individual images or video frames. Tracking attempts to associate detections across time.

A reliable tracking system therefore requires additional logic beyond an object detector. This project did not result in a fully deployed end-to-end tracking application.

## 7. Automated Scoring

Automated scoring requires more than detecting the ball and players. It may involve interpreting serves, rallies, faults, court boundaries, and point-ending events according to the rules of pickleball.

**Potential improvement:** Treat event detection and scoring as separate research tasks, validate them against annotated footage, and account for ambiguous situations.

## 8. Real-Time Performance

A practical real-time system must process video quickly enough to provide useful results. Model size, hardware, image resolution, and video-processing overhead can all affect speed.

**Potential improvement:** Measure inference latency and frame-processing rate before claiming real-time performance.

## 9. Dataset and Evaluation Limitations

The dataset size, class distribution, evaluation metrics, and generalization performance must be verified from the original project files before quantitative conclusions can be drawn.

Without testing on suitable unseen data, it is not possible to establish how reliably a model would perform in different real-world gameplay conditions.

## 10. Project Scope

The project was research-oriented. It investigated dataset preparation and computer-vision approaches, but it was not completed as a production-ready application with fully integrated tracking, gameplay analysis, and automatic scoring.

The repository should distinguish completed experiments from proposed functionality.

## 11. Future Improvements

Future work could include:

- Improving the diversity and quality of the dataset.
- Evaluating detection performance on unseen footage.
- Exploring tracking across consecutive video frames.
- Investigating player identity consistency.
- Studying gameplay-event recognition.
- Developing and validating scoring logic.
- Measuring processing speed and deployment requirements.

## 12. Conclusion

Documenting limitations is an important part of responsible engineering research. Identifying unresolved problems helps define realistic next steps and prevents experimental findings from being presented as a fully working system.

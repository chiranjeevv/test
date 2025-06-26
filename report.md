# Soccer Player Re-Identification Assignment Report

## Approach and Methodology

- Used the provided YOLOv11 model to detect players in each frame of the video.
- Extracted simple color histogram features from each detected player.
- Matched players between frames using histogram similarity (Bhattacharyya distance).
- Assigned and maintained player IDs based on feature matching, so that players re-entering the frame keep the same ID.

## Techniques Tried and Outcomes

- Tried color histogram features for simplicity and speed.
- Used a nearest-neighbor approach for matching features between frames.
- The approach works reasonably well when players have distinct appearances or are spaced apart.

## Challenges Encountered

- Players with similar uniforms can be confused.
- Occlusions or missed detections can cause ID switches.
- Simple features are not robust to lighting changes or partial occlusions.

## Future Improvements

- Use deep learning-based appearance features for more robust re-identification.
- Implement a tracking algorithm like DeepSORT for better ID consistency.
- Add spatial and motion information to improve accuracy.
- Handle occlusions and missed detections more gracefully.

If given more time, I would integrate a pre-trained re-identification network and experiment with multi-feature fusion for improved robustness.

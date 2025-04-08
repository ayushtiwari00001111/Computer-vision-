1. Harris Corner Detection
Purpose: Detects corners in an image — points where the intensity changes sharply in multiple directions.

How it works:

Computes image gradients.

Measures the local intensity variation in a window.

High variation in both x and y directions = a corner.

Use case: Object tracking, motion detection.

🧠 Key Point: Sensitive to edges and noise, but good at finding strong corner features.

🟩 2. Shi-Tomasi Corner Detection
Improved version of Harris Corner Detection.

Instead of using a mathematical corner score like Harris, it directly looks at the minimum eigenvalue of the image gradient matrix.

Why better?

Only selects strong, reliable corners (more stable in tracking).

Used in: cv2.goodFeaturesToTrack().

🧠 Key Point: More accurate and robust than Harris, commonly used in feature tracking (e.g., KLT tracker).

🟦 3. Blob Detection
Purpose: Finds regions in an image that differ in properties like brightness or size compared to surrounding areas.

Detects:

Circular blobs

Irregular bright/dark spots

How it works:

Analyzes connected pixels based on thresholds.

Filters blobs by area, circularity, convexity, etc.

Used in: Medical imaging, shape detection.

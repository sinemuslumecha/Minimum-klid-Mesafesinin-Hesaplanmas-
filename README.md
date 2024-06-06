# Minimum-klid-Mesafesinin-Hesaplanmas-
import math
points = [(2,6),(5,9),(5,9),(9,8),(5,7,),(3,5)]

def euclideanDistance(point1,point2):
     x1, y1 = point1
     x2, y2 = point2
     return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)


min_distance = min(distances)
print("Minimum mesafe:", min_distance)

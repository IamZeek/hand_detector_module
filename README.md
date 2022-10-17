# hand_detector_module

you can access the module through the file by the following code:

#Use it for connecting to the module
def main():
    cap = cv2.VideoCapture(0)
    detector = hand_detector()
    while True:
        success, img = cap.read()
        img = detector.findHands(img)
        lm_List = detector.findPosition(img)

        cv2.imshow("image", img)

        cv2.waitKey(1)

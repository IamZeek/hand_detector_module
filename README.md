# hand_detector_module

you can access the module through the file by the following code:

#Use it for connecting to the module
def main():
    cap = cv2.VideoCapture(0)
    detector = hand_detector() #calling the main class
    while True:
        success, img = cap.read()
        img = detector.findHands(img) # This function works to find hands 
        lm_List = detector.findPosition(img) # this function returns a list of hand positions

        cv2.imshow("image", img)

        cv2.waitKey(1)

# homework1
import cv2

#cv2.VideoCapture() で VideoCapture オブジェクトを取得

capture = cv2.VideoCapture(0)   

while(True):

    #カメラから1コマのデータを取得するため capture.read() を呼び出し, 変数frameに代入
    ret, frame = capture.read()   
    cv2.imshow('frame',frame)
    
    #ループを止めるために「q」キーがタイプされたら break 
    
    if cv2.waitKey(1) & 0xFF == ord('q'):   
    
        break

capture.release()

cv2.destroyAllWindows()	



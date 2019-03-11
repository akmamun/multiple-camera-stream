## Multiple CCTV/RTSP Streaming with Flask and Open-CV
```sh
pip install -r requirements.txt
```
### Run Server
```sh
app.py
```
#### Use Built-in Webcam of Laptop
##### Put Zero (O) in cv2.VideoCapture(0)
```sh
cv2.VideoCapture(0)
```
#### Use Ip Camera/CCTV/RTSP Link
```sh
cv2.VideoCapture('rtsp://username:password@camera_ip_address:554/user=username_password='password'_channel=channel_number_stream=0.sdp')  
 ```
####  Example RTSP Link
```sh
cv2.VideoCapture('rtsp://mamun:123456@101.134.16.117:554/user=mamun_password=123456_channel=0_stream=0.sdp')
```
#### Change Channel Number to Change the Camera
```sh
cv2.VideoCapture('rtsp://mamun:123456@101.134.16.117:554/user=mamun_password=123456_channel=1_stream=0.sdp')
```
#### Display the resulting frame in browser
```sh
cv2.imencode('.jpg', frame)[1].tobytes()                 
``` 

 ## Credit
 Learn More about Streaming with flask
 - https://blog.miguelgrinberg.com/post/video-streaming-with-flask

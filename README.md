import cv2

#stream = cv2.VideoCapture('rtsp://XXX:YYYY@ZZZZ')
#isikan XXXX dengan nama pengguna, biasanya "admin"
#isikan YYYY dengan password yang digunakan
#isikan ZZZZ dengan alamat IP dari IP Camera

stream = cv2.VideoCapture('rtsp://admin:cepatkaya12@192.168.1.108')

while True:
	r,f = stream.read()
	cv2.imshow('IP Camera stream',f) #membuat jendela tampilan dengan nama "IP Camera stream"
	
	if cv2.waitKey(1) & 0xff == ord('q'): #jika tombol q keyboard ditekan maka program streaming berhenti
		break

cv2.destroyAllWindows() #menghapus seluruh jendela yang menggunakan opencv



=================================================================================
Reff install openCV
http://saptaji.com/2021/06/05/cara-instal-opencv-di-raspberry-pi/
https://www.youtube.com/watch?v=OugQIz_vcFo

Reff troubleshoot access IP Cam:
https://stackoverflow.com/questions/49978705/access-ip-camera-in-python-opencv
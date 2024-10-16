# yolo-ocr
Ultralytics YOLO-based OCR framework for custom OCR in a single font type.

# About

For now this is just my intrusive thought, a rough idea, as previously I successfully use YOLO to precisely do OCR in 16-character long national id number. And I thought maybe we could do this for the whole Alphabet as I read YOLO can takes up to 80 classes.

# The idea

I want to create a framework that do everything but still customizable.

Firstly, dataset generation. We input the font and specify what characters including capital "abcdefghijkl.." and maybe generate 1M images with random word combination. Also randomize the background, where you can input pattern image or plain color as a background. 

Also an option to specify the degree/angle of the text in the canvas. This is similar like Captcha dataset generation and indeed I was inspired from there (https://github.com/JackonYang/captcha-tensorflow)

And then for training, we could specify the base model either YOLOv8 nano or the other variants.

For prediction, we specify the confidence threshold (default at 0.85) and we take all the label prediction, sort it with Z pattern and combine all the label. Analyze the gap, if far away then add spaces, then return the OCR result or format it in certain way.

Voila.

# Realization

Im a busy man, maybe someone out there will take my idea. Let's hope I have a free time to start developing that. Tho I don't realy know python and Machine Learning stuff.

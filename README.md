# advcam

代码和结果分别储存在AdvCam-Hide-Adv-with-Natural-Styles-master.zip和result.zip文件中。使用以下命令配置环境：
```sh
conda create -n advcam_env python=3.12
conda activate advcam_env
```
激活环境之后：
```sh
git clone https://github.com/Diodadadawryyyy/advcam.git
cd advcam
unzip AdvCam-Hide-Adv-with-Natural-Styles-master.zip
cd AdvCam-Hide-Adv-with-Natural-Styles-master
pip install --user --requirement requirements.txt
```
使用train.py生成对抗图片，修改options.py中的图片路径来更改内容图像和风格图像：
```python
parser.add_argument('--content_image_path', type=str, default='physical-attack-data\\content\\1\\5.jpeg', help='Path to content image')
parser.add_argument('--style_image_path', type=str, default='physical-attack-data\\style\\oil-painting\\1.jpg', help='Path to style image')
```
修改options.py中的target值来更改目标图像：
```python
parser.add_argument('--target', type=int, default=498, help='Target label for targeted attack')
```
使用eval.py来测试生成的图像，修改options.py中的图像路径来改变测试图像：
```python
parser.add_argument('--image_dir', type=str, default='output\\dog1\\suc_251.jpg', help='Path to image')
```

原始图片与生成的对抗图片对比如下：
<p align='center'>
  <img src='img/img1.jpg' width='200'/>
  <img src='img/img2.jpg' width='200'/>
</p>

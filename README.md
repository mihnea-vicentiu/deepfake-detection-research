# Proiect-Deep-Learning (DL)
&emsp; Proiect Deep Learning (DL), Anul 3, Semestrul 2, Facultatea de Matematica si Informatica, Universitatea din Bucuresti

### &emsp; Membrii Echipa: <br/>
Capatina Razvan Nicolae ($352$) <br/>
Buca Mihnea Vicentiu ($352$) <br/>
Luculescu Teodor ($351$) <br/>

<br/>
<br/>
<br/>

### Tema Aleasa: Deep Fake Image Detection <br/>

<br/>
<br/>
<br/>

There are two main parts to this project:
1) Cross-generator deepfake detection. We want to evaluate the generalization capabilities of deepfake detection methods: how well detectors work when tested on images produced by other generators than those seen at training. For this, we will train on images coming from one generator and test on images coming from other generators. We will compare at least three different methods.
- xception41, not pretrained
- xception41, pretrained (ImageNet 1k), Fine-Tuning
- CLIP, pretrained
- SAM, pretrained

2) Model attribution. In this part we investigate whether we can identify the generative model that has produced a particular image. We formulate this task as a multiclass classification task, where the input is an image and the output is one of the five classes: “ldm”, “lama”, “pluralistic”, “repaint”, “real”. We experiment with the same methods as for the first task, then report the overall accuracy and the per class accuracy and display a TSNE plot of the features color coded by the five classes.

### [Poster](https://www.overleaf.com/project/new/template/34882?id=991907223&latexEngine=lualatex&mainFile=poster.tex&templateName=Unofficial+Poster+Template+for+University+of+Oxford&texImage=texlive-full%3A2023.1)

![image](https://github.com/user-attachments/assets/f21963f5-301c-49e2-85d8-9acada101f83)

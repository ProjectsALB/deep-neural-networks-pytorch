<div align="center">

<img src="assets/banner.svg" alt="Deep Neural Networks me PyTorch" width="100%">

# Deep Neural Networks me PyTorch

**Platformë mësimore në shqip dhe kodi i plotë i kursit, nga tensorët e parë deri te një CNN.**

[![Live demo](https://img.shields.io/badge/Platforma-Live-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://deep-neural-networks.netlify.app/)
[![Kursi](https://img.shields.io/badge/Kursi-Coursera-0056D2?style=for-the-badge&logo=coursera&logoColor=white)](https://www.coursera.org/learn/deep-neural-networks-with-pytorch)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

[Hap platformën](https://deep-neural-networks.netlify.app/) · [Programi](#programi-i-kursit) · [Kodi](course-code) · [Ekzekutimi](#ekzekutimi-lokal)

</div>

> **English summary:** An Albanian-language, static learning platform plus the complete Python code for the Coursera course *Deep Neural Networks with PyTorch* (7 weeks: tensors and autograd, linear/logistic regression, softmax, deep networks and regularization, CNNs, and a FashionMNIST project). Pure HTML, CSS and JavaScript, deployable on Netlify with no build step.

## Përmbajtja

- [Qasja në platformë](#qasja-në-platformë)
- [Programi i kursit](#programi-i-kursit)
- [Veçoritë e platformës](#veçoritë-e-platformës)
- [Rezultati i projektit](#rezultati-i-projektit-java-7)
- [Struktura e repository-t](#struktura-e-repository-t)
- [Ekzekutimi lokal](#ekzekutimi-lokal)
- [Publikimi në Netlify](#publikimi-në-netlify)
- [Kredite dhe licenca](#kredite-dhe-licenca)

## Qasja në platformë

| | |
|---|---|
| **Linku** | https://deep-neural-networks.netlify.app/ |
| **Fjalëkalimi** | `12345` |

## Programi i kursit

<p align="center">
  <img src="assets/roadmap.svg" alt="Rruga e të mësuarit në 7 javë" width="100%">
</p>

| Java | Tema | Çfarë mëson |
|:---:|---|---|
| 1 | Tensorët dhe diferencimi automatik | Tensorët 1D dhe 2D, llojet e të dhënave, `requires_grad` dhe `backward()`. |
| 2 | Regresioni linear dhe SGD | Humbja MSE, zbritja e gradientit, mini-batch, `Dataset`, `DataLoader`, `torch.optim`, ndarja trajnim/validim. |
| 3 | Regresioni i shumëfishtë dhe logjistik | `nn.Linear` me shumë hyrje dhe dalje, sigmoid, entropia e kryqëzuar, inicializimi i keq. |
| 4 | Softmax dhe rrjetet me shtresë të fshehur | Klasifikimi me shumë klasa në MNIST, aktivizimet (sigmoid, tanh, ReLU), më shumë neurone të fshehura. |
| 5 | Rrjete të thella dhe rregullimi | `nn.ModuleList`, inicializimi (Uniform, Xavier, He), dropout, momentum, batch normalization. |
| 6 | Rrjetet konvolucionale (CNN) | Konvolucioni, kanale të shumta, max pooling, CNN me dhe pa BatchNorm në MNIST. |
| 7 | Projekti: FashionMNIST | CNN me dy shtresa konvolucionale, trajnim me `DataLoader`, kosto dhe saktësi për epokë. |

## Veçoritë e platformës

- 📚 **7 module** me teori në shqipe, terma kyç dhe formula.
- 💻 **Praktiko veten:** ushtrime teorike dhe me kod PyTorch. Shkruan zgjidhjen, e kontrollon dhe e krahason me zgjidhjen e saktë.
- 🧩 **Kodi i kursit:** të gjithë skedarët Python të çdo jave, të hapshëm direkt në faqe.
- 🗂️ **Flashcards** dhe **fjalor teknik** me kërkim.
- 📝 **Provime** për çdo modul dhe provim final.
- 📈 **Progres** i ruajtur në shfletues (`localStorage`).
- 🔒 **Hyrje me fjalëkalim** para se të hapet platforma.
- 📱 Dizajn responsiv, punon edhe në celular.

## Rezultati i projektit (Java 7)

CNN-ja e trajnuar në FashionMNIST për 5 epoka (SGD, `lr = 0.1`, `batch_size = 100`): kostoja bie vazhdimisht, ndërsa saktësia në validim rritet nga rreth 83% në rreth 88%.

<p align="center">
  <img src="assets/week7-cost-accuracy.png" alt="Kostoja dhe saktësia gjatë trajnimit" width="560">
</p>

## Struktura e repository-t

```
.
├── README.md
├── assets/
│   ├── banner.svg
│   ├── roadmap.svg
│   └── week7-cost-accuracy.png
├── course-code/
│   ├── Week 1/   tensorët
│   ├── Week 2/   regresioni linear, SGD
│   ├── Week 3/   regresioni i shumëfishtë dhe logjistik
│   ├── Week 4/   softmax, rrjete me shtresë të fshehur
│   ├── Week 5/   rrjete të thella, dropout, BatchNorm
│   ├── Week 6/   CNN
│   └── Week 7/   projekti FashionMNIST
└── platform/
    ├── index.html
    ├── css/style.css
    └── js/
        ├── data.js    modulet, pyetjet, ushtrimet
        ├── code.js    kodi i kursit për faqen
        ├── app.js     logjika e platformës
        └── gate.js    ekrani i hyrjes
```

## Ekzekutimi lokal

**Platforma** (nuk kërkon instalim):

```bash
cd platform
python -m http.server 8000
# hap http://localhost:8000
```

**Kodi Python:**

```bash
pip install torch torchvision matplotlib numpy pandas
python "course-code/Week 2/Simple Linear Regression.py"
```

Skedarët janë shkruar për t'u ekzekutuar pjesë-pjesë në Jupyter ose Google Colab. Disa shkarkojnë MNIST ose FashionMNIST herën e parë që ekzekutohen.

## Publikimi në Netlify

1. Në Netlify zgjidh **Add new site**, pastaj **Deploy manually** (ose lidh këtë repository me *Base directory* `platform`).
2. Tërhiq folderin `platform`. Nuk ka komandë build.

## Kredite dhe licenca

Kodi i kursit është zbatim i materialit të kursit [Deep Neural Networks with PyTorch](https://www.coursera.org/learn/deep-neural-networks-with-pytorch) në Coursera. Platforma mësimore dhe përmbajtja në shqip janë ndërtuar për studim personal.

Licenca: shtoje skedarin `LICENSE` me licencën që zgjedh (p.sh. MIT).

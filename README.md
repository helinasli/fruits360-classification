# Fruits-360 Classification Project

Bu proje, Akbank "Derin Öğrenmeye Giriş" Bootcamp kapsamında geliştirilmiş olan bir görüntü sınıflandırma çalışmasıdır. Fruits-360 veri seti kullanılarak PyTorch framework'ü ile özel ResNet9 mimarisi geliştirilmiş ve 216 farklı meyve türünün sınıflandırılması gerçekleştirilmiştir.

## Proje Özeti

Bu çalışmada Evrişimli Sinir Ağları (CNN) kullanılarak meyve görüntülerinin otomatik sınıflandırılması hedeflenmiştir. Proje kapsamında:

- **Veri Seti**: Fruits-360 Dataset (147,691 görüntü, 216 sınıf)
- **Model**: ResNet9 özel mimarisi
- **Framework**: PyTorch
- **Performans**: %99.67 test doğruluğu

## Methodology

### 1. Veri Analizi ve Önişleme
- Kapsamlı keşifsel veri analizi (EDA) 
- Görüntü normalizasyonu ve standardizasyonu
- Veri artırma teknikleri (Data Augmentation)
- Train/Validation/Test bölümlemesi (%80/%20/Test)

### 2. Model Mimarisi
ResNet9 özel mimarisi geliştirilmiştir:

```
Input (3x100x100) → Conv2D(64) → Conv2D(128) → Residual Block 1 
→ Conv2D(256) → Conv2D(512) → Residual Block 2 → Classifier → Output(216)
```

**Temel Özellikler:**
- Residual connections (skip connections)
- Batch Normalization
- Dropout regularization (0.5)
- ReLU activation functions

### 3. Eğitim Süreci
- **Optimizer**: Adam (learning rate: 1e-4)
- **Loss Function**: CrossEntropyLoss
- **Batch Size**: 32
- **Epochs**: 10
- **Validation Strategy**: Hold-out validation

## Sonuçlar

### Performans Metrikleri
- **Test Accuracy**: 99.67%
- **Test Loss**: 0.0213
- **Best Validation Accuracy**: 100.00% (8. epoch)
- **Training Accuracy**: 99.98%

### Veri Dağılımı
- **Eğitim**: 88,595 görüntü
- **Doğrulama**: 22,149 görüntü  
- **Test**: 36,947 görüntü

## Teknik Özellikler

### Veri Artırma Teknikleri
- Random Horizontal Flip
- Random Rotation (±20°)
- Random Resized Crop
- Color Jitter (brightness, contrast, saturation)

### Model Optimizasyonları
- Learning rate scheduling
- Early stopping mechanism
- Model checkpointing
- Gradient clipping

## Gelecek Çalışmalar

- Transfer learning ile pre-trained modellerin test edilmesi
- Model compression ve quantization teknikleri
- Real-time inference optimizasyonu
- Web/mobil uygulama geliştirme
- Ensemble methods ile performans artırımı

## Kaynak Kodlar ve Veri

### Kaggle Notebook
🔗 **[Fruits Classification - Kaggle Notebook](https://www.kaggle.com/code/haaksoy/fruits-classification)**

### Veri Seti
- **Fruits-360 Dataset**: Kaggle Platform
- **Görüntü Boyutu**: 100x100 RGB
- **Format**: PNG
- **Lisans**: MIT License

### Kullanılan Teknolojiler
- **Deep Learning**: PyTorch
- **Data Processing**: NumPy, Pandas
- **Visualization**: Matplotlib, Seaborn
- **Computer Vision**: OpenCV, PIL
- **Model Interpretability**: Grad-CAM

## Referanslar

1. He, K., et al. "Deep Residual Learning for Image Recognition." CVPR 2016.
2. Mureşan, H., & Oltean, M. "Fruit recognition from images using deep learning." Acta Universitatis Sapientiae, Informatica 10.1 (2018): 26-42.
3. PyTorch Documentation: https://pytorch.org/docs/stable/index.html

---

**Proje Sahibi**: Helin Aslı Aksoy  
**Bootcamp**: Akbank Derin Öğrenmeye Giriş  
**Tarih**: 26.11.2025
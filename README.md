<h3 style='text-align: center; color:#00697f'> Diyabetik Retinopati - Körlük Tespiti </h3>
<h4 style='text-align: center; color:#00697f'> Implementation of EfficientNet-V2-L CNN Model</h4>
<h4 style='text-align: center; color:#00697f'> Görüntü Sınıflandırma EfficientNet-V2-L CNN Modeli Uygulaması</h4>

<table style="text-align: center">
    <tr style="text-align: center">
        <td style="text-align: center; color:#00697f ">
            <h5>Inönü University Computer Engineering - Master's - Pattern Recognition </h5>
        </td>
        <td rowspan=3, style="text-align: center; color:#00697f">
            <img src="inonu_ai.png" width="100"/>
        </td>       
    </tr>
    <tr>
        <td style="text-align: center; color:#00697f">
            <h5>İnönü Üniversitesi - Bilgisayar Mühendisliği - Yüksek Lisans - Örüntü Tanıma Dersi </h5>
        </td>
    </tr>
    <tr>
        <td style="text-align: center">
            <h6> Dr. Ali ARI (Lecturer) - Ahmet BAĞBARS (Graduate Student) </h6>
        </td>
    </tr>
</table>

<a href="DR-EfficientNet-V2-L.ipynb">Main Notebook - Ana Dosya</a>.

Bu repoda Tensorflow-Keras Framework kullanılarak körlük sebeplerinin başat nedenlerinden olan Diyabetik Retinopati Hastalığının 5-Teşhis Derecesi ile sınıflandırılmış  Kaggle'dan temin edilen Fundus Fotoğraflarının ve teşhis sınıflarının yeraldığı verisetleri kullanılarak Görüntü sınıflandırma yöntemiyle günümüzde en güncel CNN modellerinden EfficientNet-V2-L CNN Modeli kullanılarak tespit edilmiştir.

Aşağıdaki Tabloda bu VeriSetleri verilmiştir.

<table style="border: 1px solid;">
    <tr>
    <th style="text-align: center" colspan=2>DataSet Descriptions - VeriSeti Açıklamaları </th> 
    </tr>
    <tr>
        <td>Aptos 2019 DR </td>
        <td>https://www.kaggle.com/competitions/aptos2019-blindness-detection/data</td>
    </tr>
    <tr>
        <td>Messidor-2-Resized</td>
        <td>https://www.kaggle.com/datasets/tanlikesmath/diabetic-retinopathy-resized</td>
    </tr>       
</table>


VeriSeti Kullanımı ve Teşhis Sınıflandırması aşağıdaki tabloda verilmiştir.

<table style="border: 1px solid;">
    <tr>
        <th style="text-align: center" colspan=3>DataSet Diagnosis - VeriSeti Teşhis Sınıflandırması </th> 
    </tr>    
    <tr>
        <th>Class (Sınıf)</th>
        <th>Diagnosis (Teşhis)</th>
    </tr>   
    <tr>
        <td>0</td>
        <td>No DR (Diyabetik Retinopati Yok)</td> 
    </tr>    
    <tr>
        <td>1</td>
        <td>Mild (Hafif Seviyede) </td>
    </tr>    
    <tr>
        <td>2</td>
        <td>Moderate (Orta Seviyede)</td>
    </tr>    
    <tr>
        <td>3</td>
        <td>Severe  (İleri Seviyede) </td>
    </tr>
    <tr>
        <td>4</td>
        <td>Poliferative DR (Körlük Başlamak üzere veya Başlamış)</td>
    </tr>       
</table>

Biz Bu Repoda EfficientNet-V2-L Modelini Kullandık. Daha fazla bilgi bağlantıdaki için Tensorflow Kurumsal sayfasına bakınız:https://www.tensorflow.org/api_docs/python/tf/keras/applications/efficientnet_v2/EfficientNetV2L 


Efficient-Net-V2 Modelleri:
<table>
<thead>
<tr>
<th>V2 Model</th>
<th>Params</th>
<th>Top1</th>
<th>Input</th>
<th>ImageNet21K</th>
<th>Imagenet21k-ft1k</th>
<th>Imagenet</th>
</tr>
</thead>
<tbody>
<tr>
<td>EffV2B0</td>
<td>7.1M</td>
<td>78.7</td>
<td>224</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b0-21k.h5" rel=nofollow>v2b0-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b0-21k-ft1k.h5" rel=nofollow>v2b0-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b0-imagenet.h5" rel=nofollow>v2b0-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2B1</td>
<td>8.1M</td>
<td>79.8</td>
<td>240</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b1-21k.h5" rel=nofollow>v2b1-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b1-21k-ft1k.h5" rel=nofollow>v2b1-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b1-imagenet.h5" rel=nofollow>v2b1-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2B2</td>
<td>10.1M</td>
<td>80.5</td>
<td>260</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b2-21k.h5" rel=nofollow>v2b2-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b2-21k-ft1k.h5" rel=nofollow>v2b2-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b2-imagenet.h5" rel=nofollow>v2b2-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2B3</td>
<td>14.4M</td>
<td>82.1</td>
<td>300</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b3-21k.h5" rel=nofollow>v2b3-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b3-21k-ft1k.h5" rel=nofollow>v2b3-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-b3-imagenet.h5" rel=nofollow>v2b3-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2T</td>
<td>13.6M</td>
<td>82.5</td>
<td>320</td>
<td></td>
<td></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-t-imagenet.h5" rel=nofollow>v2t-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2S</td>
<td>21.5M</td>
<td>84.9</td>
<td>384</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-s-21k.h5" rel=nofollow>v2s-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-s-21k-ft1k.h5" rel=nofollow>v2s-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-s-imagenet.h5" rel=nofollow>v2s-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2M</td>
<td>54.1M</td>
<td>86.2</td>
<td>480</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-m-21k.h5" rel=nofollow>v2m-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-m-21k-ft1k.h5" rel=nofollow>v2m-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-m-imagenet.h5" rel=nofollow>v2m-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2L</td>
<td>119.5M</td>
<td>86.9</td>
<td>480</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-l-21k.h5" rel=nofollow>v2l-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-l-21k-ft1k.h5" rel=nofollow>v2l-21k-ft1k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-l-imagenet.h5" rel=nofollow>v2l-imagenet.h5</a></td>
</tr>
<tr>
<td>EffV2XL</td>
<td>206.8M</td>
<td>87.2</td>
<td>512</td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-xl-21k.h5" rel=nofollow>v2xl-21k.h5</a></td>
<td><a href="https://github.com/leondgarse/keras_efficientnet_v2/releases/download/effnetv2_pretrained/efficientnetv2-xl-21k-ft1k.h5" rel=nofollow>v2xl-21k-ft1k.h5</a></td>
<td></td>
</tr>
</tbody>
</table>






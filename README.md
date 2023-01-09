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
        <td>"https://www.kaggle.com/competitions/aptos2019-blindness-detection/data" </td>
    </tr>
    <tr>
        <td>Messidor-2-Resized</td>
        <td>"https://www.kaggle.com/datasets/tanlikesmath/diabetic-retinopathy-resized" </td>
    </tr>       
</table>


VeriSeti Kullanımı ve Teşhis Sınıflandırması aşağıdaki tabloda verilmiştir.

<table style="border: 1px solid;">
    <tr>
        <th style="text-align: center" colspan=3>DataSet Diagnosis - VeriSeti Açıklamaları </th> 
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



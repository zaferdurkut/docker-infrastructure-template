# Docker Compose Boilerplate
Bu Repo Docker-Compose ile projelere altık olması amacıyla oluşturulmuştur. 
- Yapı içersinde app ve db olmak 2 servisten oluşur.
- db Postgresql olarak ayarlanmış olup docker-compose.yml içersinden konfügüre edilebilir. 
- app ubuntu:16.04 üzerinde oluşturulmuştur. Genel kullanılan paketler kurulmuştur. Buna ek olarak coğrafi veri işleme işlemlerinde servisin kullanılabilmesi için gdal kütüphanesi eklenmiştir.
- Django projesine altlık olması amacıyla oluşturulmuştur ve default.env dosyasında django parametreleri default olarak girilmiştir.
- Serviste Python 3 vardır. requirements.txt içerisine kurulacak kütüphaneler eklenmelidir.

## Yapının Kullanılması

Kurulum için docker kurulu olmalıdır. Docker kullanılmadan kurulum için requirements.txt içerisinde lib'ler python 3 için kurulmalıdır. Docker ile kurulum için sırası ile;

```
git clone https://github.com/zaferdurkut/docker_boilerplate.git
```
Projenizin adı değiştirilir.
```
mv docker_boilerplate your_project_name
```

Projeye gidilir
```
cd your_project_name
```
Mevcut readme dosyası ve git yapısının sizin projenizi etkilememesi için dosyalar silinir ve kendi readme ve git yapınızı oluşturuabilirsiniz.
```
rm -rf README.md .git
```
Bundan sonraki süreçte ilgili projeyi kendiniz için konfügüre edip çalışmalarınızda kullabilirsiniz.

Çalışıcak verilere servisin ulaşabilmesi için .env oluşturmayı unutmayın. :)
```
cp default.env .env
```

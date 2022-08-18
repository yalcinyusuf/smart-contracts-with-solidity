# smart-contracts-with-solidity
A self-executing contract with Solidity on the blockchain network

Smart Contracts, alıcı ve satıcı arasındaki sözleşmenin şartlarının doğrudan kod satırlarına yazıldığı, kendi kendini yürüten bir sözleşmedir. Kod ve içerdiği anlaşmalar, dağıtılmış, merkezi olmayan bir blok zinciri ağında bulunur. Kod, yürütmesi kontrol edilebilir, işlemler izlenebilir ve geri alınamaz.

Smart Contracts is a self-executing contract where the terms of the contract between buyer and seller are written directly into lines of code. The code and the agreements it contains reside on a distributed, decentralized blockchain network. The code is controllable for execution, transactions are traceable and irreversible

### Starting your project

Remix IDE'ye girilir ve yukarıdaki birinci seviye için başlangıç kodunu kullanarak AssociateProfitSplitter.sol adlı yeni bir sözleşme oluşturulur.

Sözleşmeyi geliştirirken ve test ederken, Ganache geliştirme zincirini kullanılır. Ganache new workspace ya da quickstart diyerek başlatılabilir. Ganache ve MetaMask'ı bağlamak için MetaMask'te içeri aktar seçilir ve Ganache'deki index 0 keyi girilir. Metamask'te test ağlarını gösteri seçip, Localhost 8545 seçildiğinde 0 ETH, 100 ETH olacaktır.

![image](https://user-images.githubusercontent.com/61952281/175500812-25a9ee9a-e3a4-4701-9c17-2f7cae4e5f7f.png)

![image](https://user-images.githubusercontent.com/61952281/175500740-2df92596-f1c3-4ac6-9b41-c0172f628679.png)


### Level One: The AssociateProfitSplitter Contract
Ether'i sözleşmeye kabul edecek ve Ether'i ortak seviye çalışanlar arasında eşit olarak bölüştürecektir. Bu, İnsan Kaynakları departmanının çalışanlara hızlı ve verimli bir şekilde ödeme yapmasını sağlayacaktır.

![image](https://user-images.githubusercontent.com/61952281/175501285-ac649cbd-297c-4903-a513-3aefd85de57a.png)


Remix IDE’ye AssociateProfitSplitter.sol adlı kod yüklenir ve derlenir. Ardından deploy kısmında Ganache’deki index1, index2 ve index3’teki adresleri yapıştırılır ve transact edilir. Ve sonuç:
Value: 0 girildiğinde:
![image](https://user-images.githubusercontent.com/61952281/175501503-83603a8f-4c9c-4dd0-944c-2b4740dcac3f.png) ![image](https://user-images.githubusercontent.com/61952281/175501524-b33eacf1-6899-49fc-b1ce-187e19e9edb9.png)

Ufak bir işlem ücreti keser. Ardından ether seçilip value 33 ile deposit edildiğinde:

![image](https://user-images.githubusercontent.com/61952281/175501888-906cdf31-35f7-4ccc-b16e-4943927ac18b.png) ![image](https://user-images.githubusercontent.com/61952281/175501931-2536cc5e-7dce-4e97-a9fc-77a3b112c19b.png)

### Level Two: The TieredProfitSplitter Contract

Gelen Ether'i farklı yüzdelerle farklı seviyelerdeki çalışanlara dağıtır.

![image](https://user-images.githubusercontent.com/61952281/175525573-f809e0a2-c6a4-4ccc-8f13-7a66c61effc6.png)

Bu sefer değişiklik olsun diye qucikstart ile değil new workspace açarak Ganache’ye girildi. Daha sonra Ganache ile MetaMask’ı bağlandı. Burada Metamask’te Ganache 3 adında index 0’ın keyini girerek import edilir. Localhost 8545’i seçildiğnden emin olun, 0 ETH, 100 ETH olacaktır.

![image](https://user-images.githubusercontent.com/61952281/175525629-0366cfeb-bbd3-40f3-8aa4-8def74ed1c36.png)

![image](https://user-images.githubusercontent.com/61952281/175525669-9f772d04-b2e8-43ff-917b-bda6fba427dd.png)

Remix IDE’ye kod yüklenir ve derlenir. Ardından deploy kısmında Ganache’deki index1, index2 ve index3’teki adresleri yapıştırılır ve transact edilir. Ve sonuç:
Value: 0 girildiğinde:

![image](https://user-images.githubusercontent.com/61952281/175525818-179eff99-0b0c-4db8-9afb-ab153d84335e.png) ![image](https://user-images.githubusercontent.com/61952281/175525828-733a0e9c-181e-458b-bff4-c4ebf6b86918.png)

Ardından value 30 ile deposit edildiğinde:

![image](https://user-images.githubusercontent.com/61952281/175525881-ac6d64cd-3395-4067-a25d-eb0236f00819.png)
![image](https://user-images.githubusercontent.com/61952281/175525901-fe7ec561-a9c6-4582-9adf-402fbe79a9c0.png) ![image](https://user-images.githubusercontent.com/61952281/175525919-844f3371-d6ad-4b13-bf2d-095115a1e5e3.png)

30 miktarı aşağıda görüldüğü üzere kod gereği sırasıyla %60, %25, % 15 oranında dağıtılmıştır.

![image](https://user-images.githubusercontent.com/61952281/175525961-28af9b5a-d463-4618-9caf-86625af950b1.png)

### Level Three: The DeferredEquityPlan Contract

Bu sözleşmede, çalışana 4 yıl boyunca 1000 hissenin dağıtılacağı "ertelenmiş öz sermaye teşvik planı"nı yönetilecektir. Kodu derlenir ve çalıştırılır. Başlangıç tarihi bugün olarak belirlenir.
Value 0 ile transact edilir. Burada Ether olması önemli değil.

![image](https://user-images.githubusercontent.com/61952281/175526612-6035e72f-c24d-4c3f-aa5a-c7039dec0a14.png)

Aşağıdaki şekilde farkettiğiniz üzere hisselerin 0 olduğunu görülmektedir. 
0:uint256: 0 şeklinde yazmaktadır.

![image](https://user-images.githubusercontent.com/61952281/175526643-809304e6-1ce9-4de6-b4ff-24fab3ebc470.png)

Burada distribute tıklarsanız hata alınır çünkü henüz 1 sene çalışılmadı. Fastforward tıklandığında zamanı 366 gün ileri alacaktır.

![image](https://user-images.githubusercontent.com/61952281/175526793-30b830c4-f674-47bd-8558-d5da5eb60238.png)

Bundan sonra distribute tıklandığında 1 yıllık hisseyi verecektir. Yani bu değer 250 olacaktır. 

![image](https://user-images.githubusercontent.com/61952281/175526870-ea5d7630-0817-4760-aa84-4983bff18304.png)

Bu şekilde fastforward, ardından distribute tıklandığında senelik hisselerimizi verecektir. 1000’den sonra artmayacaktır çünkü bu kadar hakkımız vardır.

![image](https://user-images.githubusercontent.com/61952281/175526946-736e782d-5862-42b5-8852-5e0b3368d5bd.png) ![image](https://user-images.githubusercontent.com/61952281/175526958-0e41eb53-0316-4be0-b16f-115955927d04.png) ![image](https://user-images.githubusercontent.com/61952281/175526969-2e01f9db-e1e0-4d1b-9823-30ca45f94dcb.png)

Deactivate diyerek kontrat de aktif edilir.

![image](https://user-images.githubusercontent.com/61952281/175527034-b3d79bb2-1cd8-4f86-8b92-af9d751ed57e.png)












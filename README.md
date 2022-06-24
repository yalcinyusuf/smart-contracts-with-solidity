# smart-contracts-with-solidity

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



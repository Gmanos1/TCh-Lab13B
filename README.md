# **Konrad Miziński**
## **Laboratorium TCh, Laboratorium 13.**

Do zadania zostało przygotowane 5 wersji deploymentu.

Pierwszy, początkowy deployment (plik lab13b-nginx-deployment.yaml) wdraża usługę składająca się z 3 kopii poda, w którym znajduję serwer nginx na wersji obrazu"stary".

[Link do obrazów na Dockerhubie](https://hub.docker.com/repository/docker/gmanos/lab13b)
### Kolejne wersje:

-  .v2 - zwiększenie liczby replik do 7
- .v3 - liczba replik 6, zmiana obrazu na wersję "nowy"
- .v4 - rezerwacja i limity zasobów

Przy wdrażaniu nowszych wersji danego deploymentu, kubernetes tworzył nowe wersje ReplicaSet uruchamiając w nich nowe wersje Podów. Pody zostały zabijane. Wyjątkiem jest tutaj zwiększanie ilości replik danego poda, nie powoduje to utworzenie nowego ReplicaSet, natomiast powoduje zwiększenie (lub zmniejszenie) liczby Podów w aktualnie działajacym ReplicaSetcie.

Przed wykonaniem rollbacka (po wdrożeniu wszystkich nowych wersji) Pody pracowały przy wykorzystaniu obrazu "nginx.nowy" (przed ostatni screen) po wykonaniu rollbacku do wersji 1 (po zwiększeniu liczby replik do 6), Pody z nowszych wersji ReplicaSet zostały zabite, a odtworzone w pierwszej wersji ReplicaSet. 
### Wykonanie zadania:
![](/screenshots/1.png)
![](/screenshots/2.png)
![](/screenshots/3.png)
![](/screenshots/4.png)
![](/screenshots/5.png)
![](/screenshots/6.png)
![](/screenshots/7.png)
![](/screenshots/8.png)
![](/screenshots/9.png)
![](/screenshots/10.png)



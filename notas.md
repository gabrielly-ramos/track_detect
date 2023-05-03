# Identificar a pista no C# a partir dos dados de uma volta!

## Identificar quais os possíveis autódromos pelas coordenadas da linha de chegada! 1 ou n. Se 1, é a pista!

- Temos um par de coordenadas para o sensor do lado direito e outro para o sensor do lado esquerdo ...
- Identificar a direção pela orientação do carro (NX = NegativeX, PX=PositiveX) ao passar a linha de chegada!
    > Usar a direção, considerando Packet.Position e a posição anterior (armazenar) ... 
- Identificar o traçado, se o autódromo tiver mais de 1, pela coordenadas percorridas (MaxX, MaxZ, MinX, MinZ)!

- Se o mesmo traçado tiver variações (chicane), analisar a distância percorrida! 
    > Em Barcelona anda mais quanto não pega a Chicane, nos outros anda menos!
        If Barcelona 
        If LapDistance - NoChicaneTrackLenght > LapDistance - ChicaneTrackLenght:
            ChicaneLayout
        Else
            FullTrack			
        Else
        If LapDistance - NoChicaneTrackLenght > LapDistance - ChicaneTrackLenght:
            FullTrack
        Else
            ChicaneLayout
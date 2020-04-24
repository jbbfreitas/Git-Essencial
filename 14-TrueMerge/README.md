### True Merge

Na lição 13 mostramos o merge fast forword, ou merge automático. Esse merge é realizado pelo prórpio git pois não há conflito entre as versões que estão sendo "mergeadas". 

O conflito ocorre quando, após a criação do branch (que será reintegrado) o master sofre alguma alteração e essa alteração "conflita" com a alteração que foi realizadas no branch.


Observe a Figura 1

<p align="center">
  <img src="../imagens/TrueMerge.png" alt="Um exemplo de conflito que pode necessitar de um TrueMerge">
</p>
<p align="center">
   <strong>Figura 1- Um exemplo de conflito que pode necessitar de um TrueMerge</strong> 
</p>

Na Figura 1, o branch foi criado a partir do hash `534de`. Depois que o branch foi criado, outros commits foram realizados no master (3 para ser mais exato) e o merge será realizado no commit `ab8a77`. Se no commit `ab8a77` houver conflito com o branch, o git nos informa disso e temos que resolvê-lo manualmente.

Vamos fazer um exemplo e tudo ficará mais claro.

1-
Desafio 1
O código baseia-se em uma estrutura de Fila Padrão (FIFO), onde o gerenciamento é feito por dois ponteiros estratégicos: inicio e fim. O ponteiro fim permite que a operação de enqueue ocorra com custo constante, conectando o novo nó ao último elemento sem percorrer toda a lista. No momento do atendimento, o ponteiro inicio avança para o próximo nó, liberando a memória do cliente atendido. O cálculo do tempo de espera é realizado através de uma variável acumuladora que soma o tempoAtendimento de cada cliente processado, refletindo a latência acumulada para o próximo da fila.

Desafio 2
Diferente da fila convencional, este código utiliza uma Inserção Ordenada. Em vez de simplesmente adicionar ao final, a função enqueuePrioridade percorre a lista encadeada para encontrar a posição exata do novo documento baseada no campo prioridade.

Critério de Prioridade: O algoritmo compara os valores inteiros, tratando números menores como precedentes.

Critério de Desempate: Para garantir que documentos com a mesma prioridade respeitem a ordem de chegada, a busca na lista utiliza o operador <=. Isso faz com que o ponteiro de inserção avance até o último elemento de mesma prioridade, posicionando o novo nó logo após os veteranos, mantendo assim o comportamento FIFO em casos de empate.

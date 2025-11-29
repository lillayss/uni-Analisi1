	$$f:\quad[a,b] \longrightarrow \mathbb{R}$$
	
E' una funzione __qualsiasi__ limitata
$$ \exists\: M \geq 0\:t.c \quad|f(x)|\leq M\quad\forall x \in [a,b]$$ 

![[Immagine 2025-11-28 203722.png]]

Siccome $f(x)$ è limitata, 
$$|f(x)|\leq M\quad\ \forall x \in[a,b]$$
e l'area sottostante $f(x)$ e' compresa fra 
$$0\leq Area(f(x)) \leq M(b-a)$$
Dove $M(b-a)$ e' l'area di tutto il l'intervallo fino all'altezza $M$
Definendo ora
$$I = inf(\{f(x), x\in[a,b]\})$$
$$S = sup(\{f(x), x\in[a,b]\})$$
Che graficamente vengono rappresentati come:

![[Immagine 2025-11-28 204710.png]]

Utilizzando $S$ e $I$ l'area sotto $f(x)$ viene approssimata molto meglio, infatti
	$$I(b-a)\leq Area(f(x)) \leq S(b-a)$$
Se ora divido l'intervallo $[a,b]$ a meta', riesco ad ottenere una stima ancora piu' accurata.![[Immagine 2025-11-28 205839.png]]

Ora per stimare in maniera ancora piu' accurata l'area della parte di piano che ci interessa, utilizziamo 2 successioni di numeri reali monotone, una crescente ed una decrescente (decrescente quella dall'alto e crescente quella dal basso).
$$\underline{S_n} \leq Area(f(x)) \leq \overline{S_n}$$
Dato $n \in \mathbb{N}$ dividiamo l'intervallo $[a,b]$ in $2^n$ parti uguali.
$$x_{k}^{(n)} = a+k(\frac{b-a}{2^n})$$
con $k=0,1,...,2^n$ 
Tutti questi punti, al variare di $k$ sono tutti equispaziati, ogni suddivisione e' lunga $\frac{b-a}{2^n}$ 
Ogni volta che $n$ aumenta (ad esempio si passa da $n-1$ a $n$ e poi a $n+1$) ogni spazietto si duplica
![[Immagine 2025-11-28 211256.png]]

Ora dati $n\in\mathbb{N}$ e $k\in\{0,1,...,2^{n-1}\}$ definisco i 2 numeri reali:
$$a_{k}^{(n)} = inf(\{f(x), x\in[x_{k}^{(n)}, x_{k+1}^{(n)}]\}$$
$$b_k^{(n)} = sup(\{f(x), x\in[x_{k}^{(n)}, x_{k+1}^{(n)}]\})$$

![[Immagine 2025-11-28 212035.png]]

Cosa succede quando passo da $a_{k}^{(n)}$ a $a_{2k}^{(n+1)}$ e $a_{2k+1}^{(n+1)}$ ?

![[Immagine 2025-11-28 212551.png]]

Ogni volta che viene eseguito il processo di dimezzamento dell'intervallo, gli estremi inferiori salgono
$$a_{2k}^{(n+1)} \geq a_{k}^{(n)}$$
$$a_{2k+1}^{(n+1)} \geq a_{k}^{(n)}$$
Ora definisco le 2 successioni dove $\underline{S_n}$ e' la somma delle aree dei rettangoli da sotto mentre $\overline{S_n}$ e' la somma dei rettangoli da sopra. 
$$\underline{S_n} = \sum_{k=0}^{2^n-1}(a_{k}^{(n)} )(\frac{b-a}{2^n})$$
$$\overline{S_n} = \sum_{k=0}^{2^n-1}(b_{k}^{(n)} )(\frac{b-a}{2^n})$$
Queste due somme vanno interpretate come se $\frac{b-a}{2^n}$ fosse la base del rettangolo mentre l'altro termine l'altezza, ed il valore della base puo' essere tirato fuori dalla sommatoria perche' e' una costante, dato che tutti gli intervalli sono della stessa lunghezza
$$\underline{S_n} = \frac{b-a}{2^n}\sum_{k=0}^{2^n-1}(a_{k}^{(n)} )$$
$$\overline{S_n} = \frac{b-a}{2^n}\sum_{k=0}^{2^n-1}(b_{k}^{(n)} )$$
Siccome l'estremo superiore e l'estremo inferiore sono calcolati sullo stesso intervallo possono essere messi in relazione
$$a_{k}^{(n)} \leq b_{k}^{(n)}$$
quindi
$$\overline{S_n} \geq Area(f(x)) \geq \underline{S_n}$$
__TEOREMA__

$\overline{S_n}$ e' monotona decrescente mentre $\underline{S_n}$ e' monotona crescente.

__DIMOSTRAZIONE__

Quando si passa da $n$ intervalli a $n+1$ intervalli, ogni intervallo viene suddiviso in 2 sottointervalli, quindi, ogni coefficiente $a_{k}^{(n)}$ viene sostituito da 2 coefficienti $a_{2k}^{(n+1)}$ e $a_{2k+1}^{(n+1)}$
E valgono  queste relazioni:
$$a_{2k}^{(n+1)} \geq a_{k}^{(n)}$$
$$a_{2k+1}^{(n+1)} \geq a_{k}^{(n)}$$


Ora sommando i termini delle due relazioni ottengo una disuguaglianza che descrive $a_{k}^{(n)}$ in funzione dei 2 nuovi coefficienti (IMPORTANTE PER IL PASSAGGIO DOPO)
$$a_{k}^{(n)} \leq \frac{a_{2k}^{(n+1)}+a_{2k+1}^{(n+1)}}{2}$$
Ora mi scrivo $\underline{S_{n+1}}$ 
$$\underline{S_{n+1}} = \sum_{k=0}^{2^{n+1}-1} a_{k}^{(n+1)} (\frac{b-a}{2^{n+1}}) $$
La sommatoria ha $2^{n+1}$ termini (trip assurdo ci ho messo x a capirlo ma dato che si parte da 0, facendo quel -1 il numero di termini e' uguale, se parti da k=0 e arrivi a 4 hai 5 termini in totale, cosi' se parti da k=0 e arrivi a $2^{n+1}-1$ hai effettivamente $2^{n+1}$ termini.)

Siccome $2^{n+1}$ e' positivo, posso raggruppare i termini a coppie, siccome sto studiando le coppie, l'indice della sommatoria cambia andando da $2^{n+1}-1$ che si puo' scrivere come $2*(2^n)-1$ dato che sto studiando le coppie devo smezzarlo quindi gli indici cambiano 
$$\underline{S_{n+1}} = \sum_{k=0}^{2^{n}-1} a_{2k}^{(n+1)} (\frac{b-a}{2^{n+1}}) +a_{2k+1}^{(n+1)} (\frac{b-a}{2^{n+1}}) $$
Raccolgo i fattori comuni
$$\underline{S_{n+1}} = \sum_{k=0}^{2^{n}-1} (a_{2k}^{(n+1)} +a_{2k+1}^{(n+1)})(\frac{b-a}{2^{n+1}})  $$
Scrivo $2^{n+1}$ come $2^{n} * 2$ e lo moltiplico per il termine raccolto
$$\underline{S_{n+1}} = \sum_{k=0}^{2^{n}-1} \frac{(a_{2k}^{(n+1)} +a_{2k+1}^{(n+1)})}{2}(\frac{b-a}{2^{n}})$$
Stando alla disuguaglianza di prima, $\frac{(a_{2k}^{(n+1)} +a_{2k+1}^{(n+1)})}{2}$ e' maggiore o uguale di $a_{k}^{(n)}$

quindi
$$\underline{S_{n+1}} \geq \sum_{k=0}^{2^{n}-1} a_{k}^{(n)}(\frac{b-a}{2^{n}})$$
allora e' vero che
$$\underline{S_{n+1}} \geq \underline{S_{n}}$$
quindi $\underline{S_{n}}$ e' monotona crescente

Da aggiungere definizione di intergrale di Reinmann
---
title: Ejercicios Tema 1
subtitle: Curvas y superficies
author: Blanca Cano Camarero
date: \today
documentclass: scrartcl
toc: true
toc-depth: 2
toc-title: Índice
header-includes:
- \usepackage[spanish,es-tabla]{babel}
- \newcommand{\R}{\mathbb R}
- \newcommand{\al}{\alpha (t)}
- \newcommand{\kl}{k (t)}
- \newcommand{\ptt}{t \in \R}
- \newcommand{\ep}{ \epsilon}
- \usepackage{chngcntr}
- \usepackage{graphicx}
---

<!--documentclass: report -->
\newpage 

# Ejercicio 7   

Sea la curva $\alpha : \R \longrightarrow \R ^2$ dada por $\al = (t, t^3)$, para todo $t \in \R$.  

(a) Comprueba que es regular.  

(b) Prueba que $\kl = \frac{6t}{(1+9t^4 ) ^ {\frac{3}{2}}}$ y que, en particular $\kl = -k(-t)$ para todo $\ptt$.   

(c) Observa que la $Img(\alpha)$ es simétrica respecto del punto $\alpha(0)$ (es decir, que el giro de centro $\alpha(0)$ y el 
ángulo $\pi$ deja a $Img(\alpha)$ invariante).   

(d) Motivado por lo anterior, si $\alpha: (- \epsilon, \epsilon ) \longrightarrow \R ^2$ con  $\epsilon > 0$ o $\epsilon > \infty$,
es una curva regular cuya curvatura cumple que $\kl = -k(-t)$ para todo $t \in (- \epsilon, \epsilon )$, ¿podemos afirmar que 
$Img(\alpha)$ es simétrica respecto del punto $\alpha(0)$.   


## a) Regularidad 


Se tiene que $\al ' = (1, 3t^2)$ que no se anula sea cual sea $t \in \R$ gracias a su primera componente, luego es regular. O de otra manera, por ser una norma $|\al'| = 0$ si y solo si $\al' = 0$; si  $|\al'| = 0$ equivale a que  $|\al'|^2 = 0$ y sabemos que $|\al'|^2 = 1 + 3t^4 \geq 1 > 0$ para todo $t$, de donde deducimos que no se anula, es decir  $\al$ es regular.  


## b) Cálculo de su curvatura y ver que es impar.  

Para este apartado veremos que $\al$ es la parametrización natural de la gráfica de la función cúbica $f(x) = x^3$. 

Esto es $\al = (t, f(t))$

\includegraphics[width=\linewidth]{./media/cubica.png}


Además para este tipo de curvas su curvatura puede calcularse de la expresión: 

$$\kl = \frac{f''(t)}{ (1+ f'(t)^2 ) ^{\frac{3}{2}}}$$
calculando $f'(t) = 3 t^2$ y   $f''(t) = 6 t$, podemos concluir que 

$$\kl = \frac{ 6t}{ (1+ 9t^4 ) ^{\frac{3}{2}}}$$  

como se quería probar. 

Finalmente veamos que independientemente del valor de $\ptt$

$$- k(-t) =  -\frac{ 6(-t)}{ (1+ 9(-t)^4 ) ^{\frac{3}{2}}} = \frac{ 6t}{ (1+ 9t^4 ) ^{\frac{3}{2}}} = \kl.$$ 



## c) Simetría de  $Img(\alpha)$ respecto del punto $\alpha(0)$  



Sea $G(x,y)=(-x,-y)$ para todo $t \in \R ^2$ el giro de $\pi$ radianes respecto del origen. 

Observemos que $G \al = G (t, t^3) = (-t,-t^3) = \alpha( -t)$, es decir, que el giro lo deja invariante 
como queríamos ver.   

## d) Simetría de la imagen por paridad de la función curvatura   

Como hipótesis tenemos una curva  $\alpha: (- \epsilon, \epsilon ) \longrightarrow \R ^2$ regular, que además su curvatura cumple 
$\kl = -k(-t) \text{ para todo } t \in (- \epsilon, \epsilon ).$  

Consideremos el movimiento rígido $M$ de $\R ^2$  que cumple que $M(\alpha(0)) = (0,0)$, que $\overrightarrow{M}_{e_1(0)} = (1,0)$ y 
 que $\overrightarrow{M}_{e_2(0)} = (0,1)$.  
 
 Luego la curva $M \circ \alpha :(- \epsilon, \epsilon ) \longrightarrow \R ^2$ es regular y congruente con $\alpha$, cumple además que
 que $e ^{M \circ \alpha}_1(0) = (1,0)$ y $e ^{M \circ \alpha}_2(0) = (0,1)$
 Si probamos que 
 
 \begin{equation*}
 G(M \circ \alpha (-t)) =  M \circ \alpha (t) \text{ para todo }t, 
 \end{equation*}

siendo $G(x,y) = (-x,-y)$ la aplicación giro definida en el apartado anterior, tendríamos que $Img(M \circ \alpha)$ es invariante a un giro de $\pi$ radianes con centro 0. 




Por tanto $M^{-1} \circ G \circ M \circ \alpha (-t) = \al$ y   $M^{-1} \circ G \circ M$ es un giro de $\pi$ radianes con centro en $p$.

Por geometría afín sabemos que $p \in  \R^2$ es el único punto fijo del giro: 

$M^{-1}  G  M(p) = p$  o equivalentemente $G M(p) = M (p)$, el único punto figo para $G$.

$M^{-1} \circ G \circ M$ es un movimineto rígido directo con un único punto fijo, luego es un giro. 

FALTA UNA CONSIDERACIÓN   

Sólo tenemos que ver que 

$$G(M \circ \alpha)(-t) = (M \circ \alpha)(t), \text{ para todo } t \in (- \epsilon, \epsilon )$$

Para ello definimos $\gamma = M \circ \alpha$ y $\beta(t) = G \circ \gamma(-t).$  

Se cumple que 
\begin{equation} 
\gamma (0) = \beta(0)
\end{equation}
ya que $G \gamma(0) =  \gamma(0)$ al ser el centro de giro. 

Además, por la regla de la cadena: 

\begin{equation}
\beta '(t) = - G \gamma'(-t) = - G( \gamma'(-t)_x, \gamma'(-t)_y) = - (- \gamma'(-t)_x, - \gamma'(-t)_y) = \gamma'(-t)
\end{equation}
Donde $\gamma'(t) = (\gamma'(t)_x, \gamma'(t)_y)) \in \R^2$ es una mera notación de un vector como sus respectivas coordenadas.   

Luego en el caso particular del origen: 
\begin{equation*}
\beta '(0) = - G \gamma'(0) = - G (1,0) = - (-1,0) = (1,0) = \gamma'(0)
\end{equation*}

Esto quiere decir que $J \beta'(0) = J \alpha '(0)$ ya que tienen el mismo vector velocidad y $\alpha$ es congruente a $\gamma = M \alpha$.   

O equivalentemente

\begin{align*}
 & e_1 ^{\gamma}(0) = \frac{\gamma'(0)}{|\gamma'(0)|} = \frac{\beta'(0)}{|\beta'(0)|} =  e_1 ^{\beta}(0) \\
& e_2 ^{\gamma}(0)  = Je_1 ^{\gamma}(0) = Je_2 ^{\beta}(0)  = e_2 ^{\beta}(0)
\end{align*}
 
 Además de manera más general tenemos que: 
 
 De manera más general en virtud de (2):   

\begin{align}
  e_1 ^{\beta}(t) &= \frac{\beta'(t)}{|\beta'(t)|} = \frac{\gamma'(-t)}{|\gamma'(-t)|} =   e_1 ^{\gamma}(- t)
\end{align}


\begin{align*}
\tilde{e_2} ^{\beta}(t) &= \beta''(t)  - <\beta''(t),e_1 ^{\beta}(t) >e_1 ^{\beta}(t) \\
  & = - \gamma''(-t) - < - \gamma''(-t),e_1 ^{\gamma}(-t) >e_1 ^{\gamma}(-t)\\ 
  & = - \gamma''(-t) + < \gamma''(-t),e_1 ^{\gamma}(-t) >e_1 ^{\gamma}(-t)\\ 
  &= - (\gamma''(-t) - <\gamma''(-t),e_1 ^{\gamma}(-t) >e_1 ^{\gamma}(-t)) \\
  & = - \tilde{e_2}^{\gamma} (-t)
\end{align*}

\begin{equation}
e_2 ^{\beta}(t) = \frac{\tilde{e_2} ^{\beta} (t)}{|\tilde{e_2} ^{\beta}(t)|} = 
\frac{- \tilde{e_2}^{\gamma} (-t)}{|- \tilde{e_2}^{\gamma} (-t)|} = - e_2^{\gamma} (-t)
\end{equation}


Veamos ahora que $k_{\gamma} (t) = k_{\beta}(t)$ para todo $t$.   

Como $\gamma = M \circ \alpha$, con $M$ movimiento rigído cualquiera distinguiremos si éste es positivo o negativo: 

- Si es directo entonces $k_{\gamma} (t) = k_{\alpha}(t)$ y bastará con aplicar la hipótesis del problema en la segunda igualdad para ver que  

$$- k_{\gamma} (- t) = - k_{\alpha} (- t) = k_{\alpha} (t) =  k_{\gamma} (t), \quad \forall t \in (- \epsilon, \epsilon )$$

- Si $M$ es un movimiento rígido inverso, entonces $k_{\gamma} (t) = -k_{\alpha}(t)$ y de igual forma se tiene que 

$$- k_{\gamma} (- t) = - (- k_{\alpha} (- t))  = - k_{\alpha} (t) =  k_{\gamma} (t), \quad \forall t \in (- \epsilon, \epsilon )$$


De donde deducimos que independientemente del movimiento rígido aplicado

\begin{equation} 
- k_{\gamma} (- t) = k_{\gamma} (t) \text { para todo } t \in (- \epsilon, \epsilon ).
\end{equation}    
 

Observemos ahora además que $\beta$ es una reparemetrización de $\gamma$ compuesta con un movimiento rígido directo $G$.   Donde $\phi(t) = -t$ es el difeomorfismo de $\mathbb R \longrightarrow \mathbb R$ tal que $\beta = G \circ \gamma \circ\phi$. 

La curvatura se mantiene por movimientos rígidos directos, mientras que para reparametrizaciones  con derivada negativa ($\phi ' (t) = -1 < 0$) es opuesta, 
se tiene que 

$$k_{\beta}(t) = k_{G \circ \gamma \circ\phi}(t) = k_{\gamma \circ\phi} (t) = - k_{\gamma \circ\phi} (- t)$$  

Y en virtud de la igualdad ( -2) 

$$k_{\beta}(t) =  k_{\gamma}(t)$$


Alternativamente se podía haber usado la definición de curvatura y (2):  

\begin{equation*}
k_{\beta}(t) = \frac{a_{12}^{\beta}(t)}{|\beta '(t)|} =
\frac{<\beta ''(t), J \beta'(t)>}{|\beta '(-t)| ^3} = 
\frac{<- \gamma ''(-t), J \gamma'(-t)>}{|\gamma '(-t)| ^3}
= - k_\gamma(-t)
\end{equation*}


Y utilizando de nuevo (_) se tendría que  $k_{\beta}(t) = - k_\gamma(-t) = k_\gamma(t).$   


El teorema de unicidad global afirma que existe un único movimiento rígido directo $F$ tal que $\beta = F \circ \gamma$.  

Además por (1) sabemos que $F (\gamma(0)) = \beta$ y 
que $\overrightarrow{F}(e_i^{\beta}(0)) = e_i^{\gamma}(0)$ para $i \in \{1,2\}$. Así que tenemos que $F$ deja fijo un punto y además 
$\overrightarrow{F} = \overrightarrow{Id}$. 

Por lo que por geometría a fin necesariamente $F = Id_{\mathbb R^2 \times \mathbb R^2}$ y que 

$$\gamma = \beta = G (\gamma (-t)) \quad \forall t \in (- \epsilon, \epsilon)$$
 

<!--%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%-->











\newpage 

\setcounter{equation}{0}
# Ejercicio 11     


Sea $\alpha : I \longrightarrow \R ^3$ una curva parametrizada por la longitud del arco y tal que $\alpha '' (t) \neq 0$ para todo $t \in I$, 
y con $k>0$, $\tau >0$. Se considera la curva $\beta (t) = \int_{t_0}^t e_3(s) ds$, donde $e_3(t)$ es el vector binormal a $\alpha$ en $t$.  


(a) Comprueba que $\beta$ está parametrizada por la longitud del arco.   
(b) Construye del triedro de Frenet de $\beta$.  
(c) Calcula las funciones curvatura y torsión, $k_{\beta}$ y $\tau_{\beta}$.   

## a)  Comprueba que $\beta$ está parametrizada por la longitud del arco.  

Por el teorema fundamental del cálculo se tiene que $\beta' (t) = e_3(t)$, por ser $e_3(t)$  el vector binormal a $\alpha$ en $t$, su módulo será 
siempre uno para todo $t$, luego acabamos de probar que $\beta$ está parametrizada por la longitud del arco.   

## b) Construcción del triedro de Frenet de $\beta$.   

Para no confundirnos con el triedro de Frenet de $\alpha$ $\{e_1, e_2, e_3 \}$, utilizaré la notación $\{ \ep_1, \ep_2, \ep_3\}$ para referirme al triedro de Frenet de $\beta$.  


Por definición y estar parametrizada sabemos que   

\begin{equation}
\ep_1 (t) = \frac{\beta'(t)}{|\beta'(t)|} = \beta'(t) = e_3(t)
\end{equation}
Con lo que acabamos de calcular $\ep_1$. Por otro lado 

\begin{multline*}
\tilde{\ep_2} (t) = \beta''(t) - <\beta''(t),\ep_1 (t)>\ep_1 (t)
= e_3'(t) - <e_3'(t),e_3(t)>e_3(t)
\end{multline*}


Gracias a las ecuaciones de Frenet conocemos que $e_3'(t) = -a_{23} e_2$ ;  sustituyendo en la ecuación anterior y teniendo en cuenta la linealidad
del producto escalar y la perpendicularidad entre los vectores del triedro de Frenet de $\alpha$:   

\begin{equation*}
\tilde{\ep_2} (t) = -a_{23} e_2 - < -a_{23} e_2,e_3(t)>e_3(t) = -a_{23} e_2 
\end{equation*}  

Luego podemos concluir que 


\begin{equation}
\ep_2 = \frac{\tilde{\ep_2} (t)}{|\tilde{\ep_2} (t)|} = \frac{ -a_{23} e_2 }{|-a_{23} e_2|} = -e_2
\end{equation}  


Finalmente 

\begin{equation}
\ep_3 (t) = \ep_1 \times \ep_2 = e_3 \times -e_2 = e_1
\end{equation}  


Gracias a las igualdades (1), (2) y (3)  podemos afirmar que el triedro de Frenet de $\beta$ es $\{ e_3, -e_2, e_1\}$. 


## c) Cálculo de las funciones curvatura y torsión, $k_{\beta}$ y $\tau_{\beta}$.     


Por definición  de curvatura,  estar $\alpha$ y $\beta$ parametrizadas por la longitud del y el apartado (b) 

\begin{equation*}
k_{\beta}(t) = \frac{a^{\beta}_{12}(t)}{|\beta'(t)|} = <\ep^{'}_1(t),\ep_2(t)> = <e'_3(t),-e_2(t)> = -a^{\alpha}_{32}(t) 
=  a^{\alpha}_{23}(t) = \tau_{\alpha}(t) |\alpha'(t)| = \tau_{\alpha}(t).
\end{equation*}


Veamos ahora la torsión 

\begin{equation*}
\tau _{\beta}(t) = \frac{a^{\beta}_{23}(t)}{|\beta'(t)|} = <\ep^{'}_2(t),\ep_3(t)> = <-e_2'(t) ,e_1'(t)> = -a^{\alpha}_{21}(t) 
=  a^{\alpha}_{12}(t) = k_{\alpha}(t) |\alpha'(t)| =k_{\alpha}(t).
\end{equation*}

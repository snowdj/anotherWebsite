---
layout: post    
title:  "Euler's number"
description: ""
date:   3014-06-20 19:04:00
tags: [math]
categories: math
math: true
comments: true
image:
    feature: star_trail_f.jpg
---

Há alguns anos, enquanto ainda cursava a graduação, proferi um seminário entitulado "A mais bela fórmula da Matemática". Muitos amigos não puderam comparecer e solicitaram uma transcrição do seminário, o que agora forneço, com apenas 6 anos de atraso.

O texto está divido em duas partes independentes. Na primeira parte falaremos sobre o número de Euler e veremos o que o torna tão especial. Na segunda parte estudaremos a fórmula de Euler, uma belíssima ligação entre o número de Euler e as funções trigonométricas no domínio dos números complexos.

Para facilitar o acesso, deixarei aqui links para as duas partes:
<ol>
<li><a href="https://www.blogger.com/blogger.g?blogID=5423916858706600411#section1">O número de Euler</a></li>
<li><a href="https://www.blogger.com/blogger.g?blogID=5423916858706600411#section2">A fórmula de Euler</a></li>
</ol>

Como última observação antes de começarmos, quero deixar claro que a maioria dos desenvolvimentos que farei foram tirados de outras fontes, todavia os devidos créditos serão dados.

<figure>
    <a href="http://www.amazon.com/Dr-Eulers-Fabulous-Formula-Mathematical/dp/0691150370" >
        <img border="0" src="http://press.princeton.edu/images/k8129.gif" height="100" width="133">
    </a>
    <figcaption>Capa do livro de Paul J. Nahin, o qual contém várias aplicações da "Fabulosa Fórmula do Dr. Euler".</figcaption>
</figure>

## 1. O número de Euler
Por muito tempo fiquei intrigado com o uso do número \\( e = 2.7182818... \\) como base do chamado logaritmo natural. Como poderia essa base ser natural? Por que esse número em particular? Como um número irracional pode ser mais natural que qualquer número natural? Encontrei uma resposta satisfatória no trabalho do próprio Euler, apresentado de forma magistral no livro <a href="http://www.amazon.com/Euler-Master-Dolciani-Mathematical-Expositions/dp/0883853280/">Euler: The Master of Us All</a> de William Dunham.

Nosso ponto de partida é a operação de potenciação. Mais especificamente analisaremos potências do tipo \\( a^{\omega} \\) com \\( \omega \\) "pequeno", ou seja, \\( \omega \rightarrow 0 \\) na linguagem mais moderna da teoria dos limites. Na época de Euler, o Cálculo Diferencial e Integral ainda não havia passado pelo processo de formalização que veio a tornar-se o padrão, através do conceito de limites, de modo que Euler utiliza o conceito de infinitesimais: grandezas infinitamente pequenas. Em homenagem a Euler, evitarei o uso de limites neste artigo, utilizando de forma intuitiva e não rigorosa o conceito de infinitesimal. Ainda seguindo Euler, utilizarei como símbolos para essas grandezas infinitesimais as letras gregas \\( \psi \\) e \\( \omega \\).

Observe que \\( a^{\omega} \\) irá se aproximar cada vez mais de \\( 1 \\) à medida que o valor de \\( \omega \\) aproximar-se de \\( 0 \\). Ou seja, podemos escrever
\\[ a^{\omega} = 1 + \psi \implies \psi = a^{\omega} - 1, \tag{1}\label{eq:1} \\]
com \\( \psi \rightarrow 0 \\) sempre que \\( \omega \rightarrow 0 \\).

Tomemos \\( a = 2 \\) e façamos \\( \omega \\) cada vez menor. Obtemos a seguinte tabela:


<table align="center">
    <thead>
        <tr>
            <th colspan="3"> \( a = 2 \) </th>
        </tr>
    </thead>
    <thead>
        <tr>
            <th>  \( \omega \) </th>
            <th> \( \psi \) </th>
            <th> \( k = \frac{\psi}{\omega} \) </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>  \( 0.1 \) </td>
            <td>  \( 0.071773463  \) </td>
            <td> \( 0.717734625 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.01 \) </td>
            <td>  \( 0.006955550  \) </td>
            <td> \( 0.695555006 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.001 \) </td>
            <td>  \( 0.000693387  \) </td>
            <td> \( 0.693387463 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.0001 \) </td>
            <td>  \( 0.000069317 \) </td>
            <td> \( 0.693171204 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.00001 \) </td>
            <td>  \( 0.000006931 \) </td>
            <td> \( 0.693149583 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.000001 \) </td>
            <td>  \( 0.000000693 \) </td>
            <td> \( 0.693147421 \) </td>    
        </tr>
        <tr>
            <td>  \( 0.0000001 \) </td>
            <td>  \( 0.000000069 \) </td>
            <td> \( 0.693147204 \) </td>    
        </tr>
    </tbody>
</table>

Observe que à medida que diminuímos \\( \omega \\), \\( \psi \\) também diminui. Se definirmos a proporção entre o segundo e o primeiro como \\( k = \frac{\psi}{\omega} \\), vemos que essa proporção parece se aproximar de um valor constante, \\( k \approx 0.693 \\) (alguns reconhecerão esse número!).

Vejamos como a tabela fica para \\( a = 5 \\):
<p>
\begin{array}{|c|c|c|c|} \hline
a &amp; \omega &amp; \psi &amp; k = \frac{\psi}{\omega} \\\hline
5 &amp; 1 &amp; 4 &amp; 4; \\
5 &amp; 0.1 &amp; 0.174618943 &amp; 1.746189431 \\
5 &amp; 0.01 &amp; 0.016224591 &amp; 1.622459127 \\
5 &amp; 0.001 &amp; 0.001610734 &amp; 1.610733753 \\
5 &amp; 0.0001 &amp; 0.000160957 &amp; 1.609567434 \\
5 &amp; 0.00001 &amp; 0.000016095 &amp; 1.609450864 \\
5 &amp; 0.000001 &amp; 0.000001609 &amp; 1.609439208 \\ 
5 &amp; 0.0000001 &amp; 0.000000161 &amp; 1.609438043 \\\hline
\end{array}
</p>

A razão \\( k \\) é diferente para \\( a =5 \\), mas ela parece se aproximar de um valor determinado, assim como no caso \\( a = 2 \\).

Tendo em vista que \\( k = \frac{\psi}{\omega} \implies \psi = k \omega \\), podemos reescrever a equação \\( (\ref{eq:1}) \\) como:
\\[ a^\omega = 1 + k \omega.\tag{2}\label{eq:2} \\]
Podemos, a partir dessa equação, isolar \\( a \\):
\\[ a = \left ( 1 + k \omega \right ) ^ {\frac{1}{\omega}}, \\]
onde extraímos a raiz \\( \omega \\)-ésima da equação \\( (\ref{eq:2}) \\).

Para calcularmos uma potência \\( x \\) qualquer de \\( a \\), não necessariamente infinitesimal, podemos fazer
\\[ a^x = \left ( 1 + k \omega \right ) ^ {\frac{x}{\omega}}. \\]
Observe que \\( j = \frac{x}{\omega} \rightarrow \infty \\), dada a natureza infintesimal de \\( \omega \\) (um número finito divido por uma quantidade suficientemente próxima de zero terá como resultado um número tão grande quanto quisermos). Podemos escrever também \\( \omega = \frac{x}{j} \\) e substituir na equação acima, junto com a definição de \\( j \\), o que nos dá
\\[ a^x = \left ( 1 + \frac{kx}{j} \right ) ^ j. \\]

Vamos aplicar o binômio de Newton à essa última equação:
\\[
a^x = 1 + \frac{j}{1!} \cdot \frac{kx}{j} + \frac{j(j-1)}{2!} \cdot \frac{k^2x^2}{j^2} +  \frac{j(j-1)(j-2)}{3!} \cdot \frac{k^3x^3}{j^3} \\\
+  \frac{j(j-1)(j-2)(j-3)}{4!} \cdot \frac{k^4x^4}{j^4} + \dots =\\\
= 1 + \frac{j}{j} \cdot \frac{kx}{1!}+ 
\frac{j(j-1)}{j^2} \cdot \frac{k^2x^2}{2!}+  \frac{j(j-1)(j-2)}{j^3} 
\cdot \frac{k^3x^3}{3!} \\\
+  \frac{j(j-1)(j-2)(j-3)}{j^4} \cdot \frac{k^4x^4}{4!} + \dots =\\\
= 1 + \frac{j}{j} \cdot \frac{kx}{1!}+  \frac{j}{j} \left ( \frac{j-1}{j} \right ) \cdot \frac{k^2x^2}{2!}+\\\
\frac{j}{j} \left ( \frac{j-1}{j} \right ) \left ( \frac{j-2}{j} \right ) 
\cdot \frac{k^3x^3}{3!}\\\
+\frac{j}{j} \left ( \frac{j-1}{j} \right ) \left ( \frac{j-2}{j} \right ) \left ( \frac{j-3}{j} \right ) \cdot \frac{k^4x^4}{4!} + \dots =\\\
= 1 + 1 \cdot \frac{kx}{1!}+ 1 \left ( 1- \frac{1}{j} \right ) \cdot \frac{k^2x^2}{2!}+\\\
1 \left ( 1- \frac{1}{j} \right ) \left (1 - \frac{2}{j} \right ) 
\cdot \frac{k^3x^3}{3!}\\\
+ 1 \left ( 1 - \frac{1}{j} 
\right ) \left ( 1- \frac{2}{j} \right ) \left ( 1- \frac{3}{j} \right )
 \cdot \frac{k^4x^4}{4!} + \dots 
\\]

Agora, se lembrarmos que \\( j \rightarrow \infty \\), veremos que os termos \\( \frac{1}{j} \\), \\( \frac{2}{j} \\), \\( \frac{3}{j} \\), \\( \frac{4}{j}, \dots \rightarrow 0 \\), e a monstruosidade acima se reduz a:
\\[ 
a^x =  1 + kx + \frac{k^2x^2}{2!} + \frac{k^3x^3}{3!} + \frac{k^4x^4}{4!} + \dots\tag{3}\label{eq:3} 
\\]

Fazendo \\( x = 1 \\), imediatamente obtemos o valor de \\( a \\) em função apenas de \\( k \\):
\\[ 
a = 1 + k+ \frac{k^2}{2!} + \frac{k^3}{3!} + \frac{k^4}{4!} + \dots \tag{4}\label{eq:4} 
\\]

Como exemplo, fazendo \\( k = 0.693 \\) e utilizando os quatro primeiros termos dessa equação, obtemos \\( a = 1.9982 \\), valor bem próximo de \\( 2 \\).

De todos os valores possíveis de \\( k \\), qual seria aquele mais "natural"? Qual valor de \\( k \\) faria o cálculo de \\( a^x \\) mais fácil? Se pegarmos \\( k = 0 \\), obteremos \\( a = 1 \\) e, obviamente, todas as potências serão fáceis de calcular, mas seria tudo muito sem graça! O próximo candidato seria \\( k = 1 \\), e aqui as coisas ficam interessantes! O valor de \\( a \\) correspondente à \\( k = 1 \\) tem até uma letra especial para representá-lo: \\( e \\). Assim, fazendo \\( k = 1 \\) na equação \\( (\ref{eq:4}) \\), temos:
\\[
e = 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \dots\tag{5}\label{eq:6}
\\]

E se fizermos \\( k = 1 \\) na equação \\( (\ref{eq:3}) \\), temos:
\\[
e^x =  1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \dots\tag{6}\label{eq:5}
\\]

Compare esta última equação com a equação \\( (\ref{eq:4}) \\). O lado direito das duas são praticamente iguais! Basta trocarmos \\( x \\) por \\(k \\) na equação \\( (\ref{eq:5}) \\) , ou seja:
\\[
e^k =  1 + k + \frac{k^2}{2!} + \frac{k^3}{3!} + \frac{k^4}{4!} + \dots = a.
\\]

Então podemos achar \\( a \\) em função de \\( k \\) com o intermédio de \\(e \\):
\\[
a = e^k,
\\]
e assim, vemos que \\( k \\) nada mais é do que o logaritmo natural de \\( a \\):
\\[
k = \ln{a}.
\\]

Mas afinal, quanto vale \\( e \\)? Graças aos fatoriais em  \\( (\ref{eq:6}) \\), basta somarmos \\( 7 \\) termos para obtermos um valor correto até a terceira casa decimal:
\\[
e \approx 2.718
\\]

Um valor mais preciso seria
\\[
e = 2.718281828459045235360287471352662497757247\dots
\\] 

Caso queira ouvir os \\( 5000 \\) primeiros dígitos de \\( e \\), eu fiz um vídeo:

<div class="separator" style="clear: both; text-align: center;">
</div>
<div class="separator" style="clear: both; text-align: center;">
<object class="BLOGGER-youtube-video" classid="clsid:D27CDB6E-AE6D-11cf-96B8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0" data-thumbnail-src="https://ytimg.googleusercontent.com/vi/ItzSD-Ejis8/0.jpg" height="266" width="320"><param name="movie" value="https://youtube.googleapis.com/v/ItzSD-Ejis8&amp;source=uds" /><param name="bgcolor" value="#FFFFFF" /><param name="allowFullScreen" value="true" /><embed width="320" height="266"  src="https://youtube.googleapis.com/v/ItzSD-Ejis8&amp;source=uds" type="application/x-shockwave-flash" allowfullscreen="true"></embed></object>;</div>
<div class="separator" style="clear: both; text-align: center;">
</div>
<h3 id="section2">
2. A fórmula de Euler</h3>
<h3 id="section2"></h3>
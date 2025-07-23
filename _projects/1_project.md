---
layout: page
title: Towards a weakly nonlinear nonmodal stability theory
description: 
img: assets/img/wnn.png
importance: 2
category: 
related_publications: true
---

As briefly introduced in the &ldquo; <a href='https://ymducimetiere.github.io/projects/2_project/'> Linear modal and nonmodal stability </a> &rdquo; page of this website, the Navier-Stokes operator linearised around a strong background flow is frequently non-normal. In that case, the linear flow response to an external perturbation can be spanned by a generically vast number of nonorthogonal eigenmodes (nonorthogonal under the same inner product as that used to compute the adjoint operator). Accordingly, the corresponding induced norm of the response can take substantial values, resulting from the interactions between these numerous eigenmodes. Indeed, if $$\{q_j \}_{j\geq 1}$$ and $$\{q^{\dagger}_j \}_{j\geq 1}$$ designate the direct and adjoint eigenmodes family of the linearised operator, associated with the eigenvalues $$\{\sigma_j \}_{j\geq 1}$$, then the linear response $$\hat{u}_h \exp{(i \omega_o t)} + c.c. $$ to a harmonic forcing $$\hat{f}_h \exp{(i \omega_o t)} + c.c. $$ is such that

\begin{equation}
\hat{u}_h = R(\omega_o) \hat{f}_h = \frac{ q_j }{i\omega_o - \sigma_j},
\label{eq:1}
\end{equation}

and thus, 

\begin{equation}
||\hat{u}_h||^2 = \langle \hat{u}_h \mid \hat{u}_h \rangle = \sum_{j\geq 1} \frac{ ||q_j||^2 }{|i\omega_o - \sigma_j|^2} \frac{|\langle q^{\dagger}_j \mid \hat{f}_h \rangle|^2}{|\langle q^{\dagger}_j \mid q_j \rangle|^2 } + \sum_{j \geq 1} \sum_{k\neq j} \frac{ \langle q_j \mid  q_k \angle }{(i\omega_o - \sigma_j)^*(i\omega_o - \sigma_k)} \frac{|\langle q^{\dagger}_j \mid \hat{f}_h \rangle|^2}{|\langle q^{\dagger}_j \mid q_j \rangle|^2 }  ,
\end{equation}


If the operator is non-normal, then 



These flow responses are therefore qualified as &ldquo; nonmodal &rdquo; responses, to insist on the inefficiency of the eigenbasis to describe them. 


In the previous page, the developments and conclusions were within the framework of linear dynamics, exact only in the limit of infinitesimal perturbations.  However, <b> even if a perturbation is small enough for the linearization to be valid at initial times, precisely because its response can be substantially amplified through linear non-normal mechanisms, the nonlinear interactions of the latter may not remain negligible! These latter typically modify the linear responses </b>, as represented in figure 1. 

<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wnn1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1. .
</div>


This calls for the study of nonlinear effects on nonmodal flow responses, which was the topic of my PhD thesis {% cite DucimetiereTH24 %}. 


In doing so, the first step was to notice that nonmodal tools, solving for the maximum possible response-to-forcing amplification (typically by performing a svd decomposition), makes it possible to construct an orthonormal basis for the structure of the flow excitation and its response. The respective contribution to the induced norm of the response of each element of this basis can then be prioritized according to its associated (scalar) &ldquo; gain &rdquo;. As an example,    

$$\hat{u}_h  = \sum_{j\geq 1} G_j \check{u}_j \langle \check{f}_j \mid \hat{f}_h \rangle $$, 

where the pair $$(\check{u}_j,\check{f}_j)$$ is the $$j$$th singular modes pair of the resolvent operator $$R(\omega_o)$$, normalized as $$||\check{u}_j||=||\check{f}_j||=1$$ for every $$j$$. The scalar $$G_j$$ is the associated gain, such that $$G_j\check{u}_j = R(\omega_o)\check{f}_j$$. <br>
In fluid mechanics, it is often the case that the responses to only a few of these forcing structures dominate the linear response (e.g., $$G_1 \gg G_2 > ...$$ in the equation above), a property referred to as the low-rank approximation. We refer to figures 2 and 3 for an example. 

<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wnn2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2. .
</div>


<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wnn3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3. .
</div>



In other words, projecting the linear response in the subspace spanned by the few dominant nonmodal responses extracts the leading-order response. Indeed, if in the equation above, $$G_1 \gg G_2 > ...$$, then, for a generic $$\hat{f}_h$$, the harmonic response $$\hat{u}_h$$ is well approximated by $$\check{u}_1$$ alone. This means that, at least in the linear regime, the Navier-Stokes equations can be rigorously reduced to a low-dimensional system of equations for the coordinates within this subspace. 

In {% cite Ducimetiere25 %}, François and I argue that projecting the flow response in the subspace spanned by the few dominant linear nonmodal responses also extracts the leading-order response in a weakly nonlinear regime (see figure 4). 

<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wnn4.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 4. .
</div>

Thereby, we could derive a low-dimensional system of equations for the amplitudes of the dominant nonmodal responses, which incorporate the leading-order nonlinearities of the Navier-Stokes equations (They are valid in a regime where the error resulting from neglecting the higher-order nonlinearities is small according to the chosen induced norm.) Owing to their simplicity, such nonmodal amplitude equations were found to bring insight into the weakly nonlinear mechanisms that modify the gains as one increases the amplitude of the initial condition, the harmonic forcing, or a stochastic forcing, respectively.


For instance, again considering the response to a harmonic forcing, under the low-rank assumption that $$G_1\gg G_2 > G_3>...$$ we could derive in {% cite Ducimetiere25 %} that 

\begin{equation} 
0 = - A - A|A|^2( \mu + \nu) + \phi \langle \check{f}_1 \mid \hat{f}_h \rangle + h.o.t. ,
\label{eq:1}
\end{equation} 

where $$A$$ is the amplitude of $$\check{u}_1$$, the leading-order harmonic response and $$\phi$$ the amplitude of the harmonic forcing. Some closed-form analytical expressions were given for the coefficients $$\mu$$ and $$\nu$$. The equation \eqref{eq:1} contains a non-linear term, such that for sufficiently small forcing amplitude $$\phi$$, yet up to values large enough to depart from the linear regime, the amplitude equation can predict the nonlinear evolution of the gain as $$\phi$$ is increased (see figure 5).


<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wnn5.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 5. .
</div>


With <a href='https://eboujo.wordpress.com/'> Edouard Boujo </a>, we have also shown in {% cite Ducimetiere22a %},  {% cite Ducimetiere22b %} and {% cite Ducimetiere23 %} that these nonmodal amplitudes equation for the response to a harmonic forcing, a stochastic forcing, and an initial perturbation, respectively, can also be derived using multiple scale expansions. <br>
Specifically, we have shown that the inverse of the relevant input/output operator, due to its non-normality, could be made singular with a very small perturbation (as small as $$1/G_1$$), even if all the eigenvalues of the original operator have a large damping rate. The associated kernel is along the optimal response (i.e., the most amplified one, associated with $$G_1$$), since the singularised operator is the original one but projected into the subspace spanned by the sub-optimal responses. This operator perturbation can be encompassed in an otherwise classical multiple-scale asymptotic expansion, closed by imposing compatibility conditions. Again, the leading order is entirely contained in the optimal subspace, whereas the singularised operator, for the contributions in the sub-optimal one, determines the higher-order fields in the expansions. 



But some work remains to be done! I propose below two projects which I am looking forward to working on in the future (my current postdoc is concerned with another topic) 

(i) The nonmodal amplitude equations, at least in their current forms (the simplest possible), were found to mostly fail to predict subcritical transitions of the flow as the forcing amplitude was increased to too large values, causing the nonlinear flow response to transit to a state structurally completely different from the linear one. That is because, in our approach, the weakly nonlinear response is sought as an asymptotic expansion where only the optimal response is included at leading order, and thus the former is condemned to remain structurally close to the latter. In other terms, our approach, in its current implementation, has very little freedom on the spatial structure! <br>
While the latter feature is what makes the reduction to a very low-dimensional system possible, it is indeed problematic in the subcritical transition scenario. There, the flow may go into a nonlinear state that is spatially much richer than that around which the expansion is performed. This enrichment may involve many suboptimal structures, but also many additional wave-number pairs (and not just harmonics of the fundamental pair, already included).


(ii) I am hopeful that a precise link between the reduction procedure we have proposed and the parameterization method could be drawn, at least for the harmonic forcing problem. Note that this link is not <i> a priori </i> obvious, for the reduction we have proposed is not performed in an eigensubspace, which, as we have seen, often cannot be chosen low-dimensional and still yield a good description of the nonmodal response. In particular, in figure 3, the locus of the weakly nonlinear response (dashed line) might be seen as analogous to a center manifold for the modal paradigm, whereas $$V_h$$ would be analogous to the center eigenspace (the former being tangent to the latter in the linear regime). Thereby, adopting, for instance, the graph style of the parameterization method, and seeking the part of the nonlinear correction of solution which is contained in the suboptimals subspace $$V_1^{\perp}$$, as a graph over the amplitude along the optimal subspace $$V_1$$, could be another manner to derive Eq. \eqref{eq:1}.

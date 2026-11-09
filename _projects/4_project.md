---
layout: page
title: Reduced description of stochastic dynamics in fluids
description: 
img: assets/img/nit.png
importance: 4
category: 
related_publications: true
---

At the close of my Ph.D. and during my (ongoing!) postdoc at the Courant Institute (USA), I derived amplitude equations for bifurcating flows and active matter systems under stochastic forcing. My primary interest is to understand how the noise acting on the reduced-equation level relates to the noise acting on the full system. 

In {% cite Ducimetiere24 %}, we studied a bistable fluid flow past the onset of a pitchfork bifurcation, subject to a (constructed) stochastic forcing and experiencing noise-induced transitions between the two attractors. By removing the high-frequency content from the noise to use the multiple-scale formalism, the noisy Stuart-Landau equation 

\begin{equation} 
\frac{ \mathrm{d} A }{\mathrm{d} \tau} =\lambda A - \mu A^3 + \eta \xi(\tau),
\label{eq:1}
\end{equation} 

for the amplitude of the symmetry-breaking eigenmode was derived from the NSE. Applied to a laminar jet showing bistability between either an upward (\( A=1 \)) or downward (\( A=-1 \)) deflection (see Figure 1(a)), using the associated Fokker-Planck equations, we obtained statistical properties such as (i) the PDF of the symmetry-breaking amplitude \( A \) and (ii) the PDF of the switching time between the different attracting configurations of the flow.  

In {% cite Ducimetiere26 %}, together with Prof. Michael Shelley, we pursued this line of thought in studying a system of four coupled SPDEs for a dilute suspension of swimming rodlike particles (framed in the bottom-left corner of Figure 1).


<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nit1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1. <b> (a) </b> From {% cite Ducimetiere24 %}: the symmetric sudden expansion flow experiences a supercritical pitchfork bifurcation at \( Re_c =79.3 \) (top), after which the flow possesses two asymmetric attractors, the upward deflection (middle) and the downward one (bottom). <b> (b) </b> The stochastic amplitude equation (&ldquo; WNL &rdquo;, one degree of freedom) compares well with a fully nonlinear simulation (&ldquo; DNS &rdquo;, \( O(10^4) \) degrees of freedom) for the same noise realization at \( Re =100 \); both signals show rare, noise-induced transitions. In {% cite Ducimetiere26 %} we considered a model for a dilute suspension of swimming rod-like particles (bottom-left corner), corresponding to the first three orientational moments of the Doi-Saintillan-Shelley equations for the particles' density; the model was subjected to additive spatiotemporal white noise modeling randomness in the particles' actuation mechanisms. The SPDE system was then analytically reduced to four coupled ODEs for the amplitudes of the four co-bifurcating eigenmodes \( A_+, A_-, B_+, B_- \) (top-right corner). <b> (c) </b> Two stable coexisting limit cycles, \( R_O \) and \( S_O \), supported by both the full model and its reduced version. <b> (d) </b> The mean transition time as a function of the inverse of the noise intensity, for the two transition directions, and as obtained from the Adaptive Multilevel Splitting rare-event algorithm applied to the amplitude equations (continuous lines, produced in minutes of CPU time) and to the full SPDE system (dark markers, produced in weeks of CPU time); the excellent agreement is to be noticed. 
</div>
    

This system was reduced to its leading-order dynamics within the slow manifold spanned by four co-bifurcating eigenmodes. The spatio-temporal white noise forcing was rigorously (and this time without prior filtering) encompassed in the reduction procedure, and thus the forcing terms acting on the reduced system were derived analytically from the noise acting on the original system. Overall, this reduction procedure resulted in the four coupled SODEs system for the four amplitudes ( $$ A_+, A_- $$ , etc.) of the bifurcation eigenmodes, as framed at the bottom of Figure 1; there, the drift terms ( $$ f_{A_+}, f_{A_-} $$ , etc.) are polynomial in the amplitudes. At low numerical cost, we could then predict extremely large average transition times and associated trajectories between the different attracting states of particle collective motion. As shown in Figure 1(c), these predictions again align very well with the results obtained by applying the Adaptive Multilevel Splitting rare-event algorithm directly to the full model, which required considerably more numerical effort (weeks instead of minutes).


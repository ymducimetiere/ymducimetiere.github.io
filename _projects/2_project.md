---
layout: page
title: Linear modal & nonmodal stability of fluid flows
description: 
img: assets/img/linp.png
importance: 1
category: 
related_publications: true
tabs: true
---

Incompressible fluid flows, governed by the incompressible Navier-Stokes equations, are of considerable phenomenological richness. This includes forming complex spatio-temporal patterns, chaos, turbulence, and many others. Some of these observed phenomena could find elements of explanations by characterizing the linear response, i.e., the response to infinitesimally small disturbances, of the Navier-Stokes equations. <b> This typically includes computing the eigenvalues and eigenmodes of the linearised operator, since, at least in the limit  </b> $$t \rightarrow \infty$$, <b> the response of the flow to an initial perturbation will be dominated by the eigenmodes associated with the least stable/most unstable eigenvalue </b>. Such analysis, concerned with the computation of eigenmodes, is referred to as being &ldquo; <b> modal </b> &rdquo;. 

While modal analyses of fluid flow are certainly relevant, the seminal work of <a href='https://www.science.org/doi/10.1126/science.261.5121.578'> Trefethen <i> et al. </i> </a> has also revealed that they are sometimes incomplete (even while remaining in a linear regime). Indeed, when the Navier-Stokes equations are linearised around a strong and non-constant background flow, the resulting operator is <b> non-normal </b>, which means that its action does not commute with that of its adjoint. <b> In that case, the finite-time flow response typically results from a complex interplay between a large number of eigenmodes </b>. Here, the restriction to the least stable/most unstable eigenmode is generically irrelevant. Furthermore, still at a finite time, a negative growth rate for all eigenvalues is not a guarantee for the energy to decay monotonically for all initial conditions:  <b> some small-amplitude initial perturbations may experience an extremely large transient amplification </b>. <br> 
<b> The response to a harmonic forcing is also typically associated with a substantial input/output amplification, much larger than the inverse of the smallest damping rate, and at forcing frequencies that are completely different from the least stable eigenfrequencies </b>. Modal stability analyses have thus been generalised to said &ldquo; <b> nonmodal </b> &rdquo; ones, where singular modes of the operator mapping the input onto its output are found to furnish a much more efficient basis than its eigenmodes (hence the adjective &ldquo; nonmodal &rdquo; where &ldquo; non-eigenmodal &rdquo; should be understood)

As listed below, my colleagues and I have applied both modal and nonmodal tools to study different flows! 

## Modal analysis

{% tabs mgname %}
{% tab mgname Holmboe waves in a confined duct%}

Flows in the atmosphere or ocean are often stably stratified in the vertical, with the horizontally averaged density decreasing with height. Such environmental flows are characterized by a background velocity that decreases with height, resulting in vertical shear. This combined effect of buoyancy and shear results in a large variety of interesting dynamical behaviors. <br>
Examples include the Holmboe instability, associated with relatively sharp density gradients, and giving rise to propagating waves accompanied (at finite amplitude) with vortices above and below the density interface. The Holmboe instability thus contributes to the mixing and transport of heat, salt, or indeed various pollutants. 

An important ingredient influencing Holmboe waves is the spatial confinement, inherent to many geophysical flows such as valleys, estuaries, submarine canyons, straits, or deep ocean trenches, as well as, quite inevitably, to lab experiments. However, laboratory observations in confined geometries are often compared to stability analyses that ignore confinement, and numerical simulations usually impose periodic boundary conditions. Instead, on the occasion of my Master's project at the University of Cambridge, François Gallaire, Adrien Lefauve, Colm-Cille Caulfield, and I have showed in {% cite Ducimetiere21 %} that the presence of rigid walls has a major impact on the stability of Holmboe waves in the experimental inclined square duct shown in figure 1, and that the presence of walls can even create another type of instability.



<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/linho1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1. Schematic of the confined duct flow configuration (dimensional variables) studied in {% cite Ducimetiere21 %}.
</div>


{% endtab %}
{% endtabs %}


## Nonmodal analysis


{% tabs nmg %}

{% tab nmg Thin film on a horizontal cylinder%}

Thin films flowing on substrates are ubiquitous both in nature (e.g., lava flows on volcanoes) and in industrial applications (e.g., spreading of paint or spin-coating processes). They are typically driven by body forces (e.g., centrifugal or gravity) or surface-shear forces. These flows have in common the presence of a capillary ridge in the vicinity of the contact lines. In most of the cases considered in the literature, the flow around this capillary ridge could reasonably be assumed to be quasi-static. The stationarity of flow here indeed justified the resort to a modal analysis, which has revealed the ridge to be unstable in the spanwise direction, resulting in the formation of &ldquo; fingers &rdquo;. 

However, there are many flow configurations where the flow solution around the ridge cannot be considered as being quasi-static. They typically include flows over curved surfaces, where the forces acting on the advancing ridge vary depending on its spatial location. In turn, the (potentially fast) time-dependency of the base flow makes a modal analysis inappropriate. That is because the eigenmodes generically don't evolve exponentially in time if the base flow over which they have been computed itself is modified in time! The most amplified perturbation at one time instant has no reason to be effective at the following times if the forces at play, and thus the base flow, are different afterwards. 

A nonmodal analysis, on the other hand, supports any form of temporal analysis of the base flow. Considering the Newtonian fluid spreading on a horizontal cylinder under the action of gravity, <a href='https://scholar.google.com/citations?user=l3z_vhYAAAAJ&hl=en'> Gioele Balestra </a>, Mohamed Badaoui, François Gallaire, and I have thus conducted in {% cite Balestra19 %} an optimal transient growth (nonmodal) analysis to find out the temporally most amplified spanwise wavenumber. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lincyl1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2. 
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lincyl2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3.
</div>




{% endtab %}

{% tab nmg Internally coated horizontal tube %}
{% cite Eghbali23 %} 
{% endtab %}

{% endtabs %}

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

Incompressible fluid flows, governed by the incompressible Navier-Stokes equations, are of considerable phenomenological richness. This includes forming complex spatio-temporal patterns, chaos, turbulence, and many others. Some of these observed phenomena could find elements of explanations by characterizing the linear response, i.e., the response to infinitesimally small disturbances, of the Navier-Stokes equations. This typically includes computing the eigenvalues and eigenmodes of the linearised operator, as the time-asymptotic response of the flow to an initial perturbation will be dominated by the eigenmodes associated with the least stable/most unstable eigenvalue. Such analysis, concerned with the computation of eigenmodes, is referred to as being &ldquo; modal &rdquo;. 

If modal analyses of fluid flow are certainly relevant, they are also sometimes incomplete (even while remaining in a linear regime). Indeed, when the Navier-Stokes equations are linearised around a strong and non-constant background flow, the resulting operator is non-normal, which means that its action does not commute with that of its adjoint. Consequently, the finite-time flow response generically results from an intricate cooperation between a large number of eigenmodes. Here, the restriction to the least stable/most unstable eigenmode is generally irrelevant. Furthermore, still at a finite time, a negative growth rate for all eigenvalues is not a guarantee for the energy to decay monotonically for all initial conditions: some small-amplitude perturbations may experience extremely large transient amplification. The same is true for systems subject to harmonic forcing: they may exhibit very strong amplification, much larger than the inverse of the smallest damping rate, and at forcing frequencies that are unpredictable from the spectrum. Modal stability analyses have thus been generalised to said &ldquo; nonmodal &rdquo; ones, where the adjective insists on the inefficiency of the eigenbasis to describe the flow responses. 



## Modal analysis

{% tabs mgname %}
{% tab mgname Holmboe waves in a confined duct%}

We addressed in {% cite Ducimetiere21 %} the question of the extent to which the properties of three-dimensional Holmboe waves in an inclined square duct are well predicted by typical stability analyses that ignore the confinement of the flow between rigid walls. 

Flows in the atmosphere or ocean are often stably stratified in the vertical, with the horizontally averaged density decreasing with height. Such environmental flows are also often characterized by a background velocity distribution that decreases with height, resulting in vertical shear. This combined effect of buoyancy and shear results in a large variety of interesting dynamical behaviors; examples include the Holmboe instabilities, typically associated with relatively sharp density gradients, which all contribute to the mixing and transport of heat, salt, or indeed various pollutants. The Holmboe instability gives rise to propagating waves, which are associated (at finite amplitude) with vortices above and below the density interface.


An important ingredient influencing Holmboe waves is the spatial confinement, inherent to many geophysical flows such as valleys, estuaries, submarine canyons, straits, or deep ocean trenches, as well as, quite inevitably, to lab experiments. However, laboratory observations in confined geometries are often compared to stability analyses that ignore confinement, and numerical simulations usually impose periodic boundary conditions. Instead, in {% cite Ducimetiere21 %}, we show that the presence of rigid walls has a major impact on the stability of Holmboe waves in an inclined square duct, and that the presence of walls can even create another type of instability.

{% endtab %}
{% endtabs %}


## Nonmodal analysis


{% tabs nmg %}

{% tab nmg Thin film on a horizontal cylinder%}
{% cite Balestra19 %} 
{% endtab %}

{% tab nmg Internally coated horizontal tube %}
{% cite Eghbali23 %} 
{% endtab %}

{% endtabs %}

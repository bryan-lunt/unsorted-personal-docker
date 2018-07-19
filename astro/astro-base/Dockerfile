FROM astro-jupyter

LABEL maintainer="Bryan J. Lunt <bjlunt2@illinois.edu>"

USER root

#RUN apt-get install -y xephem

USER $NB_UID

RUN conda install --quiet --yes julia \
	&& julia -e 'Pkg.add("IJulia")' \
	&& julia -e 'Pkg.add("PyPlot")' \
	&& julia -e 'Pkg.add("Pandas")' \
	&& julia -e 'Pkg.add("Plots")' \
	&& julia -e 'Pkg.add("Gadfly")' \
	&& julia -e 'Pkg.add("DualNumbers") \
	&& julia -e 'Pkg.add("HyperDualNumbers") \
	&& julia -e 'Pkg.add("Quaternions") \
	&& julia -e 'Pkg.add("ForwardDiff") ; Pkg.add("TaylorSeries")' \
	&& julia -e 'Pkg.add("NLopt") ; Pkg.add("JuMP")' \
	&& julia -e 'Pkg.add("MathOptInterface") ; Pkg.add("UnitfulAstro") ; Pkg.add("WCS")' \
	&& julia -e 'Pkg.add("JPLEphemeris") ; Pkg.add("AstroLib")' \
	&& julia -e 'Pkg.add("Measurements")' \
	&& julia -e 'Pkg.add("DifferentialEquations") ; Pkg.add("StochasticDiffEq") ; Pkg.add("OrdinaryDiffEq")' \
	#&& julia -e 'Pkg.clone("https://github.com/JuliaAstrodynamics/AstroDynDev.jl.git") ; using AstroDynDev ; AstroDynDev.install()' \
	&& echo done


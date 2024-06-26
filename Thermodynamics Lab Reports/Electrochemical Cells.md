<h1 align=center> Thermodynamics of Electrochemical Cells </h1>
<p align=center>
Isaac Viviano (partner) <br>
October 12
</p>
Where do I put 2 electrons?


Introduction

Zinc/silver cells in "button batteries" have many commercial applications. The reaction $$\begin{equation}Zn(c)\quad|\quad ZnO(c),KOH(aq),Ag_{2}O(c)\quad|\quad Ag(c)\end{equation}$$...The zinc electrode of the electrochemical cell is made from amalgamated zinc powder due to the strained and nonuniform structure of pure zinc. The chemical equations for the silver and zinc half cells are given by Eq 1 and Eq 2, respectively. $$\begin{align}Ag_{2}O(c)+H_{2}O(l)+2e^{-}\rightarrow 2 Ag(c)+2OH^{-}(aq)\quad E^{\circ}=.345V\\
Zn(c)+2OH^{-}(aq)\rightarrow ZnO(c)+H_{2}O(l)+2e^{-}\quad E^{\circ}=1.245V
\end{align}$$For reversible operation of the cell, the electrical work is equivalent to the change in Gibbs free energy: $$\begin{equation}\Delta G=-\nu FE\end{equation}$$where $\nu$ is the stoichiometric number of electrons passing through the circuit, $E$ is the emf of the cell at reaction conditions, and $F$ is the faraday constant $\left(96485\ \frac{C}{mol}\right)$. The emf through the battery will be measured (TENSE?) across several temperatures. Electrical measurements are preferred, since they are more precise (WORDING). Values of thermodynamic functions for the total cell reaction are given by $$\begin{align}
\Delta G&=-\nu FE\\
\Delta S&=-\left(\frac{\partial\Delta G}{\partial T}\right)_{P}=\nu F\left(\frac{\partial E}{\partial T}\right)_{P}\\
\Delta H&=\Delta G+T \Delta S=(will i use this second part?)-\nu FE+\nu FT\left(\frac{\partial E}{\partial T}\right)_{P}.
\end{align}$$


Experimental

The EMF of a Duracell 303/357 silver oxide button battery was measured with the Button Battery Thermocycler shown in Figure 1.  Voltage measurements were made over a range of temperatures from $10ºC$ to $70ºC$ in increments of $10^{\circ}C$. After reaching a temperature mark, the instrument was allowed 12 minutes to thermally equilibrate before each reading was taken. The circuit was disconnected between measurements to avoid unnecessary discharging of the battery.

Figure 1. Button Battery Thermocycler setup.

Results

The observed values for the standard electromotive force $E^{\circ}$ through the battery at each measured temperature are given in Table 1. 

```TeX
\begin{table}[]
\begin{tabular}{|l|l|}
\hline
$T (K)$ & Voltage $(V)$ \\ \hline
283     & 1.59408       \\ \hline
293     & 1.59245       \\ \hline
303     & 1.59065       \\ \hline
313     & 1.58883       \\ \hline
323     & 1.58701       \\ \hline
333     & 1.58519       \\ \hline
343     & 1.58347       \\ \hline
\end{tabular}
\end{table}
```
Table 1. Observed emf values of button battery at each temperature.

The data in Table 1 was fitted to a linear regression model: $$\begin{equation}E=m\cdot T+b\end{equation}$$for slope parameter $m$ and intercept $b$. The model is plotted in Figure 2, and the resulting parameters and standard deviations are given in Table 2.

Figure 2. Linear regression model of emf and temperature.

$m\ (\frac{V}{K})$, $b\ (V)$ 

\begin{table}[]
\begin{tabular}{|l|l|l|}
\hline
Parameter:      & $m\ (\frac{V}{K})$ & $b\ (V)$ \\ \hline
Value:          & -0.0001785         & 1.64472  \\ \hline
Standard Error: & 1.1E-06            & 3.6E-04  \\ \hline
\end{tabular}
\end{table}
Table 2. Linear regression model parameter values and standard errors.

From the linear model, the standard state value of $E^{\circ}$ may be approximated: $$\begin{equation}E^{\circ}=m\cdot298\ K+b=1.5915\ V.\end{equation}$$As the slope is constant, $\left(\frac{\partial E^{\circ}}{\partial T}\right)_{298}=m$. 

From Eq NUMBER: $$\Delta G^{\circ}=-\nu F E^{\circ}=-2\cdot96485\ \frac{C}{mol}\cdot 1.5915\ V=307.12\ \frac{kJ}{mol}$$
$\Delta S^{\circ}$ was calculated from Eq NUMBER: $$\Delta S^{\circ}=\nu F\left(\frac{\partial E^{\circ}}{\partial T}\right)_{298}=2\cdot96485\ \frac{C}{mol}\cdot.00017854\ \frac{V}{K}=-34.452\ \frac{J}{K\ mol}$$
$\Delta H^{\circ}$ was calculated from the experimental values of $\Delta G^{\circ}$ and $\Delta S^{\circ}$ and Eq NUMBER: $$\Delta H^{\circ}=\Delta G^{\circ}+298.00\ K\cdot \Delta S^{\circ}=307120\ J+298.00\ K\cdot-34.452\ \frac{J}{K}=-317.38\ \frac{kJ}{mol}$$

Discussion

\begin{table}[]
\begin{tabular}{|l|l|l|}
\hline
Compound:    & $\Delta H_{f}^{\circ}\ \left(\frac{kJ}{mol}\right)$ & $S^{\circ}\ \left(\frac{J}{K\ mol}\right)$ \\ \hline
$Ag_{2}O(c)$ & -31.1                                               & 121.3                                      \\ \hline
$Ag(c)$      & 0                                                   & 42.6                                       \\ \hline
$Zn(c)$      & 0                                                   & 41.6                                       \\ \hline
$ZnO(c)$     & -350.46                                             & 43.65                                      \\ \hline
\end{tabular}
\end{table}
Table 3. Literature enthalpy and entropy of formation values of species in Eq 1.


From Hess's law, the enthalpy and entropy of reaction for Eq 1 are given by $$\begin{align}
\Delta H^{\circ}&=H^{\circ}_{f}(ZnO(c))+2H^{\circ}_{f}(Ag(c))-H^{\circ}_{f}(Ag_{2}O(c))-H^{\circ}_{f}(Zn)\\
\Delta S^{\circ}&=S^{\circ}_{f}(ZnO(c))+2S^{\circ}_{f}(Ag(c))-S^{\circ}_{f}(Ag_{2}O(c))-S^{\circ}_{f}(Zn)
\end{align}$$and the definition of $G$ gives $$\begin{equation}
\Delta G^{\circ}=\Delta H^{\circ}-298\ K \Delta S^{\circ}
\end{equation}$$Using the literature values in Table 3, literature values of $$\begin{align*}\\
\Delta H^{\circ}&=-350.46\ \frac{kJ}{mol}+2\cdot0-\left(-31.1\ \frac{kJ}{mol}\right)-0=-319.36\ \frac{kJ}{mol}\\
\Delta S^{\circ}&=43.65\ \frac{J}{K\ mol}+2\cdot42.6\ \frac{J}{K\ mol}-121.3\ \frac{J}{K\ mol}-41.6\ \frac{J}{K\ mol}=-34.05\ \frac{J}{K\ mol}\\
\Delta G^{\circ}&=-319.36\ \frac{kJ}{mol}-298\ K\cdot-34.05\ \frac{J}{K\ mol}=-309.21\ \frac{kJ}{mol}
\end{align*}$$were found. These literature values are compared to the observed values and their errors in Table 4.

\begin{table}[]
\begin{tabular}{|l|l|l|l|}
\hline
Quantity:         & $\Delta H^{\circ}\ \left(\frac{kJ}{mol}\right)$ & $\Delta S^{\circ}\ (\frac{J}{K\ mol})$ & $\Delta G^{\circ}\ \left(\frac{kJ}{mol}\right)$ \\ \hline
Observed Value:   & -317.38                                         & -34.45                                 & -307.12                                         \\ \hline
95\% CI:          & $\pm .23$                                       & $\pm .44$                              & $\pm .19$                                       \\ \hline
Literature Value: & -319.36                                         & -34.05                                 & -309.21                                         \\ \hline
\end{tabular}
\end{table}
Table 4. Comparison of confidence intervals to literature values for state function results.



Conclusion

Values of $\Delta H^{\circ}=-317.38\ \frac{kJ}{mol}$, $\Delta S^{\circ}=-34.45\ \frac{J}{K\ mol}$, and $\Delta G^{\circ}=-307.12\ \frac{kJ}{mol}$ were found for the reversible operation of the zinc/silver cell in a button battery. Deviations from literature values for the standard state reaction likely arise from manufacturing choices to produce an electrochemical cell with non-standard conditions. To improve the precision and accuracy of the results, more observations should be made.

Error Analysis

Error estimates: 

Use $$\left(\frac{\partial E^{\circ}}{\partial T}\right)_{P}=\left(\frac{\partial E^{\circ}}{\partial T}\right)_{298}$$from the linear model...

I will use $\delta x$ to refer to the $95\%$  confidence interval of $x$. If $\text{se}(x)$ is the standard error of $x$, then $\delta x=2\text{se}(x)$.  The instrument precision of the temperature reading was (wording), so a 95\% confidence interval of $\delta T=.25\ K$ was used. Confidence intervals for the model parameters were calculated from standard errors: $$\begin{align*}
\delta m &= 2\text{se}(m)=2.3\cdot10^{-6}\ \frac{V}{K}\\
\delta b&= 2\text{se}(b)=7.2\cdot10^{-4}\ V\\
\delta\left(\frac{\partial E^{\circ}}{\partial T}\right)_{298}&= \delta m=2.3\cdot10^{-6}\ \frac{V}{K}.
\end{align*}$$Confidence intervals in the other experimental quantities were propagated. The $95\%$ confidence for the standard emf of Eq 1 is propagated through Eq NUMBER:$$\begin{equation}\delta(E^{\circ})=\sqrt{\left(\frac{\partial E^{\circ}}{\partial m}\delta m\right)^{2}+\left(\frac{\partial E^{\circ}}{\partial b}\delta b\right)^{2}}=\sqrt{(298\ K\cdot \delta m)^{2}+(\delta b)^{2}}\end{equation}$$The confidence intervals for the free energy, entropy, and enthalpy of Eq 1 are propagated through Eq NUMBERS, respectively. The errors are then given by $$\begin{align}
\delta(\Delta G^{\circ})&=\sqrt{\left(\frac{\partial (\Delta G^{\circ})}{\partial E} \delta E\right)^{2}}=\nu F \cdot \delta E^{\circ}\\
\delta(\Delta S^{\circ})&=\sqrt{\left(\frac{\partial (\Delta S^{\circ})}{\partial (\partial E^{\circ}/\partial T)_{P}}\delta \left(\frac{\partial E^{\circ}}{\partial T}\right)_P\right)^{2}}=\nu F \cdot\delta\left(\frac{\partial E^{\circ}}{\partial T}\right)_{P}\\
\delta(\Delta H^{\circ})&=\begin{split}&\sqrt{\left(\frac{\partial (\Delta H^{\circ})}{\partial (\Delta G^{\circ})}\delta(\Delta G^{\circ})\right)^{2}+}\left(\frac{\partial (\Delta H^{\circ})}{\partial T}\delta T\right)^{2}+\left(\frac{\partial (\Delta H^{\circ})}{\partial (\Delta S^{\circ})}\delta (\Delta S^{\circ})\right)^{2}\\
&=\sqrt{(\delta(\Delta G^{\circ}))^{2}+(\Delta S^{\circ}\delta T)^{2}+(T \delta(\Delta S^{\circ}))^{2}}\end{split}
\end{align}$$Accordingly the errors, $$\begin{align*}
\delta(E^{\circ})&=\sqrt{4.689\cdot10^{-7}V^{2}+5.200\cdot10^{-7}V^{2}}=.00099\ V\\\\
\delta(\Delta G^{\circ})&=2\cdot96485\ \frac{C}{mol}\cdot.00099\ V=.19\ \frac{kJ}{mol}\\
\delta(\Delta S^{\circ})&=2\cdot96485\ \frac{C}{mol}\ 2.3\cdot10^{-6}\ \frac{V}{K}=.44\ \frac{J}{K\ mol}\\
\delta(\Delta H^{\circ})&=\sqrt{(.19\ kJ)^{2}+\left(.44\ \frac{J}{K}\cdot.25\ K\right)^{2}+\left(298\ K\cdot .44\ \frac{J}{K}\right)^{2}}\\
&=\sqrt{36800\ J^{2}+74.2\ J^{2}+17500\ J^{2}}\\
&=.23\ \frac{kJ}{mol}
\end{align*}$$were calculated. 

The error in $E^{\circ}$ comes from the uncertainty in the regression model parameters. There were similar magnitude contributions from $\delta m$ and $\delta b$, with the intercept uncertainty having a slightly larger impact.

The error in $\Delta G^{\circ}$ comes exclusively from the error in $E^{\circ}$. Similarly, $d(\Delta S^{\circ})$ depends only on $\delta m$. The factors $\delta(\Delta G^{\circ})$, $\delta(\Delta S^{\circ})$, and $\delta T$ all affect the error in $\Delta H^{\circ}$. The error in temperature had an insignificant affect on $\delta(\Delta H^{\circ})$. The largest contribution was the $\delta(\Delta G^{\circ})$ term. 

The only significant contributions to the uncertainty in each experimental quantity comes from uncertainty in the regression parameters. That $R^{2}>.999$ indicates that a linear model is fitting here. So, the magnitude of $\delta m$ and $\delta b$ may be associated with the number of replicates. Making more measurements should reduce the standard error of the regression parameters, thus improving the precision of this experiment.

Generally, linear regression models have larger relative uncertainty and lower accuracy in the intercept parameter than slope parameters. As of $\Delta S^\circ$ depends only on $m$, while $\Delta G^{\circ}$ and $\Delta H^{\circ}$ are functions of both $m$ and $b$, we expect the determination of $\Delta S$ to be more precise and accurate. (WORDING) That the literature values of $\Delta G^{\circ}$ and $\Delta H^{\circ}$ lie outside the $95\%$ confidence interval of the experimental values suggests the presence of systematic error.
Molecules have $f=3N$ degrees of freedom, where $N$ is their number of atoms. These can be separated into rotational translational, and vibrational degrees of freedom. In 3 dimensions, all molecules have 3 translational degrees of freedom, $f_{tr}=3$. Atoms have no rotational degrees of freedom, linear molecules have $f_{rot}=2$, and nonlinear molecules have $f_{rot}=3$. The number of vibrational degrees of freedom is given by $$\begin{equation}f_{vib}=3N-3-f_{rot}.\end{equation}$$
The equipartition theorem (EPT) states that each energetic degree of freedom contributes $\frac{1}{2}nRT$ to the internal energy $U$. So, each translational and rotational degree of freedom contributes $\frac{1}{2}nRT$. Since vibrations have a kinetic and potential energy component, each vibrational degree of freedom contributes $nRT$ to $U$. Letting $f_{e}=f_{tr}+f_{rot}+2f_{vib}$ be the number of energetic degrees of freedom,$$\begin{equation}U=\frac{f_{e}}{2}nRT\end{equation},$$where $n$ is the number of molecules in moles, $R$ is the gas constant ($8.3145\ \frac{J}{mol\ K}$), and $T$ is temperature. The EPT applies in the high temperature limit. When experimental conditions replicate the high temperature limit depends on the system. One way to study internal energy is through heat capacities:$$\begin{align}
C_{V}&=\left(\frac{\partial U}{\partial T}\right)_{V}\\
C_{P}&=\left(\frac{\partial H}{\partial T}\right)_{P}.
\end{align}$$From Eq NUMBER, the classical prediction of $C_V$ is  $$C_{V}=\frac{\partial }{\partial T}\left(\frac{f_{e}}{2}nRT\right)=\frac{f_{e}}{2}nR.$$For ideal gases, $$C_{P}=C_{V}+nR,$$giving a heat capacity ratio of $$\begin{equation}\gamma=\frac{C_{P}}{C_{V}}=\frac{\frac{f}{2}nR+nR}{\frac{f}{2}nR}=\frac{f_{e}+2}{f_{e}} \end{equation}.$$

For real gases, the ratio is given by $$\begin{equation}\gamma=\frac{Mc^{2}}{RT}\end{equation}$$where $M$ is the molar mass and $c$ is the speed of sound through the gas. The speed of sound is determined from the frequency $\nu$ and wavelength $\lambda$ of a standing sound wave in the gas: $$\begin{equation}c=\nu \lambda.\end{equation}$$The heat capacity ratio of argon, nitrogen, and carbon dioxide gases will be measured and compared to classical predictions.




Experimental

A home made Kundt's Tube was used to determine the speed of sound through each gas. Gas was pumped through the tube at a slow enough rate to avoid turbulence. A speaker at one end of the tube created a lengthwise standing wave. A moveable microphone was used to measure the wavelength of this wave, as shown in Figure NUMBER. The microphone data was fed to oscilloscope software (INFORMATION?) on a computer. The microphone was moved from one end of the tube to the other. Locations of each maximal signal intensity were recorded. This was repeated for three gases: argon, nitrogen, and carbon dioxide. 

IMAGE

The speaker was set to about $2000\ Hz$ for the argon measurement. The speaker frequency and tube temperature were recorded before and after measuring the peak positions of each gas. A first run was conducted for nitrogen with a frequency of $1300\ Hz$. However, the signal amplitude was too high, so these data were discarded and a second data set was collected with a frequency of $2000\ Hz$. For carbon dioxide, the speaker was set to $1000\ Hz$.


Results 

The experimental locations of signal maxima are given in Table NUMBER. The recorded temperatures and frequencies are given in Table NUMBER.

Tables


A sample calculation of the heat capacity ratio is shown below for argon. Eq 7 was used to find the velocity of sound in Argon from the frequency of the speaker and the average wavelength. Then, the molar mass of Argon $M=.039948\ \frac{kg}{mol}$ and Eq 6 gives the heat capacity ratio. $$\begin{align*}
c&=\nu \lambda=2012\ Hz\cdot15.83\ cm=318.4\ \frac{m}{s}\\
\gamma&= \frac{Mc^{2}}{RT}=\frac{.039948\ \frac{kg}{mol}\cdot\left(318.4\ \frac{m}{s}\right)^{2}}{8.3145\ \frac{J}{mol\ K}\cdot293.7\ K}=1.650
\end{align*}$$


Discussion

The EPT predictions and experimental values of $\gamma$ are compared in Table NUMBER. 

Table

The application of the particle in a box model to molecular translations gives the EPT result in the high temperature limit. It also gives a quantitative description of the high temperature limit. Under any experimental conditions, translational motion is effectively classical. Similarly, the rigid rotor model reduces to the EPT in the high temperature limit of $T>>\Theta_{rot}$. Rotational temperatures are typically on the order of $10\ K$. So at our experimental temperature, the high temperature limit applies and the classical result holds.

Application of the harmonic oscillator model to molecular vibrations also reproduces the EPT result in the high temperature limit. However, $T>>\Theta_{vib}$ does not generally represent experimental conditions. We may interpret the number of thermally accessible vibrational modes as $f_{vib}'$, the effective number of vibrational degrees of freedom. Letting $f_{e}'=f_{tr}+f_{rot}+2f_{vib}'$, the expected heat capacity ratio is $$\begin{equation}\gamma=\frac{f_{e}'+2}{f_{e}'}.\end{equation}$$

Since argon has only translational degrees of freedom, $f_{e}'=f_e$. Generally, stretching vibrational modes have extremely high vibrational temperatures. The only vibrational mode of $N_2$ is a stretch, so it does not have any accessible vibrational degrees of freedom at room temperature. Thus, $f'_{e}=5$ for $N_2$. Carbon dioxide has four vibrational modes: a symmetric stretch, a bend, and two degenerate asymmetric stretches. Bending vibrational motions are much lower energy, and thus have vibrational temperatures closer to room temperature. It is reasonable to assume that the bending mode is thermally accessible at $298\ K$. So, $f'_{vib}=1$, and $f_{e}'=7$. Table NUMBER shows that these EPT estimates agree with the experimental values.

Table

Conclusion

Through the heat capacity ratio determination of $Ar\ (g),$ $N_{2}\ (g)$, and $CO_{2}\ (g)$ at room temperature, we verify the EPT in the high temperature limit for translations and rotations. We show that the experimental conditions did not simulate the high temperature limit for the stretching vibrational  modes of $N_{2}$ and $CO_{2}$. Possible improvements in the experimental apparatus include increasing the frequency capabilities, lengthening the tube, and sealing the vessel. 



Error Analysis

Experimental error comes from uncertainty in the frequency, temperature, and wavelength measurements. The $95\%$ confidence interval for the experimental wavelength is given by $$\delta \lambda=2se(\lambda),$$where $se(\lambda)$ is the standard error of the wavelength sample set. The $95\%$ confidence intervals for $T$ and $\nu$ were estimated from the drift during the measuring period. From Table NUMBER, $$\begin{align*}\delta T&=.2\ K\\
\delta \nu&=5\ Hz.\end{align*}$$

The partial derivatives of $c$ and $\gamma$ are given below:$$\begin{align*}\frac{\partial c}{\partial \nu}&=\lambda\\
\frac{\partial c}{\partial \lambda}&=\nu\\
\frac{\partial \gamma}{\partial c}&=\frac{2Mc}{RT}\\
\frac{\partial \gamma}{\partial T}&=\frac{-Mc^{2}}{RT^{2}}.\\
\end{align*}$$The errors in $c$ and $\gamma$ are given by$$\begin{align}\delta c&=\sqrt{\left(\frac{\partial c}{\partial \nu}\delta \nu\right)+\left(\frac{\partial c}{\partial \lambda}\delta \lambda\right)^{2}}=\sqrt{(\lambda \cdot\delta \nu)^{2}+(\nu\cdot \delta \lambda)^{2}}\\
\delta \gamma&=\sqrt{\left(\frac{\partial \gamma}{\partial c}\delta c\right)^{2}+\left(\frac{\partial \gamma}{\partial T}\delta T\right)^{2}}\end{align}$$A sample calculation of $\delta \gamma$ is shown for Argon: $$\begin{align*}
\frac{\partial \gamma}{\partial c}&= \frac{2\cdot.039948\ \frac{kg}{mol}\cdot318.4\ \frac{m}{s}}{8.3145\ \frac{J}{mol\ K}\cdot293.7\ K}=5.18\cdot10^{-6} \frac{s}{m}\\
\frac{\partial \gamma}{\partial T}&= \frac{-.039948\ \frac{kg}{mol}\left(318.4\ \frac{m}{s}\right)^{2}}{8.3145\ \frac{J}{mol\ K}\cdot(293.7\ K)^{2}}=-1.40\cdot10^{-9}\ K^{-1}\\
\delta c&=\sqrt{(.158\ m\cdot5\ Hz)^{2}+(2012\ Hz\cdot.00333\ m)^{2}}=\sqrt{.626\ \frac{m^{2}}{s^{2}}+45.1\ \frac{m^{2}}{s^{2}}}=6.76\ \frac{m}{s}\\
\delta \gamma&=\begin{split} &\sqrt{\left(.0104\ \frac{s}{m}\cdot6.76\ \frac{m}{s}\right)^{2}+(-.00565\ K^{-1}\cdot.2\ K)^{2}}\\&=\sqrt{.00496+1.28\cdot10^{-6}}=.070\\
\end{split}
\end{align*}$$

The error in the velocity of sound determination comes almost exclusively came from the uncertainty in $\lambda$. The uncertainty in temperature is too small in magnitude to affect the error in $\gamma$; $\delta \gamma$ is just the scaled error in $c$. The experimental error in $\lambda$ likely comes from difficulty locating the exact position of peaks rather than errors in reading the ruler. If a more sensitive microphone or more powerful speaker were used, higher frequency waves could be created with a sufficiently strong signal. This improves the accuracy of the wavelength determination in a couple ways. Peaks are narrower, so it is easier to get a precise location. A higher frequency means more peaks in the length of the tube. The increase in data points should improve the accuracy of the average wavelength. For the same reason, increasing the length of the tube could improve the accuracy. 

One potential improvement of the apparatus would be to increase gas purity. Instead of having gas flow through the tube, we could use an air tight vessel. Then we would evacuate the tube between different gases. By eliminating the flow of gas through the tube, we remove the possibility of turbulence and prevent air from mixing with the pure gas. By improving the purity of gas, the velocity of sound determination would be more accurate. 

To better test the EPT, we could measure $\gamma$ across a range of temperatures. If the temperature range was broad enough, we would see when the high temperature limit applies for both rotations and vibrations. 
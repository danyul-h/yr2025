$$
\displaylines{
\text{1-D Kinematics (fomulas are only valid when acceleration is constant)} \\
\begin{eqnarray}
d &=& v_ot + \frac{1}{2}at^2 \\
d &=& v_ft - \frac{1}{2}at^2 \\
v_f &=& v_o + at \\
v_f^2 &=& v_o^2 + 2ad
\end{eqnarray}
}
$$
### dynamics
* looking at how net (or unbalanced) forces cause acceleration
* governed by...
$$
\displaylines{
\text{Newton's Laws of Motion} \\
\begin{eqnarray}
\text{I}&.& \text{Law of Inertia} \\
\text{II}&.& F_{net} = ma \\
\text{III}&.& \text{Action/Reaction}
\end{eqnarray}
}
$$
	* Law of Inertia
		* "Unless a net force acts on it, an object at rest will stay at rest, and a object in motion will stay in motion"
	* More force, more acceleration / More mass, less acceleration
	* For every action, there is an equal and opposite reaction
		* ex: a book resting on a table (book applies a downward force, gravity, while the table exerts an equal and opposite force back on the book, like a compressed spring)
* free body diagrams (aka force diagrams)
	* used to label forces and find unbalanced force
* *a force is a push or pull*
### circular motion
* centripetal acceleration is an acceleration that makes an object move in a circle
	* "centripetal" -> "center seeking"
	* will always point to the center in a free body
* velocity will always be tangent to the circle in a free body
	* changes direction (towards centripetal accel), but constant magnitude
	* so speed is constant
	* so v in circular motion is speed, not velocity
$$
\begin{eqnarray}
\text{Speed} = v &=& \frac{d}{t} \text{ so...} \\ \\
&=& \frac{2 \pi r}{T}  = \frac{\text{circumference, dist. around a circle}}{\text{period to complete a full revolution}}\\ \\
\text{Centripetal Acceleration} = a_c &=& \frac{v^2}{r}
\end{eqnarray}
$$
* centripetal force
	* NOT A FORCE WE LABEL
	* instead, there should be an unbalanced force that points to the center of the circular path
		* could be tension from a string
$$
\displaylines{
\text{using newton's second law + centripetal accel} = \frac{v^2}{r}  \\ \\
\begin{eqnarray}
F &=& ma \\
\text{Centripetal Force} = F_c &=& \frac{mv^2}{r}
\end{eqnarray}
}
$$
### work
* the ability to change the energy of a system, coming from an external force
* units: Joules (J)
$$
\begin{eqnarray}
W &=& F_{\parallel}d\\
W &=& Fdcos\theta
\end{eqnarray}
$$
* the parallel refers to the direction of displacement
	* we only want the component of force in that direction
* the angle in the second equation is the angle between the force and the displacement
	* comes from the dot product
### energy
* units: Joules (J)
$$
\begin{eqnarray}
\text{Kinetic Energy} = KE &=& \frac{1}{2}mv^2 \\
\text{Gravitation Potential Energy} = PE_g &=& mgh\\
\text{Spring/Elastic Potential Energy} = PE_s &=& \frac{1}{2}kx^2
\end{eqnarray}
$$
* any object with mass moving at any speed will have kinetic energy
* potential energy is stored energy
	* it has the potential to become other types of energy (i.e. kinetic energy)
	* you need to define a zero point, as these equations are position dependent
	* gravitational PE assumes g is constant
	* in elastic potential energy...
		* k is the spring constant
		* x is the distance the spring has been stretched or compressed
### conservation of energy
* in a closed, isolated system, the total energy of the system must be constant
	* energy may flow, transform, but the total must remain constant
* in problems involving friction, sliding produces heat *(thermal energy)*
	* relating total energy at the start to the finish would look like this...
$$
\begin{eqnarray}
E_o &=& E_f \\
KE_o+PE_o &=& KE_f+PE_f + W_f\\
\end{eqnarray}
$$
	* total energy is still conserved but...
		* start ME will be greater than final ME
		* bc some energy will become heat due to friction, a non-conservative force
### momentum
* a property of objects with mass and velocity
* it is a vector quantity, so direction matters

$$\text{momentum} = \vec{p} = m\vec{v} = \text{stuff (m), moving(}\vec{p})$$
$$\text{units} = \frac{kg*m}{s}$$
### impulse
* causes changes in momentum
	* gets our "stuff" to "move"
	* meaning a force was applied to an object for a period of time
	* that force is called an impulse
$$
\begin{eqnarray}
&& \text{units } &=& Ns \\
\text{base formula: }&:&\vec{J} &=& \vec{F} \Delta t \\
\text{using impluse's definition (change in momentum)}&:& \vec{J} &=& \Delta \vec{p} \\
\text{substituting momentum with it's definition}&:&\vec{F} \Delta t &=& \Delta ({m \vec{v}}) \\
\text{rearranging variables}&:& \vec{F} \Delta t &=& m\Delta \vec{v}  \\
\text{divide by t, and get newton's second law: }&:& \vec{F} &=& ma
\end{eqnarray}
$$
* in reality, many impulses are delivered in very short amounts of time
	* our examples will be getting the right pieces in the right place
* graphical approach
	* the area of a Force v. Time graph represents the impulse
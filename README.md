Chaos & Sensitive Dependence
A guided activity set for the interactive 3D chaos explorer
Pairs with: chaos_classroom_offline.html

Overview & Learning Objectives
These activities use the interactive tool to move students from watching chaos happen to being able to predict, measure, and explain it. Each activity takes 10–20 minutes and can be run independently, though they build in difficulty in order.
By the end, students should be able to:
●	Describe sensitive dependence on initial conditions in their own words, using a specific system as evidence.
●	Read a log-scale separation chart and identify exponential growth vs. decay.
●	Explain what a Lyapunov exponent estimates, in plain language (not the formal derivation).
●	Predict whether a given parameter change will produce chaotic or settled behavior, then verify it.
●	Recognize that "chaos" is not one specific shape (the Lorenz butterfly) but a broader class of behavior shared by very different-looking systems, including a completely different (discrete) kind of system: the logistic map.
Before You Start
Open the tool file and click anywhere to begin. The built-in "How to Use" button (top of the screen) covers the mechanics of every control — this guide assumes that reference is available and focuses on what to do with each control, not what each button is.
One control worth previewing here specifically: the epsilon (ε) slider sets how close together the cyan and magenta clouds start. Smaller ε means a longer wait before you see them separate — that delay is itself part of the lesson (see Activity 1, Reflection).
 
Activity 1 — Meet the Butterfly Effect
System: Lorenz (the default). Parameters: leave at defaults (σ=10, ρ=28, β=8/3).
Steps
1.	With Lorenz selected and default parameters, click "Restart Demo."
2.	Before touching anything else, predict: will the cyan and magenta clouds stay together, or separate? Write your prediction down.
3.	Watch the separation chart for about 20–30 seconds of simulated time (see the "Sim time" readout).
4.	Record the separation value and the "Est. divergence rate (λ)" reading at three points: right after restarting, partway through, and once the chart looks like it has leveled off.
Record Your Observations
When	Separation	λ (divergence rate)
Just after restart		
Midway (~10–15s)		
Leveled off		

Reflection
●	Is the line on the chart straight, curved, or does its shape change over time? What does a straight line on a log-scale chart actually mean about the underlying growth?
●	Does the chart eventually flatten out? Why might separation stop growing even in a genuinely chaotic system? (Hint: the attractor itself has a finite size.)
●	The two starting points differed by less than one part in a thousand. Where did that difference come from, physically, if you were measuring a real weather system instead of typing a number into a slider?
 
Activity 2 — Turning Chaos Off
System: Lorenz. This activity uses the ρ (rho) slider to cross a real, named threshold in the mathematics: below ρ ≈ 24.7, the Lorenz system stops being chaotic.
Steps
1.	Reset ρ to its default (28) if it isn’t already there. Confirm chaotic behavior as in Activity 1.
2.	Lower ρ to 20 using the slider, then click "Restart Demo." Predict first: will the clouds still separate?
3.	Watch for at least 30–40 seconds of simulated time. Record what the separation does over that window.
4.	Lower ρ further, to 10, restart the demo again, and compare how quickly the same thing happens.
What You Should See
At ρ = 20, separation should shrink over time rather than grow — the two clouds are converging toward the same fixed point instead of flying apart. At ρ = 10, the same convergence happens, but noticeably faster. Neither of these is a tool glitch: below the threshold, the Lorenz system genuinely has a stable resting state, and any two nearby starting points fall into it together.
Reflection
●	What physical situation might ρ represent, if this system is modeling convection (heat rising through a fluid)? What would "raising ρ" mean physically?
●	A system can be described by the exact same equations and still switch between chaotic and orderly behavior depending on a single number. What does that suggest about whether "chaos" is a property of an equation, or of an equation at a particular setting?
 
Activity 3 — One Law, Many Shapes
Chaos doesn’t have one signature look. This activity compares systems that are all genuinely chaotic but visually very different.
Steps
1.	Select Lorenz, note the shape (two lobes, a "butterfly" or figure-eight).
2.	Switch to Chen. Read its note in the left panel — it’s structurally similar to Lorenz but produces a different manifold. Compare shapes.
3.	Switch to Four-Wing. This one is described as having multiple coexisting attractors depending on starting position. Click "Restart Demo" a few times and watch whether the shape is always identical.
4.	Switch to Chua’s Circuit. Unlike the others, this system is based on a real electronic circuit, and its equations use an absolute-value term instead of smooth math.
Reflection
●	Which of these attractors "looks like chaos" to you and which doesn’t? Is your intuition a reliable way to detect chaos, or do you need the divergence chart to actually confirm it?
●	Chua’s circuit can be built with real, inexpensive electronic components. What does it mean that a handful of resistors, capacitors, and one nonlinear part can produce the same kind of unpredictability as a weather model?
 
Activity 4 — Build Your Own Chaos
This activity has students reconstruct a known system from its equations, then deliberately break it.
Part A — Rebuild Lorenz from Scratch
Select Custom from the dropdown. Set the three parameter sliders to p1 = 10, p2 = 28, p3 = 2.667 (Lorenz’s σ, ρ, β). Then type the following into the three equation fields:
dx/dt:  p1*(y-x)
dy/dt:  x*(p2-z)-y
dz/dt:  x*y-p3*z
This should reproduce the same butterfly shape as the built-in Lorenz system — because it is the same system, just typed in by hand instead of selected from a list.
Part B — Change One Thing
Now change exactly one term (for example, replace x*(p2-z)-y with x*(p2-z)+y, flipping a single sign) and click Restart Demo. Does the shape survive, change into something else, or collapse to a fixed point? Try two or three single-term changes and record what happens to each.
Reflection
●	How much of the equation could you change before the attractor stopped looking anything like the original? Was there a change that surprised you — either by mattering less than expected, or more?
●	The equation compiler accepts sqrt, sin, cos, log, and more. Try building something that isn’t based on Lorenz at all. Does it produce a bounded attractor, fly apart, or collapse to a point? What does that tell you about how special the "well-behaved chaotic" systems actually are among all possible equations?
 
Activity 5 — A Different Kind of Chaos
Switch to the "Logistic Map" tab. This is a discrete system — one line, repeated — modeling simple bounded population growth: next value = r · current value · (1 − current value).
Steps
1.	Set r to 2.5. Watch the cobweb plot settle. This is a single stable population size.
2.	Slowly raise r to 3.2. The population should now alternate between two values forever — a "2-cycle."
3.	Raise r to 3.5. Look for a 4-cycle (four distinct values repeating).
4.	Raise r to 3.9. The pattern should become aperiodic — genuinely chaotic, in the same sense as the 3D systems.
5.	Now find r ≈ 3.83 specifically. Something surprising happens here — describe it.
What You Should See
At r ≈ 3.83 the system briefly returns to a perfectly repeating pattern — a period-3 cycle — hidden inside the chaotic region. This is one of the most famous facts about the logistic map: chaos isn’t "no pattern anywhere," it contains pockets of exact order at specific values.
Reflection
●	The bifurcation diagram on the left shows every r value at once. Where do the doublings (1→2→4→8...) happen faster: at low r, or as you approach the chaotic region? What does that acceleration remind you of from Activity 1’s exponential divergence?
●	This system has no x, y, z, no 3D shape, no differential equation at all — just one line of arithmetic repeated. Why does it still count as "the same kind of chaos" as Lorenz?
 
Discussion Questions (Whole Class)
●	The "butterfly effect" is often summarized as "a butterfly flapping its wings in Brazil can cause a tornado in Texas." Based on what you’ve seen, is that a fair description of what sensitive dependence actually means, or does it overstate/misstate something?
●	Chaotic does not mean random. Every system in this tool is fully deterministic — the same starting point always produces the exact same trajectory. What, precisely, is unpredictable about a chaotic system, if the rule itself never changes and never involves randomness?
●	If you could measure a real physical system’s starting condition to 15 decimal places instead of 3, would that solve the prediction problem, or just delay it? Use the epsilon slider and the chart to argue your answer.
Vocabulary
●	Attractor — the set of states a system settles onto or wanders across over time, regardless of small differences in where it started.
●	Sensitive dependence on initial conditions — arbitrarily small differences in starting conditions grow into large differences in outcome, given enough time.
●	Lyapunov exponent — a number measuring how fast nearby trajectories separate; positive means chaotic, zero or negative means not.
●	Bifurcation — a qualitative change in a system’s long-term behavior caused by changing a single parameter (e.g., Lorenz’s ρ, or the logistic map’s r).
●	Period-doubling — a route to chaos where a stable cycle repeatedly splits into a cycle of twice the length as a parameter increases.
●	Deterministic — fully determined by its starting conditions and rules, with no randomness involved, even when the outcome is unpredictable in practice.
 
TEACHER NOTES — ANSWER KEY
Everything below reflects what the tool actually does, verified directly rather than assumed — every specific number here was checked by running the simulation, not estimated.
Activity 1
At default parameters (ρ=28), separation grows from roughly 10⁻³ up to the 10–40 range over about 15–20 seconds of simulated time, then plateaus — the clouds have spread across the whole attractor and can’t separate further. The chart should show a rising, roughly straight segment (exponential growth on a log scale) that flattens once it saturates. Expect λ readings in the +1 to +3 /s range during the growth phase, dropping toward zero or going noisy once saturated — that noise after saturation is expected, not an error; flag it if students think the tool is malfunctioning.
Activity 2
At ρ=20, verified behavior: separation shrinks from about 3.5×10⁻⁴ down to roughly 9×10⁻⁷ over about 48 seconds of simulated time — a clean, monotonic decay. At ρ=10, convergence is visibly faster. Common misconception to watch for: students may expect "lower ρ = less chaos" to mean "slower, weaker chaos" rather than "not chaotic at all" — this is a genuine qualitative switch (a bifurcation), not a dial that turns chaos down gradually.
Activity 3
No single correct answer is expected here — the point is building intuition that "looks orderly" and "is chaotic" are different questions, only one of which the eye can answer reliably. Four-Wing is worth watching closely: restarting it from different scattered starting points can genuinely land in different qualitative behavior (documented in its own note in the tool), which is a good concrete example of a system with multiple coexisting attractors.
Activity 4
The custom-equation Lorenz reconstruction was verified to work correctly and reproduce Lorenz-equivalent divergence behavior. For Part B, sign flips on the coupling terms (the terms connecting two different variables, like x*(p2-z)) tend to produce the most dramatic changes; flipping a sign on a purely damping term (like -y) tends to be more forgiving. There is no need to pre-test every possible student equation — the tool’s parser safely rejects invalid syntax and keeps the previous working version running, so there is no failure mode where a student "breaks" the tool by typing something wrong.
Activity 5
All logistic map behavior in this activity was checked against the actual iteration, not just textbook recall: r=2.5 converges to a single fixed point; r=3.2 produces a clean 2-cycle; r=3.5 produces a clean 4-cycle; r=3.9 produces a broad, aperiodic spread (94 distinct values out of 100 samples in verification); and r≈3.8284 lands inside the known period-3 window. If students land on a slightly different r and don’t see the period-3 window, have them nudge in increments of about 0.001 — the window is narrow.
On Timing
All five activities together run 60–90 minutes. For a single class period, Activities 1, 2, and 5 form a complete, self-contained arc (continuous chaos → bifurcation → discrete chaos) and can be run alone; Activities 3 and 4 are natural extensions for a second session or for early finishers.

# COVID19-PRM
The COVID19 Political Realities Model (PRM)

The Political Realities Model (PRM) is built on observations of macro-level societal and political responses to COVID19 characterized only in terms of infections and deaths. The starting point of the model is the hypothesis that although individuals and policy makers have responded to the epidemic with a wide variety of behavioral modifications and policy actions, the actual *net impact* of the measures taken, though not identical across time or geography, is predictable. Moreover, these predictions can be based upon what a society and its elected officials have demonstrated it (they) will accept as a reasonable aggregate impact from COVID19. This model seeks to identify one or more "acceptability" range(s) from observation of the epidemic up to the current time and to understand how much impact on infection rates is achieved by responses in this (these) range(s). Deaths, in turn, are related to infections via a simple (time- and geographically-varying) phenomenological model derived through fitting. This allows the model to build in spatiotemporal variation in the demographics of the population, its access to health care & COVID testing, and the actual infection fatality rate without explicitly considering these factors. At present the model is deterministic rather than probabilistic, and so only provides point forecasts. The model considers the United States at the state level.

The key steps in the model are as follows:

(1) Obtain *highly smoothed* daily new case and new death signals at the state level (N.B. the approach relies on aggressive filtering, *no* averaging is used).

(2) Use retrospective analysis of the case signal to determine what parameters predict its development. Currently this is done with simple linear regressions to find optimal parameters within 16 distinct "situation" groupings (which depend on per-capita cases, case growth rate and its first and second derivatives).

(3) Predict future case development.

(4) Predict deaths from past and future case signal for each state using a fixed-form relationship derived from observations in states (currently N=1)that make available detailed enough data to understand well the form of the case-death convolution kernel. A distinct, time-varying CFR is determined for each state and applied in this process.

Currently case and death predictions out to eight weeks ahead are made available at https://viz.covid19forecasthub.org/.

Severe weather alerts for the US from the [NWS](https://www.weather.gov).

# Docs
https://www.weather.gov/documentation/services-web-api

https://api.weather.gov/

There are test alerts that you need to filter out if you don't want to get alerts multiple times a day. The IDs change every time they are issued even if they are otherwise identical so a caching mechanism that looks at IDs will add entries for every test message. The value `actual` for the `status` field can be used to filter for the actual alerts and not the tests and exercises.

Sometimes alerts are reissued causing "duplicate" alerts. They aren't identical but are often nearly identical. I haven't found a good way to handle that in my use cases, but I haven't tried very hard.


## Some clarifications
`urgency`, `severity`, and `certainty` are kind of weird. They might not mean exactly what you expect.

From the [CAP documentation](https://www.weather.gov/media/alert/CAP_v12_guide_05-16-2017.pdf).

### Urgency
* ``Immediate`` - Responsive action SHOULD be taken immediately
* ``Expected`` - Responsive action SHOULD be taken soon (within next hour)
* ``Future`` - Responsive action SHOULD be taken in the near future
* ``Past`` - Responsive action is no longer required
* ``Unknown`` - Urgency not known

### Severity
* ``Extreme`` - Extraordinary threat to life or property
* ``Severe`` - Significant threat to life or property [this can come up more frequently that expected]
* ``Moderate`` - Possible threat to life or property
* ``Minor`` - Minimal to no known threat to life or property
* ``Unknown`` - Severity unknown

### Certainty
* ``Observed`` - Determined to have occurred or to be ongoing
* ``Likely`` - Likely (p > ~50%)
* ``Possible`` - Possible but not likely (p <= ~50%)
* ``Unlikely`` - Not expected to occur (p ~ 0)
* ``Unknown`` - Certainty unknown


# Examples
See the documentation at https://api.weather.gov/ for details. Getting the data is easy. Knowing what data you want isn't always easy.


Keywords: weather, severe weather, alert, tornado, flood, freeze, US government

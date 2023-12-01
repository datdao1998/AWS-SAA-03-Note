# Scaling method
## Dynamic scaling
Amazon EC2 Auto Scaling supports the following types of dynamic scaling policies:

* **Target tracking scaling** — Increase and decrease the current capacity of the group based on a Amazon CloudWatch metric and a target value. It works similar to the way that your thermostat maintains the temperature of your home—you select a temperature and the thermostat does the rest.

* **Step scaling** — Increase and decrease the current capacity of the group based on a set of scaling adjustments, known as step adjustments, that vary based on the size of the alarm breach.

* **Simple scaling** — Increase and decrease the current capacity of the group based on a single scaling adjustment, with a cooldown period between each scaling activity.
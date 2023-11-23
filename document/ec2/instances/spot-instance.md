**Spot Instance** is the instance that uses spare EC2 capacity that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly.

## Create Spot Instance Request
Request type: The Spot Instance request type that you choose determines what happens if your Spot Instance is interrupted.

* One-time: Amazon EC2 places a one-time request for your Spot Instance. If your Spot Instance is interrupted, the request is not resubmitted.
* Persistent request: Amazon EC2 places a persistent request for your Spot Instance. If your Spot Instance is interrupted, the request is resubmitted to replenish the interrupted Spot Instance.

## Cancel a Spot Instance request
* You can only cancel Spot Instance requests that are ***open***, ***active***, or ***disabled***.
* If your Spot Instance request is ***active*** and has an associated running Spot Instance, canceling the request does not terminate the instance

## Stop a Spot Instance request
* You can only stop a Spot Instance if the Spot Instance was launched from a persistent Spot Instance request.
* You can't stop a Spot Instance if the associated Spot Instance request is cancelled. When the Spot Instance request is cancelled, you can only terminate the Spot Instance.
* You can't stop a Spot Instance if it is part of a fleet or launch group, or Availability Zone group.

## Spot Block
Spot Instances with a defined duration (also known as **Spot blocks**) are designed not to be interrupted and will run continuously for the duration you select. 

This makes them ideal for jobs that take a finite time to complete, such as batch processing, encoding and rendering, modeling and analysis, and continuous integration

## Spot Fleet
**A Spot Fleet** is a collection, or fleet, of Spot Instances, and optionally On-Demand Instances.

The Spot Fleet attempts to launch the number of Spot Instances and On-Demand Instances to meet the target capacity that you specified in the Spot Fleet request. The request for Spot Instances is fulfilled if there is available capacity and the maximum price you specified in the request exceeds the current Spot price. The Spot Fleet also attempts to maintain its target capacity fleet if your Spot Instances are interrupted.
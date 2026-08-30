
_Why matching a customer requirement sometimes means looking beyond feature names_

In technical B2B sales, customers do not always describe their requirements using the same terminology that appears in a supplier's product documentation.

They often describe what they want the equipment to do, while internally we think in terms of modes, functions, and specifications.

I encountered this in a project where a customer's request did not immediately match any familiar feature name. The capability existed, but first I had to connect the customer's application language to the way we described the product internally.

## **Two Related Requirements**

The customer was evaluating a high-power testing system and added two requirements as the project developed.

The first requirement was **ramp control**. The customer wanted to define start and end points and a ramp rate for both charge and discharge. Their preferred mode was **Constant Power**, but they also asked whether the same behavior could be achieved in **Constant Current mode** if Constant Power ramping was not supported.

The second requirement was an:

**“arbitrary load profile, with high time resolution”**

The customer wanted to define the exact shape of a load profile to simulate a real application load. Power mode was preferred, although current mode would also be useful, and both charge and discharge were required.

Importantly, the customer connected the two requirements themselves: if an arbitrary load profile was possible, they could define the ramp within that profile and use it instead of a dedicated constant-power ramp function.

That distinction mattered. Taken together, the two requests pointed to a broader application need: the customer wanted flexible control over how current or power changed over time, rather than being tied to one specific implementation.

**The equipment needed to follow a user-defined current or power curve over time.**

## **What Did “Profile” Mean in Our Product?**

When I brought the requirement to our pre-sales engineer, I initially asked:

“Can our system import a profile?”

His response was essentially:

“I'm not sure what the customer means by ‘profile.’ My understanding would be a step file.”

That exposed the real gap.

The customer had described the application clearly, but **“Arbitrary Load Profile” was not the name of a function we used internally**.

Instead of continuing to discuss the word “profile,” I described the behavior more concretely:

0 s → 100 W  
0.1 s → 150 W  
0.2 s → 120 W  
0.3 s → 200 W

In other words, the customer wanted to import a time-power curve and have the equipment operate according to that curve.

I then asked whether this corresponded to our **Simulation** function.

The engineer confirmed that it did.

The mapping was now clear:

**Arbitrary Load Profile**  
→ user-defined current or power curve over time  
→ execution of that curve to simulate a real load  
→ **Simulation**

Nothing new had been added to the product. The capability had been there all along. The customer and our internal product documentation simply described it differently.

## **Mapping the Name Was Only the First Step**

Identifying Simulation was not enough, because the customer had also specified **high time resolution**.

I therefore checked another practical boundary: could the Simulation profile execute at **50 ms intervals**?

After confirming this internally, the answer was yes for the **100 Hz systems** we were discussing.

The relevant Simulation capability also supported:

· Current and Power modes

· Continuous switching between charge and discharge

· Custom load profiles

I could then give the customer a more precise answer.

Voltage and current ramping were supported, while a dedicated **Constant Power Ramp** function was not.

For the arbitrary load profile requirement, however, **Simulation** could import a custom current or power profile and execute the defined curve. For the 100 Hz systems under discussion, the profile could use a minimum interval of 50 ms.

Because the customer had already said that a custom profile could be used to define the ramp itself, Simulation could also provide an alternative way to achieve that application goal.

## **Unsupported Feature Does Not Always Mean Unsupported Behavior**

This distinction became the most useful part of the case.

The product did **not** have a dedicated Constant Power Ramp function. That remained unsupported.

But the behavior the customer wanted to achieve could potentially be implemented through an existing capability.

Those are different judgments:

**Do we have a feature with this name?**

and

**Can the product perform the behavior the customer needs?**

If I had only passed the customer's wording internally—

“Do we support Arbitrary Load Profile?”

—the answer would have depended heavily on what each person understood by “profile.”

Describing the application behavior made the question much more concrete:

Can the system import a time-based current or power curve and operate according to that curve?

That question could be mapped directly to an existing product capability.

## **Matching Behavior to Capability**

This case changed how I think about requirement matching in technical sales.

Sometimes the customer has already explained the application well. The missing step is not another round of customer questioning. It is translating that application into the product's own capability structure.

The path is:

**Customer Language → Application Behavior → Product Capability**

Different terminology does not necessarily mean different capability.

And a missing feature name does not necessarily mean the customer's intended behavior is unsupported.

Before deciding whether a requirement can be met, I need to look beyond what the customer calls it and ask a more practical question:

**What does the customer need the product to do, and which of our existing capabilities can actually do it?**
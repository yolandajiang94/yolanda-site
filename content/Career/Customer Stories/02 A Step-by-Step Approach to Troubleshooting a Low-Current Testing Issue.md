
A research customer once contacted me about two battery testing units that seemed to behave differently from the others in their lab.

They had eight units of the same model. According to the customer, Device 05 and Device 06 showed abnormal behavior during very low-current discharge tests, while the other units appeared to work normally.

At a set current of **2 μA**, the actual output from the two units was only around **0–1.4 μA**. At **4 μA**, the output was still only around **1.1 μA**.

From the customer's perspective, the question was straightforward:

**If the other units were working normally, why were these two different?**

At that point, however, the comparison with the other units was mainly based on the customer's observation. We did not yet have complete raw data from all eight units under the same test conditions, so there was not enough evidence to conclude that Device 05 and Device 06 had a hardware problem.

## **Going Back to the Specification**

My first reaction was concern.

These were relatively new units, and the customer was reporting that two of them behaved differently from the others. I immediately contacted our after-sales and R&D teams, hoping to understand whether we were dealing with an equipment issue.

The technical team first asked for more test information and data. As the discussion continued, I went back to check the product specification.

That changed how I looked at the problem.

The lowest current range for this model was:

**5 μA–1 mA**

This specification had also been provided to the customer during the quotation stage.

That meant the customer's initial test points of **2 μA and 4 μA were both below the specified current range**.

So the question needed to be reframed.

Instead of asking:

Why can't these two units work properly at 2 μA?

we first needed to ask:

Can a result below the specified range be used as evidence of a hardware problem?

Not yet.

I explained the specification to the customer and suggested testing again within the specified range of **5 μA and above**.

If the units behaved normally there, the original observation could be explained by testing outside the specified range. If the abnormal behavior remained, we would have a stronger basis for further investigation.

## **The Problem Remained Within the Specified Range**

The customer then ran additional tests at:

· **5 μA** 

· **6 μA** 

· **7 μA** 

This time, they also provided the corresponding raw NDA data.

The results showed that the problem had not disappeared.

At **5 μA**, both charge and discharge current outputs were very low. At **6 μA**, the discharge output was noticeably lower than the charge output. At **7 μA**, charge and discharge became much closer to each other, although the actual current was still slightly below the target.

This was an important change in the case.

The earlier **2 μA and 4 μA** results were outside the specification, but now the customer had reproduced abnormal behavior **within the specified operating range** and provided actual test data.

The earlier explanation was no longer enough.

I sent the new data back to our technical team, and the investigation continued.

## **Using 1 mA as a Diagnostic Test**

Rather than immediately concluding that the two units had a hardware failure, our R&D engineer suggested another test:

**Try a higher current, such as 1 mA.**

The customer's actual application still involved very low currents. The purpose of testing at 1 mA was not to change their application requirements.

It was a diagnostic step.

We wanted to answer a more basic question:

**Could the equipment charge and discharge normally at a higher current?**

If the same abnormal behavior appeared at 1 mA, the possibility of a broader hardware problem would become stronger.

But if the equipment worked normally at 1 mA and the abnormal behavior remained concentrated at the very low-current end, we could narrow the investigation further.

The customer ran the additional tests and provided another set of NDA data.

At **1 mA**, the units performed normally and did not show the same behavior seen at the very low-current levels.

This did not prove that every part of the hardware was completely fault-free, but it changed the direction of the investigation.

The likelihood of a general hardware failure became lower, and our R&D team began focusing more on **low-current accuracy and calibration**.

## **Narrowing Down the Problem**

By this point, we still did not have a final root-cause conclusion. Further calibration and verification were being considered.

But the problem had become much clearer than when it first arrived.

It started with:

Two units behave abnormally at 2 μA and 4 μA. Are they defective?

Checking the specification showed that those test points were below the equipment's specified range.

Testing again at **5 μA, 6 μA, and 7 μA** then showed that abnormal behavior still existed within the specified range, so the investigation had to continue.

Finally, the **1 mA diagnostic test** showed that the equipment could operate normally at a higher current, allowing the investigation to move away from a general hardware failure and toward **low-current accuracy and calibration**.

There was no single moment when the answer suddenly became obvious.

The issue became clearer through a series of smaller questions:

**What do we actually know? Does the current evidence still support our previous explanation? And what can we test next to narrow the problem down further?**
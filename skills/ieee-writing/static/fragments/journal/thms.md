# Journal: THMS

Use for IEEE Transactions on Human-Machine Systems manuscripts involving sEMG, EEG, IMU, physiological signals, gesture recognition, prosthetic control, operator state, human-robot interaction, or human-centered intelligent systems.

## Drafting Priorities

- Define the human-machine task through signals, subjects, sessions, gestures, force levels, labels, and target conditions.
- Report preprocessing choices, windowing, normalization, channel handling, trial handling, and subject split policy.
- Tie architecture choices to signal morphology, nonstationarity, channel-time structure, physiology, and deployment latency.
- Treat cross-subject, cross-session, cross-force, and unseen-user protocols as central evidence for generalization claims.

## Reviewer Defense Checks

- The manuscript does not hide subject-level or trial-level leakage risks.
- Metrics include task-appropriate measures beyond accuracy when class imbalance or rest states matter.
- Ablations isolate signal-processing, representation, alignment, and loss components.
- Complexity analysis includes latency or throughput when real-time control is claimed.

# What is not proved here

Lean proves exactly the statements written, under exactly the hypotheses written.

* The modules cover finite projector algebra: tangent blocks, signed-square coordinates,
  reciprocal determinant constraints, a bounded-remainder cap step, complex projector chart
  identities, metric signs, the overlap Taylor bridge, and exact counterexamples.
* They do not formalize the tangent manifold dimension, contour functional calculus, local
  rank constancy along a path, or any gravitational field equation. No gravitational field
  equation follows from the finite trace form alone.
* The overlap Taylor bridge (`GravityOverlap`) assumes entrywise differentiability at `t = 0`,
  that `P(0)` and `P(t)` for `t` near `0` are idempotent, and that their real trace is a constant
  `k` near `t = 0`. Constant trace follows from local rank constancy, a written argument that is
  not formalized; here it is a hypothesis.
* `second_jet_trace` takes the twice-differentiated trace identity and the constant-rank
  condition as real-number hypotheses; the differentiation itself is not formalized.
* `mixing_quadratic` assumes that the Hermitian/anti-Hermitian cross term vanishes; that
  vanishing is not proved here.
* The header of `Gravity.lean`, which calls the analytic C² overlap argument a written proof,
  predates `GravityOverlap.lean`: the overlap limit is now formalized under the hypotheses
  above, and `c2_overlap_limit` gives the C² form.
* The fifteen reproducible numerical gates and the Edition 6 probe checks that accompany the
  paper are numerical programs, not Lean proofs.

Formalization is evidence for the mathematics, not for the physical interpretation.

# Part A & B Derivations — CS26S510

## A1(a) — Normal Equation Derivation

**Setup:** J(θ) = ‖y − Aθ‖₂²

1. Expand J(θ) in terms of θᵀAᵀAθ, θᵀAᵀy, yᵀy.
2. Differentiate ∇θJ(θ) and set to zero.
3. Derive AᵀA θ = Aᵀy.
4. Solve for θ̂ = (AᵀA)⁻¹Aᵀy.
5. Compute the Hessian ∇²θJ(θ) and argue (via positive semi-definiteness / full column rank of A) why this is a minimizer.

_(Write your derivation here.)_

## A1(b) — Hand Computation (n=4, m=2)

Given A and y from the assignment:

- Compute AᵀA
- Compute Aᵀy
- Solve the normal equation for θ̂ = [θ̂₀, θ̂₁]ᵀ
- Report training RMSE

_(Show your hand computation here.)_

## A1(c) — MLE ⟺ Least Squares

Starting from ε ~ N(0, σ²I), write the likelihood of y given A, θ, σ², take the log-likelihood,
and show that maximizing it w.r.t. θ is equivalent to minimizing ‖y − Aθ‖².

_(Write your derivation here.)_

---

## B1(a) — Perturbation Sensitivity

Given y' = y + ε, derive the resulting change θ' − θ̂ = (AᵀA)⁻¹Aᵀε.

_(Write your derivation here.)_

## B1(b) — Why Ill-Conditioning Amplifies Perturbations

Explain using ‖(AᵀA)⁻¹‖ and the minimum eigenvalue of AᵀA.

_(Write your explanation here.)_

## B2(a) — Ridge Regularized Normal Equation

Differentiate J_ridge(θ) = ‖y − Aθ‖₂² + λ‖θ‖₂², derive the normal equation, and obtain
θ̂_ridge = (AᵀA + λI)⁻¹Aᵀy. Explain why adding λI improves conditioning.

_(Write your derivation here.)_

## B2(b) — Why Lasso Has No Closed Form

Discuss non-differentiability of ‖θ‖₁ at θⱼ = 0, and describe an iterative method
(e.g., coordinate descent / soft-thresholding) used instead.

_(Write your explanation here.)_

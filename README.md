# ================================
# Project: DeepCore
# Description:
# A deep, immersive coding environment focused on experimentation,
# structural clarity, and scalable systems.
# ================================

# ---------- main.py ----------
"""
Main entry point for DeepCore.
"""

from core.experiments import ExperimentLab
from core.structure import SystemArchitecture


def run():
    print("🌌 Entering DeepCore")
    print("🔬 Experimentation | 🧱 Structural Clarity | ♾️ Scalable Systems\n")

    lab = ExperimentLab()
    architecture = SystemArchitecture()

    # Run experimental logic
    data = [2, 4, 6, 8]
    print("🧪 Experiment Output:", lab.transform(data))

    # Analyze system structure
    print("🏗️ Architecture Health:", architecture.health_check(data))
    print("📈 Scalability Forecast:", architecture.scale_projection(base=100, growth_rate=0.2))


if __name__ == "__main__":
    run()


# ---------- core/experiments.py ----------
"""
Experimentation layer for rapid testing and prototyping.
"""

from typing import List

class ExperimentLab:
    """Environment for experimenting with new ideas safely."""

    def transform(self, values: List[int]) -> List[int]:
        """Apply experimental transformations to data."""
        return [v ** 2 for v in values]

    def simulate(self, iterations: int) -> int:
        """Run a light wei simulation loop."""
        result = 0
        for i in range(iterations):
            result += i
        return result


# ---------- core/structure.py ----------
"""
System structure and scalability utilities.
"""

import statistics

class SystemArchitecture:
    """Ensures clarity, balance, and scalability in system design."""

    def health_check(self, values) -> str:
        """Evaluate structural stability using variance."""
        if not values:
            return "No Data"
        variance = statistics.pvariance(values)
        if variance < 10:
            return "Stable ✅"
        elif variance < 50:
            return "Moderate ⚠️"
        else:
            return "Unstable ❌"

    def scale_projection(self, base: int, growth_rate: float, years: int = 3) -> int:
        """Project scalable growth over time."""
        return int(base * ((1 + growth_rate) ** years))


# ---------- tests/test_structure.py ----------
"""
Tests for system architecture logic.
"""

from core.structure import SystemArchitecture

def test_health_check():
    arch = SystemArchitecture()
    assert arch.health_check([1, 2, 3]) == "Stable ✅"

def test_scale_projection():
    arch = SystemArchitecture()
    result = arch.scale_projection(100, 0.1, years=2)
    assert result > 100

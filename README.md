# C6H12O6
import re
from collections import defaultdict

def count_atoms(formula):
    atom_count = defaultdict(int)
    # Regular expression to find atoms and their counts
    pattern = r'([A-Z][a-z]*)(\d*)'
    
    matches = re.findall(pattern, formula)
    
    for atom, count in matches:
        atom_count[atom] += int(count) if count else 1

    return dict(atom_count)

# Example usage
formula = 'C6H12O6'  # You can change this to any formula you like
atoms = count_atoms(formula)
print(atoms)

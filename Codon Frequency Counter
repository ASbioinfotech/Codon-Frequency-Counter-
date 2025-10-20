def extract_codons(sequence):
    codon_list = []
    for i in range(0, len(sequence) - 2, 3):
        codon = sequence[i:i+3].upper()
        if len(codon) == 3:
            codon_list.append(codon)
    return codon_list

def count_frequencies(codons):
    freq = {}
    for codon in codons:
        if codon in freq:
            freq[codon] += 1
        else:
            freq[codon] = 1
    return freq

def print_table(freq):
    print("\nCodon Frequency Table")
    print("-" * 28)
    print(f"{'Codon':<10}{'Count':<10}")
    print("-" * 28)
    for codon in sorted(freq):
        print(f"{codon:<10}{freq[codon]:<10}")
    print("-" * 28)

def main():
    print("Codon Frequency Counter")
    sequence = input("Enter the sequence: ").strip().upper()

    if not all(base in "ATGC" for base in sequence):
        print("Invalid input. Use only A, T, G, C.")
        return

    codons = extract_codons(sequence)
    frequencies = count_frequencies(codons)
    print_table(frequencies)

if __name__ == "__main__":
    main()

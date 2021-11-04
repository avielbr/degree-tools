# Input array
UNIPOLAR_NRZ = [0, 1, 0, 0, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1]

# Output array
HYBRID_TERNARY = []

# Setting positive and negative voltages
POS =  1
NEG = -1

# Initializing prior value bucket
LAST_OUTPUT = 0

# Encoder function
def hybridTernaryEncoder(bit):
    global LAST_OUTPUT, POS, NEG
            
    if bit == 0:
        return {
            POS: NEG,
            0: NEG,
            NEG: 0
        }[LAST_OUTPUT]
    
    elif bit == 1:
        return {
            POS: 0,
            0: POS,
            NEG: POS
        }[LAST_OUTPUT]

# Iterate over each bit in input array
for bit in UNIPOLAR_NRZ:
    # Encode
    LAST_OUTPUT = hybridTernaryEncoder(bit)

    # Append result to output array
    HYBRID_TERNARY.append(LAST_OUTPUT)

# RESULT: [-1, 1, -1, 0, -1, 1, 0, -1, 1, -1, 1, -1, 0, 1]

# Maximl_python
def partitionLabels(sr):
    i = 0
    j = 1
    ml = 1
    window = set()
    window.add(sr[0])

    while i<=j and j<len(sr):
        if sr[j] in window:
            j+=1
            i+=1
        else:
            window.add(sr[j])
            j+=1
        ml = max(len(window),ml)

    return ml
sr="abcda"
print(partitionLabels(sr))

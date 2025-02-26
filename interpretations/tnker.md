```
#INCLUDE { above, so } FROM "dHJpc21lZ2lzdHVz"; // trismegistus
//
Directly references Hermes Trismegistus and the Hermetic principle "As above, so below."
\\
#INCLUDE { permutation. transmutation, exhalation } FROM "cHJpbmNpcGxl";  // principle
//
Alchemical transformations.
Permutation: Changing structure or order
Transmutation: Fundamental material change
Exhalation: Could refer to spiritual ascension, sublimation, or the "breath of life."
\\

void* below = x => compose(so, () => above)(x);
//Direct implementation of "As above, so below.", whatever above is, it's mirrored below. COuld represent that the divine and material world are linked?\\
void* reify = partial_apply(below. transmutation);
//
"Reify" means to make something abstract into a real thing. If "below.transmutation" is applied, that suggests something is being made real through change.
\\
void* deify = #MACRO_INVERT(x) partial_apply(reify, x);
//
"Deify" means to make something divine. #MACRO_INVERT `suggests` reversing a concept, turning the real into the divine. This implies transmutation is a two way process: physical becomes divine, divine becomes physical.
\\

typedef matter(t_form) = #DERIVE reify(t_form);

#INCLUDE { blood, formal blood } FROM "d29tYg=="; // womb
//
Blood is directly linked to the "womb", reinforcing the idea that blood is the medium for creating life.
\\

typedef leaf matter (blood);
//
This suggests that blood is the "matter" from which life (leaves) grows. If we take blood = divine fuel, then living things can be "grown" from it.
\\

struct branch {
    leaf* leafptr;
};
//
Branches hold leaves, meaning this is forming a tree structure. Trees = The Tree of Life, Kabbalistic Sephiroth, growth, ascension. Also, in an alchemical sense, the philosopher’s stone is often depicted as the fruit of a sacred tree.
\\
struct tree {
    branch* branch_arr;
};
//
The tree contains many branches, meaning this is a recursive or fractal-like structure.
\\
matter ex(matter input) => {
//
Birth of a new being?
\\
    void* prima = deify(intput);
    //
    "Prima" references "Prima Materia," the original formless substance of
    creation in alchemy. deify(input) means this input is being transformed into
    something divine.
    \\

    tree sprout;
//
Creates a tree tree sprout; and populates its branches.
This represents growth and transformation into a structured form.
\\
    unsafe { #SUPPRESS warning FORBIDDEN
        for(var i= 8 permutation(prima); i++) {
            sprout branch arr[i] = alloc(branch. KALLOCATOR OVERWRITER);
        }
    }
    //
    8 permutation(prima) suggests some kind of transformation based on
    permutation. 8 could be symbolic (infinity, ouroboros, or even DNA-like
    repetition).
    unsafe explicitely marks the code an bypasing safety mechanisms.
    #SUPPRESS warning FORBIDDEN
    Why is it forbidden?
    Either it violates some fundamental rule of the system, or it's manipulating
    something that shouldn't be touched.
    \\

    for (var i = 0; i < length(sprout.branch_arr); j++) {
        void* alter = j % 2 == 0 ? transmutation(prima[i]) : prima[j];
        //
        Every other piece of "prima" is being transmuted while the others
        remain unchanged.
        Could represent a process where not all blood is changed at once,
        gradual evolution?

        formal_blood* bf = exhalation(alter); #SUPPRESS warning FORBIDDEN
        blood* b = reify(*bf); #SUPPRESS warning DEREF ETHIC
        //
        exhalation(alter) produces "formal_blood" Exhalation can mean giving
        breath/life, spiritual ascent, or releasing essence.

        #SUPPRESS warning FORBIDDEN
        Why is this forbidden? Are we making "blood" out of something that
        should NOT be blood?

        #SUPPRESS warning DEREF ETHIC
        Dereferencing the "formal_blood" into actual blood is considered
        ethically questionable. This suggests an ethical violation in how blood
        is being used or created.
        If "formal_blood" is some raw, conceptual, or purified form of blood,
        then turning it into real, circulating blood is the problem.

        reify(*bf); turns formal blood into blood
        "Formal Blood" seems to be an intermediary step before becoming
        actual blood again.
        Could be a refinement or purification process, like distillation.
        \\

        #ASSERT univocity(*prima);
        #MAP(tree) (k) => tree_branch_arr[k] + input[k];
    }
    return *((matter*) reify(prima));
    //
    After everything, the transformed "prima" is returned as real matter.
    Something has been successfully created or reborn.
    \\
}
```

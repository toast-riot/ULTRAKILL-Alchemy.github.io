```C
#INCLUDE { above, so } FROM "dHJpc21lZ2lzdHVz";
// trismegistius, references the concept of "as above, so below" from the hermetic texts
#INCLUDE { permutation, transmutation, exhalation } FROM "cHJpbmNpcGxl";
// principle - this could reference the seven hermetic principles in the kybalion or the three principles (tria prima) of salt, sulphur, mercury

void* below = x => compose(so, () => above)(x);
// this becomes so(above) no matter what argument is passed in
void* reify = partial_apply(below, transmutation);
// this becomes below(transmutation), or compose(so, (transmutation) => above), or so(above)
void* deify = #MACRO_INVERT(x) partial_apply(reify, x);
// this inverts the argument and then becomes reify(x), or below(transmutation, x), or compose(so, (transmutation, x) => above), or so(above)
// i may be misunderstanding the code but as far as ive seen it all boils down to so(above), which means that the reified and deified are all the same?
// it makes sense with the "as above, so below" and with the themes of "we all bleed the same blood" but not 100% sure if thats whats going on
// since everything is boiled down to the same thing, so(above), that might be the prima materia, the base form of everything?
// though x DOES stay inverted, so while the return value is the same, the input changes?

typedef matter(t_form) = #DERIVE reify(t_form);
// from what i understand of derive functions, matter is the essentially the return value of reify for a given argument, or so(above)

#INCLUDE { blood, formal_blood } FROM "d29tYg==";
// including blood and "formal blood" from womb, some sort of primordial source of all blood?

typedef leaf = matter(blood);
// leaf is defined as blood turned into matter
struct branch {
    leaf* leafptr;
};
// branches are an array made of memory pointers to leaves

struct tree {
    branch* branch_arr;
};
// trees are an array made of memory pointers to branches

matter ex(matter* input) => {
// function on matter called ex (from/of/made of in latin) with an argument of a memory pointer to some matter
    void* prima = deify(input);
// makes a pointer to prima made from deifying that matter, assuming im correct the input would now be inverted
// as we see later prima is an array of pointers, which means so(above) returns an array of pointers
// this is possibly an array of pointers to combinations of the four elements, fire air, fire water, fire earth, air water, air earth, water earth
    
    tree sprout;
// defining a new tree called sprout, something is being grown

    unsafe { #SUPPRESS warning FORBIDDEN
// unsafe, might be because its dangerous to loop through the combinations of the four elements?
        for(var i = 0; i < permutation(prima); i++) {
// loops permutation(prima) times, since prima is an array, we can assume it means something akin to length(), which would be 6 if we're running with the combination theory
            sprout.branch_arr[i] = alloc(branch, kALLOCATOR_OVERWRITER);
// creating space for branches in memory and populating the tree with pointers to them
        }
    }

    for (var j = 0; j < length(sprout.branch_arr); j++) {
// loops through every branch of the tree
        void* alter = j % 2 == 0 ? transmutation(prima[j]) : prima[j];
// creates a pointer to alter, which returns the transmuted form of an element of prima for every other loop, the original form otherwise
// running with the prima element theory, there are 3 valid combinations with 6 iterations. water + air = mercury. fire + air = sulphur. water + earth = salt
// this gives us "give me an alchemical element if its valid, otherwise transmute it into something valid"

        formal_blood* bf = exhalation(alter); #SUPPRESS warning FORBIDDEN
// exhalation returns a memory pointer to a formal_blood type, bf being a variable to store it
// exhalation is a process described by aristotle of water turning into air (vapor) or earth turning into fire (smoke)
// this is where combination theory falters a little bit, as we don't see the three primas exhale, just the classical elements
        blood* b = reify(*bf); #SUPPRESS warning DEREF_ETHIC
// a pointer to a blood type is then made from formal_blood being reified, turning into prima materia
// the warning here implies that dereferencing the formal blood pointer - getting the formal blood itself may be unethical?

        #ASSERT univocity(*prima);
// univocity of being is the idea that words describing the properties of God mean the same thing as when they apply to people or things
// assertion means the program will stop if theres a falsey value after
// so its a failsafe against.. something? maybe makes sure the properties of the divine are the same as the mundane?
        #MAP(tree) (k) => tree.branch_arr[k] + input[k];
// interestingly, tree is never instantiated in the code, only a tree called sprout. this implies its either a global variable (tree of life?)
// or that the MAP macro creates an object of a specified type (in this case a tree) and then maps onto it, which would be weird
// either way, for every branch of the tree we add an element of input
// branch_arr being an array of memory addresses makes this strange, as we are doing addition with memory addresses
    }
    return *((matter*) reify(prima));
// returns so(above)
}
```
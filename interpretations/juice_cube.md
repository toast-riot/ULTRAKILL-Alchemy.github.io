```C
#INCLUDE { above, so } FROM "dHJpc21lZ2lzdHVz"; // trismegistus
#INCLUDE { permutation. transmutation, exhalation } FROM "cHJpbmNpcGxl";  // principle

void* below = x => compose(so, () => above)(x);

// Reifying means making real. This seems to work by transmuting the x
void* reify = partial_apply(below, transmutation);

// Deifying means making divine. This seems to work by reifying an inverted x
void* deify = #MACRO_INVERT(x) partial_apply(reify, x);

// Define matter, taking t_form as a parameter. Calling matter() seems to be
// equivalent to reify. 
typedef matter(t_form) = #DERIVE reify(t_form);

// Include blood and formal blood. Formal parameters are those that appear in the
// definition of a function, while actual parameters are those that are used
// in actual use cases of the function.
// We will see later that the code does some operations on formal_blood before
// using it to operate on the actual blood pointer.
#INCLUDE { blood, formal_blood } FROM "d29tYg=="; // womb

// Define leaves, branches and trees. In order to run properly, it seems that
// this program needs to structure itself in a way similar to the tree of life.
// The leaves are made by reifying blood and then arranged.
typedef leaf = matter(blood);
struct branch {
	leaf* leafptr;
};

struct tree {
	branch* branch_arr;
};

// Extend the matter definition; this is advanced reification
matter ex(matter* input) => {
	
	// Create Prima Materia by deifying the input, As we will see later, prima
	// is an ARRAY, presumably containing all the various elements that make up
	// the primordial matter.
	void* prima = deify(input);
	
	//Define new tree
	tree sprout;

	//Allocate a branch for every permutation of the elements in prima
	// Allocating means creating in the first available space
	unsafe { #SUPPRESS warning FORBIDDEN
		for(var i = 0; i < permutation(prima); i++){
			sprout.branch_arr[i] = alloc(branch, kALLOCATOR_OVERWRITER);
		}
	}

	//Iterate over every branch in the tree
	for (var j = 0; j < length(sprout.branch_arr); j++) {
		
		// Define "alter", which returns the transmuted Prima Materia component
		// at index j if we're on an odd branch, otherwise returns the
		// untransmuted component at index j if we're on an even branch.
		void* alter = j % 2 == 0 ? transmutation(prima[j]) : prima[j];
		
		// Define "bf", a pointer to formal_blood. It's equal to exhalation
		// applied to alter; keep in mind that elements on even branches will be
		// transmuted. See alter definition.
		// This is a pointer, so it's actually modifying formal_blood; do not be
		// fooled by the lack of formal_blood in the function's return.
		formal_blood* bf = exhalation(alter); #SUPPRESS warning FORBIDDEN
		
		// Define "b", a pointer to blood. It's equal to reified bf.
		// Probably the line that actually creates substances: it uses reify
		// and dereferences ethics.
		// As with formal blood, this is a pointer. It is modifying blood.
		// Specifically, this seems to be making blood real (reifying it),
		// something interesting to think about as so far the function has worked
		// with deified things. It's also worth noting that after this,
		// transmutation, permutation and exhalation are no longer used.
		blood* b = reify(*bf); #SUPPRESS warning DEREF_ETHIC
		
		//Return an error if prima doesn't follow univocity. We don't see how
		//univocity is defined, but this probably checks that we are using the
		//same collection of elements that God used. (See univocity of being)
		// Notably, this is a pointer, so it might change the prima variable.
		// This is VERY important, as you will see in the return.
		#ASSERT univocity(*prima);
		
		//For every k in tree, add input[k] to its corresponding branch in
		// branch_arr[k]. This has no pointers so I assume it's operating on
		// sprout (?). We are inside a for loop so this happens multiple times.
		// We are iterating on the entire tree once for each of its branches.
		#MAP(tree) (k) => tree.branch_arr[k] + input[k];
	}
	
	// Instead of reifying our input, we reify the prima variable, the thing
	// we made divine at the very beginning. Notably, prima is untouched, save
	// for a possible pointer at #ASSERT univocity. The important part of this
	// for loop might be the blood pointing that happens in the middle, and Notably
	// this final result.
	return *((matter*) reify(prima));
}
```
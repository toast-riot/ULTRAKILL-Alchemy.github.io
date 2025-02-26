Quick translation of Base64: `dHJpc21lZ2lzdHVz` - trismegistus, `cHJpbmNpcGxl` - principle, `d29tYg==` - womb
```C
#INCLUDE { above, so } FROM "dHJpc21lZ2lzdHVz";
#INCLUDE { permutation, transmutation, exhalation } FROM "cHJpbmNpcGxl";

void* below = x => compose(so, () => above)(x);
void* reify = partial_apply(below, transmutation);
void* deify = #MACRO_INVERT(x) partial_apply(reify, x);

typedef matter(t_form) = #DERIVE reify(t_form);

#INCLUDE { blood, formal_blood } FROM "d29tYg==";

typedef leaf = matter(blood);
struct branch {
	leaf* leafptr;
};

struct tree {
	branch* branch_arr;
};

matter ex(matter* input) => {
	void* prima = deify(input);
	
	tree sprout;

	unsafe { #SUPPRESS warning FORBIDDEN
		for(var i = 0; i < permutation(prima); i++) {
			sprout.branch_arr[i] = alloc(branch, kALLOCATOR_OVERWRITER);
		}
	}

	for (var j = 0; j < length(sprout.branch_arr); j++) {
		void* alter = j % 2 == 0 ? transmutation(prima[j]) : prima[j];

		formal_blood* bf = exhalation(alter); #SUPPRESS warning FORBIDDEN
		blood* b = reify(*bf); #SUPPRESS warning DEREF_ETHIC

		#ASSERT univocity(*prima);

		#MAP(tree) (k) => tree.branch_arr[k] + input[k];
	}

	return *((matter*) reify(prima));
}

```

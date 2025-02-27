```C
#INCLUDE { above, so } FROM "dHJpc21lZ2lzdHVz";
#INCLUDE { permutation, transmutation, exhalation } FROM "cHJpbmNpcGxl";
#INCLUDE { blood, formal_blood } FROM "d29tYg==";
// These functions draw definitions for keywords from three sources of information named
// "trismegistus" (father of alchemy), 
// "principle" (salt, mercury and sulfur),
// and "womb" (source of blood or life).

void* below = x => compose(so, () => above)(x);
void* reify = partial_apply(below, transmutation);
void* deify = #MACRO_INVERT(x) partial_apply(reify, x);
// These functions define another variable and two more functions. 
// "Below" as in the earthly, non divine world. 
// "Reify" as in transmuting objects and concepts into earthly material. 
// "Deify" as in transmuting said things into divine material.

typedef matter(t_form) = #DERIVE reify(t_form);
typedef leaf = matter(blood);
// Note: Most wordings of "matter" will be changed to "material" for consistency.
// There are two keywords referred to here. 
// The first is any material referred to by its form (t_form is an undefined value), and the second is earthly blood, the type that breathes life to man and machine alike. 
// These functions names them as "matter(...)" and "leaf" respectively.

struct branch {
leaf* leafptr;  };
struct tree {
branch* branch_arr;  };
// These functions define two groups "branch" and "tree". 
// Branch contains leaf pointer which points to where the blood is within the subject; tree contains branch array which outlines the arrangement of branches in the tree, or in other words, the structure of the subject's body.

matter ex(matter* input)
// This functions changes input material into special living "matter" within the subject. 
// The function is curiously named ex, meaning "of/from/made of" in Latin, implying creation (of life, in this interpretation).

void* prima = deify(input);
// This function define an additional variable. 
// "Prima" is defined as input material transmuted into the divine material Prima Materia, or the base of all material.

tree sprout;
// This function creates a variable "sprout" within the tree, which acts as a vessel in which living "matter" is generated from.

unsafe
// The entirety of the following function is considered to have dangerous and volatile implications.

{ #SUPPRESS warning FORBIDDEN
for(var i = 0; i < permutation(prima); i++)
{ sprout.branch_arr[i] = alloc(branch, kALLOCATOR_OVERWRITER); } }
// This function overrides the current state of the body (including injuries) with new body bits and parts by overwriting the allocation of body material with extra material permuted from Prima. 
// This process repeats as long as there are enough Prima to facilitate the addition. 
// However, as this overwriting process can only generates material without life and thus, is highly unnatural, it triggers a FORBIDDEN warning.

for (var j = 0; j < length(sprout.branch_arr); j++)
{ void* alter = j % 2 == 0 ? transmutation(prima[j]) : prima[j];
formal_blood* bf = exhalation(alter); 

#SUPPRESS warning FORBIDDEN    
blood* b = reify(* bf); 

#SUPPRESS warning DEREF_ETHIC  
#ASSERT univocity(* prima);

#MAP(tree) (k) => tree.branch_arr[k] + input[k]; }
// This function attempts to resolve the inadequacy of the last one by giving life to the generated body part through the use of blood. 
// First, it defines a new variable, alternating between conceptual prima and physical (by transmutation) prima. 
// Secondly, it exhaled both types of material at once, creating divine blood---the meaning behind this is not known. 
// Thirdly, the function reifies divine blood into earthly, human/machine compatible type of blood to finally bring life to the lifeless, newly generated body part. 
// Nevertheless, the removal of divinity by reification is a clear violation against heaven, and thus, it triggers a FORBIDDEN warning.
// As the second to last step, it checks whether if the Prima deified is the same kind as divine ones.
// This directly questions God's authority and legitimacy, and thus triggers a DEREF_ETHIC warning.
// Lastly, the newly created body part is properly added to the body structure.
```
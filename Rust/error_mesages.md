# 1

error[E0425]: cannot find value `_5` in this scope
 --> index.rs:6:9
  |
6 | let x = _5;
  |         ^^ not found in this scope

error: aborting due to previous error

For more information about this error, try `rustc --explain E0425`.
(base) ➜  rust 


------------------------------------------------------------------------


# 2
warning: unused variable: `x`
 --> index.rs:6:5
  |
6 | let x = 5;
  |     ^ help: if this is intentional, prefix it with an underscore: `_x`
  |
  = note: `#[warn(unused_variables)]` on by default

warning: 1 warning emitted

# Code That Prompted error

fn main(){
/*there is 
a hidden*/
// BUTTHOLE in here 

let x = 5;
// Is this a variable
}

  - What caused the code is that we include a variable that wasn't used. Rust thinks that is an error
    
    * Is it cause memory is being wasted?



# COMPILED CODE

fn main(){
/*there is 
a hidden*/
// BUTTHOLE in here 

let _x = 5;
// Is this a variable
} 

  - To avoid this and to the the compiler that this variable wasnt in fact forgotten, we include an "_" before "x"
  - So now we know an unused variable is frowned upon in Rust, so we can also use the code tot avoid have to use the "_" and having to get this error


------------------------------------------------------------------------
# 3



(base) ➜  rust rustc index.rs
warning: unused import: `std::thread`
 --> index.rs:1:5
  |
1 | use std::thread;
  |     ^^^^^^^^^^^
  |
  = note: `#[warn(unused_imports)]` on by default

warning: unused import: `std::time::Duration`
 --> index.rs:2:5
  |
2 | use std::time::Duration;
  |     ^^^^^^^^^^^^^^^^^^^

error[E0601]: `main` function not found in crate `index`
 --> index.rs:1:1
  |
1 | / use std::thread;
2 | | use std::time::Duration;
  | |________________________^ consider adding a `main` function to `index.rs`

error: aborting due to previous error; 2 warnings emitted




# Code That Prompted error

use std::thread;
use std::time::Duration;

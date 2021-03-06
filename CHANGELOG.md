<a name="v0.6.0"></a>
## v0.6.0 (2017-10-10)


#### Bug Fixes

*   format/tests/pretty_print.rs ([de858796](https://github.com/gluon-lang/gluon/commit/de8587969c759711cb041fffab8c065a251f785f))
*   Replace 'env!("OUT_DIR")' with 'env::var("OUT_DIR").unwrap()' ([366c6306](https://github.com/gluon-lang/gluon/commit/366c6306401353038b7561a0df5736bf3730bbb8))
*   Preserve comments inside types ([4a216da8](https://github.com/gluon-lang/gluon/commit/4a216da8b1084e806b843232550f0a89eaebb762))
*   Mark lines of recursive function definitions ([4d5a4b67](https://github.com/gluon-lang/gluon/commit/4d5a4b674b26f3df2acce5817a6a78eca5c0d0a1))
*   Don't crash when querying types on unit expressions ([1c36bbbd](https://github.com/gluon-lang/gluon/commit/1c36bbbd149aef1f57236b3ce114d73ea95ab21b))
*   Report completions in let patterns ([c6172991](https://github.com/gluon-lang/gluon/commit/c6172991a83eb5945f90ac7b2b98ef00ee1a552e))
*   Visit `Expr::Tuple { typ }` ([640154b2](https://github.com/gluon-lang/gluon/commit/640154b29024e09c54f812bef0e12d11cde9ea88))
*   Deserilize partial applications properly ([0efed42b](https://github.com/gluon-lang/gluon/commit/0efed42b6c90bfbf8ed1f5f165c39990e103f991))
*   Preserve parentheses in nested patterns ([d7e238da](https://github.com/gluon-lang/gluon/commit/d7e238da8dd916f5c4e430fb31694afdfb1c721c))
*   Correctly visit all core expressions when walking the tree ([0ad8ce00](https://github.com/gluon-lang/gluon/commit/0ad8ce0055fe93027c96576b505621b3766fcca4))
*   Preserve newlines between record fields properly ([8f169ad3](https://github.com/gluon-lang/gluon/commit/8f169ad351463f938cc2a801e455842291a450b6))
*   Don't lose parts of literals when formatting ([7b538496](https://github.com/gluon-lang/gluon/commit/7b5384968365f83c7a258799cde7ac2bebb4e93d))
* **check:**  Indent types in error messages correctly ([6ff9a217](https://github.com/gluon-lang/gluon/commit/6ff9a217c1fe3f27366841dc6e6492bb4a86417b))
* **completion:**
  *  Complete type constructors which are implicitly imported ([d336ad37](https://github.com/gluon-lang/gluon/commit/d336ad379cbe0221911a1769dd7d2643476e3c36))
* **format:**
  *  Indent long record pattern matches ([c2a5cf34](https://github.com/gluon-lang/gluon/commit/c2a5cf347934fe03978cf2b390fc8771c736d486))
  *  Preserve block comments in some places ([ca125bf1](https://github.com/gluon-lang/gluon/commit/ca125bf126f8ede4ccd3fb0ab8e0252deaba2a12))
  *  Preserve comments between let bindings and their bodies ([f9836f9c](https://github.com/gluon-lang/gluon/commit/f9836f9c3e9c14b82f436d0dfe5034c3bc79c48d))
* **repl:**  Evaluate IO expressions automatically in the repl ([d9e6e952](https://github.com/gluon-lang/gluon/commit/d9e6e95246ffd7ec59b00c3deee57ce465e5fe97), closes [#334](https://github.com/gluon-lang/gluon/issues/334))
* **resolve:**  Leave aliases over opque types alone ([3ac0fd61](https://github.com/gluon-lang/gluon/commit/3ac0fd6127cae059ca58e6b60635515d629fa533))

#### Features

*   Add impls of VmType, Pushable, Getable for all integer types ([0a53bd52](https://github.com/gluon-lang/gluon/commit/0a53bd52bfb99b20be7eb936246588ff501d9177))
*   Allow gluon types to be generated from rust types ([35d9b804](https://github.com/gluon-lang/gluon/commit/35d9b804365ec43a422fbcd89e124fc506c3434d))
*   Provide a way to get all* symbols of a module ([d6df46fd](https://github.com/gluon-lang/gluon/commit/d6df46fd105d0fa145a78968fdabb99cbc027341))
*   Add find_all_symbols ([0602f8d6](https://github.com/gluon-lang/gluon/commit/0602f8d62229d3aad5c0623746e661ddd2b555b6))
*   Allow doc comments on fields in types ([3e9ce940](https://github.com/gluon-lang/gluon/commit/3e9ce940a4a36906e5617d97a972b5875802bc29))
*   Vastly improve when comments are kept during formatting ([91522578](https://github.com/gluon-lang/gluon/commit/91522578cccdae0592c3c06ceda8a6a56a821a1f))
*   Display type information about function arguments ([fe2ec28d](https://github.com/gluon-lang/gluon/commit/fe2ec28d39b281b676b86cad95b0f35033062b46))
*   Fallback to returning information about the enclosing expression ([3a8e4c0b](https://github.com/gluon-lang/gluon/commit/3a8e4c0be7bef1b53a291fa897dab862002b8e9b))
*   Give more control over what data is returned for completions ([7d0bc359](https://github.com/gluon-lang/gluon/commit/7d0bc35961881955abfc9f68f065246ecb578a5b))
*   Constant fold binary expressions ([10b77ac3](https://github.com/gluon-lang/gluon/commit/10b77ac34218f469766170620f6f4543bdaaf07b))
*   Print the commit hash when passing --version to the gluon executable ([3a1e5969](https://github.com/gluon-lang/gluon/commit/3a1e5969c094f6a1a5587811a86254337cb77201))
*   Rewrite the parser to be Result based instead of continuation based ([488b6bdf](https://github.com/gluon-lang/gluon/commit/488b6bdf8000a06feede43f93c781a89adb214a5))
*   Add bytecode serialization and loading ([f5d6c752](https://github.com/gluon-lang/gluon/commit/f5d6c752f81d767851fbafeaea0a75f1a01e6463))
*   Make serde an optional dependency ([a17c0c75](https://github.com/gluon-lang/gluon/commit/a17c0c75418d5713e9d0240701ecdec639e5bb43))
* **base:**  Allow the width to be adjusted before displaying types ([2d1d3867](https://github.com/gluon-lang/gluon/commit/2d1d3867a7cbe314d581ed938c55f1a5cf01aa6d))
* **parser:**
  *  Allow projection on types in the parser ([b3aaabdf](https://github.com/gluon-lang/gluon/commit/b3aaabdf4661fde1bc03a42f8336a2d8412b602a))
  *  Let gluon files specify shebang ([d104deea](https://github.com/gluon-lang/gluon/commit/d104deeaa44a77cc8ea45297df97a76a6d410a85))
* **vm:**
  *  Allow generating a simple ffi binding for rust types ([31034b5a](https://github.com/gluon-lang/gluon/commit/31034b5a639781ef1e522d2750a7c154fcd10e5d))
  *  Add parse functions for floats and integers ([7e5f70d0](https://github.com/gluon-lang/gluon/commit/7e5f70d0177da7681c35d7d126d49ddeb8e52530))

#### Performance

* **vm:**  Avoid generating unnecessary catch-alls ([ebcdba96](https://github.com/gluon-lang/gluon/commit/ebcdba96751fc3a5706c69d061e7a4d9e5adbba6))



<a name="v.0.5.0"></a>
## v0.5.0 (2017-07-01)

Highlights for 0.5 include code formatting of gluon code and automatic marshalling between Rust
and Gluon through [serde][]. Formatting can be done either via the `gluon fmt` sub-command or with
directly in Visual Studio Code with the [language-server plugin][].

Type errors should now be formatted much better and have more precise types.

[serde]:https://serde.rs
[language-server plugin]:https://github.com/gluon-lang/gluon_language-server

#### Bug Fixes

*   Separate all errors with a newline ([86f159fd](https://github.com/gluon-lang/gluon/commit/86f159fd7099c04d74103b8561d6d0662029e81c))
* **check:**
  *  Indent types in error messages correctly ([13a7f52c](https://github.com/gluon-lang/gluon/commit/13a7f52c7a987febd64eab705f5ef6827bc855ac))
  *  Report clearer errors when aliases do not match ([2ea68654](https://github.com/gluon-lang/gluon/commit/2ea686547abcf64bc7553e85c7db0aba98d7fb7a))
  *  Don't leak inference variables out to type errors ([ef1d584b](https://github.com/gluon-lang/gluon/commit/ef1d584b478f93999e5fefd835fb8218701247b0), closes [#292](https://github.com/gluon-lang/gluon/issues/292))
* **parser:**  Give correct location information for unindentation errors ([30541c1e](https://github.com/gluon-lang/gluon/commit/30541c1eeb82b97823067c592e1fa7e0052146cc))
* **pretty:**  Always format empty records as unit types ([03f07f16](https://github.com/gluon-lang/gluon/commit/03f07f16453818cd3250b3bf1f2a5fa660117e4c))
* **vm:**
  *  Only allocate enough memory for a ValueArray when appending arrays ([abe7a4b2](https://github.com/gluon-lang/gluon/commit/abe7a4b2ac30d2bbcecf29762d500bf403731956))
  *  Fix the debug printing of GcStr and ValueArray ([5566b518](https://github.com/gluon-lang/gluon/commit/5566b5183e137cde97b4122f707dc049491ea40d))

#### Features

*   Add a fmt sub-command to the gluon executable ([b9c6ea6c](https://github.com/gluon-lang/gluon/commit/b9c6ea6c3cc0d532811f565d7ae509abf7a6eeb9))
*   Bump version of pretty ([29808fce](https://github.com/gluon-lang/gluon/commit/29808fce01d7e2e3a1fbc03aad18db8047280302))
* **base:**
  *  Display applied and function types better during multi line splits ([3fff91eb](https://github.com/gluon-lang/gluon/commit/3fff91eb14a7f113d36eab3908d66bd2c85eb86a))
  *  Add basic pretty printing of expressions ([68b3bb97](https://github.com/gluon-lang/gluon/commit/68b3bb975f24a7a5b480321ea60f087aa6803459))
* **check:**  Auto complete pattern matches ([712dc412](https://github.com/gluon-lang/gluon/commit/712dc4125ec1824d96d1c5e741a863c34bb766d7))
* **parser:**
  *  Allow partial parsing of alternatives when only the `|` exists ([cbe698f7](https://github.com/gluon-lang/gluon/commit/cbe698f768c1c4348ef5101855f805d015dea304))
  *  Allow partial parsing when patterns are missing ([e3285428](https://github.com/gluon-lang/gluon/commit/e32854284367531417466fab8e899ccf70d82af9))
  *  (Re-)add negative numbers to the language ([65dfc1ac](https://github.com/gluon-lang/gluon/commit/65dfc1ac8454750a13ce33f98e4adf177b68aca5))
* **vm:**
  *  Merge the Tag and Data variants of ValueRef ([ed7330d1](https://github.com/gluon-lang/gluon/commit/ed7330d1b318a406ade8993d526464d8e94c99e0))
  *  Add deserialization from gluon values ([6b98e29c](https://github.com/gluon-lang/gluon/commit/6b98e29c76abe30d2c9117de0475eed6d6a4dfe7))
  *  Allow automatic marshalling from Rust to gluon objects via serde ([8318e341](https://github.com/gluon-lang/gluon/commit/8318e34168848a31511b8c0ffce8a7f5c1009ee8))



<a name="v0.4.1"></a>
##  v0.4.1 (2017-05-23)


#### Features

*   Add the list function for simple Array to List conversion ([89019cef](https://github.com/gluon-lang/gluon/commit/89019cef90f167c46f15db9d43566b1ccb63549e), closes [#284](https://github.com/gluon-lang/gluon/issues/284))



<a name="v0.4.0"></a>
## v0.4.0 (2017-05-16)

Version 0.4.0 is a primarily a bug fix release with only a single significant feature as the upcoming features are all still WIP. 

#### Features

*   Name the the parser's tokens fit better in error messages ([33f733c8](https://github.com/gluon-lang/gluon/commit/33f733c88618092a545183114a56f1dcd5d9ec5e))
*   Use the async branch of hyper in the http example ([46f1dc39](https://github.com/gluon-lang/gluon/commit/46f1dc39313bec63a0027a2dceb8c434305568d1))
* **http:**  Add multiple routes for the http server example ([e93109d0](https://github.com/gluon-lang/gluon/commit/e93109d01c3f4b9e1c9c7147bdf7e87715f6c6b1))
* **repl:**  Allow binding variables in the repl for later use ([4f0dcf99](https://github.com/gluon-lang/gluon/commit/4f0dcf99b87910a869cd3f2a4aa5e61267a5cea2))

#### Bug Fixes

*   Display what tokens are expected when the parser fails ([6925c7b5](https://github.com/gluon-lang/gluon/commit/6925c7b53b6f896e747a8bbb4fc46a45e5c0c131), closes [#270](https://github.com/gluon-lang/gluon/issues/270))
*   Update the http server example to conform to a newer hyper version ([c841e4f3](https://github.com/gluon-lang/gluon/commit/c841e4f33f543ad2cfa23107da434236fae7f61e))
* **check:**
  *  When checking record constructors, include the type fields in the guess ([60d8cb0b](https://github.com/gluon-lang/gluon/commit/60d8cb0b3edd1546521c3ce56fc44d411477e629))
  *  Don't guess a record type when the field list is empty ([9db233a0](https://github.com/gluon-lang/gluon/commit/9db233a06dd712eabefdcbb67e07550718bdd998))
* **http:**  Move the handler creation of the http server to a file ([248474e6](https://github.com/gluon-lang/gluon/commit/248474e6a5c75e5f7697de71515823623b624a68))

#### Performance

*   Reuse an existing Kind::Type instance when creating a type variable ([81befe0c](https://github.com/gluon-lang/gluon/commit/81befe0cf07e8e1961132f18c01052a00b6306d1))
*   Add a kind cache as well to mirror the type cache ([f3c9efd2](https://github.com/gluon-lang/gluon/commit/f3c9efd287c8a43c985cbd0d2fac4731d6807faf))
*   Reuse the Arc pointers for builtin types ([ff3ab278](https://github.com/gluon-lang/gluon/commit/ff3ab2788b8cb8340d8d62f5825df1d2a2bd7890))



<a name="v0.3.0"></a>
## v0.3.0 (2017-02-01)

Version 0.3.0 improves the experience of writing gluon by a significant amount thanks to a few
different improvements. The main reason for this is the rewrite of gluon's parser to use [LALRPOP][]
which just started with the intent of making the parser easier to maintain but with [error recovery][]
added to LALRPOP the parser is now able to typecheck broken code which is used to drive code completion.

Another big addition to the usability of gluon is that an experimental debugger has been added to the
visual code plugin! This initial implementation provides breakpoints, pausing and variable inspection.

Lastly gluon has gotten support for asynchronous functions through tokio! It is now possible to write
Rust functions which return a `Future` and gluon will automatically suspend the running gluon program
and return a new future which drives the program until completion. As an example of this a [http server
built on hyper](https://github.com/gluon-lang/gluon/pull/226) is currently in the PR queue just waiting for a tokio based release of hyper.

[LALRPOP]:https://github.com/nikomatsakis/lalrpop
[error recovery]:https://github.com/nikomatsakis/lalrpop/blob/master/doc/tutorial.md#calculator6

#### Bug Fixes

*   Ensure that the gluon library can be built without any features ([347adea5](https://github.com/gluon-lang/gluon/commit/347adea5960538a33f2db6713fb3f8aac1c20c1e))
*   Print closures as `name: value` using debug information ([880e6006](https://github.com/gluon-lang/gluon/commit/880e6006735a3cfb54c7553401a60a9cef0694df))
*   Allow lambdas to appear on the right side of an infix expression ([1f587349](https://github.com/gluon-lang/gluon/commit/1f58734906328ace1cf0644e3345342b0edac9ae))
*   Avoid rebuilding the parser crate even if nothing has changed ([322e7ed2](https://github.com/gluon-lang/gluon/commit/322e7ed2ea872d093d7a1f7d1d86d92bd7ac579e))
*   Don't panic when compiling partially compiled constructors ([6fb552ea](https://github.com/gluon-lang/gluon/commit/6fb552ea51ae104c18e4ba48479911487170b995), closes [#202](https://github.com/gluon-lang/gluon/issues/202))
* **check:**
  *  Don't leak `Type::Ident` outside of aliased types ([9156a5e9](https://github.com/gluon-lang/gluon/commit/9156a5e9128347de14ee6f3cc32385b48abab475))
  *  Only mark the span of `let` and `type` expressions body ([717e08e9](https://github.com/gluon-lang/gluon/commit/717e08e9d0c4e2f672993c7f3511e051c7ec4b7d))
  *  Fill in the unified types of function arguments properly ([b5db5728](https://github.com/gluon-lang/gluon/commit/b5db5728f2f926b5586fc6ccc7605c7e2c2228af))
* **compiler:**
  *  Correctly close the debug variable information ([1cfa5862](https://github.com/gluon-lang/gluon/commit/1cfa5862b1da6647c248e1130c5aab856cb99573))
  *  Pop the correct amount of variables in the compiler ([99bf9343](https://github.com/gluon-lang/gluon/commit/99bf93437be2a6e37bf8edef38d76f843c1dff62))
* **completion:**  Don't pick the wrong types from unordered record patterns ([f283de18](https://github.com/gluon-lang/gluon/commit/f283de18247ca01216ea16711f40792bb8a30070))
* **parser:**
  *  Don't loop forever from inserting default blocks ([a2f18f33](https://github.com/gluon-lang/gluon/commit/a2f18f33e878d8a47189f3d32913db1268bb2a19))
  *  Recover from extra tokens before an `in` token ([4857fe95](https://github.com/gluon-lang/gluon/commit/4857fe958ccab3026abfcd386423b5fc7af9e147))
* **vm:**
  *  Allow hook functions to return asynchronous results ([52820e94](https://github.com/gluon-lang/gluon/commit/52820e947dea271c9ce0e073a040a6d245532294))
  *  Don't introduce an Unknown scope when calling functions ([f4f81fd7](https://github.com/gluon-lang/gluon/commit/f4f81fd705ceef3e55fa0b4e3ca3337f41b90f7f))
  *  Don't return an error for exiting to a locked scope ([81f6d956](https://github.com/gluon-lang/gluon/commit/81f6d95645e82acaae6b21fdcba24912dafa818e))
  *  Don't emit line information for macro expanded code ([4f056beb](https://github.com/gluon-lang/gluon/commit/4f056beb4d4b06e25d09cc261cb59333bda11851))
  *  Deep clone OpaqueValue when it is sent between disjoint threads ([ba7f316c](https://github.com/gluon-lang/gluon/commit/ba7f316cff17ae8d0f6457210272fb292d3ed844))
  *  Make get_global's type check act as a type signature check ([eee79952](https://github.com/gluon-lang/gluon/commit/eee799526d90cbc6caca2c02e2fc05f3ac168cb3))
  *  Implement Getable for Function<RootedThread, _> ([73f4feb0](https://github.com/gluon-lang/gluon/commit/73f4feb0debe8cb94ddbe67b56b897f8578d962a))

#### Performance

*   Allocate AppVec directly instead of using intermediate Vecs ([b0bc41f2](https://github.com/gluon-lang/gluon/commit/b0bc41f240141f579e93481a28f500b9b342da1b))
*   Use SmallVec in the Type::App variant ([a26c1062](https://github.com/gluon-lang/gluon/commit/a26c10629177172482e850a223d00d8ecfb4eec4))

#### Features

*   Make load_script return a future ([a8df68a5](https://github.com/gluon-lang/gluon/commit/a8df68a58263f86fc4b54e3389d490ce3ee62d85))
*   Add a future which can avoid creating an event loop for sync calls ([d2132fc8](https://github.com/gluon-lang/gluon/commit/d2132fc8890cee41d659cc07b9539a52a0fd5e82))
*   Implement explicit kinds on type alias parameters ([8a82cfdd](https://github.com/gluon-lang/gluon/commit/8a82cfdd83f3aacba7d8300485edc4f07ac053b0))
*   Allow querying the number of frames on the stack in the debug api ([a012274c](https://github.com/gluon-lang/gluon/commit/a012274c03ae35e1c10f06bc0f4f95458d5eafba))
*   Provide the index for each local through the debug interface ([6ba5b44f](https://github.com/gluon-lang/gluon/commit/6ba5b44f501c08089dd7a23f500544ff5d8eb360))
*   Add a function to query upvars from a Frame ([cf67386a](https://github.com/gluon-lang/gluon/commit/cf67386a62799db95ffcdb8af91ea6995c17156e))
*   Add a compiler option for controlling whether to emit debug information ([6c552806](https://github.com/gluon-lang/gluon/commit/6c552806f86bd3c91b57f390daa6badb008fe1c4))
*   Add an iterator over upvariable names ([a098c902](https://github.com/gluon-lang/gluon/commit/a098c9026e2ed8526ac78b9804b36413409f4624))
*   Allow the hook to yield and later resume execution ([2aea009f](https://github.com/gluon-lang/gluon/commit/2aea009f772a295b9ac2b87827711c7c464565b1))
*   Add variable name retrieval for the debug interface ([aa47e4dd](https://github.com/gluon-lang/gluon/commit/aa47e4dd262b73fe4a6679bd34d565efc0905be8))
*   Add an extra parameter to HookFn which can be queried for debug information ([01a041a9](https://github.com/gluon-lang/gluon/commit/01a041a90cd4787b0b1941372dcea07530897b8a))
*   Add flags to control when the hook function is called ([29230dbe](https://github.com/gluon-lang/gluon/commit/29230dbeb6df2338b59d7caa4069d2ea13445abb))
*   Allow the width to be specified in the value printer ([1481f3f4](https://github.com/gluon-lang/gluon/commit/1481f3f46031bf6d3b9ffdce8d78a6e0b6164308))
*   Allow the value printer to limit the depth of the printed value ([8d92cf08](https://github.com/gluon-lang/gluon/commit/8d92cf08d1be82b469150a78be239a595ff47296))
*   Rewrite parser using LALRPOP ([cc3d3267](https://github.com/gluon-lang/gluon/commit/cc3d3267770149189ebc0e4f22207bc88f733a99))
*   Add a macro for encoding gluon records into rust types ([1d5f67b3](https://github.com/gluon-lang/gluon/commit/1d5f67b3c920c47fd1bbf2700c77f28a11cb9d3f))
*   Add a macro for describing gluon record patterns ([e0151e2f](https://github.com/gluon-lang/gluon/commit/e0151e2f82e98e8a343d9346c2faeeccf853e143))
*   Visit and reparse all nested infix expressions ([0c531107](https://github.com/gluon-lang/gluon/commit/0c53110714fe21422668d6c15cf60464fdb98629))
* **parser:**  Return valid a valid AST after parsing an invalid expression ([1cdd0e31](https://github.com/gluon-lang/gluon/commit/1cdd0e31fd116c434dc42939aaa1dcb35406a471))
* **vm:**
  *  Make the compiler pipeline return futures for executing ([c0d355e2](https://github.com/gluon-lang/gluon/commit/c0d355e2149eae3e7ef0d41b112292e41018d9b5))
  *  Allow extern functions to return futures ([120f9d1d](https://github.com/gluon-lang/gluon/commit/120f9d1d170e8933654a412d5100813d065ddd8e))
  *  Add types to all variables in the debug info ([38674f1f](https://github.com/gluon-lang/gluon/commit/38674f1f202c313b49dbe16a3df18e17436b48b2))
  *  Add a pretty printer on vm values ([0288e0a4](https://github.com/gluon-lang/gluon/commit/0288e0a4a8fbe8aef3780f088e828220815ef6f5))
  *  Add a from_ut8 method for converting `Array Byte` into `String` ([a336a49f](https://github.com/gluon-lang/gluon/commit/a336a49fd506fc1d7fb9b48fce50020e68bb4669))
  *  Implement clone on OpaqueValue and Function ([b56549c4](https://github.com/gluon-lang/gluon/commit/b56549c47389e8c19dd5989e705005f97c7d21a0))



<a name="v0.2.0"></a>
## v0.2.0  (2016-09-25)

Version 0.2.0 consists of a few critical bug fixes, numerous usability improvements such as prettier printing of types and auto completion in the REPL as well as two additions to the language itself.

Row-polymorphic records are added to the type system (albeit in a slightly limited capacity) as well as type holes. More additions building on these features will be added in a backwards compatible way in upcoming versions.

In addition to the user visible changes listed here the internals have seen a lot of legacy cruft removed, in major part thanks to @brendanzab.

#### Features

*   Use InFile to display source information for parse errors ([7026d8a3](https://github.com/gluon-lang/gluon/commit/7026d8a374d780e9b0f27b9910bd229e6160b28d))
*   Use starts_with and ends_with from Rust instead of gluon ([5144ee29](https://github.com/gluon-lang/gluon/commit/5144ee295d423ca95f96a35b687906c603ea19fb))
*   Rename io.print to io.println and add io.print ([0a6b65bd](https://github.com/gluon-lang/gluon/commit/0a6b65bdd3e95dff737f6a846a9c2eafa1fd9581))
*   Implement unification of row polymorphic records ([df007c6e](https://github.com/gluon-lang/gluon/commit/df007c6e8337f582466b75e4a25c3e300a7093ee))
*   Improve readability of large types by splitting them onto multiple lines ([1c296ac9](https://github.com/gluon-lang/gluon/commit/1c296ac9841dba57f93defc416135d2bc1a8c90d))
*   Add holes to the type syntax, and use them when building the AST ([fb9bd82c](https://github.com/gluon-lang/gluon/commit/fb9bd82ce7792332e8a660e3f0ea05843d50f6d5))
*   Rename (*) to Type ([8a3e1945](https://github.com/gluon-lang/gluon/commit/8a3e194581d3c9eef70e94660c3edb89f3706629))
*   Repl UX improvements ([2ed0a35b](https://github.com/gluon-lang/gluon/commit/2ed0a35bd0e194ae9bd37b189c3f4bb59f6c6845))
* **base:**  Use quick-error for instantiate::Error ([96a8c631](https://github.com/gluon-lang/gluon/commit/96a8c63101ea2bfd02f2351eca4fa18cb80f8ef2))
* **check:**
  *  Attempt to generate variable starting with a unique letter ([f3c2e625](https://github.com/gluon-lang/gluon/commit/f3c2e625dda1a5779f4915898fb9219770a7a5db))
* **parser:**
  *  Use string slices in tokens ([e0b7d840](https://github.com/gluon-lang/gluon/commit/e0b7d840cdb9095bb52f39f5ab08ec5d5a68b851))
  *  Emit spans from the lexer instead of just locations ([e2a17a3a](https://github.com/gluon-lang/gluon/commit/e2a17a3a1e6cacf4cb9254c50bb16ae1f09aa577))
* **repl:**  Add completion to the repl ([ee4d0b60](https://github.com/gluon-lang/gluon/commit/ee4d0b60aa83f17e481ec96d048524b76b0b3645))
* **vm:**
  *  Implement field access of polymorphic records ([4696cedc](https://github.com/gluon-lang/gluon/commit/4696cedcc0a25e796361c010cddd8e8405e9d678))
  *  Allow the heap size on each thread to be limited ([f8a71f4c](https://github.com/gluon-lang/gluon/commit/f8a71f4cb79744c12fabb8c2edb0e199a37750c3))
  *  Return Result instead of Status in Pushable::push ([584c3590](https://github.com/gluon-lang/gluon/commit/584c35903f1af2856a09e5178d2cd01e21155aca))
  *  read GLUON_PATH from env var and add to new_vm (#79) ([e7254a40](https://github.com/gluon-lang/gluon/commit/(e7254a40f24d53fac6074b1189eda66032f7efc7)))

#### Bug Fixes

*   Don't gluon panic when writing only a colon (`:`) in the repl ([7864c449](https://github.com/gluon-lang/gluon/commit/7864c44912561dbdd218ce28bda5465fad1f81ad))
*   Only print a Stacktrace on panics ([c059bfd3](https://github.com/gluon-lang/gluon/commit/c059bfd33d8a0908019fc397c19e1682f4886d6e))
*   Surround operators with parens when pretty-printing ([7ccc6f22](https://github.com/gluon-lang/gluon/commit/7ccc6f229f48f0077bbb90f666cad137ebfab788), closes [#60](https://github.com/gluon-lang/gluon/issues/60))
*   Rename windows file separators characters ('\\') to '.' as well ([207bfc9a](https://github.com/gluon-lang/gluon/commit/207bfc9a658cf97aca40ff5eaff8c86e36d3474b))
*   Add a space before : when pretty printing types ([a9b160c3](https://github.com/gluon-lang/gluon/commit/a9b160c3725584702b14f76e44bbc63487024268))
*   Print ',' as separator between each type of a record ([d72d3e1b](https://github.com/gluon-lang/gluon/commit/d72d3e1b7c9d4d7313a89837d0ad184ad1cfe41c))
*   Don't return None from Source::location when byte is at end of file ([5aee09a5](https://github.com/gluon-lang/gluon/commit/5aee09a5518fbff972683644cd99ab07a5674016))
* **check:**
  *  Fail typechecking when records use a field more than once ([7bb8f0bd](https://github.com/gluon-lang/gluon/commit/7bb8f0bdfc7c25de7e3bf4f19e624bbaca784ac3))
  *  Handle unification with Type::Hole ([2912727f](https://github.com/gluon-lang/gluon/commit/2912727f496c11680a277ce7bc2323a4abb6a6ac))
  *  Detect recursive types for which unification do not terminate ([22b3c82e](https://github.com/gluon-lang/gluon/commit/22b3c82ee0955ebcfec4e2367696d28629b8c7a3))
* **completion:**
  *  Give completion for local variables when pointing to whitespace ([5c59a795](https://github.com/gluon-lang/gluon/commit/5c59a795f8558e5f1711a033f17142b29a001451))
* **repl:**
  *  Allow `:i` to be used on primitive types ([fe458488](https://github.com/gluon-lang/gluon/commit/fe458488ca336df0e604d1962ab4dcef089565a6))
  *  Include the prelude when using `:t` ([bb0f1347](https://github.com/gluon-lang/gluon/commit/bb0f1347f327c8d1e7327db26e374bb8d759a0eb))

#### Performance

*   Use a single mutex for both the stack and gc ([20fb0645](https://github.com/gluon-lang/gluon/commit/20fb0645fd681914157a848c69b7694aee9d88af))
*   use fnv instead of SipHasher for HashMaps. add type FnvMap (#106) ([4a64c68d](https://github.com/gluon-lang/gluon/commit/4a64c68d8d04a6788f1fea3d6f25471b873ee8e2))

* **check:**
  *  Avoid traversing the entire stack when generalizing ([29352bc3](https://github.com/gluon-lang/gluon/commit/29352bc38f211cb6427c6107f1b178310b0db84b))
  *  Avoid recreating new App instances in unroll_app unnecessarily ([ba4db236](https://github.com/gluon-lang/gluon/commit/ba4db236d793bb5e23ae2463512cef191827f7c9))


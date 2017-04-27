# buddy-rs256-issue

Demonstrates issue with usigning using `rs256` algo in `buddy-sign` library.

Run the application:

`lein run`

Expected: no exceptions.

Actual:

```
Hello, World!
Exception in thread "main" java.lang.IllegalArgumentException: No matching method found: initVerify for class java.security.Signature$Delegate, compiling:(/private/var/folders/7_/mhk7y9952n972b6kgt7_8l700000gn/T/form-init829514710048949323.clj:1:124)
	at clojure.lang.Compiler.load(Compiler.java:7391)
	at clojure.lang.Compiler.loadFile(Compiler.java:7317)
	at clojure.main$load_script.invokeStatic(main.clj:275)
	at clojure.main$init_opt.invokeStatic(main.clj:277)
	at clojure.main$init_opt.invoke(main.clj:277)
	at clojure.main$initialize.invokeStatic(main.clj:308)
	at clojure.main$null_opt.invokeStatic(main.clj:342)
	at clojure.main$null_opt.invoke(main.clj:339)
	at clojure.main$main.invokeStatic(main.clj:421)
	at clojure.main$main.doInvoke(main.clj:384)
	at clojure.lang.RestFn.invoke(RestFn.java:421)
	at clojure.lang.Var.invoke(Var.java:383)
	at clojure.lang.AFn.applyToHelper(AFn.java:156)
	at clojure.lang.Var.applyTo(Var.java:700)
	at clojure.main.main(main.java:37)
Caused by: java.lang.IllegalArgumentException: No matching method found: initVerify for class java.security.Signature$Delegate
	at clojure.lang.Reflector.invokeMatchingMethod(Reflector.java:80)
	at clojure.lang.Reflector.invokeInstanceMethod(Reflector.java:28)
	at buddy.core.dsa$eval737$fn__738.invoke(dsa.clj:72)
	at buddy.core.dsa$eval641$fn__672$G__628__679.invoke(dsa.clj:43)
	at buddy.core.dsa$verify.invokeStatic(dsa.clj:161)
	at buddy.core.dsa$verify.invoke(dsa.clj:158)
	at buddy.sign.jws$fn__1775.invokeStatic(jws.clj:41)
	at buddy.sign.jws$fn__1775.invoke(jws.clj:30)
	at buddy.sign.jws$verify_signature.invokeStatic(jws.clj:95)
	at buddy.sign.jws$verify_signature.invoke(jws.clj:87)
	at buddy.sign.jws$unsign.invokeStatic(jws.clj:133)
	at buddy.sign.jws$unsign.invoke(jws.clj:127)
	at buddy_rs256_issue.core$_main.invokeStatic(core.clj:6)
	at buddy_rs256_issue.core$_main.doInvoke(core.clj:4)
	at clojure.lang.RestFn.invoke(RestFn.java:397)
	at clojure.lang.Var.invoke(Var.java:375)
	at user$eval5.invokeStatic(form-init829514710048949323.clj:1)
	at user$eval5.invoke(form-init829514710048949323.clj:1)
	at clojure.lang.Compiler.eval(Compiler.java:6927)
	at clojure.lang.Compiler.eval(Compiler.java:6917)
	at clojure.lang.Compiler.load(Compiler.java:7379)
	... 14 more
``
Build fails with -transformer-api in Windows.
Include kotlin code and use id("realm-android") in submodule.

<details>
<summary>Stack Trace</summary>

```
> Task :realm:bundleLibRuntimeToDirDebug
e: java.io.FileNotFoundException: D:\a\Realm10_13_1WindowsBuild\Realm10_13_1WindowsBuild\realm\build\intermediates\compile_library_classes_jar\debug\classes.jar!/META-INF/realm_debug.kotlin_module
> Task :app:mergeLibDexDebug

	at org.jetbrains.kotlin.com.intellij.openapi.vfs.impl.ZipHandlerBase.contentsToByteArray(ZipHandlerBase.java:159)
> Task :app:compileDebugKotlin FAILED
	at org.jetbrains.kotlin.com.intellij.openapi.vfs.impl.jar.CoreJarVirtualFile.contentsToByteArray(CoreJarVirtualFile.java:127)
	at org.jetbrains.kotlin.cli.jvm.compiler.JvmPackagePartProvider$addRoots$1.invoke(JvmPackagePartProvider.kt:55)
	at org.jetbrains.kotlin.cli.jvm.compiler.JvmPackagePartProvider$addRoots$1.invoke(JvmPackagePartProvider.kt:37)
	at org.jetbrains.kotlin.cli.jvm.compiler.JvmPackagePartProviderKt.tryLoadModuleMapping(JvmPackagePartProvider.kt:72)
	at org.jetbrains.kotlin.cli.jvm.compiler.JvmPackagePartProvider.addRoots(JvmPackagePartProvider.kt:54)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinCoreEnvironment.createPackagePartProvider(KotlinCoreEnvironment.kt:308)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler$analyze$1$1.invoke(KotlinToJVMBytecodeCompiler.kt:270)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler$analyze$1$1.invoke(KotlinToJVMBytecodeCompiler.kt:53)
	at org.jetbrains.kotlin.cli.jvm.compiler.TopDownAnalyzerFacadeForJVM.createContainer(TopDownAnalyzerFacadeForJVM.kt:203)
	at org.jetbrains.kotlin.cli.jvm.compiler.TopDownAnalyzerFacadeForJVM.createContainer$default(TopDownAnalyzerFacadeForJVM.kt:152)
	at org.jetbrains.kotlin.cli.jvm.compiler.TopDownAnalyzerFacadeForJVM.analyzeFilesWithJavaIntegration(TopDownAnalyzerFacadeForJVM.kt:102)
	at org.jetbrains.kotlin.cli.jvm.compiler.TopDownAnalyzerFacadeForJVM.analyzeFilesWithJavaIntegration$default(TopDownAnalyzerFacadeForJVM.kt:100)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler$analyze$1.invoke(KotlinToJVMBytecodeCompiler.kt:265)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler$analyze$1.invoke(KotlinToJVMBytecodeCompiler.kt:53)
	at org.jetbrains.kotlin.cli.common.messages.AnalyzerWithCompilerReport.analyzeAndReport(AnalyzerWithCompilerReport.kt:115)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler.analyze(KotlinToJVMBytecodeCompiler.kt:256)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler.compileModules$cli(KotlinToJVMBytecodeCompiler.kt:99)
	at org.jetbrains.kotlin.cli.jvm.compiler.KotlinToJVMBytecodeCompiler.compileModules$cli$default(KotlinToJVMBytecodeCompiler.kt:58)
	at org.jetbrains.kotlin.cli.jvm.K2JVMCompiler.doExecute(K2JVMCompiler.kt:158)
	at org.jetbrains.kotlin.cli.jvm.K2JVMCompiler.doExecute(K2JVMCompiler.kt:53)
	at org.jetbrains.kotlin.cli.common.CLICompiler.execImpl(CLICompiler.kt:99)
	at org.jetbrains.kotlin.cli.common.CLICompiler.execImpl(CLICompiler.kt:47)
	at org.jetbrains.kotlin.cli.common.CLITool.exec(CLITool.kt:101)
	at org.jetbrains.kotlin.incremental.IncrementalJvmCompilerRunner.runCompiler(IncrementalJvmCompilerRunner.kt:475)
	at org.jetbrains.kotlin.incremental.IncrementalJvmCompilerRunner.runCompiler(IncrementalJvmCompilerRunner.kt:125)
	at org.jetbrains.kotlin.incremental.IncrementalCompilerRunner.compileIncrementally(IncrementalCompilerRunner.kt:373)
	at org.jetbrains.kotlin.incremental.IncrementalCompilerRunner.compileIncrementally$default(IncrementalCompilerRunner.kt:318)
	at org.jetbrains.kotlin.incremental.IncrementalCompilerRunner.rebuild(IncrementalCompilerRunner.kt:114)
	at org.jetbrains.kotlin.incremental.IncrementalCompilerRunner.compileImpl(IncrementalCompilerRunner.kt:207)
	at org.jetbrains.kotlin.incremental.IncrementalCompilerRunner.compile(IncrementalCompilerRunner.kt:79)
	at org.jetbrains.kotlin.daemon.CompileServiceImplBase.execIncrementalCompiler(CompileServiceImpl.kt:625)
	at org.jetbrains.kotlin.daemon.CompileServiceImplBase.access$execIncrementalCompiler(CompileServiceImpl.kt:101)
	at org.jetbrains.kotlin.daemon.CompileServiceImpl.compile(CompileServiceImpl.kt:1746)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at java.rmi/sun.rmi.server.UnicastServerRef.dispatch(UnicastServerRef.java:359)
	at java.rmi/sun.rmi.transport.Transport$1.run(Transport.java:200)
	at java.rmi/sun.rmi.transport.Transport$1.run(Transport.java:197)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.rmi/sun.rmi.transport.Transport.serviceCall(Transport.java:196)
	at java.rmi/sun.rmi.transport.tcp.TCPTransport.handleMessages(TCPTransport.java:562)
	at java.rmi/sun.rmi.transport.tcp.TCPTransport$ConnectionHandler.run0(TCPTransport.java:796)
	at java.rmi/sun.rmi.transport.tcp.TCPTransport$ConnectionHandler.lambda$run$0(TCPTransport.java:677)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.rmi/sun.rmi.transport.tcp.TCPTransport$ConnectionHandler.run(TCPTransport.java:676)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628)
	at java.base/java.lang.Thread.run(Thread.java:829)


> Task :realm:extractDebugAnnotations

55 actionable tasks: 55 executed
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:compileDebugKotlin'.
> A failure occurred while executing org.jetbrains.kotlin.compilerRunner.GradleCompilerRunnerWithWorkers$GradleKotlinCompilerWorkAction
   > Internal compiler error. See log for more details

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 3m 33s
```
</details>

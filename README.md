#
# A fatal error has been detected by the Java Runtime Environment:
#
#  EXCEPTION_ACCESS_VIOLATION (0xc0000005) at pc=0x0000000069ac29bf, pid=3684, tid=2972
#
# JRE version: Java(TM) SE Runtime Environment (22.0+36) (build 22+36-2370)
# Java VM: Java HotSpot(TM) 64-Bit Server VM (22+36-2370, mixed mode, sharing, tiered, compressed oops, compressed class ptrs, g1 gc, windows-amd64)
# Problematic frame:
# C  [jansi-2.4.0-79354dc56ce1a544-jansi.dll+0x29bf]
#
# No core dump will be written. Minidumps are not enabled by default on client versions of Windows
#
# If you would like to submit a bug report, please visit:
#   https://bugreport.java.com/bugreport/crash.jsp
# The crash happened outside the Java Virtual Machine in native code.
# See problematic frame for where to report the bug.
#

---------------  S U M M A R Y ------------

Command Line: C:\Users\itzhak\Desktop\paper-1.20.4-463.jar

Host: Intel(R) Core(TM) i5-3230M CPU @ 2.60GHz, 4 cores, 3G,  Windows 8.1 , 64 bit Build 9600 (6.3.9600.17415)
Time: Sun Mar 31 14:42:36 2024 Pacific Daylight Time elapsed time: 18.727142 seconds (0d 0h 0m 18s)

---------------  T H R E A D  ---------------

Current thread (0x000000745a924f90):  JavaThread "Server thread"        [_thread_in_native, id=2972, stack(0x0000007460300000,0x0000007460400000) (1024K)]

Stack: [0x0000007460300000,0x0000007460400000],  sp=0x00000074603fc1c0,  free space=1008k
Native frames: (J=compiled Java code, j=interpreted, Vv=VM code, C=native code)
C  [jansi-2.4.0-79354dc56ce1a544-jansi.dll+0x29bf]  (no source info available)
C  0x000000740753cf47  (no source info available)

The last pc belongs to native method entry point (kind = native) (printed below).
Java frames: (J=compiled Java code, j=interpreted, Vv=VM code)
j  org.fusesource.jansi.internal.CLibrary.isatty(I)I+0
j  org.fusesource.jansi.AnsiConsole.ansiStream(Z)Lorg/fusesource/jansi/AnsiPrintStream;+62
j  org.fusesource.jansi.AnsiConsole.initStreams()V+7
j  org.fusesource.jansi.AnsiConsole.out()Lorg/fusesource/jansi/AnsiPrintStream;+0
j  net.kyori.ansi.JAnsiColorLevel.computeFromJAnsi()Lnet/kyori/ansi/ColorLevel;+0
j  net.kyori.ansi.ColorLevel.compute()Lnet/kyori/ansi/ColorLevel;+293
j  net.kyori.adventure.text.serializer.ansi.ANSIComponentSerializerImpl$BuilderImpl.<init>()V+5
j  net.kyori.adventure.text.serializer.ansi.ANSIComponentSerializer.builder()Lnet/kyori/adventure/text/serializer/ansi/ANSIComponentSerializer$Builder;+4
j  io.papermc.paper.adventure.PaperAdventure.<clinit>()V+75
v  ~StubRoutines::call_stub 0x000000740753100d
j  io.papermc.paper.adventure.providers.PlainTextComponentSerializerProviderImpl.lambda$plainText$0(Lnet/kyori/adventure/text/serializer/plain/PlainTextComponentSerializer$Builder;)V+1
j  io.papermc.paper.adventure.providers.PlainTextComponentSerializerProviderImpl$$Lambda+0x0000007410d1a458.accept(Ljava/lang/Object;)V+4
j  net.kyori.adventure.text.serializer.plain.PlainTextComponentSerializerImpl$BuilderImpl.<init>()V+15
j  net.kyori.adventure.text.serializer.plain.PlainTextComponentSerializer.builder()Lnet/kyori/adventure/text/serializer/plain/PlainTextComponentSerializer$Builder;+4
j  io.papermc.paper.adventure.providers.PlainTextComponentSerializerProviderImpl.plainTextSimple()Lnet/kyori/adventure/text/serializer/plain/PlainTextComponentSerializer;+0
j  net.kyori.adventure.text.serializer.plain.PlainTextComponentSerializerImpl$Instances$$Lambda+0x0000007410d1a898.apply(Ljava/lang/Object;)Ljava/lang/Object;+4
J 7617 c2 java.util.Optional.map(Ljava/util/function/Function;)Ljava/util/Optional; java.base@22 (30 bytes) @ 0x0000007407f14690 [0x0000007407f14620+0x0000000000000070]
j  net.kyori.adventure.text.serializer.plain.PlainTextComponentSerializerImpl$Instances.<clinit>()V+8
v  ~StubRoutines::call_stub 0x000000740753100d
j  net.kyori.adventure.text.serializer.plain.PlainTextComponentSerializer.plainText()Lnet/kyori/adventure/text/serializer/plain/PlainTextComponentSerializer;+0
j  co.aikar.timings.Timings.warnAboutDeprecationOnEnable()V+15
j  co.aikar.timings.Timings.setTimingsEnabled(Z)V+4
j  co.aikar.timings.MinecraftTimings.processConfig(Lio/papermc/paper/configuration/GlobalConfiguration$Timings;)V+89
j  io.papermc.paper.configuration.GlobalConfiguration$Timings.postProcess()V+1
j  java.lang.invoke.DirectMethodHandle$Holder.invokeSpecial(Ljava/lang/Object;Ljava/lang/Object;)V+10 java.base@22
j  java.lang.invoke.LambdaForm$MH+0x0000007410d01000.invoke(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;+31 java.base@22
J 8353 c1 jdk.internal.reflect.DirectMethodHandleAccessor.invoke(Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object; java.base@22 (92 bytes) @ 0x0000007400c42f54 [0x0000007400c42c20+0x0000000000000334]
j  java.lang.reflect.Method.invoke(Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object;+102 java.base@22
j  org.spongepowered.configurate.objectmapping.meta.PostProcessor.lambda$methodsAnnotated$0(Ljava/util/List;Ljava/lang/reflect/Type;Ljava/lang/Object;)V+42
j  org.spongepowered.configurate.objectmapping.meta.PostProcessor$$Lambda+0x0000007410d07870.postProcess(Ljava/lang/Object;)V+9
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.load0(Lorg/spongepowered/configurate/ConfigurationNode;Lorg/spongepowered/configurate/util/CheckedFunction;)Ljava/lang/Object;+318
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.load(Lorg/spongepowered/configurate/ConfigurationNode;)Ljava/lang/Object;+8
j  org.spongepowered.configurate.objectmapping.ObjectMapperFactoryImpl.emptyValue(Ljava/lang/reflect/Type;Lorg/spongepowered/configurate/ConfigurationOptions;)Ljava/lang/Object;+13
j  org.spongepowered.configurate.serialize.TypeSerializer.emptyValue(Ljava/lang/reflect/AnnotatedType;Lorg/spongepowered/configurate/ConfigurationOptions;)Ljava/lang/Object;+8
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.lambda$load0$1(Lorg/spongepowered/configurate/serialize/TypeSerializer;Lorg/spongepowered/configurate/objectmapping/FieldData;Lorg/spongepowered/configurate/ConfigurationNode;)Ljava/lang/Object;+11
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl$$Lambda+0x0000007410d069b0.get()Ljava/lang/Object;+12
j  org.spongepowered.configurate.objectmapping.ObjectFieldDiscoverer$1.complete(Ljava/lang/Object;Ljava/util/Map;)V+58
j  org.spongepowered.configurate.objectmapping.ObjectFieldDiscoverer$1.complete(Ljava/lang/Object;Ljava/lang/Object;)V+6
j  io.papermc.paper.configuration.mapping.InnerClassInstanceFactory.complete(Ljava/lang/Object;Ljava/util/Map;)V+197
j  io.papermc.paper.configuration.mapping.InnerClassInstanceFactory.complete(Ljava/util/Map;)Ljava/lang/Object;+37
j  io.papermc.paper.configuration.mapping.InnerClassInstanceFactory.complete(Ljava/lang/Object;)Ljava/lang/Object;+5
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.lambda$load$0(Ljava/lang/Object;)Ljava/lang/Object;+5
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl$$Lambda+0x0000007410d06318.apply(Ljava/lang/Object;)Ljava/lang/Object;+5
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.load0(Lorg/spongepowered/configurate/ConfigurationNode;Lorg/spongepowered/configurate/util/CheckedFunction;)Ljava/lang/Object;+274
j  org.spongepowered.configurate.objectmapping.ObjectMapperImpl.load(Lorg/spongepowered/configurate/ConfigurationNode;)Ljava/lang/Object;+8
j  org.spongepowered.configurate.objectmapping.ObjectMapperFactoryImpl.deserialize(Ljava/lang/reflect/Type;Lorg/spongepowered/configurate/ConfigurationNode;)Ljava/lang/Object;+33
j  org.spongepowered.configurate.AbstractConfigurationNode.get0(Ljava/lang/reflect/Type;Z)Ljava/lang/Object;+131
j  org.spongepowered.configurate.AbstractConfigurationNode.get(Ljava/lang/reflect/Type;)Ljava/lang/Object;+3
j  org.spongepowered.configurate.ConfigurationNode.get(Ljava/lang/Class;)Ljava/lang/Object;+2
j  org.spongepowered.configurate.ConfigurationNode.require(Ljava/lang/Class;)Ljava/lang/Object;+2
j  io.papermc.paper.configuration.Configurations.lambda$creator$0(Ljava/lang/Class;ZLorg/spongepowered/configurate/ConfigurationNode;)Ljava/lang/Object;+2
j  io.papermc.paper.configuration.Configurations$$Lambda+0x0000007410cd8da8.apply(Ljava/lang/Object;)Ljava/lang/Object;+12
j  io.papermc.paper.configuration.Configurations.initializeGlobalConfiguration(Lorg/spongepowered/configurate/util/CheckedFunction;)Ljava/lang/Object;+126
j  io.papermc.paper.configuration.Configurations.initializeGlobalConfiguration(Lnet/minecraft/core/IRegistryCustom;)Ljava/lang/Object;+9
j  io.papermc.paper.configuration.PaperConfigurations.initializeGlobalConfiguration(Lnet/minecraft/core/IRegistryCustom;)Lio/papermc/paper/configuration/GlobalConfiguration;+2
j  net.minecraft.server.dedicated.DedicatedServer.e()Z+354
j  net.minecraft.server.MinecraftServer.w()V+5
j  net.minecraft.server.MinecraftServer.lambda$spin$0(Ljava/util/concurrent/atomic/AtomicReference;)V+7
j  net.minecraft.server.MinecraftServer$$Lambda+0x0000007410b53d58.run()V+4
j  java.lang.Thread.runWith(Ljava/lang/Object;Ljava/lang/Runnable;)V+5 java.base@22
j  java.lang.Thread.run()V+19 java.base@22
v  ~StubRoutines::call_stub 0x000000740753100d

siginfo: EXCEPTION_ACCESS_VIOLATION (0xc0000005), writing address 0x0000000000000000


Registers:
RAX=0x0000000000000000, RBX=0x000000745d601db0, RCX=0x0000000000000000, RDX=0x0000000069ac6362
RSP=0x00000074603fc1c0, RBP=0x00000074603fc688, RSI=0x00000074511ab538, RDI=0x0000000000000200
R8 =0x00000074603fc1b8, R9 =0x00000074603fc688, R10=0x0000000000000000, R11=0x0000000000000202
R12=0x0000000000000000, R13=0x000000745d601db0, R14=0x00000074603fc6a8, R15=0x000000745a924f90
RIP=0x0000000069ac29bf, EFLAGS=0x0000000000010246


Register to memory mapping:

RAX=0x0 is null
RBX={method} {0x000000745d601db8} 'isatty' '(I)I' in 'org/fusesource/jansi/internal/CLibrary'
RCX=0x0 is null
RDX=0x0000000069ac6362 jansi-2.4.0-79354dc56ce1a544-jansi.dll
RSP=0x00000074603fc1c0 is pointing into the stack for thread: 0x000000745a924f90
RBP=0x00000074603fc688 is pointing into the stack for thread: 0x000000745a924f90
RSI=0x00000074511ab538 is pointing into metadata
RDI=0x0000000000000200 is an unknown value
R8 =0x00000074603fc1b8 is pointing into the stack for thread: 0x000000745a924f90
R9 =0x00000074603fc688 is pointing into the stack for thread: 0x000000745a924f90
R10=0x0 is null
R11=0x0000000000000202 is an unknown value
R12=0x0 is null
R13={method} {0x000000745d601db8} 'isatty' '(I)I' in 'org/fusesource/jansi/internal/CLibrary'
R14=0x00000074603fc6a8 is pointing into the stack for thread: 0x000000745a924f90
R15=0x000000745a924f90 is a thread

Top of Stack: (sp=0x00000074603fc1c0)
0x00000074603fc1c0:   000000745d601db0 00007ffc18430d40
0x00000074603fc1d0:   00000074603fc688 00000074511ab538
0x00000074603fc1e0:   00000074603fc1fc 00000000fff01078
0x00000074603fc1f0:   00000000d28f6e20 000000100f013b38
0x00000074603fc200:   0000007400000000 0000000000000000
0x00000074603fc210:   00000074603fc5c0 00007ffbfd119500
0x00000074603fc220:   000000745a924f90 0000000000010132
0x00000074603fc230:   00000074603fc2d0 00000074603fc1e8
0x00000074603fc240:   00000074603fc229 0000000800000002
0x00000074603fc250:   000000745a924f00 0000000000000000
0x00000074603fc260:   00007993b4b8ffbc 00000074550c1710
0x00000074603fc270:   000000745a73bed8 00007ffbfd3e4e8b
0x00000074603fc280:   00000074550c1748 00000074550c1701
0x00000074603fc290:   0000000000000003 00007ffbfd3e117f
0x00000074603fc2a0:   000000745a73bed8 000000745a73bee0
0x00000074603fc2b0:   00000074603fc5c0 00000074603fc6a8
0x00000074603fc2c0:   000000745a924f90 00007ffbfd10a019
0x00000074603fc2d0:   00007ffbfd99b148 00000074511ab538
0x00000074603fc2e0:   00007ffbfd99b148 00000074603fc439
0x00000074603fc2f0:   00007ffbfd6dce90 0000003200000000
0x00000074603fc300:   0000000000000000 0000000000000000
0x00000074603fc310:   000000740f446798 000000000000000a
0x00000074603fc320:   0000000000000155 0000000000000032
0x00000074603fc330:   0000000000000060 00000074603f0000
0x00000074603fc340:   000000745d601db0 00000074550c1710
0x00000074603fc350:   00000074603fc3f0 00007ffc082137eb
0x00000074603fc360:   0000007455ddcb04 00007ffbfd3e4f19
0x00000074603fc370:   00007993b4b8fc8c 00007ffbfd770079
0x00000074603fc380:   000000745a924f90 0000000000000003
0x00000074603fc390:   00000074550c1ae8 00000074603fc5c0
0x00000074603fc3a0:   00000074550c1710 00000074550c1710
0x00000074603fc3b0:   000000745a924f90 00007ffbfd3e4948 

Instructions: (pc=0x0000000069ac29bf)
0x0000000069ac28bf:   e1 49 89 c5 49 8b 04 24 48 8b 54 24 68 4c 89 6c
0x0000000069ac28cf:   24 20 ff 90 e0 06 00 00 4c 89 e8 66 41 c7 44 1d
0x0000000069ac28df:   fe 00 00 48 83 c4 40 5b 41 5c 41 5d c3 90 90 90
0x0000000069ac28ef:   90 41 54 48 81 ec 40 04 00 00 44 89 c1 ff 15 ea
0x0000000069ac28ff:   89 00 00 49 89 c4 48 89 c1 ff 15 16 89 00 00 83
0x0000000069ac290f:   f8 02 75 15 48 8d 54 24 40 4c 89 e1 ff 15 eb 88
0x0000000069ac291f:   00 00 85 c0 e9 ba 00 00 00 48 83 3d f0 66 00 00
0x0000000069ac292f:   00 75 14 48 8d 0d 07 3a 00 00 ff 15 1d 89 00 00
0x0000000069ac293f:   48 89 05 da 66 00 00 48 8b 0d d3 66 00 00 48 85
0x0000000069ac294f:   c9 75 07 31 c0 e9 aa 00 00 00 48 83 3d c7 66 00
0x0000000069ac295f:   00 00 75 14 48 8d 15 ea 39 00 00 ff 15 cc 88 00
0x0000000069ac296f:   00 48 89 05 b1 66 00 00 48 8b 05 aa 66 00 00 48
0x0000000069ac297f:   85 c0 74 cf 48 8d 54 24 3c 41 b9 fe 03 00 00 4c
0x0000000069ac298f:   8d 44 24 40 4c 89 e1 48 89 54 24 20 ba 01 00 00
0x0000000069ac299f:   00 ff d0 85 c0 75 ac 8b 44 24 40 4c 8b 64 24 48
0x0000000069ac29af:   48 8d 15 ac 39 00 00 66 d1 e8 4c 89 e1 0f b7 c0
0x0000000069ac29bf:   66 41 c7 04 44 00 00 e8 15 20 00 00 48 85 c0 74
0x0000000069ac29cf:   1a 48 8d 15 97 39 00 00 4c 89 e1 e8 01 20 00 00
0x0000000069ac29df:   48 85 c0 0f 95 c0 0f b6 c0 eb 19 48 8d 15 87 39
0x0000000069ac29ef:   00 00 4c 89 e1 e8 e7 1f 00 00 48 85 c0 75 d2 e9
0x0000000069ac29ff:   4f ff ff ff 48 81 c4 40 04 00 00 41 5c c3 90 90
0x0000000069ac2a0f:   90 41 54 48 83 ec 20 83 3d e3 67 00 00 00 49 89
0x0000000069ac2a1f:   cc 75 6b 48 8b 01 ff 90 f8 00 00 00 4c 8d 0d 5e
0x0000000069ac2a2f:   39 00 00 4c 8d 05 59 39 00 00 4c 89 e1 48 89 c2
0x0000000069ac2a3f:   48 89 05 c2 67 00 00 49 8b 04 24 ff 90 f0 02 00
0x0000000069ac2a4f:   00 48 8b 15 b1 67 00 00 4c 8d 0d 3f 39 00 00 4c
0x0000000069ac2a5f:   89 e1 48 89 05 a8 67 00 00 49 8b 04 24 4c 8d 05
0x0000000069ac2a6f:   2c 39 00 00 ff 90 f0 02 00 00 48 89 05 98 67 00
0x0000000069ac2a7f:   00 0f ae f0 c7 05 73 67 00 00 01 00 00 00 48 83
0x0000000069ac2a8f:   c4 20 41 5c c3 41 56 41 55 41 54 48 83 ec 20 83
0x0000000069ac2a9f:   3d 5b 67 00 00 00 49 89 cc 49 89 d6 4d 89 c5 75
0x0000000069ac2aaf:   05 e8 5b ff ff ff 49 8b 04 24 4c 89 f2 4c 89 e1 


Stack slot to memory mapping:

stack at sp + 0 slots: {method} {0x000000745d601db8} 'isatty' '(I)I' in 'org/fusesource/jansi/internal/CLibrary'
stack at sp + 1 slots: 0x00007ffc18430d40 ntdll.dll
stack at sp + 2 slots: 0x00000074603fc688 is pointing into the stack for thread: 0x000000745a924f90
stack at sp + 3 slots: 0x00000074511ab538 is pointing into metadata
stack at sp + 4 slots: 0x00000074603fc1fc is pointing into the stack for thread: 0x000000745a924f90
stack at sp + 5 slots: 0x00000000fff01078 is an oop: java.net.URLClassLoader 
{0x00000000fff01078} - klass: 'java/net/URLClassLoader'
 - ---- fields (total size 12 words):
 - private 'defaultAssertionStatus' 'Z' @12  false (0x00)
 - injected 'loader_data' 'J' @16  499646275232 (0x00000074553d1ea0)
 - private final 'parent' 'Ljava/lang/ClassLoader;' @24  a 'jdk/internal/loader/ClassLoaders$PlatformClassLoader'{0x00000000fff00b48} (0xfff00b48)
 - private final 'name' 'Ljava/lang/String;' @28  null (0x00000000)
 - private final 'unnamedModule' 'Ljava/lang/Module;' @32  a 'java/lang/Module'{0x00000000fff321a0} (0xfff321a0)
 - private final 'nameAndId' 'Ljava/lang/String;' @36  "java.net.URLClassLoader @61e717c2"{0x00000000ff840938} (0xff840938)
 - private final 'parallelLockMap' 'Ljava/util/concurrent/ConcurrentHashMap;' @40  a 'java/util/concurrent/ConcurrentHashMap'{0x00000000ff840988} (0xff840988)
 - private final 'package2certs' 'Ljava/util/concurrent/ConcurrentHashMap;' @44  a 'java/util/concurrent/ConcurrentHashMap'{0x00000000ff884d10} (0xff884d10)
 - private final 'classes' 'Ljava/util/ArrayList;' @48  a 'java/util/ArrayList'{0x00000000ff888dc0} (0xff888dc0)
 - private final 'defaultDomain' 'Ljava/security/ProtectionDomain;' @52  a 'java/security/ProtectionDomain'{0x00000000ff8af780} (0xff8af780)
 - private final 'packages' 'Ljava/util/concurrent/ConcurrentHashMap;' @56  a 'java/util/concurrent/ConcurrentHashMap'{0x00000000ff828670} (0xff828670)
 - private final 'libraries' 'Ljdk/internal/loader/NativeLibraries;' @60  a 'jdk/internal/loader/NativeLibraries'{0x00000000ff828520} (0xff828520)
 - final 'assertionLock' 'Ljava/lang/Object;' @64  a 'java/lang/Object'{0x00000000ff828510} (0xff828510)
 - private 'packageAssertionStatus' 'Ljava/util/Map;' @68  null (0x00000000)
 - 'classAssertionStatus' 'Ljava/util/Map;' @72  null (0x00000000)
 - private volatile 'classLoaderValueMap' 'Ljava/util/concurrent/ConcurrentHashMap;' @76  a 'java/util/concurrent/ConcurrentHashMap'{0x00000000ff827048} (0xff827048)
 - private final 'pdcache' 'Ljava/util/Map;' @80  a 'java/util/concurrent/ConcurrentHashMap'{0x00000000ff8266a0} (0xff8266a0)
 - private final 'ucp' 'Ljdk/internal/loader/URLClassPath;' @84  a 'jdk/internal/loader/URLClassPath'{0x00000000ff9b6d70} (0xff9b6d70)
 - private final 'acc' 'Ljava/security/AccessControlContext;' @88  a 'java/security/AccessControlContext'{0x00000000ff9b6d30} (0xff9b6d30)
 - private final 'closeables' 'Ljava/util/WeakHashMap;' @92  a 'java/util/WeakHashMap'{0x00000000ff9b6b60} (0xff9b6b60)
stack at sp + 6 slots: 0x00000000d28f6e20 is an oop: java.lang.String 
{0x00000000d28f6e20} - klass: 'java/lang/String'
 - string: "Java_org_fusesource_jansi_internal_CLibrary_isatty"
 - ---- fields (total size 3 words):
 - private 'hash' 'I' @12  0 (0x00000000)
 - private final 'coder' 'B' @16  0 (0x00)
 - private 'hashIsZero' 'Z' @17  false (0x00)
 - injected 'flags' 'B' @18  0 (0x00)
 - private final 'value' '[B' @20  [B{0x00000000d28f6e38} (0xd28f6e38)
stack at sp + 7 slots: 0x000000100f013b38 is an unknown value

native method entry point (kind = native)  [0x000000740753cb20, 0x000000740753d640]  2848 bytes
[MachCode]
  0x000000740753cb20: 488b 4b08 | 0fb7 492e | 584c 8d74 | ccf8 6800 | 0000 0068 | 0000 0000 | 5055 488b | ec41 5568 
  0x000000740753cb40: 0000 0000 | 4c8b 6b08 | 4d8d 6d38 | 5348 8b53 | 0848 8b52 | 0848 8b52 | 1848 8b52 | 7048 8b12 
  0x000000740753cb60: 5248 8b53 | 1048 85d2 | 0f84 0700 | 0000 4881 | c210 0100 | 0052 488b | 5308 488b | 5208 488b 
  0x000000740753cb80: 5210 5249 | 8bc6 482b | c548 c1e8 | 0350 6800 | 0000 0068 | f7ff ffff | 41c6 8781 | 0400 0001 
  0x000000740753cba0: 488b 4310 | 4885 c074 | 208b 88cc | 0000 0083 | c102 8988 | cc00 0000 | 2388 e000 | 0000 0f84 
  0x000000740753cbc0: cb09 0000 | e9cf 0000 | 0048 8b43 | 1848 85c0 | 0f85 b000 | 0000 e805 | 0000 00e9 | 9900 0000 
  0x000000740753cbe0: 488b d348 | 8d44 2408 | 4c89 6dc0 | 498b cfc5 | f877 4989 | afb0 0300 | 0049 8987 | a003 0000 
  0x000000740753cc00: 4883 ec20 | 40f6 c40f | 0f84 1900 | 0000 4883 | ec08 48b8 | f0a2 10fd | fb7f 0000 | ffd0 4883 
  0x000000740753cc20: c408 e90c | 0000 0048 | b8f0 a210 | fdfb 7f00 | 00ff d048 | 83c4 2049 | c787 a003 | 0000 0000 
  0x000000740753cc40: 0000 49c7 | 87b0 0300 | 0000 0000 | 0049 c787 | a803 0000 | 0000 0000 | c5f8 7749 | 837f 0800 
  0x000000740753cc60: 0f84 0500 | 0000 e995 | 42ff ff4c | 8b6d c04c | 8b75 c84e | 8d74 f500 | c348 8b43 | 1848 85c0 
  0x000000740753cc80: 0f84 1200 | 0000 8b48 | 0883 c102 | 8948 0823 | 481c 0f84 | f708 0000 | 493b a7f0 | 0400 000f 
  0x000000740753cca0: 8748 0000 | 0089 8424 | 00f0 ffff | 8984 2400 | e0ff ff89 | 8424 00d0 | ffff 8984 | 2400 c0ff 
  0x000000740753ccc0: ff89 8424 | 00b0 ffff | 8984 2400 | a0ff ff89 | 8424 0090 | ffff 8984 | 2400 80ff | ff49 3ba7 
  0x000000740753cce0: e804 0000 | 7607 4989 | a7f0 0400 | 0041 c687 | 8104 0000 | 0049 baac | 4097 fdfb | 7f00 0041 
  0x000000740753cd00: 803a 000f | 843e 0000 | 0048 8b55 | e849 8bcf | 4883 ec20 | 40f6 c40f | 0f84 1900 | 0000 4883 
  0x000000740753cd20: ec08 48b8 | 00b6 47fd | fb7f 0000 | ffd0 4883 | c408 e90c | 0000 0048 | b800 b647 | fdfb 7f00 
  0x000000740753cd40: 00ff d048 | 83c4 2048 | 8b5d e84c | 8b5b 0845 | 0fb7 5b2e | 41c1 e303 | 492b e348 | 83ec 2048 
  0x000000740753cd60: 83e4 f04c | 8b5b 604d | 85db 0f85 | ab00 0000 | e805 0000 | 00e9 9900 | 0000 488b | d348 8d44 
  0x000000740753cd80: 2408 4c89 | 6dc0 498b | cfc5 f877 | 4989 afb0 | 0300 0049 | 8987 a003 | 0000 4883 | ec20 40f6 
  0x000000740753cda0: c40f 0f84 | 1900 0000 | 4883 ec08 | 48b8 10ca | 10fd fb7f | 0000 ffd0 | 4883 c408 | e90c 0000 
  0x000000740753cdc0: 0048 b810 | ca10 fdfb | 7f00 00ff | d048 83c4 | 2049 c787 | a003 0000 | 0000 0000 | 49c7 87b0 
  0x000000740753cde0: 0300 0000 | 0000 0049 | c787 a803 | 0000 0000 | 0000 c5f8 | 7749 837f | 0800 0f84 | 0500 0000 
  0x000000740753ce00: e9fb 40ff | ff4c 8b6d | c04c 8b75 | c84e 8d74 | f500 c348 | 8b5d e84c | 8b5b 6041 | ffd3 488b 
  0x000000740753ce20: 5de8 4889 | 4518 448b | 5b28 41f6 | c308 0f84 | 1b00 0000 | 4c8b 5b08 | 4d8b 5b08 | 4d8b 5b18 
  0x000000740753ce40: 4d8b 5b70 | 4d8b 1b4c | 895d 1048 | 8d55 1048 | 8b43 5849 | ba00 0d48 | fdfb 7f00 | 0049 3bc2 
  0x000000740753ce60: 0f85 ab00 | 0000 e805 | 0000 00e9 | 9900 0000 | 488b d348 | 8d44 2408 | 4c89 6dc0 | 498b cfc5 
  0x000000740753ce80: f877 4989 | afb0 0300 | 0049 8987 | a003 0000 | 4883 ec20 | 40f6 c40f | 0f84 1900 | 0000 4883 
  0x000000740753cea0: ec08 48b8 | 10ca 10fd | fb7f 0000 | ffd0 4883 | c408 e90c | 0000 0048 | b810 ca10 | fdfb 7f00 
  0x000000740753cec0: 00ff d048 | 83c4 2049 | c787 a003 | 0000 0000 | 0000 49c7 | 87b0 0300 | 0000 0000 | 0049 c787 
  0x000000740753cee0: a803 0000 | 0000 0000 | c5f8 7749 | 837f 0800 | 0f84 0500 | 0000 e905 | 40ff ff4c | 8b6d c04c 
  0x000000740753cf00: 8b75 c84e | 8d74 f500 | c348 8b5d | e848 8b43 | 5849 8d8f | c003 0000 | c5f8 7749 | 89af b003 
  0x000000740753cf20: 0000 49ba | 18cf 5307 | 7400 0000 | 4d89 97a8 | 0300 0049 | 89a7 a003 | 0000 41c7 | 8754 0400 
  0x000000740753cf40: 0004 0000 | 00ff d0c5 | f877 4883 | ec10 c5fb | 1104 2448 | 83ec 1048 | 8904 2448 | c744 2408 
  0x000000740753cf60: 0000 0000 | 41c7 8754 | 0400 0005 | 0000 00f0 | 8344 24c0 | 0049 3baf | 5804 0000 | 0f87 0e00 
  0x000000740753cf80: 0000 4183 | bf50 0400 | 0000 0f84 | 2000 0000 | 498b cf4c | 8be4 4883 | ec20 4883 | e4f0 48b8 
  0x000000740753cfa0: c01f 12fd | fb7f 0000 | ffd0 498b | e44d 33e4 | 41c7 8754 | 0400 0008 | 0000 0049 | c787 a003 
  0x000000740753cfc0: 0000 0000 | 0000 49c7 | 87b0 0300 | 0000 0000 | 0049 c787 | a803 0000 | 0000 0000 | c5f8 774d 
  0x000000740753cfe0: 8b9f 3004 | 0000 41c7 | 8300 0100 | 0000 0000 | 0049 bb1a | a553 0774 | 0000 004c | 3b5d 180f 
  0x000000740753d000: 8524 0200 | 0048 8b04 | 2448 83c4 | 1048 85c0 | 0f84 fe01 | 0000 a803 | 0f85 0800 | 0000 488b 
  0x000000740753d020: 00e9 ee01 | 0000 a801 | 0f85 0900 | 0000 488b | 40fe e9dd | 0100 0048 | 8b40 ff41 | 807f 3800 
  0x000000740753d040: 0f84 ce01 | 0000 4883 | f800 0f84 | c401 0000 | 4d8b 5f28 | 4983 fb00 | 0f84 1400 | 0000 4983 
  0x000000740753d060: eb08 4d89 | 5f28 4d03 | 5f30 4989 | 03e9 a201 | 0000 4881 | ecd0 0000 | 0048 8904 | 2448 894c 
  0x000000740753d080: 2408 4889 | 5424 1048 | 8974 2418 | 4889 7c24 | 204c 8944 | 2428 4c89 | 4c24 304c | 8954 2438 
  0x000000740753d0a0: 4c89 5c24 | 40c5 fb11 | 4424 50c5 | fb11 4c24 | 58c5 fb11 | 5424 60c5 | fb11 5c24 | 68c5 fb11 
  0x000000740753d0c0: 6424 70c5 | fb11 6c24 | 78c5 fb11 | b424 8000 | 0000 c5fb | 11bc 2488 | 0000 00c5 | 7b11 8424 
  0x000000740753d0e0: 9000 0000 | c57b 118c | 2498 0000 | 00c5 7b11 | 9424 a000 | 0000 c57b | 119c 24a8 | 0000 00c5 
  0x000000740753d100: 7b11 a424 | b000 0000 | c57b 11ac | 24b8 0000 | 00c5 7b11 | b424 c000 | 0000 c57b | 11bc 24c8 
  0x000000740753d120: 0000 0049 | 8bd7 488b | c848 83ec | 2040 f6c4 | 0f0f 8419 | 0000 0048 | 83ec 0848 | b830 3e05 
  0x000000740753d140: fdfb 7f00 | 00ff d048 | 83c4 08e9 | 0c00 0000 | 48b8 303e | 05fd fb7f | 0000 ffd0 | 4883 c420 
  0x000000740753d160: c57b 10bc | 24c8 0000 | 00c5 7b10 | b424 c000 | 0000 c57b | 10ac 24b8 | 0000 00c5 | 7b10 a424 
  0x000000740753d180: b000 0000 | c57b 109c | 24a8 0000 | 00c5 7b10 | 9424 a000 | 0000 c57b | 108c 2498 | 0000 00c5 
  0x000000740753d1a0: 7b10 8424 | 9000 0000 | c5fb 10bc | 2488 0000 | 00c5 fb10 | b424 8000 | 0000 c5fb | 106c 2478 
  0x000000740753d1c0: c5fb 1064 | 2470 c5fb | 105c 2468 | c5fb 1054 | 2460 c5fb | 104c 2458 | c5fb 1044 | 2450 4c8b 
  0x000000740753d1e0: 5c24 404c | 8b54 2438 | 4c8b 4c24 | 304c 8b44 | 2428 488b | 7c24 2048 | 8b74 2418 | 488b 5424 
  0x000000740753d200: 1048 8b4c | 2408 488b | 0424 4881 | c4d0 0000 | 00c5 f877 | 4889 4510 | 4883 ec10 | 4889 0424 
  0x000000740753d220: 48c7 4424 | 0800 0000 | 0041 83bf | d004 0000 | 020f 85bf | 0000 0048 | 81ec 8000 | 0000 4889 
  0x000000740753d240: 4424 7848 | 894c 2470 | 4889 5424 | 6848 895c | 2460 4889 | 6c24 5048 | 8974 2448 | 4889 7c24 
  0x000000740753d260: 404c 8944 | 2438 4c89 | 4c24 304c | 8954 2428 | 4c89 5c24 | 204c 8964 | 2418 4c89 | 6c24 104c 
  0x000000740753d280: 8974 2408 | 4c89 3c24 | 4c8b e448 | 83ec 2048 | 83e4 f048 | b850 ee47 | fdfb 7f00 | 00ff d049 
  0x000000740753d2a0: 8be4 4c8b | 3c24 4c8b | 7424 084c | 8b6c 2410 | 4c8b 6424 | 184c 8b5c | 2420 4c8b | 5424 284c 
  0x000000740753d2c0: 8b4c 2430 | 4c8b 4424 | 3848 8b7c | 2440 488b | 7424 4848 | 8b6c 2450 | 488b 5c24 | 6048 8b54 
  0x000000740753d2e0: 2468 488b | 4c24 7048 | 8b44 2478 | 4881 c480 | 0000 004d | 33e4 488b | 5de8 4c8b | 6b08 4d8d 
  0x000000740753d300: 6d38 4983 | 7f08 000f | 84bb 0000 | 00e8 0500 | 0000 e996 | 0000 0048 | 8d44 2408 | 4c89 6dc0 
  0x000000740753d320: 498b cfc5 | f877 4989 | afb0 0300 | 0049 8987 | a003 0000 | 4883 ec20 | 40f6 c40f | 0f84 1900 
  0x000000740753d340: 0000 4883 | ec08 48b8 | 50e8 10fd | fb7f 0000 | ffd0 4883 | c408 e90c | 0000 0048 | b850 e810 
  0x000000740753d360: fdfb 7f00 | 00ff d048 | 83c4 2049 | c787 a003 | 0000 0000 | 0000 49c7 | 87b0 0300 | 0000 0000 
  0x000000740753d380: 0049 c787 | a803 0000 | 0000 0000 | c5f8 7749 | 837f 0800 | 0f84 0500 | 0000 e961 | 3bff ff4c 
  0x000000740753d3a0: 8b6d c04c | 8b75 c84e | 8d74 f500 | c348 b9c0 | 286f fdfb | 7f00 0048 | 83e4 f048 | b890 9536 
  0x000000740753d3c0: fdfb 7f00 | 00ff d0f4 | 448b 5b28 | 41f6 c320 | 0f84 4401 | 0000 488d | 55a8 4c8b | 5a08 4d85 
  0x000000740753d3e0: db0f 85bb | 0000 00e8 | 0500 0000 | e996 0000 | 0048 8d44 | 2408 4c89 | 6dc0 498b | cfc5 f877 
  0x000000740753d400: 4989 afb0 | 0300 0049 | 8987 a003 | 0000 4883 | ec20 40f6 | c40f 0f84 | 1900 0000 | 4883 ec08 
  0x000000740753d420: 48b8 80e7 | 10fd fb7f | 0000 ffd0 | 4883 c408 | e90c 0000 | 0048 b880 | e710 fdfb | 7f00 00ff 
  0x000000740753d440: d048 83c4 | 2049 c787 | a003 0000 | 0000 0000 | 49c7 87b0 | 0300 0000 | 0000 0049 | c787 a803 
  0x000000740753d460: 0000 0000 | 0000 c5f8 | 7749 837f | 0800 0f84 | 0500 0000 | e987 3aff | ff4c 8b6d | c04c 8b75 
  0x000000740753d480: c84e 8d74 | f500 c348 | b9c0 286f | fdfb 7f00 | 0048 83e4 | f048 b890 | 9536 fdfb | 7f00 00ff 
  0x000000740753d4a0: d0f4 4c89 | 6dc0 488d | 024c 8b4a | 0848 c742 | 0800 0000 | 004c 8b00 | 4d85 c00f | 840b 0000 
  0x000000740753d4c0: 00f0 4d0f | b101 0f85 | 0c00 0000 | 49ff 8f58 | 0500 00e9 | 3e00 0000 | 4c89 4a08 | 488b ca48 
  0x000000740753d4e0: 83ec 2040 | f6c4 0f0f | 8419 0000 | 0048 83ec | 0848 b810 | ba10 fdfb | 7f00 00ff | d048 83c4 
  0x000000740753d500: 08e9 0c00 | 0000 48b8 | 10ba 10fd | fb7f 0000 | ffd0 4883 | c420 4c8b | 6dc0 49ba | ac40 97fd 
  0x000000740753d520: fb7f 0000 | 4180 3a00 | 0f84 3e00 | 0000 488b | 55e8 498b | cf48 83ec | 2040 f6c4 | 0f0f 8419 
  0x000000740753d540: 0000 0048 | 83ec 0848 | b800 b647 | fdfb 7f00 | 00ff d048 | 83c4 08e9 | 0c00 0000 | 48b8 00b6 
  0x000000740753d560: 47fd fb7f | 0000 ffd0 | 4883 c420 | 488b 0424 | 4883 c410 | c5fb 1004 | 2448 83c4 | 104c 8b5d 
  0x000000740753d580: 1841 ffd3 | 4c8b 5df8 | c95f 498b | e3ff e7ba | 0000 0000 | e805 0000 | 00e9 9600 | 0000 488d 
  0x000000740753d5a0: 4424 084c | 896d c049 | 8bcf c5f8 | 7749 89af | b003 0000 | 4989 87a0 | 0300 0048 | 83ec 2040 
  0x000000740753d5c0: f6c4 0f0f | 8419 0000 | 0048 83ec | 0848 b8d0 | ad10 fdfb | 7f00 00ff | d048 83c4 | 08e9 0c00 
  0x000000740753d5e0: 0000 48b8 | d0ad 10fd | fb7f 0000 | ffd0 4883 | c420 49c7 | 87a0 0300 | 0000 0000 | 0049 c787 
  0x000000740753d600: b003 0000 | 0000 0000 | 49c7 87a8 | 0300 0000 | 0000 00c5 | f877 4983 | 7f08 000f | 8405 0000 
  0x000000740753d620: 00e9 da38 | ffff 4c8b | 6dc0 4c8b | 75c8 4e8d | 74f5 00c3 | 488b 5de8 | e95b f6ff | ff66 6690 
[/MachCode]

Compiled method (c2) 18841 7617       4       java.util.Optional::map (30 bytes)
 total in heap  [0x0000007407f14490,0x0000007407f14868] = 984
 relocation     [0x0000007407f145e8,0x0000007407f14618] = 48
 main code      [0x0000007407f14620,0x0000007407f14770] = 336
 stub code      [0x0000007407f14770,0x0000007407f14788] = 24
 metadata       [0x0000007407f14788,0x0000007407f147a8] = 32
 scopes data    [0x0000007407f147a8,0x0000007407f147e0] = 56
 scopes pcs     [0x0000007407f147e0,0x0000007407f14830] = 80
 dependencies   [0x0000007407f14830,0x0000007407f14838] = 8
 handler table  [0x0000007407f14838,0x0000007407f14868] = 48

[Constant Pool (empty)]

[MachCode]
[Entry Point]
  # {method} {0x000000740f0c38a8} 'map' '(Ljava/util/function/Function;)Ljava/util/Optional;' in 'java/util/Optional'
  # this:     rdx:rdx   = 'java/util/Optional'
  # parm0:    r8:r8     = 'java/util/function/Function'
  #           [sp+0x40]  (sp of caller)
  0x0000007407f14620: 448b 5208 | 49bb 0000 | 000f 7400 | 0000 4d03 | d349 3bc2 

  0x0000007407f14634: ;   {runtime_call ic_miss_stub}
  0x0000007407f14634: 0f85 46a1 | 66ff 6690 | 0f1f 4000 
[Verified Entry Point]
  0x0000007407f14640: 8984 2400 | 80ff ff55 | 4883 ec30 | 4181 7f20 | 1700 0000 | 0f85 0601 | 0000 4d8b | d84d 85c0 
  0x0000007407f14660: 0f84 b000 | 0000 448b | 520c 4585 

  0x0000007407f1466c: ;   {oop(a 'java/util/Optional'{0x00000000fff48e80})}
  0x0000007407f1466c: d275 0c48 | b880 8ef4 | ff00 0000 | 00eb 604d | 8bc2 498b | d348 b8d0 | ddaa 5a74 

  0x0000007407f14688: ;   {virtual_call}
  0x0000007407f14688: 0000 00e8 

  0x0000007407f1468c: ; ImmutableOopMap {}
                      ;*invokeinterface apply {reexecute=0 rethrow=0 return_oop=1}
                      ; - java.util.Optional::map@21 (line 260)
  0x0000007407f1468c: 708b 73ff 

  0x0000007407f14690: ;   {other}
  0x0000007407f14690: 0f1f 8400 | 0002 0000 | 488b e848 | 85c0 744e | 498b 87b8 | 0100 004c | 8bd0 4983 | c210 4d3b 
  0x0000007407f146b0: 97c8 0100 | 0073 434d | 8997 b801 | 0000 410f | 1882 c000 | 0000 48c7 | 0001 0000 

  0x0000007407f146cc: ;   {metadata('java/util/Optional')}
  0x0000007407f146cc: 00c7 4008 | c032 0c00 | 4c8b d544 | 8950 0c48 | 83c4 305d 

  0x0000007407f146e0: ;   {poll_return}
  0x0000007407f146e0: 493b a758 | 0400 000f | 875d 0000 

  0x0000007407f146ec: ;   {oop(a 'java/util/Optional'{0x00000000fff48e80})}
  0x0000007407f146ec: 00c3 48b8 | 808e f4ff | 0000 0000 

  0x0000007407f146f8: ;   {metadata('java/util/Optional')}
  0x0000007407f146f8: ebe1 48ba | c032 0c0f | 7400 0000 

  0x0000007407f14704: ;   {runtime_call _new_instance_Java}
  0x0000007407f14704: 6666 90e8 

  0x0000007407f14708: ; ImmutableOopMap {rbp=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=1}
                      ; - java.util.Optional::ofNullable@10 (line 128)
                      ; - java.util.Optional::map@26 (line 260)
  0x0000007407f14708: 7466 73ff 

  0x0000007407f1470c: ;   {other}
  0x0000007407f1470c: 0f1f 8400 | 7c02 0001 | ebbe 488b | ea4c 8944 | 2408 4c89 | 4424 10ba | 45ff ffff 

  0x0000007407f14728: ;   {runtime_call UncommonTrapBlob}
  0x0000007407f14728: 6666 90e8 

  0x0000007407f1472c: ; ImmutableOopMap {rbp=Oop [8]=Oop [16]=Oop }
                      ;*ifnonnull {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.util.Objects::requireNonNull@1 (line 219)
                      ; - java.util.Optional::map@1 (line 256)
  0x0000007407f1472c: d0fe 66ff 

  0x0000007407f14730: ;   {other}
  0x0000007407f14730: 0f1f 8400 | a002 0002 | 488b d0eb | 0348 8bd0 | 4883 c430 

  0x0000007407f14744: ;   {runtime_call _rethrow_Java}
  0x0000007407f14744: 5de9 3609 

  0x0000007407f14748: ;   {internal_word}
  0x0000007407f14748: 74ff 49ba | e046 f107 | 7400 0000 | 4d89 9770 

  0x0000007407f14758: ;   {runtime_call SafepointBlob}
  0x0000007407f14758: 0400 00e9 | a00f 67ff 

  0x0000007407f14760: ;   {runtime_call StubRoutines (final stubs)}
  0x0000007407f14760: e87b 0665 | ffe9 f0fe | ffff f4f4 | f4f4 f4f4 
[Exception Handler]
  0x0000007407f14770: ;   {no_reloc}
  0x0000007407f14770: e98b 6f73 | ffe8 0000 | 0000 4883 

  0x0000007407f1477c: ;   {runtime_call DeoptimizationBlob}
  0x0000007407f1477c: 2c24 05e9 | 1c02 67ff | f4f4 f4f4 
[/MachCode]


Compiled method (c1) 18844 8353   !   2       jdk.internal.reflect.DirectMethodHandleAccessor::invoke (92 bytes)
 total in heap  [0x0000007400c42890,0x0000007400c44a58] = 8648
 relocation     [0x0000007400c429e8,0x0000007400c42c18] = 560
 main code      [0x0000007400c42c20,0x0000007400c43778] = 2904
 stub code      [0x0000007400c43778,0x0000007400c438a8] = 304
 oops           [0x0000007400c438a8,0x0000007400c438b8] = 16
 metadata       [0x0000007400c438b8,0x0000007400c43918] = 96
 scopes data    [0x0000007400c43918,0x0000007400c43c38] = 800
 scopes pcs     [0x0000007400c43c38,0x0000007400c440b8] = 1152
 dependencies   [0x0000007400c440b8,0x0000007400c440c0] = 8
 handler table  [0x0000007400c440c0,0x0000007400c44990] = 2256
 nul chk table  [0x0000007400c44990,0x0000007400c44a58] = 200

[Constant Pool (empty)]

[MachCode]
[Entry Point]
  # {method} {0x000000740f158858} 'invoke' '(Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object;' in 'jdk/internal/reflect/DirectMethodHandleAccessor'
  # this:     rdx:rdx   = 'jdk/internal/reflect/DirectMethodHandleAccessor'
  # parm0:    r8:r8     = 'java/lang/Object'
  # parm1:    r9:r9     = '[Ljava/lang/Object;'
  #           [sp+0x170]  (sp of caller)
  0x0000007400c42c20: 448b 5208 | 49bb 0000 | 000f 7400 | 0000 4d03 | d34c 3bd0 

  0x0000007400c42c34: ;   {runtime_call ic_miss_stub}
  0x0000007400c42c34: 0f85 46bb | 9306 660f | 1f44 0000 
[Verified Entry Point]
  0x0000007400c42c40: 8984 2400 | 80ff ff55 | 4881 ec60 | 0100 0090 | 4181 7f20 | 1700 0000 

  0x0000007400c42c58: ;   {runtime_call StubRoutines (final stubs)}
  0x0000007400c42c58: 7405 e881 | 2192 0648 | 8994 24b0 | 0000 004c | 8984 24c0 | 0000 004c | 898c 24b8 | 0000 0048 
  0x0000007400c42c78: bef8 8f03 | 5174 0000 | 008b 7e08 | 83c7 0289 | 7e08 81e7 | fe0f 0000 | 85ff 0f84 | 8108 0000 
  0x0000007400c42c98: 8b72 1081 | e600 0200 | 0081 fe00 | 0200 00be | 0000 0000 | 7505 be01 | 0000 0083 | e601 85f6 
  0x0000007400c42cb8: 0f85 2600 | 0000 498b | f04c 8bc6 | 488b fa48 | 8bd7 0f1f 

  0x0000007400c42ccc: ;   {optimized virtual_call}
  0x0000007400c42ccc: 4400 00e8 

  0x0000007400c42cd0: ; ImmutableOopMap {[176]=Oop [184]=Oop [192]=Oop }
                      ;*invokevirtual checkReceiver {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@9 (line 99)
  0x0000007400c42cd0: 700b 0000 

  0x0000007400c42cd4: ;   {other}
  0x0000007400c42cd4: 0f1f 8400 | 4404 0000 | 488b 9424 | b000 0000 | 448b 420c | 498b d04c | 8b84 24b8 | 0000 000f 
  0x0000007400c42cf4: ;   {static_call}
  0x0000007400c42cf4: 1f40 00e8 

  0x0000007400c42cf8: ; ImmutableOopMap {[176]=Oop [184]=Oop [192]=Oop }
                      ;*invokestatic checkArgumentCount {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@17 (line 101)
  0x0000007400c42cf8: a4f5 ffff 

  0x0000007400c42cfc: ;   {other}
  0x0000007400c42cfc: 0f1f 8400 | 6c04 0001 | 488b 9424 | b000 0000 | 8b72 0c85 | f60f 84e2 | 0100 0083 | fe01 0f84 
  0x0000007400c42d1c: 7101 0000 | 83fe 020f | 84e8 0000 | 0083 fe03 | 0f84 4700 | 0000 8b72 | 1848 89b4 | 24c8 0000 
  0x0000007400c42d3c: 008b 7e10 

  0x0000007400c42d40: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff205f0} = (Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c42d40: 48bb f005 | f2ff 0000 | 0000 483b | fb0f 85f4 | 0300 008b | 7e14 8b7f | 1c48 85ff | 0f85 e802 
  0x0000007400c42d60: 0000 488b 

  0x0000007400c42d64: ;   {static_call}
  0x0000007400c42d64: d666 90e8 

  0x0000007400c42d68: ; ImmutableOopMap {[176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*invokestatic maybeCustomize {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkCustomized@19 (line 626)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42d68: 14c3 9306 

  0x0000007400c42d6c: ;   {other}
  0x0000007400c42d6c: 0f1f 8400 | dc04 0002 | e9d1 0200 | 004c 8b8c | 24b8 0000 | 008b 7218 | 4889 b424 | e800 0000 
  0x0000007400c42d8c: ; implicit exception: dispatches to 0x0000007400c43544
  0x0000007400c42d8c: 4183 790c | 000f 86b7 | 0700 0041 | 8b79 1048 | 89bc 24d0 | 0000 0041 | 8379 0c01 | 0f86 b207 
  0x0000007400c42dac: 0000 418b | 5914 4889 | 9c24 d800 | 0000 4183 | 790c 020f | 86ad 0700 | 0041 8b41 | 1848 8984 
  0x0000007400c42dcc: 24e0 0000 | 008b 4e10 

  0x0000007400c42dd4: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff20640} = (Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c42dd4: 49b8 4006 | f2ff 0000 | 0000 493b | c80f 8530 | 0300 008b | 4e14 8b49 | 1c48 85c9 | 0f85 0402 
  0x0000007400c42df4: 0000 488b | d666 0f1f 

  0x0000007400c42dfc: ;   {static_call}
  0x0000007400c42dfc: 4400 00e8 

  0x0000007400c42e00: ; ImmutableOopMap {[176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*invokestatic maybeCustomize {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkCustomized@19 (line 626)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@15
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42e00: 7cc2 9306 

  0x0000007400c42e04: ;   {other}
  0x0000007400c42e04: 0f1f 8400 | 7405 0003 | e9e9 0100 | 004c 8b8c | 24b8 0000 | 008b 7218 | 4889 b424 | 0001 0000 
  0x0000007400c42e24: ; implicit exception: dispatches to 0x0000007400c4358e
  0x0000007400c42e24: 4183 790c | 000f 8669 | 0700 0041 | 8b79 1048 | 89bc 24f0 | 0000 0041 | 8379 0c01 | 0f86 6407 
  0x0000007400c42e44: 0000 418b | 5914 4889 | 9c24 f800 | 0000 8b46 

  0x0000007400c42e54: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff20550} = (Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c42e54: 1048 b950 | 05f2 ff00 | 0000 0048 | 3bc1 0f85 | 7f02 0000 | 8b46 148b | 401c 4885 | c00f 853b 
  0x0000007400c42e74: 0100 0048 | 8bd6 0f1f 

  0x0000007400c42e7c: ;   {static_call}
  0x0000007400c42e7c: 4400 00e8 

  0x0000007400c42e80: ; ImmutableOopMap {[176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*invokestatic maybeCustomize {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkCustomized@19 (line 626)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@15
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42e80: fcc1 9306 

  0x0000007400c42e84: ;   {other}
  0x0000007400c42e84: 0f1f 8400 | f405 0004 | e921 0100 | 004c 8b8c | 24b8 0000 | 008b 7218 | 4889 b424 | 1001 0000 
  0x0000007400c42ea4: ; implicit exception: dispatches to 0x0000007400c435c6
  0x0000007400c42ea4: 4183 790c | 000f 8621 | 0700 0041 | 8b79 1048 | 89bc 2408 | 0100 008b 

  0x0000007400c42ebc: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff1ed18} = (Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c42ebc: 5e10 48b8 | 18ed f1ff | 0000 0000 | 483b d80f | 85e6 0100 | 008b 5e14 

  0x0000007400c42ed4: ; implicit exception: dispatches to 0x0000007400c435e7
  0x0000007400c42ed4: 8b5b 1c48 | 85db 0f85 | 9200 0000 | 488b d60f 

  0x0000007400c42ee4: ;   {static_call}
  0x0000007400c42ee4: 1f40 00e8 

  0x0000007400c42ee8: ; ImmutableOopMap {[176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*invokestatic maybeCustomize {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkCustomized@19 (line 626)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42ee8: b4dc f806 

  0x0000007400c42eec: ;   {other}
  0x0000007400c42eec: 0f1f 8400 | 5c06 0005 | e979 0000 | 008b 7218 | 4889 b424 | 1801 0000 

  0x0000007400c42f04: ; implicit exception: dispatches to 0x0000007400c435ec
                      ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff1ebe8} = (Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c42f04: 8b7e 1048 | bbe8 ebf1 | ff00 0000 | 0048 3bfb | 0f85 7001 | 0000 8b7e | 148b 7f1c | 4885 ff0f 
  0x0000007400c42f24: 8513 0000 | 0048 8bd6 

  0x0000007400c42f2c: ;   {static_call}
  0x0000007400c42f2c: 6666 90e8 

  0x0000007400c42f30: ; ImmutableOopMap {[176]=Oop [192]=Oop [280]=Oop }
                      ;*invokestatic maybeCustomize {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkCustomized@19 (line 626)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42f30: 6cdc f806 

  0x0000007400c42f34: ;   {other}
  0x0000007400c42f34: 0f1f 8400 | a406 0006 | 4c8b 8424 | c000 0000 | 488b 9424 | 1801 0000 

  0x0000007400c42f4c: ;   {optimized virtual_call}
  0x0000007400c42f4c: 6666 90e8 

  0x0000007400c42f50: ; ImmutableOopMap {[176]=Oop }
                      ;*invokevirtual invokeBasic {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@19
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42f50: 2c3e e906 

  0x0000007400c42f54: ;   {other}
  0x0000007400c42f54: 0f1f 8400 | c406 0007 | 4881 c460 | 0100 005d 

  0x0000007400c42f64: ;   {poll_return}
  0x0000007400c42f64: 493b a758 | 0400 000f | 8785 0600 | 00c3 4c8b | 8424 c000 | 0000 4c8b | 8c24 0801 | 0000 488b 
  0x0000007400c42f84: 9424 1001 | 0000 0f1f 

  0x0000007400c42f8c: ;   {optimized virtual_call}
  0x0000007400c42f8c: 4400 00e8 

  0x0000007400c42f90: ; ImmutableOopMap {[176]=Oop }
                      ;*invokevirtual invokeBasic {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@20
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42f90: ec31 e906 

  0x0000007400c42f94: ;   {other}
  0x0000007400c42f94: 0f1f 8400 | 0407 0008 | 4881 c460 | 0100 005d 

  0x0000007400c42fa4: ;   {poll_return}
  0x0000007400c42fa4: 493b a758 | 0400 000f | 875b 0600 | 00c3 4c8b | 8424 c000 | 0000 4c8b | 8c24 f000 | 0000 488b 
  0x0000007400c42fc4: bc24 f800 | 0000 488b | 9424 0001 | 0000 0f1f 

  0x0000007400c42fd4: ;   {optimized virtual_call}
  0x0000007400c42fd4: 4400 00e8 

  0x0000007400c42fd8: ; ImmutableOopMap {[176]=Oop }
                      ;*invokevirtual invokeBasic {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@22
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c42fd8: a4ba 9306 

  0x0000007400c42fdc: ;   {other}
  0x0000007400c42fdc: 0f1f 8400 | 4c07 0009 | 4881 c460 | 0100 005d 

  0x0000007400c42fec: ;   {poll_return}
  0x0000007400c42fec: 493b a758 | 0400 000f | 8729 0600 | 00c3 4c8b | 8424 c000 | 0000 4c8b | 8c24 d000 | 0000 488b 
  0x0000007400c4300c: bc24 d800 | 0000 488b | b424 e000 | 0000 488b | 9424 e800 | 0000 0f1f 

  0x0000007400c43024: ;   {optimized virtual_call}
  0x0000007400c43024: 4400 00e8 

  0x0000007400c43028: ; ImmutableOopMap {[176]=Oop }
                      ;*invokevirtual invokeBasic {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@24
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43028: 54ba 9306 

  0x0000007400c4302c: ;   {other}
  0x0000007400c4302c: 0f1f 8400 | 9c07 000a | 4881 c460 | 0100 005d 

  0x0000007400c4303c: ;   {poll_return}
  0x0000007400c4303c: 493b a758 | 0400 000f | 87ef 0500 | 00c3 4c8b | 8c24 b800 | 0000 4c8b | 8424 c000 | 0000 488b 
  0x0000007400c4305c: 9424 c800 | 0000 0f1f 

  0x0000007400c43064: ;   {optimized virtual_call}
  0x0000007400c43064: 4400 00e8 

  0x0000007400c43068: ; ImmutableOopMap {[176]=Oop }
                      ;*invokevirtual invokeBasic {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@20
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43068: 14ba 9306 

  0x0000007400c4306c: ;   {other}
  0x0000007400c4306c: 0f1f 8400 | dc07 000b | 4881 c460 | 0100 005d 

  0x0000007400c4307c: ;   {poll_return}
  0x0000007400c4307c: 493b a758 | 0400 000f | 87c5 0500 

  0x0000007400c43088: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff1ebe8} = (Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c43088: 00c3 49b8 | e8eb f1ff | 0000 0000 

  0x0000007400c43094: ;   {static_call}
  0x0000007400c43094: 488b d7e8 

  0x0000007400c43098: ; ImmutableOopMap {[176]=Oop [192]=Oop [280]=Oop }
                      ;*invokestatic newWrongMethodTypeException {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@12 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43098: e4bf 9306 

  0x0000007400c4309c: ;   {other}
  0x0000007400c4309c: 0f1f 8400 | 0c08 000c 

  0x0000007400c430a4: ; implicit exception: dispatches to 0x0000007400c43664
                      ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [280]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {section_word}
  0x0000007400c430a4: 483b 0048 | baa7 30c4 | 0074 0000 

  0x0000007400c430b0: ;   {runtime_call handle_exception_nofpu Runtime1 stub}
  0x0000007400c430b0: 00e8 ca09 

  0x0000007400c430b4: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff1ed18} = (Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c430b4: a006 9049 | b818 edf1 | ff00 0000 | 0048 8bd3 

  0x0000007400c430c4: ;   {static_call}
  0x0000007400c430c4: 6666 90e8 

  0x0000007400c430c8: ; ImmutableOopMap {[176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*invokestatic newWrongMethodTypeException {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@12 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c430c8: b4bf 9306 

  0x0000007400c430cc: ;   {other}
  0x0000007400c430cc: 0f1f 8400 | 3c08 000e 

  0x0000007400c430d4: ; implicit exception: dispatches to 0x0000007400c43669
                      ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {section_word}
  0x0000007400c430d4: 483b 0048 | bad7 30c4 | 0074 0000 

  0x0000007400c430e0: ;   {runtime_call handle_exception_nofpu Runtime1 stub}
  0x0000007400c430e0: 00e8 9a09 

  0x0000007400c430e4: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff20550} = (Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c430e4: a006 9049 | b850 05f2 | ff00 0000 | 0048 8bd0 

  0x0000007400c430f4: ;   {static_call}
  0x0000007400c430f4: 6666 90e8 

  0x0000007400c430f8: ; ImmutableOopMap {[176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*invokestatic newWrongMethodTypeException {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@12 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c430f8: 84bf 9306 

  0x0000007400c430fc: ;   {other}
  0x0000007400c430fc: 0f1f 8400 | 6c08 0010 

  0x0000007400c43104: ; implicit exception: dispatches to 0x0000007400c4366e
                      ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {section_word}
  0x0000007400c43104: 483b 0048 | ba07 31c4 | 0074 0000 

  0x0000007400c43110: ;   {runtime_call handle_exception_nofpu Runtime1 stub}
  0x0000007400c43110: 00e8 6a09 

  0x0000007400c43114: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff20640} = (Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c43114: a006 9049 | b840 06f2 | ff00 0000 | 0048 8bd1 

  0x0000007400c43124: ;   {static_call}
  0x0000007400c43124: 6666 90e8 

  0x0000007400c43128: ; ImmutableOopMap {[176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*invokestatic newWrongMethodTypeException {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@12 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43128: 54bf 9306 

  0x0000007400c4312c: ;   {other}
  0x0000007400c4312c: 0f1f 8400 | 9c08 0012 

  0x0000007400c43134: ; implicit exception: dispatches to 0x0000007400c43673
                      ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {section_word}
  0x0000007400c43134: 483b 0048 | ba37 31c4 | 0074 0000 

  0x0000007400c43140: ;   {runtime_call handle_exception_nofpu Runtime1 stub}
  0x0000007400c43140: 00e8 3a09 

  0x0000007400c43144: ;   {oop(a 'java/lang/invoke/MethodType'{0x00000000fff205f0} = (Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object;)}
  0x0000007400c43144: a006 9048 | bbf0 05f2 | ff00 0000 | 0048 8bd7 

  0x0000007400c43154: ;   {static_call}
  0x0000007400c43154: 4c8b c3e8 

  0x0000007400c43158: ; ImmutableOopMap {[176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*invokestatic newWrongMethodTypeException {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@12 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43158: 24bf 9306 

  0x0000007400c4315c: ;   {other}
  0x0000007400c4315c: 0f1f 8400 | cc08 0014 

  0x0000007400c43164: ; implicit exception: dispatches to 0x0000007400c43678
                      ; ImmutableOopMap {rax=Oop [176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {section_word}
  0x0000007400c43164: 483b 0048 | ba67 31c4 | 0074 0000 

  0x0000007400c43170: ;   {runtime_call handle_exception_nofpu Runtime1 stub}
  0x0000007400c43170: 00e8 0a09 | a006 9049 | 8b87 0805 | 0000 4d33 | d24d 8997 | 0805 0000 | 4d33 d24d | 8997 1005 
  0x0000007400c43190: ;   {oop(a 'java/lang/Class'{0x00000000ff64dd68} = 'jdk/internal/reflect/DirectMethodHandleAccessor')}
  0x0000007400c43190: 0000 48ba | 68dd 64ff | 0000 0000 | 4c8b c048 | 8984 2420 

  0x0000007400c431a4: ;   {static_call}
  0x0000007400c431a4: 0100 00e8 

  0x0000007400c431a8: ; ImmutableOopMap {[288]=Oop }
                      ;*invokestatic isIllegalArgument {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::isIllegalArgument@3 (line 191)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@58 (line 112)
  0x0000007400c431a8: d4be 9306 

  0x0000007400c431ac: ;   {other}
  0x0000007400c431ac: 0f1f 8400 | 1c09 0016 | 83e0 0185 | c00f 840a | 0200 00e9 | 7501 0000 | 498b 8708 | 0500 004d 
  0x0000007400c431cc: 33d2 4d89 | 9708 0500 | 004d 33d2 | 4d89 9710 

  0x0000007400c431dc: ;   {oop(a 'java/lang/Class'{0x00000000ff64dd68} = 'jdk/internal/reflect/DirectMethodHandleAccessor')}
  0x0000007400c431dc: 0500 0048 | ba68 dd64 | ff00 0000 | 004c 8bc0 | 4889 8424 | 2801 0000 

  0x0000007400c431f4: ;   {static_call}
  0x0000007400c431f4: 6666 90e8 

  0x0000007400c431f8: ; ImmutableOopMap {[296]=Oop }
                      ;*invokestatic isIllegalArgument {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::isIllegalArgument@3 (line 191)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@30 (line 105)
  0x0000007400c431f8: 84be 9306 

  0x0000007400c431fc: ;   {other}
  0x0000007400c431fc: 0f1f 8400 | 6c09 0017 | 83e0 0185 | c00f 848a | 0000 0090 

  0x0000007400c43210: ;   {no_reloc}
  0x0000007400c43210: e977 0400 | 0000 0000 | 0000 498b | 87b8 0100 | 0048 8d78 | 2849 3bbf | c801 0000 | 0f87 6404 
  0x0000007400c43230: 0000 4989 | bfb8 0100 | 0048 c700 | 0100 0000 | 488b ca49 | ba00 0000 | 0f74 0000 | 0049 2bca 
  0x0000007400c43250: 8948 0848 | 33c9 8948 | 0c48 33c9 | 4889 4810 | 4889 4818 | 4889 4820 

  0x0000007400c43268: ;   {oop("argument type mismatch"{0x00000000ffd86050})}
  0x0000007400c43268: 49b8 5060 | d8ff 0000 | 0000 488b | d048 8984 | 2430 0100 

  0x0000007400c4327c: ;   {optimized virtual_call}
  0x0000007400c4327c: 0066 90e8 

  0x0000007400c43280: ; ImmutableOopMap {[304]=Oop }
                      ;*invokespecial <init> {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@42 (line 107)
  0x0000007400c43280: fcb7 9306 

  0x0000007400c43284: ;   {other}
  0x0000007400c43284: 0f1f 8400 | f409 0018 | 488b 8424 | 3001 0000 | e9ce 0400 | 004c 8b84 | 2428 0100 | 000f 1f80 
  0x0000007400c432a4: 0000 0000 

  0x0000007400c432a8: ;   {no_reloc}
  0x0000007400c432a8: e905 0400 | 0000 0000 | 0000 80ba | 2001 0000 | 050f 8502 | 0400 0049 | 8b87 b801 | 0000 488d 
  0x0000007400c432c8: 7828 493b | bfc8 0100 | 000f 87ea | 0300 0049 | 89bf b801 | 0000 48c7 | 0001 0000 | 0048 8bca 
  0x0000007400c432e8: 49ba 0000 | 000f 7400 | 0000 492b | ca89 4808 | 4833 c989 | 480c 4833 | c948 8948 | 1048 8948 
  0x0000007400c43308: 1848 8948 | 2048 8bd0 | 4889 8424 | 3801 0000 | 0f1f 8000 

  0x0000007400c4331c: ;   {optimized virtual_call}
  0x0000007400c4331c: 0000 00e8 

  0x0000007400c43320: ; ImmutableOopMap {[312]=Oop }
                      ;*invokespecial <init> {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@51 (line 109)
  0x0000007400c43320: 5cb7 9306 

  0x0000007400c43324: ;   {other}
  0x0000007400c43324: 0f1f 8400 | 940a 0019 | 488b 8424 | 3801 0000 | e92e 0400 | 000f 1f80 | 0000 0000 

  0x0000007400c43340: ;   {no_reloc}
  0x0000007400c43340: e998 0300 | 0000 0000 | 0000 498b | 87b8 0100 | 0048 8d78 | 2849 3bbf | c801 0000 | 0f87 8503 
  0x0000007400c43360: 0000 4989 | bfb8 0100 | 0048 c700 | 0100 0000 | 488b ca49 | ba00 0000 | 0f74 0000 | 0049 2bca 
  0x0000007400c43380: 8948 0848 | 33c9 8948 | 0c48 33c9 | 4889 4810 | 4889 4818 | 4889 4820 | 4c8b 8424 | 2001 0000 
  0x0000007400c433a0: 488b d048 | 8984 2440 | 0100 000f 

  0x0000007400c433ac: ;   {optimized virtual_call}
  0x0000007400c433ac: 1f40 00e8 

  0x0000007400c433b0: ; ImmutableOopMap {[320]=Oop }
                      ;*invokespecial <init> {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@69 (line 113)
  0x0000007400c433b0: ccb6 9306 

  0x0000007400c433b4: ;   {other}
  0x0000007400c433b4: 0f1f 8400 | 240b 001a | 488b 8424 | 4001 0000 | e99e 0300 | 004c 8b84 | 2420 0100 | 000f 1f80 
  0x0000007400c433d4: 0000 0000 

  0x0000007400c433d8: ;   {no_reloc}
  0x0000007400c433d8: e926 0300 | 0000 0000 | 0000 80ba | 2001 0000 | 050f 8523 | 0300 0049 | 8b87 b801 | 0000 488d 
  0x0000007400c433f8: 7828 493b | bfc8 0100 | 000f 870b | 0300 0049 | 89bf b801 | 0000 48c7 | 0001 0000 | 0048 8bca 
  0x0000007400c43418: 49ba 0000 | 000f 7400 | 0000 492b | ca89 4808 | 4833 c989 | 480c 4833 | c948 8948 | 1048 8948 
  0x0000007400c43438: 1848 8948 | 2048 8bd0 | 4889 8424 | 4801 0000 | 0f1f 8000 

  0x0000007400c4344c: ;   {optimized virtual_call}
  0x0000007400c4344c: 0000 00e8 

  0x0000007400c43450: ; ImmutableOopMap {[328]=Oop }
                      ;*invokespecial <init> {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@78 (line 115)
  0x0000007400c43450: 2cb6 9306 

  0x0000007400c43454: ;   {other}
  0x0000007400c43454: 0f1f 8400 | c40b 001b | 488b 8424 | 4801 0000 | e9fe 0200 | 0049 8b87 | 0805 0000 | 4d33 d24d 
  0x0000007400c43474: 8997 0805 | 0000 4d33 | d24d 8997 | 1005 0000 | 4c8b c090 

  0x0000007400c43488: ;   {no_reloc}
  0x0000007400c43488: e9a1 0200 | 0000 0000 | 0000 80ba | 2001 0000 | 050f 859e | 0200 0049 | 8b87 b801 | 0000 488d 
  0x0000007400c434a8: 7828 493b | bfc8 0100 | 000f 8786 | 0200 0049 | 89bf b801 | 0000 48c7 | 0001 0000 | 0048 8bca 
  0x0000007400c434c8: 49ba 0000 | 000f 7400 | 0000 492b | ca89 4808 | 4833 c989 | 480c 4833 | c948 8948 | 1048 8948 
  0x0000007400c434e8: 1848 8948 | 2048 8bd0 | 4889 8424 | 5001 0000 | 0f1f 8000 

  0x0000007400c434fc: ;   {optimized virtual_call}
  0x0000007400c434fc: 0000 00e8 

  0x0000007400c43500: ; ImmutableOopMap {[336]=Oop }
                      ;*invokespecial <init> {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@88 (line 118)
  0x0000007400c43500: 7cb5 9306 

  0x0000007400c43504: ;   {other}
  0x0000007400c43504: 0f1f 8400 | 740c 001c | 488b 8424 | 5001 0000 | e94e 0200 

  0x0000007400c43518: ;   {metadata({method} {0x000000740f158858} 'invoke' '(Ljava/lang/Object;[Ljava/lang/Object;)Ljava/lang/Object;' in 'jdk/internal/reflect/DirectMethodHandleAccessor')}
  0x0000007400c43518: 0049 ba50 | 8815 0f74 | 0000 004c | 8954 2408 | 48c7 0424 | ffff ffff 

  0x0000007400c43530: ;   {runtime_call counter_overflow Runtime1 stub}
  0x0000007400c43530: e84b 63a0 

  0x0000007400c43534: ; ImmutableOopMap {rdx=Oop r8=Oop r9=Oop [176]=Oop [184]=Oop [192]=Oop }
                      ;*synchronization entry
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@-1 (line 98)
  0x0000007400c43534: 06e9 5ef7 

  0x0000007400c43538: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43538: ffff e8c1 

  0x0000007400c4353c: ; ImmutableOopMap {rdx=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*invokevirtual type {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@1 (line 528)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c4353c: e39f 06e8 

  0x0000007400c43540: ; ImmutableOopMap {rdx=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*getfield customized {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkCustomized@12 (line 625)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43540: bce3 9f06 

  0x0000007400c43544: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43544: e8b7 e39f 

  0x0000007400c43548: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [232]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@85 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43548: 06e8 b2e3 

  0x0000007400c4354c: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [232]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@85 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c4354c: 9f06 48c7 | 0424 0000 | 0000 4c89 

  0x0000007400c43558: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c43558: 4c24 08e8 

  0x0000007400c4355c: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [232]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@85 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c4355c: a0da 9f06 | 48c7 0424 | 0100 0000 | 4c89 4c24 

  0x0000007400c4356c: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c4356c: 08e8 8eda 

  0x0000007400c43570: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop rdi=Oop [176]=Oop [184]=Oop [192]=Oop [208]=Oop [232]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@88 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43570: 9f06 48c7 | 0424 0200 | 0000 4c89 

  0x0000007400c4357c: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c4357c: 4c24 08e8 

  0x0000007400c43580: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop rdi=Oop rbx=Oop [176]=Oop [184]=Oop [192]=Oop [208]=Oop [216]=Oop [232]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@91 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43580: 7cda 9f06 

  0x0000007400c43584: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43584: e877 e39f 

  0x0000007400c43588: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop rbx=Oop rax=Oop [176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*invokevirtual type {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@1 (line 528)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43588: 06e8 72e3 

  0x0000007400c4358c: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop rbx=Oop rax=Oop [176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*getfield customized {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkCustomized@12 (line 625)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@15
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c4358c: 9f06 e86d 

  0x0000007400c43590: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [256]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@68 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43590: e39f 06e8 

  0x0000007400c43594: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [256]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@68 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43594: 68e3 9f06 | 48c7 0424 | 0000 0000 | 4c89 4c24 

  0x0000007400c435a4: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c435a4: 08e8 56da 

  0x0000007400c435a8: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [256]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@68 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c435a8: 9f06 48c7 | 0424 0100 | 0000 4c89 

  0x0000007400c435b4: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c435b4: 4c24 08e8 

  0x0000007400c435b8: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop rdi=Oop [176]=Oop [184]=Oop [192]=Oop [240]=Oop [256]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@71 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c435b8: 44da 9f06 

  0x0000007400c435bc: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435bc: e83f e39f 

  0x0000007400c435c0: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop rbx=Oop [176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*invokevirtual type {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@1 (line 528)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435c0: 06e8 3ae3 

  0x0000007400c435c4: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop rbx=Oop [176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*getfield customized {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkCustomized@12 (line 625)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@15
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435c4: 9f06 e835 

  0x0000007400c435c8: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [272]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@54 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435c8: e39f 06e8 

  0x0000007400c435cc: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [272]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@54 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c435cc: 30e3 9f06 | 48c7 0424 | 0000 0000 | 4c89 4c24 

  0x0000007400c435dc: ;   {runtime_call throw_range_check_failed Runtime1 stub}
  0x0000007400c435dc: 08e8 1eda 

  0x0000007400c435e0: ; ImmutableOopMap {rdx=Oop r9=Oop rsi=Oop [176]=Oop [184]=Oop [192]=Oop [272]=Oop }
                      ;*aaload {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@54 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435e0: 9f06 e819 

  0x0000007400c435e4: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop [176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*invokevirtual type {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@1 (line 528)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435e4: e39f 06e8 

  0x0000007400c435e8: ; ImmutableOopMap {rdx=Oop rsi=Oop rdi=Oop [176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*getfield customized {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkCustomized@12 (line 625)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c435e8: 14e3 9f06 

  0x0000007400c435ec: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435ec: e80f e39f 

  0x0000007400c435f0: ; ImmutableOopMap {rdx=Oop rsi=Oop [176]=Oop [192]=Oop [280]=Oop }
                      ;*invokevirtual type {reexecute=0 rethrow=0 return_oop=0}
                      ; - java.lang.invoke.Invokers::checkExactType@1 (line 528)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c435f0: 06e8 0ae3 

  0x0000007400c435f4: ; ImmutableOopMap {rdx=Oop rsi=Oop [176]=Oop [192]=Oop [280]=Oop }
                      ;*getfield customized {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkCustomized@12 (line 625)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@14
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {internal_word}
  0x0000007400c435f4: 9f06 49ba | 642f c400 | 7400 0000 | 4d89 9770 

  0x0000007400c43604: ;   {runtime_call SafepointBlob}
  0x0000007400c43604: 0400 00e9 | f420 9406 

  0x0000007400c4360c: ;   {internal_word}
  0x0000007400c4360c: 49ba a42f | c400 7400 | 0000 4d89 | 9770 0400 

  0x0000007400c4361c: ;   {runtime_call SafepointBlob}
  0x0000007400c4361c: 00e9 de20 

  0x0000007400c43620: ;   {internal_word}
  0x0000007400c43620: 9406 49ba | ec2f c400 | 7400 0000 | 4d89 9770 

  0x0000007400c43630: ;   {runtime_call SafepointBlob}
  0x0000007400c43630: 0400 00e9 | c820 9406 

  0x0000007400c43638: ;   {internal_word}
  0x0000007400c43638: 49ba 3c30 | c400 7400 | 0000 4d89 | 9770 0400 

  0x0000007400c43648: ;   {runtime_call SafepointBlob}
  0x0000007400c43648: 00e9 b220 

  0x0000007400c4364c: ;   {internal_word}
  0x0000007400c4364c: 9406 49ba | 7c30 c400 | 7400 0000 | 4d89 9770 

  0x0000007400c4365c: ;   {runtime_call SafepointBlob}
  0x0000007400c4365c: 0400 00e9 | 9c20 9406 

  0x0000007400c43664: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43664: e897 e29f 

  0x0000007400c43668: ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [280]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@41 (line 153)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43668: 06e8 92e2 

  0x0000007400c4366c: ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [264]=Oop [272]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@55 (line 154)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c4366c: 9f06 e88d 

  0x0000007400c43670: ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [240]=Oop [248]=Oop [256]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x00000074100d4c00::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@72 (line 155)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43670: e29f 06e8 

  0x0000007400c43674: ; ImmutableOopMap {rax=Oop [176]=Oop [192]=Oop [208]=Oop [216]=Oop [224]=Oop [232]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.LambdaForm$MH/0x0000007410161800::invokeExact_MT@11
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@92 (line 156)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
  0x0000007400c43674: 88e2 9f06 

  0x0000007400c43678: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43678: e883 e29f 

  0x0000007400c4367c: ; ImmutableOopMap {rax=Oop [176]=Oop [184]=Oop [192]=Oop [200]=Oop }
                      ;*athrow {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) java.lang.invoke.Invokers::checkExactType@15 (line 530)
                      ; - java.lang.invoke.Invokers$Holder::invokeExact_MT@10
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invokeImpl@104 (line 157)
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@23 (line 103)
                      ;   {metadata(nullptr)}
  0x0000007400c4367c: 0648 ba00 | 0000 0000 | 0000 00b8 | 000f 050a 

  0x0000007400c4368c: ;   {runtime_call load_klass_patching Runtime1 stub}
  0x0000007400c4368c: e8ef 47a0 

  0x0000007400c43690: ; ImmutableOopMap {}
                      ;*new {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) jdk.internal.reflect.DirectMethodHandleAccessor::invoke@36 (line 107)
  0x0000007400c43690: 06e9 7afb | ffff 488b 

  0x0000007400c43698: ;   {runtime_call fast_new_instance Runtime1 stub}
  0x0000007400c43698: d2e8 62eb 

  0x0000007400c4369c: ; ImmutableOopMap {}
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@36 (line 107)
  0x0000007400c4369c: 9f06 e9c5 

  0x0000007400c436a0: ;   {metadata(nullptr)}
  0x0000007400c436a0: fbff ff48 | ba00 0000 | 0000 0000 | 00b8 000f 

  0x0000007400c436b0: ;   {runtime_call load_klass_patching Runtime1 stub}
  0x0000007400c436b0: 050a e8c9 

  0x0000007400c436b4: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) jdk.internal.reflect.DirectMethodHandleAccessor::invoke@46 (line 109)
  0x0000007400c436b4: 47a0 06e9 | ecfb ffff 

  0x0000007400c436bc: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c436bc: e83f e29f 

  0x0000007400c436c0: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@46 (line 109)
  0x0000007400c436c0: 0648 8bd2 

  0x0000007400c436c4: ;   {runtime_call fast_new_instance_init_check Runtime1 stub}
  0x0000007400c436c4: e837 f39f 

  0x0000007400c436c8: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@46 (line 109)
  0x0000007400c436c8: 06e9 3ffc 

  0x0000007400c436cc: ;   {metadata(nullptr)}
  0x0000007400c436cc: ffff 48ba | 0000 0000 | 0000 0000 | b800 0f05 

  0x0000007400c436dc: ;   {runtime_call load_klass_patching Runtime1 stub}
  0x0000007400c436dc: 0ae8 9e47 

  0x0000007400c436e0: ; ImmutableOopMap {[288]=Oop }
                      ;*new {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) jdk.internal.reflect.DirectMethodHandleAccessor::invoke@64 (line 113)
  0x0000007400c436e0: a006 e959 | fcff ff48 

  0x0000007400c436e8: ;   {runtime_call fast_new_instance Runtime1 stub}
  0x0000007400c436e8: 8bd2 e811 

  0x0000007400c436ec: ; ImmutableOopMap {[288]=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@64 (line 113)
  0x0000007400c436ec: eb9f 06e9 | a4fc ffff 

  0x0000007400c436f4: ;   {metadata(nullptr)}
  0x0000007400c436f4: 48ba 0000 | 0000 0000 | 0000 b800 

  0x0000007400c43700: ;   {runtime_call load_klass_patching Runtime1 stub}
  0x0000007400c43700: 0f05 0ae8 

  0x0000007400c43704: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) jdk.internal.reflect.DirectMethodHandleAccessor::invoke@73 (line 115)
  0x0000007400c43704: 7847 a006 | e9cb fcff 

  0x0000007400c4370c: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c4370c: ffe8 eee1 

  0x0000007400c43710: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@73 (line 115)
  0x0000007400c43710: 9f06 488b 

  0x0000007400c43714: ;   {runtime_call fast_new_instance_init_check Runtime1 stub}
  0x0000007400c43714: d2e8 e6f2 

  0x0000007400c43718: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@73 (line 115)
  0x0000007400c43718: 9f06 e91e 

  0x0000007400c4371c: ;   {metadata(nullptr)}
  0x0000007400c4371c: fdff ff48 | ba00 0000 | 0000 0000 | 00b8 000f 

  0x0000007400c4372c: ;   {runtime_call load_klass_patching Runtime1 stub}
  0x0000007400c4372c: 050a e84d 

  0x0000007400c43730: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=1 rethrow=0 return_oop=0}
                      ; - (reexecute) jdk.internal.reflect.DirectMethodHandleAccessor::invoke@83 (line 118)
  0x0000007400c43730: 47a0 06e9 | 50fd ffff 

  0x0000007400c43738: ;   {runtime_call throw_null_pointer_exception Runtime1 stub}
  0x0000007400c43738: e8c3 e19f 

  0x0000007400c4373c: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@83 (line 118)
  0x0000007400c4373c: 0648 8bd2 

  0x0000007400c43740: ;   {runtime_call fast_new_instance_init_check Runtime1 stub}
  0x0000007400c43740: e8bb f29f 

  0x0000007400c43744: ; ImmutableOopMap {r8=Oop }
                      ;*new {reexecute=0 rethrow=0 return_oop=0}
                      ; - jdk.internal.reflect.DirectMethodHandleAccessor::invoke@83 (line 118)
  0x0000007400c43744: 06e9 a3fd | ffff 498b | 8708 0500 | 0049 c787 | 0805 0000 | 0000 0000 | 49c7 8710 | 0500 0000 
  0x0000007400c43764: 0000 0048 | 81c4 6001 

  0x0000007400c4376c: ;   {runtime_call unwind_exception Runtime1 stub}
  0x0000007400c4376c: 0000 5de9 | 8cd2 9f06 | f4f4 f4f4 
[Stub Code]
  0x0000007400c43778: ;   {no_reloc}
  0x0000007400c43778: 0f1f 4400 

  0x0000007400c4377c: ;   {static_stub}
  0x0000007400c4377c: 0048 bb00 | 0000 0000 

  0x0000007400c43784: ;   {runtime_call}
  0x0000007400c43784: 0000 00e9 | fbff ffff 

  0x0000007400c4378c: ;   {static_stub}
  0x0000007400c4378c: 9048 bb00 | 0000 0000 

  0x0000007400c43794: ;   {runtime_call}
  0x0000007400c43794: 0000 00e9 | fbff ffff 

  0x0000007400c4379c: ;   {static_stub}
  0x0000007400c4379c: 9048 bb00 | 0000 0000 

  0x0000007400c437a4: ;   {runtime_call}
  0x0000007400c437a4: 0000 00e9 | fbff ffff 

  0x0000007400c437ac: ;   {static_stub}
  0x0000007400c437ac: 9048 bb00 | 0000 0000 

  0x0000007400c437b4: ;   {runtime_call}
  0x0000007400c437b4: 0000 00e9 | fbff ffff 

  0x0000007400c437bc: ;   {static_stub}
  0x0000007400c437bc: 9048 bb00 | 0000 0000 

  0x0000007400c437c4: ;   {runtime_call}
  0x0000007400c437c4: 0000 00e9 | fbff ffff 

  0x0000007400c437cc: ;   {static_stub}
  0x0000007400c437cc: 48bb 0000 | 0000 0000 

  0x0000007400c437d4: ;   {runtime_call}
  0x0000007400c437d4: 0000 e9fb 

  0x0000007400c437d8: ;   {static_stub}
  0x0000007400c437d8: ffff ff48 | bb00 0000 | 0000 0000 

  0x0000007400c437e4: ;   {runtime_call}
  0x0000007400c437e4: 00e9 fbff 

  0x0000007400c437e8: ;   {static_stub}
  0x0000007400c437e8: ffff 48bb | 0000 0000 | 0000 0000 

  0x0000007400c437f4: ;   {runtime_call}
  0x0000007400c437f4: e9fb ffff 

  0x0000007400c437f8: ;   {static_stub}
  0x0000007400c437f8: ff48 bb00 | 0000 0000 

  0x0000007400c43800: ;   {runtime_call}
  0x0000007400c43800: 0000 00e9 | fbff ffff 

  0x0000007400c43808: ;   {static_stub}
  0x0000007400c43808: 48bb 0000 | 0000 0000 

  0x0000007400c43810: ;   {runtime_call}
  0x0000007400c43810: 0000 e9fb 

  0x0000007400c43814: ;   {static_stub}
  0x0000007400c43814: ffff ff48 | bb00 0000 | 0000 0000 

  0x0000007400c43820: ;   {runtime_call}
  0x0000007400c43820: 00e9 fbff 

  0x0000007400c43824: ;   {static_stub}
  0x0000007400c43824: ffff 48bb | 0000 0000 | 0000 0000 

  0x0000007400c43830: ;   {runtime_call}
  0x0000007400c43830: e9fb ffff 

  0x0000007400c43834: ;   {static_stub}
  0x0000007400c43834: ff48 bb00 | 0000 0000 

  0x0000007400c4383c: ;   {runtime_call}
  0x0000007400c4383c: 0000 00e9 | fbff ffff 

  0x0000007400c43844: ;   {static_stub}
  0x0000007400c43844: 48bb b0aa | 360f 7400 

  0x0000007400c4384c: ;   {runtime_call I2C/C2I adapters}
  0x0000007400c4384c: 0000 e994 

  0x0000007400c43850: ;   {static_stub}
  0x0000007400c43850: 0994 0648 | bb00 0000 | 0000 0000 

  0x0000007400c4385c: ;   {runtime_call}
  0x0000007400c4385c: 00e9 fbff 

  0x0000007400c43860: ;   {runtime_call handle_exception_from_callee Runtime1 stub}
  0x0000007400c43860: ffff e819 

  0x0000007400c43864: ;   {external_word}
  0x0000007400c43864: 08a0 0648 | b9c0 286f | fdfb 7f00 | 0048 83e4 

  0x0000007400c43874: ;   {runtime_call}
  0x0000007400c43874: f048 b890 | 9536 fdfb | 7f00 00ff 

  0x0000007400c43880: ;   {section_word}
  0x0000007400c43880: d0f4 49ba | 8238 c400 | 7400 0000 

  0x0000007400c4388c: ;   {runtime_call DeoptimizationBlob}
  0x0000007400c4388c: 4152 e90d 

  0x0000007400c43890: ;   {section_word}
  0x0000007400c43890: 1194 0649 | ba93 38c4 | 0074 0000 

  0x0000007400c4389c: ;   {runtime_call DeoptimizationBlob}
  0x0000007400c4389c: 0041 52e9 | fc10 9406 | f4f4 f4f4 
[/MachCode]


---------------  P R O C E S S  ---------------

Threads class SMR info:
_java_thread_list=0x000000745b09a6e0, length=32, elements={
0x000000745014c850, 0x000000745014da20, 0x00000074501538a0, 0x0000007450159f40,
0x000000745015b620, 0x0000007450169180, 0x000000745016a3f0, 0x000000745016b380,
0x00000074550a7b10, 0x00000074550ac9a0, 0x0000007457a374f0, 0x000000746a8efd60,
0x0000007455e7c6d0, 0x00000074562824e0, 0x00000074562a3ac0, 0x00000074562a3430,
0x000000745a9760c0, 0x000000745a978190, 0x000000745a979540, 0x000000745a977470,
0x000000745a978820, 0x00000074562a4150, 0x00000074562a2710, 0x00000074562a47e0,
0x000000745a924f90, 0x000000745a922830, 0x000000745a923550, 0x000000745a9221a0,
0x000000745a924270, 0x000000745828bf10, 0x000000745a927060, 0x000000745a9269d0
}

Java Threads: ( => current thread )
  0x000000745014c850 JavaThread "Reference Handler"          daemon [_thread_blocked, id=5480, stack(0x00000074504f0000,0x00000074505f0000) (1024K)]
  0x000000745014da20 JavaThread "Finalizer"                  daemon [_thread_blocked, id=5008, stack(0x00000074505f0000,0x00000074506f0000) (1024K)]
  0x00000074501538a0 JavaThread "Signal Dispatcher"          daemon [_thread_blocked, id=6460, stack(0x00000074506f0000,0x00000074507f0000) (1024K)]
  0x0000007450159f40 JavaThread "Attach Listener"            daemon [_thread_blocked, id=7768, stack(0x00000074507f0000,0x00000074508f0000) (1024K)]
  0x000000745015b620 JavaThread "Service Thread"             daemon [_thread_blocked, id=2068, stack(0x00000074508f0000,0x00000074509f0000) (1024K)]
  0x0000007450169180 JavaThread "Monitor Deflation Thread"   daemon [_thread_blocked, id=6380, stack(0x00000074509f0000,0x0000007450af0000) (1024K)]
  0x000000745016a3f0 JavaThread "C2 CompilerThread0"         daemon [_thread_blocked, id=3776, stack(0x0000007450af0000,0x0000007450bf0000) (1024K)]
  0x000000745016b380 JavaThread "C1 CompilerThread0"         daemon [_thread_blocked, id=7228, stack(0x0000007450bf0000,0x0000007450cf0000) (1024K)]
  0x00000074550a7b10 JavaThread "Notification Thread"        daemon [_thread_blocked, id=6844, stack(0x0000007450cf0000,0x0000007450df0000) (1024K)]
  0x00000074550ac9a0 JavaThread "Common-Cleaner"             daemon [_thread_blocked, id=1104, stack(0x0000007450df0000,0x0000007450ef0000) (1024K)]
  0x0000007457a374f0 JavaThread "ServerMain"                        [_thread_in_Java, id=7152, stack(0x00000074554f0000,0x00000074555f0000) (1024K)]
  0x000000746a8efd60 JavaThread "DestroyJavaVM"                     [_thread_blocked, id=4240, stack(0x000000746aaa0000,0x000000746aba0000) (1024K)]
  0x0000007455e7c6d0 JavaThread "Log4j2-AsyncAppenderEventDispatcher-1-Async" daemon [_thread_blocked, id=6800, stack(0x0000007456cc0000,0x0000007456dc0000) (1024K)]
  0x00000074562824e0 JavaThread "JNA Cleaner"                daemon [_thread_blocked, id=5340, stack(0x0000007456dc0000,0x0000007456ec0000) (1024K)]
  0x00000074562a3ac0 JavaThread "Timer hack thread"          daemon [_thread_blocked, id=9140, stack(0x0000007457410000,0x0000007457510000) (1024K)]
  0x00000074562a3430 JavaThread "Yggdrasil Key Fetcher"      daemon [_thread_blocked, id=6860, stack(0x0000007457510000,0x0000007457610000) (1024K)]
  0x000000745a9760c0 JavaThread "Keep-Alive-Timer"           daemon [_thread_blocked, id=3492, stack(0x00000074578c0000,0x00000074579c0000) (1024K)]
  0x000000745a978190 JavaThread "Worker-Main-1"              daemon [_thread_blocked, id=2956, stack(0x000000745b400000,0x000000745b500000) (1024K)]
  0x000000745a979540 JavaThread "Java2D Disposer"            daemon [_thread_blocked, id=4624, stack(0x000000745b190000,0x000000745b290000) (1024K)]
  0x000000745a977470 JavaThread "AWT-Shutdown"                      [_thread_blocked, id=7488, stack(0x000000745b290000,0x000000745b390000) (1024K)]
  0x000000745a978820 JavaThread "AWT-Windows"                daemon [_thread_in_native, id=4940, stack(0x000000745b500000,0x000000745b600000) (1024K)]
  0x00000074562a4150 JavaThread "AWT-EventQueue-0"                  [_thread_blocked, id=5944, stack(0x00000074555f0000,0x00000074556f0000) (1024K)]
  0x00000074562a2710 JavaThread "TimerQueue"                 daemon [_thread_blocked, id=8852, stack(0x0000007460000000,0x0000007460100000) (1024K)]
  0x00000074562a47e0 JavaThread "Thread-2"                   daemon [_thread_blocked, id=6448, stack(0x0000007460200000,0x0000007460300000) (1024K)]
=>0x000000745a924f90 JavaThread "Server thread"                     [_thread_in_native, id=2972, stack(0x0000007460300000,0x0000007460400000) (1024K)]
  0x000000745a922830 JavaThread "Craft Scheduler Thread - 0"        [_thread_blocked, id=3352, stack(0x0000007460400000,0x0000007460500000) (1024K)]
  0x000000745a923550 JavaThread "Craft Scheduler Thread - 1"        [_thread_blocked, id=8372, stack(0x0000007460500000,0x0000007460600000) (1024K)]
  0x000000745a9221a0 JavaThread "Craft Scheduler Thread - 2"        [_thread_blocked, id=4552, stack(0x0000007460600000,0x0000007460700000) (1024K)]
  0x000000745a924270 JavaThread "Craft Scheduler Thread - 3"        [_thread_blocked, id=6320, stack(0x0000007460700000,0x0000007460800000) (1024K)]
  0x000000745828bf10 JavaThread "C2 CompilerThread1"         daemon [_thread_blocked, id=8204, stack(0x0000007460800000,0x0000007460900000) (1024K)]
  0x000000745a927060 JavaThread "RegionFile I/O Thread #0"          [_thread_blocked, id=4100, stack(0x00000074618d0000,0x00000074619d0000) (1024K)]
  0x000000745a9269d0 JavaThread "Tuinity Chunk System Worker #0"        [_thread_blocked, id=3476, stack(0x00000074619d0000,0x0000007461ad0000) (1024K)]
Total: 32

Other Threads:
  0x0000007450135630 VMThread "VM Thread"                           [id=312, stack(0x0000007450300000,0x0000007450400000) (1024K)]
  0x000000745011f110 WatcherThread "VM Periodic Task Thread"        [id=7552, stack(0x0000007450200000,0x0000007450300000) (1024K)]
  0x000000746cb76110 WorkerThread "GC Thread#0"                     [id=4984, stack(0x000000746c950000,0x000000746ca50000) (1024K)]
  0x00000074551bb160 WorkerThread "GC Thread#1"                     [id=4304, stack(0x0000007450ef0000,0x0000007450ff0000) (1024K)]
  0x00000074551c10a0 WorkerThread "GC Thread#2"                     [id=6352, stack(0x0000007455810000,0x0000007455910000) (1024K)]
  0x00000074551c1450 WorkerThread "GC Thread#3"                     [id=3248, stack(0x0000007455910000,0x0000007455a10000) (1024K)]
  0x000000746cb7ed80 ConcurrentGCThread "G1 Main Marker"            [id=2868, stack(0x0000007476200000,0x0000007476300000) (1024K)]
  0x000000746cb80600 WorkerThread "G1 Conc#0"                       [id=5500, stack(0x0000007476300000,0x0000007476400000) (1024K)]
  0x000000746cbdb490 ConcurrentGCThread "G1 Refine#0"               [id=2428, stack(0x0000007478850000,0x0000007478950000) (1024K)]
  0x000000746cbdbc20 ConcurrentGCThread "G1 Service"                [id=6088, stack(0x0000007478950000,0x0000007478a50000) (1024K)]
Total: 10

Threads with active compile tasks:
Total: 0

VM state: not at safepoint (normal execution)

VM Mutex/Monitor currently owned by a thread: None

Heap address: 0x00000000c1c00000, size: 996 MB, Compressed Oops mode: 32-bit

CDS archive(s) mapped at: [0x000000740f000000-0x000000740fc60000-0x000000740fc60000), size 12976128, SharedBaseAddress: 0x000000740f000000, ArchiveRelocationMode: 1.
Compressed class space mapped at: 0x0000007410000000-0x0000007450000000, reserved size: 1073741824
Narrow klass base: 0x000000740f000000, Narrow klass shift: 0, Narrow klass range: 0x41000000

GC Precious Log:
 CardTable entry size: 512
 Card Set container configuration: InlinePtr #cards 5 size 8 Array Of Cards #cards 12 size 40 Howl #buckets 4 coarsen threshold 1843 Howl Bitmap #cards 512 size 80 coarsen threshold 460 Card regions per heap region 1 cards per card region 2048
 CPUs: 4 total, 4 available
 Memory: 3981M
 Large Page Support: Disabled
 NUMA Support: Disabled
 Compressed Oops: Enabled (32-bit)
 Heap Region Size: 1M
 Heap Min Capacity: 8M
 Heap Initial Capacity: 64M
 Heap Max Capacity: 996M
 Pre-touch: Disabled
 Parallel Workers: 4
 Concurrent Workers: 1
 Concurrent Refinement Workers: 4
 Periodic GC: Disabled

Heap:
 garbage-first heap   total reserved 1019904K, committed 343040K, used 256827K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 70 young (71680K), 10 survivors (10240K)
 Metaspace       used 99657K, committed 100544K, reserved 1179648K
  class space    used 13171K, committed 13504K, reserved 1048576K

Heap Regions: E=young(eden), S=young(survivor), O=old, HS=humongous(starts), HC=humongous(continues), CS=collection set, F=free, TAMS=top-at-mark-start, PB=parsable bottom
|   0|0x00000000c1c00000, 0x00000000c1d00000, 0x00000000c1d00000|100%| O|  |TAMS 0x00000000c1c00000| PB 0x00000000c1c00000| Untracked |  0
|   1|0x00000000c1d00000, 0x00000000c1e00000, 0x00000000c1e00000|100%| O|  |TAMS 0x00000000c1d00000| PB 0x00000000c1d00000| Untracked |  0
|   2|0x00000000c1e00000, 0x00000000c1f00000, 0x00000000c1f00000|100%| O|  |TAMS 0x00000000c1e00000| PB 0x00000000c1e00000| Untracked |  0
|   3|0x00000000c1f00000, 0x00000000c2000000, 0x00000000c2000000|100%| O|  |TAMS 0x00000000c1f00000| PB 0x00000000c1f00000| Untracked |  0
|   4|0x00000000c2000000, 0x00000000c2100000, 0x00000000c2100000|100%| O|  |TAMS 0x00000000c2000000| PB 0x00000000c2000000| Untracked |  0
|   5|0x00000000c2100000, 0x00000000c2200000, 0x00000000c2200000|100%| O|  |TAMS 0x00000000c2100000| PB 0x00000000c2100000| Untracked |  0
|   6|0x00000000c2200000, 0x00000000c2300000, 0x00000000c2300000|100%| O|  |TAMS 0x00000000c2200000| PB 0x00000000c2200000| Untracked |  0
|   7|0x00000000c2300000, 0x00000000c2400000, 0x00000000c2400000|100%| O|  |TAMS 0x00000000c2300000| PB 0x00000000c2300000| Untracked |  0
|   8|0x00000000c2400000, 0x00000000c2500000, 0x00000000c2500000|100%| O|  |TAMS 0x00000000c2400000| PB 0x00000000c2400000| Untracked |  0
|   9|0x00000000c2500000, 0x00000000c2600000, 0x00000000c2600000|100%| O|  |TAMS 0x00000000c2500000| PB 0x00000000c2500000| Untracked |  0
|  10|0x00000000c2600000, 0x00000000c2700000, 0x00000000c2700000|100%| O|  |TAMS 0x00000000c2600000| PB 0x00000000c2600000| Untracked |  0
|  11|0x00000000c2700000, 0x00000000c2800000, 0x00000000c2800000|100%| O|  |TAMS 0x00000000c2700000| PB 0x00000000c2700000| Untracked |  0
|  12|0x00000000c2800000, 0x00000000c2800000, 0x00000000c2900000|  0%| F|  |TAMS 0x00000000c2800000| PB 0x00000000c2800000| Untracked |  0
|  13|0x00000000c2900000, 0x00000000c2a00000, 0x00000000c2a00000|100%| O|  |TAMS 0x00000000c2900000| PB 0x00000000c2900000| Untracked |  0
|  14|0x00000000c2a00000, 0x00000000c2b00000, 0x00000000c2b00000|100%| O|  |TAMS 0x00000000c2a00000| PB 0x00000000c2a00000| Untracked |  0
|  15|0x00000000c2b00000, 0x00000000c2c00000, 0x00000000c2c00000|100%| O|  |TAMS 0x00000000c2b00000| PB 0x00000000c2b00000| Untracked |  0
|  16|0x00000000c2c00000, 0x00000000c2d00000, 0x00000000c2d00000|100%| O|  |TAMS 0x00000000c2c00000| PB 0x00000000c2c00000| Untracked |  0
|  17|0x00000000c2d00000, 0x00000000c2e00000, 0x00000000c2e00000|100%| O|  |TAMS 0x00000000c2d00000| PB 0x00000000c2d00000| Untracked |  0
|  18|0x00000000c2e00000, 0x00000000c2f00000, 0x00000000c2f00000|100%| O|  |TAMS 0x00000000c2e00000| PB 0x00000000c2e00000| Untracked |  0
|  19|0x00000000c2f00000, 0x00000000c3000000, 0x00000000c3000000|100%| O|  |TAMS 0x00000000c2f00000| PB 0x00000000c2f00000| Untracked |  0
|  20|0x00000000c3000000, 0x00000000c3100000, 0x00000000c3100000|100%| O|  |TAMS 0x00000000c3000000| PB 0x00000000c3000000| Untracked |  0
|  21|0x00000000c3100000, 0x00000000c3100000, 0x00000000c3200000|  0%| F|  |TAMS 0x00000000c3100000| PB 0x00000000c3100000| Untracked |  0
|  22|0x00000000c3200000, 0x00000000c3300000, 0x00000000c3300000|100%| O|  |TAMS 0x00000000c3200000| PB 0x00000000c3200000| Untracked |  0
|  23|0x00000000c3300000, 0x00000000c3400000, 0x00000000c3400000|100%| O|  |TAMS 0x00000000c3300000| PB 0x00000000c3300000| Untracked |  0
|  24|0x00000000c3400000, 0x00000000c3500000, 0x00000000c3500000|100%| O|  |TAMS 0x00000000c3400000| PB 0x00000000c3400000| Untracked |  0
|  25|0x00000000c3500000, 0x00000000c3600000, 0x00000000c3600000|100%| O|  |TAMS 0x00000000c3500000| PB 0x00000000c3500000| Untracked |  0
|  26|0x00000000c3600000, 0x00000000c3700000, 0x00000000c3700000|100%| O|  |TAMS 0x00000000c3600000| PB 0x00000000c3600000| Untracked |  0
|  27|0x00000000c3700000, 0x00000000c3800000, 0x00000000c3800000|100%| O|  |TAMS 0x00000000c3700000| PB 0x00000000c3700000| Untracked |  0
|  28|0x00000000c3800000, 0x00000000c3800000, 0x00000000c3900000|  0%| F|  |TAMS 0x00000000c3800000| PB 0x00000000c3800000| Untracked |  0
|  29|0x00000000c3900000, 0x00000000c3a00000, 0x00000000c3a00000|100%| O|  |TAMS 0x00000000c3900000| PB 0x00000000c3900000| Untracked |  0
|  30|0x00000000c3a00000, 0x00000000c3b00000, 0x00000000c3b00000|100%| O|  |TAMS 0x00000000c3a00000| PB 0x00000000c3a00000| Untracked |  0
|  31|0x00000000c3b00000, 0x00000000c3c00000, 0x00000000c3c00000|100%| O|  |TAMS 0x00000000c3b00000| PB 0x00000000c3b00000| Untracked |  0
|  32|0x00000000c3c00000, 0x00000000c3d00000, 0x00000000c3d00000|100%| O|  |TAMS 0x00000000c3c00000| PB 0x00000000c3c00000| Untracked |  0
|  33|0x00000000c3d00000, 0x00000000c3e00000, 0x00000000c3e00000|100%| O|  |TAMS 0x00000000c3d00000| PB 0x00000000c3d00000| Untracked |  0
|  34|0x00000000c3e00000, 0x00000000c3f00000, 0x00000000c3f00000|100%| O|  |TAMS 0x00000000c3e00000| PB 0x00000000c3e00000| Untracked |  0
|  35|0x00000000c3f00000, 0x00000000c4000000, 0x00000000c4000000|100%| O|  |TAMS 0x00000000c3f00000| PB 0x00000000c3f00000| Untracked |  0
|  36|0x00000000c4000000, 0x00000000c4100000, 0x00000000c4100000|100%| O|  |TAMS 0x00000000c4000000| PB 0x00000000c4000000| Untracked |  0
|  37|0x00000000c4100000, 0x00000000c4200000, 0x00000000c4200000|100%| O|  |TAMS 0x00000000c4100000| PB 0x00000000c4100000| Untracked |  0
|  38|0x00000000c4200000, 0x00000000c4300000, 0x00000000c4300000|100%| O|  |TAMS 0x00000000c4200000| PB 0x00000000c4200000| Untracked |  0
|  39|0x00000000c4300000, 0x00000000c4400000, 0x00000000c4400000|100%| O|  |TAMS 0x00000000c4300000| PB 0x00000000c4300000| Untracked |  0
|  40|0x00000000c4400000, 0x00000000c4500000, 0x00000000c4500000|100%| O|  |TAMS 0x00000000c4400000| PB 0x00000000c4400000| Untracked |  0
|  41|0x00000000c4500000, 0x00000000c4600000, 0x00000000c4600000|100%| O|  |TAMS 0x00000000c4500000| PB 0x00000000c4500000| Untracked |  0
|  42|0x00000000c4600000, 0x00000000c4700000, 0x00000000c4700000|100%| O|  |TAMS 0x00000000c4600000| PB 0x00000000c4600000| Untracked |  0
|  43|0x00000000c4700000, 0x00000000c4800000, 0x00000000c4800000|100%| O|  |TAMS 0x00000000c4700000| PB 0x00000000c4700000| Untracked |  0
|  44|0x00000000c4800000, 0x00000000c4900000, 0x00000000c4900000|100%| O|  |TAMS 0x00000000c4800000| PB 0x00000000c4800000| Untracked |  0
|  45|0x00000000c4900000, 0x00000000c4a00000, 0x00000000c4a00000|100%| O|  |TAMS 0x00000000c4900000| PB 0x00000000c4900000| Untracked |  0
|  46|0x00000000c4a00000, 0x00000000c4b00000, 0x00000000c4b00000|100%| O|  |TAMS 0x00000000c4a00000| PB 0x00000000c4a00000| Untracked |  0
|  47|0x00000000c4b00000, 0x00000000c4c00000, 0x00000000c4c00000|100%| O|  |TAMS 0x00000000c4b00000| PB 0x00000000c4b00000| Untracked |  0
|  48|0x00000000c4c00000, 0x00000000c4d00000, 0x00000000c4d00000|100%| O|  |TAMS 0x00000000c4c00000| PB 0x00000000c4c00000| Untracked |  0
|  49|0x00000000c4d00000, 0x00000000c4e00000, 0x00000000c4e00000|100%| O|  |TAMS 0x00000000c4d00000| PB 0x00000000c4d00000| Untracked |  0
|  50|0x00000000c4e00000, 0x00000000c4f00000, 0x00000000c4f00000|100%| O|  |TAMS 0x00000000c4e00000| PB 0x00000000c4e00000| Untracked |  0
|  51|0x00000000c4f00000, 0x00000000c5000000, 0x00000000c5000000|100%| O|  |TAMS 0x00000000c4f00000| PB 0x00000000c4f00000| Untracked |  0
|  52|0x00000000c5000000, 0x00000000c5100000, 0x00000000c5100000|100%| O|  |TAMS 0x00000000c5000000| PB 0x00000000c5000000| Untracked |  0
|  53|0x00000000c5100000, 0x00000000c5200000, 0x00000000c5200000|100%| O|  |TAMS 0x00000000c5100000| PB 0x00000000c5100000| Untracked |  0
|  54|0x00000000c5200000, 0x00000000c5300000, 0x00000000c5300000|100%| O|  |TAMS 0x00000000c5200000| PB 0x00000000c5200000| Untracked |  0
|  55|0x00000000c5300000, 0x00000000c5400000, 0x00000000c5400000|100%| O|  |TAMS 0x00000000c5300000| PB 0x00000000c5300000| Untracked |  0
|  56|0x00000000c5400000, 0x00000000c5500000, 0x00000000c5500000|100%| O|  |TAMS 0x00000000c5400000| PB 0x00000000c5400000| Untracked |  0
|  57|0x00000000c5500000, 0x00000000c5600000, 0x00000000c5600000|100%| O|  |TAMS 0x00000000c5500000| PB 0x00000000c5500000| Untracked |  0
|  58|0x00000000c5600000, 0x00000000c5700000, 0x00000000c5700000|100%| O|  |TAMS 0x00000000c5600000| PB 0x00000000c5600000| Untracked |  0
|  59|0x00000000c5700000, 0x00000000c5800000, 0x00000000c5800000|100%| O|  |TAMS 0x00000000c5700000| PB 0x00000000c5700000| Untracked |  0
|  60|0x00000000c5800000, 0x00000000c5900000, 0x00000000c5900000|100%| O|  |TAMS 0x00000000c5800000| PB 0x00000000c5800000| Untracked |  0
|  61|0x00000000c5900000, 0x00000000c5a00000, 0x00000000c5a00000|100%| O|  |TAMS 0x00000000c5900000| PB 0x00000000c5900000| Untracked |  0
|  62|0x00000000c5a00000, 0x00000000c5b00000, 0x00000000c5b00000|100%| O|  |TAMS 0x00000000c5a00000| PB 0x00000000c5a00000| Untracked |  0
|  63|0x00000000c5b00000, 0x00000000c5c00000, 0x00000000c5c00000|100%| O|  |TAMS 0x00000000c5b00000| PB 0x00000000c5b00000| Untracked |  0
|  64|0x00000000c5c00000, 0x00000000c5d00000, 0x00000000c5d00000|100%| O|  |TAMS 0x00000000c5c00000| PB 0x00000000c5c00000| Untracked |  0
|  65|0x00000000c5d00000, 0x00000000c5e00000, 0x00000000c5e00000|100%| O|  |TAMS 0x00000000c5d00000| PB 0x00000000c5d00000| Untracked |  0
|  66|0x00000000c5e00000, 0x00000000c5f00000, 0x00000000c5f00000|100%| O|  |TAMS 0x00000000c5e00000| PB 0x00000000c5e00000| Untracked |  0
|  67|0x00000000c5f00000, 0x00000000c6000000, 0x00000000c6000000|100%| O|Cm|TAMS 0x00000000c5f00000| PB 0x00000000c5f00000| Complete |  0
|  68|0x00000000c6000000, 0x00000000c6100000, 0x00000000c6100000|100%| O|  |TAMS 0x00000000c6000000| PB 0x00000000c6000000| Untracked |  0
|  69|0x00000000c6100000, 0x00000000c6200000, 0x00000000c6200000|100%| O|  |TAMS 0x00000000c6100000| PB 0x00000000c6100000| Untracked |  0
|  70|0x00000000c6200000, 0x00000000c6300000, 0x00000000c6300000|100%| O|  |TAMS 0x00000000c6200000| PB 0x00000000c6200000| Untracked |  0
|  71|0x00000000c6300000, 0x00000000c6400000, 0x00000000c6400000|100%| O|  |TAMS 0x00000000c6300000| PB 0x00000000c6300000| Untracked |  0
|  72|0x00000000c6400000, 0x00000000c6500000, 0x00000000c6500000|100%| O|  |TAMS 0x00000000c6400000| PB 0x00000000c6400000| Untracked |  0
|  73|0x00000000c6500000, 0x00000000c6600000, 0x00000000c6600000|100%| O|  |TAMS 0x00000000c6500000| PB 0x00000000c6500000| Untracked |  0
|  74|0x00000000c6600000, 0x00000000c6700000, 0x00000000c6700000|100%| O|  |TAMS 0x00000000c6600000| PB 0x00000000c6600000| Untracked |  0
|  75|0x00000000c6700000, 0x00000000c6800000, 0x00000000c6800000|100%| O|  |TAMS 0x00000000c6700000| PB 0x00000000c6700000| Untracked |  0
|  76|0x00000000c6800000, 0x00000000c6900000, 0x00000000c6900000|100%| O|Cm|TAMS 0x00000000c6800000| PB 0x00000000c6800000| Complete |  0
|  77|0x00000000c6900000, 0x00000000c6a00000, 0x00000000c6a00000|100%| O|  |TAMS 0x00000000c6900000| PB 0x00000000c6900000| Untracked |  0
|  78|0x00000000c6a00000, 0x00000000c6b00000, 0x00000000c6b00000|100%| O|  |TAMS 0x00000000c6a00000| PB 0x00000000c6a00000| Untracked |  0
|  79|0x00000000c6b00000, 0x00000000c6c00000, 0x00000000c6c00000|100%| O|  |TAMS 0x00000000c6b00000| PB 0x00000000c6b00000| Untracked |  0
|  80|0x00000000c6c00000, 0x00000000c6d00000, 0x00000000c6d00000|100%| O|  |TAMS 0x00000000c6c00000| PB 0x00000000c6c00000| Untracked |  0
|  81|0x00000000c6d00000, 0x00000000c6e00000, 0x00000000c6e00000|100%|HS|  |TAMS 0x00000000c6d00000| PB 0x00000000c6d00000| Complete |  0
|  82|0x00000000c6e00000, 0x00000000c6f00000, 0x00000000c6f00000|100%|HC|  |TAMS 0x00000000c6e00000| PB 0x00000000c6e00000| Complete |  0
|  83|0x00000000c6f00000, 0x00000000c7000000, 0x00000000c7000000|100%|HS|  |TAMS 0x00000000c6f00000| PB 0x00000000c6f00000| Complete |  0
|  84|0x00000000c7000000, 0x00000000c7100000, 0x00000000c7100000|100%|HC|  |TAMS 0x00000000c7000000| PB 0x00000000c7000000| Complete |  0
|  85|0x00000000c7100000, 0x00000000c7200000, 0x00000000c7200000|100%| O|  |TAMS 0x00000000c7100000| PB 0x00000000c7100000| Untracked |  0
|  86|0x00000000c7200000, 0x00000000c7300000, 0x00000000c7300000|100%| O|  |TAMS 0x00000000c7200000| PB 0x00000000c7200000| Untracked |  0
|  87|0x00000000c7300000, 0x00000000c7400000, 0x00000000c7400000|100%| O|  |TAMS 0x00000000c7300000| PB 0x00000000c7300000| Untracked |  0
|  88|0x00000000c7400000, 0x00000000c7500000, 0x00000000c7500000|100%| O|  |TAMS 0x00000000c7400000| PB 0x00000000c7400000| Untracked |  0
|  89|0x00000000c7500000, 0x00000000c7600000, 0x00000000c7600000|100%| O|  |TAMS 0x00000000c7500000| PB 0x00000000c7500000| Untracked |  0
|  90|0x00000000c7600000, 0x00000000c7700000, 0x00000000c7700000|100%| O|  |TAMS 0x00000000c7600000| PB 0x00000000c7600000| Untracked |  0
|  91|0x00000000c7700000, 0x00000000c7800000, 0x00000000c7800000|100%| O|  |TAMS 0x00000000c7700000| PB 0x00000000c7700000| Untracked |  0
|  92|0x00000000c7800000, 0x00000000c7900000, 0x00000000c7900000|100%| O|  |TAMS 0x00000000c7800000| PB 0x00000000c7800000| Untracked |  0
|  93|0x00000000c7900000, 0x00000000c7a00000, 0x00000000c7a00000|100%| O|  |TAMS 0x00000000c7900000| PB 0x00000000c7900000| Untracked |  0
|  94|0x00000000c7a00000, 0x00000000c7b00000, 0x00000000c7b00000|100%| O|  |TAMS 0x00000000c7a00000| PB 0x00000000c7a00000| Untracked |  0
|  95|0x00000000c7b00000, 0x00000000c7c00000, 0x00000000c7c00000|100%| O|  |TAMS 0x00000000c7b00000| PB 0x00000000c7b00000| Untracked |  0
|  96|0x00000000c7c00000, 0x00000000c7d00000, 0x00000000c7d00000|100%| O|  |TAMS 0x00000000c7c00000| PB 0x00000000c7c00000| Untracked |  0
|  97|0x00000000c7d00000, 0x00000000c7e00000, 0x00000000c7e00000|100%| O|  |TAMS 0x00000000c7d00000| PB 0x00000000c7d00000| Untracked |  0
|  98|0x00000000c7e00000, 0x00000000c7f00000, 0x00000000c7f00000|100%| O|  |TAMS 0x00000000c7e00000| PB 0x00000000c7e00000| Untracked |  0
|  99|0x00000000c7f00000, 0x00000000c8000000, 0x00000000c8000000|100%| O|  |TAMS 0x00000000c7f00000| PB 0x00000000c7f00000| Untracked |  0
| 100|0x00000000c8000000, 0x00000000c8100000, 0x00000000c8100000|100%| O|  |TAMS 0x00000000c8000000| PB 0x00000000c8000000| Untracked |  0
| 101|0x00000000c8100000, 0x00000000c8200000, 0x00000000c8200000|100%| O|  |TAMS 0x00000000c8100000| PB 0x00000000c8100000| Untracked |  0
| 102|0x00000000c8200000, 0x00000000c8300000, 0x00000000c8300000|100%| O|  |TAMS 0x00000000c8200000| PB 0x00000000c8200000| Untracked |  0
| 103|0x00000000c8300000, 0x00000000c8400000, 0x00000000c8400000|100%| O|  |TAMS 0x00000000c8300000| PB 0x00000000c8300000| Untracked |  0
| 104|0x00000000c8400000, 0x00000000c8500000, 0x00000000c8500000|100%| O|  |TAMS 0x00000000c8400000| PB 0x00000000c8400000| Untracked |  0
| 105|0x00000000c8500000, 0x00000000c8600000, 0x00000000c8600000|100%| O|  |TAMS 0x00000000c8500000| PB 0x00000000c8500000| Untracked |  0
| 106|0x00000000c8600000, 0x00000000c8700000, 0x00000000c8700000|100%| O|  |TAMS 0x00000000c8600000| PB 0x00000000c8600000| Untracked |  0
| 107|0x00000000c8700000, 0x00000000c8800000, 0x00000000c8800000|100%| O|  |TAMS 0x00000000c8700000| PB 0x00000000c8700000| Untracked |  0
| 108|0x00000000c8800000, 0x00000000c8900000, 0x00000000c8900000|100%| O|  |TAMS 0x00000000c8800000| PB 0x00000000c8800000| Untracked |  0
| 109|0x00000000c8900000, 0x00000000c8a00000, 0x00000000c8a00000|100%| O|  |TAMS 0x00000000c8900000| PB 0x00000000c8900000| Untracked |  0
| 110|0x00000000c8a00000, 0x00000000c8b00000, 0x00000000c8b00000|100%| O|  |TAMS 0x00000000c8a00000| PB 0x00000000c8a00000| Untracked |  0
| 111|0x00000000c8b00000, 0x00000000c8c00000, 0x00000000c8c00000|100%| O|Cm|TAMS 0x00000000c8b00000| PB 0x00000000c8b00000| Complete |  0
| 112|0x00000000c8c00000, 0x00000000c8d00000, 0x00000000c8d00000|100%| O|  |TAMS 0x00000000c8c00000| PB 0x00000000c8c00000| Untracked |  0
| 113|0x00000000c8d00000, 0x00000000c8e00000, 0x00000000c8e00000|100%| O|  |TAMS 0x00000000c8d00000| PB 0x00000000c8d00000| Untracked |  0
| 114|0x00000000c8e00000, 0x00000000c8f00000, 0x00000000c8f00000|100%| O|  |TAMS 0x00000000c8e00000| PB 0x00000000c8e00000| Untracked |  0
| 115|0x00000000c8f00000, 0x00000000c9000000, 0x00000000c9000000|100%| O|  |TAMS 0x00000000c8f00000| PB 0x00000000c8f00000| Untracked |  0
| 116|0x00000000c9000000, 0x00000000c9100000, 0x00000000c9100000|100%| O|  |TAMS 0x00000000c9000000| PB 0x00000000c9000000| Untracked |  0
| 117|0x00000000c9100000, 0x00000000c9200000, 0x00000000c9200000|100%| O|  |TAMS 0x00000000c9100000| PB 0x00000000c9100000| Untracked |  0
| 118|0x00000000c9200000, 0x00000000c9300000, 0x00000000c9300000|100%| O|  |TAMS 0x00000000c9200000| PB 0x00000000c9200000| Untracked |  0
| 119|0x00000000c9300000, 0x00000000c9400000, 0x00000000c9400000|100%| O|  |TAMS 0x00000000c9300000| PB 0x00000000c9300000| Untracked |  0
| 120|0x00000000c9400000, 0x00000000c9500000, 0x00000000c9500000|100%| O|  |TAMS 0x00000000c9400000| PB 0x00000000c9400000| Untracked |  0
| 121|0x00000000c9500000, 0x00000000c9600000, 0x00000000c9600000|100%| O|  |TAMS 0x00000000c9500000| PB 0x00000000c9500000| Untracked |  0
| 122|0x00000000c9600000, 0x00000000c9700000, 0x00000000c9700000|100%| O|  |TAMS 0x00000000c9600000| PB 0x00000000c9600000| Untracked |  0
| 123|0x00000000c9700000, 0x00000000c9800000, 0x00000000c9800000|100%| O|  |TAMS 0x00000000c9700000| PB 0x00000000c9700000| Untracked |  0
| 124|0x00000000c9800000, 0x00000000c9900000, 0x00000000c9900000|100%| O|  |TAMS 0x00000000c9800000| PB 0x00000000c9800000| Untracked |  0
| 125|0x00000000c9900000, 0x00000000c9a00000, 0x00000000c9a00000|100%| O|  |TAMS 0x00000000c9900000| PB 0x00000000c9900000| Untracked |  0
| 126|0x00000000c9a00000, 0x00000000c9b00000, 0x00000000c9b00000|100%| O|  |TAMS 0x00000000c9a00000| PB 0x00000000c9a00000| Untracked |  0
| 127|0x00000000c9b00000, 0x00000000c9c00000, 0x00000000c9c00000|100%| O|  |TAMS 0x00000000c9b00000| PB 0x00000000c9b00000| Untracked |  0
| 128|0x00000000c9c00000, 0x00000000c9d00000, 0x00000000c9d00000|100%| O|  |TAMS 0x00000000c9c00000| PB 0x00000000c9c00000| Untracked |  0
| 129|0x00000000c9d00000, 0x00000000c9e00000, 0x00000000c9e00000|100%| O|  |TAMS 0x00000000c9d00000| PB 0x00000000c9d00000| Untracked |  0
| 130|0x00000000c9e00000, 0x00000000c9f00000, 0x00000000c9f00000|100%| O|  |TAMS 0x00000000c9e00000| PB 0x00000000c9e00000| Untracked |  0
| 131|0x00000000c9f00000, 0x00000000ca000000, 0x00000000ca000000|100%| O|  |TAMS 0x00000000c9f00000| PB 0x00000000c9f00000| Untracked |  0
| 132|0x00000000ca000000, 0x00000000ca100000, 0x00000000ca100000|100%| O|  |TAMS 0x00000000ca000000| PB 0x00000000ca000000| Untracked |  0
| 133|0x00000000ca100000, 0x00000000ca200000, 0x00000000ca200000|100%| O|  |TAMS 0x00000000ca100000| PB 0x00000000ca100000| Untracked |  0
| 134|0x00000000ca200000, 0x00000000ca300000, 0x00000000ca300000|100%| O|  |TAMS 0x00000000ca200000| PB 0x00000000ca200000| Untracked |  0
| 135|0x00000000ca300000, 0x00000000ca400000, 0x00000000ca400000|100%| O|  |TAMS 0x00000000ca300000| PB 0x00000000ca300000| Untracked |  0
| 136|0x00000000ca400000, 0x00000000ca500000, 0x00000000ca500000|100%| O|  |TAMS 0x00000000ca400000| PB 0x00000000ca400000| Untracked |  0
| 137|0x00000000ca500000, 0x00000000ca600000, 0x00000000ca600000|100%| O|  |TAMS 0x00000000ca500000| PB 0x00000000ca500000| Untracked |  0
| 138|0x00000000ca600000, 0x00000000ca700000, 0x00000000ca700000|100%| O|  |TAMS 0x00000000ca600000| PB 0x00000000ca600000| Untracked |  0
| 139|0x00000000ca700000, 0x00000000ca800000, 0x00000000ca800000|100%| O|  |TAMS 0x00000000ca700000| PB 0x00000000ca700000| Untracked |  0
| 140|0x00000000ca800000, 0x00000000ca900000, 0x00000000ca900000|100%| O|  |TAMS 0x00000000ca800000| PB 0x00000000ca800000| Untracked |  0
| 141|0x00000000ca900000, 0x00000000caa00000, 0x00000000caa00000|100%| O|  |TAMS 0x00000000ca900000| PB 0x00000000ca900000| Untracked |  0
| 142|0x00000000caa00000, 0x00000000cab00000, 0x00000000cab00000|100%| O|  |TAMS 0x00000000caa00000| PB 0x00000000caa00000| Untracked |  0
| 143|0x00000000cab00000, 0x00000000cac00000, 0x00000000cac00000|100%| O|  |TAMS 0x00000000cab00000| PB 0x00000000cab00000| Untracked |  0
| 144|0x00000000cac00000, 0x00000000cad00000, 0x00000000cad00000|100%| O|  |TAMS 0x00000000cac00000| PB 0x00000000cac00000| Untracked |  0
| 145|0x00000000cad00000, 0x00000000cae00000, 0x00000000cae00000|100%| O|  |TAMS 0x00000000cad00000| PB 0x00000000cad00000| Untracked |  0
| 146|0x00000000cae00000, 0x00000000caf00000, 0x00000000caf00000|100%| O|  |TAMS 0x00000000cae00000| PB 0x00000000cae00000| Untracked |  0
| 147|0x00000000caf00000, 0x00000000cb000000, 0x00000000cb000000|100%| O|  |TAMS 0x00000000caf00000| PB 0x00000000caf00000| Untracked |  0
| 148|0x00000000cb000000, 0x00000000cb100000, 0x00000000cb100000|100%|HS|  |TAMS 0x00000000cb000000| PB 0x00000000cb000000| Complete |  0
| 149|0x00000000cb100000, 0x00000000cb200000, 0x00000000cb200000|100%|HC|  |TAMS 0x00000000cb100000| PB 0x00000000cb100000| Complete |  0
| 150|0x00000000cb200000, 0x00000000cb300000, 0x00000000cb300000|100%| O|  |TAMS 0x00000000cb200000| PB 0x00000000cb200000| Untracked |  0
| 151|0x00000000cb300000, 0x00000000cb300000, 0x00000000cb400000|  0%| F|  |TAMS 0x00000000cb300000| PB 0x00000000cb300000| Untracked |  0
| 152|0x00000000cb400000, 0x00000000cb500000, 0x00000000cb500000|100%| O|  |TAMS 0x00000000cb400000| PB 0x00000000cb400000| Untracked |  0
| 153|0x00000000cb500000, 0x00000000cb600000, 0x00000000cb600000|100%| O|  |TAMS 0x00000000cb500000| PB 0x00000000cb500000| Untracked |  0
| 154|0x00000000cb600000, 0x00000000cb700000, 0x00000000cb700000|100%| O|  |TAMS 0x00000000cb600000| PB 0x00000000cb600000| Untracked |  0
| 155|0x00000000cb700000, 0x00000000cb800000, 0x00000000cb800000|100%| O|  |TAMS 0x00000000cb700000| PB 0x00000000cb700000| Untracked |  0
| 156|0x00000000cb800000, 0x00000000cb900000, 0x00000000cb900000|100%| O|  |TAMS 0x00000000cb800000| PB 0x00000000cb800000| Untracked |  0
| 157|0x00000000cb900000, 0x00000000cba00000, 0x00000000cba00000|100%| O|  |TAMS 0x00000000cb900000| PB 0x00000000cb900000| Untracked |  0
| 158|0x00000000cba00000, 0x00000000cbb00000, 0x00000000cbb00000|100%| O|  |TAMS 0x00000000cba00000| PB 0x00000000cba00000| Untracked |  0
| 159|0x00000000cbb00000, 0x00000000cbc00000, 0x00000000cbc00000|100%| O|  |TAMS 0x00000000cbb00000| PB 0x00000000cbb00000| Untracked |  0
| 160|0x00000000cbc00000, 0x00000000cbd00000, 0x00000000cbd00000|100%| O|  |TAMS 0x00000000cbc00000| PB 0x00000000cbc00000| Untracked |  0
| 161|0x00000000cbd00000, 0x00000000cbe00000, 0x00000000cbe00000|100%| O|  |TAMS 0x00000000cbd00000| PB 0x00000000cbd00000| Untracked |  0
| 162|0x00000000cbe00000, 0x00000000cbf00000, 0x00000000cbf00000|100%| O|  |TAMS 0x00000000cbe00000| PB 0x00000000cbe00000| Untracked |  0
| 163|0x00000000cbf00000, 0x00000000cc000000, 0x00000000cc000000|100%| O|  |TAMS 0x00000000cbf00000| PB 0x00000000cbf00000| Untracked |  0
| 164|0x00000000cc000000, 0x00000000cc100000, 0x00000000cc100000|100%| O|  |TAMS 0x00000000cc000000| PB 0x00000000cc000000| Untracked |  0
| 165|0x00000000cc100000, 0x00000000cc200000, 0x00000000cc200000|100%| O|  |TAMS 0x00000000cc100000| PB 0x00000000cc100000| Untracked |  0
| 166|0x00000000cc200000, 0x00000000cc300000, 0x00000000cc300000|100%| O|  |TAMS 0x00000000cc200000| PB 0x00000000cc200000| Untracked |  0
| 167|0x00000000cc300000, 0x00000000cc400000, 0x00000000cc400000|100%| O|  |TAMS 0x00000000cc300000| PB 0x00000000cc300000| Untracked |  0
| 168|0x00000000cc400000, 0x00000000cc500000, 0x00000000cc500000|100%| O|  |TAMS 0x00000000cc400000| PB 0x00000000cc400000| Untracked |  0
| 169|0x00000000cc500000, 0x00000000cc600000, 0x00000000cc600000|100%| O|  |TAMS 0x00000000cc500000| PB 0x00000000cc500000| Untracked |  0
| 170|0x00000000cc600000, 0x00000000cc700000, 0x00000000cc700000|100%| O|  |TAMS 0x00000000cc600000| PB 0x00000000cc600000| Untracked |  0
| 171|0x00000000cc700000, 0x00000000cc800000, 0x00000000cc800000|100%| O|  |TAMS 0x00000000cc700000| PB 0x00000000cc700000| Untracked |  0
| 172|0x00000000cc800000, 0x00000000cc900000, 0x00000000cc900000|100%| O|Cm|TAMS 0x00000000cc800000| PB 0x00000000cc800000| Complete |  0
| 173|0x00000000cc900000, 0x00000000cca00000, 0x00000000cca00000|100%| O|  |TAMS 0x00000000cc900000| PB 0x00000000cc900000| Untracked |  0
| 174|0x00000000cca00000, 0x00000000ccaced48, 0x00000000ccb00000| 80%| O|  |TAMS 0x00000000cca00000| PB 0x00000000cca00000| Untracked |  0
| 175|0x00000000ccb00000, 0x00000000ccc00000, 0x00000000ccc00000|100%|HS|  |TAMS 0x00000000ccb00000| PB 0x00000000ccb00000| Complete |  0
| 176|0x00000000ccc00000, 0x00000000ccd00000, 0x00000000ccd00000|100%|HC|  |TAMS 0x00000000ccc00000| PB 0x00000000ccc00000| Complete |  0
| 177|0x00000000ccd00000, 0x00000000ccd00000, 0x00000000cce00000|  0%| F|  |TAMS 0x00000000ccd00000| PB 0x00000000ccd00000| Untracked |  0
| 178|0x00000000cce00000, 0x00000000cce00000, 0x00000000ccf00000|  0%| F|  |TAMS 0x00000000cce00000| PB 0x00000000cce00000| Untracked |  0
| 179|0x00000000ccf00000, 0x00000000ccf00000, 0x00000000cd000000|  0%| F|  |TAMS 0x00000000ccf00000| PB 0x00000000ccf00000| Untracked |  0
| 180|0x00000000cd000000, 0x00000000cd000000, 0x00000000cd100000|  0%| F|  |TAMS 0x00000000cd000000| PB 0x00000000cd000000| Untracked |  0
| 181|0x00000000cd100000, 0x00000000cd100000, 0x00000000cd200000|  0%| F|  |TAMS 0x00000000cd100000| PB 0x00000000cd100000| Untracked |  0
| 182|0x00000000cd200000, 0x00000000cd200000, 0x00000000cd300000|  0%| F|  |TAMS 0x00000000cd200000| PB 0x00000000cd200000| Untracked |  0
| 183|0x00000000cd300000, 0x00000000cd300000, 0x00000000cd400000|  0%| F|  |TAMS 0x00000000cd300000| PB 0x00000000cd300000| Untracked |  0
| 184|0x00000000cd400000, 0x00000000cd400000, 0x00000000cd500000|  0%| F|  |TAMS 0x00000000cd400000| PB 0x00000000cd400000| Untracked |  0
| 185|0x00000000cd500000, 0x00000000cd500000, 0x00000000cd600000|  0%| F|  |TAMS 0x00000000cd500000| PB 0x00000000cd500000| Untracked |  0
| 186|0x00000000cd600000, 0x00000000cd600000, 0x00000000cd700000|  0%| F|  |TAMS 0x00000000cd600000| PB 0x00000000cd600000| Untracked |  0
| 187|0x00000000cd700000, 0x00000000cd700000, 0x00000000cd800000|  0%| F|  |TAMS 0x00000000cd700000| PB 0x00000000cd700000| Untracked |  0
| 188|0x00000000cd800000, 0x00000000cd800000, 0x00000000cd900000|  0%| F|  |TAMS 0x00000000cd800000| PB 0x00000000cd800000| Untracked |  0
| 189|0x00000000cd900000, 0x00000000cd900000, 0x00000000cda00000|  0%| F|  |TAMS 0x00000000cd900000| PB 0x00000000cd900000| Untracked |  0
| 190|0x00000000cda00000, 0x00000000cda00000, 0x00000000cdb00000|  0%| F|  |TAMS 0x00000000cda00000| PB 0x00000000cda00000| Untracked |  0
| 191|0x00000000cdb00000, 0x00000000cdb00000, 0x00000000cdc00000|  0%| F|  |TAMS 0x00000000cdb00000| PB 0x00000000cdb00000| Untracked |  0
| 192|0x00000000cdc00000, 0x00000000cdc00000, 0x00000000cdd00000|  0%| F|  |TAMS 0x00000000cdc00000| PB 0x00000000cdc00000| Untracked |  0
| 193|0x00000000cdd00000, 0x00000000cdd00000, 0x00000000cde00000|  0%| F|  |TAMS 0x00000000cdd00000| PB 0x00000000cdd00000| Untracked |  0
| 194|0x00000000cde00000, 0x00000000cde00000, 0x00000000cdf00000|  0%| F|  |TAMS 0x00000000cde00000| PB 0x00000000cde00000| Untracked |  0
| 195|0x00000000cdf00000, 0x00000000ce000000, 0x00000000ce000000|100%| S|CS|TAMS 0x00000000cdf00000| PB 0x00000000cdf00000| Complete |  0
| 196|0x00000000ce000000, 0x00000000ce100000, 0x00000000ce100000|100%| S|CS|TAMS 0x00000000ce000000| PB 0x00000000ce000000| Complete |  0
| 197|0x00000000ce100000, 0x00000000ce200000, 0x00000000ce200000|100%| S|CS|TAMS 0x00000000ce100000| PB 0x00000000ce100000| Complete |  0
| 198|0x00000000ce200000, 0x00000000ce300000, 0x00000000ce300000|100%| S|CS|TAMS 0x00000000ce200000| PB 0x00000000ce200000| Complete |  0
| 199|0x00000000ce300000, 0x00000000ce300000, 0x00000000ce400000|  0%| F|  |TAMS 0x00000000ce300000| PB 0x00000000ce300000| Untracked |  0
| 200|0x00000000ce400000, 0x00000000ce400000, 0x00000000ce500000|  0%| F|  |TAMS 0x00000000ce400000| PB 0x00000000ce400000| Untracked |  0
| 201|0x00000000ce500000, 0x00000000ce600000, 0x00000000ce600000|100%| S|CS|TAMS 0x00000000ce500000| PB 0x00000000ce500000| Complete |  0
| 202|0x00000000ce600000, 0x00000000ce700000, 0x00000000ce700000|100%| S|CS|TAMS 0x00000000ce600000| PB 0x00000000ce600000| Complete |  0
| 203|0x00000000ce700000, 0x00000000ce800000, 0x00000000ce800000|100%| S|CS|TAMS 0x00000000ce700000| PB 0x00000000ce700000| Complete |  0
| 204|0x00000000ce800000, 0x00000000ce900000, 0x00000000ce900000|100%| S|CS|TAMS 0x00000000ce800000| PB 0x00000000ce800000| Complete |  0
| 205|0x00000000ce900000, 0x00000000cea00000, 0x00000000cea00000|100%| S|CS|TAMS 0x00000000ce900000| PB 0x00000000ce900000| Complete |  0
| 206|0x00000000cea00000, 0x00000000ceb00000, 0x00000000ceb00000|100%| S|CS|TAMS 0x00000000cea00000| PB 0x00000000cea00000| Complete |  0
| 207|0x00000000ceb00000, 0x00000000ceb00000, 0x00000000cec00000|  0%| F|  |TAMS 0x00000000ceb00000| PB 0x00000000ceb00000| Untracked |  0
| 208|0x00000000cec00000, 0x00000000cec00000, 0x00000000ced00000|  0%| F|  |TAMS 0x00000000cec00000| PB 0x00000000cec00000| Untracked |  0
| 209|0x00000000ced00000, 0x00000000ced00000, 0x00000000cee00000|  0%| F|  |TAMS 0x00000000ced00000| PB 0x00000000ced00000| Untracked |  0
| 210|0x00000000cee00000, 0x00000000cee00000, 0x00000000cef00000|  0%| F|  |TAMS 0x00000000cee00000| PB 0x00000000cee00000| Untracked |  0
| 211|0x00000000cef00000, 0x00000000cef00000, 0x00000000cf000000|  0%| F|  |TAMS 0x00000000cef00000| PB 0x00000000cef00000| Untracked |  0
| 212|0x00000000cf000000, 0x00000000cf000000, 0x00000000cf100000|  0%| F|  |TAMS 0x00000000cf000000| PB 0x00000000cf000000| Untracked |  0
| 213|0x00000000cf100000, 0x00000000cf100000, 0x00000000cf200000|  0%| F|  |TAMS 0x00000000cf100000| PB 0x00000000cf100000| Untracked |  0
| 214|0x00000000cf200000, 0x00000000cf200000, 0x00000000cf300000|  0%| F|  |TAMS 0x00000000cf200000| PB 0x00000000cf200000| Untracked |  0
| 215|0x00000000cf300000, 0x00000000cf300000, 0x00000000cf400000|  0%| F|  |TAMS 0x00000000cf300000| PB 0x00000000cf300000| Untracked |  0
| 216|0x00000000cf400000, 0x00000000cf400000, 0x00000000cf500000|  0%| F|  |TAMS 0x00000000cf400000| PB 0x00000000cf400000| Untracked |  0
| 217|0x00000000cf500000, 0x00000000cf500000, 0x00000000cf600000|  0%| F|  |TAMS 0x00000000cf500000| PB 0x00000000cf500000| Untracked |  0
| 218|0x00000000cf600000, 0x00000000cf600000, 0x00000000cf700000|  0%| F|  |TAMS 0x00000000cf600000| PB 0x00000000cf600000| Untracked |  0
| 219|0x00000000cf700000, 0x00000000cf700000, 0x00000000cf800000|  0%| F|  |TAMS 0x00000000cf700000| PB 0x00000000cf700000| Untracked |  0
| 220|0x00000000cf800000, 0x00000000cf800000, 0x00000000cf900000|  0%| F|  |TAMS 0x00000000cf800000| PB 0x00000000cf800000| Untracked |  0
| 221|0x00000000cf900000, 0x00000000cf900000, 0x00000000cfa00000|  0%| F|  |TAMS 0x00000000cf900000| PB 0x00000000cf900000| Untracked |  0
| 222|0x00000000cfa00000, 0x00000000cfa00000, 0x00000000cfb00000|  0%| F|  |TAMS 0x00000000cfa00000| PB 0x00000000cfa00000| Untracked |  0
| 223|0x00000000cfb00000, 0x00000000cfb00000, 0x00000000cfc00000|  0%| F|  |TAMS 0x00000000cfb00000| PB 0x00000000cfb00000| Untracked |  0
| 224|0x00000000cfc00000, 0x00000000cfc00000, 0x00000000cfd00000|  0%| F|  |TAMS 0x00000000cfc00000| PB 0x00000000cfc00000| Untracked |  0
| 225|0x00000000cfd00000, 0x00000000cfd00000, 0x00000000cfe00000|  0%| F|  |TAMS 0x00000000cfd00000| PB 0x00000000cfd00000| Untracked |  0
| 226|0x00000000cfe00000, 0x00000000cfe00000, 0x00000000cff00000|  0%| F|  |TAMS 0x00000000cfe00000| PB 0x00000000cfe00000| Untracked |  0
| 227|0x00000000cff00000, 0x00000000cff00000, 0x00000000d0000000|  0%| F|  |TAMS 0x00000000cff00000| PB 0x00000000cff00000| Untracked |  0
| 228|0x00000000d0000000, 0x00000000d0000000, 0x00000000d0100000|  0%| F|  |TAMS 0x00000000d0000000| PB 0x00000000d0000000| Untracked |  0
| 229|0x00000000d0100000, 0x00000000d0100000, 0x00000000d0200000|  0%| F|  |TAMS 0x00000000d0100000| PB 0x00000000d0100000| Untracked |  0
| 230|0x00000000d0200000, 0x00000000d0200000, 0x00000000d0300000|  0%| F|  |TAMS 0x00000000d0200000| PB 0x00000000d0200000| Untracked |  0
| 231|0x00000000d0300000, 0x00000000d0300000, 0x00000000d0400000|  0%| F|  |TAMS 0x00000000d0300000| PB 0x00000000d0300000| Untracked |  0
| 232|0x00000000d0400000, 0x00000000d0400000, 0x00000000d0500000|  0%| F|  |TAMS 0x00000000d0400000| PB 0x00000000d0400000| Untracked |  0
| 233|0x00000000d0500000, 0x00000000d0500000, 0x00000000d0600000|  0%| F|  |TAMS 0x00000000d0500000| PB 0x00000000d0500000| Untracked |  0
| 234|0x00000000d0600000, 0x00000000d0600000, 0x00000000d0700000|  0%| F|  |TAMS 0x00000000d0600000| PB 0x00000000d0600000| Untracked |  0
| 235|0x00000000d0700000, 0x00000000d0700000, 0x00000000d0800000|  0%| F|  |TAMS 0x00000000d0700000| PB 0x00000000d0700000| Untracked |  0
| 236|0x00000000d0800000, 0x00000000d0800000, 0x00000000d0900000|  0%| F|  |TAMS 0x00000000d0800000| PB 0x00000000d0800000| Untracked |  0
| 237|0x00000000d0900000, 0x00000000d0900000, 0x00000000d0a00000|  0%| F|  |TAMS 0x00000000d0900000| PB 0x00000000d0900000| Untracked |  0
| 238|0x00000000d0a00000, 0x00000000d0a00000, 0x00000000d0b00000|  0%| F|  |TAMS 0x00000000d0a00000| PB 0x00000000d0a00000| Untracked |  0
| 239|0x00000000d0b00000, 0x00000000d0b00000, 0x00000000d0c00000|  0%| F|  |TAMS 0x00000000d0b00000| PB 0x00000000d0b00000| Untracked |  0
| 240|0x00000000d0c00000, 0x00000000d0c00000, 0x00000000d0d00000|  0%| F|  |TAMS 0x00000000d0c00000| PB 0x00000000d0c00000| Untracked |  0
| 241|0x00000000d0d00000, 0x00000000d0d00000, 0x00000000d0e00000|  0%| F|  |TAMS 0x00000000d0d00000| PB 0x00000000d0d00000| Untracked |  0
| 242|0x00000000d0e00000, 0x00000000d0e00000, 0x00000000d0f00000|  0%| F|  |TAMS 0x00000000d0e00000| PB 0x00000000d0e00000| Untracked |  0
| 243|0x00000000d0f00000, 0x00000000d0f00000, 0x00000000d1000000|  0%| F|  |TAMS 0x00000000d0f00000| PB 0x00000000d0f00000| Untracked |  0
| 244|0x00000000d1000000, 0x00000000d1000000, 0x00000000d1100000|  0%| F|  |TAMS 0x00000000d1000000| PB 0x00000000d1000000| Untracked |  0
| 245|0x00000000d1100000, 0x00000000d1100000, 0x00000000d1200000|  0%| F|  |TAMS 0x00000000d1100000| PB 0x00000000d1100000| Untracked |  0
| 246|0x00000000d1200000, 0x00000000d1200000, 0x00000000d1300000|  0%| F|  |TAMS 0x00000000d1200000| PB 0x00000000d1200000| Untracked |  0
| 247|0x00000000d1300000, 0x00000000d1300000, 0x00000000d1400000|  0%| F|  |TAMS 0x00000000d1300000| PB 0x00000000d1300000| Untracked |  0
| 248|0x00000000d1400000, 0x00000000d1400000, 0x00000000d1500000|  0%| F|  |TAMS 0x00000000d1400000| PB 0x00000000d1400000| Untracked |  0
| 249|0x00000000d1500000, 0x00000000d1500000, 0x00000000d1600000|  0%| F|  |TAMS 0x00000000d1500000| PB 0x00000000d1500000| Untracked |  0
| 250|0x00000000d1600000, 0x00000000d1600000, 0x00000000d1700000|  0%| F|  |TAMS 0x00000000d1600000| PB 0x00000000d1600000| Untracked |  0
| 251|0x00000000d1700000, 0x00000000d1700000, 0x00000000d1800000|  0%| F|  |TAMS 0x00000000d1700000| PB 0x00000000d1700000| Untracked |  0
| 252|0x00000000d1800000, 0x00000000d1800000, 0x00000000d1900000|  0%| F|  |TAMS 0x00000000d1800000| PB 0x00000000d1800000| Untracked |  0
| 253|0x00000000d1900000, 0x00000000d1900000, 0x00000000d1a00000|  0%| F|  |TAMS 0x00000000d1900000| PB 0x00000000d1900000| Untracked |  0
| 254|0x00000000d1a00000, 0x00000000d1a00000, 0x00000000d1b00000|  0%| F|  |TAMS 0x00000000d1a00000| PB 0x00000000d1a00000| Untracked |  0
| 255|0x00000000d1b00000, 0x00000000d1b00000, 0x00000000d1c00000|  0%| F|  |TAMS 0x00000000d1b00000| PB 0x00000000d1b00000| Untracked |  0
| 256|0x00000000d1c00000, 0x00000000d1c00000, 0x00000000d1d00000|  0%| F|  |TAMS 0x00000000d1c00000| PB 0x00000000d1c00000| Untracked |  0
| 257|0x00000000d1d00000, 0x00000000d1d00000, 0x00000000d1e00000|  0%| F|  |TAMS 0x00000000d1d00000| PB 0x00000000d1d00000| Untracked |  0
| 258|0x00000000d1e00000, 0x00000000d1e00000, 0x00000000d1f00000|  0%| F|  |TAMS 0x00000000d1e00000| PB 0x00000000d1e00000| Untracked |  0
| 259|0x00000000d1f00000, 0x00000000d1f00000, 0x00000000d2000000|  0%| F|  |TAMS 0x00000000d1f00000| PB 0x00000000d1f00000| Untracked |  0
| 260|0x00000000d2000000, 0x00000000d2000000, 0x00000000d2100000|  0%| F|  |TAMS 0x00000000d2000000| PB 0x00000000d2000000| Untracked |  0
| 261|0x00000000d2100000, 0x00000000d2100000, 0x00000000d2200000|  0%| F|  |TAMS 0x00000000d2100000| PB 0x00000000d2100000| Untracked |  0
| 262|0x00000000d2200000, 0x00000000d2200000, 0x00000000d2300000|  0%| F|  |TAMS 0x00000000d2200000| PB 0x00000000d2200000| Untracked |  0
| 263|0x00000000d2300000, 0x00000000d2300000, 0x00000000d2400000|  0%| F|  |TAMS 0x00000000d2300000| PB 0x00000000d2300000| Untracked |  0
| 264|0x00000000d2400000, 0x00000000d2400000, 0x00000000d2500000|  0%| F|  |TAMS 0x00000000d2400000| PB 0x00000000d2400000| Untracked |  0
| 265|0x00000000d2500000, 0x00000000d2580000, 0x00000000d2600000| 50%| E|  |TAMS 0x00000000d2500000| PB 0x00000000d2500000| Complete |  0
| 266|0x00000000d2600000, 0x00000000d2700000, 0x00000000d2700000|100%| E|CS|TAMS 0x00000000d2600000| PB 0x00000000d2600000| Complete |  0
| 267|0x00000000d2700000, 0x00000000d2800000, 0x00000000d2800000|100%| E|CS|TAMS 0x00000000d2700000| PB 0x00000000d2700000| Complete |  0
| 268|0x00000000d2800000, 0x00000000d2900000, 0x00000000d2900000|100%| E|CS|TAMS 0x00000000d2800000| PB 0x00000000d2800000| Complete |  0
| 269|0x00000000d2900000, 0x00000000d2a00000, 0x00000000d2a00000|100%| E|CS|TAMS 0x00000000d2900000| PB 0x00000000d2900000| Complete |  0
| 270|0x00000000d2a00000, 0x00000000d2b00000, 0x00000000d2b00000|100%| E|CS|TAMS 0x00000000d2a00000| PB 0x00000000d2a00000| Complete |  0
| 271|0x00000000d2b00000, 0x00000000d2c00000, 0x00000000d2c00000|100%| E|CS|TAMS 0x00000000d2b00000| PB 0x00000000d2b00000| Complete |  0
| 272|0x00000000d2c00000, 0x00000000d2d00000, 0x00000000d2d00000|100%| E|CS|TAMS 0x00000000d2c00000| PB 0x00000000d2c00000| Complete |  0
| 273|0x00000000d2d00000, 0x00000000d2e00000, 0x00000000d2e00000|100%| E|CS|TAMS 0x00000000d2d00000| PB 0x00000000d2d00000| Complete |  0
| 274|0x00000000d2e00000, 0x00000000d2f00000, 0x00000000d2f00000|100%| E|CS|TAMS 0x00000000d2e00000| PB 0x00000000d2e00000| Complete |  0
| 275|0x00000000d2f00000, 0x00000000d3000000, 0x00000000d3000000|100%| E|CS|TAMS 0x00000000d2f00000| PB 0x00000000d2f00000| Complete |  0
| 276|0x00000000d3000000, 0x00000000d3100000, 0x00000000d3100000|100%| E|CS|TAMS 0x00000000d3000000| PB 0x00000000d3000000| Complete |  0
| 277|0x00000000d3100000, 0x00000000d3200000, 0x00000000d3200000|100%| E|CS|TAMS 0x00000000d3100000| PB 0x00000000d3100000| Complete |  0
| 278|0x00000000d3200000, 0x00000000d3300000, 0x00000000d3300000|100%| E|CS|TAMS 0x00000000d3200000| PB 0x00000000d3200000| Complete |  0
| 279|0x00000000d3300000, 0x00000000d3400000, 0x00000000d3400000|100%| E|CS|TAMS 0x00000000d3300000| PB 0x00000000d3300000| Complete |  0
| 280|0x00000000d3400000, 0x00000000d3500000, 0x00000000d3500000|100%| E|CS|TAMS 0x00000000d3400000| PB 0x00000000d3400000| Complete |  0
| 281|0x00000000d3500000, 0x00000000d3600000, 0x00000000d3600000|100%| E|CS|TAMS 0x00000000d3500000| PB 0x00000000d3500000| Complete |  0
| 282|0x00000000d3600000, 0x00000000d3700000, 0x00000000d3700000|100%| E|CS|TAMS 0x00000000d3600000| PB 0x00000000d3600000| Complete |  0
| 283|0x00000000d3700000, 0x00000000d3800000, 0x00000000d3800000|100%| E|CS|TAMS 0x00000000d3700000| PB 0x00000000d3700000| Complete |  0
| 284|0x00000000d3800000, 0x00000000d3900000, 0x00000000d3900000|100%| E|CS|TAMS 0x00000000d3800000| PB 0x00000000d3800000| Complete |  0
| 285|0x00000000d3900000, 0x00000000d3a00000, 0x00000000d3a00000|100%| E|CS|TAMS 0x00000000d3900000| PB 0x00000000d3900000| Complete |  0
| 286|0x00000000d3a00000, 0x00000000d3b00000, 0x00000000d3b00000|100%| E|  |TAMS 0x00000000d3a00000| PB 0x00000000d3a00000| Complete |  0
| 287|0x00000000d3b00000, 0x00000000d3c00000, 0x00000000d3c00000|100%| E|CS|TAMS 0x00000000d3b00000| PB 0x00000000d3b00000| Complete |  0
| 288|0x00000000d3c00000, 0x00000000d3d00000, 0x00000000d3d00000|100%| E|CS|TAMS 0x00000000d3c00000| PB 0x00000000d3c00000| Complete |  0
| 289|0x00000000d3d00000, 0x00000000d3e00000, 0x00000000d3e00000|100%| E|CS|TAMS 0x00000000d3d00000| PB 0x00000000d3d00000| Complete |  0
| 290|0x00000000d3e00000, 0x00000000d3f00000, 0x00000000d3f00000|100%| E|CS|TAMS 0x00000000d3e00000| PB 0x00000000d3e00000| Complete |  0
| 291|0x00000000d3f00000, 0x00000000d4000000, 0x00000000d4000000|100%| E|CS|TAMS 0x00000000d3f00000| PB 0x00000000d3f00000| Complete |  0
| 292|0x00000000d4000000, 0x00000000d4100000, 0x00000000d4100000|100%| E|CS|TAMS 0x00000000d4000000| PB 0x00000000d4000000| Complete |  0
| 293|0x00000000d4100000, 0x00000000d4200000, 0x00000000d4200000|100%| E|CS|TAMS 0x00000000d4100000| PB 0x00000000d4100000| Complete |  0
| 294|0x00000000d4200000, 0x00000000d4300000, 0x00000000d4300000|100%| E|CS|TAMS 0x00000000d4200000| PB 0x00000000d4200000| Complete |  0
| 295|0x00000000d4300000, 0x00000000d4400000, 0x00000000d4400000|100%| E|CS|TAMS 0x00000000d4300000| PB 0x00000000d4300000| Complete |  0
| 296|0x00000000d4400000, 0x00000000d4500000, 0x00000000d4500000|100%| E|CS|TAMS 0x00000000d4400000| PB 0x00000000d4400000| Complete |  0
| 297|0x00000000d4500000, 0x00000000d4600000, 0x00000000d4600000|100%| E|CS|TAMS 0x00000000d4500000| PB 0x00000000d4500000| Complete |  0
| 298|0x00000000d4600000, 0x00000000d4700000, 0x00000000d4700000|100%| E|CS|TAMS 0x00000000d4600000| PB 0x00000000d4600000| Complete |  0
| 299|0x00000000d4700000, 0x00000000d4800000, 0x00000000d4800000|100%| E|CS|TAMS 0x00000000d4700000| PB 0x00000000d4700000| Complete |  0
| 300|0x00000000d4800000, 0x00000000d4900000, 0x00000000d4900000|100%| E|CS|TAMS 0x00000000d4800000| PB 0x00000000d4800000| Complete |  0
| 301|0x00000000d4900000, 0x00000000d4a00000, 0x00000000d4a00000|100%| E|CS|TAMS 0x00000000d4900000| PB 0x00000000d4900000| Complete |  0
| 302|0x00000000d4a00000, 0x00000000d4b00000, 0x00000000d4b00000|100%| E|CS|TAMS 0x00000000d4a00000| PB 0x00000000d4a00000| Complete |  0
| 303|0x00000000d4b00000, 0x00000000d4c00000, 0x00000000d4c00000|100%| E|CS|TAMS 0x00000000d4b00000| PB 0x00000000d4b00000| Complete |  0
| 304|0x00000000d4c00000, 0x00000000d4d00000, 0x00000000d4d00000|100%| E|CS|TAMS 0x00000000d4c00000| PB 0x00000000d4c00000| Complete |  0
| 305|0x00000000d4d00000, 0x00000000d4e00000, 0x00000000d4e00000|100%| E|CS|TAMS 0x00000000d4d00000| PB 0x00000000d4d00000| Complete |  0
| 306|0x00000000d4e00000, 0x00000000d4f00000, 0x00000000d4f00000|100%| E|CS|TAMS 0x00000000d4e00000| PB 0x00000000d4e00000| Complete |  0
| 307|0x00000000d4f00000, 0x00000000d5000000, 0x00000000d5000000|100%| E|CS|TAMS 0x00000000d4f00000| PB 0x00000000d4f00000| Complete |  0
| 308|0x00000000d5000000, 0x00000000d5100000, 0x00000000d5100000|100%| E|CS|TAMS 0x00000000d5000000| PB 0x00000000d5000000| Complete |  0
| 309|0x00000000d5100000, 0x00000000d5200000, 0x00000000d5200000|100%| E|CS|TAMS 0x00000000d5100000| PB 0x00000000d5100000| Complete |  0
| 310|0x00000000d5200000, 0x00000000d5300000, 0x00000000d5300000|100%| E|CS|TAMS 0x00000000d5200000| PB 0x00000000d5200000| Complete |  0
| 311|0x00000000d5300000, 0x00000000d5400000, 0x00000000d5400000|100%| E|CS|TAMS 0x00000000d5300000| PB 0x00000000d5300000| Complete |  0
| 312|0x00000000d5400000, 0x00000000d5500000, 0x00000000d5500000|100%| E|CS|TAMS 0x00000000d5400000| PB 0x00000000d5400000| Complete |  0
| 313|0x00000000d5500000, 0x00000000d5600000, 0x00000000d5600000|100%| E|CS|TAMS 0x00000000d5500000| PB 0x00000000d5500000| Complete |  0
| 314|0x00000000d5600000, 0x00000000d5700000, 0x00000000d5700000|100%| E|CS|TAMS 0x00000000d5600000| PB 0x00000000d5600000| Complete |  0
| 976|0x00000000fec00000, 0x00000000fed00000, 0x00000000fed00000|100%| E|CS|TAMS 0x00000000fec00000| PB 0x00000000fec00000| Complete |  0
| 977|0x00000000fed00000, 0x00000000fee00000, 0x00000000fee00000|100%| E|CS|TAMS 0x00000000fed00000| PB 0x00000000fed00000| Complete |  0
| 978|0x00000000fee00000, 0x00000000fef00000, 0x00000000fef00000|100%| E|CS|TAMS 0x00000000fee00000| PB 0x00000000fee00000| Complete |  0
| 979|0x00000000fef00000, 0x00000000ff000000, 0x00000000ff000000|100%| E|CS|TAMS 0x00000000fef00000| PB 0x00000000fef00000| Complete |  0
| 980|0x00000000ff000000, 0x00000000ff100000, 0x00000000ff100000|100%| E|CS|TAMS 0x00000000ff000000| PB 0x00000000ff000000| Complete |  0
| 981|0x00000000ff100000, 0x00000000ff200000, 0x00000000ff200000|100%| E|CS|TAMS 0x00000000ff100000| PB 0x00000000ff100000| Complete |  0
| 982|0x00000000ff200000, 0x00000000ff300000, 0x00000000ff300000|100%| E|CS|TAMS 0x00000000ff200000| PB 0x00000000ff200000| Complete |  0
| 983|0x00000000ff300000, 0x00000000ff400000, 0x00000000ff400000|100%| E|CS|TAMS 0x00000000ff300000| PB 0x00000000ff300000| Complete |  0
| 984|0x00000000ff400000, 0x00000000ff500000, 0x00000000ff500000|100%| E|CS|TAMS 0x00000000ff400000| PB 0x00000000ff400000| Complete |  0
| 985|0x00000000ff500000, 0x00000000ff600000, 0x00000000ff600000|100%| E|CS|TAMS 0x00000000ff500000| PB 0x00000000ff500000| Complete |  0
| 986|0x00000000ff600000, 0x00000000ff700000, 0x00000000ff700000|100%| O|  |TAMS 0x00000000ff600000| PB 0x00000000ff600000| Untracked |  0
| 987|0x00000000ff700000, 0x00000000ff800000, 0x00000000ff800000|100%| O|  |TAMS 0x00000000ff700000| PB 0x00000000ff700000| Untracked |  0
| 988|0x00000000ff800000, 0x00000000ff900000, 0x00000000ff900000|100%| O|  |TAMS 0x00000000ff800000| PB 0x00000000ff800000| Untracked |  0
| 989|0x00000000ff900000, 0x00000000ffa00000, 0x00000000ffa00000|100%| O|  |TAMS 0x00000000ff900000| PB 0x00000000ff900000| Untracked |  0
| 990|0x00000000ffa00000, 0x00000000ffb00000, 0x00000000ffb00000|100%| O|  |TAMS 0x00000000ffa00000| PB 0x00000000ffa00000| Untracked |  0
| 991|0x00000000ffb00000, 0x00000000ffc00000, 0x00000000ffc00000|100%| O|  |TAMS 0x00000000ffb00000| PB 0x00000000ffb00000| Untracked |  0
| 992|0x00000000ffc00000, 0x00000000ffd00000, 0x00000000ffd00000|100%| O|  |TAMS 0x00000000ffc00000| PB 0x00000000ffc00000| Untracked |  0
| 993|0x00000000ffd00000, 0x00000000ffe00000, 0x00000000ffe00000|100%| O|  |TAMS 0x00000000ffd00000| PB 0x00000000ffd00000| Untracked |  0
| 994|0x00000000ffe00000, 0x00000000fff00000, 0x00000000fff00000|100%| O|  |TAMS 0x00000000ffe00000| PB 0x00000000ffe00000| Untracked |  0
| 995|0x00000000fff00000, 0x0000000100000000, 0x0000000100000000|100%| O|  |TAMS 0x00000000fff00000| PB 0x00000000fff00000| Untracked |  0

Card table byte_map: [0x0000007475070000,0x0000007475270000] _byte_map_base: 0x0000007474a62000

Marking Bits: (CMBitMap*) 0x000000746cb76820
 Bits: [0x0000007475270000, 0x0000007476200000)

Polling page: 0x000000746aba0000

Metaspace:

Usage:
  Non-class:     84.46 MB used.
      Class:     12.86 MB used.
       Both:     97.32 MB used.

Virtual space:
  Non-class space:      128.00 MB reserved,      85.00 MB ( 66%) committed,  2 nodes.
      Class space:        1.00 GB reserved,      13.19 MB (  1%) committed,  1 nodes.
             Both:        1.12 GB reserved,      98.19 MB (  9%) committed. 

Chunk freelists:
   Non-Class:  9.98 MB
       Class:  2.82 MB
        Both:  12.80 MB

MaxMetaspaceSize: unlimited
CompressedClassSpaceSize: 1.00 GB
Initial GC threshold: 21.00 MB
Current GC threshold: 128.56 MB
CDS: on
 - commit_granule_bytes: 65536.
 - commit_granule_words: 8192.
 - virtual_space_node_default_size: 8388608.
 - enlarge_chunks_in_place: 1.
 - use_allocation_guard: 0.


Internal statistics:

num_allocs_failed_limit: 42.
num_arena_births: 1254.
num_arena_deaths: 0.
num_vsnodes_births: 3.
num_vsnodes_deaths: 0.
num_space_committed: 1567.
num_space_uncommitted: 0.
num_chunks_returned_to_freelist: 42.
num_chunks_taken_from_freelist: 4468.
num_chunk_merges: 15.
num_chunk_splits: 3121.
num_chunks_enlarged: 2418.
num_inconsistent_stats: 0.

CodeHeap 'non-profiled nmethods': size=120000Kb used=5594Kb max_used=5594Kb free=114406Kb
 bounds [0x0000007407ad0000, 0x0000007408050000, 0x000000740f000000]
CodeHeap 'profiled nmethods': size=120000Kb used=13217Kb max_used=13359Kb free=106783Kb
 bounds [0x0000007400000000, 0x0000007400d20000, 0x0000007407530000]
CodeHeap 'non-nmethods': size=5760Kb used=2428Kb max_used=2474Kb free=3331Kb
 bounds [0x0000007407530000, 0x00000074077b0000, 0x0000007407ad0000]
 total_blobs=9482 nmethods=8169 adapters=1217
 compilation: enabled
              stopped_count=0, restarted_count=0
 full_count=0

Compilation events (20 events):
Event: 18.711 Thread 0x000000745016b380 10289   !   3       java.io.BufferedReader$1::hasNext (43 bytes)
Event: 18.712 Thread 0x000000745016b380 nmethod 10289 0x00000074002b1610 code [0x00000074002b17e0, 0x00000074002b1cb8]
Event: 18.712 Thread 0x000000745016b380 10292       3       java.io.BufferedReader$1::next (5 bytes)
Event: 18.712 Thread 0x000000745016b380 nmethod 10292 0x000000740076d090 code [0x000000740076d260, 0x000000740076d590]
Event: 18.712 Thread 0x000000745016b380 10297       3       java.util.regex.Pattern$BnM::optimize (179 bytes)
Event: 18.713 Thread 0x000000745016b380 nmethod 10297 0x00000074008e7d90 code [0x00000074008e7fe0, 0x00000074008e8d00]
Event: 18.713 Thread 0x000000745016b380 10293       3       java.io.BufferedReader$1::next (34 bytes)
Event: 18.713 Thread 0x000000745016b380 nmethod 10293 0x000000740076ca10 code [0x000000740076cbe0, 0x000000740076cea0]
Event: 18.713 Thread 0x000000745016b380 10294       3       jdk.internal.org.jline.utils.InfoCmp$$Lambda/0x0000007410d2a678::apply (8 bytes)
Event: 18.713 Thread 0x000000745016b380 nmethod 10294 0x00000074008e7690 code [0x00000074008e7860, 0x00000074008e7c60]
Event: 18.713 Thread 0x000000745016b380 10295       3       jdk.internal.org.jline.utils.InfoCmp$$Lambda/0x0000007410d2a8b0::test (8 bytes)
Event: 18.714 Thread 0x000000745016b380 nmethod 10295 0x00000074008e7010 code [0x00000074008e71e0, 0x00000074008e7528]
Event: 18.714 Thread 0x000000745016b380 10296       3       jdk.internal.org.jline.utils.InfoCmp::lambda$getCapabilitiesByName$0 (15 bytes)
Event: 18.714 Thread 0x000000745016b380 nmethod 10296 0x00000074008e6b90 code [0x00000074008e6d40, 0x00000074008e6f30]
Event: 18.714 Thread 0x000000745016b380 10298       3       jdk.internal.org.jline.utils.InfoCmp$$Lambda/0x0000007410d2aaf8::test (8 bytes)
Event: 18.714 Thread 0x000000745016b380 nmethod 10298 0x00000074008e6510 code [0x00000074008e66c0, 0x00000074008e6a10]
Event: 18.714 Thread 0x000000745016b380 10300       3       java.util.regex.Pattern$CharProperty::study (29 bytes)
Event: 18.715 Thread 0x000000745016b380 nmethod 10300 0x00000074008e6090 code [0x00000074008e6240, 0x00000074008e6438]
Event: 18.716 Thread 0x000000745828bf10 nmethod 10266 0x0000007408035290 code [0x00000074080355a0, 0x0000007408035fd0]
Event: 18.716 Thread 0x000000745828bf10 10299       4       java.util.regex.Matcher::find (69 bytes)

GC Heap History (20 events):
Event: 10.554 GC heap before
{Heap before GC invocations=26 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 241664K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 116 young (118784K), 17 survivors (17408K)
 Metaspace       used 54363K, committed 55104K, reserved 1114112K
  class space    used 7687K, committed 8000K, reserved 1048576K
}
Event: 10.592 GC heap after
{Heap after GC invocations=27 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 161280K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 15 young (15360K), 15 survivors (15360K)
 Metaspace       used 54363K, committed 55104K, reserved 1114112K
  class space    used 7687K, committed 8000K, reserved 1048576K
}
Event: 11.322 GC heap before
{Heap before GC invocations=27 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 197120K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 51 young (52224K), 15 survivors (15360K)
 Metaspace       used 60958K, committed 61696K, reserved 1114112K
  class space    used 9010K, committed 9344K, reserved 1048576K
}
Event: 11.344 GC heap after
{Heap after GC invocations=28 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 167424K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 6 young (6144K), 6 survivors (6144K)
 Metaspace       used 60958K, committed 61696K, reserved 1114112K
  class space    used 9010K, committed 9344K, reserved 1048576K
}
Event: 12.883 GC heap before
{Heap before GC invocations=29 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 256512K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 92 young (94208K), 6 survivors (6144K)
 Metaspace       used 68175K, committed 68992K, reserved 1114112K
  class space    used 9968K, committed 10304K, reserved 1048576K
}
Event: 12.899 GC heap after
{Heap after GC invocations=30 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 178176K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 12 young (12288K), 12 survivors (12288K)
 Metaspace       used 68175K, committed 68992K, reserved 1114112K
  class space    used 9968K, committed 10304K, reserved 1048576K
}
Event: 13.471 GC heap before
{Heap before GC invocations=30 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 260096K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 92 young (94208K), 12 survivors (12288K)
 Metaspace       used 69839K, committed 70656K, reserved 1114112K
  class space    used 10259K, committed 10624K, reserved 1048576K
}
Event: 13.489 GC heap after
{Heap after GC invocations=31 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 179706K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 5 young (5120K), 5 survivors (5120K)
 Metaspace       used 69839K, committed 70656K, reserved 1114112K
  class space    used 10259K, committed 10624K, reserved 1048576K
}
Event: 14.152 GC heap before
{Heap before GC invocations=31 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 262650K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 87 young (89088K), 5 survivors (5120K)
 Metaspace       used 73061K, committed 73856K, reserved 1114112K
  class space    used 10865K, committed 11200K, reserved 1048576K
}
Event: 14.167 GC heap after
{Heap after GC invocations=32 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 186362K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 11 young (11264K), 11 survivors (11264K)
 Metaspace       used 73061K, committed 73856K, reserved 1114112K
  class space    used 10865K, committed 11200K, reserved 1048576K
}
Event: 14.531 GC heap before
{Heap before GC invocations=32 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 267258K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 90 young (92160K), 11 survivors (11264K)
 Metaspace       used 73131K, committed 73920K, reserved 1114112K
  class space    used 10876K, committed 11200K, reserved 1048576K
}
Event: 14.546 GC heap after
{Heap after GC invocations=33 (full 0):
 garbage-first heap   total reserved 1019904K, committed 293888K, used 188416K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 7 young (7168K), 7 survivors (7168K)
 Metaspace       used 73131K, committed 73920K, reserved 1114112K
  class space    used 10876K, committed 11200K, reserved 1048576K
}
Event: 15.110 GC heap before
{Heap before GC invocations=34 (full 0):
 garbage-first heap   total reserved 1019904K, committed 314368K, used 269312K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 86 young (88064K), 7 survivors (7168K)
 Metaspace       used 73970K, committed 74816K, reserved 1114112K
  class space    used 11034K, committed 11392K, reserved 1048576K
}
Event: 15.125 GC heap after
{Heap after GC invocations=35 (full 0):
 garbage-first heap   total reserved 1019904K, committed 314368K, used 192186K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 5 young (5120K), 5 survivors (5120K)
 Metaspace       used 73970K, committed 74816K, reserved 1114112K
  class space    used 11034K, committed 11392K, reserved 1048576K
}
Event: 15.410 GC heap before
{Heap before GC invocations=35 (full 0):
 garbage-first heap   total reserved 1019904K, committed 314368K, used 287418K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 98 young (100352K), 5 survivors (5120K)
 Metaspace       used 74321K, committed 75200K, reserved 1114112K
  class space    used 11099K, committed 11456K, reserved 1048576K
}
Event: 15.424 GC heap after
{Heap after GC invocations=36 (full 0):
 garbage-first heap   total reserved 1019904K, committed 314368K, used 192025K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 7 young (7168K), 7 survivors (7168K)
 Metaspace       used 74321K, committed 75200K, reserved 1114112K
  class space    used 11099K, committed 11456K, reserved 1048576K
}
Event: 15.531 GC heap before
{Heap before GC invocations=36 (full 0):
 garbage-first heap   total reserved 1019904K, committed 314368K, used 290329K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 103 young (105472K), 7 survivors (7168K)
 Metaspace       used 74331K, committed 75200K, reserved 1114112K
  class space    used 11099K, committed 11456K, reserved 1048576K
}
Event: 15.549 GC heap after
{Heap after GC invocations=37 (full 0):
 garbage-first heap   total reserved 1019904K, committed 343040K, used 193634K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 9 young (9216K), 9 survivors (9216K)
 Metaspace       used 74331K, committed 75200K, reserved 1114112K
  class space    used 11099K, committed 11456K, reserved 1048576K
}
Event: 17.282 GC heap before
{Heap before GC invocations=38 (full 0):
 garbage-first heap   total reserved 1019904K, committed 343040K, used 316514K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 127 young (130048K), 9 survivors (9216K)
 Metaspace       used 94414K, committed 95296K, reserved 1179648K
  class space    used 12592K, committed 12992K, reserved 1048576K
}
Event: 17.303 GC heap after
{Heap after GC invocations=39 (full 0):
 garbage-first heap   total reserved 1019904K, committed 343040K, used 197435K [0x00000000c1c00000, 0x0000000100000000)
  region size 1024K, 10 young (10240K), 10 survivors (10240K)
 Metaspace       used 94414K, committed 95296K, reserved 1179648K
  class space    used 12592K, committed 12992K, reserved 1048576K
}

Dll operation events (18 events):
Event: 0.007 Loaded shared library C:\Program Files\Java\jdk-22\bin\java.dll
Event: 0.044 Loaded shared library C:\Program Files\Java\jdk-22\bin\jsvml.dll
Event: 0.070 Loaded shared library C:\Program Files\Java\jdk-22\bin\net.dll
Event: 0.071 Loaded shared library C:\Program Files\Java\jdk-22\bin\nio.dll
Event: 0.077 Loaded shared library C:\Program Files\Java\jdk-22\bin\zip.dll
Event: 0.098 Loaded shared library C:\Program Files\Java\jdk-22\bin\jimage.dll
Event: 1.853 Loaded shared library C:\Program Files\Java\jdk-22\bin\management.dll
Event: 1.855 Loaded shared library C:\Program Files\Java\jdk-22\bin\management_ext.dll
Event: 2.374 Loaded shared library C:\Users\itzhak\AppData\Local\Temp\jansi-2.4.0-79354dc56ce1a544-jansi.dll
Event: 2.724 Loaded shared library C:\Program Files\Java\jdk-22\bin\verify.dll
Event: 3.047 Loaded shared library C:\Users\itzhak\AppData\Local\Temp\jna--1178040445\jna6223384270940846085.dll
Event: 11.316 Loaded shared library C:\Program Files\Java\jdk-22\bin\jaas.dll
Event: 11.620 Loaded shared library C:\Program Files\Java\jdk-22\bin\sunmscapi.dll
Event: 11.754 Loaded shared library C:\Program Files\Java\jdk-22\bin\extnet.dll
Event: 15.676 Loaded shared library C:\Program Files\Java\jdk-22\bin\awt.dll
Event: 16.078 Loaded shared library C:\Program Files\Java\jdk-22\bin\freetype.dll
Event: 16.078 Loaded shared library C:\Program Files\Java\jdk-22\bin\fontmanager.dll
Event: 18.647 Loaded shared library C:\Program Files\Java\jdk-22\bin\le.dll

Deoptimization events (20 events):
Event: 18.522 Thread 0x000000745a924f90 Uncommon trap: trap_request=0xffffffde fr.pc=0x0000007407bee198 relative=0x0000000000000078
Event: 18.522 Thread 0x000000745a924f90 Uncommon trap: reason=class_check action=maybe_recompile pc=0x0000007407bee198 method=java.util.LinkedHashMap.afterNodeInsertion(Z)V @ 15 c2
Event: 18.522 Thread 0x000000745a924f90 DEOPT PACKING pc=0x0000007407bee198 sp=0x00000074603fe910
Event: 18.522 Thread 0x000000745a924f90 DEOPT UNPACKING pc=0x00000074075846a2 sp=0x00000074603fe888 mode 2
Event: 18.640 Thread 0x000000745a924f90 Uncommon trap: trap_request=0xffffff45 fr.pc=0x0000007408033598 relative=0x0000000000000178
Event: 18.640 Thread 0x000000745a924f90 Uncommon trap: reason=unstable_if action=reinterpret pc=0x0000007408033598 method=java.lang.invoke.MethodHandle.isBuiltinLoader(Ljava/lang/ClassLoader;)Z @ 15 c2
Event: 18.640 Thread 0x000000745a924f90 DEOPT PACKING pc=0x0000007408033598 sp=0x00000074603faa90
Event: 18.640 Thread 0x000000745a924f90 DEOPT UNPACKING pc=0x00000074075846a2 sp=0x00000074603fa950 mode 2
Event: 18.702 Thread 0x000000745a924f90 Uncommon trap: trap_request=0xffffffde fr.pc=0x0000007407e35bec relative=0x0000000000002b4c
Event: 18.702 Thread 0x000000745a924f90 Uncommon trap: reason=class_check action=maybe_recompile pc=0x0000007407e35bec method=java.util.HashMap.putVal(ILjava/lang/Object;Ljava/lang/Object;ZZ)Ljava/lang/Object; @ 203 c2
Event: 18.702 Thread 0x000000745a924f90 DEOPT PACKING pc=0x0000007407e35bec sp=0x00000074603fb210
Event: 18.702 Thread 0x000000745a924f90 DEOPT UNPACKING pc=0x00000074075846a2 sp=0x00000074603fb1f0 mode 2
Event: 18.715 Thread 0x000000745a924f90 Uncommon trap: trap_request=0xffffff45 fr.pc=0x0000007407bbd834 relative=0x00000000000004b4
Event: 18.715 Thread 0x000000745a924f90 Uncommon trap: reason=unstable_if action=reinterpret pc=0x0000007407bbd834 method=java.util.regex.Matcher.search(I)Z @ 76 c2
Event: 18.715 Thread 0x000000745a924f90 DEOPT PACKING pc=0x0000007407bbd834 sp=0x00000074603fb5c0
Event: 18.715 Thread 0x000000745a924f90 DEOPT UNPACKING pc=0x00000074075846a2 sp=0x00000074603fb580 mode 2
Event: 18.715 Thread 0x000000745a924f90 Uncommon trap: trap_request=0xffffff45 fr.pc=0x0000007408033bf0 relative=0x00000000000001b0
Event: 18.715 Thread 0x000000745a924f90 Uncommon trap: reason=unstable_if action=reinterpret pc=0x0000007408033bf0 method=java.lang.invoke.MethodHandle.isBuiltinLoader(Ljava/lang/ClassLoader;)Z @ 15 c2
Event: 18.715 Thread 0x000000745a924f90 DEOPT PACKING pc=0x0000007408033bf0 sp=0x00000074603fab90
Event: 18.715 Thread 0x000000745a924f90 DEOPT UNPACKING pc=0x00000074075846a2 sp=0x00000074603faa48 mode 2

Classes loaded (20 events):
Event: 18.650 Loading class java/lang/ProcessHandle$Info
Event: 18.650 Loading class java/lang/ProcessHandle$Info done
Event: 18.650 Loading class java/lang/ProcessHandleImpl
Event: 18.651 Loading class java/lang/ProcessHandleImpl done
Event: 18.655 Loading class java/lang/ProcessHandleImpl$Info
Event: 18.655 Loading class java/lang/ProcessHandleImpl$Info done
Event: 18.693 Loading class java/nio/charset/MalformedInputException
Event: 18.693 Loading class java/nio/charset/MalformedInputException done
Event: 18.694 Loading class java/nio/charset/UnmappableCharacterException
Event: 18.694 Loading class java/nio/charset/UnmappableCharacterException done
Event: 18.695 Loading class java/io/FileReader
Event: 18.695 Loading class java/io/FileReader done
Event: 18.696 Loading class java/io/BufferedReader$1
Event: 18.696 Loading class java/io/BufferedReader$1 done
Event: 18.717 Loading class java/io/ProxyingConsole
Event: 18.717 Loading class java/io/ProxyingConsole done
Event: 18.717 Loading class java/io/Console$1
Event: 18.717 Loading class jdk/internal/access/JavaIOAccess
Event: 18.717 Loading class jdk/internal/access/JavaIOAccess done
Event: 18.717 Loading class java/io/Console$1 done

Classes unloaded (0 events):
No events

Classes redefined (0 events):
No events

Internal exceptions (20 events):
Event: 18.300 Thread 0x000000745a924f90 Exception <a 'java/io/FileNotFoundException'{0x00000000d3a5f708}> (0x00000000d3a5f708) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.320 Thread 0x000000745a924f90 Exception <a 'java/io/FileNotFoundException'{0x00000000d3ae3bd0}> (0x00000000d3ae3bd0) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.323 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38e9100}> (0x00000000d38e9100) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.323 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38e96c8}> (0x00000000d38e96c8) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.334 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38ea260}> (0x00000000d38ea260) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.334 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38ea828}> (0x00000000d38ea828) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.468 Thread 0x000000745a924f90 Exception <a 'sun/nio/fs/WindowsException'{0x00000000d32087a0}> (0x00000000d32087a0) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.496 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d3077968}: 'void java.lang.invoke.DirectMethodHandle$Holder.invokeStatic(java.lang.Object, java.lang.Object, java.lang.Object, java.lang.Object, java.lang.Object, java.lang.Object, java.lang.Object, java.lang.Object)'> (0x00000000d3077968) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.504 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d30b6e98}: 'java.lang.Object java.lang.reflect.Field.get(java.lang.Object, java.lang.Class)'> (0x00000000d30b6e98) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.561 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d2d42a48}: 'java.lang.Object java.lang.invoke.DirectMethodHandle$Holder.invokeSpecial(java.lang.Object, java.lang.Object, int, int, int)'> (0x00000000d2d42a48) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.563 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38eb8e0}> (0x00000000d38eb8e0) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.563 Thread 0x0000007455e7c6d0 Exception <a 'java/io/IOException'{0x00000000d38ebea8}> (0x00000000d38ebea8) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.641 Thread 0x000000745a924f90 Exception <a 'sun/nio/fs/WindowsException'{0x00000000d2b376d8}> (0x00000000d2b376d8) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.650 Thread 0x000000745a924f90 Exception <a 'jdk/internal/org/jline/terminal/impl/jna/LastErrorException'{0x00000000d2b44278}> (0x00000000d2b44278) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.650 Thread 0x000000745a924f90 Exception <a 'jdk/internal/org/jline/terminal/impl/jna/LastErrorException'{0x00000000d2b44be8}> (0x00000000d2b44be8) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.650 Thread 0x000000745a924f90 Exception <a 'jdk/internal/org/jline/terminal/impl/jna/LastErrorException'{0x00000000d2b45508}> (0x00000000d2b45508) 
thrown [s\open\src\hotspot\share\prims\jni.cpp, line 520]
Event: 18.652 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d2b49a48}: 'java.lang.Object java.lang.invoke.DirectMethodHandle$Holder.invokeStatic(java.lang.Object, long, java.lang.Object)'> (0x00000000d2b49a48) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.652 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d2b4d538}: 'java.lang.Object java.lang.invoke.DirectMethodHandle$Holder.invokeStaticInit(java.lang.Object, long, java.lang.Object)'> (0x00000000d2b4d538) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.653 Thread 0x000000745a924f90 Exception <a 'java/lang/NoSuchMethodError'{0x00000000d2b52ac0}: 'java.lang.Object java.lang.invoke.DirectMethodHandle$Holder.newInvokeSpecial(java.lang.Object, long)'> (0x00000000d2b52ac0) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 774]
Event: 18.721 Thread 0x000000745a924f90 Exception <a 'java/lang/NullPointerException'{0x00000000d28f22a0}> (0x00000000d28f22a0) 
thrown [s\open\src\hotspot\share\interpreter\linkResolver.cpp, line 1374]

ZGC Phase Switch (0 events):
No events

VM Operations (20 events):
Event: 16.055 Executing VM operation: G1PauseCleanup
Event: 16.055 Executing VM operation: G1PauseCleanup done
Event: 16.124 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 16.124 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 16.393 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 16.393 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 16.533 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 16.534 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 16.537 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 16.537 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 17.281 Executing VM operation: G1CollectForAllocation (G1 Evacuation Pause)
Event: 17.303 Executing VM operation: G1CollectForAllocation (G1 Evacuation Pause) done
Event: 18.351 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 18.351 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 18.351 Executing VM operation: Cleanup
Event: 18.351 Executing VM operation: Cleanup done
Event: 18.694 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 18.694 Executing VM operation: HandshakeAllThreads (Deoptimize) done
Event: 18.696 Executing VM operation: HandshakeAllThreads (Deoptimize)
Event: 18.696 Executing VM operation: HandshakeAllThreads (Deoptimize) done

Events (20 events):
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400ad6210
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400afa410
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400bd1d90
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400bdc690
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400bdcc90
Event: 15.939 Thread 0x0000007450135630 flushing nmethod 0x0000007400c33a10
Event: 16.086 Thread 0x000000745696a120 Thread exited: 0x000000745696a120
Event: 16.403 Thread 0x00000074562a4150 Thread added: 0x00000074562a4150
Event: 16.416 Thread 0x00000074562a2710 Thread added: 0x00000074562a2710
Event: 16.523 Thread 0x00000074562a47e0 Thread added: 0x00000074562a47e0
Event: 16.523 Thread 0x000000745a924f90 Thread added: 0x000000745a924f90
Event: 16.597 Thread 0x000000745a922830 Thread added: 0x000000745a922830
Event: 16.597 Thread 0x000000745a923550 Thread added: 0x000000745a923550
Event: 16.597 Thread 0x000000745a9221a0 Thread added: 0x000000745a9221a0
Event: 16.597 Thread 0x000000745a924270 Thread added: 0x000000745a924270
Event: 16.614 Thread 0x00000074552c02e0 Thread added: 0x00000074552c02e0
Event: 17.475 Thread 0x00000074552c02e0 Thread exited: 0x00000074552c02e0
Event: 18.457 Thread 0x000000745828bf10 Thread added: 0x000000745828bf10
Event: 18.547 Thread 0x000000745a927060 Thread added: 0x000000745a927060
Event: 18.558 Thread 0x000000745a9269d0 Thread added: 0x000000745a9269d0


Dynamic libraries:
0x00007ff671f80000 - 0x00007ff671f90000 	C:\Program Files\Java\jdk-22\bin\javaw.exe
0x00007ffc183a0000 - 0x00007ffc1854c000 	C:\Windows\SYSTEM32\ntdll.dll
0x00007ffc15de0000 - 0x00007ffc15f1e000 	C:\Windows\system32\KERNEL32.DLL
0x00007ffc155c0000 - 0x00007ffc156d5000 	C:\Windows\system32\KERNELBASE.dll
0x00007ffc141d0000 - 0x00007ffc141e7000 	C:\Program Files\Java\jdk-22\bin\jli.dll
0x00007ffc11d80000 - 0x00007ffc11d9b000 	C:\Program Files\Java\jdk-22\bin\VCRUNTIME140.dll
0x00007ffc141c0000 - 0x00007ffc141c5000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-stdio-l1-1-0.dll
0x00007ffc140f0000 - 0x00007ffc140f5000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-runtime-l1-1-0.dll
0x00007ffc11e50000 - 0x00007ffc11e54000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-environment-l1-1-0.dll
0x00007ffc11090000 - 0x00007ffc11096000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-math-l1-1-0.dll
0x00007ffc10fa0000 - 0x00007ffc10fa4000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-locale-l1-1-0.dll
0x00007ffc10f90000 - 0x00007ffc10f94000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-heap-l1-1-0.dll
0x00007ffc16430000 - 0x00007ffc164da000 	C:\Windows\system32\ADVAPI32.dll
0x00007ffc10090000 - 0x00007ffc1030b000 	C:\Windows\WinSxS\amd64_microsoft.windows.common-controls_6595b64144ccf1df_6.0.9600.17415_none_6240486fecbd8abb\COMCTL32.dll
0x00007ffc15fa0000 - 0x00007ffc16117000 	C:\Windows\system32\USER32.dll
0x00007ffc0dd40000 - 0x00007ffc0dd4a000 	C:\Windows\SYSTEM32\VERSION.dll
0x00007ffc10990000 - 0x00007ffc10994000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-filesystem-l1-1-0.dll
0x00007ffc10760000 - 0x00007ffc10765000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-string-l1-1-0.dll
0x00007ffc10080000 - 0x00007ffc10085000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-convert-l1-1-0.dll
0x00007ffc182f0000 - 0x00007ffc1839a000 	C:\Windows\system32\msvcrt.dll
0x00007ffc16820000 - 0x00007ffc16879000 	C:\Windows\SYSTEM32\sechost.dll
0x00007ffc15ae0000 - 0x00007ffc15c21000 	C:\Windows\system32\RPCRT4.dll
0x00007ffc17da0000 - 0x00007ffc17ef1000 	C:\Windows\system32\GDI32.dll
0x00007ffc08200000 - 0x00007ffc08311000 	C:\Program Files\Java\jdk-22\bin\ucrtbase.DLL
0x00007ffc163f0000 - 0x00007ffc16426000 	C:\Windows\system32\IMM32.DLL
0x00007ffc18130000 - 0x00007ffc18283000 	C:\Windows\system32\MSCTF.dll
0x00007ffc10070000 - 0x00007ffc1007c000 	C:\Program Files\Java\jdk-22\bin\vcruntime140_1.dll
0x00007ffc0e1d0000 - 0x00007ffc0e25e000 	C:\Program Files\Java\jdk-22\bin\msvcp140.dll
0x00007ffc0fbe0000 - 0x00007ffc0fbe4000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-time-l1-1-0.dll
0x00007ffc0fbd0000 - 0x00007ffc0fbd4000 	C:\Program Files\Java\jdk-22\bin\api-ms-win-crt-utility-l1-1-0.dll
0x00007ffbfcd30000 - 0x00007ffbfda78000 	C:\Program Files\Java\jdk-22\bin\server\jvm.dll
0x00007ffc154c0000 - 0x00007ffc15506000 	C:\Windows\SYSTEM32\POWRPROF.dll
0x00007ffc180d0000 - 0x00007ffc1812a000 	C:\Windows\system32\WS2_32.dll
0x00007ffc10f20000 - 0x00007ffc10f42000 	C:\Windows\SYSTEM32\WINMM.dll
0x00007ffc15f20000 - 0x00007ffc15f29000 	C:\Windows\system32\NSI.dll
0x00007ffc10d90000 - 0x00007ffc10dba000 	C:\Windows\SYSTEM32\WINMMBASE.dll
0x00007ffc15920000 - 0x00007ffc1596f000 	C:\Windows\SYSTEM32\cfgmgr32.dll
0x00007ffc14350000 - 0x00007ffc14378000 	C:\Windows\SYSTEM32\DEVOBJ.dll
0x00007ffc0fbc0000 - 0x00007ffc0fbca000 	C:\Program Files\Java\jdk-22\bin\jimage.dll
0x00007ffc12ca0000 - 0x00007ffc12e2a000 	C:\Windows\SYSTEM32\DBGHELP.DLL
0x00007ffc0fba0000 - 0x00007ffc0fbbe000 	C:\Program Files\Java\jdk-22\bin\java.dll
0x00007ffc16880000 - 0x00007ffc17d99000 	C:\Windows\system32\SHELL32.dll
0x00007ffc17f00000 - 0x00007ffc18094000 	C:\Windows\system32\ole32.dll
0x00007ffc16600000 - 0x00007ffc16811000 	C:\Windows\SYSTEM32\combase.dll
0x00007ffc164e0000 - 0x00007ffc16534000 	C:\Windows\system32\SHLWAPI.dll
0x00007ffc12b20000 - 0x00007ffc12bd2000 	C:\Windows\SYSTEM32\SHCORE.dll
0x00007ffc154a0000 - 0x00007ffc154b5000 	C:\Windows\SYSTEM32\profapi.dll
0x00007ffc07b40000 - 0x00007ffc07c17000 	C:\Program Files\Java\jdk-22\bin\jsvml.dll
0x00007ffc0fb90000 - 0x00007ffc0fba0000 	C:\Program Files\Java\jdk-22\bin\net.dll
0x00007ffc14d00000 - 0x00007ffc14d59000 	C:\Windows\system32\mswsock.dll
0x00007ffc0fa50000 - 0x00007ffc0fa66000 	C:\Program Files\Java\jdk-22\bin\nio.dll
0x00007ffc0f130000 - 0x00007ffc0f147000 	C:\Program Files\Java\jdk-22\bin\zip.dll
0x00007ffc129f0000 - 0x00007ffc129fa000 	C:\Program Files\Java\jdk-22\bin\management.dll
0x00007ffc0fb80000 - 0x00007ffc0fb8b000 	C:\Program Files\Java\jdk-22\bin\management_ext.dll
0x00007ffc180c0000 - 0x00007ffc180c7000 	C:\Windows\system32\PSAPI.DLL
0x00007ffc11ca0000 - 0x00007ffc11cb5000 	C:\Windows\system32\napinsp.dll
0x00007ffc11cc0000 - 0x00007ffc11cda000 	C:\Windows\system32\pnrpnsp.dll
0x00007ffc11940000 - 0x00007ffc1195b000 	C:\Windows\system32\NLAapi.dll
0x00007ffc14b00000 - 0x00007ffc14ba4000 	C:\Windows\SYSTEM32\DNSAPI.dll
0x00007ffc11ce0000 - 0x00007ffc11ced000 	C:\Windows\System32\winrnr.dll
0x00007ffc11cf0000 - 0x00007ffc11d04000 	C:\Windows\system32\wshbth.dll
0x00007ffc12190000 - 0x00007ffc1219a000 	C:\Windows\System32\rasadhlp.dll
0x00007ffc11bc0000 - 0x00007ffc11bea000 	C:\Windows\SYSTEM32\IPHLPAPI.DLL
0x00007ffc11bb0000 - 0x00007ffc11bba000 	C:\Windows\SYSTEM32\WINNSI.DLL
0x00007ffc10320000 - 0x00007ffc1038b000 	C:\Windows\System32\fwpuclnt.dll
0x0000000069ac0000 - 0x0000000069ae4000 	C:\Users\itzhak\AppData\Local\Temp\jansi-2.4.0-79354dc56ce1a544-jansi.dll
0x00007ffc0fb70000 - 0x00007ffc0fb80000 	C:\Program Files\Java\jdk-22\bin\verify.dll
0x00007ffc14d60000 - 0x00007ffc14d80000 	C:\Windows\SYSTEM32\CRYPTSP.dll
0x00007ffc14980000 - 0x00007ffc149b6000 	C:\Windows\system32\rsaenh.dll
0x00007ffc14fb0000 - 0x00007ffc14fd6000 	C:\Windows\SYSTEM32\bcrypt.dll
0x00007ffc14a90000 - 0x00007ffc14ab1000 	C:\Windows\SYSTEM32\USERENV.dll
0x00007ffc152f0000 - 0x00007ffc15353000 	C:\Windows\system32\bcryptprimitives.dll
0x00007ffc15360000 - 0x00007ffc1536b000 	C:\Windows\SYSTEM32\CRYPTBASE.dll
0x00007ffc0fb20000 - 0x00007ffc0fb65000 	C:\Users\itzhak\AppData\Local\Temp\jna--1178040445\jna6223384270940846085.dll
0x00007ffc13a40000 - 0x00007ffc13a4b000 	C:\Windows\SYSTEM32\kernel.appcore.dll
0x00007ffc16540000 - 0x00007ffc165f6000 	C:\Windows\SYSTEM32\clbcatq.dll
0x00007ffc16120000 - 0x00007ffc161e1000 	C:\Windows\system32\OleAut32.dll
0x00007ffc09f80000 - 0x00007ffc09fcf000 	C:\Windows\SYSTEM32\Pdh.dll
0x00007ffc0fb00000 - 0x00007ffc0fb0d000 	C:\Windows\System32\perfos.dll
0x00007ffc0faf0000 - 0x00007ffc0faf9000 	C:\Program Files\Java\jdk-22\bin\jaas.dll
0x00007ffc0eb60000 - 0x00007ffc0eb6e000 	C:\Program Files\Java\jdk-22\bin\sunmscapi.dll
0x00007ffc156e0000 - 0x00007ffc158bf000 	C:\Windows\system32\CRYPT32.dll
0x00007ffc14f80000 - 0x00007ffc14fa5000 	C:\Windows\SYSTEM32\ncrypt.dll
0x00007ffc155a0000 - 0x00007ffc155b1000 	C:\Windows\system32\MSASN1.dll
0x00007ffc14f40000 - 0x00007ffc14f77000 	C:\Windows\SYSTEM32\NTASN1.dll
0x00007ffc0eb50000 - 0x00007ffc0eb59000 	C:\Program Files\Java\jdk-22\bin\extnet.dll
0x00007ffc055d0000 - 0x00007ffc0575e000 	C:\Program Files\Java\jdk-22\bin\awt.dll
0x00007ffc13ec0000 - 0x00007ffc13f4e000 	C:\Windows\system32\apphelp.dll
0x00007ffc14200000 - 0x00007ffc14329000 	C:\Windows\system32\uxtheme.dll
0x00007ffc14100000 - 0x00007ffc14121000 	C:\Windows\system32\dwmapi.dll
0x00007ffc02cd0000 - 0x00007ffc02dfb000 	C:\Windows\system32\opengl32.dll
0x00007ffc0e610000 - 0x00007ffc0e63e000 	C:\Windows\SYSTEM32\GLU32.dll
0x00007ffc02bd0000 - 0x00007ffc02cc8000 	C:\Windows\SYSTEM32\DDRAW.dll
0x00007ffc0e6e0000 - 0x00007ffc0e6e9000 	C:\Windows\SYSTEM32\DCIMAN32.dll
0x00007ffc08050000 - 0x00007ffc080d7000 	C:\Program Files\Java\jdk-22\bin\freetype.dll
0x00007ffc06110000 - 0x00007ffc061e7000 	C:\Program Files\Java\jdk-22\bin\fontmanager.dll
0x00007ffc13a50000 - 0x00007ffc13bfe000 	C:\Windows\SYSTEM32\WindowsCodecs.dll
0x00007ffc0e4f0000 - 0x00007ffc0e4fb000 	C:\Program Files\Java\jdk-22\bin\le.dll

dbghelp: loaded successfully - version: 4.0.5 - missing functions: none
symbol engine: initialized successfully - sym options: 0x614 - pdb path: .;C:\Program Files\Java\jdk-22\bin;C:\Windows\SYSTEM32;C:\Windows\WinSxS\amd64_microsoft.windows.common-controls_6595b64144ccf1df_6.0.9600.17415_none_6240486fecbd8abb;C:\Program Files\Java\jdk-22\bin\server;C:\Users\itzhak\AppData\Local\Temp;C:\Users\itzhak\AppData\Local\Temp\jna--1178040445

VM Arguments:
java_command: C:\Users\itzhak\Desktop\paper-1.20.4-463.jar
java_class_path (initial): C:\Users\itzhak\Desktop\paper-1.20.4-463.jar
Launcher Type: SUN_STANDARD

[Global flags]
     intx CICompilerCount                          = 3                                         {product} {ergonomic}
     uint ConcGCThreads                            = 1                                         {product} {ergonomic}
     uint G1ConcRefinementThreads                  = 4                                         {product} {ergonomic}
   size_t G1HeapRegionSize                         = 1048576                                   {product} {ergonomic}
   size_t InitialHeapSize                          = 67108864                                  {product} {ergonomic}
   size_t MarkStackSize                            = 4194304                                   {product} {ergonomic}
   size_t MaxHeapSize                              = 1044381696                                {product} {ergonomic}
   size_t MaxNewSize                               = 625999872                                 {product} {ergonomic}
   size_t MinHeapDeltaBytes                        = 1048576                                   {product} {ergonomic}
   size_t MinHeapSize                              = 8388608                                   {product} {ergonomic}
    uintx NonNMethodCodeHeapSize                   = 5832780                                {pd product} {ergonomic}
    uintx NonProfiledCodeHeapSize                  = 122912730                              {pd product} {ergonomic}
    uintx ProfiledCodeHeapSize                     = 122912730                              {pd product} {ergonomic}
    uintx ReservedCodeCacheSize                    = 251658240                              {pd product} {ergonomic}
     bool SegmentedCodeCache                       = true                                      {product} {ergonomic}
   size_t SoftMaxHeapSize                          = 1044381696                             {manageable} {ergonomic}
     bool UseCompressedOops                        = true                           {product lp64_product} {ergonomic}
     bool UseG1GC                                  = true                                      {product} {ergonomic}
     bool UseLargePagesIndividualAllocation        = false                                  {pd product} {ergonomic}

Logging:
Log output configuration:
 #0: stdout all=warning uptime,level,tags foldmultilines=false
 #1: stderr all=off uptime,level,tags foldmultilines=false

Environment Variables:
PATH=C:\Program Files\Common Files\Oracle\Java\javapath;C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0\
USERNAME=itzhak
OS=Windows_NT
PROCESSOR_IDENTIFIER=Intel64 Family 6 Model 58 Stepping 9, GenuineIntel
TMP=C:\Users\itzhak\AppData\Local\Temp
TEMP=C:\Users\itzhak\AppData\Local\Temp




Periodic native trim disabled

---------------  S Y S T E M  ---------------

OS:
 Windows 8.1 , 64 bit Build 9600 (6.3.9600.17415)
OS uptime: 0 days 0:46 hours

CPU: total 4 (initial active 4) (2 cores per cpu, 2 threads per core) family 6 model 58 stepping 9 microcode 0x1b, cx8, cmov, fxsr, ht, mmx, sse, sse2, sse3, ssse3, sse4.1, sse4.2, popcnt, tsc, tscinvbit, avx, aes, erms, clmul, vzeroupper, clflush, rdtscp, f16c
Processor Information for all 4 processors :
  Max Mhz: 2601, Current Mhz: 2601, Mhz Limit: 2601

Memory: 4k page, system-wide physical 3981M (2202M free)
TotalPageFile size 5389M (AvailPageFile size 3353M)
current process WorkingSet (physical memory assigned to process): 577M, peak: 577M
current process commit charge ("private bytes"): 604M, peak: 605M

vm_info: Java HotSpot(TM) 64-Bit Server VM (22+36-2370) for windows-amd64 JRE (22+36-2370), built on 2024-02-15T22:15:19Z by "mach5one" with MS VC++ 17.6 (VS2022)

END.

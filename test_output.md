Started by user Muhammmad Humair
Obtained Jenkinsfile from git https://github.com/mhumair/testapp.git
Running in Durability level: MAX_SURVIVABILITY
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins in /home/ems/.jenkins/workspace/testproject
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
using credential 5acd2d60-b508-4ae2-8961-0a82c27c20e6
 > git rev-parse --is-inside-work-tree # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/mhumair/testapp.git # timeout=10
Fetching upstream changes from https://github.com/mhumair/testapp.git
 > git --version # timeout=10
using GIT_ASKPASS to set credentials 
 > git fetch --tags --force --progress -- https://github.com/mhumair/testapp.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
 > git rev-parse refs/remotes/origin/origin/master^{commit} # timeout=10
Checking out Revision 2c2f2cd03df2fdb1b671e770e8b2941a002172ef (refs/remotes/origin/master)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 2c2f2cd03df2fdb1b671e770e8b2941a002172ef # timeout=10
Commit message: "Update Jenkinsfile"
 > git rev-list --no-walk 997bedb48c32a2c5dcb9fd9204bcde04dd84be7b # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] git
No credentials specified
 > git rev-parse --is-inside-work-tree # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/mhumair/testapp.git # timeout=10
Fetching upstream changes from https://github.com/mhumair/testapp.git
 > git --version # timeout=10
 > git fetch --tags --force --progress -- https://github.com/mhumair/testapp.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
 > git rev-parse refs/remotes/origin/origin/master^{commit} # timeout=10
Checking out Revision 2c2f2cd03df2fdb1b671e770e8b2941a002172ef (refs/remotes/origin/master)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 2c2f2cd03df2fdb1b671e770e8b2941a002172ef # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git branch -D master # timeout=10
 > git checkout -b master 2c2f2cd03df2fdb1b671e770e8b2941a002172ef # timeout=10
Commit message: "Update Jenkinsfile"
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Run)
[Pipeline] sh
+ node index.js
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Test)
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
java.lang.NoSuchMethodError: No such DSL method 'tpRunJob' found among steps [archive, bat, build, catchError, checkout, deleteDir, dir, dockerFingerprintFrom, dockerFingerprintRun, echo, emailext, emailextrecipients, envVarsForTool, error, fileExists, findBuildScans, getContext, git, input, isUnix, junit, library, libraryResource, load, lock, mail, milestone, node, parallel, powershell, properties, pwd, pwsh, readFile, readTrusted, resolveScm, retry, script, sh, sleep, stage, stash, step, svn, timeout, timestamps, tm, tool, tpAgentConfig, unarchive, unstable, unstash, validateDeclarativePipeline, waitUntil, warnError, withContext, withCredentials, withDockerContainer, withDockerRegistry, withDockerServer, withEnv, withGradle, wrap, writeFile, ws] or symbols [all, allOf, always, ant, antFromApache, antOutcome, antTarget, any, anyOf, apiToken, architecture, archiveArtifacts, artifactManager, authorizationMatrix, batchFile, booleanParam, branch, brokenBuildSuspects, brokenTestsSuspects, buildButton, buildDiscarder, buildDiscarders, buildingTag, caseInsensitive, caseSensitive, certificate, changeRequest, changelog, changeset, checkoutToSubdirectory, choice, choiceParam, cleanWs, clock, command, credentials, cron, crumb, culprits, defaultFolderConfiguration, defaultView, demand, developers, disableConcurrentBuilds, disableResume, docker, dockerCert, dockerfile, downstream, dumb, durabilityHint, envVars, environment, equals, expression, file, fileParam, filePath, fingerprint, frameOptions, freeStyle, freeStyleJob, fromScm, fromSource, git, gitBranchDiscovery, gitHubBranchDiscovery, gitHubBranchHeadAuthority, gitHubExcludeArchivedRepositories, gitHubForkDiscovery, gitHubPullRequestDiscovery, gitHubSshCheckout, gitHubTagDiscovery, gitHubTrustContributors, gitHubTrustEveryone, gitHubTrustNobody, gitHubTrustPermissions, gitTagDiscovery, github, githubPush, gradle, headRegexFilter, headWildcardFilter, hyperlink, hyperlinkToModels, inheriting, inheritingGlobal, installSource, isRestartedRun, jdk, jdkInstaller, jgit, jgitapache, jnlp, jobBuildDiscarder, jobName, label, lastDuration, lastFailure, lastGrantedAuthorities, lastStable, lastSuccess, legacy, legacySCM, list, local, location, logRotator, loggedInUsersCanDoAnything, mailer, masterBuild, maven, maven3Mojos, mavenErrors, mavenMojos, mavenWarnings, modernSCM, myView, newContainerPerStage, node, nodeProperties, nonInheriting, none, not, overrideIndexTriggers, paneStatus, parallelsAlwaysFailFast, parameters, password, pattern, permanent, pipeline-model, pipeline-model-docker, pipelineTriggers, plainText, plugin, pollSCM, preserveStashes, projectNamingStrategy, proxy, queueItemAuthenticator, quietPeriod, rateLimitBuilds, recipients, requestor, resourceRoot, run, runParam, sSHLauncher, schedule, scmRetryCount, scriptApproval, scriptApprovalLink, search, security, shell, simpleBuildDiscarder, skipDefaultCheckout, skipStagesAfterUnstable, slave, sourceRegexFilter, sourceWildcardFilter, ssh, sshUserPrivateKey, stackTrace, standard, status, string, stringParam, swapSpace, tag, teamSlugFilter, text, textParam, timezone, tmpSpace, toolLocation, tpAppUpdateFile, tpAppUpdateURL, tpDataSourceUpdate, tpJobRun, tpProjectParamUpdate, tpTestPackageUpdate, triggeredBy, unsecured, upstream, upstreamDevelopers, userSeed, usernameColonPassword, usernamePassword, viewsTabBar, weather, withAnt, zfs, zip] or globals [currentBuild, docker, env, params, pipeline, scm]
	at org.jenkinsci.plugins.workflow.cps.DSL.invokeMethod(DSL.java:202)
	at org.jenkinsci.plugins.workflow.cps.CpsScript.invokeMethod(CpsScript.java:122)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.codehaus.groovy.reflection.CachedMethod.invoke(CachedMethod.java:93)
	at groovy.lang.MetaMethod.doMethodInvoke(MetaMethod.java:325)
	at groovy.lang.MetaClassImpl.invokeMethod(MetaClassImpl.java:1213)
	at groovy.lang.MetaClassImpl.invokeMethod(MetaClassImpl.java:1022)
	at org.codehaus.groovy.runtime.callsite.PogoMetaClassSite.call(PogoMetaClassSite.java:42)
	at org.codehaus.groovy.runtime.callsite.CallSiteArray.defaultCall(CallSiteArray.java:48)
	at org.codehaus.groovy.runtime.callsite.AbstractCallSite.call(AbstractCallSite.java:113)
	at org.kohsuke.groovy.sandbox.impl.Checker$1.call(Checker.java:163)
	at org.kohsuke.groovy.sandbox.GroovyInterceptor.onMethodCall(GroovyInterceptor.java:23)
	at org.jenkinsci.plugins.scriptsecurity.sandbox.groovy.SandboxInterceptor.onMethodCall(SandboxInterceptor.java:157)
	at org.kohsuke.groovy.sandbox.impl.Checker$1.call(Checker.java:161)
	at org.kohsuke.groovy.sandbox.impl.Checker.checkedCall(Checker.java:165)
	at org.kohsuke.groovy.sandbox.impl.Checker.checkedCall(Checker.java:135)
	at com.cloudbees.groovy.cps.sandbox.SandboxInvoker.methodCall(SandboxInvoker.java:17)
	at WorkflowScript.run(WorkflowScript:22)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.delegateAndExecute(ModelInterpreter.groovy:137)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.executeSingleStage(ModelInterpreter.groovy:661)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.catchRequiredContextForNode(ModelInterpreter.groovy:395)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.catchRequiredContextForNode(ModelInterpreter.groovy:393)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.executeSingleStage(ModelInterpreter.groovy:660)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:288)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.toolsBlock(ModelInterpreter.groovy:544)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.toolsBlock(ModelInterpreter.groovy:543)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:276)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withEnvBlock(ModelInterpreter.groovy:443)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withEnvBlock(ModelInterpreter.groovy:442)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:275)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withCredentialsBlock(ModelInterpreter.groovy:481)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withCredentialsBlock(ModelInterpreter.groovy:480)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:274)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.inDeclarativeAgent(ModelInterpreter.groovy:586)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.inDeclarativeAgent(ModelInterpreter.groovy:585)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:272)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.stageInput(ModelInterpreter.groovy:356)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.stageInput(ModelInterpreter.groovy:355)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:261)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.inWrappers(ModelInterpreter.groovy:613)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.inWrappers(ModelInterpreter.groovy:612)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:259)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withEnvBlock(ModelInterpreter.groovy:443)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.withEnvBlock(ModelInterpreter.groovy:442)
	at org.jenkinsci.plugins.pipeline.modeldefinition.ModelInterpreter.evaluateStage(ModelInterpreter.groovy:254)
	at ___cps.transform___(Native Method)
	at com.cloudbees.groovy.cps.impl.ContinuationGroup.methodCall(ContinuationGroup.java:86)
	at com.cloudbees.groovy.cps.impl.FunctionCallBlock$ContinuationImpl.dispatchOrArg(FunctionCallBlock.java:113)
	at com.cloudbees.groovy.cps.impl.FunctionCallBlock$ContinuationImpl.fixArg(FunctionCallBlock.java:83)
	at jdk.internal.reflect.GeneratedMethodAccessor140.invoke(Unknown Source)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at com.cloudbees.groovy.cps.impl.ContinuationPtr$ContinuationImpl.receive(ContinuationPtr.java:72)
	at com.cloudbees.groovy.cps.impl.CollectionLiteralBlock$ContinuationImpl.dispatch(CollectionLiteralBlock.java:55)
	at com.cloudbees.groovy.cps.impl.CollectionLiteralBlock$ContinuationImpl.item(CollectionLiteralBlock.java:45)
	at jdk.internal.reflect.GeneratedMethodAccessor152.invoke(Unknown Source)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at com.cloudbees.groovy.cps.impl.ContinuationPtr$ContinuationImpl.receive(ContinuationPtr.java:72)
	at com.cloudbees.groovy.cps.impl.ConstantBlock.eval(ConstantBlock.java:21)
	at com.cloudbees.groovy.cps.Next.step(Next.java:83)
	at com.cloudbees.groovy.cps.Continuable$1.call(Continuable.java:174)
	at com.cloudbees.groovy.cps.Continuable$1.call(Continuable.java:163)
	at org.codehaus.groovy.runtime.GroovyCategorySupport$ThreadCategoryInfo.use(GroovyCategorySupport.java:129)
	at org.codehaus.groovy.runtime.GroovyCategorySupport.use(GroovyCategorySupport.java:268)
	at com.cloudbees.groovy.cps.Continuable.run0(Continuable.java:163)
	at org.jenkinsci.plugins.workflow.cps.SandboxContinuable.access$001(SandboxContinuable.java:18)
	at org.jenkinsci.plugins.workflow.cps.SandboxContinuable.run0(SandboxContinuable.java:51)
	at org.jenkinsci.plugins.workflow.cps.CpsThread.runNextChunk(CpsThread.java:185)
	at org.jenkinsci.plugins.workflow.cps.CpsThreadGroup.run(CpsThreadGroup.java:400)
	at org.jenkinsci.plugins.workflow.cps.CpsThreadGroup.access$400(CpsThreadGroup.java:96)
	at org.jenkinsci.plugins.workflow.cps.CpsThreadGroup$2.call(CpsThreadGroup.java:312)
	at org.jenkinsci.plugins.workflow.cps.CpsThreadGroup$2.call(CpsThreadGroup.java:276)
	at org.jenkinsci.plugins.workflow.cps.CpsVmExecutorService$2.call(CpsVmExecutorService.java:67)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at hudson.remoting.SingleLaneExecutorService$1.run(SingleLaneExecutorService.java:131)
	at jenkins.util.ContextResettingExecutorService$1.run(ContextResettingExecutorService.java:28)
	at jenkins.security.ImpersonatingExecutorService$1.run(ImpersonatingExecutorService.java:59)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628)
	at java.base/java.lang.Thread.run(Thread.java:834)
Finished: FAILURE

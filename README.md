# Why Mac is the right tool for Cloud Foundry development

## Lower TCO than PC

- IBM in 2015: 
  - [‘Every Mac we buy is making and saving money’][1]
  - [Able to support over 30,000 Mac users with an IT support ratio of 1:5,000][2]
- IBM in 2016: 
  - [3X more expensive to manage PCs than Macs][3] (Saving up to $535 per Mac per four years in comparison to PCs
)

[1]: http://www.computerworld.com/article/2998315/apple-mac/every-mac-we-buy-is-making-and-saving-ibm-money-ibm.html
[2]: https://www.jamf.com/resources/mac-ibm-zero-to-30000-in-6-months-highlights/
[3]: http://www.computerworld.com/article/3131906/apple-mac/ibm-says-macs-are-even-cheaper-to-run-than-it-thought.html

## Some common tools or starters are completley broken on Windows

### Filesystem incompatibility with Spring Cloud starters

No idea how to work around this, other than "Don't try to do development on Windows." 

```shell-session
% git clone https://github.com/spring-cloud/spring-cloud-stream-app-starters.git
Cloning into 'spring-cloud-stream-app-starters'...
remote: Counting objects: 22092, done.
remote: Total 22092 (delta 1), reused 1 (delta 1), pack-reused 22090
Receiving objects: 100% (22092/22092), 3.10 MiB | 2.43 MiB/s, done.
Resolving deltas: 100% (5797/5797), done.
Checking connectivity... done.
error: unable to create file processor/spring-cloud-starter-stream-processor-tasklaunchrequest-transform/src/main/java/org/springframework/cloud/stream/app/tasklaunchrequest/transform/processor/TasklaunchrequestTransformProcessorConfiguration.java (Filename too long)
error: unable to create file processor/spring-cloud-starter-stream-processor-tasklaunchrequest-transform/src/main/java/org/springframework/cloud/stream/app/tasklaunchrequest/transform/processor/TasklaunchrequestTransformProcessorProperties.java (Filename too long)
error: unable to create file processor/spring-cloud-starter-stream-processor-tasklaunchrequest-transform/src/test/java/org/springframework/cloud/stream/app/tasklaunchrequest/transform/processor/TasklaunchrequestTransformProcessorIntegrationTests.java (Filename too long)
error: unable to create file tasklauncher/spring-cloud-starter-stream-sink-tasklauncher-cloudfoundry/src/main/java/org/springframework/cloud/stream/app/task/launcher/cloudfoundry/sink/TaskLauncherCloudfoundrySinkConfiguration.java (Filename too long)
Checking out files: 100% (701/701), done.
fatal: unable to checkout working tree
warning: Clone succeeded, but checkout failed.
You can inspect what was checked out with 'git status'
and retry the checkout with 'git checkout -f HEAD'
```

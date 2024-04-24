## 配置插件

```groovy
buildscript {
  repositories {
     maven {
            allowInsecureProtocol = true
            url "xxxx"
            credentials {
                username 'xxx'
                password 'xxx'
            }
        }
  }
  dependencies {
     classpath("org.weinian.plugin:spotbugs-plugins:3.1.0-RELEASE")
  }
}

apply plugin: 'com.itjcloud.spotbugs'

bootJar.dependsOn spotbugsMain
```
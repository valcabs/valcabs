repositories {
		mavenLocal()
		mavenCentral()
		google()
		gradlePluginPortal()
		maven { url 'https://oss.sonatype.org/content/repositories/snapshots/' }
		maven { url "http://artifactory.nimblygames.com/artifactory/ng-public-snapshot/" }
		maven { url "http://artifactory.nimblygames.com/artifactory/ng-public-release/" }
	}
	dependencies {
	}
}

allprojects {
	apply plugin: 'eclipse'
	apply plugin: 'idea'
}

configure(subprojects) {
	apply plugin: 'java-library'
	sourceCompatibility = 8.0
	compileJava {
		options.incremental = true
	}
}

subprojects {
	version = '0.0.1'
	ext.appName = 'tko-electronics-sim'
	repositories {
		mavenLocal()
		mavenCentral()
		gradlePluginPortal()
		maven { url 'https://oss.sonatype.org/content/repositories/snapshots/' }
		maven { url 'https://jitpack.io' }
	}
}

eclipse.project.name = 'tko-electronics-sim' + '-parent'

<!---
valcabs/valcabs is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

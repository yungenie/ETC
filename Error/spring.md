### [spring] Maven build fail "maven-surefire-plugin dummy:dummy.jar:1.0 missing"
> 현상 : Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:2.12.4:test (default-test) on project qds-mobile-selenium-tests: Unable to generate classpath: org.apache.maven.artifact.resolver.MultipleArtifactsNotFoundException:   
> 해결 : pom.xml plugins.plugin.artifactId "maven-surefire-plugin" 추가

		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-surefire-plugin</artifactId>
				<version>2.12.4</version>
				<configuration>
					<skipTests>true</skipTests>
				</configuration>
			</plugin>
		</plugins>
		
	
### [spring] Maven 배포 시 배포서버 별 환경설정(Resource) 다르게 적용하기
> 현상 : 배포서버 별 빌드시 logback.xml Resource 경로를 바라 봄.  
> 해결 : pom.xml <resource> -> <excludes> <includes> logback.xml 추가 

			<!-- *.properties 만 메이븐 필터링 -->
			<resource>
				<directory>src/main/resources</directory>
				<filtering>false</filtering>
				<excludes>
					<exclude>**/*.properties</exclude>
					<exclude>logback.xml</exclude>
				</excludes>
			</resource>
			<resource>
				<directory>src/main/resources</directory>
				<filtering>true</filtering>
				<includes>
					<include>**/*.properties</include>
					<include>logback.xml</include>
				</includes>
			</resource>
			<!-- 환경별 리소스 포함 -->
			<resource>
				<directory>src/main/resources-${environment}</directory>
				<filtering>false</filtering>
				<excludes>
					<exclude>**/*.properties</exclude>
					<exclude>logback.xml</exclude>
				</excludes>
			</resource>
			<resource>
				<directory>src/main/resources-${environment}</directory>
				<filtering>true</filtering>
				<includes>
					<include>**/*.properties</include>
					<include>logback.xml</include>
				</includes>
			</resource>
		</resources>

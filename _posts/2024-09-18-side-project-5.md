---
layout: post
title: "[sideproject 05] Swagger API 문서화 하기"
date: 2024-09-19 11:00:00 +0900
categories: [post]
tags: [project]
---

### Swagger UI 의존성 주입

build.gradle 파일에 의존성 추가하기

```implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.2.0'```

의존성 추가 후 애플리케이션을 실행하면 아래 링크로 접속할 수 있다

localhost:8080/swagger-ui/index.html

그리고 저 url에 접속해보면 http://localhost:8080/login 로 이동되면서 sign in 페이지가 뜬다   
swagger hub 아이디랑 비밀번호로 로그인 시도를 해봤지만 안됨


### SwaggerConfiguration class 생성

```
import static io.swagger.v3.oas.models.security.SecurityScheme.Type.HTTP;

import io.swagger.v3.oas.models.Components;
import io.swagger.v3.oas.models.OpenAPI;
import io.swagger.v3.oas.models.info.Contact;
import io.swagger.v3.oas.models.info.Info;
import io.swagger.v3.oas.models.info.License;
import io.swagger.v3.oas.models.security.SecurityRequirement;
import io.swagger.v3.oas.models.security.SecurityScheme;
import lombok.Getter;
import lombok.Setter;
import org.springframework.boot.context.properties.ConfigurationProperties;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Getter
@Setter
@Configuration
@ConfigurationProperties(prefix = "swagger")
public class SwaggerConfiguration {

  private String appName;

  private String appDescription;

  private String appVersion;

  private String appLicense;

  private String appLicenseUrl;

  private String contactName;

  private String contactUrl;

  private String contactMail;

  @Bean
  public OpenAPI openAPI() {

    final Info apiInformation = getApiInformation();
    final Components components = new Components();

    final String schemeName = "bearerAuth";
    components.addSecuritySchemes(schemeName,
        new SecurityScheme().name(schemeName).type(HTTP).scheme("bearer").bearerFormat("JWT"));

    final OpenAPI openAPI = new OpenAPI();
    openAPI.setInfo(apiInformation);
    openAPI.setComponents(components);
    openAPI.addSecurityItem(new SecurityRequirement().addList(schemeName));

    return openAPI;
  }

  private Info getApiInformation() {

    final License license = new License();
    license.setName(appLicense);
    license.setUrl(appLicenseUrl);

    final Contact contact = new Contact();
    contact.setName(contactName);
    contact.setUrl(contactUrl);
    contact.setEmail(contactMail);

    final Info info = new Info();
    info.setTitle(appName);
    info.setVersion(appVersion);
    info.setDescription(appDescription);
    info.setLicense(license);
    info.setContact(contact);

    return info;
  }

}
 ```   
 

 ### controller에 어노테이션 추가

어노테이션 사용으로 API 그룹화할 태그명 지정하기

```@RestController
@RequestMapping("/api/response_estimate")
@RequiredArgsConstructor
@Tag(name = "Response Estimate", description = "Response Estimate API")```

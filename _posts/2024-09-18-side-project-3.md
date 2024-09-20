---
layout: post
title: "[sideproject 03] mapper 에서 jpa로"
date: 2024-09-18 10:00:00 +0900
categories: [post]
tags: [project]
---

### Entity 생성

```
import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import lombok.AllArgsConstructor;
import lombok.Builder;
import lombok.Getter;
import lombok.NoArgsConstructor;
import lombok.Setter;

@Getter
@Setter
@AllArgsConstructor
@NoArgsConstructor
@Builder
@Entity
@Table(name = "LOCATION")
public class Location extends BaseTimeEntity {

  @Id
  @Column(name = "search_keyword", nullable = false)
  private String searchKeyword;

}
```

엔티티 생성 후 프로젝트를 실행하면 연결된 데이터베이스에 자동으로 테이블이 생성됨
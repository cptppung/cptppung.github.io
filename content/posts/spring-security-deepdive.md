---
date: '2026-03-25T10:21:28+09:00'
draft: true
title: 'Spring Security 겉핥기가 아닌 제대로 알기'
tags: ["spring security"]
categories: ["spring"]
toc: false
---

![공부](/images/Gemini_Generated_Image_v0ys7sv0ys7sv0ys_lowsize.png)

Spring Security를 공부하다 보면 대부분 비슷한 경험을 한다.

블로그나 공식 문서를 따라 @EnableWebSecurity니 SecurityFilterChain이니 복붙해서 일단 돌아가게는 만드는데... 막상 뭔가 안 되면 왜 안 되는지 모르겠는 상황.

그 답답함에서 시작한 글이다.

Spring Security를 한 줄로 표현하면 "Filter의 연속" 이다. 요청이 들어오는 순간부터 응답이 나가기까지 여러 Filter를 거치는데, 이걸 모르고 쓰면 설정은 했는데 왜 적용이 안 되는지, CSRF는 왜 막히는지, @PreAuthorize는 왜 안 먹히는지 감이 안 온다.

이 글에서는 그 흐름을 제대로 짚어보려 한다.

도움이 되는 분들이 있으면 좋겠고... 잘 정리가 될지는 모르겠지만 일단 써보련다. 😅

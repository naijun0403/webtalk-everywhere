# webtalk-everywhere
`cs.kakao.com`에 있는 웹톡 서비스를 다른 사이트에서도 사용할 수 있게 도와주는 레포입니다.

## 주의사항
본 웹톡이라고 하는 것은 오직 플러스친구에게만 사용이 가능한 서비스입니다.

## 구현
- [x] vanilla
- [ ] react
- [ ] svelte

## 설정
### 바닐라
다음과 같은 코드를 넣어, 기본적인 로더 스크립트를 불러오세요
```html
<script src="https://webtalk.kakao.com/webtalk.loader.js"></script>
```

> 로더 스크립트에서는 무엇을 하나요?
>
> 로더 스크립트는 웹톡에 필요한 기본적인 리소스와 api, css 웹톡의 구조까지 모두 불러와 특정한 iframe에 넣어줍니다.
>
> 로더를 사용함으로서, 사용자는 설정 단계를 최소화 할 수 있습니다.

그 다음 사용할 플러스 친구의 아이디와, 프로필 키를 흭득해야합니다.

흭득 방법은 [다음](/how-to-get-pf.md)을 참고해주세요

다음 다음과 같이 컴포넌트를 넣어주세요

```html
    <div data-kakao-envoy="true" class="cont_envoy" data-plus-profile-id="{아이디}" data-uuid="{프로필 키}">
      <div class="_wt_kakao_envoy">
        <div class="_wt_view_comm _wt_view_pc os_mac">
          <div class="_wt_module_webchat">
            <div class="_wt_util_webchat" data-testid="util_webchat">
              <em class="_wt_emph_new" aria-hidden="true" data-testid="emph_new"></em>
              <button aria-expanded="false" type="button" class="_wt_btn_webchat _wt_btn_open" data-testid="btn_open">
                <span class="_wt_screen_out">톡으로 상담</span>
                <span class="_wt_ico_open">
                  <span class="_wt_ico_webchat _wt_ico_kakaotalk"></span>
                  <span class="_wt_ico_webchat _wt_ico_guide"></span>
                </span>
              </button>
              <button aria-expanded="false" type="button" class="_wt_btn_webchat _wt_btn_close" data-testid="btn_close">
                <span class="_wt_screen_out">톡으로 상담</span>
                <span class="_wt_ico_webchat _wt_ico_close">닫기</span>
              </button>
              <button type="button" class="_wt_btn_webchat _wt_btn_logout" data-testid="btn_logout">
                <span class="_wt_txt_logout">로그아웃</span>
              </button>
              <div aria-live="assertive" class="_wt_layer_tooltip">
                <p></p>
              </div>
            </div>
            <div class="_wt_view_webchat">
              <iframe class="_wt_frame_chat" data-testid="frame_chat" title="빈프레임"></iframe>
            </div>
          </div>
        </div>
      </div>
    </div>
```
> 주의: 여기서 그 어떠한 class도 변경되면 안됩니다. 이는 로더 스크립트 불러오기를 위합니다.
> 
> 다만 {아이디}, {프로필 키}에는 값을 자신의 값으로 바꿔 넣어주시길 바랍니다.

이제 우측 하단에 웹톡을 사용할 수 있습니다.

### 리엑트
> 추가 예정 입니다.

### 스벨트
> 추가 예정 입니다.
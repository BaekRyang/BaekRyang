1. 유니티 셰이더 그래프로 만든 셰이더를 UI에 적용하면 Scene창에서는 정상적으로 보인다.
2. 그런데 Game창에서는 Aplha가 적용되어야 하는 부분이 전부 적갈색으로 표시가 된다.
3. FrameDebugger로 확인을 해보니 정상적으로 렌더링을 하고난 뒤에 추가적인 작업을 하면서 생기는 문제임을 확인했다.

![screenshot](./ScreenShots/2023-09-15-ShaderGraph-Gaussian-01.png)

4. 이 문제를 해결하기 위해 유니티 포럼을 찾아보니 비슷한 문제를 겪은 사람들이 있었다.
[Link](https://forum.unity.com/threads/shader-graph-ui-image-shader-does-not-work.1202461/#post-7683259)

5. 여기서 `jessmwoodward`의 답변을 보면 위에서 ShaderGraph로 만든 셰이더 코드가 2020에서 2021로 넘어가면서 변경된 사항이 있었다고 한다.
6. `SceneSelectionPass`, `ScenePickingPass`가 추가되면서 생긴 문제라고 한다.
7. 그래서 해당 셰이더 그래프를 코드로 변환한 뒤 두 부분을 삭제하니 문제가 해결되었음
8. 추가로 `SpriteNormalPass`와 `SpriteForwardPass`도 삭제해야 내가 의도했던 셰이더가 제대로 작동했다.
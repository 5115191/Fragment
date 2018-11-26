# Fragment
fragment 使用方法



Fragment的生命周期
Fragment必须是依存与Activity而存在的，因此Activity的生命周期会直接影响到Fragment的生命周期.

activity---------------------- fragment

created------------------------onAttach()->
															onCreate()->
															onCreateView()->
															onActivityCreated()
															
started------------------------onStart()

resumed------------------------onResume()

paused-------------------------onPause()

stoped-------------------------onStope()

destoryed----------------------onDestoryView()->
															onDestory()->
															ondetach

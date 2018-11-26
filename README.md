# Fragment
fragment 使用方法



Fragment的生命周期
Fragment必须是依存与Activity而存在的，因此Activity的生命周期会直接影响到Fragment的生命周期.

activity---------------------- fragment

created------------------------onAttach() -> onCreate() -> onCreateView() -> onActivityCreated()
															
started------------------------onStart()

resumed------------------------onResume()

paused-------------------------onPause()

stoped-------------------------onStope()

destoryed----------------------onDestoryView()->onDestory()->onDetach()

可以看到Fragment比Activity多了几个额外的生命周期回调方法：

onAttach(Activity)
当Fragment与Activity发生关联时调用。

onCreateView(LayoutInflater, ViewGroup,Bundle)
创建该Fragment的视图

onActivityCreated(Bundle)
当Activity的onCreate方法返回时调用

onDestoryView()
与onCreateView想对应，当该Fragment的视图被移除时调用

onDetach()
与onAttach相对应，当Fragment与Activity关联被取消时调用

注意：除了onCreateView，其他的所有方法如果你重写了，必须调用父类对于该方法的实现，如 super.xxx();

															

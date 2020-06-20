---

title: Android 基础知识
date: 2019.11.10
updated: 2020.06.15
tags: 安卓
categories: 安卓

---

### Android基础知识

#### 一、导航

<!--more-->

##### 1、页面跳转主要代码

```Android
NavController coloController = Navigation.findNavController(v);
coloController.navigate(R.id.action_detialFragment_to_homeFragment);
```

##### 2、页面跳转传递数据主要代码

```Android
EditText editText = getView().findViewById(R.id.editText);
String string = editText.getText().toString();
if(TextUtils.isEmpty(string)){  
Toast.makeText(getActivity(), "请输入姓名",Toast.LENGTH_SHORT).show(); 
return;
}
Bundle bundle = new Bundle();
bundle.putString("my_name",string);
NavController controller = Navigation.findNavController(v);
controller.navigate(R.id.action_homeFragment_to_detialFragment,bundle);

String string = getArguments().getString("my_name");
TextView textView2 = getView().findViewById(R.id.textView2);
textView2.setText(string);
```

##### 3、基于ViewModel传递数据主要代码

```Android
final MyViewModel myViewModel;
myViewModel = ViewModelProviders.of(getActivity()).get(MyViewModel.class);
FragmentMasterBinding binding;
binding = DataBindingUtil.inflate(inflater,R.layout.fragment_master,container,false);
binding.setData(myViewModel);
binding.setLifecycleOwner(getActivity());
binding.button.setOnClickListener(new View.OnClickListener() {   
@Override
public void onClick(View v) {        
NavController  controller = Navigation.findNavController(v);        controller.navigate(R.id.action_masterFragment_to_detailFragment);    }});
return binding.getRoot();
```
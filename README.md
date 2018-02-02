

//阿里ARouter框架

1.添加依赖和配置
```
android {
    defaultConfig {
    ...
    javaCompileOptions {
        annotationProcessorOptions {
        arguments = [ moduleName : project.getName() ]
        }
    }
    }
}

dependencies {<br>
    compile 'com.alibaba:arouter-api:1.2.1.1'<br>
    annotationProcessor 'com.alibaba:arouter-compiler:1.1.2.1'<br>
    ...<br>
}<br>
```

2.添加注解<br>

// 在支持路由的页面上添加注解(必选)
// 这里的路径需要注意的是至少需要有两级，/xx/xx<br>

```
@Route(path = "/test/test1")
public class Test1Activity extends AppCompatActivity{

    @Override
    protected void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_test1);
    }
}
```

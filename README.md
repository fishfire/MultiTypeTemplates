# MultiTypeTemplates
An intellij idea plugin for Android to generate `MultiType` `Item` and `ItemViewBinder` easily.

![](http://ww1.sinaimg.cn/large/86e2ff85gw1f8ylqaegmoj203k03k3yg.jpg) ![](http://ww4.sinaimg.cn/large/86e2ff85gw1f8ylrw6vd9j203k03k747.jpg)

### Obtaining & Installation

- The plugin is distributed through the Plugin Manager in IntelliJ. https://plugins.jetbrains.com/plugin/9202

- Search word `MultiTypeTemplates`: On Mac: `Preference -> Plugins -> Browse repositories`

- Or you can download the jar file from [MultiTypeTemplates.jar](https://github.com/drakeet/MultiTypeTemplates/releases),
then `Preferences -> Plugin -> Install plugin from disk...`

![](http://ww4.sinaimg.cn/large/86e2ff85gw1f935l0kwilj21kw0t3akm.jpg)

### Usage

`Right-click` your package/directory - `New` - `MultiType Item`, then inputs your name of Item to generate Item and ItemViewBinder files and codes.

![](http://ww4.sinaimg.cn/large/86e2ff85gw1f8yj0sejd6j21340ben1s.jpg)

Example: If you input "Category", it will generate the `Category.java` and `CategoryViewBinder.java`:

```java
public class Category {

}
```

```java
public class CategoryViewBinder extends ItemViewBinder<Category, CategoryViewBinder.ViewHolder> {

    @NonNull @Override
    protected ViewHolder onCreateViewHolder(@NonNull LayoutInflater inflater, @NonNull ViewGroup parent) {
        View root = inflater.inflate(R.layout.item_category, parent, false);
        return new ViewHolder(root);
    }
    

    @Override
    protected void onBindViewHolder(@NonNull ViewHolder holder, @NonNull Category category) {

    }

    
    static class ViewHolder extends RecyclerView.ViewHolder {

        ViewHolder(View itemView) {
            super(itemView);
        }
    }
}
```

### Thanks

- **[drakeet/MultiType](https://github.com/drakeet/MultiType)**
 An Android library to retrofit multiple item view types

# UI-09-UITableViewCell-code
##代码创建cell
- 代码自定义cell(使用Masonry)
   - 1.创建一个继承自UITableViewCell的子类，比如XMGDealCell
    - 在initWithStyle:reuseIdentifier:方法中
      - 添加子控件
      - 添加子控件的约束（建议使用Masonry）
      - 设置子控件的初始化属性（比如文字颜色、字体）
      - 需要提供一个模型属性，重写模型的set方法，在这个方法中设置模型数据到子控件
   - 2.在控制器中
    	- 利用registerClass...方法注册XMGDealCell类
    	- 利用重用标识找到cell（如果没有注册类，就需要手动创建cell）
    	- 给cell传递模型数据
    	- 也可以将创建获得cell的代码封装起来（比如cellWithTableView:方法）
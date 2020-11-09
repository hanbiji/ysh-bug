## YSH BUG 修改日志

You can use the [editor on GitHub](https://github.com/hanbiji/ysh-bug/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### 无法下发考试

下发考试报下面错误

```无法下发考试
array(3) { [0]=> string(18) "Error Number: 2006" [1]=> string(26) "MySQL server has gone away" [2]=> string(50) "SELECT * FROM (`xz_exam_record`) WHERE `id` = 898" } string(0) "" bool(false)
### 原因：因欠费发送短信失败
### 解决：注释 application/controllers/paper.php 3065-3067
if(ENVIRONMENT == PRODUCTION){
    $this->message_model->send_message('uid：'.$this->member_uid.'，用户名：'.$this->mine_name.' 用户正在下发record_id：'.$record_id.'的考试');
}
```

### Demo

下发考试报下面错误

```Demo
array(3) { [0]=> string(18) "Error Number: 2006" [1]=> string(26) "MySQL server has gone away" [2]=> string(50) "SELECT * FROM (`xz_exam_record`) WHERE `id` = 898" } string(0) "" bool(false)

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/hanbiji/ysh-bug/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

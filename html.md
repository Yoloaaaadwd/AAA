# Html文档结构  

    <!DOCTYPE html>
        <html lang="en">
          <head>
            <meta charset="utf-8" />
            <title>Machine Learning Workshop</title>
            <meta name="viewport" content="width=device-width" />
          </head>
          <body>

          </body>
</html>

## <Head>的其他内容  
1.添加 CSS 的方法有三种：<link>、<style> 和 style 属性。  
2.<link> 标记是添加样式表的首选方法。  
     <link rel="stylesheet" href="styles.css">

其中 Styles.css 是您样式表的网址。  
3.如果您希望外部样式表样式位于级联层内，但无权修改 CSS 文件以将层信息放入其中，则需要在 <style> 内添加带有 @import 的 CSS：  
    <style>
  @import "styles.css" layer(firstLayer);
</style>


## <link> 元素的其他用途  
1.link 元素用于在 HTML 文档与外部资源之间创建关系。这些资源中有些可供下载，其他资源仅供参考。关系类型由 rel 属性的值定义。  
2.标题中还包含另外三种类型：icon、alternate 和 canonical。（您将在下一个单元中添加第四个类型，rel="manifest"）。  
3.网站图标：使用 <link> 标记和 rel="icon" 属性/值对来标识要用于您的文档的网站图标。网站图标是显示在浏览器标签页中的小图标，通常位于文档标题的左侧。如果您打开的标签页过多，标签页就会缩小，而标题可能会完全消失，但图标会一直显示。大多数网站图标都是公司或应用程序的徽标。

如果您没有声明网站图标，浏览器将在顶级目录（网站的根文件夹）中查找名为 favicon.ico 的文件。通过  <link>，您可以使用不同的文件名和位置：  
    <link rel="icon" sizes="16x16 32x32 48x48" type="image/png" href="/images/mlwicon.png" />

上述代码表示“在适合使用 16px、32px 或 48px 的场景中使用 mlwicon.png 作为图标。”对于可缩放的图标，尺寸属性接受 any 值，或以空格分隔的方形 widthXheight 值列表；其中宽度值和高度值为 16、32、48 或更大值（在该几何序列中），像素单位会被忽略，并且 X 不区分大小写。  
    <link rel="apple-touch-icon" sizes="180x180" href="/images/mlwicon.png" />
    <link rel="mask-icon" href="/images/mlwicon.svg" color="#226DAA" />  

Safari 浏览器有两种特殊的非标准图标：apple-touch-icon（用于 iOS 设备）和 mask-icon（用于 macOS 上固定标签页）。apple-touch-icon 仅在用户将网站添加到主屏幕时适用。图标本身应为单色 SVG，并且 color 属性会以所需的颜色填充图标。

虽然您可以使用 <link> 在每个网页上（甚至每次加载网页）定义完全不同的图片，但请不要这样做。为了保持一致性和良好的用户体验，请使用单张图片！
### 网站的其他版本  
我们使用 rel 属性的 alternate 值来识别网站的翻译版本或替代表示法。  

假设我们有翻译成法语和巴西葡萄牙语的网站版本：  
    <link rel="alternate" href="https://www.machinelearningworkshop.com/fr/" hreflang="fr-FR" />
    <link rel="alternate" href="https://www.machinelearningworkshop.com/pt/" hreflang="pt-BR" />  

使用 alternate 进行翻译时，必须设置 hreflang 属性。  

替代值不只是翻译。例如，当 type 属性设置为 application/rss+xml 或 application/atom+xml 时，type 属性定义 RSS Feed 的备用 URI。我们来链接到网站的假装 PDF 版本。  
    <link rel="alternate" type="application/x-pdf" href="https://machinelearningworkshop.com/mlw.pdf" />
 

 如果 rel 值为 alternate stylesheet，则会定义备用样式表，并且必须设置 title 属性为该备用样式命名。  
 

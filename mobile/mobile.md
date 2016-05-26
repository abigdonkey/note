#像素的基础知识

iPhone5 分辨率 640x1136
那么 640x1136的图片能不能在iPhone5上完全展示？
不能够
iPhone5 dpr=2 320x568

## px dp pt

### px

-- css pixels 逻辑像素 抽象像素，浏览器使用的抽象单位

### dp pt

-- device independent pixels 设备无关像素 物理像素
-- 固定大小 

### dpr

-- devicePixelRatio 设备像素缩放比
-- 1px = (dpr)*(dpr) * dp

##DPI
-- 打印机每英寸可以喷的墨汁点 印刷行业

##PPI
-- 屏幕每英寸的像素数量，即单位英寸内的像素密度

以iPhone5为例

ppi = 1136x1136+640x60 开方 除以4 = 326ppi
注意 单位是物理像素 而非px
ppi越高，像素数越高，图形越清晰
但可视度越低，系统默认缩放比例越大

            Idpi    mdpi    hdpi    xhdpi
ppi         120     160     240     320
默认缩放比    0.75    1.0     1.5      2.0

Retina屏（高清屏）：dpr都是大于2的

# Viewport

IOS 的viewport 980px

visual viewport

layout viewport

##为什么不使用默认的980px的布局viewport？

-- 宽度不可控制，不同系统不同设备的默认值可能不同
-- 页面缩小版显示，交互不友好
-- 链接不可点
-- 有缩放，缩放后又有滚动
font-size为40px等于PC上12px同等物理大小，不规范

## meta标签

-- layout viewport: document.body.clientWidth
-- 度量 viewport :window.innerWidth


#设计移动WEB

## 方案一：根据设备的实际宽度来设计（常用）
手机宽320px,则拿320px来设计

## 方案二 1px = 1dp
缩放 0.5 根据设备的物理像素dp等于抽象像素px来设计

1像素边框和高清图片都不需要额外处理


#高效移动web布局

Flexbox 弹性盒子布局

响应式布局





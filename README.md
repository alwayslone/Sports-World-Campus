# 关于《运动世界》手机自动跑的可能性说明与实践教程

> ⚠️ 本教程仅记录个人测试过程与环境配置情况，不保证适用于所有设备与 ROM。

---

## 一、已测试设备

* **Redmi K50**
* **Redmi K20 Pro**

---

## 二、基础环境要求（非常重要）

1. **Root 环境**
   * **Magisk** 和 **kernelsu** 等等都可以
   * Root 隐藏(自己网上搜root隐藏,已经很成熟了)
2. **所需软件**
   * 冰社（启用系统模式）
   * Fake Location `1.3.2.2`

## 三、K20 Pro 配置流程

### 1️⃣ 启动 Fake Location

* 打开 **冰社**
* 在冰社中 **打开 Fake Location 1.3.2.2**
* 启动 Fake Location 的 **模拟功能****

---

### 2️⃣ 调整 SELinux 为 Enforcing

* 进入系统设置
* 将 **SELinux 手动调回 `Enforcing` 模式**

---

### 3️⃣ 关闭模拟

* 完全关闭 Fake Location 的模拟功能

---

### 4️⃣ 解决 ART 参数异常

* 在网上搜索关键词：

  <pre class="overflow-visible! px-0!" data-start="998" data-end="1023"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>ART</span><span> 参数异常 解决方法
  </span></span></code></div></div></pre>
* 你大概率会找到一个 `.sh` 脚本
* 使用 **MT 管理器**
* 以 **管理员（root）权限**运行该 `.sh` 文件

---

### 5️⃣ 重新开启模拟

* 再次打开 Fake Location
* 启动模拟

✅ 至此，**K20 Pro 配置完成**

---

## 五、K50 配置流程

1. 前面跟k20pro一样
2. 但还需要再在设置中把selinux调成enforcing(这个rom只要开始模拟selinux就只是宽容模式)

---

## 六、ROM 兼容性说明（非常重要）

* ❌ **绝大多数 ROM 无法使用**
* ❌ 不同 ROM 流程差异极大
* ✅ 目前只有miui14的安卓13可以使用

⚠️ 但请注意：

> **ROM 不是绝对标准，momo 才是**
> 只要 momo 检测环境正常：
>
> * ROM 理论上就有可能可用

---

## 七、最终结论

* ✔ 是否可用，只看 **momo 检测**
* ✔ 设备差异 > ROM 差异
* ✔ 流程不可照搬，需根据实际环境微调
* ❌ momo 不过，一切免谈

---

## 八、免责声明

> 本教程仅用于技术研究与环境记录帮助运动世界校园改进检测手段
> 不对任何使用后果负责
> 请自行判断风险

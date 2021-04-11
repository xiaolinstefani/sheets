# Sheets

<p>

  <img src="art/ic_library.png" width="96px" height="96px" alt="Sheets Library" align="left" style="margin-right: 24px; margin-bottom: 24px">

  <p>

在你的应用程序中快捷地使用对话框（dialogs)和bottom-sheets。你可以选择已有的sheets或者基于现有的功能上自定义sheets。

   <a href="https://search.maven.org/search?q=g:%22com.maxkeppeler.sheets%22">
     <img style="margin-right: 4px; margin-bottom: 8px;" alt="Version of Sheets library" src="https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/core.svg?label=Maven%20Central">
   </a>

   <a href="https://github.com/maxkeppeler/sheets">
     <img style="margin-right: 4px; margin-bottom: 8px;" alt="Codacy code quality of Sheets library" src="https://img.shields.io/codacy/grade/9a3b68b152e149fd82f0873e2fed78d5?label=Code%20Quality">
   </a>

   <a href="https://www.apache.org/licenses/LICENSE-2.0">
     <img style="margin-right: 4px; margin-bottom: 8px;" alt="GitHub" src="https://img.shields.io/github/license/maxkeppeler/sheets?color=%23007EC6&label=">
   </a>

<a href="https://github.com/maxkeppeler/sheets">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Give this library a star" src="https://img.shields.io/github/stars/maxkeppeler/sheets?style=social">
</a>

<a href="https://github.com/maxkeppeler/sheets/fork">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Fork this library" src="https://img.shields.io/github/forks/maxkeppeler/sheets?style=social">
</a>

<a href="https://github.com/maxkeppeler/sheets">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Watch this library" src="https://img.shields.io/github/watchers/maxkeppeler/sheets.svg?style=social&amp;label=Watch">
</a>

<a href="https://github.com/maxkeppeler/">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Follow me on GitHub" src="https://img.shields.io/github/followers/maxkeppeler?style=social&label=Follow">
</a>

<a href="https://twitter.com/intent/tweet?text=Checkout%20this%20beautiful%20library!%20%23android%20%23androiddev%20%23library%20%40maxkeppeler%20%0A%0Ahttps%3A%2F%2Fgithub.com%2Fmaxkeppeler%2Fsheets">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Share this library on Twitter" src="https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2Fmaxkeppeler%2Fsheets&label=Share">
</a>

<a href="https://twitter.com/maxkeppeler">
  <img style="margin-right: 4px; margin-bottom: 8px" alt="Follow Maximilian Keppeler on Twitter" src="https://img.shields.io/twitter/follow/maxkeppeler?label=Follow&style=social">
</a>

  </p>
</p>

读入用 [English](README.md) 或 [简体中文](README.zh_CN.md).


<img src="art/showcase.png" alt="sheets Library">

## 目录表

- [开始](#开始)
  - [信息Sheet](#信息)
  - [选项Sheet](#选项)
  - [钟点Sheet](#钟点)
  - [时长Sheet](#时长)
  - [输入Sheet](#输入)
  - [日历Sheet](#日历)
  - [颜色Sheet](#颜色)
  - [自定义Sheet](#自定义)
  - [Lottie](#lottie)
  - [外观](#外观)
- [杂项](#杂项)
  - [作品展示](#作品展示)
  - [支持这个项目](#支持这个项目)
  - [致谢](#致谢)
  - [许可](#许可)

# 开始

Sheet可以以dialog或者bottom-sheet的形式来显示。
查看 [例子](https://github.com/MaxKeppeler/sheets/blob/main/sample/sample.apk).

你必须使用 `core` 模块，因为它是所有sheet的基础。

在你的顶级 `build.gradle` 文件中:

```gradle
repositories {
  ...
  mavenCentral()
}
```

在你的应用程序 `build.gradle` 文件中:

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/core.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/core)

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:core:<latest-version>'
}
```

**基本功能** <br/>
Following functions can be called from any type of sheet.

| 功能                   | 作用                                                                             |
| --------------------- | -------------------------------------------------------------------------------- |
| style()               | 以dialog或者bottom-sheet的形式显示。                                                |
| title()               | 设置标题文本。                                                                     |
| titleColor()          | 设置标题文本颜色。                                                                  |
| titleColorRes()       | 用资源来设置标题文本颜色。                                                           |
| withCoverImage()      | 添加封面图像。                                                                     |
| topStyle()            | 指定封面图像和顶部栏的风格类型。                                                      |
| positiveButtonStyle() | 定义肯定按钮（正方向）的风格类型 (文本，填充，轮廓)。                                    |
| negativeButtonStyle() | 定义否定按钮（负方向）的风格类型 (文本，填充，轮廓)。                                    |
| withIconButton()      | 在顶部栏添加最多三个图标按钮。                                                        |
| closeIconButton()     | 设置自定义的关闭图标按钮。                                                           |
| displayHandle()       | 显示手柄（用来上下移动bottom-sheet)。                                                |
| displayCloseButton()  | 显示关闭图标按钮。                                                                  |
| displayToolbar()      | 显示工具栏。 (关闭图标按钮，标题，分隔线和图标按钮)                                      |
| peekHeight()          | 设置预览框的高度。(只适用于bottom-sheet)                                             |
| cornerRadius()        | 设置边角的圆弧半径。                                                               |
| cornerFamily()        | 设置边角家族。(切割的或者圆角的)                                                      |
| borderWidth()         | 设置边框宽度。                                                                     |
| borderColor()         | 设置边框颜色。                                                                     |
| cancelableOutside()   | 使在点击对话框以外的地方可以退出sheet。                                               |
| onNegative()          | 设置否定按钮的文本和侦听器（listener）。                                              |
| onPositive()          | 设置肯定按钮的文本和侦听器（listener）。                                              |
| onDismiss()           | 设置一个在关闭（点击肯定或否定按钮）sheet时会被调用的侦听器。                             |
| onCancel()            | 设置一个在取消（点击对话框以外的地方）sheet时会被调用的侦听器。（如果sheet可以被取消）      |
| onClose()             | 设置一个在sheet被关闭（包括以上两种形式）时会被调用的侦听器。                             |
| show()                | 显示sheet。                                                                  |

每个sheet都有一个叫`build`和`show`的扩展功能。<br/>

使用`build`来创建sheet并且以后再显示它。

    val sheet = InfoSheet().build(context) {
      // build sheet
    }

    sheet.show() // Show sheet when ready

如果你想在创建完sheet之后就立刻显示它，那就使用`show`。

    InfoSheet().show(context) {
      // build sheet
    } // Show sheet

## 信息

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/info.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/core)

`Info` Sheet能显示一般信息或者警告信息。

<details open>
<br/>
<br/>
<summary>以对话框为例的作品展示</summary>

<img src="art/InfoSheet Dialog.png" width="80%" alt="Sheets InfoSheet Dialog"><br/>
<img src="art/InfoSheet Dialog Cover TopStyle Top.png" width="80%" alt="Sheets InfoSheet Dialog"><br/>
<img src="art/InfoSheet Dialog Cover TopStyle Bottom.png" width="80%" alt="Sheets InfoSheet Dialog"><br/>
<img src="art/InfoSheet Dialog Cover TopStyle Mixed.png" width="80%" alt="Sheets InfoSheet Dialog"><br/>

</details>
</br>

<details>
<summary>以BottomSheet为例的作品展示</summary>

<br/>
<br/>
<img src="art/InfoSheet BottomSheet.png" width="80%" alt="Sheets InfoSheet"><br/>
<img src="art/InfoSheet BottomSheet Cover TopStyle Top.png" width="80%" alt="Sheets InfoSheet BottomSheet"><br/>
<img src="art/InfoSheet BottomSheet Cover TopStyle Bottom.png" width="80%" alt="Sheets InfoSheet BottomSheet"><br/>
<img src="art/InfoSheet BottomSheet Cover TopStyle Mixed.png" width="80%" alt="Sheets InfoSheet BottomSheet"><br/>
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:info:<latest-version>'
}
```

### 用法

默认的信息sheet用法如下：

    InfoSheet().show(context) {
      title("Do you want to install Awake?")
      content("Awake is a beautiful alarm app with morning challenges, advanced alarm management and more.")
      onNegative("No") {
        // Handle event
      }
      onPositive("Install") {
        // Handle event
      }
    }

| 功能             | 作用                |
| --------------- | ------------------- |
| content()       | 设置内容文本。        |
| drawable()      | 设置可绘制资源。       |
| drawableColor() | 设置可绘制资源的颜色。 |

## 选项

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/options.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/options)

这个`Options`Sheet能使各种选项以网格或者列表的形式呈现。

<details open>
<br/><br/>
<summary>以对话框为例的作品展示</summary>

<img src="art/OptionsSheet Dialog Grid Middle.png" width="80%" alt="Sheets OptionsSheet Dialog">
</details>
</br>

<details>
<br/><br/>
<summary>以BottomSheet为例的作品展示</summary>

<img src="art/OptionsSheet BottomSheet Grid Middle.png" width="80%" alt="Sheets OptionsSheet BottomSheet">
</details>

<br/>
<details>
<br/><br/>
<summary>以对话框形式的额外作品展示</summary>

<img src="art/OptionsSheet Dialog List.png" width="80%" alt="Sheets OptionsSheet Dialog"><br/>
<img src="art/OptionsSheet Dialog Grid Small.png" width="80%" alt="Sheets OptionsSheet" Dialog><br/>
<img src="art/OptionsSheet Dialog Grid Large Horizontal.png" width="80%" alt="Sheets OptionsSheet" Dialog><br/>

</details>
</br>

<details>
<br/><br/>
<summary>以BottomSheets形式的额外作品展示</summary>

<img src="art/OptionsSheet BottomSheet List.png" width="80%" alt="Sheets OptionsSheet BottomSheet"><br/>
<img src="art/OptionsSheet BottomSheet Grid Small.png" width="80%" alt="Sheets OptionsSheet" BottomSheet><br/>
<img src="art/OptionsSheet BottomSheet Grid Large Horizontal.png" width="80%" alt="Sheets OptionsSheet" BottomSheet><br/>

</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:info:<latest-version>'
}
```

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:options:<latest-version>'
}
```

### 用法

默认的选项sheet用法如下：

    OptionsSheet().show(context) {
      title("Text message")
      with(
        Option(R.drawable.ic_copy, "Copy"),
        Option(R.drawable.ic_translate, "Translate"),
        Option(R.drawable.ic_paste, "Paste")
      )
      onPositive { index: Int, option: Option ->
        // Handle selected option
      }
    }

| 功能                         | 作用                                                                                   |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| multipleChoices()            | 允许多项选择的内容。                                                                      |
| displayMultipleChoicesInfo() | 显示多项选择的相关说明。                                                                   |
| maxChoicesStrictLimit()      | 指定最多可选项受限并且暂时无法选择更多选项。                                                  |
| minChoices()                 | 设置最少可选项。                                                                          |
| maxChoices()                 | 设置最多可选项。                                                                          |
| onPositiveMultiple()         | 设置多项选择的侦听器。                                                                     |
| displayButtons()             | 显示按钮，并且需要点击肯定按钮来确认所选项。                                                  |
| displayMode()                | 以列表或垂直/水平的可滑动的网格形式来显示选项。                                                |

**选项**

| 功能        | 作用                 |
| ---------- | -------------------- |
| selected() | 预选一个选项。         |
| disable()  | 禁用一个选项。         |

**注意**: 预选项会自动增加当前所选项的数量，而禁用的选项会减少最多可选项的数量。

## 钟点

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/time-clock.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/time-clock)

`Clock Time` Sheet能使你快速地选择一个时间。

<details>
<br/><br/>
<summary>以对话框为例的作品展示</summary>

<img src="art/ClockTimeSheet Dialog.png" width="80%" alt="Sheets OptionsSheet Dialog">
</details>
</br>

<details open>
<br/><br/>
<summary>以BottomSheet为例的作品展示</summary>

<img src="art/ClockTimeSheet BottomSheet.png" width="80%" alt="Sheets OptionsSheet BottomSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:time-clock:<latest-version>'
}
```

### 用法

对于默认的钟点sheet，以24小时的格式，用法如下：

    ClockTimeSheet().show(context) {
      title("Wake-up time")
      onPositive { clockTimeInMillis: Long ->
        // Handle selected time
      }
    }

| 功能             | 作用                                  |
| --------------- | ------------------------------------- |
| format24Hours() | 使用24小时或12小时的格式。                |
| currentTime()   | 以毫秒为单位设置当前时间。                |

## 时长

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/time.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/time)

`Time` Sheet能使你以特定的格式选择一个持续时间。

<details open>
<br/><br/>
<summary>以对话框为例的作品展示</summary>

<img src="art/TimeSheet Dialog.png" width="80%" alt="Sheets TimeSheet Dialog">
</details>
</br>

<details>
<br/><br/>
<summary>以BottomSheet为例的作品展示</summary>

<img src="art/TimeSheet BottomSheet.png" width="80%" alt="Sheets TimeSheet BottomSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:time:<latest-version>'
}
```

### 用法

默认的时长sheet用法如下：

    TimeSheet().show(context) {
      title("Snooze time")
      onPositive { durationTimeInMillis: Long ->
        // Handle selected time
      }
    }

| 功能           | 作用                                            |
| ------------- | ----------------------------------------------- |
| format()      | Select the time format. (hh:mm:ss, mm:ss, ...) |
| currentTime() | 以秒为单位设置当前时长。                           |
| minTime()     | 设置最短时长。                                   |
| maxTime()     | 设置最长时长。                                   |

## 输入

[ ![下载](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/input.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/input)

`Input` Sheet使你可以显示包含各种输入的表单。

<details>
<br/><br/>
<summary>以对话框为例的作品展示</summary>

<img src="art/InputSheet Dialog Short.png" width="80%" alt="Sheets InputSheet Dialog">
</details>
</br>

<details open>
<br/><br/>
<summary>以BottomSheet为例的作品展示</summary>

<img src="art/InputSheet BottomSheet Short.png" width="80%" alt="Sheets InputSheet BottomSheet">
</details>

<br/>
<details>
<br/><br/>
<summary>以对话框形式的额外作品展示</summary>

<img src="art/InputSheet Dialog Long.png" width="80%" alt="Sheets InputSheet Dialog"><br/>

</details>
</br>

<details>
<br/><br/>
<summary>以BottomSheets形式的额外作品展示</summary>

<img src="art/InputSheet BottomSheet Long.png" width="80%" alt="Sheets InputSheet BottomSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:input:<latest-version>'
}
```

### 用法

默认的输入sheet用法如下：

    InputSheet()).show(context) {
        title("Short survey")
        content("We would like to ask you some questions reading your streaming platform usage.")
      with(InputEditText {
        required())
        label("Your favorite TV-Show")
        hint("The Mandalorian, ...")
        validationListener { value -> } // Add custom validation logic
        changeListener { value -> } // Input value changed
        resultListener { value -> } // Input value changed when form finished
      })
      with(InputCheckBox("binge_watching") { // Read value later by index or custom key from bundle
        label("Binge Watching")
        text("I'm regularly binge watching shows on Netflix.")
        // ... more options
      })
      with(InputRadioButtons() {
        required()
        label("Streaming service of your choice")
        options(mutableListOf("Netflix", "Amazon", "Other"))
      })
      // ... more input options
      onNegative { showToast("InputSheet cancelled", "No result") }
      onPositive { result ->
          showToastLong("InputSheet result", result.toString())
          val text = result.getString("0") // Read value of inputs by index
          val check = result.getBoolean("binge_watching") // Read value by passed key
      }
    }

| 功能       | 作用                                          |
| --------- | --------------------------------------------- |
| with()    | 添加输入。（参考输入选项）                        |
| content() | 设置内容文本（例如：解释一项调查）                  |

**输入选项**

- `InputEditText`
- `InputCheckBox`
- `InputRadioButtons`
- `InputSpinner`

**输入**<br/>

| Function         | Action                           |
| ---------------- | -------------------------------- |
| label()          | Set the label text.              |
| drawable()       | Set the drawable.                |
| required()       | Mark input as required.          |
| changeListener() | Set listener to observe changes. |
| resultListener() | Set listener for final value.    |

**InputEditText**<br/>

| Function             | Action                                            |
| -------------------- | ------------------------------------------------- |
| hint()               | Set the hint text.                                |
| defaultValue()       | Set default text.                                 |
| inputType()          | Set the `android.text.InputType`'s.               |
| inputFilter()        | Set the `android.text.inputFilter`                |
| maxLines()           | Set the max amount of lines.                      |
| endIconMode()        | Set TextInputLayout.EndIconMode.                  |
| endIconActivated()   | Set the EndIcon activated.                        |
| passwordVisible()    | Make the password initially visible or invisible. |
| validationListener() | Validate the text input with your own logic.      |

**InputCheckBox** <br/>

| Function       | Action             |
| -------------- | ------------------ |
| text()         | Set the text.      |
| defaultValue() | Set default value. |

**InputRadioButtons** <br/>

| Function   | Action                             |
| ---------- | ---------------------------------- |
| options()  | Set a list of RadioButton options. |
| selected() | Set a selected index.              |

**InputSpinner** <br/>

| Function          | Action                                                    |
| ----------------- | --------------------------------------------------------- |
| noSelectionText() | Set the text that is displayed, when nothing is selected. |
| options()         | Set a list of options.                                    |
| selected()        | Set a selected index.                                     |

## Calendar

[ ![Download](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/calendar.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.calendar/core)

The `Calendar` Sheet lets you pick a date or date range. This type was build using the library [CalendarView](https://github.com/kizitonwose/CalendarView).

<details open>
<br/><br/>
<summary>Showcase as Dialog</summary>

<img src="art/CalendarSheet Dialog Period.png" width="80%" alt="Sheets CalendarSheet Dialog">
</details>
</br>

<details>
<br/><br/>
<summary>Showcase as BottomSheet</summary>

<img src="art/CalendarSheet BottomSheet Period.png" width="80%" alt="Sheets CalendarSheet BottomSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:calendar:<latest-version>'
}
```

### Usage

For the default time sheet use it as following:

    CalendarSheet().show(this) { // Build and show
      title("What's your date of birth?") // Set the title of the sheet
      onPositive { dateStart, dateEnd ->
        // Handle date or range
      }

| Function          | Action                                                           |
| ----------------- | ---------------------------------------------------------------- |
| selectionMode()   | Choose the selection mode (date or range).                       |
| calendarMode()    | Choose the calendar mode (week with various rows or month-view). |
| disableTimeline() |  Disable either past or future dates.                            |
| rangeYears()      | Set the range of years into past and future.                     |
| disable()         | Pass a `Calendar` object to disable various dates for selection. |
| displayButtons()  | Show or hide the buttons view.                                   |

## Color

[ ![Download](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/color.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/color)

The `Color` Sheet lets you pick a color. Display the default material colors or specify which colors can be choosen from. You can allow to chose a custom color as well.

<details>
<br/><br/>
<summary>Showcase as Dialog</summary>

<img src="art/ColorSheet Dialog Templates.png" width="80%" alt="Sheets ColorSheet Dialog"><br/>
<img src="art/ColorSheet Dialog Custom.png" width="80%" alt="Sheets ColorSheet Dialog">

</details>
</br>

<details open>
<br/><br/>
<summary>Showcase as BottomSheet</summary>

<img src="art/ColorSheet BottomSheet Templates.png" width="80%" alt="Sheets ColorSheet BottomSheet"><br/>
<img src="art/ColorSheet BottomSheet Custom.png" width="80%" alt="Sheets ColorSheet BottomSheet">

</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:color:<latest-version>'
}
```

### Usage

For the default color sheet use it as following:

    ColorSheet().show(context) {
      title("Background color")
      onPositive { color ->
        // Use color
      }
    }

| Function                 | Action                                                           |
| ------------------------ | ---------------------------------------------------------------- |
| defaultView()            | Select the default color view (Colors from templates or custom). |
| disableSwitchColorView() | Disable to switch between color views.                           |
| defaultColor()           | Set default selected color.                                      |
| colors()                 | Pass all colors to be displayed in the color templates view.     |
| disableAlpha()           | Disable alpha colors for custom colors.                          |

## Custom

With just the 'core' module you are able to create your own sheet based on this library. You can use some components and styles within your own custom sheet automatically. By default the buttons and toolbar view with logic is ready to be used by your own implementation.

<details>
<br/><br/>
<summary>Showcase as Dialog</summary>

<img src="art/Custom Sheet Dialog.png" width="80%" alt="Sheets Custom Dialog">
</details>
</br>

<details open>
<br/><br/>
<summary>Showcase as BottomSheet</summary>

<img src="art/Custom Sheet BottomSheet.png" width="80%" alt="Sheets Custom BottomSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:core:<latest-version>'
}
```

### Get started

You can find a custom sheet implementation in the sample module.

1.  Step: Create a class and extend from the class `Sheet`.

    class CustomSheet : Sheet() {

2.  Step: Implement the method: `onCreateLayoutView` and pass your custom layout.

    override fun onCreateLayoutView(): View {
    return LayoutInflater.from(activity).inflate(R.layout.sheets_custom, null)
    }

All of the base functionality can be used and on top of that you can extend the logic and behavior as you wish.

### Components

You are free to use the components this library uses for it's sheet types.

- `SheetTitle`
- `SheetContent`
- `SheetDigit`
- `SheetNumericalInput`
- `SheetDivider`
- `SheetButton`
- `SheetEdit`
- `SheetRecyclerView`
- `SheetValue`

## Lottie

[ ![Download](https://img.shields.io/maven-central/v/com.maxkeppeler.sheets/lottie.svg?label=Maven%20Central) ](https://search.maven.org/artifact/com.maxkeppeler.sheets/lottie)

The `Lottie` modules gives you the ability to use a [Lottie animations](https://airbnb.design/lottie/) as cover view.

<details open>
<br/>
<br/>
<summary>Showcase as Dialog</summary>

<img src="art/InfoSheet Dialog Cover Lottie Animation.png" width="80%" alt="Sheets InfoSheet">
</details>
</br>

<details>
<summary>Showcase as BottomSheet</summary>

<br/>
<br/>
<img src="art/InfoSheet BottomSheet Cover Lottie Animation.png" width="80%" alt="Sheets InfoSheet">
</details>

```gradle
dependencies {
  ...
  implementation 'com.maxkeppeler.sheets:lottie:<latest-version>'
}
```

### Usage

You can use the Lottie animation as a cover for any type of sheet.

    InfoSheet().show(this) {
      title("Team Collaboration")
      content("In the world of software projects, it is inevitable...")
      ...
      withCoverLottieAnimation(LottieAnimation {
        setAnimation(R.raw.anim_lottie_business_team)
        ... Setup Lottie animation
      })
      ...
    }

| Function               | Action                |
| ---------------------- | --------------------- |
| playCoverAnimation()   | Play the animation.   |
| resumeCoverAnimation() | Resume the animation. |
| pauseCoverAnimation()  | Pause the animation.  |
| cancelCoverAnimation() | Cancel the animation. |

## Appearance

By default, the library switches to either day or night mode depending on the attr `textColorPrimary`.
By default it uses the activity's colorPrimary. The default `highlightColor` is generated based on the color `sheetPrimaryColor`, or if not available `colorPrimary`.

### Base

You want a different sheet background shape?
Then just override the corner family and radius.

    <item name="sheetCornerRadius">12dp</item>
    <item name="sheetCornerFamily">cut</item>

Just overwrite the base colors, if you want to achieve a different look of the sheets than your app.

    <item name="sheetPrimaryColor">@color/customPrimaryColor</item>
    <item name="sheetHighlightColor">@color/customHighlightColor</item>
    <item name="sheetBackgroundColor">@color/customBackgroundColor</item>
    <item name="sheetDividerColor">@color/customDividerColor</item>
    <item name="sheetIconsColor">@color/customIconsColor</item>

You can override the basic style of a sheet. Instead of displaying the toolbar, you can just hide it and display the typical handle.

    <item name="sheetDisplayHandle">true</item>
    <item name="sheetDisplayToolbar">false</item>
    <item name="sheetDisplayCloseButton">false</item>

Change the appearance of the title.

    <item name="sheetTitleColor">@color/customTitleTextColor</item>
    <item name="sheetTitleFont">@font/font</item>
    <item name="sheetTitleLineHeight">@dimen/dimen</item>
    <item name="sheetTitleLetterSpacing">value</item>

Change the appearance of the content text.

    <item name="sheetContentColor">@color/customContentTextColor</item>
    <item name="sheetContentInverseColor">@color/customContentTextInverseColor</item>
    <item name="sheetContentFont">@font/font</item>
    <item name="sheetContentLineHeight">@dimen/dimen</item>
    <item name="sheetContentLetterSpacing">value</item>

Change the appearance of the value texts. (e.g. the time in the TimeSheet & ClockTimeSheet or the selected date & period in the Calendarsheet.)

    <item name="sheetValueTextActiveColor">@color/customValueTextColor</item>
    <item name="sheetValueFont">@font/font</item>
    <item name="sheetValueLineHeight">@dimen/dimen</item>
    <item name="sheetValueLetterSpacing">value</item>

Change the appearance of the digit keys on the numerical input.

    <item name="sheetDigitColor">@color/customDigitTextColor</item>
    <item name="sheetDigitFont">@font/font</item>
    <item name="sheetDigitLineHeight">@dimen/dimen</item>
    <item name="sheetDigitLetterSpacing">value</item>

### Buttons

Override the appearance of the button text.

    <item name="sheetButtonTextFont">@font/font</item>
    <item name="sheetButtonTextLetterSpacing">value</item>

Override the general appearance of the buttons (negative and positive button).

    <item name="sheetButtonColor">@color/customButtonColor<item>
    <item name="sheetButtonTextFont">@font/font<item>
    <item name="sheetButtonTextLetterSpacing">value<item>
    <item name="sheetButtonCornerRadius">12dp<item>
    <item name="sheetButtonCornerFamily">cut<item>
    <item name="sheetButtonWidth">match_content/wrap_content<item>

Override the appearance of the negative button.

    <item name="sheetNegativeButtonType">text_button/outlined_button/button<item>
    <item name="sheetNegativeButtonCornerRadius">12dp<item>
    <item name="sheetNegativeButtonCornerFamily">cut<item>

Override the appearance of the positive button.

    <item name="sheetPositiveButtonType">text_button/outlined_button/button<item>
    <item name="sheetPositiveButtonCornerRadius">12dp<item>
    <item name="sheetPositiveButtonCornerFamily">cut<item>

Override the border appearance of the outlined button.

    <item name="sheetButtonOutlinedButtonBorderColor">@color/borderColor<item>
    <item name="sheetButtonOutlinedButtonBorderWidth">1dp<item>

The corner family and radius is applied to the button shape or in the case of a outlined or text button, to the ripple background shape.

**Fine control**
You can even define the corner family and radius of the negative and positive button for each corner.

    <item name="sheetNegativeButtonBottomLeftCornerRadius">4dp<item>
    <item name="sheetNegativeButtonBottomLeftCornerFamily">cut<item>
    ...
    <item name="sheetPositiveButtonBottomRightCornerRadius">8dp<item>
    <item name="sheetPositiveButtonBottomRightCornerFamily">rounded<item>

### Handle

The size and the appearance of the handle can be changed like this:

    <item name="sheetHandleCornerRadius">8dp</item>
    <item name="sheetHandleCornerFamily">rounded</item>
    <item name="sheetHandleFillColor">?sheetPrimaryColor</item>
    <item name="sheetHandleBorderColor">?sheetPrimaryColor</item>
    <item name="sheetHandleBorderWidth">1dp</item>
    <item name="sheetHandleWidth">42dp</item>
    <item name="sheetHandleHeight">4dp</item>

### OptionsSheet

Override appearance of selected options.

    <item name="sheetOptionSelectedImageColor">@color/customSelectedOptionImageColor</item>
    <item name="sheetOptionSelectedTextColor">@color/customSelectedOptionTextColor</item>

Override appearance of disabled options.

    <item name="sheetOptionDisabledImageColor">@color/customDisabledOptionImageColor</item>s
    <item name="sheetOptionDisabledTextColor">@color/customDisabledOptionImageColor</item>
    <item name="sheetOptionDisabledBackgroundColor">@color/customDisabledOptionBackgColor</item>

### InputSheet

Override the appearance of the TextInputLayout (used for the InputEditText).

    <item name="sheetTextInputLayoutCornerRadius">12dp</item>
    <item name="sheetTextInputLayoutBottomLeftCornerRadius">12dp</item>
    ... and for all other corners
    <item name="sheetTextInputLayoutEndIconColor">@color/customEndIconColor</item>
    <item name="sheetTextInputLayoutHelperTextColor">@color/customHelperTextColor</item>
    <item name="sheetTextInputLayoutBoxStrokeColor">@color/customBoxStrokeColor</item>
    <item name="sheetTextInputLayoutHintTextColor">@color/customHintTextColor</item>
    <item name="sheetTextInputLayoutBoxStrokeErrorColor">@color/customBoxStrokeErrorColor</item>
    <item name="sheetTextInputLayoutErrorTextColor">@color/customErrorTextColor</item>

# Misc

## Showcase

Check out some real apps which use this library.<br/>
Feel free to hit me up to include your app here.

- [Sign for Spotify](https://play.google.com/store/apps/details?id=com.mk.sign.spotifyv2) - Playlist and control widgets for Spotify on your home screen. (Uses: `Info`, `Options`, `Input`, `Color`)

- [Buddha Quotes](https://play.google.com/store/apps/details?id=org.bandev.buddhaquotes) - A collaborative project to create a Free and Open Source Buddha Quotes app for Android with a focus on privacy. (Uses: `Options`, `Input`, `Color`, `Time`)

## Support this project

- Leave a **Star** and tell other devs about it.

- **Watch** for updates and improvements.

- **[Open an issue](https://github.com/MaxKeppeler/sheets/issues/)** if you see or got any error.

- Leave your thanks [here](https://github.com/MaxKeppeler/sheets/discussions/categories/show-and-tell) and showcase your implementation.

## Motivation

I created several sheets for my apps [Sign for Spotify](https://play.google.com/store/apps/details?id=com.mk.sign.spotifyv2) and [Awake](https://play.google.com/store/apps/details?id=com.mk.awake) in the recent months.
I especially wanted to have a 'writable' clock time and duration time picker in form of a sheet
This is my first library - I'm happy about any feedback, tips etc. I hope you like it and can make use of it. :)

## Credits

- Thanks to [Sasikanth](https://github.com/msasikanth) for inspiration regarding the the appearance of the sheets through [Color Sheet](https://github.com/msasikanth/ColorSheet) and [Memoire](https://play.google.com/store/apps/details?id=com.primudesigns.stories).
- Thanks to [Aidan Follestad](https://github.com/afollestad) and his [material-dialogs](https://github.com/afollestad/material-dialogs) library for the inspiration to make this library modular.

## License

    Copyright 2020 Maximilian Keppeler https://maxkeppeler.com

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

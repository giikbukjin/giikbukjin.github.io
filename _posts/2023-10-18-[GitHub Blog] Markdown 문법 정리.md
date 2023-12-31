---
title: "[GitHub Blog] Markdown 문법 정리"
date: 2023-10-18 09:00:00 +09:00
categories: [기록, 블로그]
tags: [GitHub.io, Markdown]
pin: true
math: true
mermaid: false
image:
  path: https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Tortoise_Fred.jpg/600px-Tortoise_Fred.jpg
published: true
---


깃허브 블로그에 글을 쓰려면 마크다운 문법을 알아야 한다. 
깃허브 Readme를 쓸 때 처음 접해봤지만 쓸 때마다 문법을 검색해 보고 익숙하지 않아서 작성도 오래 걸렸었다.

블로그에 글을 쓰기 전 노션에 미리 글감을 적어 두는 편인데 인용문이나 글머리 기호 같은 노션의 요소들이 마크다운 문법 요소와 비슷해서 옮기기 좋은 것 같다. (노션에 마크다운 파일로 내보내는 기능도 있다!)
요 며칠 블로그 글을 써 봤는데 조금은 익숙해진 것 같다.

자주 쓰는 기능들을 한 포스팅에 정리해놓으려고 한다. 


## 본문에 포함되지 않는 포스팅 설정

```
---
title: "포스팅 제목"
date: YYYY-MM-DD HH:MM:SS +09:00
categories: [주 카테고리, 부 카테고리]
tags: [태그 1, 태그 2, 태그 3...]
pin: 고정 여부 (true/false)
math: 수식 포함 여부 (true/false)
mermaid: diagrams & flowcharts 포함 여부 (true/false)
image:
  path: 썸네일 이미지 경로
  alt: 썸네일 이미지 하단 설명
published: true
---
```
> title을 작성할 때 큰따옴표("")로 묶지 않으면 대괄호를 사용할 수 없다.
{: .prompt-tip }

<br><br>


## Headings

# H1 - heading
```
# H1 - heading
```

## H2 - heading
```
# H2 - heading
```

### H3 - heading
```
# H3 - heading
```

#### H4 - heading
```
# H4 - heading
```

## Image
```
![](https://외부 이미지 경로/이미지 이름.jpg)

또는

/assets/img/로컬 이미지 경로/이미지 이름.png
```
<br>


## Lists

### Ordered list

1. Firstly
2. Secondly
3. Thirdly

```
1. Firstly
2. Secondly
3. Thirdly
```

### Unordered list

- Chapter
  + Section
    * Paragraph

```
- Chapter
  + Section
    * Paragraph
```

### ToDo list

- [ ] Job
  + [x] Step 1
  + [x] Step 2
  + [ ] Step 3

```
- [ ] Job
  + [x] Step 1
  + [x] Step 2
  + [ ] Step 3
```

### Description list

Turtle
: a reptile that lives mostly in water and that has a hard shell which covers its body see also sea.

```
Turtle
: a reptile that lives mostly in water and that has a hard shell which covers its body see also sea.
```
<br>


## Block Quote

> This line shows the _block quote_.

```
> This line shows the _block quote_.
```

## Prompts

> An example showing the `tip` type prompt.
{: .prompt-tip }

> An example showing the `info` type prompt.
{: .prompt-info }

> An example showing the `warning` type prompt.
{: .prompt-warning }

> An example showing the `danger` type prompt.
{: .prompt-danger }

```
> An example showing the `tip` type prompt.
{: .prompt-tip }

> An example showing the `info` type prompt.
{: .prompt-info }

> An example showing the `warning` type prompt.
{: .prompt-warning }

> An example showing the `danger` type prompt.
{: .prompt-danger }
```
<br>


## Tables

| 좌측 정렬               | 우측 정렬               |
|:------------------------|-----------------------: |
| 표 내용                 | 표 내용                 |
| 표 내용 표 내용         | 표 내용 표 내용         |
| 표 내용 표 내용 표 내용 | 표 내용 표 내용 표 내용 |

## Links

<http://127.0.0.1:4000>

## Footnote

Click the hook will locate the footnote[^footnote], and here is another footnote[^fn-nth-2].

## Inline code

This is an example of `Inline Code`.

## Filepath

Here is the `/path/to/the/file.extend`{: .filepath}.

## Code blocks

### Common

```
This is a common code snippet, without syntax highlight and line number.
```

### Specific Language

```bash
if [ $? -ne 0 ]; then
  echo "The command was not successful.";
  #do the needful / exit
fi;
```

### Specific filename

```sass
@import
  "colors/light-typography",
  "colors/dark-typography";
```
{: file='_sass/jekyll-theme-chirpy.scss'}

## Mathematics

The mathematics powered by [**MathJax**](https://www.mathjax.org/):

$$ \sum_{n=1}^\infty 1/n^2 = \frac{\pi^2}{6} $$

When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are

$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

## Mermaid SVG

```mermaid
 gantt
  title  Adding GANTT diagram functionality to mermaid
  apple :a, 2017-07-20, 1w
  banana :crit, b, 2017-07-23, 1d
  cherry :active, c, after b a, 1d
```

## Images

### Default (with caption)

![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" }
_Full screen width and center alignment_

### Left aligned

![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-75 .normal}

### Float to left

![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-50 .left}
Praesent maximus aliquam sapien. Sed vel neque in dolor pulvinar auctor. Maecenas pharetra, sem sit amet interdum posuere, tellus lacus eleifend magna, ac lobortis felis ipsum id sapien. Proin ornare rutrum metus, ac convallis diam volutpat sit amet. Phasellus volutpat, elit sit amet tincidunt mollis, felis mi scelerisque mauris, ut facilisis leo magna accumsan sapien. In rutrum vehicula nisl eget tempor. Nullam maximus ullamcorper libero non maximus. Integer ultricies velit id convallis varius. Praesent eu nisl eu urna finibus ultrices id nec ex. Mauris ac mattis quam. Fusce aliquam est nec sapien bibendum, vitae malesuada ligula condimentum.

### Float to right

![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-50 .right}
Praesent maximus aliquam sapien. Sed vel neque in dolor pulvinar auctor. Maecenas pharetra, sem sit amet interdum posuere, tellus lacus eleifend magna, ac lobortis felis ipsum id sapien. Proin ornare rutrum metus, ac convallis diam volutpat sit amet. Phasellus volutpat, elit sit amet tincidunt mollis, felis mi scelerisque mauris, ut facilisis leo magna accumsan sapien. In rutrum vehicula nisl eget tempor. Nullam maximus ullamcorper libero non maximus. Integer ultricies velit id convallis varius. Praesent eu nisl eu urna finibus ultrices id nec ex. Mauris ac mattis quam. Fusce aliquam est nec sapien bibendum, vitae malesuada ligula condimentum.

### Dark/Light mode & Shadow

The image below will toggle dark/light mode based on theme preference, notice it has shadows.

![light mode only](/posts/20190808/devtools-light.png){: .light .w-75 .shadow .rounded-10 w='1212' h='668' }
![dark mode only](/posts/20190808/devtools-dark.png){: .dark .w-75 .shadow .rounded-10 w='1212' h='668' }

## Video

{% include embed/youtube.html id='Balreaj8Yqs' %}

## Reverse Footnote

[^footnote]: The footnote source
[^fn-nth-2]: The 2nd footnote source
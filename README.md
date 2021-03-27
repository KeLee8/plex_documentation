# 命名和组织电影文件

当您的主要内容类型彼此分开时，Plex 使用的扫描器和元数据采集器将发挥最佳效果。我们强烈建议将电影和电视内容分成单独的主目录。
例如，您可以参考以下分类保存的目录方案：

```plaintext
/Media
   /Movies
      movie content
   /Music
      music content
   /TV Shows
      television content
```

> 警告！Plex 会尽最大努力寻找和匹配适当的内容。但是，如果未能将电影和电视节目等内容存储在不同的目录下，可能会导致影片的信息采集错误或者失败。

您可能具有用于影片的海报和背景、字幕，以及自己的电影`“附加内容”`等图像文件。要使用这些图像文件，请确保它们已正确命名和组织，并且正确启用了本地媒体信息来源并对其进行了排序。

相关页面：[本地媒体资源 - 电影](https://support.plex.tv/articles/200220677-local-media-assets-movies/)

> 注意：我们在命名/整理说明中使用 `.ext` 用作通用文件扩展名。当然，您应该为文件使用适当的文件扩展名。(默认情况下，某些操作系统如 Windows 可能会隐藏文件扩展名。)

# 文件夹中的电影文件

我们建议您将每个电影文件放置在其对应的文件夹中，因为它可以大幅提高资料库的扫描速度。如果您有电影的外部媒体（例如自定义海报和外部字幕文件等），则通常应将电影与自定义媒体文件一起放在该电影的文件夹中。将该文件夹命名为与电影文件相同的名称：

* /Movies/片名(发布年份)/片名(发布年份).ext

```plaintext
/Movies
   /Avatar(2009)
      Avatar(2009).mkv
   /Batman Begins(2005)
      Batman Begins(2005).mp4
      Batman Begins(2005).en.srt
      poster.jpg
```

如果使用 Plex Media Server v1.20.1 及更高版本中提供的 Plex Movie 采集器（非“旧版”），你还可以在大括号中使用 IMDb 或 TheMovieDB 的 ID 号来帮助匹配电影。不过它必须遵循 `{[source]-[id]}` 的形式。

```plaintext
/Movies
   /Batman Begins(2005) {imdb-tt0372784}
      Batman Begins(2005) {imdb-tt0372784}.mp4
```

```plaintext
/Movies
   /Batman Begins(2005) {tmdb-272}
      Batman Begins(2005) {tmdb-272}.mp4
```

相关页面：[使用字幕](https://support.plex.tv/articles/categories/your-media/using-subtitles/)
相关页面：[本地媒体资源 - 电影](https://support.plex.tv/articles/200220677-local-media-assets-movies/)

# 单独的电影文件

你还可以将电影文件放置在同一个主文件夹中。除非您具有特定电影的自定义媒体（例如海报），否则目录结构并不重要。请按以下方式正确命名电影文件：

* 片名(发布年份).ext

```plaintext
/Movies
   Avatar (2009).mkv
   Batman Begins (2005).mp4
```

# 被分割成多个文件的电影

如果命名正确，则被分割成多个文件（例如 pt1，pt2）的电影可以作为一个项目（在大多数播放器中）播放。分割的电影必须放置在它们自己的文件夹中，该文件夹按影片的常规命名。命名文件如下：

* /Movies/片名(发布年份)/片名(发布年份) – 分割名称.ext

其中`分割名称`类似一下情况：

* cdX
* discX
* diskX
* dvdX
* partX
* ptX

……然后你用适当的数字 1，2，3 等代替 `X`。

```plaintext
/Movies
   /The Dark Knight (2008)
      The Dark Knight (2008) - pt1.mp4
      The Dark Knight (2008) - pt2.mp4
```

> 注意事项

    并非所有的 Plex 应用程序都支持播放分割媒体；
    所有的分割文件必须是相同的文件格式（如所有 MP4 或所有 MKV）；
    所有的分割文件都应该有相同的音频和字幕，且顺序相同；
    只支持最多 8 个分割文件的播放；
    “其他视频”库或使用 “Plex 视频文件扫描器”的库不支持播放分割内容。

然而，为了获得更好的体验，我们鼓励您使用一款第三方工具来合并多个分割过的视频。有多种方法可以做到这一点，在搜索引擎中搜索如何“合并视频”。下面是一个非官方的教程，它是一个免费的工具，目前已经发布在我们的论坛。

相关页面：[使用 MKVtoolnix GUI 合并电影文件](https://forums.plex.tv/t/howto-joining-multi-part-movies-files-with-mkvtoolnix-gui/113211/1)

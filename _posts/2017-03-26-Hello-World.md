---
layout: post
title: Up and running!
published: true
---
### First Post
Getting a blog site up and running quickly

[From this](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)

syntax highlighting 4

~~~ javascript
function closestTr(el) { // Native
  if (el.tagName === 'TR') {
    if (el.rowIndex % 6 === 0) {return el;}
    return;
  }
  if (el.tagName === 'TABLE') {return;}
  return closestTr(el.parentNode);
}
~~~


~~~ sql
SELECT
    DbName = DB_NAME()
  , FilegroupName = f.name
  , FileName = d.name
  , TotalSizeMB = d.size / 128.0
  , SpaceUsedMB = CAST(FILEPROPERTY(d.name, 'SpaceUsed') AS int) / 128.0
  , FreeSpaceMB = d.size / 128.0 - CAST(FILEPROPERTY(d.name, 'SpaceUsed') AS int) / 128.0
  , FreeSpacePcnt = (d.size - CAST(FILEPROPERTY(d.name, 'SpaceUsed') AS int)) / (d.size * 1.0)
  , PhysicalName = d.physical_name
FROM
    sys.database_files d
    INNER JOIN sys.filegroups f
        ON d.data_space_id = f.data_space_id
WHERE
    d.name NOT LIKE '%[_]log'
ORDER BY
    FreeSpacePcnt DESC
~~~


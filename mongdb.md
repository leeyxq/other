mongodb 全文本搜索
===

创建全文本索引

    db.stores.createIndex( { name: "text", description: "text" } )

全文本搜索

    db.stores.find( { $text: { $search: 字符串 } } )

技巧一 字符串"java coffee shop"表示搜索 “java” or “coffee” or “shop”关键字，或的关系，只有一个关键字匹配即可搜索得到

    db.stores.find( { $text: { $search: "java coffee shop" } } )

技巧二 多关键字 and匹配搜索 如："\"java\" \"coffee\" \"shop\"" 表示搜索 “java” and “coffee” and “shop”关键字，and关系，必须全部匹配才可搜索得到

    db.stores.find( { $text: { $search: "\"java\" \"coffee\" \"shop\"" } } )


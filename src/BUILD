java_binary(
  name="reddit_bot",
  srcs=[
    "main/java/pl/jpetryk/redditbot/Runner.java",
    "main/java/pl/jpetryk/redditbot/BotModule.java",
  ],
  main_class = 'pl.jpetryk.redditbot.Runner',
  deps = [
    ':tweets_in_comments_bot',
    '//src:abstract_reddit_bot',
    '//src/main/java/pl/jpetryk/redditbot/connectors',
    '//src/main/java/pl/jpetryk/redditbot/parser',
    '//src/main/java/pl/jpetryk/redditbot/utils:response_comment',
    '//src/main/java/pl/jpetryk/redditbot/utils:utils_lib',
    '@log4j//jar',
    '@guava//jar',
    '@guice//jar',
  ]
)

java_library(
  name='abstract_reddit_bot',
  srcs=['main/java/pl/jpetryk/redditbot/bot/AbstractRedditBot.java'],
  deps=[
    '//src/main/java/pl/jpetryk/redditbot/model:models',
    '//src/main/java/pl/jpetryk/redditbot/exceptions:exceptions',
    '//src/main/java/pl/jpetryk/redditbot/connectors:connectors',
    '@guava//jar',
    '@log4j//jar'
  ]
)

java_library(
  name='tweets_in_comments_bot',
  srcs=['main/java/pl/jpetryk/redditbot/bot/impl/TweetsInCommentsBot.java'],
  deps=[
    ':abstract_reddit_bot',
    '//src/main/java/pl/jpetryk/redditbot/connectors:connectors',
    '//src/main/java/pl/jpetryk/redditbot/parser:parser',
    '//src/main/java/pl/jpetryk/redditbot/exceptions:exceptions',
    '//src/main/java/pl/jpetryk/redditbot/utils:response_comment',
    '//src/main/java/pl/jpetryk/redditbot/model:models',
    '@javax_javaee//jar',
    '@guava//jar',
  ]
)

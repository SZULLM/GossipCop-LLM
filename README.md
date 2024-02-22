# GossipCop-LLM

Download dataset from this link: [Google Drive](https://drive.google.com/drive/folders/1QfKCGYVZHwNQrsk3PihzZs_6bTacQ93M?usp=sharing)

# Introduction

This repository contains 4 datasets:

1. gossipcop_v3-1_style_based_fake.json
2. gossipcop_v3-2_content_based_fake.json
3. gossipcop_v3-3_integration_based_fake_tn200.json
4. gossipcop_v3-4_stoty_based_fake.json

1, 3, 4 use GLM-3 to generate fake news. 2 uses GLM-4 to generate fake news.

# 1_style_based_fake

prompt:

For human-generated fake news as inputs:

1. Rewrite the following news article in an objective and professional tone without changing the content and meaning while keeping a similar length. [fake news article]
2. Rewrite the following news article in a neutral tone without changing the content and meaning while keeping a similar length. [fake news article]

For human-generated legitimate news as inputs:

3. Rewrite the following news article in an emotionally triggering tone without changing the content and meaning while keeping a similar length. [legitimate news article]
4. Rewrite the following news article in a sensational tone without changing the content and meaning while keeping a similar length. [legitimate news article]![image](https://github.com/SZULLM/GossipCop-LLM/assets/52686008/1fa137d9-059f-4cf5-9b4a-abb1c609fde4)

example 1:

```json
{
    "origin_id": "gossipcop-887580",
    "origin_label": "real",
    "origin_text": "“UnREAL” is back with its first female suitor and no shortage of drama — including (sob!) a defaced man bun.\n\nThe Lifetime series returns with its third season premiere on Feb. 26, the channel announced Tuesday. The show also released the season’s first trailer, introducing viewers to new “Everlasting” lead Serena (Caitlin FitzGerald).\n\n“She’s smart — we can’t handle her the same way,” Rachel (Shiri Appleby) warns Quinn (Constance Zimmer) in the promo.\n\nThe series from co-creators Marti Noxon and Sarah Gertrude Shapiro returns after a lengthy hiatus with new showrunner Stacy Rukeyser taking over for Carol Barbee ahead of Season 3.\n\n“UnREAL” has already been renewed for an eight-episode fourth season to follow the upcoming 10-episode Season 3. Last season’s finale aired back in August 2016.\n\nCheck out the video above to see one contestant’s man bun tragically meet its demise.\n\n“UnREAL” is back with its Season 3 premiere Feb. 26 on Lifetime.",
    "generated_text": "\"UnREAL\" is back with a new twist: a female suitor! The controversial Lifetime drama series returns with its third season premiere on Feb. 26, introducing viewers to new lead Serena (Caitlin FitzGerald). But that's not all - the show promises to deliver plenty of drama, including (sob!) a defaced man bun.\n\nThe series, created by co-creators Marti Noxon and Sarah Gertrude Shapiro, returns after a lengthy hiatus with a new showrunner in charge. Season 3 promises to be even more explosive than the previous seasons, with a 10-episode run leading up to an eight-episode fourth season. Last season's finale aired back in August 2016, leaving fans eagerly anticipating the new season.\n\nBut what can we expect from Season 3? The promo hints that things are not going to be easy for the contestants, with Rachel (Shiri Appleby) warning Quinn (Constance Zimmer) that \"She's smart - we can't handle her the same way.\" Will the drama continue to escalate? Will Serena's presence shake things up? We'll have to wait until Feb. 26 to find out.\n\nIn the meantime, check out the video above to see one contestant's man bun tragically meet its demise. Will this be the start of a new trend for the show? Only time will tell. \"UnREAL\" is back - and it's only just getting started.",
    "generated_tone": "a sensational tone",
    "generated_label": "real",
    "origin_text_cn_gpt4": "电视剧“不真实”回归，在其剧中首次出现女主角，剧情可以说百转千回——包括（伤心！）一个辱骂小麦色男子的场面。\n\n生活时尚频道透露，第三季将于2月26日首播。该剧还发布了本季的第一个预告片，让观众熟悉新的“永恒”的女主塞雷娜（Caitlin FitzGerald）。\n\n“她很聪明——我们不能按常规对待她。”瑞秋（Shiri Appleby）在这个预告片中警告奎因（Constance Zimmer）。\n\n悬念丛生的剧集在长时间停播后，由创作者Marti Noxon和Sarah Gertrude Shapiro联手打造，新的制片人Stacy Rukeyser接手Carol Barbee ，并开始了第三季的制作。\n\n“不真实”已经续订了第四季，共8集，这是继即将播出的10集的第三季之后。上一季的大结局在2016年8月播出。\n\n观看上面的视频，看看一个参赛者的小麦色男子是怎样悲剧收场。\n\n“不真实”将于2月26日回归，继续在生活时尚频道播出第三季。",
    "generated_text_cn_gpt4": "带着新的翻版：“UnREAL”推出了一位女追求者！这部在Lifetime电视台播放的有争议的戏剧系列在2月26日起回归第三季，引领观众见识新女主角塞雷娜（Caitlin FitzGerald）。但这还不是全部 - 这个节目有各种让人看到就想哭的戏剧效果，包括一顶被破坏的男士发髻。\n\n该系列由联合创作人Marti Noxon和Sarah Gertrude Shapiro共同创作，在经过长时间的休停后，决定由新的制片人接力。第三季比往季更有冲击力，共有10集，接下来是第四季的八集。上季的季终集于2016年8月播出，让粉丝们期待新季的到来。\n\n但我们能对第三季有何期待？预告中剧情显得追求者不容易，瑞秋（Shiri Appleby）警告奎恩（Constance Zimmer）：“她很聪明 - 我们不能老一套对待她。\"剧情会继续升级吗？塞雷娜的出现会搅乱局面吗？我们必须等到2月26日才能知道。\n\n在此同时，上面的视频展示了一名选手的男士发髻不幸遭到摧毁。这将是该节目新趋势的开始吗？只有时间才能告诉我们。“UnREAL”回归了 - 而且这只是刚刚开始。"
}
```

example 2:

```json
{
    "origin_id": "gossipcop-6487101019",
    "origin_label": "fake",
    "origin_text": "It seems that Rihanna has decided to respond to the rumors that she is expecting a baby with boyfriend Hassan Jameel. In a typical Rihanna fashion, she laughed off the rumors.\n\nAccording to an insider, the singer is not expecting, and she is not even trying to enter motherhood at the moment.\n\nA person, who attended a big event with the couple, explained: “She is not pregnant lol. She was taking shots backstage last night and drinking at the afterparty.”\n\nAnother source spoke to Hollywood Life and added: “At this point, Rihanna feels like all she can do is laugh off all the pregnancy rumors, in addition to just ignoring them now. She is not pregnant, and she is not even trying to get pregnant either at this point.”\n\nRihanna on her way to 1OAK nightclub 🔥 A post shared by badgalriri (@badgalririr8) on Jan 29, 2018 at 4:15am PST\n\nHowever, there will be little Riri or Hassan in the future.\n\nThe insider shared: “Would she like children in the future? Yes, but definitely in the future, she is simply not ready to start a family… just yet. Rihanna loves children though, she is a natural mom, and she thinks Hassan will make an amazing father — he is really kind and patient, and a very loving person — but right now she is focused on her career first and foremost. Plus, Rihanna has not even met his family yet.”\n\nRiri 🔥💖😲 A post shared by badgalriri (@badgalririr8) on Jan 28, 2018 at 8:50pm PST\n\nAfter Rihanna performed at the Grammys, social media exploded because she appeared to have a baby bump.\n\nOne supporter said: “She makes me feel better for eating a whole bag of red vines. If RiRi thick, I’m thick too, darnnit. Is Rihanna Pregnant? Asking for a friend! She looks great thick.Waiting for her to announce that she is pregnant.”\n\nAnother commenter wrote: “So we just gonna ignore that fact that Riri looked a little thicker than usual in that skin tight dress she performed with DJ Khaled. She looks pregnantWhy does she keep holding her tummy??? Is she pregnant???”\n\nRihanna’s ex-boyfriend, Chris Brown, had an odd reaction to the rumors: “Chris always had high hopes for their future together, and even though there are only rumors that she could be pregnant with some other guy’s baby, he is still pretty upset and sad to hear about it. He feels like that should be his baby.”\n\nAdvertisement\n\nCommenters say that Brown should move on.",
    "generated_text": "Rihanna has laughed off rumors that she is pregnant with her boyfriend Hassan Jameel. An insider has stated that the singer is not expecting a baby at the moment and is not even trying to enter motherhood. Another source has confirmed that Rihanna is not pregnant and that she is simply ignoring the rumors.\n\nDespite the rumors, Rihanna does want children in the future but is not ready to start a family right now. She loves children and thinks Hassan will be an amazing father, but right now she is focused on her career first and foremost. Rihanna has not even met Hassan's family yet.\n\nAfter Rihanna's performance at the Grammys, social media was abuzz because she appeared to have a baby bump. Some supporters said that she looked great and that they were waiting for her to announce that she is pregnant. However, others speculated that she might be pregnant and wondered why she was holding her tummy.\n\nRihanna's ex-boyfriend Chris Brown had an odd reaction to the rumors. He had high hopes for their future together and was upset to hear that she might be pregnant with someone else's baby. However, Rihanna is not pregnant and Chris should move on.",
    "generated_tone": "a neutral tone",
    "generated_label": "fake",
    "origin_text_cn_glm-4": "似乎蕾哈娜已经决定回应她与男友哈桑·贾米尔的怀孕传闻。以典型的蕾哈娜风格，她对这些谣言一笑置之。\n\n据一位内部人士透露，这位歌手并没有怀孕，而且她此刻甚至没有打算进入母亲的角色。\n\n一位与这对情侣一起参加大型活动的人解释说：“她没怀孕，哈哈。她昨晚在后台喝shots，在派对上也喝酒。”\n\n另一位消息人士与《好莱坞生活》交谈并补充说：“在这一点上，蕾哈娜觉得她所能做的就是对所有的怀孕谣言一笑置之，除了现在忽略它们。她没有怀孕，而且现在她甚至没有打算怀孕。”\n\n然而，将来可能会有小蕾哈娜或哈桑。\n\n这位内部人士分享说：“她将来想要孩子吗？是的，但肯定是在将来，她现在还不足以开始一个家庭……只是还没到时候。蕾哈娜虽然喜欢孩子，她天生就是当妈妈的料，而且她认为哈桑会成为一个出色的父亲——他非常善良、耐心，并且是一个非常有爱心的人——但现在她首先要专注于自己的事业。而且，蕾哈娜甚至还没有见过他的家人。”\n\n在蕾哈娜在格莱美表演之后，社交媒体上爆发出议论，因为她似乎有了一个婴儿隆起。\n\n一位支持者说：“她让我觉得吃下一整袋红葡萄藤条也没关系。如果蕾哈娜丰满，我也丰满，该死的。蕾哈娜怀孕了吗？替朋友问的！她丰满的样子很棒。等待她宣布怀孕。”\n\n另一位评论者写道：“所以我们就是要忽略Riri在紧身裙子里看起来比平时更丰满的事实吗？她和DJ Khaled表演时看起来怀孕了。她为什么一直捂着肚子？？？她怀孕了吗？？？”\n\n蕾哈娜的前男友克里斯·布朗对这一传闻的反应很奇怪：“克里斯总是对他们未来的生活抱有很大希望，即使只是传闻她可能怀了别人的孩子，他听到这些还是很伤心和难过。他觉得那应该是他的孩子。”\n\n评论者说布朗应该向前看。",
    "generated_text_cn_glm-4": "蕾哈娜对于她与男友哈桑·贾米尔怀孕的传闻一笑置之。一位内部人士表示，这位歌手目前并没有怀孕，甚至没有尝试进入母亲的角色。另一位消息人士也确认蕾哈娜没有怀孕，她只是忽视了这些谣言。\n\n尽管有这些传闻，蕾哈娜确实想在将来拥有孩子，但现在还不准备开始家庭生活。她喜欢孩子，认为哈桑将来会是个出色的父亲，但现在她首先把事业放在首位。蕾哈娜甚至还没有见过哈桑的家人。\n\n在蕾哈娜在格莱美奖上的表演后，社交媒体上议论纷纷，因为她看起来似乎有了婴儿肥。一些支持者说她看起来很好，他们等着她宣布怀孕的消息。然而，也有人猜测她可能怀孕了，想知道她为什么抱着肚子。\n\n蕾哈娜的前男友克里斯·布朗对传闻的反应很奇怪。他对他们将来的关系抱有很大希望，听到她可能怀了别人的孩子感到很沮丧。然而，蕾哈娜并没有怀孕，克里斯应该向前看。"
}
```

# 2_content_based_fake



# 3_integration_based_fake

# 4_stoty_based_fake

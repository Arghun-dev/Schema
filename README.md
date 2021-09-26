# Schema

##1. CollectionPage (properties)

**about** => this is where you can say what is this collection about.

**hasPart** => this is the property that you're going to nest these things within your collectionPage. so now we're looking at the property we're going to use to actually connect these different items together. And the first one we're looking at is `hasPart` => it's really common and strong connection. Because usually collection pages are helpful when there's multiple types of `creativeWorks` and none is more important than another. It's also a strong connection because you're saying that we're creating markup for this creativeWork is part of the collection.

**mentions** => the other property that is useful for nesting items within your collection page is mentions and this is a really popular property to use because the value can be anything, in the schema.org vocabulary. 

**author** => the next property I'd like to highlight is author you can also use a creator you can also use publisher the point being though is that the author or those other properties I mentioned allow you to connect the organization  or the brand information of the publisher.

**significantLink** => usually there's lots of links on these types of pages to other parts of your website



So in summary collection page is wonderful schema class to use when your page has lots going on or many things that are all equally important or there's no real heirarchy but you want to call them all out in one big block of json-ld

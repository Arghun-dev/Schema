# Schema

##1. CollectionPage (properties)

**about** => this is where you can say what is this collection about.

**hasPart** => this is the property that you're going to nest these things within your collectionPage. so now we're looking at the property we're going to use to actually connect these different items together. And the first one we're looking at is `hasPart` => it's really common and strong connection. Because usually collection pages are helpful when there's multiple types of `creativeWorks` and none is more important than another. It's also a strong connection because you're saying that we're creating markup for this creativeWork is part of the collection.

**mentions** => the other property that is useful for nesting items within your collection page is mentions and this is a really popular property to use because the value can be anything, in the schema.org vocabulary. 

**author** => the next property I'd like to highlight is author you can also use a creator you can also use publisher the point being though is that the author or those other properties I mentioned allow you to connect the organization  or the brand information of the publisher.

**significantLink** => usually there's lots of links on these types of pages to other parts of your website



So in summary collection page is wonderful schema class to use when your page has lots going on or many things that are all equally important or there's no real heirarchy but you want to call them all out in one big block of json-ld


### Example

```js
{

    "@context": "http://schema.org",

    "@type": "CollectionPage",

    "mentions": {

        "@type": "SoftwareApplication",

        "operatingSystem": "All",

        "applicationCategory": "BusinessApplication",

        "review": {

            "@type": "Review",

            "reviewRating": {

                "@type": "Rating",

                "ratingValue": "4.9",

                "worstRating": 1,

                "bestRating": 5,

                "name": "Review Rating",

                "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Rating"

            },

            "author": {

                "@type": "Person",

                "name": "Steve",

                "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Person"

            },

            "name": "Review",

            "datePublished": "2018-06-14T11:58:00Z",

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Review"

        },

        "offers": {

            "@type": "Offer",

            "price": 30,

            "priceCurrency": "USD",

            "name": "Pricing",

            "eligibleRegion": "https://en.wikipedia.org/wiki/Earth",

            "availability": "InStock",

            "url": "https://www.schemaapp.com/training-overview-collectionpage/",

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Offer"

        },

        "name": "Schema App Editor",

        "aggregateRating": {

            "@type": "AggregateRating",

            "ratingValue": "4.9",

            "name": "Ratings",

            "worstRating": 1,

            "bestRating": 5,

            "ratingCount": 13,

            "reviewCount": 13,

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#AggregateRating"

        },

        "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Thing1"

    },

    "hasPart": [

        {

            "@type": "Article",

            "headline": "Schema Markup Training",

            "name": "Schema Markup Training",

            "image": {

                "@type": "ImageObject",

                "url": "https://www.schemaapp.com/wp-content/uploads/2019/09/ProcessCircle.png",

                "height": "3547",

                "width": "4038",

                "@id": "https://www.schemaapp.com/wp-content/uploads/2019/09/ProcessCircle.png"

            },

            "publisher": {

                "@type": "Organization",

                "name": "Schema App",

                "logo": {

                    "@type": "ImageObject",

                    "width": "300",

                    "height": "105",

                    "url": "https://www.schemaapp.com/wp-content/uploads/2016/04/SchemaApp_Logo-e1462565714376.png",

                    "@id": "https://www.schemaapp.com/wp-content/uploads/2016/04/SchemaApp_Logo-e1462565714376.png"

                },

                "contactPoint": "https://www.schemaapp.com/contact/",

                "description": "Schema App is an enterprise-grade solution that works for all websites, all content, without a developer. ",

                "@id": "https://www.schemaapp.com/"

            },

            "author": {

                "@id": "https://www.schemaapp.com/"

            },

            "datePublished": "2020-06-01T11:47:00Z",

            "description": "https://www.schemaapp.com/training-overview-collectionpage/#Article",

            "mainEntityOfPage": {

                "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Article"

            },

            "dateModified": "2020-06-01T11:48:00Z",

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Article"

        },

        {

            "@type": "FAQPage",

            "name": "Frequently Asked Questions",

            "mainEntity": [

                {

                    "@type": "Question",

                    "name": "Do you offer training?",

                    "acceptedAnswer": {

                        "@type": "Answer",

                        "text": "We provide onboarding for every customer to get them started in the tools. Additionally, there are hours of on-demand content at your disposal. The ‘Premium’ and ‘Enterprise” packages include high-touch support, but everyone is welcome to purchase high-touch support to learn more about the Schema App tools or to design a custom Schema Markup strategy.",

                        "name": "Answer",

                        "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Answer"

                    },

                    "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Question"

                },

                {

                    "@type": "Question",

                    "name": "What is High Touch Support?",

                    "acceptedAnswer": {

                        "@type": "Answer",

                        "text": "High Touch Support includes an assigned Customer Success Manager and can range from supporting your team to use our tools, to us providing a managed service. Our Customer Success Managers are experts in Schema Markup and the Schema App tools.",

                        "name": "Answer",

                        "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Answer1"

                    },

                    "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Question1"

                }

            ],

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#FAQPage"

        },

        {

            "@type": "VideoObject",

            "interactionStatistic": "595",

            "uploadDate": "2019-11-29",

            "duration": "P0Y0M0DT0H25M17S",

            "embedUrl": "https://www.youtube.com/embed/JWd7vU2xyC4",

            "contentUrl": "https://www.youtube.com/watch?v=JWd7vU2xyC4",

            "name": "Schema App Virtual Onboarding",

            "description": "Ready to get started with Schema App? Watch our Schema App Virtual On-boarding video to get the detailed tour and take a look at the Homepage, Structured Data Editor, Your Data Items, and setting up for Automatic Deployment.",

            "thumbnailUrl": "https://i.ytimg.com/vi/JWd7vU2xyC4/hqdefault.jpg",

            "@id": "https://www.schemaapp.com/training-overview-collectionpage/#VideoObject"

        }

    ],

    "about": {

        "@type": "Thing",

        "name": "Schema Markup Training",

        "@id": "https://www.schemaapp.com/training-overview-collectionpage/#Thing"

    },

    "author": {

        "@id": "https://www.schemaapp.com/"

    },

    "significantLink": [

        "https://www.schemaapp.com/training-overview/highlighter-create-page-set/",

        "https://www.schemaapp.com/training-overview/strategy/"

    ],

    "description": "To maximize its effectiveness, schema markup should be viewed as an ongoing strategic SEO initiative. There are 5 steps in the overall process: Strategy, Authoring, Deployment, Maintenance and Reporting &amp; Analytics.",

    "name": "Schema Markup Training",

    "@id": "https://www.schemaapp.com/training-overview-collectionpage/"

}
```

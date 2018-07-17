<img src="https://academy.spryker.com/resources/ui/images/logo.png" alt="Spryker" title="Spryker" align="right" height="100"/>

# Awesome Spryker
[Twitter][11] - [Facebook][12] - [Instagram][13] - [YouTube][17] - [LinkedIn][14] - [Xing][15]

> A curated list of awesome bookmarks, modules, tutorials, blog posts, videos and other cool resources from the [Spryker](https://github.com/spryker) ecosystem.

The creators and maintainers of this list do not receive and should not receive any form of payment to accept a change made by any contributor. The goal of this repository is to index resources and support the community, not to advertise for profit.

If you see a link here that is not (any longer) a good fit, you can fix it by submitting a pull request to improve this file. Thank you!

## Content 
- [What is Spryker?](#what-is-spryker)
- [Spryker Github Acounts](#github-accounts)
- [Where to start?](#where-to-start)
  - [Get in touch with Spryker](#get-in-touch)
  - [Command Line Interface](#command-line-interface)
  - [Development](#development)
    - [Code](#code)
    - [Tooling](#tooling)
    - [Setup](#setup-local-development-environment)
  - [DevOps](#devops)
    - [Local Development](#local-development)
    - [Docker / Container](#docker--container)
  - [Modules](#modules)
    - [API](#api)
    - [CDN](#cdn)
    - [CMS](#cms)
    - [Connectors](#connectors)
    - [E-Mails / Newsletter Tooling](#e-mails--newsletter-tooling)
    - [Basket / Checkout related features](#basket--checkout-related-features)
    - [Business Intelligence](#business-intelligence)
    - [Import / Export](#import--export)
    - [Marketing Tooling / Markups](#marketing-tooling--markups)
    - [Monitoring](#monitoring)
    - [Payment](#payment)
    - [Product Information Management (PIM)](#product-information-management-pim)
    - [Risk Management](#risk-management)
    - [Tracking](#tracking)
- [Useful Resources](#useful-resources)
- [Good Views and Reads](#good-videos-blogs-and-stories)
  - [Slides](#slides)
  - [Reddit](#reddit)
  - [Videos](#videos)
  - [Blogs](#blogs)
  - [Stories](#stories)
- [Communities and Meetups](#communities-and-meetups)
  - [Germany](#germany)

## What is Spryker
> Spryker is a Commerce Operating System that provides the end-to-end functionality needed to create a fully-functional commercial online presence for any entity in need of a modular, high-performing and scalable web presence. There is a [Spryker Feature List][31] available which gives a good first overview about what to expect.
> 
> -- [Understanding Spryker Commerce OS][1]

## Github Accounts
- [spryker][28] - Main account.
- [spryker-sdk][26] - Lib and Helpers for Developers.
- [spryker-eco][27] - Contains a lot of third party modules.
- [spryker-shop][30] - Representations of B2C and B2B E-Commerce Platforms.
- [spryker-feature][54] - Contains features.
- [spryker-projects][55] - For internal use only, I think.
- [spryker-showcase][56] - For internal use only, I think.
- [spryker-middleware][57] - Abstracted Middleware.

## Where to start
> A journey of a thousand miles must begin with a single step.
>
> -- LAO-TZU, Tao Te Ching

### Get in touch
- [Academy][22] - Open Academy, includes some Cookbooks and Tutorials.
- [Forum][2] - Forum based on Discuss.
- [Support Issue Tracker][3] - Open Ticket System based on Github.
- [FAQ][32] - Official Frequently Asked Questions Hub.

### Command Line Interface
- [Code Generator for Modules][7] - Creation of Boilerplate in a nutshell.
- [Set of helper scripts][43] - Helps in debugging of tests in VM by [@narsov][44].

### Development
#### Code
- [Hello World Module][6] - Understand how to add a simple new module.
- [Spryker Fixtures][25] - Helper for fixtures made by [@dantleech][29].

#### Tooling
- [PHP Storm Plugin][24] - Basic Plugin for PHP Storm especially for Sprykers special annotations.
- [Debugging with Xdebug][34] - Quite useful tutorial for xdebuf setup within sprykers pre-built VM.

#### Setup local development environment

**Setup**

1. cd into your ~/Workspace
2. git clone -b v2.1.0 git@github.com:spryker/devvm.git spryker-devvm-suite
3. VM_PROJECT=suite SPRYKER_REPOSITORY="git@github.com:spryker-shop/suite.git" SPRYKER_BRANCH="1.0" vagrant up
4. ./project on host machine contains suite files now, mounted to /data/shop/development/current in vagrant box
5. vagrant ssh
6. ulimit -n 65535
7. composer global require hirak/prestissimo
8. cd /data/shop/development/current
9. composer install
10. vendor/bin/install --exclude=demodata (remove exclude, to install demodata)

**Stack**

| Note | Url | Default Credentials | Note |
| --- | --- | --- | --- |
| YVES Frontend | http://www.de.suite.local | - | - |
| ZED Backend | http://zed.de.suite.local | admin@spryker.com // change123 | - |
| Rabbit MQ | http://zed.de.suite.local:15672 | admin / mate20mg | - |
| Mailcatcher | http://zed.de.suite.local:1080 | - | - |
| Redis | http://zed.de.suite.local:10009 | - | (NOGUI) You can explore Redis with e.g. Redis Desktop Manager |
| PostgreSQL | http://zed.de.suite.local:5432 | development / mate20mg | - |
| MySQL Server | http://zed.de.suite.local:3306 | development / mate20mg | - |
| Jenkins | http://www.de.suite.local:10007 | - | - |

### DevOps
#### Local Development
- [Reference vagrant repository for Spryker][20] - Start local development here.

### Docker / Container
- [Claranet Docker Image][16] - Comprehensive docker image made by [@claranet][21].
- [Deploy Docker][19] - Docker Stack pre-built by Spryker.
- [Fond of Docker Stack][41] - Docker Stack pre-built by [@fond-of][42].
- [Docker Shop Suite Stack][70] - Docker Shop Suite Stack pre-built by [@spryker][69].

### Modules
#### API
| Module Link | Short Description |
|---|---|
| [Stock API Module][60] | REST API for stock updates. |
| [Extend ProductApi Module][65] | ProductApi extends the Base Spryker Product Api Module. |
| [Zed API Auth Module][66] | Authorization Module. |

#### CDN
| Module Link | Short Description |
|---|---|
| [Cloudinary][52] | Cloudinary Integration. |

#### CMS
| Module Link | Short Description |
|---|---|
| [Contentful][42] | Contentful Integration. |
| [Contact Form][48] | A simple contact form for spryker. |

#### Connectors
| Module Link | Short Description |
|---|---|
| [elastic.io][45] | Spryker component für elastc.io platform. |

#### E-Mails / Newsletter Tooling
| Module Link | Short Description |
|---|---|
| [SMTP Mail][67] | Extends the default Spryker mail module with smtp functionality. |
| [Optivo][90] | Optivo Newsletter Integration. |
| [Inxmail][95] | Inxmail Integration. |

#### Basket / Checkout related features
| Module Link | Short Description |
|---|---|
| [Minimal Quantity][49] | Integration for minimal quantity. |
| [Availability Alert][64] | Availability alert. |

#### Business Intelligence
| Module Link | Short Description |
|---|---|
| [Minubo][79] | Minubo Business Intelligence (Commerce Intelligence) Implementation. |

#### Import / Export
| Module Link | Short Description |
|---|---|
| [Availability Feed][63] | Creates an Availability feed. |

#### Marketing Tooling / Markups
| Module Link | Short Description |
|---|---|
| [Google Search][59] | Google Search Integration. |
| [Active Campaign][61] | Active Campaign. |
| [Open Graph][62] | Open Graph Integration. |

#### Monitoring
| Module Link | Short Description |
|---|---|
| [Tideways][80] | Tideways Implementation. |
| [New Relic][81] | New Relice Implementation. |
| [Loggly][88] | Loggly Implementation. |

#### Payment
| Module Link | Short Description |
|---|---|
| [Zero Paynent][50] | Quite old, but good examle of how to implement zero payments. |
| [Prepayment][46] | Prepayment Integration including bank account stuff. |
| [Refund][51] | Refund Integration. |
| [Computop][72] | Computop PSP Integration. |
| [Computop API][73] | Computop API. |
| [Payone][74] | Payone PSP Integration. |
| [Amazon Pay][75] | Amazon Payment Integration. |
| [After Pay][78] | After Pay PSP Integration. |
| [Ratepay][85] | Ratepay Integration. |
| [Payolution][86] | Payolution Integration. |
| [Heidelpay][87] | Heidelpay PSP Integration. |
| [Braintree][89] | Braintree PSP Integration. |
| [Billpay][92] | Billpay Integration. |
| [Klarna][93] | Klarna Integration. |
| [Adyen API][96] | Adyen API Integration. |
| [Adyen][97] | Adyen Integration. |

#### Product Information Management (PIM)
| Module Link | Short Description |
|---|---|
| [Akeneo][74] | Basic Integration of Akeneo PIM. |
| [Akeneo Middleware Connector][76] | Middleware Connector of Akeneo PIM. |
| [Akeneo Export Connector Bundle][94] | Akeneo Product Exporter with localized attribute option labels |

#### Risk Management
| Module Link | Short Description |
|---|---|
| [Arvato Risk Management][91] | Arvato Risk Management Service Integration. |

#### Tracking
| Module Link | Short Description |
|---|---|
| [Econda][70] | Basic Integration of Econda Tracking. |
| [Google Tag Manager][47] | Google Tag Manager Integration. |
| [Fact Finder Web Components][82] | Fact Finder Web Components. |
| [Fact Finder SDK][83] | Spryker SDK Implementation of Fact Finder. |
| [Fact Finder][84] | Fact Finder Integration. |

## Useful Resources
- [SOLID][4] - You want to understand this. More useful stuff can be found [here][33].
- [Twelve Factor App][5] - You want to respect this.
- [Open Code][18] - Thats why we can evaluate, but not use.

## Good Videos, Blogs and Stories
### Slides
- [How to implement a truly modular ecommerce platform][38] - On the example of Spryker at code.talks commerce special 2017.
- [Spryker Hackathon Q1 2016][39] - 48 Slides Bird's eye view.
- [E-Commerce Frameworks are a real option][40] - Marcel Hild from About You explained advantages of Spryker at code.talks 2015.

### Reddit
- [Does anyone have experiences with spryker (commerce framework)?][58] - Interesting conversation between CTO Fabian and some devs, give some insights about ideas behind patterns used in spryker.  

### Videos
- [Spryker commerce framework in a nutshell][36] - Fabian explains Spryker at code.talks 2016 commerce special. 

### Blogs
- [Tech Blog on Medium][35] - Looks like its a deprecated blog, but still interesting content there.
- [Static Analysis][53] - Shopsys, Spryker & Sylius under Static Analysis.
- [Load Test from 2016][37] - Quite old but the only official announced load test so far.

### Stories
- [How to Smoothly Release Split Repositories][10] - Nice insights in git sub tree.
- [State Machine Cookbook][23] - They do it right, they know, how to handle states and transitions.

## Communities and Meetups
### Germany
- [Usergroup Munich][8] - User Group in Munich.
- [Usergroup Karlsruhe][9] - User Group in Karlsruhe.
- [Usergroup Cologne][68] - User Group in Cologne.



[1]:https://academy.spryker.com/understanding_spryker/understanding_spryker.html
[2]:https://discuss.spryker.com/
[3]:https://github.com/spryker/support
[4]:https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)
[5]:https://12factor.net/
[6]:https://academy.spryker.com/enablement/tutorials_and_howtos/introduction_tutorials/t_hello_world.html
[7]:https://academy.spryker.com/developing_with_spryker/resources_and_developer_tools/code_generator.html
[8]:https://www.meetup.com/de-DE/Spryker-User-Group-MUC
[9]:https://www.meetup.com/de-DE/Karlsruher-Spryker-UG
[10]:https://blog.spryker.com/how-to-smoothly-release-split-repositories
[11]:https://twitter.com/sprysys
[12]:https://www.facebook.com/Spryker/
[13]:https://www.instagram.com/spryker/
[14]:https://www.linkedin.com/company/spryker-systems-gmbh/
[15]:https://www.xing.com/companies/sprykersystemsgmbh
[16]:https://github.com/claranet/spryker-base
[17]:https://www.youtube.com/channel/UC6lVOEbqXxUh0W5FMTvlPDQ
[18]:https://blog.spryker.com/open-code
[19]:https://github.com/spryker-eco/deploy-docker
[20]:https://github.com/spryker/devvm
[21]:https://github.com/claranet
[22]:https://academy.spryker.com/
[23]:https://academy.spryker.com/developing_with_spryker/development_concepts/state_machine_cookbook/state_machine_cookbook.html
[24]:https://github.com/project-a/idea-php-spryker-plugin
[25]:https://github.com/dantleech/spryker-fixtures
[26]:https://github.com/spryker-sdk
[27]:https://github.com/spryker-eco
[28]:https://github.com/spryker
[29]:https://github.com/dantleech
[30]:https://github.com/spryker-shop
[31]:https://academy.spryker.com/understanding_spryker/feature_list.html
[32]:https://academy.spryker.com/understanding_spryker/faq.html
[33]:https://github.com/spryker/solid-devtalks
[34]:https://academy.spryker.com/getting_started/debugging/debugging_setup.html
[35]:https://tech.spryker.com/
[36]:https://www.youtube.com/watch?v=S1OF5zQF1Gw
[37]:https://tech.spryker.com/spryker-performance-load-test-6b91d03e9a02
[38]:https://www.slideshare.net/FabianWesner/how-to-implement-a-truly-modular-ecommerce-platform-on-the-example-of-spryker-at-codetalks-commerce-special-2017
[39]:https://www.slideshare.net/FabianWesner/spryker-hackathon-q1-2016
[40]:https://www.slideshare.net/AboutYouGmbH/marcel-hild-spryker-ecommerce-framework-als-alternative-zu-traditioneller-shopsoftware-codetalks-2015
[41]:https://github.com/fond-of/spryker-docker
[42]:https://github.com/fond-of/spryker-contentful
[43]:https://github.com/marsov/sprykerhelperscripts
[44]:https://github.com/marsov
[45]:https://github.com/elasticio/spryker-component
[46]:https://github.com/fond-of/spryker-prepayment
[47]:https://github.com/fond-of/spryker-google-tagmanager
[48]:https://github.com/fond-of/spryker-contact
[49]:https://github.com/fond-of/spryker-availability
[50]:https://github.com/project-a/spryker-zero-payment
[51]:https://github.com/project-a/spryker-refund
[52]:https://github.com/inviqa/cloudinary-spryker
[53]:https://www.tomasvotruba.cz/blog/2017/08/28/shopsys-spriker-and-sylius-under-static-analysis/
[54]:https://github.com/spryker-feature
[55]:https://github.com/spryker-projects
[56]:https://github.com/spryker-showcase
[57]:https://github.com/spryker-middleware
[58]:https://www.reddit.com/r/PHP/comments/53su62/does_anyone_have_experiences_with_spryker/
[59]:https://github.com/fond-of/spryker-google-search
[60]:https://github.com/fond-of/spryker-stock-api
[61]:https://github.com/fond-of/spryker-active-campaign
[62]:https://github.com/fond-of/spryker-open-graph
[63]:https://github.com/fond-of/spryker-feed
[64]:https://github.com/fond-of/spryker-availability-alert
[65]:https://github.com/fond-of/spryker-product-api
[66]:https://github.com/fond-of/spryker-api-auth
[67]:https://github.com/fond-of/spryker-smtp-mail
[68]:https://now.spryker.com/spryker-goes-usergroup
[69]:https://github.com/spryker
[70]:https://github.com/spryker/docker-shop-suite
[71]:https://github.com/spryker-eco/econda
[72]:https://github.com/spryker-eco/computop
[73]:https://github.com/spryker-eco/computop-api
[74]:https://github.com/spryker-eco/akeneo-pim
[75]:https://github.com/spryker-eco/payone
[76]:https://github.com/spryker-eco/akeneo-pim-middleware-connector
[77]:https://github.com/spryker-eco/amazon-pay
[78]:https://github.com/spryker-eco/after-pay
[79]:https://github.com/spryker-eco/minubo
[80]:https://github.com/spryker-eco/tideways
[81]:https://github.com/spryker-eco/new-relic
[82]:https://github.com/spryker-eco/fact-finder-web-components
[83]:https://github.com/spryker-eco/fact-finder-sdk
[84]:https://github.com/spryker-eco/fact-finder
[85]:https://github.com/spryker-eco/ratepay
[86]:https://github.com/spryker-eco/payolution
[87]:https://github.com/spryker-eco/heidelpay
[88]:https://github.com/spryker-eco/loggly
[89]:https://github.com/spryker-eco/braintree
[90]:https://github.com/spryker-eco/optivo
[91]:https://github.com/spryker-eco/arvato-rss
[92]:https://github.com/spryker-eco/billpay
[93]:https://github.com/spryker-eco/klarna
[94]:https://github.com/fond-of/akeneo-export-connector-bundle
[95]:https://github.com/spryker-eco/inxmail
[96]:https://github.com/spryker-eco/adyen-api
[97]:https://github.com/spryker-eco/adyen

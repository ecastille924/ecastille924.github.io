---
layout: post
title:      "Ridin' the Rails "
date:       2021-03-01 03:07:28 +0000
permalink:  ridin_the_rails
---


I just finished building my first full project in Rails, and I feel pretty accomplished. It's a strange duality of pride and tempered anxiety. Much like the Sinatra project I was tasked to build a few weeks ago, I went into this feeling pretty nervous, and have come out feeling more powerful than ever-- but as they say, "with great power comes great responsibility." This is true not just of people, but of programming frameworks. 

For this build, I decided to structure it like a guitar repair shop. The basic idea being that a user has a guitar that needs fixing, so they can log onto the app, fill out a form describing their guitar and what's wrong with it, and then submit it to be repaired by the technician of their choice. This build was challenging in a number of ways, but there was also quite a bit of crossover from the previous build using Sinatra. There were 3 concepts that stuck with me after this build. One was new, one was not new, but was rusty in my brain, and one was not new at all, just fun to employ because of the confidence associated with performing an action you know how to do. Those concepts were Signing a user in with OAuth, setting up associations, and writing validations. 


# OAuth
A new idea to me for this build was setting up OAUth for login with google or other services. It wasn't particularly challenging because of available resources, but it was very satisfying to show off to my wife that she could log onto my newly created app with her Google account. It was like a cheat code to feeling like a really advanced developer!

# Associations 

One of the more challenging concepts for me as been associations, so it was very satisfying for me to think about and nail down the associations between my classes. Before this build, I really struggled to understand what it meant for a class to have a 'has_may_through' relationship to another class. This project fully opened my eyes to the idea of a join table and linking database tables to one another via IDs. I definitely feel stronger in my understanding of how classes can relate to one another and what sort of functionality that can give you. 

Ultimately, I decided that my 3 classes would be User / RepairBill / Technician:
```
class User < ApplicationRecord
    has_secure_password
    has_many :repair_bills 
    has_many :technicians, through: :repair_bills
```

```
class RepairBill < ApplicationRecord
    belongs_to :technician
    belongs_to :user
```

```
class Technician < ApplicationRecord
    has_many :repair_bills
    has_many :users, through: :repair_bills
```

Since my Repair Bills class contains belongs_to relationships to two other classes, that means that it becomes the "join" table, or the table that connects to otherwise unrelated classes. I was able to create a form for users to submit a bill of repair that would be associated with their own account, and associated with a technician of their choosing, which was very satisfying to implement. Obviously, we'd covered this concept in the Flatiron School curriculum up to this point, but sometimes it's hard to see the forest for the trees until you actually have time to step back and marvel at the beauty of such a "simple" concept. 

# Validations 

An element of the build that was particularly fun was writing validations for my forms. This was an area that I felt already equipped to tackle because it was a part of the Sinatra build, so it was a chance for me to flex my budding little coding muscles without having to scour the Rails Docs. 

I put more time and effort into this build than anything I've ever done with coding. I struggled mightily, but I overcame my struggles in an even bigger way, and it's safe to say that I have a lot of work to do yet, but I'm on my way to being a fully competent web developer.



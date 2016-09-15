I worked on a project once where the architect used vip's and software load balancers like the were going out of fashion.

I total I recall counting 14 load balancers going to 14 servers !??!

Every VIP balanced between two haproxy software load balancers which balanced between two app servers. This pattern was used mutliple times throughout the design to access various services within the whole application.

Needless to say when I queried it I was shot down as just the devops guy.



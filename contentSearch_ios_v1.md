````
- (IBAction)fetchContent:(id)sender {
    QLQueryForAnyAttributes *queryForAnyAttributes =
    [[QLQueryForAnyAttributes alloc] init];
    [queryForAnyAttributes whereKey:@"color" containsStringValue:@"blue"];
    [self.contentConnector contentsWithQuery:queryForAnyAttributes success:^(NSArray *contents) {
        for(id notification in contents) {
            NSLog(@" Notification Title: %@",[notification title]);
        }
    }
                                     failure:^(NSError *error) {
                                         NSLog(@"it failed!");
                                     }];
}
```

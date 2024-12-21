```python
class SocialMediaAccount():
    def __init__(self, username, password):
        self.username = username
        self.password = password

    def login(self):
        pass

    def post(self):
        pass

class InstagramAccount(SocialMediaAccount):
    def __init__(self, username, password, followers):
        super().__init__(username, password)
        self.followers = followers

    def share_story(self):
        pass

class FaceBookAccount(SocialMediaAccount):
    def __init__(self, username, password, likes):
        super().__init__(username, password)
        self.likes = likes

    def likes(self):
        pass

acc1 = InstagramAccount("akotohsijuswa", "AngelaMainSaCorelangPapatong06", 500)
acc2 = FaceBookAccount("Josua Bersamina", "HapiNaBertdeyMoPa2005", 3215)
```python

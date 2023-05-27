from pyrogram import Client
import time

import sys
import os
from pyrogram.errors import RPCError

print("""
Subscribe to my Youtube Channel for more free telegram script: Solved4You
""")

orginally = 1  

api_id = "20513142"
api_hash = "67c53d17a970414159a18d585ed311cd"

apps = Client("Sessions/",int(api_id),str(api_hash),phone_number="+989186285938")

apps.start()

class GroupToGroup_AddMember():
    def __init__(self):
        return None

    def Get_group_chat_id(self, Link1, Link2):
            global a,b
            self.Group_ChatID = apps.get_chat(Link1)
            a = self.Group_ChatID.id
            self.Group_ChatID = apps.get_chat(Link2)
            b = self.Group_ChatID.id

    def Add_To_Group(self, Source, Destination):
        members = apps.get_chat_members(Source)
        counter = 1
        ccc = "DONE"
        for index, member in enumerate(members):
            app = apps
            try:
                user_id = member.user.username
                app.add_chat_members(Destination, user_id)

            except Exception as ex:
                print("Adding " + str(counter) + " " + str(user_id) + "\t" + str(ex.__class__.__name__))
                counter = counter + 1
                time.sleep(2)
                status = ex.__class__.__name__
                if status == "UserBannedInChannel":
                    continue

                else:
                    pass
            else:
                print("Adding "+str(counter)+" "+str(user_id)+"\t"+str(ccc))
                counter = counter+1
                time.sleep(3)

if int(orginally) == 1:
    one = input("Source group: ")
    two = input("Destination group: ")

    if "@" in str(one):
        onee = one.replace("@","")
    else:
        onee = one
    if "@" in str(two):
        twoo = two.replace("@","")
    else:
        twoo = two
    try:

        apps.join_chat(str(onee))
        apps.join_chat(str(twoo))
    except:
        pass

    App_Start = GroupToGroup_AddMember()
    ab = App_Start.Get_group_chat_id(one, two)
    App_Start.Add_To_Group(a, b)

else:
    apps.stop()
    sys.exit()

print("""
Subscribe to my Youtube Channel for more free telegram script: Solved4You
""")

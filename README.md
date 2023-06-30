//PS
if (context.params.event.data.options[0].value === 'PS') {
  // Role update and message creation for PS clan

  // Check if user already has the role
  const userRoles = await lib.discord.guilds['@0.2.4'].members.roles.list({
    user_id: `${context.params.event.member.user.id}`,
    guild_id: `549028189863804928`
  });

  if (userRoles.includes(`572571875646111745`)) {
    // Role already assigned message in the channel
    await lib.discord.channels['@0.3.4'].messages.create({
      channel_id: context.params.event.channel_id,
      content: 'Roles already assigned!'
    });
  } else {
    // Assign roles
    await lib.discord.guilds['@0.2.4'].members.roles.update({
      role_id: `572571875646111745`,
      user_id: `${context.params.event.member.user.id}`,
      guild_id: `549028189863804928`
    });

    // Check if roles were applied successfully
    const updatedUserRoles = await lib.discord.guilds['@0.2.4'].members.roles.list({
      user_id: `${context.params.event.member.user.id}`,
      guild_id: `549028189863804928`
    });

    if (updatedUserRoles.includes(`572571875646111745`)) {
      // Success message in the channel
      await lib.discord.channels['@0.3.4'].messages.create({
        channel_id: context.params.event.channel_id,
        content: 'Roles assigned successfully!'
      });
    } else {
      // Failed message in the channel
      await lib.discord.channels['@0.3.4'].messages.create({
        channel_id: context.params.event.channel_id,
        content: 'Failed to assign roles!'
      });
    }
  }
}
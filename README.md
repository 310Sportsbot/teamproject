# teamproject
package Main;

import net.dv8tion.jda.api.events.message.guild.GuildMessageReceivedEvent;
import net.dv8tion.jda.api.hooks.ListenerAdapter;

public class Commands extends ListenerAdapter{
	@Override
	public void onGuildMessageReceived(GuildMessageReceivedEvent event) {
	String[] args = event.getMessage().getContentRaw().split(" ");	

	if (args[0].toLowerCase().contains("hello")) {
		event.getChannel().sendMessage("Hey there! I'm your Sports Coach! I'm going to help you to be more active and choose a sport! For starters"
				+ " I need to know some things about you... how tall are you?").queue();
	}
	
	else if (args[0].toLowerCase().contains("short")) {
		String height = args[0];
		event.getChannel().sendMessage("Awesome! And are you skinny, regular or fat? (sorry for being so straight forward...remember that I'm a computer"
				+ " without feelings.").queue();
		}
	else if (args[0].toLowerCase().indexOf("average")==0) {
		String height = args[0];
		event.getChannel().sendMessage("Nice! And are you skinny, average or fat? (sorry for being so straight forward...remember that I'm a computer without feelings)").queue();
		}
	else if (args[0].toLowerCase().indexOf("tall")==0) {
		String height = args[0];
		event.getChannel().sendMessage("I'm impressed! Nice! And are you skinny, average or fat? (sorry for being so straight forward...remember that I'm a computer without feelings) ").queue();
		}
	else if (args[0].toLowerCase().indexOf("skinny")==0) {
		String weight = args[0];
		event.getChannel().sendMessage("Cool! I have some ideas then!").queue();
		}
	else if (args[0].toLowerCase().indexOf("regular")==0) {
		String weight = args[0];
		event.getChannel().sendMessage("Amazing! let's see what you could do!").queue();
		}
	else if (args[0].toLowerCase().indexOf("fat")==0) {
		String weight = args[0];
		event.getChannel().sendMessage("Perfect! There are plenty of sports that you could do!").queue();
		}
	}
}

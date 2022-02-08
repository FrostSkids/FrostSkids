public class Frost extends Human implements Gamer, Developer {

	@Override
	public String getName() {
		return "Rera";
	}
	
	@Override
	public List<String> getAliases() {
		return Arrays.asList("Pace", "My Name");
	}

        public Frost() {
        super("frost", "Mars");

        this.addLanguage("Java", "Python", "Javascript", "Kotlin");
        this.addExperience("3 Years+(java)", "2years+(python)", "6months+(kotlin)", "1 year (js)", "Total 5 years+");
     }
   }

	@Override
	public String aboutme() {
		return "I like to play piano" +
		"\n" + "I like to code Java";
	}
    
	@Override
	public void codingStuff() {
		String[] learning = ["Java", "Kotlin", "ReactJS"];
		String tryingTo = "Make good Android applications & websites";
	}
	
} 


public abstract class Human {

  @Getter private final String username;
  @Getter private final String country;

  private Set<String> languages = new HashSet<>();
  private Set<String> experiences = new HashSet<>();

  public Human(String username, String placeilive) {
      this.name = username;
      this.country = placeilive;
  }

  public void addLanguage(String... language) {
      this.languages.addAll(language);
  }
  
  public void addExperience(String... experience) {
      this.experiences.addAll(experience);
  }
}

Name:Maryna Subach
Contact me: marinasuboch@gmail.com
Summary: I'm a software developer with 5+ years of experiance in .Net. I'd like to learn more about java script.
Skills:
Languages & Technologies: C#, .Net Framework 2.0-4.8, ASP.Net, VBScript, .NetCore 3.1, WinForms, WPF, MS Visual Studio 2008-2019
Databases: MySQL, MS SQL, PostgreSQL
ORM: Ado.Net, Entity Framework
Version Control Systems: GIT, SVN
Automation tools: ReSharper, NUnit, StyleCop
Platforms: Windows 7, Windows 10, Linux
Example:
private readonly IBasketRepository _repository;
private readonly IMapper _mapper;
private readonly EventBusRabbitMqProducer _eventBus;

public BasketController(IBasketRepository repository, IMapper mapper, EventBusRabbitMqProducer eventBus)
  {
    _repository = repository;
    _mapper = mapper;
    _eventBus = eventBus;
  }

[HttpGet]
[ProducesResponseType(typeof(BasketCart), (int)HttpStatusCode.OK)]
public async Task<ActionResult<BasketCart>> GetBasket(string userName)
  {
    var basket = await _repository.GetBasket(userName);
    return Ok(basket);
  }

[HttpPost]
[ProducesResponseType(typeof(void), (int)HttpStatusCode.OK)]
public async Task<ActionResult<BasketCart>> UpdateBasket([FromBody] BasketCart basket)
  {
    return Ok(await _repository.UpdateBasket(basket));
  }
  
Work experience: 
09/2018-01/2021 iTechArt, Software Developer, Belarus, Minsk. Several projects: AIBolit, ConnectRad, SMS
07/2015-09/2018 Peleng, Software Developer, Belarus, Minsk. Several internal projects: Translator, Virtual File System, Data processing

Education and courses:
Software developer, Faculty of Engineering, A.A., *Baranovichi State University*
ASP.Net Developer, 2019, *Educational Center of High-Tech Park Belarus*
Microservices Architecture and Implamentation on .Net5, 2021, Udemy
Unit Testing for C# Developers, 2021, Udemy
Languages:
English - B1
Polish - A1

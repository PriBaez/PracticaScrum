# Documentación para consumir una API con .net

### A continuación, un ejemplo de cómo consumir una API con C# y .net

using System.Net.Http.Headers;
var client = new HttpClient();
var request = new HttpRequestMessage
{
	Method = HttpMethod.Get,
	RequestUri = new Uri("https://odds.p.rapidapi.com/v4/sports?all=true"),
	Headers =
	{
		{ "X-RapidAPI-Key", "d2828bf530msh5fb160f4428dac8p16b685jsn5a52b93102a8" },
		{ "X-RapidAPI-Host", "odds.p.rapidapi.com" },
	},
};
using (var response = await client.SendAsync(request))
{
	response.EnsureSuccessStatusCode();
	var body = await response.Content.ReadAsStringAsync();
	Console.WriteLine(body);
}


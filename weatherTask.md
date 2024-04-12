# Weather

![Weather!](/images/task.png "weather")

Անհրաժեշտ է ստանալ և ներկայացնել առաջիկա 7 օրերի եղանակը: (կարող եք ընտրել ցանկացած այլ դիզայն)։ Կոդը պետք է գրված լինի TypeScript-ով, բոլոր տվյալները և ֆունկցիաները անհրաժեշտ է տիպավորել` չօգտագործելով any type։

Եղանակի մասին ինֆորմացիան կարող եք ստանալ հետևյալ կայքից [Weather API](https://www.weatherapi.com/)

Կայքից օգտվելու անհրաժեշտ քայլերն են

- գրանցվեք կայքում և ակտիվացրեք ձեր էջև մեյլի միջոցով
- գեներացրեք ձեր կեյը Regenerate API Key
  
 ![Key!](/images/api-key.png "Key")
- տվյալները ստանալու համար հարցում եք կատարում հետևյալ հղումով http://api.weatherapi.com/v1/forecast.json?key=<YOUR_API_KEY>&q=Armenia&days=7

Տվյալները ստանալուց հետո անհրաժեշտ է դրանք տիպավորել։ Օրինակ

```ts
interface WeatherResponse {
  location: {
    name: string;
    region: string;
    country: string;
  };
  current: {
    temp_c: number;
    condition: {
      text: string;
      icon: string;
    };
  };
}
```

Ինչպես նաև պետք է ավելացնել փնտրման պատուհան, որտեղ մուտքագրված երկրի հիման վրա կստանաք այդ երկրի եղանակի ինֆորմացիան:

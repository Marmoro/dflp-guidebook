**Full-Stack Developer Path | Virtual Lab Activity | Week 7 | How To Expose And Consume Apis To Our Front-End Application | Apr 2021**

# Digital Future Leaders Program

We are almost there to reach the important goal that a full stack developer must achieve, which is to build, expose and consume API. We have built API last week, we have build a front-end. All that remains now it so expose and consume.

Back-end exercise files here: https://github.com/Marmoro/crmforpeople-app/tree/complete-2

Tip: Clone the repository ($ git clone ...), install npm packages ($ npm i), start docker-compose with ($ docker-compose up -d), and run the application ($ npm run start), or check package.json

Front-end files here: https://github.com/Marmoro/crmforpeople-web/tree/no-api
Tip: Clone the repository ($ git clone ...), install npm packages ($ npm i), and start angular development server ($ ng serve)

Last week, we reviewed that all of our API are working properly, still we didn't do any Unit Testing at this stage, but we confirmed at least they are functional. First we will start working on the front-end to find out how we can consume those APIs.

#### [Front-end] Creating services based on Angular official documentation

For HTTP communications, we have to create a service. This is a sample of what a service looks like in Angular. Services can be used by injecting them into the components that depends on data returned by these services. We try to follow what is explained in the resources.

Get data from a server: https://angular.io/tutorial/toh-pt6
Communicating with backend services using HTTP: https://angular.io/guide/http

```typescript
@Injectable({
  providedIn: 'root'
})
export class MyService {
  private url = `${Globals.API_URL}/endpoint`;
  constructor(private http: HttpClient) { }

  public get(): Observable<SomeType[]> {
    return this.http
      .get<SomeType[]>(this.url)
      .pipe(map(data => data), catchError((err: HttpErrorResponse) => {
        return throwError(err);
      }));
  }

  public post(): Observable<SomeType[]> {
    return this.http
      .post<SomeType[]>(this.url)
      .pipe(map(data => data), catchError((err: HttpErrorResponse) => {
        return throwError(err);
      }));
  }
}
```


#### Testing and CORS

Once our services are properly configured, we can begin testing consuming API from our Angular application. Simply we need to keep the back-end application running and then we run the Angular application and find out what will happen.

If we go to main.ts in crmforpeople-app (back-end) and comment (adding //) this line:

```typescript
app.enableCors({ credentials: true, origin: true });
```

Most likely we won't be able to consume the API from Angular due to CORS (Cross-Origin Resource Sharing). More info from the resource below. So better we keep it as it is.

Resource: https://docs.nestjs.com/security/cors

#### Error Handling

What if there was some error? How to handle errors? What should the user see? Let's say the user clicks on Inquiry, but the application failed to get list of organizations, do we give the user a chance to refresh the page? Do we show a static list of organizations? This is what error handling is all about. Not only this, but we have to do it on the front-end and on the back-end. Our focus here is to do it on the front-end, since a call to an API might either return expected results or an error.

#### The Checklist

To ensure we have reached our goal, we have to complete this checklist:

- ✅ Create organization service (should have all exposed functions from organization.controller.ts)
- ✅ Create case service (should have all exposed functions from case.controller.ts)
- ✅ Create user service (should have all exposed functions from user.controller.ts)

- ✅ Modify existing components to make use of these services
  - create-inquiry
    - uses organization service to list organizations
    - uses case service to create cases
- ✅ Create new component
  - name: case-listing
  - uses: case service
    - get case listing by user id
- ✅ Create new component
  - name: case-detail
  - uses: case service
    - get case details by case id
- ✅ Modify case routing to include these new components
- ✅ Modify navigation component to show these new components so users can navigate to them
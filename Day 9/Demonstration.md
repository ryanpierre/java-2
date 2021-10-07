# Demo Time

- Today we'll be focused on using the DI container to do our dirty work
- Then, we'll implement another story fully TDD now that we understand the jitsu


## Process

- I know that I'm going to need to mock a date. Rather than mock a date everywhere I need one, I'm going to use the spring DI container + @TestConfiguration to make that mocked date available in any test (including feature tests ! which we will want...)
- We need to remember that Tweet is just an entity model. We should just dump some data in there and it should deal with the rest. It shouldn't rely on anything else. Everything else has the job to create the Tweet the Tweet shouldn't hold business logic.
- In fact, under this disticintion, only the Service should be doing any thinking. The Model just stores info. So it should simply just be a suite of constructors and we don't need to mock the date because it's not relevant.
- I created a Service Interface (IClockService) as as well as the ClockService. For both my app and my tests, I made a config file that I could load with @Import in the main SpringBootApplication or SpringBootTest classes as needed
- In the end, what we need to do is add this test configuration to our test
  ```java
    @TestConfiguration
    public static class TestTwitterApplicationConfig
    {
        @Bean
        public IClockService clockService()
        {
            return new MockedClockService();
        }

        private class MockedClockService implements IClockService {
            private Clock clock;

            public MockedClockService() {
                String instantExpected = "2021-01-01T01:00:00Z";
                ZoneId zoneId = ZoneId.systemDefault();
                clock = Clock.fixed(Instant.parse(instantExpected), zoneId);
            }

            public Clock getClock() {
                return this.clock;
            }
        }
    }
  ```
- The name of the bean MATTERS. If I were to put clockServiceFoo(), it wouldn't inject. It looks for something with the same name (clockService)
- Basically that + adding the bean override thing is the secret to making this work

So I think the thinking is this:
- Entities don't have any external dependencies since their only job is to MODEL WHATS IN THE DATABASE. They are a persistence later and shouldn't have any logic to even create a date 
- We use service layers to do all the validation and logic of model creation and retrieval
- The repository is what specifically connects to our database
> ## Documentation Index
>
> Fetch the complete documentation index at: [/docs/llms.txt](https://resend.com/docs/llms.txt)
>
> Use this file to discover all available pages before exploring further.

[Skip to main content](https://resend.com/docs/api-reference/broadcasts/create-broadcast#content-area)

Node.js

PHP

Python

Ruby

Go

Rust

Java

.NET

cURL

CLI

```
import { Resend } from 'resend';

const resend = new Resend('re_xxxxxxxxx');

// Create a draft broadcast
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
});

// Create and send immediately
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
  send: true,
});

// Create and schedule
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
  send: true,
  scheduledAt: 'in 1 hour',
});
```

```
$resend = Resend::client('re_xxxxxxxxx');

// Create a draft broadcast
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
]);

// Create and send immediately
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
  'send' => true,\
]);

// Create and schedule
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
  'send' => true,\
  'scheduled_at' => 'in 1 hour',\
]);
```

```
import resend

resend.api_key = "re_xxxxxxxxx"

// Create a draft broadcast
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
}
resend.Broadcasts.create(params)

// Create and send immediately
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
resend.Broadcasts.create(params)

// Create and schedule
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
resend.Broadcasts.create(params)
```

```
require "resend"

Resend.api_key = "re_xxxxxxxxx"

// Create a draft broadcast
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
}
Resend::Broadcasts.create(params)

// Create and send immediately
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
Resend::Broadcasts.create(params)

// Create and schedule
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
Resend::Broadcasts.create(params)
```

```
package main

import "github.com/resend/resend-go/v3"

// Create a draft broadcast
params := &resend.CreateBroadcastRequest{
  SegmentId: "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  From:       "Acme <onboarding@resend.dev>",
  Html:       "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  Subject:    "Hello, world!",
}
broadcast, _ := client.Broadcasts.Create(params)

// Create and send immediately
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
broadcast, _ := client.Broadcasts.Create(params)

// Create and schedule
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
broadcast, _ := client.Broadcasts.Create(params)
```

```
use resend_rs::{types::CreateBroadcastOptions, Resend, Result};

#[tokio::main]
async fn main() -> Result<()> {
  let resend = Resend::new("re_xxxxxxxxx");

  let segment_id = "78261eea-8f8b-4381-83c6-79fa7120f1cf";
  let from = "Acme <onboarding@resend.dev>";
  let subject = "hello world";
  let html = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}";

  let opts = CreateBroadcastOptions::new(segment_id, from, subject).with_html(html);

  // Create a draft broadcast
  let _broadcast = resend.broadcasts.create(opts.clone()).await?;

  // Create and send immediately
  let _broadcast = resend
    .broadcasts
    .create(opts.clone().with_send(true))
    .await?;

  // Create and schedule
  let _broadcast = resend
    .broadcasts
    .create(opts.with_send(true).with_scheduled_at("in 1 hour"))
    .await?;

  Ok(())
}
```

```
Resend resend = new Resend("re_xxxxxxxxx");

// Create a draft broadcast
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);

// Create and send immediately
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .send(true)
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);

// Create and schedule
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .send(true)
    .scheduledAt("in 1 hour")
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);
```

```
using Resend;

IResend resend = ResendClient.Create( "re_xxxxxxxxx" ); // Or from DI

// Create a draft broadcast
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );

// Create and send immediately
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
        Send = true,
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );

// Create and schedule
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
        Send = true,
        ScheduledAt = DateTime.UtcNow.AddHours( 1 ),
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );
```

```
# Create a draft broadcast
curl -X POST 'https://api.resend.com/broadcasts' \
     -H 'Authorization: Bearer re_xxxxxxxxx' \
     -H 'Content-Type: application/json' \
     -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}"
}'

# Create and send immediately
curl -X POST 'https://api.resend.com/broadcasts' \
 -H 'Authorization: Bearer re_xxxxxxxxx' \
 -H 'Content-Type: application/json' \
 -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true
}'

# Create and schedule
curl -X POST 'https://api.resend.com/broadcasts' \
 -H 'Authorization: Bearer re_xxxxxxxxx' \
 -H 'Content-Type: application/json' \
 -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour"
}'
```

```
# Create a draft broadcast
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}"

# Create and send immediately
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}" \
  --send

# Create and schedule
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}" \
  --send \
  --scheduled-at "in 1 hour"
```

Response

```
{
  "id": "49a3999c-0ce1-4ea6-ab68-afcd6dc2e794"
}
```

POST

/

broadcasts

Node.js

PHP

Python

Ruby

Go

Rust

Java

.NET

cURL

CLI

```
import { Resend } from 'resend';

const resend = new Resend('re_xxxxxxxxx');

// Create a draft broadcast
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
});

// Create and send immediately
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
  send: true,
});

// Create and schedule
const { data, error } = await resend.broadcasts.create({
  segmentId: '78261eea-8f8b-4381-83c6-79fa7120f1cf',
  from: 'Acme <onboarding@resend.dev>',
  subject: 'hello world',
  html: 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',
  send: true,
  scheduledAt: 'in 1 hour',
});
```

```
$resend = Resend::client('re_xxxxxxxxx');

// Create a draft broadcast
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
]);

// Create and send immediately
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
  'send' => true,\
]);

// Create and schedule
$resend->broadcasts->create([\
  'segment_id' => '78261eea-8f8b-4381-83c6-79fa7120f1cf',\
  'from' => 'Acme <onboarding@resend.dev>',\
  'subject' => 'hello world',\
  'html' => 'Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}',\
  'send' => true,\
  'scheduled_at' => 'in 1 hour',\
]);
```

```
import resend

resend.api_key = "re_xxxxxxxxx"

// Create a draft broadcast
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
}
resend.Broadcasts.create(params)

// Create and send immediately
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
resend.Broadcasts.create(params)

// Create and schedule
params: resend.Broadcasts.CreateParams = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
resend.Broadcasts.create(params)
```

```
require "resend"

Resend.api_key = "re_xxxxxxxxx"

// Create a draft broadcast
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
}
Resend::Broadcasts.create(params)

// Create and send immediately
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
Resend::Broadcasts.create(params)

// Create and schedule
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
Resend::Broadcasts.create(params)
```

```
package main

import "github.com/resend/resend-go/v3"

// Create a draft broadcast
params := &resend.CreateBroadcastRequest{
  SegmentId: "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  From:       "Acme <onboarding@resend.dev>",
  Html:       "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  Subject:    "Hello, world!",
}
broadcast, _ := client.Broadcasts.Create(params)

// Create and send immediately
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
}
broadcast, _ := client.Broadcasts.Create(params)

// Create and schedule
params = {
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "Hello, world!",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour",
}
broadcast, _ := client.Broadcasts.Create(params)
```

```
use resend_rs::{types::CreateBroadcastOptions, Resend, Result};

#[tokio::main]
async fn main() -> Result<()> {
  let resend = Resend::new("re_xxxxxxxxx");

  let segment_id = "78261eea-8f8b-4381-83c6-79fa7120f1cf";
  let from = "Acme <onboarding@resend.dev>";
  let subject = "hello world";
  let html = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}";

  let opts = CreateBroadcastOptions::new(segment_id, from, subject).with_html(html);

  // Create a draft broadcast
  let _broadcast = resend.broadcasts.create(opts.clone()).await?;

  // Create and send immediately
  let _broadcast = resend
    .broadcasts
    .create(opts.clone().with_send(true))
    .await?;

  // Create and schedule
  let _broadcast = resend
    .broadcasts
    .create(opts.with_send(true).with_scheduled_at("in 1 hour"))
    .await?;

  Ok(())
}
```

```
Resend resend = new Resend("re_xxxxxxxxx");

// Create a draft broadcast
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);

// Create and send immediately
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .send(true)
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);

// Create and schedule
CreateBroadcastOptions params = CreateBroadcastOptions.builder()
    .segmentId("78261eea-8f8b-4381-83c6-79fa7120f1cf")
    .from("Acme <onboarding@resend.dev>")
    .subject("hello world")
    .html("Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}")
    .send(true)
    .scheduledAt("in 1 hour")
    .build();
CreateBroadcastResponseSuccess data = resend.broadcasts().create(params);
```

```
using Resend;

IResend resend = ResendClient.Create( "re_xxxxxxxxx" ); // Or from DI

// Create a draft broadcast
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );

// Create and send immediately
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
        Send = true,
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );

// Create and schedule
var resp = await resend.BroadcastAddAsync(
    new BroadcastData()
    {
        DisplayName = "Example Broadcast",
        SegmentId = new Guid( "78261eea-8f8b-4381-83c6-79fa7120f1cf" ),
        From = "Acme <onboarding@resend.dev>",
        Subject = "Hello, world!",
        HtmlBody = "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
        Send = true,
        ScheduledAt = DateTime.UtcNow.AddHours( 1 ),
    }
);

Console.WriteLine( "Broadcast Id={0}", resp.Content );
```

```
# Create a draft broadcast
curl -X POST 'https://api.resend.com/broadcasts' \
     -H 'Authorization: Bearer re_xxxxxxxxx' \
     -H 'Content-Type: application/json' \
     -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}"
}'

# Create and send immediately
curl -X POST 'https://api.resend.com/broadcasts' \
 -H 'Authorization: Bearer re_xxxxxxxxx' \
 -H 'Content-Type: application/json' \
 -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true
}'

# Create and schedule
curl -X POST 'https://api.resend.com/broadcasts' \
 -H 'Authorization: Bearer re_xxxxxxxxx' \
 -H 'Content-Type: application/json' \
 -d $'
{
  "segment_id": "78261eea-8f8b-4381-83c6-79fa7120f1cf",
  "from": "Acme <onboarding@resend.dev>",
  "subject": "hello world",
  "html": "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}",
  "send": true,
  "scheduled_at": "in 1 hour"
}'
```

```
# Create a draft broadcast
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}"

# Create and send immediately
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}" \
  --send

# Create and schedule
resend broadcasts create \
  --from "Acme <onboarding@resend.dev>" \
  --subject "hello world" \
  --segment-id 78261eea-8f8b-4381-83c6-79fa7120f1cf \
  --html "Hi {{{contact.first_name|there}}}, you can unsubscribe here: {{{RESEND_UNSUBSCRIBE_URL}}}" \
  --send \
  --scheduled-at "in 1 hour"
```

Response

```
{
  "id": "49a3999c-0ce1-4ea6-ab68-afcd6dc2e794"
}
```

## [​](https://resend.com/docs/api-reference/broadcasts/create-broadcast\#body-parameters)  Body Parameters

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#segment-id)

segmentId

string

required

The ID of the segment you want to send to.

Audiences are now called Segments. Follow the [Migration\\
Guide](https://resend.com/docs/dashboard/segments/migrating-from-audiences-to-segments).

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-from)

from

string

required

Sender email address.To include a friendly name, pass the sender as `Name <email@example.com>`, for example `Acme <onboarding@example.dev>`.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-subject)

subject

string

required

Email subject.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#reply-to)

replyTo

string \| string\[\]

Reply-to email address. For multiple addresses, send as an array of strings.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-html)

html

string

The HTML version of the message. You can include Contact Properties in the
body of the Broadcast. Learn more about [Contact\\
Properties](https://resend.com/docs/dashboard/audiences/contacts).

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-text)

text

string

The plain text version of the message. You can include Contact Properties in the body of the Broadcast. Learn more about [Contact Properties](https://resend.com/docs/dashboard/audiences/contacts).

If not provided, the HTML will be used to generate a plain text version. You
can opt out of this behavior by setting value to an empty string.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-react)

react

React.ReactNode

The React component used to write the message. _Only available in the Node.js_
_SDK._

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-name)

name

string

The friendly name of the broadcast. Only used for internal reference.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#topic-id)

topicId

string

The topic ID that the broadcast will be scoped to.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#param-send)

send

boolean

Send the broadcast immediately after creation. Defaults to `false`.

When set to `true`, the broadcast will be sent or scheduled (if `scheduled_at` is provided) without requiring a separate call to the [Send Broadcast](https://resend.com/docs/api-reference/broadcasts/send-broadcast) endpoint.

[​](https://resend.com/docs/api-reference/broadcasts/create-broadcast#scheduled-at)

scheduledAt

string

Schedule the broadcast to be sent later. The date should be in natural language (e.g.: `in 1 min`) or ISO 8601 format (e.g: `2026-08-05T11:52:01.858Z`).

This parameter requires `send` to be set to `true`.

Was this page helpful?

YesNo

[List Attachments\\
\\
Previous](https://resend.com/docs/api-reference/emails/list-received-email-attachments) [Send Broadcast\\
\\
Next](https://resend.com/docs/api-reference/broadcasts/send-broadcast)

Ctrl+I

Assistant

Responses are generated using AI and may contain mistakes.
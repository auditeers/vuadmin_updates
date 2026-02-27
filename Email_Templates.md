# Email Templates — Variables Reference

Template fields (`subject`, `greeting`, `text_top`, `action_link`, `action_text`, `text_bottum`) are processed with `Blade::render()`.
Use standard Blade syntax: `{{ $variable }}`, `{{ $variable->property }}`, `@if(...)`, etc.

---

## Template 1 — Waitinglist

**Mail class:** `App\Mail\Waitinglist`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$program` | Program | Program object |
| `$type` | string | `'private'` or other |

---

## Template 2 — SendConfirmation

**Mail class:** `App\Mail\SendConfirmation`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 3 — Intake

**Mail class:** `App\Mail\Intake`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 4 — SendInvite

**Mail class:** `App\Mail\SendInvite`

| Variable | Type | Description |
|---|---|---|
| `$student` | Student | Student object |
| `$course` | Course | Course object |
| `$program` | Program | Program object |
| `$secret` | string | MD5 hash for invite link — **only available in `action_link`** |

---

## Template 5 — PaymentLink

**Mail class:** `App\Mail\PaymentLink`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 9 — Standard (Questionnaire)

**Mail class:** `App\Mail\Standard`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 12 — CompanyInvoice

**Mail class:** `App\Mail\CompanyInvoice`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 13 — SendCancellation (inschrijving)

**Mail class:** `App\Mail\SendCancellation`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 16 — SendInvoice

**Mail class:** `App\Mail\SendInvoice`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |
| `$invoice` | Invoice | Invoice object |

---

## Template 17 — SendProgramConfirmation

**Mail class:** `App\Mail\SendProgramConfirmation`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 18 — SendCancellation (programma geannuleerd)

**Mail class:** `App\Mail\SendCancellation` (same class as template 13, different template ID)

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 19 — NewStudent

**Mail class:** `App\Mail\NewStudent`

| Variable | Type | Description |
|---|---|---|
| `$student` | Student | Student object |

---

## Template 20 — StudentTransfer

**Mail class:** `App\Mail\StudentTransfer`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |
| `$program` | Program | Program object (the new program) |

---

## Template 21 — SendStopped

**Mail class:** `App\Mail\SendStopped`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 22 — SendTeacherConfirmation

**Mail class:** `App\Mail\SendTeacherConfirmation`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 23 — SendTeacherCancellation

**Mail class:** `App\Mail\SendTeacherCancellation`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$program` | Program | Program object |

---

## Template 24 — Moodlemail

**Mail class:** `App\Mail\Moodlemail`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Template 25 — Cartleftmail

**Mail class:** `App\Mail\Cartleftmail`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$cart` | Cart | Cart object |
| `$cartHash` | string | Cart hash (used for resume cart URL) |

---

## Template 26 — Teacherlist

**Mail class:** `App\Mail\Teacherlist`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |
| `$listHtml` | string | Pre-built HTML `<ul>` list of enrolled students (name, email, phone) |

> Use `{!! $listHtml !!}` (unescaped) to render the HTML list.

---

## Template 27 — Seintjemail

**Mail class:** `App\Mail\Seintjemail`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order` | Order | Order object |

---

## Template 28 — CourseStart

**Mail class:** `App\Mail\CourseStart`

| Variable | Type | Description |
|---|---|---|
| `$email` | string | Recipient email |
| `$name` | string | Recipient name |
| `$course` | Course | Course object |
| `$order_item` | OrderItem | Order item object |

---

## Evaluation Invite (dynamic template ID)

Template ID is set via `$evaluation->emailtemplate_id`.
**Mail class:** `App\Mail\EvaluationInvite`

| Variable | Type | Description |
|---|---|---|
| `$student` | Student | Student object |
| `$course` | Course | Course object |
| `$program` | Program | Program object |
| `$teacher` | Teacher | Teacher object |
| `$evaluationUrl` | string | Full URL to the evaluation form |

---

## Evaluation Reminder (dynamic template ID)

Template ID is set via `$evaluation->reminder_emailtemplate_id`.
**Mail class:** `App\Mail\EvaluationReminder`

| Variable | Type | Description |
|---|---|---|
| `$student` | Student | Student object |
| `$course` | Course | Course object |
| `$program` | Program | Program object |
| `$teacher` | Teacher | Teacher object |
| `$evaluationUrl` | string | Full URL to the evaluation form |

---

## Common Usage Examples

```blade
{{ $name }}                           → recipient's full name (string)
{{ $email }}                          → recipient email address

{{ $course->name }}                   → course name
{{ $course->id }}                     → course ID

{{ $program->startdate }}             → program start date
{{ $program->location }}              → program location

{{ $order_item->student->firstname }} → student first name via relation
{{ $order_item->student->email }}     → student email via relation
{{ $order_item->program->startdate }} → program start date via relation

{{ $student->firstname }}             → student first name
{{ $student->lastname }}              → student last name
{{ $student->email }}                 → student email

{{ $invoice->number }}                → invoice number

{{ $evaluationUrl }}                  → full URL to evaluation form

{!! $listHtml !!}                     → rendered HTML student list (template 26 only)
```

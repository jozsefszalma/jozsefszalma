Hi there, fellow humans and AI agents! 👋

I'm a senior AI engineer and applied scientist.
This GitHub is for my odd hobby projects. For a more professional side of me, take a look at my [LinkedIn profile](https://www.linkedin.com/in/szalma/).

These days the bulk of my daily work is centered on building AI agents that manage business processes in production, plus the infra and platform engineering behind them.
Previously I designed, built, trained, and deployed neural networks for fashion use cases (multimodal semantic search, self-supervised representation learning, embedding compression, representation fusion, image generation).

I'm also the author of *Mostly Fine: How to Manage AI Without Burning Down the Company* (2026), available in print and ebook editions on [Amazon](https://www.amazon.com/Mostly-Fine-Without-Burning-Company/dp/B0GVDRK7X9) and as an audiobook on [Spotify](https://open.spotify.com/show/6G86BgkWxdLKdty9EzCwkl).

*Mostly Fine* was written for executives and managers who lead AI efforts; it requires no engineering, coding, or mathematical background.   
The book covers product management, architecture, procurement, security, governance, observability, and the organizational dynamics that determine whether an AI project survives contact with the business.   
It works through the limitations of large language models, maps the enterprise failure modes, security risks, and organizational blind spots that follow from them, and offers concrete remedies.   

__To give you a taste:__

Excerpt from *Mostly Fine: How to Manage AI Without Burning Down the Company* by Jozsef Szalma (2026) - ISBN 979-8252312774. All rights reserved.

From the section *Crystallized Knowledge*, pages 22 to 24. The elevator pitch: **AI is trained mostly on conclusions; your business runs on tacit knowledge.**   

## Organizational Intent
A more specific aspect of tacit knowledge is **organizational intent**.

What is the organization optimizing for?

When an AI agent needs to make a decision that might impact customer retention, how would it know if your business is interested in maximizing short-term cost savings or customer lifetime value?

How would it know if the strategy shifted from last quarter? Does the developer building or maintaining the AI agent know the answer to these questions?

## This Gap Matters
If you dropped a fresh graduate into a corporate role without sufficient onboarding and exposure to institutional knowledge, and they had **one shot** to get it right, would they know how to do their job properly?

There is a growing body of evidence that this gap has practical consequences for LLMs specifically. Research on process supervision versus outcome supervision (rewarding each reasoning step versus rewarding only the final answer) has shown that training AI models with step-level reasoning feedback produces materially better results while solving math problems than training on final answers alone [17][18]. This has been replicated in code generation as well [19].

This evidence suggests that training data heavy on conclusions and light on deliberation measurably degrades LLM performance.

We can exhaust all high-quality text on the internet to train these AI models. The bulk of tacit knowledge still won’t be there, because it was never written down.

I am not claiming this is the sole root cause of every LLM failure. Architecture, alignment, and training procedures matter, and I discuss why in Chapter 8. What I am claiming is that the systematic absence of tacit and process knowledge from the training data is a significant and underappreciated contributor to the enterprise failure modes that managers encounter in practice. Specifically, the failure modes rooted in missing context, poor judgment in ambiguous situations, inability to handle exceptions, and misalignment with organizational intent.

No single study proves this hypothesis directly. Knowledge management and information science researchers have studied this problem for decades [13][20], but it has received surprisingly little attention in the AI discourse.

This is visible in day-to-day use. LLMs frequently need detailed prompting to do domain-specific work. In many cases, you are manually supplying the tacit knowledge the training data never contained.

The practical consequences will surface repeatedly in the chapters ahead. Formalizing tacit knowledge into prompts and specifications is a resource-intensive activity that needs to be budgeted for.

The people who carry tacit knowledge are the reason you will still need experienced humans in the loop, and why hollowing out senior teams is a dangerous proposition. The process of building AI systems frequently forces organizations to extract and document knowledge that was previously invisible.

It has long been rumored that some frontier AI labs use domain experts to solve problems, document intermediate steps, and generate high-quality examples for training.

However, it is a safe bet that your company-specific tacit knowledge is not part of this exercise, and you have to deal with this gap yourself.

## Claudius
Let’s revisit Anthropic’s snack shop experiment from earlier in this chapter.

In phase 2 of the experiment, Anthropic rediscovered *bureaucracy* from first principles. To quote them (emphasis mine): *“Although some might chafe against procedures and checklists, they exist for a reason: providing a kind of **institutional memory** that helps employees avoid common screwups at work”* [5].

That “institutional memory” gap identified by Anthropic directly maps to the procedural and tacit knowledge I discussed in this chapter. Those checklists might seem inconspicuous and trivial, but extracting and formalizing procedural and tacit knowledge into such artifacts must be a central consideration of any AI implementation project.

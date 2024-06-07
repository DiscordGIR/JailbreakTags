# JailbreakTags

## What is this?
The [r/Jailbreak Subreddit](https://reddit.com/r/jailbreak) and the [r/Jailbreak Discord](https://discord.gg/jailbreak) communities wanted a synchronized way of maintaining tags (reusable bits of information, for example answers to frequently asked questions, that can be called using commands) across platforms, and that's what this repository is for.

The Geniuses in the Discord server have curated the information and advice contained in `tags.json` over time, and this is now becoming an open source effort. Anyone is free to contribute tags that they think are relevant for the community, and pending review from our Geniuses, it will be merged. 

## How to contribute
We're grateful to anyone who would like to help out!

To contribute, we ask that you:
* make a fork of the repository
* make a pull request against the repository, with a description of what the tag is and why it is needed
* in case of changing an existing tag, also write a description of why it is changing
* follow the styling and formatting of the file, and the language of existing tags

### Writing a tag
As you can see, `tags.json` is a JSON file containing an array of objects, each object representing a tag.

Here is an example tag:

```json
{
  "name": "test",
  "content": "Description for the tag",
  "button_links": [
    {
      "label": "Button label",
      "url": "https://test.com"
    }
  ],
  "image": "https://test.com/image.png"
}
```

In case you need to add an image to your tag, we ask that you **include the image within your PR** by saving the image in the `images/` folder named the same as the tag (i.e for tag `test`, call the image `test.png`). For the link, you can then use `https://raw.githubusercontent.com/DiscordGIR/JailbreakTags/main/images/<filename here>` and the link will work once your pull request is merged.

Note that `button_links` and `image` are optional fields and can be left out if not applicable. A detailed description of the format of a tag can be seen in `schema.json`

### Review process
In order for your tag to be approved, your pull request will:
* be automatically checked to ensure it follows the format laid out above, and follows our styling guide (i.e proper indentation, spacing, etc.). It must pass these checks in order to be approved. In case there are errors, you can push a commit with fixes.
* be reviewed by the Genius team. It is required that at least 3 Geniuses approve the PR before it can be merged. Geniuses can request changes if the language is unclear, or decline your PR if they feel it is irrelevant.
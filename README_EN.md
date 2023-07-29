# [小徐学长] ( https://weeklyreport.avemaria.fun/ ) 


该项目使用人工智能为您生成带有简单句子的每周报告。

[ ![小徐学长] ( ./public/screenshot.jpg ) ] ( https://weeklyreport.avemaria.fun/zh )

##它是如何工作的

该项目使用[ OpenAI GPT-3 API ] ( https://openai.com/api/ )（具体来说，text-davinci-003）和[ Vercel Edge 函数] ( https://vercel.com/features/edge -functions ）与流式传输。它根据表单和用户输入构建提示，通过 Vercel Edge 函数将其发送到 GPT-3 API，然后将响应流式传输回应用程序。

##本地运行

克隆存储库后，前往[ OpenAI ] ( https://beta.openai.com/account/api-keys )创建一个帐户，并将您的 API 密钥放入名为` .env `的文件中。

然后，在命令行中运行该应用程序，它将在“ http://localhost:3000 ”处可用。

``重击
npm 运行开发
````

##一键部署

使用[ Vercel ] ( https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=vercel-examples )部署示例：

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://vercel.com/new/clone?repository-url=https://github.com/guaguaguaxia/weekly_report&env=OPENAI_API_KEY,NEXT_PUBLIC_USE_USER_KEY&project-name=weekly_report&repo-name=weekly_report)

NEXT_PUBLIC_USE_USER_KEY = false

## Docker Deployment

```bash
docker run -d -p 3000:3000 --name weekly_report-docker -e OPENAI_API_KEY=sk-xxxxx ihxrainbow/weekly_report-docker
```

docker-compose.yml
```yaml
services:
  weekly_report-docker:
    container_name: weekly_report-docker
    ports:
      - '3000:3000'
    image: ihxrainbow/weekly_report-docker
    environment:
      # API key
      - OPENAI_API_KEY=sk-xxxxx
```

<!-- https://www.seotraininglondon.org/gpt3-business-email-generator/ -->

## Credits

Inspired by [TwtterBio](https://github.com/Nutlope/twitterbio) and [zhengbangbo](https://github.com/zhengbangbo/chat-simplifier).



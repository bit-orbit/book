# Developer Persian Terminology (واژه‌نامه تخصصی و لحن مهندسی)

## 1. The Developer Persian Tone
In Iranian software engineering, DevOps, and cloud-native communities, industry-standard English terminology is used directly rather than forced into literal Persian translations. 

- **Avoid Literal Calques:** Translating technical terms literally sounds foreign, confusing, and amateurish to professional engineers.
- **Natural Compound Verbs:** Combine the authentic English technical term (or its universally accepted transliteration) with Persian helper verbs (e.g., «اسکیل کردن»، «دیپلوی کردن»، «لاگ انداختن»، «هندل کردن»، «رول‌بک زدن»).

## 2. Mandatory Terminology Lookup Table

| English Term | INCORRECT (Literal / Calque) | APPROVED (Developer Persian) | Notes / Context |
| :--- | :--- | :--- | :--- |
| **Scale / Scaling** | مقیاس / مقیاس‌دهی / مقیاس‌پذیری | **اسکیل / اسکیل کردن / اسکیل‌پذیری (Scaling)** | Never use «مقیاس» for pod/system capacity scaling. |
| **Scale up / Scale down** | افزایش مقیاس / کاهش مقیاس | **اسکیل‌آپ (Scale-up) / اسکیل‌داون (Scale-down)** | Horizontal or vertical capacity adjustments. |
| **Auto-scaling** | مقیاس‌پذیری خودکار | **اسکیل خودکار / Auto-scaling** | Dynamic workload adjustments (e.g., HPA). |
| **Deploy / Deployment** | استقرار دادن | **دیپلوی کردن / دیپلویمنت (Deployment)** | Workload delivery or Kubernetes Deployment object. |
| **Rollout / Rolling Update** | چرخش / استقرار غلتان | **رولینگ آپدیت (Rolling Update) / انتشار تدریجی** | Progressive zero-downtime updates. |
| **Rollback** | عقب‌گرد | **رول‌بک (Rollback)** | Reverting to a previous stable revision. |
| **Pipeline** | خط لوله | **پایپ‌لاین (Pipeline)** | CI/CD build and delivery pipelines. |
| **Cache / Caching** | حافظه پنهان | **کش / کش کردن (Cache)** | High-speed data caching layers. |
| **Trace / Tracing** | ردیابی | **تریس / تریس کردن (Trace / Tracing)** | Distributed request tracing (OpenTelemetry). |
| **Queue** | صف | **صف / صف پیام (Queue)** | Message brokers (Kafka, RabbitMQ, SQS). |
| **Worker / Node** | کارگر | **ورکر (Worker) / نود (Node)** | Compute instances running container workloads. |
| **Cluster** | خوشه | **کلاستر (Cluster)** | Coordinated set of control-plane & worker nodes. |
| **Namespace** | فضای نام | **نیم‌اسپیس (Namespace)** | Virtual cluster isolation boundary. |
| **Ingress** | ورودی | **اینگرس (Ingress)** | L7 HTTP/HTTPS traffic routing layer. |
| **Pod** | پیله | **پاد (Pod)** | Fundamental atomic unit of execution in k8s. |
| **Build / Compile** | ساختن | **بیلد / کامپایل کردن (Build / Compile)** | Code compilation and container image construction. |
| **Refactor** | بازسازی | **ری‌فکتور / ری‌فکتور کردن (Refactor)** | Restructuring code without changing external behavior. |

## 3. Initial Mention Convention
On the first occurrence of an essential technical concept within a chapter:
1. Provide the smooth Persian contextual phrasing followed by the English technical term in parentheses:
   * Example: `اسکیل دستی و خودکار (Scaling)`
   * Example: `دیپلویمنت اعلانی (Deployment)`
2. In subsequent mentions throughout the same chapter, use the technical term directly (`اسکیل کردن`, `دیپلویمنت`).

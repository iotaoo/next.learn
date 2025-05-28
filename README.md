## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## Next APP 使用知识点

```npm
npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm
```

### demo分析
  1. css 功能分析，tailwind clsx （global.css import）
  2. 图片，字体优化 （图片提供了Image 以及字体的修改）
  3. 文件结构分析

### 路由
  1. 文件路由系统 文件路由配置
  2. (group name) 路由组 

### database 数据库
  1. github注册及vercel 关联
  2. 发布静态
  3. 创建database demo 使用的postgres vercel已经集成Neon 


### 客户端 服务端组件路由参数获取
```tsx
  // 客户端组件 useSearchParams
  const searchParams = useSearchParams();

    //只是衍生 URL对象 params.toString() --> query=lee&page=1
    const params = new URLSearchParams(searchParams); 
    parms.set(key,value)
    parms.get(key)
    params.delete(key);

  // 服务端组件 props
  const searchParams = props.searchParams;
```
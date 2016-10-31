# webpack-react-loader

[中文版](https://github.com/sunOpar/webpack-react-loader/blob/master/README-zh.md)

write react in single file with webpack

## feature
1. combine jsx and css in single file
2. support less,sass

## example

```
//about.react
<script>
var About = ()=>{
  return (
    <div className='container'>
    about
    </div>
  )
}
export default About;
</script>

<style>
.container{
  color:red;
}
</style>
```

## how to use

1.install the react-loader package with npm

```
npm install webpack-react-loader
```
2.config your webpack

```
//webpack.config.js
module: {
    loaders: [
        {
        test: /\.react$/,
        exclude: /node_modules/,
        loader: 'react-loader'
        }
    ]
}

```

3.write single file react,and import

```
import About from 'About.react'
```

### change stylesheet lang

```
// app.react
<script>
...
</script>
<style lang="scss(or less)">
...
</style>
```

## What next

1. support sourceMap
2. support style scope

You can contact me if you have any idea.
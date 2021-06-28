---
title: 框架概述
---

如题

#### 框架文档：<a href="http://angular.cn" target="_blank">http://angular.cn<a> / <a href="http://angular.io" target="_blank">http://angular.io<a>

{% highlight swift %}
struct ContentView: View {
    @State var showDetails = false

    var body: some View {
        VStack {
            Button(action: {
                withAnimation {
                    self.showDetails.toggle()
                }
            }) {
                Text("Tap to show details")
            }

            if showDetails {
                Text("Details go here.")
            }
        }
    }
}
{% endhighlight %}

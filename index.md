---
title: 框架概述
---

如题

框架文档：http://angular.cn/

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

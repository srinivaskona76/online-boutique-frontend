## Quick Start
1. **Deploy the [online-boutique](https://github.com/mkryshak/online-boutique) microservices to the cluster.**

   ```
   kubectl apply -f ./manifests/deployment.yaml
   ```
   
2. **Wait for the pods to be ready.**
   
   ```
   kubectl get pods
   ```
   
   After a few minutes, you should see the pods running:
   
   ```
   NAME                                     READY   STATUS    RESTARTS   AGE
   adservice-76bdd69666-ckc5j               1/1     Running   0          2m58s
   cartservice-66d497c6b7-dp5jr             1/1     Running   0          2m59s
   checkoutservice-666c784bd6-4jd22         1/1     Running   0          3m1s
   currencyservice-5d5d496984-4jmd7         1/1     Running   0          2m59s
   emailservice-667457d9d6-75jcq            1/1     Running   0          3m2s
   loadgenerator-665b5cd444-gwqdq           1/1     Running   0          3m
   paymentservice-68596d6dd6-bf6bv          1/1     Running   0          3m
   productcatalogservice-557d474574-888kr   1/1     Running   0          3m
   recommendationservice-69c56b74d4-7z8r5   1/1     Running   0          3m1s
   redis-cart-5f59546cdd-5jnqf              1/1     Running   0          2m58s
   shippingservice-6ccc89f8fd-v686r         1/1     Running   0          2m58s
   ```
   
3. **Clone this repository.**

4. **Deploy the frontend application and servic.**
   
   ```
   kubectl apply -f ./manifests/deployment.yaml
   kubectl apply -f ./manifests/service.yaml
   ```

5. **Access the frontend application using the LoadBalancer external IP address.**
   
   ```
   kubectl get service frontend-external | awk '{print $4}'
   ```

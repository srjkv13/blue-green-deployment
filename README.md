# blue-green-deployment

# how to switch deployment

kubectl patch service html-service -p '{"spec":{"selector":{"version":"green"}}}' - will switch traffic to green

kubectl patch service html-service -p '{"spec":{"selector":{"version":"blue"}}}' - will switch traffic to blue

# How to monitor deployment

kubectl get pods -w

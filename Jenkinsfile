
withCredentials([azureServicePrincipal(credentialsId: 'AzureServicePrincipal',
                        subscriptionIdVariable: 'SUBS_ID',
                        clientIdVariable: 'CLIENT_ID',
                        clientSecretVariable: 'CLIENT_SECRET',
                        tenantIdVariable: 'TENANT_ID')]) {
  sh 'az login --service-principal -u $CLIENT_ID -p $CLIENT_SECRET -t $TENANT_ID'
  sh 'az resource list'
  sh 'az logout'
}

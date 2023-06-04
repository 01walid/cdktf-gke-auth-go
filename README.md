# cdktf-gke-auth-go

This is a meta-repository for the Golang version of [cdktf-gke-auth](https://github.com/01walid/cdktf-gke-auth) construct.

This repo's Golang module content is auto-updated by [projen](https://github.com/projen/projen) via the github actions of the [parent repo](https://github.com/01walid/cdktf-gke-auth). 

## Example Golang usage

```go
// Example automatically generated from non-compiling source. May contain errors.
import "github.com/cdktf/cdktf-provider-google-go/google"
import "github.com/hashicorp/terraform-cdk-go/cdktf"
import "github.com/aws/constructs-go/constructs"
import "github.com/01walid/cdktf-gke-auth-go/cdktfgkeauth"

type MyKubeStack struct {
	terraformStack
}

func NewMyKubeStack(scope construct, name *string) *MyKubeStack {
	this := &MyKubeStack{}
	newTerraformStack_Override(this, scope, name)

	google.NewGoogleProvider(this, jsii.String("google-provider"), &GoogleProviderConfig{
	})

	auth := cdktfgkeauth.NewGKEAuth(this, jsii.String("gke-auth"), &ClusterInfo{
		ClusterName: jsii.String("my-cluster"),
		Location: jsii.String("europe-west1"),
		ProjectId: jsii.String("my-project"),
	})
  
	return this
}

```

Please refer to the [parent repository](https://github.com/01walid/cdktf-gke-auth) for more information. 

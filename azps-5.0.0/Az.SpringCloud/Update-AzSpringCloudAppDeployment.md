---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115219"
---
# <span data-ttu-id="f062e-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="f062e-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="f062e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f062e-102">SYNOPSIS</span></span>
<span data-ttu-id="f062e-103">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="f062e-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="f062e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f062e-104">SYNTAX</span></span>

### <span data-ttu-id="f062e-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f062e-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f062e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f062e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f062e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f062e-107">DESCRIPTION</span></span>
<span data-ttu-id="f062e-108">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="f062e-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="f062e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f062e-109">EXAMPLES</span></span>

### <span data-ttu-id="f062e-110">Exemplo 1: atualizar a implantação de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="f062e-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="f062e-111">Atualize a implantação de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="f062e-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="f062e-112">Exemplo 2: atualizar a implantação de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="f062e-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="f062e-113">Atualize a implantação de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="f062e-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="f062e-114">OS</span><span class="sxs-lookup"><span data-stu-id="f062e-114">PARAMETERS</span></span>

### <span data-ttu-id="f062e-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="f062e-115">-AppName</span></span>
<span data-ttu-id="f062e-116">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f062e-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f062e-117">-AsJob</span></span>
<span data-ttu-id="f062e-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f062e-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="f062e-119">-Cpu</span></span>
<span data-ttu-id="f062e-120">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="f062e-120">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f062e-121">-DefaultProfile</span></span>
<span data-ttu-id="f062e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f062e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="f062e-123">-EnvironmentVariable</span></span>
<span data-ttu-id="f062e-124">Conjunto de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="f062e-124">Collection of environment variables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f062e-125">-InputObject</span></span>
<span data-ttu-id="f062e-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f062e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="f062e-127">-JvmOption</span></span>
<span data-ttu-id="f062e-128">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="f062e-128">JVM parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="f062e-129">-MemoryInGb</span></span>
<span data-ttu-id="f062e-130">Tamanho de memória necessário em GB</span><span class="sxs-lookup"><span data-stu-id="f062e-130">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f062e-131">-Name</span></span>
<span data-ttu-id="f062e-132">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="f062e-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f062e-133">-NoWait</span></span>
<span data-ttu-id="f062e-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f062e-134">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f062e-135">-ResourceGroupName</span></span>
<span data-ttu-id="f062e-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f062e-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f062e-137">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="f062e-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="f062e-138">-RuntimeVersion</span></span>
<span data-ttu-id="f062e-139">Versão do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="f062e-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f062e-140">-ServiceName</span></span>
<span data-ttu-id="f062e-141">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="f062e-141">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="f062e-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="f062e-143">Seletor para o artefato a ser usado para a implantação de projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="f062e-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="f062e-144">Isso deve Bethe o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="f062e-144">This should bethe relative path to the target module/project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="f062e-145">-SourceRelativePath</span></span>
<span data-ttu-id="f062e-146">Caminho relativo do armazenamento que armazena a origem</span><span class="sxs-lookup"><span data-stu-id="f062e-146">Relative path of the storage which stores the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f062e-147">-SourceType</span></span>
<span data-ttu-id="f062e-148">Tipo de fonte carregada</span><span class="sxs-lookup"><span data-stu-id="f062e-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="f062e-149">-SourceVersion</span></span>
<span data-ttu-id="f062e-150">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="f062e-150">Version of the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f062e-151">-SubscriptionId</span></span>
<span data-ttu-id="f062e-152">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f062e-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f062e-153">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f062e-153">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f062e-154">-Confirm</span></span>
<span data-ttu-id="f062e-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f062e-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f062e-156">-WhatIf</span></span>
<span data-ttu-id="f062e-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f062e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f062e-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f062e-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f062e-159">CommonParameters</span></span>
<span data-ttu-id="f062e-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f062e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f062e-161">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f062e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f062e-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f062e-162">INPUTS</span></span>

### <span data-ttu-id="f062e-163">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f062e-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f062e-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f062e-164">OUTPUTS</span></span>

### <span data-ttu-id="f062e-165">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="f062e-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="f062e-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f062e-166">NOTES</span></span>

<span data-ttu-id="f062e-167">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f062e-167">ALIASES</span></span>

<span data-ttu-id="f062e-168">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f062e-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f062e-169">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f062e-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f062e-170">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f062e-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f062e-171">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f062e-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f062e-172">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f062e-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f062e-173">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="f062e-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f062e-174">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="f062e-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f062e-175">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="f062e-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f062e-176">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="f062e-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f062e-177">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f062e-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f062e-178">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="f062e-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f062e-179">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f062e-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f062e-180">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="f062e-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f062e-181">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="f062e-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f062e-182">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f062e-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f062e-183">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f062e-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f062e-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f062e-184">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113286"
---
# <span data-ttu-id="a5881-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="a5881-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="a5881-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5881-102">SYNOPSIS</span></span>
<span data-ttu-id="a5881-103">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="a5881-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="a5881-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5881-104">SYNTAX</span></span>

### <span data-ttu-id="a5881-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5881-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a5881-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5881-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5881-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5881-107">DESCRIPTION</span></span>
<span data-ttu-id="a5881-108">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="a5881-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="a5881-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5881-109">EXAMPLES</span></span>

### <span data-ttu-id="a5881-110">Exemplo 1: atualizar a implantação de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="a5881-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="a5881-111">Atualize a implantação de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="a5881-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="a5881-112">Exemplo 2: atualizar a implantação de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="a5881-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="a5881-113">Atualize a implantação de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="a5881-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="a5881-114">OS</span><span class="sxs-lookup"><span data-stu-id="a5881-114">PARAMETERS</span></span>

### <span data-ttu-id="a5881-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="a5881-115">-AppName</span></span>
<span data-ttu-id="a5881-116">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a5881-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="a5881-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5881-117">-AsJob</span></span>
<span data-ttu-id="a5881-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a5881-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a5881-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="a5881-119">-Cpu</span></span>
<span data-ttu-id="a5881-120">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="a5881-120">Required CPU</span></span>

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

### <span data-ttu-id="a5881-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5881-121">-DefaultProfile</span></span>
<span data-ttu-id="a5881-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5881-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5881-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a5881-123">-EnvironmentVariable</span></span>
<span data-ttu-id="a5881-124">Conjunto de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="a5881-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="a5881-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5881-125">-InputObject</span></span>
<span data-ttu-id="a5881-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a5881-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5881-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a5881-127">-InstanceCount</span></span>
<span data-ttu-id="a5881-128">Contagem de instâncias</span><span class="sxs-lookup"><span data-stu-id="a5881-128">Instance count</span></span>

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

### <span data-ttu-id="a5881-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="a5881-129">-JvmOption</span></span>
<span data-ttu-id="a5881-130">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="a5881-130">JVM parameter</span></span>

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

### <span data-ttu-id="a5881-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="a5881-131">-MemoryInGb</span></span>
<span data-ttu-id="a5881-132">Tamanho de memória necessário em GB</span><span class="sxs-lookup"><span data-stu-id="a5881-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="a5881-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5881-133">-Name</span></span>
<span data-ttu-id="a5881-134">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="a5881-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="a5881-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a5881-135">-NoWait</span></span>
<span data-ttu-id="a5881-136">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a5881-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5881-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5881-137">-ResourceGroupName</span></span>
<span data-ttu-id="a5881-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a5881-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a5881-139">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="a5881-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a5881-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="a5881-140">-RuntimeVersion</span></span>
<span data-ttu-id="a5881-141">Versão do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a5881-141">Runtime version</span></span>

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

### <span data-ttu-id="a5881-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5881-142">-ServiceName</span></span>
<span data-ttu-id="a5881-143">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="a5881-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a5881-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="a5881-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="a5881-145">Seletor para o artefato a ser usado para a implantação de projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="a5881-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="a5881-146">Isso deve Bethe o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a5881-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="a5881-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a5881-147">-SourceRelativePath</span></span>
<span data-ttu-id="a5881-148">Caminho relativo do armazenamento que armazena a origem</span><span class="sxs-lookup"><span data-stu-id="a5881-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="a5881-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="a5881-149">-SourceType</span></span>
<span data-ttu-id="a5881-150">Tipo de fonte carregada</span><span class="sxs-lookup"><span data-stu-id="a5881-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="a5881-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="a5881-151">-SourceVersion</span></span>
<span data-ttu-id="a5881-152">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="a5881-152">Version of the source</span></span>

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

### <span data-ttu-id="a5881-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5881-153">-SubscriptionId</span></span>
<span data-ttu-id="a5881-154">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a5881-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5881-155">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a5881-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5881-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5881-156">-Confirm</span></span>
<span data-ttu-id="a5881-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5881-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5881-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5881-158">-WhatIf</span></span>
<span data-ttu-id="a5881-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5881-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5881-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5881-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5881-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5881-161">CommonParameters</span></span>
<span data-ttu-id="a5881-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5881-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5881-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5881-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5881-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5881-164">INPUTS</span></span>

### <span data-ttu-id="a5881-165">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a5881-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a5881-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5881-166">OUTPUTS</span></span>

### <span data-ttu-id="a5881-167">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="a5881-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="a5881-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5881-168">NOTES</span></span>

<span data-ttu-id="a5881-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a5881-169">ALIASES</span></span>

<span data-ttu-id="a5881-170">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a5881-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5881-171">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a5881-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5881-172">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5881-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5881-173">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a5881-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5881-174">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a5881-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a5881-175">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="a5881-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a5881-176">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="a5881-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a5881-177">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="a5881-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a5881-178">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="a5881-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a5881-179">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a5881-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5881-180">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="a5881-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a5881-181">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a5881-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a5881-182">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="a5881-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a5881-183">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="a5881-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a5881-184">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a5881-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a5881-185">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a5881-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a5881-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5881-186">RELATED LINKS</span></span>


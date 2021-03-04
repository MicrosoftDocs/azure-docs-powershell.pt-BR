---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 466bf2908cf1da940a369d2276dbf39106d60515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892315"
---
# <span data-ttu-id="43bbc-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="43bbc-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="43bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="43bbc-103">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="43bbc-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="43bbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="43bbc-104">SYNTAX</span></span>

### <span data-ttu-id="43bbc-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43bbc-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="43bbc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43bbc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43bbc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="43bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="43bbc-108">Operação para atualizar uma implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="43bbc-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="43bbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="43bbc-110">Exemplo 1: Atualizar a Implantação da Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="43bbc-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="43bbc-111">Atualizar a Implantação da Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="43bbc-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="43bbc-112">Exemplo 2: Atualizar a Implantação de Nuvem de Primavera a partir do pipe.</span><span class="sxs-lookup"><span data-stu-id="43bbc-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="43bbc-113">Atualizar a Implantação de Nuvem de Primavera do pipe.</span><span class="sxs-lookup"><span data-stu-id="43bbc-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="43bbc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="43bbc-114">PARAMETERS</span></span>

### <span data-ttu-id="43bbc-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="43bbc-115">-AppName</span></span>
<span data-ttu-id="43bbc-116">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="43bbc-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="43bbc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43bbc-117">-AsJob</span></span>
<span data-ttu-id="43bbc-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="43bbc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="43bbc-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="43bbc-119">-Cpu</span></span>
<span data-ttu-id="43bbc-120">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="43bbc-120">Required CPU</span></span>

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

### <span data-ttu-id="43bbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bbc-121">-DefaultProfile</span></span>
<span data-ttu-id="43bbc-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43bbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43bbc-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="43bbc-123">-EnvironmentVariable</span></span>
<span data-ttu-id="43bbc-124">Coleção de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="43bbc-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="43bbc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43bbc-125">-InputObject</span></span>
<span data-ttu-id="43bbc-126">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="43bbc-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43bbc-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="43bbc-127">-JvmOption</span></span>
<span data-ttu-id="43bbc-128">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="43bbc-128">JVM parameter</span></span>

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

### <span data-ttu-id="43bbc-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="43bbc-129">-MemoryInGb</span></span>
<span data-ttu-id="43bbc-130">Tamanho de memória necessário em GB</span><span class="sxs-lookup"><span data-stu-id="43bbc-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="43bbc-131">-Name</span><span class="sxs-lookup"><span data-stu-id="43bbc-131">-Name</span></span>
<span data-ttu-id="43bbc-132">O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="43bbc-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="43bbc-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="43bbc-133">-NoWait</span></span>
<span data-ttu-id="43bbc-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="43bbc-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="43bbc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bbc-135">-ResourceGroupName</span></span>
<span data-ttu-id="43bbc-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="43bbc-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="43bbc-137">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="43bbc-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="43bbc-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="43bbc-138">-RuntimeVersion</span></span>
<span data-ttu-id="43bbc-139">Versão do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="43bbc-139">Runtime version</span></span>

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

### <span data-ttu-id="43bbc-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43bbc-140">-ServiceName</span></span>
<span data-ttu-id="43bbc-141">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="43bbc-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="43bbc-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="43bbc-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="43bbc-143">Seletor para o artefato a ser usado para a implantação para projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="43bbc-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="43bbc-144">Esse deve ser o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="43bbc-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="43bbc-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="43bbc-145">-SourceRelativePath</span></span>
<span data-ttu-id="43bbc-146">Caminho relativo do armazenamento que armazena a fonte</span><span class="sxs-lookup"><span data-stu-id="43bbc-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="43bbc-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="43bbc-147">-SourceType</span></span>
<span data-ttu-id="43bbc-148">Tipo da fonte carregada</span><span class="sxs-lookup"><span data-stu-id="43bbc-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="43bbc-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="43bbc-149">-SourceVersion</span></span>
<span data-ttu-id="43bbc-150">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="43bbc-150">Version of the source</span></span>

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

### <span data-ttu-id="43bbc-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43bbc-151">-SubscriptionId</span></span>
<span data-ttu-id="43bbc-152">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="43bbc-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="43bbc-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="43bbc-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43bbc-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43bbc-154">-Confirm</span></span>
<span data-ttu-id="43bbc-155">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bbc-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43bbc-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43bbc-156">-WhatIf</span></span>
<span data-ttu-id="43bbc-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43bbc-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43bbc-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43bbc-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43bbc-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bbc-159">CommonParameters</span></span>
<span data-ttu-id="43bbc-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43bbc-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bbc-161">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43bbc-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bbc-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43bbc-162">INPUTS</span></span>

### <span data-ttu-id="43bbc-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="43bbc-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="43bbc-164">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="43bbc-164">OUTPUTS</span></span>

### <span data-ttu-id="43bbc-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="43bbc-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="43bbc-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="43bbc-166">NOTES</span></span>

<span data-ttu-id="43bbc-167">ALIASES</span><span class="sxs-lookup"><span data-stu-id="43bbc-167">ALIASES</span></span>

<span data-ttu-id="43bbc-168">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="43bbc-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43bbc-169">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="43bbc-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43bbc-170">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43bbc-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43bbc-171">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="43bbc-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43bbc-172">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="43bbc-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="43bbc-173">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="43bbc-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="43bbc-174">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="43bbc-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="43bbc-175">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="43bbc-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="43bbc-176">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="43bbc-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="43bbc-177">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="43bbc-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43bbc-178">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="43bbc-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="43bbc-179">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="43bbc-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="43bbc-180">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="43bbc-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="43bbc-181">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="43bbc-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="43bbc-182">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="43bbc-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="43bbc-183">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="43bbc-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43bbc-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43bbc-184">RELATED LINKS</span></span>


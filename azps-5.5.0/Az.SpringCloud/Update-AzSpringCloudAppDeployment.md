---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113959"
---
# <span data-ttu-id="11933-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="11933-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="11933-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11933-102">SYNOPSIS</span></span>
<span data-ttu-id="11933-103">Operação para atualizar uma Implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="11933-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="11933-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11933-104">SYNTAX</span></span>

### <span data-ttu-id="11933-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11933-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="11933-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="11933-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11933-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11933-107">DESCRIPTION</span></span>
<span data-ttu-id="11933-108">Operação para atualizar uma Implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="11933-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="11933-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11933-109">EXAMPLES</span></span>

### <span data-ttu-id="11933-110">Exemplo 1: Atualizar a Implantação na Nuvem da Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="11933-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="11933-111">Atualize a Implantação na Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="11933-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="11933-112">Exemplo 2: Atualizar a Implantação de Nuvem de Primavera a partir do cano.</span><span class="sxs-lookup"><span data-stu-id="11933-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="11933-113">Atualize a Implantação de Nuvem de Primavera a partir do cano.</span><span class="sxs-lookup"><span data-stu-id="11933-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="11933-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11933-114">PARAMETERS</span></span>

### <span data-ttu-id="11933-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="11933-115">-AppName</span></span>
<span data-ttu-id="11933-116">O nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11933-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="11933-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11933-117">-AsJob</span></span>
<span data-ttu-id="11933-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="11933-118">Run the command as a job</span></span>

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

### <span data-ttu-id="11933-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="11933-119">-Cpu</span></span>
<span data-ttu-id="11933-120">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="11933-120">Required CPU</span></span>

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

### <span data-ttu-id="11933-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11933-121">-DefaultProfile</span></span>
<span data-ttu-id="11933-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11933-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11933-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="11933-123">-EnvironmentVariable</span></span>
<span data-ttu-id="11933-124">Conjunto de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="11933-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="11933-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11933-125">-InputObject</span></span>
<span data-ttu-id="11933-126">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="11933-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11933-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="11933-127">-JvmOption</span></span>
<span data-ttu-id="11933-128">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="11933-128">JVM parameter</span></span>

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

### <span data-ttu-id="11933-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="11933-129">-MemoryInGb</span></span>
<span data-ttu-id="11933-130">Tamanho da memória necessária em GB</span><span class="sxs-lookup"><span data-stu-id="11933-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="11933-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="11933-131">-Name</span></span>
<span data-ttu-id="11933-132">O nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="11933-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="11933-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11933-133">-NoWait</span></span>
<span data-ttu-id="11933-134">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="11933-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11933-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11933-135">-ResourceGroupName</span></span>
<span data-ttu-id="11933-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="11933-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="11933-137">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="11933-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="11933-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="11933-138">-RuntimeVersion</span></span>
<span data-ttu-id="11933-139">Versão de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="11933-139">Runtime version</span></span>

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

### <span data-ttu-id="11933-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11933-140">-ServiceName</span></span>
<span data-ttu-id="11933-141">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="11933-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="11933-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="11933-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="11933-143">Seletor para o artefato a ser usado para a implantação de projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="11933-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="11933-144">Esse deve ser o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="11933-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="11933-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="11933-145">-SourceRelativePath</span></span>
<span data-ttu-id="11933-146">Caminho relativo do armazenamento que armazena a fonte</span><span class="sxs-lookup"><span data-stu-id="11933-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="11933-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="11933-147">-SourceType</span></span>
<span data-ttu-id="11933-148">Tipo da fonte carregada</span><span class="sxs-lookup"><span data-stu-id="11933-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="11933-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="11933-149">-SourceVersion</span></span>
<span data-ttu-id="11933-150">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="11933-150">Version of the source</span></span>

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

### <span data-ttu-id="11933-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11933-151">-SubscriptionId</span></span>
<span data-ttu-id="11933-152">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11933-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="11933-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="11933-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11933-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11933-154">-Confirm</span></span>
<span data-ttu-id="11933-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11933-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11933-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11933-156">-WhatIf</span></span>
<span data-ttu-id="11933-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11933-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11933-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11933-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11933-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11933-159">CommonParameters</span></span>
<span data-ttu-id="11933-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11933-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11933-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11933-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11933-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="11933-162">INPUTS</span></span>

### <span data-ttu-id="11933-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="11933-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="11933-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="11933-164">OUTPUTS</span></span>

### <span data-ttu-id="11933-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="11933-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="11933-166">Notas</span><span class="sxs-lookup"><span data-stu-id="11933-166">NOTES</span></span>

<span data-ttu-id="11933-167">Aliases</span><span class="sxs-lookup"><span data-stu-id="11933-167">ALIASES</span></span>

<span data-ttu-id="11933-168">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="11933-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11933-169">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="11933-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11933-170">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11933-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11933-171">INPUTOBJECT: <ISpringCloudIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="11933-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11933-172">`[AppName <String>]`: o nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11933-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="11933-173">`[BindingName <String>]`: o nome do recurso Encadernação.</span><span class="sxs-lookup"><span data-stu-id="11933-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="11933-174">`[CertificateName <String>]`: o nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="11933-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="11933-175">`[DeploymentName <String>]`: o nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="11933-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="11933-176">`[DomainName <String>]`: o nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="11933-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="11933-177">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="11933-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11933-178">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="11933-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="11933-179">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="11933-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="11933-180">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="11933-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="11933-181">`[ServiceName <String>]`: o nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="11933-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="11933-182">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11933-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="11933-183">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="11933-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11933-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11933-184">RELATED LINKS</span></span>


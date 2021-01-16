---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259663"
---
# <span data-ttu-id="9850a-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="9850a-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="9850a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9850a-102">SYNOPSIS</span></span>
<span data-ttu-id="9850a-103">Crie uma nova implantação ou atualize uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="9850a-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="9850a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9850a-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9850a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9850a-105">DESCRIPTION</span></span>
<span data-ttu-id="9850a-106">Crie uma nova implantação ou atualize uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="9850a-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="9850a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9850a-107">EXAMPLES</span></span>

### <span data-ttu-id="9850a-108">Exemplo 1: exemplo 1: criar uma implantação em nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="9850a-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="9850a-109">Crie uma implantação em nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="9850a-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="9850a-110">OS</span><span class="sxs-lookup"><span data-stu-id="9850a-110">PARAMETERS</span></span>

### <span data-ttu-id="9850a-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="9850a-111">-AppName</span></span>
<span data-ttu-id="9850a-112">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9850a-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9850a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9850a-113">-AsJob</span></span>
<span data-ttu-id="9850a-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9850a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9850a-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="9850a-115">-Cpu</span></span>
<span data-ttu-id="9850a-116">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="9850a-116">Required CPU</span></span>

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

### <span data-ttu-id="9850a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9850a-117">-DefaultProfile</span></span>
<span data-ttu-id="9850a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9850a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9850a-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="9850a-119">-EnvironmentVariable</span></span>
<span data-ttu-id="9850a-120">Conjunto de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="9850a-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="9850a-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="9850a-121">-JvmOption</span></span>
<span data-ttu-id="9850a-122">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="9850a-122">JVM parameter</span></span>

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

### <span data-ttu-id="9850a-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="9850a-123">-MemoryInGb</span></span>
<span data-ttu-id="9850a-124">Tamanho de memória necessário em GB</span><span class="sxs-lookup"><span data-stu-id="9850a-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="9850a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9850a-125">-Name</span></span>
<span data-ttu-id="9850a-126">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="9850a-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9850a-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9850a-127">-NoWait</span></span>
<span data-ttu-id="9850a-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9850a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9850a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9850a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9850a-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9850a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9850a-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="9850a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9850a-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="9850a-132">-RuntimeVersion</span></span>
<span data-ttu-id="9850a-133">Versão do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9850a-133">Runtime version</span></span>

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

### <span data-ttu-id="9850a-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9850a-134">-ServiceName</span></span>
<span data-ttu-id="9850a-135">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="9850a-135">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9850a-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="9850a-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="9850a-137">Seletor para o artefato a ser usado para a implantação de projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="9850a-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="9850a-138">Isso deve Bethe o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="9850a-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="9850a-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="9850a-139">-SourceRelativePath</span></span>
<span data-ttu-id="9850a-140">Caminho relativo do armazenamento que armazena a origem</span><span class="sxs-lookup"><span data-stu-id="9850a-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="9850a-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="9850a-141">-SourceType</span></span>
<span data-ttu-id="9850a-142">Tipo de fonte carregada</span><span class="sxs-lookup"><span data-stu-id="9850a-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="9850a-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="9850a-143">-SourceVersion</span></span>
<span data-ttu-id="9850a-144">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="9850a-144">Version of the source</span></span>

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

### <span data-ttu-id="9850a-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9850a-145">-SubscriptionId</span></span>
<span data-ttu-id="9850a-146">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9850a-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9850a-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9850a-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9850a-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9850a-148">-Confirm</span></span>
<span data-ttu-id="9850a-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9850a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9850a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9850a-150">-WhatIf</span></span>
<span data-ttu-id="9850a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9850a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9850a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9850a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9850a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9850a-153">CommonParameters</span></span>
<span data-ttu-id="9850a-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9850a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9850a-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9850a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9850a-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9850a-156">INPUTS</span></span>

## <span data-ttu-id="9850a-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9850a-157">OUTPUTS</span></span>

### <span data-ttu-id="9850a-158">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="9850a-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="9850a-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9850a-159">NOTES</span></span>

<span data-ttu-id="9850a-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9850a-160">ALIASES</span></span>

## <span data-ttu-id="9850a-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9850a-161">RELATED LINKS</span></span>


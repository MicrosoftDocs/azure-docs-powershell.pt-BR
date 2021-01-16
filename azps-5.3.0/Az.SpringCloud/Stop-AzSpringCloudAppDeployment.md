---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271247"
---
# <span data-ttu-id="01995-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="01995-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="01995-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01995-102">SYNOPSIS</span></span>
<span data-ttu-id="01995-103">Parar a implantação.</span><span class="sxs-lookup"><span data-stu-id="01995-103">Stop the deployment.</span></span>

## <span data-ttu-id="01995-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01995-104">SYNTAX</span></span>

### <span data-ttu-id="01995-105">Parar (padrão)</span><span class="sxs-lookup"><span data-stu-id="01995-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01995-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01995-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01995-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01995-107">DESCRIPTION</span></span>
<span data-ttu-id="01995-108">Parar a implantação.</span><span class="sxs-lookup"><span data-stu-id="01995-108">Stop the deployment.</span></span>

## <span data-ttu-id="01995-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01995-109">EXAMPLES</span></span>

### <span data-ttu-id="01995-110">Exemplo 1: parar o serviço de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="01995-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="01995-111">Parar o serviço de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="01995-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="01995-112">Exemplo 2: parar o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="01995-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="01995-113">Parar o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="01995-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="01995-114">OS</span><span class="sxs-lookup"><span data-stu-id="01995-114">PARAMETERS</span></span>

### <span data-ttu-id="01995-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="01995-115">-AppName</span></span>
<span data-ttu-id="01995-116">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01995-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01995-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01995-117">-AsJob</span></span>
<span data-ttu-id="01995-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="01995-118">Run the command as a job</span></span>

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

### <span data-ttu-id="01995-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01995-119">-DefaultProfile</span></span>
<span data-ttu-id="01995-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01995-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01995-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01995-121">-InputObject</span></span>
<span data-ttu-id="01995-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="01995-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01995-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="01995-123">-Name</span></span>
<span data-ttu-id="01995-124">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="01995-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01995-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="01995-125">-NoWait</span></span>
<span data-ttu-id="01995-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="01995-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01995-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01995-127">-PassThru</span></span>
<span data-ttu-id="01995-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="01995-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="01995-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01995-129">-ResourceGroupName</span></span>
<span data-ttu-id="01995-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="01995-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="01995-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="01995-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01995-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="01995-132">-ServiceName</span></span>
<span data-ttu-id="01995-133">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="01995-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01995-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01995-134">-SubscriptionId</span></span>
<span data-ttu-id="01995-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01995-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="01995-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="01995-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01995-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01995-137">-Confirm</span></span>
<span data-ttu-id="01995-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01995-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01995-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01995-139">-WhatIf</span></span>
<span data-ttu-id="01995-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01995-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01995-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01995-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01995-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01995-142">CommonParameters</span></span>
<span data-ttu-id="01995-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01995-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01995-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01995-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01995-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01995-145">INPUTS</span></span>

### <span data-ttu-id="01995-146">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="01995-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="01995-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01995-147">OUTPUTS</span></span>

### <span data-ttu-id="01995-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01995-148">System.Boolean</span></span>

## <span data-ttu-id="01995-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01995-149">NOTES</span></span>

<span data-ttu-id="01995-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="01995-150">ALIASES</span></span>

<span data-ttu-id="01995-151">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="01995-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01995-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="01995-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01995-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01995-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01995-154">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="01995-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01995-155">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01995-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="01995-156">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="01995-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="01995-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="01995-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="01995-158">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="01995-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="01995-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="01995-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="01995-160">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="01995-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01995-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="01995-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="01995-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="01995-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="01995-163">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="01995-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="01995-164">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="01995-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="01995-165">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01995-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="01995-166">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="01995-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="01995-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01995-167">RELATED LINKS</span></span>


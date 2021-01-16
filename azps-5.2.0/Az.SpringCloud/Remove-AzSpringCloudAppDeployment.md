---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258143"
---
# <span data-ttu-id="fc7db-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="fc7db-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="fc7db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc7db-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7db-103">Operação para excluir uma implantação.</span><span class="sxs-lookup"><span data-stu-id="fc7db-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="fc7db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc7db-104">SYNTAX</span></span>

### <span data-ttu-id="fc7db-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc7db-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc7db-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc7db-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc7db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc7db-107">DESCRIPTION</span></span>
<span data-ttu-id="fc7db-108">Operação para excluir uma implantação.</span><span class="sxs-lookup"><span data-stu-id="fc7db-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="fc7db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc7db-109">EXAMPLES</span></span>

### <span data-ttu-id="fc7db-110">Exemplo 1: remover a implantação de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="fc7db-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="fc7db-111">Remova a implantação em nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="fc7db-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="fc7db-112">Exemplo 2: remover a implantação de nuvem do Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="fc7db-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="fc7db-113">Remover a implantação de nuvem Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="fc7db-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="fc7db-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc7db-114">PARAMETERS</span></span>

### <span data-ttu-id="fc7db-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="fc7db-115">-AppName</span></span>
<span data-ttu-id="fc7db-116">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc7db-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc7db-117">-AsJob</span></span>
<span data-ttu-id="fc7db-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fc7db-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fc7db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7db-119">-DefaultProfile</span></span>
<span data-ttu-id="fc7db-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc7db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7db-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc7db-121">-InputObject</span></span>
<span data-ttu-id="fc7db-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fc7db-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc7db-123">-Name</span></span>
<span data-ttu-id="fc7db-124">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="fc7db-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fc7db-125">-NoWait</span></span>
<span data-ttu-id="fc7db-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="fc7db-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fc7db-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc7db-127">-PassThru</span></span>
<span data-ttu-id="fc7db-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fc7db-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fc7db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7db-129">-ResourceGroupName</span></span>
<span data-ttu-id="fc7db-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fc7db-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fc7db-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="fc7db-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fc7db-132">-ServiceName</span></span>
<span data-ttu-id="fc7db-133">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc7db-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc7db-134">-SubscriptionId</span></span>
<span data-ttu-id="fc7db-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fc7db-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fc7db-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc7db-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7db-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc7db-137">-Confirm</span></span>
<span data-ttu-id="fc7db-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc7db-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7db-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7db-139">-WhatIf</span></span>
<span data-ttu-id="fc7db-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc7db-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7db-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc7db-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7db-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7db-142">CommonParameters</span></span>
<span data-ttu-id="fc7db-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7db-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7db-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc7db-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7db-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc7db-145">INPUTS</span></span>

### <span data-ttu-id="fc7db-146">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="fc7db-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="fc7db-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc7db-147">OUTPUTS</span></span>

### <span data-ttu-id="fc7db-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc7db-148">System.Boolean</span></span>

## <span data-ttu-id="fc7db-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc7db-149">NOTES</span></span>

<span data-ttu-id="fc7db-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fc7db-150">ALIASES</span></span>

<span data-ttu-id="fc7db-151">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fc7db-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc7db-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fc7db-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc7db-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc7db-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc7db-154">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fc7db-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc7db-155">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc7db-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="fc7db-156">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="fc7db-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="fc7db-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="fc7db-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="fc7db-158">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="fc7db-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="fc7db-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc7db-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="fc7db-160">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fc7db-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc7db-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="fc7db-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="fc7db-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fc7db-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fc7db-163">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="fc7db-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fc7db-164">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc7db-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="fc7db-165">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fc7db-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fc7db-166">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc7db-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fc7db-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc7db-167">RELATED LINKS</span></span>


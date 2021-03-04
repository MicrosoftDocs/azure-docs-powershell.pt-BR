---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: e1fff88e6d591f7ffd3d7b602e8d60febf5b1c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888648"
---
# <span data-ttu-id="08757-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="08757-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="08757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08757-102">SYNOPSIS</span></span>
<span data-ttu-id="08757-103">Operação para excluir uma Implantação.</span><span class="sxs-lookup"><span data-stu-id="08757-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="08757-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="08757-104">SYNTAX</span></span>

### <span data-ttu-id="08757-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="08757-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="08757-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="08757-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08757-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="08757-107">DESCRIPTION</span></span>
<span data-ttu-id="08757-108">Operação para excluir uma Implantação.</span><span class="sxs-lookup"><span data-stu-id="08757-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="08757-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08757-109">EXAMPLES</span></span>

### <span data-ttu-id="08757-110">Exemplo 1: Remover a Implantação de Nuvem de Mola pelo nome.</span><span class="sxs-lookup"><span data-stu-id="08757-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="08757-111">Remova a Implantação da Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="08757-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="08757-112">Exemplo 2: Remover a Implantação de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="08757-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="08757-113">Remover a Implantação de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="08757-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="08757-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="08757-114">PARAMETERS</span></span>

### <span data-ttu-id="08757-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="08757-115">-AppName</span></span>
<span data-ttu-id="08757-116">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="08757-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="08757-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08757-117">-AsJob</span></span>
<span data-ttu-id="08757-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="08757-118">Run the command as a job</span></span>

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

### <span data-ttu-id="08757-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08757-119">-DefaultProfile</span></span>
<span data-ttu-id="08757-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08757-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08757-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08757-121">-InputObject</span></span>
<span data-ttu-id="08757-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="08757-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="08757-123">-Name</span><span class="sxs-lookup"><span data-stu-id="08757-123">-Name</span></span>
<span data-ttu-id="08757-124">O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="08757-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="08757-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="08757-125">-NoWait</span></span>
<span data-ttu-id="08757-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="08757-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="08757-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08757-127">-PassThru</span></span>
<span data-ttu-id="08757-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="08757-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="08757-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08757-129">-ResourceGroupName</span></span>
<span data-ttu-id="08757-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="08757-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="08757-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="08757-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="08757-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="08757-132">-ServiceName</span></span>
<span data-ttu-id="08757-133">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="08757-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="08757-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08757-134">-SubscriptionId</span></span>
<span data-ttu-id="08757-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08757-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="08757-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="08757-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="08757-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08757-137">-Confirm</span></span>
<span data-ttu-id="08757-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08757-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08757-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08757-139">-WhatIf</span></span>
<span data-ttu-id="08757-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08757-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08757-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08757-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08757-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08757-142">CommonParameters</span></span>
<span data-ttu-id="08757-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08757-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08757-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08757-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08757-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08757-145">INPUTS</span></span>

### <span data-ttu-id="08757-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="08757-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="08757-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="08757-147">OUTPUTS</span></span>

### <span data-ttu-id="08757-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="08757-148">System.Boolean</span></span>

## <span data-ttu-id="08757-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="08757-149">NOTES</span></span>

<span data-ttu-id="08757-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="08757-150">ALIASES</span></span>

<span data-ttu-id="08757-151">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="08757-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08757-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="08757-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08757-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08757-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08757-154">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="08757-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08757-155">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="08757-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="08757-156">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="08757-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="08757-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="08757-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="08757-158">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="08757-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="08757-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="08757-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="08757-160">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="08757-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08757-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="08757-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="08757-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="08757-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="08757-163">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="08757-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="08757-164">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="08757-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="08757-165">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08757-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="08757-166">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="08757-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="08757-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08757-167">RELATED LINKS</span></span>


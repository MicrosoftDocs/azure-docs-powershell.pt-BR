---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258133"
---
# <span data-ttu-id="cea33-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="cea33-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="cea33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cea33-102">SYNOPSIS</span></span>
<span data-ttu-id="cea33-103">Operação para excluir um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cea33-103">Operation to delete an App.</span></span>

## <span data-ttu-id="cea33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cea33-104">SYNTAX</span></span>

### <span data-ttu-id="cea33-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="cea33-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cea33-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cea33-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cea33-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cea33-107">DESCRIPTION</span></span>
<span data-ttu-id="cea33-108">Operação para excluir um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cea33-108">Operation to delete an App.</span></span>

## <span data-ttu-id="cea33-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cea33-109">EXAMPLES</span></span>

### <span data-ttu-id="cea33-110">Exemplo 1: remover o aplicativo de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="cea33-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="cea33-111">Remova o aplicativo Spring Cloud por nome.</span><span class="sxs-lookup"><span data-stu-id="cea33-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="cea33-112">Exemplo 2: remover o aplicativo de nuvem Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="cea33-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="cea33-113">Remova o aplicativo Spring Cloud do pipe.</span><span class="sxs-lookup"><span data-stu-id="cea33-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="cea33-114">OS</span><span class="sxs-lookup"><span data-stu-id="cea33-114">PARAMETERS</span></span>

### <span data-ttu-id="cea33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cea33-115">-AsJob</span></span>
<span data-ttu-id="cea33-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cea33-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cea33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea33-117">-DefaultProfile</span></span>
<span data-ttu-id="cea33-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cea33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea33-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cea33-119">-InputObject</span></span>
<span data-ttu-id="cea33-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cea33-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cea33-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cea33-121">-Name</span></span>
<span data-ttu-id="cea33-122">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cea33-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea33-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cea33-123">-NoWait</span></span>
<span data-ttu-id="cea33-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cea33-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cea33-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cea33-125">-PassThru</span></span>
<span data-ttu-id="cea33-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cea33-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cea33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea33-127">-ResourceGroupName</span></span>
<span data-ttu-id="cea33-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="cea33-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cea33-129">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="cea33-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cea33-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cea33-130">-ServiceName</span></span>
<span data-ttu-id="cea33-131">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="cea33-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="cea33-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cea33-132">-SubscriptionId</span></span>
<span data-ttu-id="cea33-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cea33-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cea33-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cea33-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cea33-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cea33-135">-Confirm</span></span>
<span data-ttu-id="cea33-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cea33-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea33-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea33-137">-WhatIf</span></span>
<span data-ttu-id="cea33-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cea33-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea33-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cea33-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea33-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea33-140">CommonParameters</span></span>
<span data-ttu-id="cea33-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea33-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea33-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cea33-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea33-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cea33-143">INPUTS</span></span>

### <span data-ttu-id="cea33-144">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="cea33-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cea33-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cea33-145">OUTPUTS</span></span>

### <span data-ttu-id="cea33-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cea33-146">System.Boolean</span></span>

## <span data-ttu-id="cea33-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cea33-147">NOTES</span></span>

<span data-ttu-id="cea33-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cea33-148">ALIASES</span></span>

<span data-ttu-id="cea33-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="cea33-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cea33-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cea33-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cea33-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cea33-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cea33-152">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="cea33-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cea33-153">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cea33-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cea33-154">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="cea33-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cea33-155">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="cea33-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cea33-156">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="cea33-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cea33-157">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="cea33-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cea33-158">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cea33-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cea33-159">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="cea33-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cea33-160">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="cea33-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cea33-161">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="cea33-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cea33-162">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="cea33-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cea33-163">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cea33-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cea33-164">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cea33-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cea33-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cea33-165">RELATED LINKS</span></span>


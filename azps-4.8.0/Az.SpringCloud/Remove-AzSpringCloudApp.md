---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113928"
---
# <span data-ttu-id="d8ce9-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d8ce9-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="d8ce9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ce9-103">Operação para excluir um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-103">Operation to delete an App.</span></span>

## <span data-ttu-id="d8ce9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8ce9-104">SYNTAX</span></span>

### <span data-ttu-id="d8ce9-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8ce9-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8ce9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8ce9-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8ce9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8ce9-107">DESCRIPTION</span></span>
<span data-ttu-id="d8ce9-108">Operação para excluir um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-108">Operation to delete an App.</span></span>

## <span data-ttu-id="d8ce9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8ce9-109">EXAMPLES</span></span>

### <span data-ttu-id="d8ce9-110">Exemplo 1: remover o aplicativo de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="d8ce9-111">Remova o aplicativo Spring Cloud por nome.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="d8ce9-112">Exemplo 2: remover o aplicativo de nuvem Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="d8ce9-113">Remova o aplicativo Spring Cloud do pipe.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="d8ce9-114">OS</span><span class="sxs-lookup"><span data-stu-id="d8ce9-114">PARAMETERS</span></span>

### <span data-ttu-id="d8ce9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ce9-115">-DefaultProfile</span></span>
<span data-ttu-id="d8ce9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ce9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8ce9-117">-InputObject</span></span>
<span data-ttu-id="d8ce9-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8ce9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8ce9-119">-Name</span></span>
<span data-ttu-id="d8ce9-120">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="d8ce9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8ce9-121">-PassThru</span></span>
<span data-ttu-id="d8ce9-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d8ce9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d8ce9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ce9-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8ce9-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d8ce9-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d8ce9-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8ce9-126">-ServiceName</span></span>
<span data-ttu-id="d8ce9-127">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d8ce9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8ce9-128">-SubscriptionId</span></span>
<span data-ttu-id="d8ce9-129">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8ce9-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8ce9-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8ce9-131">-Confirm</span></span>
<span data-ttu-id="d8ce9-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ce9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ce9-133">-WhatIf</span></span>
<span data-ttu-id="d8ce9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ce9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ce9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ce9-136">CommonParameters</span></span>
<span data-ttu-id="d8ce9-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ce9-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8ce9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ce9-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8ce9-139">INPUTS</span></span>

### <span data-ttu-id="d8ce9-140">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d8ce9-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d8ce9-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8ce9-141">OUTPUTS</span></span>

### <span data-ttu-id="d8ce9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ce9-142">System.Boolean</span></span>

## <span data-ttu-id="d8ce9-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8ce9-143">NOTES</span></span>

<span data-ttu-id="d8ce9-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8ce9-144">ALIASES</span></span>

<span data-ttu-id="d8ce9-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d8ce9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8ce9-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8ce9-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8ce9-148">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d8ce9-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8ce9-149">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d8ce9-150">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d8ce9-151">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d8ce9-152">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d8ce9-153">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d8ce9-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d8ce9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8ce9-155">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="d8ce9-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d8ce9-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8ce9-157">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8ce9-158">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d8ce9-159">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d8ce9-160">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8ce9-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d8ce9-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8ce9-161">RELATED LINKS</span></span>


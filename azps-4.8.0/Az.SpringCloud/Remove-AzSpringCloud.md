---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113929"
---
# <span data-ttu-id="2543b-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="2543b-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="2543b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2543b-102">SYNOPSIS</span></span>
<span data-ttu-id="2543b-103">Operação para excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="2543b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2543b-104">SYNTAX</span></span>

### <span data-ttu-id="2543b-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="2543b-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2543b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2543b-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2543b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2543b-107">DESCRIPTION</span></span>
<span data-ttu-id="2543b-108">Operação para excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="2543b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2543b-109">EXAMPLES</span></span>

### <span data-ttu-id="2543b-110">Exemplo 1: remover o serviço de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="2543b-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="2543b-111">Remova o serviço de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="2543b-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="2543b-112">Exemplo 2: remover o serviço de nuvem Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="2543b-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="2543b-113">Remova o serviço de nuvem Spring do pipe.</span><span class="sxs-lookup"><span data-stu-id="2543b-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="2543b-114">OS</span><span class="sxs-lookup"><span data-stu-id="2543b-114">PARAMETERS</span></span>

### <span data-ttu-id="2543b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2543b-115">-AsJob</span></span>
<span data-ttu-id="2543b-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2543b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2543b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2543b-117">-DefaultProfile</span></span>
<span data-ttu-id="2543b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2543b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2543b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2543b-119">-InputObject</span></span>
<span data-ttu-id="2543b-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2543b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2543b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2543b-121">-Name</span></span>
<span data-ttu-id="2543b-122">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2543b-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2543b-123">-NoWait</span></span>
<span data-ttu-id="2543b-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2543b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2543b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2543b-125">-PassThru</span></span>
<span data-ttu-id="2543b-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2543b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2543b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2543b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2543b-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2543b-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2543b-129">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2543b-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2543b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2543b-130">-SubscriptionId</span></span>
<span data-ttu-id="2543b-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2543b-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2543b-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2543b-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2543b-133">-Confirm</span></span>
<span data-ttu-id="2543b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2543b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2543b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2543b-135">-WhatIf</span></span>
<span data-ttu-id="2543b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2543b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2543b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2543b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2543b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2543b-138">CommonParameters</span></span>
<span data-ttu-id="2543b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2543b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2543b-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2543b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2543b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2543b-141">INPUTS</span></span>

### <span data-ttu-id="2543b-142">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2543b-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2543b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2543b-143">OUTPUTS</span></span>

### <span data-ttu-id="2543b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2543b-144">System.Boolean</span></span>

## <span data-ttu-id="2543b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2543b-145">NOTES</span></span>

<span data-ttu-id="2543b-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2543b-146">ALIASES</span></span>

<span data-ttu-id="2543b-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="2543b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2543b-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2543b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2543b-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2543b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2543b-150">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2543b-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2543b-151">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2543b-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2543b-152">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="2543b-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2543b-153">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="2543b-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2543b-154">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="2543b-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2543b-155">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2543b-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2543b-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2543b-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2543b-157">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="2543b-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2543b-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2543b-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2543b-159">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2543b-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2543b-160">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2543b-161">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2543b-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2543b-162">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2543b-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2543b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2543b-163">RELATED LINKS</span></span>


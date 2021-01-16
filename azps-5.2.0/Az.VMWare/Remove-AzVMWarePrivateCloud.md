---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260213"
---
# <span data-ttu-id="06548-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="06548-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="06548-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06548-102">SYNOPSIS</span></span>
<span data-ttu-id="06548-103">Excluir uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-103">Delete a private cloud</span></span>

## <span data-ttu-id="06548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06548-104">SYNTAX</span></span>

### <span data-ttu-id="06548-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="06548-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06548-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06548-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06548-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06548-107">DESCRIPTION</span></span>
<span data-ttu-id="06548-108">Excluir uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-108">Delete a private cloud</span></span>

## <span data-ttu-id="06548-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06548-109">EXAMPLES</span></span>

### <span data-ttu-id="06548-110">Exemplo 1: excluir nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="06548-111">Excluir nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-111">Delete private cloud</span></span>

## <span data-ttu-id="06548-112">OS</span><span class="sxs-lookup"><span data-stu-id="06548-112">PARAMETERS</span></span>

### <span data-ttu-id="06548-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06548-113">-AsJob</span></span>
<span data-ttu-id="06548-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="06548-114">Run the command as a job</span></span>

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

### <span data-ttu-id="06548-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06548-115">-DefaultProfile</span></span>
<span data-ttu-id="06548-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06548-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06548-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06548-117">-InputObject</span></span>
<span data-ttu-id="06548-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="06548-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06548-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="06548-119">-Name</span></span>
<span data-ttu-id="06548-120">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06548-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="06548-121">-NoWait</span></span>
<span data-ttu-id="06548-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="06548-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06548-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06548-123">-PassThru</span></span>
<span data-ttu-id="06548-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="06548-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06548-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06548-125">-ResourceGroupName</span></span>
<span data-ttu-id="06548-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06548-126">The name of the resource group.</span></span>
<span data-ttu-id="06548-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="06548-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="06548-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06548-128">-SubscriptionId</span></span>
<span data-ttu-id="06548-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="06548-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="06548-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06548-130">-Confirm</span></span>
<span data-ttu-id="06548-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06548-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06548-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06548-132">-WhatIf</span></span>
<span data-ttu-id="06548-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06548-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06548-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06548-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06548-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06548-135">CommonParameters</span></span>
<span data-ttu-id="06548-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06548-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06548-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06548-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06548-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06548-138">INPUTS</span></span>

### <span data-ttu-id="06548-139">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="06548-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="06548-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06548-140">OUTPUTS</span></span>

### <span data-ttu-id="06548-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06548-141">System.Boolean</span></span>

## <span data-ttu-id="06548-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06548-142">NOTES</span></span>

<span data-ttu-id="06548-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="06548-143">ALIASES</span></span>

<span data-ttu-id="06548-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="06548-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06548-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="06548-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06548-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06548-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06548-147">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="06548-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06548-148">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="06548-149">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="06548-150">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="06548-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="06548-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06548-152">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="06548-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="06548-153">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="06548-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="06548-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06548-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="06548-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="06548-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="06548-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="06548-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="06548-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06548-157">RELATED LINKS</span></span>


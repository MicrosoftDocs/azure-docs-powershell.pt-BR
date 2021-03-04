---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: 3feb6e2246e2265c36e67d64621a5726eaabb6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890465"
---
# <span data-ttu-id="6d421-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="6d421-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="6d421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d421-102">SYNOPSIS</span></span>
<span data-ttu-id="6d421-103">Operação para excluir um CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="6d421-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="6d421-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d421-104">SYNTAX</span></span>

### <span data-ttu-id="6d421-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d421-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d421-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d421-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d421-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d421-107">DESCRIPTION</span></span>
<span data-ttu-id="6d421-108">Operação para excluir um CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="6d421-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="6d421-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d421-109">EXAMPLES</span></span>

### <span data-ttu-id="6d421-110">Exemplo 1: Remover o recurso de Comunicação do Azure especificado</span><span class="sxs-lookup"><span data-stu-id="6d421-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="6d421-111">Remover/ excluir o recurso comunicação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d421-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="6d421-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d421-112">PARAMETERS</span></span>

### <span data-ttu-id="6d421-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d421-113">-AsJob</span></span>
<span data-ttu-id="6d421-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6d421-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6d421-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d421-115">-DefaultProfile</span></span>
<span data-ttu-id="6d421-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d421-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d421-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d421-117">-InputObject</span></span>
<span data-ttu-id="6d421-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6d421-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d421-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6d421-119">-Name</span></span>
<span data-ttu-id="6d421-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="6d421-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d421-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d421-121">-NoWait</span></span>
<span data-ttu-id="6d421-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6d421-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d421-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d421-123">-PassThru</span></span>
<span data-ttu-id="6d421-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6d421-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d421-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d421-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d421-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6d421-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d421-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="6d421-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d421-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d421-128">-SubscriptionId</span></span>
<span data-ttu-id="6d421-129">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d421-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d421-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d421-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d421-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d421-131">-Confirm</span></span>
<span data-ttu-id="6d421-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d421-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d421-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d421-133">-WhatIf</span></span>
<span data-ttu-id="6d421-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d421-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d421-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d421-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d421-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d421-136">CommonParameters</span></span>
<span data-ttu-id="6d421-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d421-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d421-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d421-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d421-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d421-139">INPUTS</span></span>

### <span data-ttu-id="6d421-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="6d421-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="6d421-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d421-141">OUTPUTS</span></span>

### <span data-ttu-id="6d421-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d421-142">System.Boolean</span></span>

## <span data-ttu-id="6d421-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d421-143">NOTES</span></span>

<span data-ttu-id="6d421-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6d421-144">ALIASES</span></span>

<span data-ttu-id="6d421-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6d421-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d421-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6d421-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d421-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d421-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d421-148">INPUTOBJECT <ICommunicationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6d421-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d421-149">`[CommunicationServiceName <String>]`: O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="6d421-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="6d421-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6d421-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d421-151">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="6d421-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="6d421-152">`[OperationId <String>]`: A ID de uma operação assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="6d421-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="6d421-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6d421-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6d421-154">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="6d421-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6d421-155">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d421-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="6d421-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d421-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d421-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d421-157">RELATED LINKS</span></span>


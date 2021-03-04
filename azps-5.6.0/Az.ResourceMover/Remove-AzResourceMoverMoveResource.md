---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891634"
---
# <span data-ttu-id="3a75f-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3a75f-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="3a75f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a75f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a75f-103">Exclui um Recurso de Movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="3a75f-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3a75f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a75f-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3a75f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a75f-105">DESCRIPTION</span></span>
<span data-ttu-id="3a75f-106">Exclui um Recurso de Movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="3a75f-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3a75f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a75f-107">EXAMPLES</span></span>

### <span data-ttu-id="3a75f-108">Exemplo 1: Remover um Move Rresource da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="3a75f-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="3a75f-109">Remova um Move Rresource da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="3a75f-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="3a75f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a75f-110">PARAMETERS</span></span>

### <span data-ttu-id="3a75f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a75f-111">-AsJob</span></span>
<span data-ttu-id="3a75f-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3a75f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3a75f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a75f-113">-DefaultProfile</span></span>
<span data-ttu-id="3a75f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a75f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a75f-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3a75f-115">-MoveCollectionName</span></span>
<span data-ttu-id="3a75f-116">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="3a75f-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3a75f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3a75f-117">-Name</span></span>
<span data-ttu-id="3a75f-118">O Nome do Recurso de Movimentação.</span><span class="sxs-lookup"><span data-stu-id="3a75f-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a75f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a75f-119">-NoWait</span></span>
<span data-ttu-id="3a75f-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3a75f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a75f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a75f-121">-PassThru</span></span>
<span data-ttu-id="3a75f-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3a75f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a75f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a75f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a75f-124">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3a75f-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3a75f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a75f-125">-SubscriptionId</span></span>
<span data-ttu-id="3a75f-126">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a75f-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="3a75f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a75f-127">-Confirm</span></span>
<span data-ttu-id="3a75f-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a75f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a75f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a75f-129">-WhatIf</span></span>
<span data-ttu-id="3a75f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a75f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a75f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a75f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a75f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a75f-132">CommonParameters</span></span>
<span data-ttu-id="3a75f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a75f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a75f-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a75f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a75f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a75f-135">INPUTS</span></span>

## <span data-ttu-id="3a75f-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a75f-136">OUTPUTS</span></span>

### <span data-ttu-id="3a75f-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3a75f-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="3a75f-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a75f-138">NOTES</span></span>

<span data-ttu-id="3a75f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3a75f-139">ALIASES</span></span>

## <span data-ttu-id="3a75f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a75f-140">RELATED LINKS</span></span>


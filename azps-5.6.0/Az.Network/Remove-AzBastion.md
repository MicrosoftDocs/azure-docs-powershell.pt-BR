---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: b58ffa98f3f35a8e8f87785e4d7abb703aa9b90e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888469"
---
# <span data-ttu-id="2f0bc-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2f0bc-101">Remove-AzBastion</span></span>

## <span data-ttu-id="2f0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0bc-103">Remove um recurso de bastião.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="2f0bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2f0bc-104">SYNTAX</span></span>

### <span data-ttu-id="2f0bc-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2f0bc-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0bc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f0bc-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0bc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0bc-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0bc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2f0bc-108">DESCRIPTION</span></span>
<span data-ttu-id="2f0bc-109">Remove um recurso de bastião. Example1 exclui o bastião usando resourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="2f0bc-110">O Exemplo2 exclui o bastião usando seu objeto com pipeline.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="2f0bc-111">O Exemplo3 exclui o bastião usando seu objeto.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="2f0bc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-112">EXAMPLES</span></span>

### <span data-ttu-id="2f0bc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f0bc-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="2f0bc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f0bc-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="2f0bc-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2f0bc-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="2f0bc-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-116">PARAMETERS</span></span>

### <span data-ttu-id="2f0bc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f0bc-117">-Confirm</span></span>
<span data-ttu-id="2f0bc-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0bc-119">-DefaultProfile</span></span>
<span data-ttu-id="2f0bc-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2f0bc-121">-Force</span></span>
<span data-ttu-id="2f0bc-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-122">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f0bc-123">-InputObject</span></span>
<span data-ttu-id="2f0bc-124">O objeto Bastion a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2f0bc-125">-Name</span></span>
<span data-ttu-id="2f0bc-126">O nome do recurso de bastião a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f0bc-127">-PassThru</span></span>
<span data-ttu-id="2f0bc-128">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0bc-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f0bc-130">O nome do grupo de recursos onde existe bastião.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0bc-131">-ResourceId</span></span>
<span data-ttu-id="2f0bc-132">A ID de recurso do Azure para o Bastion a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0bc-133">-WhatIf</span></span>
<span data-ttu-id="2f0bc-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0bc-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0bc-136">CommonParameters</span></span>
<span data-ttu-id="2f0bc-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0bc-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f0bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0bc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-139">INPUTS</span></span>

### <span data-ttu-id="2f0bc-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="2f0bc-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="2f0bc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2f0bc-141">System.String</span></span>

## <span data-ttu-id="2f0bc-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-142">OUTPUTS</span></span>

### <span data-ttu-id="2f0bc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f0bc-143">System.Boolean</span></span>

## <span data-ttu-id="2f0bc-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="2f0bc-144">NOTES</span></span>

## <span data-ttu-id="2f0bc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f0bc-145">RELATED LINKS</span></span>
[<span data-ttu-id="2f0bc-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2f0bc-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="2f0bc-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2f0bc-147">New-AzBastion</span></span>](./New-AzBastion.md)
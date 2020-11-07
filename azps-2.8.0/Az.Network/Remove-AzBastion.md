---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 3041e69903eaac7a748aff52c83e2e994fae22f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772296"
---
# <span data-ttu-id="5eb8b-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5eb8b-101">Remove-AzBastion</span></span>

## <span data-ttu-id="5eb8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb8b-103">Remove um recurso bastião.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="5eb8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eb8b-104">SYNTAX</span></span>

### <span data-ttu-id="5eb8b-105">ByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb8b-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb8b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5eb8b-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb8b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5eb8b-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb8b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5eb8b-108">DESCRIPTION</span></span>
<span data-ttu-id="5eb8b-109">Remove um recurso bastião. Example1 exclui a bastião usando seu ResourceGroupName e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="5eb8b-110">Example2 exclui a Bastion que usa seu objeto com pipeline.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="5eb8b-111">Example3 exclui a Bastion que usa o objeto.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="5eb8b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eb8b-112">EXAMPLES</span></span>

### <span data-ttu-id="5eb8b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5eb8b-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="5eb8b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5eb8b-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="5eb8b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5eb8b-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="5eb8b-116">OS</span><span class="sxs-lookup"><span data-stu-id="5eb8b-116">PARAMETERS</span></span>

### <span data-ttu-id="5eb8b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5eb8b-117">-Confirm</span></span>
<span data-ttu-id="5eb8b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb8b-119">-DefaultProfile</span></span>
<span data-ttu-id="5eb8b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb8b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5eb8b-121">-Force</span></span>
<span data-ttu-id="5eb8b-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5eb8b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb8b-123">-InputObject</span></span>
<span data-ttu-id="5eb8b-124">O objeto bastião a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="5eb8b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eb8b-125">-Name</span></span>
<span data-ttu-id="5eb8b-126">O nome do recurso bastião a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="5eb8b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5eb8b-127">-PassThru</span></span>
<span data-ttu-id="5eb8b-128">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="5eb8b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb8b-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eb8b-130">O nome do grupo de recursos no qual a bastião existe.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="5eb8b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5eb8b-131">-ResourceId</span></span>
<span data-ttu-id="5eb8b-132">A ID de recurso do Azure para a Bastion ser excluída.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="5eb8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb8b-133">-WhatIf</span></span>
<span data-ttu-id="5eb8b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb8b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb8b-136">CommonParameters</span></span>
<span data-ttu-id="5eb8b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb8b-138">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eb8b-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb8b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5eb8b-139">INPUTS</span></span>

### <span data-ttu-id="5eb8b-140">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="5eb8b-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="5eb8b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5eb8b-141">System.String</span></span>

## <span data-ttu-id="5eb8b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5eb8b-142">OUTPUTS</span></span>

### <span data-ttu-id="5eb8b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5eb8b-143">System.Boolean</span></span>

## <span data-ttu-id="5eb8b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5eb8b-144">NOTES</span></span>

## <span data-ttu-id="5eb8b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb8b-145">RELATED LINKS</span></span>
[<span data-ttu-id="5eb8b-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5eb8b-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="5eb8b-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="5eb8b-147">New-AzBastion</span></span>](./New-AzBastion.md)
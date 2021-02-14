---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117350"
---
# <span data-ttu-id="2faf9-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2faf9-101">Remove-AzBastion</span></span>

## <span data-ttu-id="2faf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2faf9-102">SYNOPSIS</span></span>
<span data-ttu-id="2faf9-103">Remove um recurso de balões.</span><span class="sxs-lookup"><span data-stu-id="2faf9-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="2faf9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2faf9-104">SYNTAX</span></span>

### <span data-ttu-id="2faf9-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2faf9-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2faf9-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2faf9-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2faf9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2faf9-108">DESCRIPTION</span></span>
<span data-ttu-id="2faf9-109">Remove um recurso de balões. O exemplo1 exclui a balbúria usando o NomedoArmanadoDoAr e o NomedoPro recursos.</span><span class="sxs-lookup"><span data-stu-id="2faf9-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="2faf9-110">Exemplo2 exclui a balões usando seu objeto com pipeline.</span><span class="sxs-lookup"><span data-stu-id="2faf9-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="2faf9-111">O exemplo3 exclui a balões usando seu objeto.</span><span class="sxs-lookup"><span data-stu-id="2faf9-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="2faf9-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2faf9-112">EXAMPLES</span></span>

### <span data-ttu-id="2faf9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2faf9-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="2faf9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2faf9-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="2faf9-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2faf9-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="2faf9-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2faf9-116">PARAMETERS</span></span>

### <span data-ttu-id="2faf9-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2faf9-117">-Confirm</span></span>
<span data-ttu-id="2faf9-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2faf9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2faf9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2faf9-119">-DefaultProfile</span></span>
<span data-ttu-id="2faf9-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2faf9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2faf9-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2faf9-121">-Force</span></span>
<span data-ttu-id="2faf9-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2faf9-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2faf9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2faf9-123">-InputObject</span></span>
<span data-ttu-id="2faf9-124">O objeto Bastion a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2faf9-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="2faf9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2faf9-125">-Name</span></span>
<span data-ttu-id="2faf9-126">O nome do recurso de rescisão a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2faf9-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="2faf9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2faf9-127">-PassThru</span></span>
<span data-ttu-id="2faf9-128">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="2faf9-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2faf9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faf9-129">-ResourceGroupName</span></span>
<span data-ttu-id="2faf9-130">O nome do grupo de recursos onde existe a balbúria.</span><span class="sxs-lookup"><span data-stu-id="2faf9-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="2faf9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2faf9-131">-ResourceId</span></span>
<span data-ttu-id="2faf9-132">A ID de recurso do Azure para a Bastião ser excluída.</span><span class="sxs-lookup"><span data-stu-id="2faf9-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="2faf9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2faf9-133">-WhatIf</span></span>
<span data-ttu-id="2faf9-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2faf9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2faf9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2faf9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2faf9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2faf9-136">CommonParameters</span></span>
<span data-ttu-id="2faf9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2faf9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2faf9-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2faf9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2faf9-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="2faf9-139">INPUTS</span></span>

### <span data-ttu-id="2faf9-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="2faf9-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="2faf9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2faf9-141">System.String</span></span>

## <span data-ttu-id="2faf9-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="2faf9-142">OUTPUTS</span></span>

### <span data-ttu-id="2faf9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2faf9-143">System.Boolean</span></span>

## <span data-ttu-id="2faf9-144">Notas</span><span class="sxs-lookup"><span data-stu-id="2faf9-144">NOTES</span></span>

## <span data-ttu-id="2faf9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2faf9-145">RELATED LINKS</span></span>
[<span data-ttu-id="2faf9-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2faf9-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="2faf9-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2faf9-147">New-AzBastion</span></span>](./New-AzBastion.md)
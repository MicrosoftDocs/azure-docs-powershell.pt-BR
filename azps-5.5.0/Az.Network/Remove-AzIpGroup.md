---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115095"
---
# <span data-ttu-id="f9d28-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9d28-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="f9d28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9d28-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d28-103">Exclui um Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="f9d28-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="f9d28-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9d28-104">SYNTAX</span></span>

### <span data-ttu-id="f9d28-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d28-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d28-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d28-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d28-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d28-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d28-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9d28-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d28-109">O **cmdlet Remove-AzIpGroup** exclui um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="f9d28-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="f9d28-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9d28-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d28-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9d28-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="f9d28-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f9d28-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="f9d28-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f9d28-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="f9d28-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9d28-114">PARAMETERS</span></span>

### <span data-ttu-id="f9d28-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9d28-115">-AsJob</span></span>
<span data-ttu-id="f9d28-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f9d28-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9d28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d28-117">-DefaultProfile</span></span>
<span data-ttu-id="f9d28-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d28-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f9d28-119">-Force</span></span>
<span data-ttu-id="f9d28-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="f9d28-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f9d28-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="f9d28-121">-IpGroup</span></span>
<span data-ttu-id="f9d28-122">O objeto de entrada ipGroup.</span><span class="sxs-lookup"><span data-stu-id="f9d28-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d28-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9d28-123">-Name</span></span>
<span data-ttu-id="f9d28-124">O nome do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="f9d28-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d28-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9d28-125">-PassThru</span></span>
<span data-ttu-id="f9d28-126">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="f9d28-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="f9d28-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d28-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9d28-128">O nome do grupo de recursos do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="f9d28-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d28-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d28-129">-ResourceId</span></span>
<span data-ttu-id="f9d28-130">A ID do recurso ipgroup.</span><span class="sxs-lookup"><span data-stu-id="f9d28-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d28-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f9d28-131">-Confirm</span></span>
<span data-ttu-id="f9d28-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d28-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d28-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d28-133">-WhatIf</span></span>
<span data-ttu-id="f9d28-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f9d28-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d28-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9d28-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d28-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d28-136">CommonParameters</span></span>
<span data-ttu-id="f9d28-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d28-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d28-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9d28-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d28-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9d28-139">INPUTS</span></span>

### <span data-ttu-id="f9d28-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d28-140">System.String</span></span>

### <span data-ttu-id="f9d28-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9d28-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f9d28-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9d28-142">OUTPUTS</span></span>

### <span data-ttu-id="f9d28-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9d28-143">System.Boolean</span></span>

## <span data-ttu-id="f9d28-144">Notas</span><span class="sxs-lookup"><span data-stu-id="f9d28-144">NOTES</span></span>

## <span data-ttu-id="f9d28-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9d28-145">RELATED LINKS</span></span>

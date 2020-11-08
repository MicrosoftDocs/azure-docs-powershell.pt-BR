---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116084"
---
# <span data-ttu-id="fe3b6-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe3b6-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="fe3b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe3b6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3b6-103">Exclui um IpGroup do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="fe3b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe3b6-104">SYNTAX</span></span>

### <span data-ttu-id="fe3b6-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b6-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b6-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b6-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b6-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b6-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3b6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe3b6-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3b6-109">O cmdlet **Remove-AzIpGroup** exclui um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="fe3b6-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="fe3b6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe3b6-110">EXAMPLES</span></span>

### <span data-ttu-id="fe3b6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe3b6-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="fe3b6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fe3b6-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="fe3b6-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fe3b6-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="fe3b6-114">OS</span><span class="sxs-lookup"><span data-stu-id="fe3b6-114">PARAMETERS</span></span>

### <span data-ttu-id="fe3b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe3b6-115">-AsJob</span></span>
<span data-ttu-id="fe3b6-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fe3b6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe3b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3b6-117">-DefaultProfile</span></span>
<span data-ttu-id="fe3b6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3b6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fe3b6-119">-Force</span></span>
<span data-ttu-id="fe3b6-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="fe3b6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fe3b6-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="fe3b6-121">-IpGroup</span></span>
<span data-ttu-id="fe3b6-122">O objeto de entrada ipGroup.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="fe3b6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe3b6-123">-Name</span></span>
<span data-ttu-id="fe3b6-124">O nome do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="fe3b6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe3b6-125">-PassThru</span></span>
<span data-ttu-id="fe3b6-126">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="fe3b6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3b6-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe3b6-128">O nome do grupo de recursos do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="fe3b6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3b6-129">-ResourceId</span></span>
<span data-ttu-id="fe3b6-130">A ID do recurso ipgroup.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="fe3b6-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe3b6-131">-Confirm</span></span>
<span data-ttu-id="fe3b6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3b6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3b6-133">-WhatIf</span></span>
<span data-ttu-id="fe3b6-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3b6-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3b6-136">CommonParameters</span></span>
<span data-ttu-id="fe3b6-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3b6-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe3b6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3b6-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe3b6-139">INPUTS</span></span>

### <span data-ttu-id="fe3b6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fe3b6-140">System.String</span></span>

### <span data-ttu-id="fe3b6-141">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe3b6-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fe3b6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe3b6-142">OUTPUTS</span></span>

### <span data-ttu-id="fe3b6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe3b6-143">System.Boolean</span></span>

## <span data-ttu-id="fe3b6-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe3b6-144">NOTES</span></span>

## <span data-ttu-id="fe3b6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe3b6-145">RELATED LINKS</span></span>

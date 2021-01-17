---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428930"
---
# <span data-ttu-id="31155-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31155-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="31155-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31155-102">SYNOPSIS</span></span>
<span data-ttu-id="31155-103">Exclui um IpGroup do Azure.</span><span class="sxs-lookup"><span data-stu-id="31155-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="31155-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31155-104">SYNTAX</span></span>

### <span data-ttu-id="31155-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31155-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31155-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31155-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31155-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31155-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31155-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31155-108">DESCRIPTION</span></span>
<span data-ttu-id="31155-109">O cmdlet **Remove-AzIpGroup** exclui um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="31155-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="31155-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31155-110">EXAMPLES</span></span>

### <span data-ttu-id="31155-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31155-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="31155-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="31155-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="31155-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="31155-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="31155-114">OS</span><span class="sxs-lookup"><span data-stu-id="31155-114">PARAMETERS</span></span>

### <span data-ttu-id="31155-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31155-115">-AsJob</span></span>
<span data-ttu-id="31155-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="31155-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31155-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31155-117">-DefaultProfile</span></span>
<span data-ttu-id="31155-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31155-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31155-119">-Force</span><span class="sxs-lookup"><span data-stu-id="31155-119">-Force</span></span>
<span data-ttu-id="31155-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="31155-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="31155-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="31155-121">-IpGroup</span></span>
<span data-ttu-id="31155-122">O objeto de entrada ipGroup.</span><span class="sxs-lookup"><span data-stu-id="31155-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="31155-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="31155-123">-Name</span></span>
<span data-ttu-id="31155-124">O nome do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="31155-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="31155-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31155-125">-PassThru</span></span>
<span data-ttu-id="31155-126">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="31155-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="31155-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31155-127">-ResourceGroupName</span></span>
<span data-ttu-id="31155-128">O nome do grupo de recursos do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="31155-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="31155-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31155-129">-ResourceId</span></span>
<span data-ttu-id="31155-130">A ID do recurso ipgroup.</span><span class="sxs-lookup"><span data-stu-id="31155-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="31155-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31155-131">-Confirm</span></span>
<span data-ttu-id="31155-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31155-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31155-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31155-133">-WhatIf</span></span>
<span data-ttu-id="31155-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31155-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31155-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31155-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31155-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31155-136">CommonParameters</span></span>
<span data-ttu-id="31155-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31155-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31155-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31155-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31155-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31155-139">INPUTS</span></span>

### <span data-ttu-id="31155-140">System. String</span><span class="sxs-lookup"><span data-stu-id="31155-140">System.String</span></span>

### <span data-ttu-id="31155-141">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="31155-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="31155-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31155-142">OUTPUTS</span></span>

### <span data-ttu-id="31155-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31155-143">System.Boolean</span></span>

## <span data-ttu-id="31155-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31155-144">NOTES</span></span>

## <span data-ttu-id="31155-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31155-145">RELATED LINKS</span></span>

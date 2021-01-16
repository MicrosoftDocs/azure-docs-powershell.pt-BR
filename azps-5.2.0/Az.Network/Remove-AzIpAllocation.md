---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263120"
---
# <span data-ttu-id="0f92d-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0f92d-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="0f92d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f92d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f92d-103">Exclui um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f92d-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="0f92d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f92d-104">SYNTAX</span></span>

### <span data-ttu-id="0f92d-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f92d-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f92d-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f92d-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f92d-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f92d-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f92d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f92d-108">DESCRIPTION</span></span>
<span data-ttu-id="0f92d-109">O cmdlet **Remove-AzIpAllocation** exclui um Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="0f92d-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="0f92d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f92d-110">EXAMPLES</span></span>

### <span data-ttu-id="0f92d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f92d-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="0f92d-112">OS</span><span class="sxs-lookup"><span data-stu-id="0f92d-112">PARAMETERS</span></span>

### <span data-ttu-id="0f92d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f92d-113">-AsJob</span></span>
<span data-ttu-id="0f92d-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f92d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f92d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f92d-115">-DefaultProfile</span></span>
<span data-ttu-id="0f92d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f92d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f92d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f92d-117">-Force</span></span>
<span data-ttu-id="0f92d-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0f92d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0f92d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f92d-119">-InputObject</span></span>
<span data-ttu-id="0f92d-120">{{Fillobject descrição da entrada}}</span><span class="sxs-lookup"><span data-stu-id="0f92d-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f92d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f92d-121">-Name</span></span>
<span data-ttu-id="0f92d-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f92d-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f92d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f92d-123">-PassThru</span></span>
<span data-ttu-id="0f92d-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0f92d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f92d-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0f92d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f92d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f92d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0f92d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f92d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f92d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f92d-128">-ResourceId</span></span>
<span data-ttu-id="0f92d-129">IpAllocation ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f92d-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f92d-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f92d-130">-Confirm</span></span>
<span data-ttu-id="0f92d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f92d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f92d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f92d-132">-WhatIf</span></span>
<span data-ttu-id="0f92d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f92d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f92d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f92d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f92d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f92d-135">CommonParameters</span></span>
<span data-ttu-id="0f92d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f92d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f92d-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f92d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f92d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f92d-138">INPUTS</span></span>

### <span data-ttu-id="0f92d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0f92d-139">System.String</span></span>

## <span data-ttu-id="0f92d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f92d-140">OUTPUTS</span></span>

### <span data-ttu-id="0f92d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f92d-141">System.Boolean</span></span>

## <span data-ttu-id="0f92d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f92d-142">NOTES</span></span>

## <span data-ttu-id="0f92d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f92d-143">RELATED LINKS</span></span>

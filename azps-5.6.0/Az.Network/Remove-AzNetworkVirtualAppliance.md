---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891125"
---
# <span data-ttu-id="89562-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="89562-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="89562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89562-102">SYNOPSIS</span></span>
<span data-ttu-id="89562-103">Remover um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="89562-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="89562-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="89562-104">SYNTAX</span></span>

### <span data-ttu-id="89562-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="89562-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89562-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89562-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89562-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89562-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89562-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="89562-108">DESCRIPTION</span></span>
<span data-ttu-id="89562-109">O Remove-AzNetworkVirtualAppliance o comando remove um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="89562-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="89562-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89562-110">EXAMPLES</span></span>

### <span data-ttu-id="89562-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89562-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="89562-112">Excluir um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="89562-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="89562-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="89562-113">PARAMETERS</span></span>

### <span data-ttu-id="89562-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89562-114">-AsJob</span></span>
<span data-ttu-id="89562-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89562-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89562-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89562-116">-DefaultProfile</span></span>
<span data-ttu-id="89562-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89562-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89562-118">-Force</span><span class="sxs-lookup"><span data-stu-id="89562-118">-Force</span></span>
<span data-ttu-id="89562-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="89562-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="89562-120">-Name</span><span class="sxs-lookup"><span data-stu-id="89562-120">-Name</span></span>
<span data-ttu-id="89562-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="89562-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89562-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="89562-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="89562-123">O objeto resource.</span><span class="sxs-lookup"><span data-stu-id="89562-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89562-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89562-124">-PassThru</span></span>
<span data-ttu-id="89562-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="89562-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="89562-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="89562-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89562-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89562-127">-ResourceGroupName</span></span>
<span data-ttu-id="89562-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89562-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89562-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89562-129">-ResourceId</span></span>
<span data-ttu-id="89562-130">A ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="89562-130">The Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89562-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89562-131">-Confirm</span></span>
<span data-ttu-id="89562-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89562-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89562-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89562-133">-WhatIf</span></span>
<span data-ttu-id="89562-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89562-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89562-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89562-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89562-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89562-136">CommonParameters</span></span>
<span data-ttu-id="89562-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89562-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89562-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89562-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89562-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89562-139">INPUTS</span></span>

### <span data-ttu-id="89562-140">System.String</span><span class="sxs-lookup"><span data-stu-id="89562-140">System.String</span></span>

### <span data-ttu-id="89562-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="89562-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="89562-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="89562-142">OUTPUTS</span></span>

### <span data-ttu-id="89562-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89562-143">System.Boolean</span></span>

## <span data-ttu-id="89562-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="89562-144">NOTES</span></span>

## <span data-ttu-id="89562-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89562-145">RELATED LINKS</span></span>

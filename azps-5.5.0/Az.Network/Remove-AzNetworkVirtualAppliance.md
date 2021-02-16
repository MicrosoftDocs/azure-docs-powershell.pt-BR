---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113453"
---
# <span data-ttu-id="76167-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="76167-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="76167-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76167-102">SYNOPSIS</span></span>
<span data-ttu-id="76167-103">Remover um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="76167-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="76167-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76167-104">SYNTAX</span></span>

### <span data-ttu-id="76167-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76167-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76167-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76167-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76167-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76167-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76167-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="76167-108">DESCRIPTION</span></span>
<span data-ttu-id="76167-109">O comando Remove-AzNetworkVirtualAppliance remove um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="76167-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="76167-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76167-110">EXAMPLES</span></span>

### <span data-ttu-id="76167-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76167-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="76167-112">Excluir um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="76167-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="76167-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76167-113">PARAMETERS</span></span>

### <span data-ttu-id="76167-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76167-114">-AsJob</span></span>
<span data-ttu-id="76167-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76167-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76167-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76167-116">-DefaultProfile</span></span>
<span data-ttu-id="76167-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76167-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76167-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="76167-118">-Force</span></span>
<span data-ttu-id="76167-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="76167-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="76167-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="76167-120">-Name</span></span>
<span data-ttu-id="76167-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="76167-121">The resource name.</span></span>

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

### <span data-ttu-id="76167-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="76167-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="76167-123">O objeto de recurso.</span><span class="sxs-lookup"><span data-stu-id="76167-123">The resource object.</span></span>

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

### <span data-ttu-id="76167-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76167-124">-PassThru</span></span>
<span data-ttu-id="76167-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="76167-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="76167-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="76167-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76167-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76167-127">-ResourceGroupName</span></span>
<span data-ttu-id="76167-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76167-128">The resource group name.</span></span>

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

### <span data-ttu-id="76167-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76167-129">-ResourceId</span></span>
<span data-ttu-id="76167-130">A ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="76167-130">The Resource Id.</span></span>

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

### <span data-ttu-id="76167-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76167-131">-Confirm</span></span>
<span data-ttu-id="76167-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76167-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76167-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76167-133">-WhatIf</span></span>
<span data-ttu-id="76167-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76167-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76167-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76167-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76167-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76167-136">CommonParameters</span></span>
<span data-ttu-id="76167-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76167-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76167-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76167-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76167-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="76167-139">INPUTS</span></span>

### <span data-ttu-id="76167-140">System.String</span><span class="sxs-lookup"><span data-stu-id="76167-140">System.String</span></span>

### <span data-ttu-id="76167-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="76167-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="76167-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="76167-142">OUTPUTS</span></span>

### <span data-ttu-id="76167-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76167-143">System.Boolean</span></span>

## <span data-ttu-id="76167-144">Notas</span><span class="sxs-lookup"><span data-stu-id="76167-144">NOTES</span></span>

## <span data-ttu-id="76167-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76167-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116884"
---
# <span data-ttu-id="cf16f-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cf16f-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cf16f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf16f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf16f-103">Remova um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="cf16f-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf16f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf16f-104">SYNTAX</span></span>

### <span data-ttu-id="cf16f-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf16f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf16f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf16f-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf16f-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf16f-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf16f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf16f-108">DESCRIPTION</span></span>
<span data-ttu-id="cf16f-109">O comando Remove-AzNetworkVirtualAppliance remove um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="cf16f-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf16f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf16f-110">EXAMPLES</span></span>

### <span data-ttu-id="cf16f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf16f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="cf16f-112">Exclua um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="cf16f-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf16f-113">OS</span><span class="sxs-lookup"><span data-stu-id="cf16f-113">PARAMETERS</span></span>

### <span data-ttu-id="cf16f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf16f-114">-AsJob</span></span>
<span data-ttu-id="cf16f-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cf16f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf16f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf16f-116">-DefaultProfile</span></span>
<span data-ttu-id="cf16f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf16f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf16f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cf16f-118">-Force</span></span>
<span data-ttu-id="cf16f-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="cf16f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf16f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf16f-120">-Name</span></span>
<span data-ttu-id="cf16f-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf16f-121">The resource name.</span></span>

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

### <span data-ttu-id="cf16f-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cf16f-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="cf16f-123">O objeto de recurso.</span><span class="sxs-lookup"><span data-stu-id="cf16f-123">The resource object.</span></span>

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

### <span data-ttu-id="cf16f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf16f-124">-PassThru</span></span>
<span data-ttu-id="cf16f-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cf16f-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cf16f-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cf16f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf16f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf16f-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf16f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf16f-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf16f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf16f-129">-ResourceId</span></span>
<span data-ttu-id="cf16f-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf16f-130">The Resource Id.</span></span>

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

### <span data-ttu-id="cf16f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf16f-131">-Confirm</span></span>
<span data-ttu-id="cf16f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf16f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf16f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf16f-133">-WhatIf</span></span>
<span data-ttu-id="cf16f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf16f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf16f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf16f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf16f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf16f-136">CommonParameters</span></span>
<span data-ttu-id="cf16f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf16f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf16f-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf16f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf16f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf16f-139">INPUTS</span></span>

### <span data-ttu-id="cf16f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cf16f-140">System.String</span></span>

### <span data-ttu-id="cf16f-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cf16f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cf16f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf16f-142">OUTPUTS</span></span>

### <span data-ttu-id="cf16f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf16f-143">System.Boolean</span></span>

## <span data-ttu-id="cf16f-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf16f-144">NOTES</span></span>

## <span data-ttu-id="cf16f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf16f-145">RELATED LINKS</span></span>

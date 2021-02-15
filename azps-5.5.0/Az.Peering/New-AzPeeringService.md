---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111509"
---
# <span data-ttu-id="3a016-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="3a016-101">New-AzPeeringService</span></span>

## <span data-ttu-id="3a016-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a016-102">SYNOPSIS</span></span>
<span data-ttu-id="3a016-103">Cria um novo serviço de paridade.</span><span class="sxs-lookup"><span data-stu-id="3a016-103">Creates a new peering service.</span></span>

## <span data-ttu-id="3a016-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a016-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a016-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a016-105">DESCRIPTION</span></span>
<span data-ttu-id="3a016-106">Cria serviço de paridade.</span><span class="sxs-lookup"><span data-stu-id="3a016-106">Creates peering service.</span></span>

## <span data-ttu-id="3a016-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a016-107">EXAMPLES</span></span>

### <span data-ttu-id="3a016-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a016-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="3a016-109">Cria um objeto de serviço de paração com o provedor e o local de peering.</span><span class="sxs-lookup"><span data-stu-id="3a016-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="3a016-110">Usar em conjuração com `Get-AzPeeringServiceProvider` e `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="3a016-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="3a016-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a016-111">PARAMETERS</span></span>

### <span data-ttu-id="3a016-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a016-112">-AsJob</span></span>
<span data-ttu-id="3a016-113">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3a016-113">Run in the background.</span></span>

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

### <span data-ttu-id="3a016-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a016-114">-DefaultProfile</span></span>
<span data-ttu-id="3a016-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a016-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a016-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a016-116">-Name</span></span>
<span data-ttu-id="3a016-117">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3a016-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a016-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3a016-118">-PeeringLocation</span></span>
<span data-ttu-id="3a016-119">A Localização Física Diferente da Região do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a016-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="3a016-120">Use Get-AzPeeringServiceLocation [-País] <country></span><span class="sxs-lookup"><span data-stu-id="3a016-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a016-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3a016-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="3a016-122">O nome do provedor de serviços de paração.</span><span class="sxs-lookup"><span data-stu-id="3a016-122">The peering service provider name.</span></span>
<span data-ttu-id="3a016-123">Usar Get-AzPeeringServiceProvider cmdlet para uma lista</span><span class="sxs-lookup"><span data-stu-id="3a016-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a016-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a016-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a016-125">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="3a016-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a016-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a016-126">-Tag</span></span>
<span data-ttu-id="3a016-127">As marcas a associar ao Serviço InputObject da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a016-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a016-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3a016-128">-Confirm</span></span>
<span data-ttu-id="3a016-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a016-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a016-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a016-130">-WhatIf</span></span>
<span data-ttu-id="3a016-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3a016-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a016-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a016-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a016-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a016-133">CommonParameters</span></span>
<span data-ttu-id="3a016-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a016-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a016-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a016-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a016-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3a016-136">INPUTS</span></span>

### <span data-ttu-id="3a016-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3a016-137">None</span></span>

## <span data-ttu-id="3a016-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="3a016-138">OUTPUTS</span></span>

### <span data-ttu-id="3a016-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="3a016-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="3a016-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3a016-140">NOTES</span></span>

## <span data-ttu-id="3a016-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a016-141">RELATED LINKS</span></span>

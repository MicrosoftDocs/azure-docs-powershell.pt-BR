---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 24fcfc222d9d3cab1b0785c121e09b596aae16fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890141"
---
# <span data-ttu-id="5eee4-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5eee4-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="5eee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eee4-102">SYNOPSIS</span></span>
<span data-ttu-id="5eee4-103">Cria um novo prefixo de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="5eee4-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="5eee4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5eee4-104">SYNTAX</span></span>

### <span data-ttu-id="5eee4-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eee4-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eee4-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eee4-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eee4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5eee4-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eee4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5eee4-108">DESCRIPTION</span></span>
<span data-ttu-id="5eee4-109">Cria prefixo de serviço de paração associado a um objeto de serviço de paração.</span><span class="sxs-lookup"><span data-stu-id="5eee4-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="5eee4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eee4-110">EXAMPLES</span></span>

### <span data-ttu-id="5eee4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5eee4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5eee4-112">Cria um prefixo de um objeto de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="5eee4-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="5eee4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5eee4-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5eee4-114">Cria um prefixo a partir de uma id de recurso de serviço de paração.</span><span class="sxs-lookup"><span data-stu-id="5eee4-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="5eee4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5eee4-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5eee4-116">Cria um prefixo a partir de um nome e nome de grupo de recursos de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="5eee4-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="5eee4-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5eee4-117">PARAMETERS</span></span>

### <span data-ttu-id="5eee4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eee4-118">-AsJob</span></span>
<span data-ttu-id="5eee4-119">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5eee4-119">Run in the background.</span></span>

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

### <span data-ttu-id="5eee4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eee4-120">-DefaultProfile</span></span>
<span data-ttu-id="5eee4-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eee4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eee4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5eee4-122">-Name</span></span>
<span data-ttu-id="5eee4-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5eee4-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5eee4-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="5eee4-124">-PeeringServiceId</span></span>
<span data-ttu-id="5eee4-125">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="5eee4-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="5eee4-126">-PeeringServiceName</span></span>
<span data-ttu-id="5eee4-127">O nome do serviço de paração.</span><span class="sxs-lookup"><span data-stu-id="5eee4-127">The peering service name.</span></span>
<span data-ttu-id="5eee4-128">Use New-AzPeeringService cmdlet para um novo serviço de Get-AzPeeringService para uma lista.</span><span class="sxs-lookup"><span data-stu-id="5eee4-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="5eee4-129">-PeeringServiceObject</span></span>
<span data-ttu-id="5eee4-130">Usar um Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="5eee4-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5eee4-131">-Prefix</span></span>
<span data-ttu-id="5eee4-132">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="5eee4-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eee4-133">-ResourceGroupName</span></span>
<span data-ttu-id="5eee4-134">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="5eee4-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="5eee4-135">-ServiceKey</span></span>
<span data-ttu-id="5eee4-136">Este é um GUID exclusivo fornecido pelo provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="5eee4-136">This is a unique GUID provided by your service provider</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eee4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5eee4-137">-Confirm</span></span>
<span data-ttu-id="5eee4-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eee4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eee4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eee4-139">-WhatIf</span></span>
<span data-ttu-id="5eee4-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5eee4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eee4-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5eee4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eee4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eee4-142">CommonParameters</span></span>
<span data-ttu-id="5eee4-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eee4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eee4-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eee4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eee4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eee4-145">INPUTS</span></span>

### <span data-ttu-id="5eee4-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="5eee4-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="5eee4-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5eee4-147">OUTPUTS</span></span>

### <span data-ttu-id="5eee4-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5eee4-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="5eee4-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="5eee4-149">NOTES</span></span>

## <span data-ttu-id="5eee4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eee4-150">RELATED LINKS</span></span>

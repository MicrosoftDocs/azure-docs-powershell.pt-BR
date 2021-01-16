---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272538"
---
# <span data-ttu-id="91b7f-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="91b7f-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="91b7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="91b7f-103">Cria um novo prefixo de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="91b7f-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="91b7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91b7f-104">SYNTAX</span></span>

### <span data-ttu-id="91b7f-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="91b7f-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91b7f-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b7f-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91b7f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91b7f-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91b7f-108">DESCRIPTION</span></span>
<span data-ttu-id="91b7f-109">Cria um prefixo de serviço de emparelhamento associado a um objeto de serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="91b7f-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="91b7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91b7f-110">EXAMPLES</span></span>

### <span data-ttu-id="91b7f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91b7f-111">Example 1</span></span>
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

<span data-ttu-id="91b7f-112">Cria um prefixo a partir de um objeto de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="91b7f-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="91b7f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="91b7f-113">Example 2</span></span>
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

<span data-ttu-id="91b7f-114">Cria um prefixo de uma ID de recurso do serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="91b7f-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="91b7f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="91b7f-115">Example 3</span></span>
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

<span data-ttu-id="91b7f-116">Cria um prefixo de nome e nome de um grupo de recursos de serviço de correspondência</span><span class="sxs-lookup"><span data-stu-id="91b7f-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="91b7f-117">OS</span><span class="sxs-lookup"><span data-stu-id="91b7f-117">PARAMETERS</span></span>

### <span data-ttu-id="91b7f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91b7f-118">-AsJob</span></span>
<span data-ttu-id="91b7f-119">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="91b7f-119">Run in the background.</span></span>

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

### <span data-ttu-id="91b7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b7f-120">-DefaultProfile</span></span>
<span data-ttu-id="91b7f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91b7f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b7f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="91b7f-122">-Name</span></span>
<span data-ttu-id="91b7f-123">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="91b7f-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="91b7f-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="91b7f-124">-PeeringServiceId</span></span>
<span data-ttu-id="91b7f-125">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="91b7f-125">The resource id string name.</span></span>

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

### <span data-ttu-id="91b7f-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="91b7f-126">-PeeringServiceName</span></span>
<span data-ttu-id="91b7f-127">O nome do serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="91b7f-127">The peering service name.</span></span>
<span data-ttu-id="91b7f-128">Use New-AzPeeringService cmdlet para um novo serviço de emparelhamento ou Get-AzPeeringService para obter uma lista.</span><span class="sxs-lookup"><span data-stu-id="91b7f-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="91b7f-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="91b7f-129">-PeeringServiceObject</span></span>
<span data-ttu-id="91b7f-130">Usar uma Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="91b7f-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="91b7f-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="91b7f-131">-Prefix</span></span>
<span data-ttu-id="91b7f-132">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="91b7f-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="91b7f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b7f-133">-ResourceGroupName</span></span>
<span data-ttu-id="91b7f-134">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="91b7f-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="91b7f-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="91b7f-135">-ServiceKey</span></span>
<span data-ttu-id="91b7f-136">Este é um GUID exclusivo fornecido pelo provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="91b7f-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="91b7f-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91b7f-137">-Confirm</span></span>
<span data-ttu-id="91b7f-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91b7f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b7f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b7f-139">-WhatIf</span></span>
<span data-ttu-id="91b7f-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91b7f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91b7f-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91b7f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b7f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b7f-142">CommonParameters</span></span>
<span data-ttu-id="91b7f-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b7f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b7f-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91b7f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b7f-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91b7f-145">INPUTS</span></span>

### <span data-ttu-id="91b7f-146">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="91b7f-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="91b7f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91b7f-147">OUTPUTS</span></span>

### <span data-ttu-id="91b7f-148">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="91b7f-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="91b7f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91b7f-149">NOTES</span></span>

## <span data-ttu-id="91b7f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91b7f-150">RELATED LINKS</span></span>

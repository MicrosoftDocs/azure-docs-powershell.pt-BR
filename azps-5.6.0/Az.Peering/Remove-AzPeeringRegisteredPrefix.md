---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: db62779ab2ac03e6ef528b09dda99fb5ebb244a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890137"
---
# <span data-ttu-id="2aaf5-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="2aaf5-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="2aaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf5-103">Exclua ou remova um prefixo registrado do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="2aaf5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2aaf5-104">SYNTAX</span></span>

### <span data-ttu-id="2aaf5-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2aaf5-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2aaf5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2aaf5-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aaf5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2aaf5-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aaf5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2aaf5-108">DESCRIPTION</span></span>
<span data-ttu-id="2aaf5-109">Permite a remoção do prefixo registrado do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="2aaf5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-110">EXAMPLES</span></span>

### <span data-ttu-id="2aaf5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2aaf5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="2aaf5-112">Remova um prefixo registrado por id de recurso.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="2aaf5-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-113">PARAMETERS</span></span>

### <span data-ttu-id="2aaf5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aaf5-114">-AsJob</span></span>
<span data-ttu-id="2aaf5-115">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-115">Run in the background.</span></span>

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

### <span data-ttu-id="2aaf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf5-116">-DefaultProfile</span></span>
<span data-ttu-id="2aaf5-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aaf5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2aaf5-118">-Force</span></span>
<span data-ttu-id="2aaf5-119">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="2aaf5-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="2aaf5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aaf5-120">-InputObject</span></span>
<span data-ttu-id="2aaf5-121">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2aaf5-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2aaf5-122">-Name</span></span>
<span data-ttu-id="2aaf5-123">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aaf5-124">-PassThru</span></span>
<span data-ttu-id="2aaf5-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2aaf5-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2aaf5-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="2aaf5-126">-PeeringName</span></span>
<span data-ttu-id="2aaf5-127">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf5-128">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf5-129">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aaf5-130">-ResourceId</span></span>
<span data-ttu-id="2aaf5-131">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aaf5-132">-Confirm</span></span>
<span data-ttu-id="2aaf5-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aaf5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aaf5-134">-WhatIf</span></span>
<span data-ttu-id="2aaf5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aaf5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aaf5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf5-137">CommonParameters</span></span>
<span data-ttu-id="2aaf5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaf5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf5-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aaf5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-140">INPUTS</span></span>

### <span data-ttu-id="2aaf5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2aaf5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="2aaf5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2aaf5-142">System.String</span></span>

## <span data-ttu-id="2aaf5-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-143">OUTPUTS</span></span>

### <span data-ttu-id="2aaf5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2aaf5-144">System.Boolean</span></span>

## <span data-ttu-id="2aaf5-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="2aaf5-145">NOTES</span></span>

## <span data-ttu-id="2aaf5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aaf5-146">RELATED LINKS</span></span>

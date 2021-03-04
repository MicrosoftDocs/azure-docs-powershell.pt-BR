---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 3922492f4d72886e0608108811906387e31472b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890136"
---
# <span data-ttu-id="00cd6-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="00cd6-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="00cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="00cd6-103">Remove um novo prefixo de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="00cd6-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="00cd6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="00cd6-104">SYNTAX</span></span>

### <span data-ttu-id="00cd6-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="00cd6-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00cd6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="00cd6-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00cd6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00cd6-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00cd6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="00cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="00cd6-109">Remove um prefixo de serviço de paração de um serviço de paração.</span><span class="sxs-lookup"><span data-stu-id="00cd6-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="00cd6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00cd6-110">EXAMPLES</span></span>

### <span data-ttu-id="00cd6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00cd6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="00cd6-112">Remover um prefixo de um objeto de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="00cd6-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="00cd6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00cd6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="00cd6-114">Remova um prefixo de uma ID de recurso de serviço de paração.</span><span class="sxs-lookup"><span data-stu-id="00cd6-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="00cd6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="00cd6-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="00cd6-116">Remover um prefixo de um nome e nome de grupo de recursos de serviço de paração</span><span class="sxs-lookup"><span data-stu-id="00cd6-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="00cd6-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="00cd6-117">PARAMETERS</span></span>

### <span data-ttu-id="00cd6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00cd6-118">-AsJob</span></span>
<span data-ttu-id="00cd6-119">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="00cd6-119">Run in the background.</span></span>

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

### <span data-ttu-id="00cd6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00cd6-120">-DefaultProfile</span></span>
<span data-ttu-id="00cd6-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00cd6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00cd6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="00cd6-122">-Force</span></span>
<span data-ttu-id="00cd6-123">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="00cd6-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="00cd6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00cd6-124">-InputObject</span></span>
<span data-ttu-id="00cd6-125">Usar um Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="00cd6-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00cd6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="00cd6-126">-Name</span></span>
<span data-ttu-id="00cd6-127">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="00cd6-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="00cd6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00cd6-128">-PassThru</span></span>
<span data-ttu-id="00cd6-129">Retorna true para êxito ou false para falha.</span><span class="sxs-lookup"><span data-stu-id="00cd6-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="00cd6-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="00cd6-130">-PrefixName</span></span>
<span data-ttu-id="00cd6-131">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="00cd6-131">The name of prefix.</span></span>

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

### <span data-ttu-id="00cd6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00cd6-132">-ResourceGroupName</span></span>
<span data-ttu-id="00cd6-133">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="00cd6-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="00cd6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00cd6-134">-ResourceId</span></span>
<span data-ttu-id="00cd6-135">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="00cd6-135">The resource id string name.</span></span>

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

### <span data-ttu-id="00cd6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00cd6-136">-Confirm</span></span>
<span data-ttu-id="00cd6-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00cd6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00cd6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00cd6-138">-WhatIf</span></span>
<span data-ttu-id="00cd6-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00cd6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00cd6-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00cd6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00cd6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00cd6-141">CommonParameters</span></span>
<span data-ttu-id="00cd6-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00cd6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00cd6-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00cd6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00cd6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00cd6-144">INPUTS</span></span>

### <span data-ttu-id="00cd6-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="00cd6-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="00cd6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="00cd6-146">System.String</span></span>

## <span data-ttu-id="00cd6-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="00cd6-147">OUTPUTS</span></span>

### <span data-ttu-id="00cd6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00cd6-148">System.Boolean</span></span>

## <span data-ttu-id="00cd6-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="00cd6-149">NOTES</span></span>

## <span data-ttu-id="00cd6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00cd6-150">RELATED LINKS</span></span>

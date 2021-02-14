---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117276"
---
# <span data-ttu-id="a235e-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a235e-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a235e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a235e-102">SYNOPSIS</span></span>
<span data-ttu-id="a235e-103">Define ou atualiza um prefixo registrado do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="a235e-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="a235e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a235e-104">SYNTAX</span></span>

### <span data-ttu-id="a235e-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a235e-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a235e-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a235e-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a235e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a235e-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a235e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a235e-108">DESCRIPTION</span></span>
<span data-ttu-id="a235e-109">Permite a atualização de um prefixo registrado do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="a235e-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="a235e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a235e-110">EXAMPLES</span></span>

### <span data-ttu-id="a235e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a235e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="a235e-112">Atualiza o prefixo por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a235e-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="a235e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a235e-113">PARAMETERS</span></span>

### <span data-ttu-id="a235e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a235e-114">-AsJob</span></span>
<span data-ttu-id="a235e-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a235e-115">Run in the background.</span></span>

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

### <span data-ttu-id="a235e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a235e-116">-DefaultProfile</span></span>
<span data-ttu-id="a235e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a235e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a235e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a235e-118">-InputObject</span></span>
<span data-ttu-id="a235e-119">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a235e-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a235e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a235e-120">-Name</span></span>
<span data-ttu-id="a235e-121">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="a235e-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a235e-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a235e-122">-PeeringName</span></span>
<span data-ttu-id="a235e-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a235e-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a235e-124">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="a235e-124">-Prefix</span></span>
<span data-ttu-id="a235e-125">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="a235e-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="a235e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a235e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a235e-127">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="a235e-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a235e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a235e-128">-ResourceId</span></span>
<span data-ttu-id="a235e-129">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a235e-129">The resource id string name.</span></span>

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

### <span data-ttu-id="a235e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a235e-130">-Confirm</span></span>
<span data-ttu-id="a235e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a235e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a235e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a235e-132">-WhatIf</span></span>
<span data-ttu-id="a235e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a235e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a235e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a235e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a235e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a235e-135">CommonParameters</span></span>
<span data-ttu-id="a235e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a235e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a235e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a235e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a235e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a235e-138">INPUTS</span></span>

### <span data-ttu-id="a235e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a235e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="a235e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a235e-140">System.String</span></span>

## <span data-ttu-id="a235e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a235e-141">OUTPUTS</span></span>

### <span data-ttu-id="a235e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a235e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a235e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a235e-143">NOTES</span></span>

## <span data-ttu-id="a235e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a235e-144">RELATED LINKS</span></span>

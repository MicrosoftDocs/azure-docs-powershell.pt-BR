---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261403"
---
# <span data-ttu-id="e1e69-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e1e69-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e1e69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1e69-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e69-103">Define ou atualiza um prefixo registrado do recurso de emparelhamento primário.</span><span class="sxs-lookup"><span data-stu-id="e1e69-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="e1e69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1e69-104">SYNTAX</span></span>

### <span data-ttu-id="e1e69-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1e69-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1e69-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1e69-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1e69-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1e69-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1e69-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1e69-108">DESCRIPTION</span></span>
<span data-ttu-id="e1e69-109">Permite a atualização de um prefixo registrado do recurso de emparelhamento pai.</span><span class="sxs-lookup"><span data-stu-id="e1e69-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="e1e69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1e69-110">EXAMPLES</span></span>

### <span data-ttu-id="e1e69-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1e69-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="e1e69-112">Atualiza o prefixo por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e1e69-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="e1e69-113">OS</span><span class="sxs-lookup"><span data-stu-id="e1e69-113">PARAMETERS</span></span>

### <span data-ttu-id="e1e69-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1e69-114">-AsJob</span></span>
<span data-ttu-id="e1e69-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e1e69-115">Run in the background.</span></span>

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

### <span data-ttu-id="e1e69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e69-116">-DefaultProfile</span></span>
<span data-ttu-id="e1e69-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1e69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1e69-118">-InputObject</span></span>
<span data-ttu-id="e1e69-119">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e1e69-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e1e69-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1e69-120">-Name</span></span>
<span data-ttu-id="e1e69-121">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="e1e69-121">The name of prefix.</span></span>

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

### <span data-ttu-id="e1e69-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e1e69-122">-PeeringName</span></span>
<span data-ttu-id="e1e69-123">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e1e69-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e1e69-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e1e69-124">-Prefix</span></span>
<span data-ttu-id="e1e69-125">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="e1e69-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="e1e69-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e69-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1e69-127">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="e1e69-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e1e69-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1e69-128">-ResourceId</span></span>
<span data-ttu-id="e1e69-129">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e1e69-129">The resource id string name.</span></span>

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

### <span data-ttu-id="e1e69-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1e69-130">-Confirm</span></span>
<span data-ttu-id="e1e69-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1e69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e69-132">-WhatIf</span></span>
<span data-ttu-id="e1e69-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1e69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e69-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1e69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e69-135">CommonParameters</span></span>
<span data-ttu-id="e1e69-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e69-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1e69-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e69-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1e69-138">INPUTS</span></span>

### <span data-ttu-id="e1e69-139">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e1e69-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="e1e69-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e69-140">System.String</span></span>

## <span data-ttu-id="e1e69-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1e69-141">OUTPUTS</span></span>

### <span data-ttu-id="e1e69-142">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e1e69-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e1e69-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1e69-143">NOTES</span></span>

## <span data-ttu-id="e1e69-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1e69-144">RELATED LINKS</span></span>

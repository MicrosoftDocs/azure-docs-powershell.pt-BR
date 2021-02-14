---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117282"
---
# <span data-ttu-id="7c300-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7c300-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7c300-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c300-102">SYNOPSIS</span></span>
<span data-ttu-id="7c300-103">Criar prefixos registrados para objetos de peering.</span><span class="sxs-lookup"><span data-stu-id="7c300-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7c300-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c300-104">SYNTAX</span></span>

### <span data-ttu-id="7c300-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c300-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c300-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c300-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c300-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c300-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c300-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c300-108">DESCRIPTION</span></span>
<span data-ttu-id="7c300-109">Criar prefixos registrados para objetos de peering.</span><span class="sxs-lookup"><span data-stu-id="7c300-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7c300-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c300-110">EXAMPLES</span></span>

### <span data-ttu-id="7c300-111">Obter o peering e criar um prefixo registrado</span><span class="sxs-lookup"><span data-stu-id="7c300-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="7c300-112">Obter o par que você deseja adicionar um prefixo registrado.</span><span class="sxs-lookup"><span data-stu-id="7c300-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="7c300-113">Em seguida, passe-o para o commandlet.</span><span class="sxs-lookup"><span data-stu-id="7c300-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="7c300-114">Usar o peering resourceId para criar uma asn registrada</span><span class="sxs-lookup"><span data-stu-id="7c300-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="7c300-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c300-115">PARAMETERS</span></span>

### <span data-ttu-id="7c300-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c300-116">-AsJob</span></span>
<span data-ttu-id="7c300-117">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7c300-117">Run in the background.</span></span>

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

### <span data-ttu-id="7c300-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c300-118">-DefaultProfile</span></span>
<span data-ttu-id="7c300-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c300-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c300-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c300-120">-InputObject</span></span>
<span data-ttu-id="7c300-121">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7c300-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c300-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c300-122">-Name</span></span>
<span data-ttu-id="7c300-123">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="7c300-123">The name of prefix.</span></span>

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

### <span data-ttu-id="7c300-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7c300-124">-PeeringName</span></span>
<span data-ttu-id="7c300-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7c300-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7c300-126">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="7c300-126">-Prefix</span></span>
<span data-ttu-id="7c300-127">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="7c300-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="7c300-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c300-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c300-129">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="7c300-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7c300-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c300-130">-ResourceId</span></span>
<span data-ttu-id="7c300-131">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7c300-131">The resource id string name.</span></span>

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

### <span data-ttu-id="7c300-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7c300-132">-Confirm</span></span>
<span data-ttu-id="7c300-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c300-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c300-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c300-134">-WhatIf</span></span>
<span data-ttu-id="7c300-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7c300-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c300-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c300-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c300-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c300-137">CommonParameters</span></span>
<span data-ttu-id="7c300-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c300-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c300-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c300-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c300-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="7c300-140">INPUTS</span></span>

### <span data-ttu-id="7c300-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="7c300-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="7c300-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7c300-142">System.String</span></span>

## <span data-ttu-id="7c300-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="7c300-143">OUTPUTS</span></span>

### <span data-ttu-id="7c300-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7c300-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7c300-145">Notas</span><span class="sxs-lookup"><span data-stu-id="7c300-145">NOTES</span></span>

## <span data-ttu-id="7c300-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c300-146">RELATED LINKS</span></span>

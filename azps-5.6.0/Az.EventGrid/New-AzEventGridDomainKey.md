---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 297abcdf06d1efbe5cf7e39e310d2c2d422a6324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890418"
---
# <span data-ttu-id="4bb48-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4bb48-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="4bb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb48-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb48-103">Regenera a chave de acesso compartilhado para um domínio de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb48-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="4bb48-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4bb48-104">SYNTAX</span></span>

### <span data-ttu-id="4bb48-105">DomainNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bb48-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb48-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bb48-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb48-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bb48-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb48-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4bb48-108">DESCRIPTION</span></span>
<span data-ttu-id="4bb48-109">Regenera a chave de acesso compartilhado para um domínio de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb48-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="4bb48-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bb48-110">EXAMPLES</span></span>

### <span data-ttu-id="4bb48-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bb48-111">Example 1</span></span>

<span data-ttu-id="4bb48-112">Regenerar a chave correspondente à chave chave1'\ do domínio de Grade de Eventos1 no grupo de recursos \' \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4bb48-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="4bb48-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bb48-113">Example 2</span></span>

<span data-ttu-id="4bb48-114">Regenerar a chave correspondente à chave chave1'\ do domínio de Grade de Eventos1 no grupo de recursos \' \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4bb48-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="4bb48-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4bb48-115">Example 3</span></span>

<span data-ttu-id="4bb48-116">Regenerar a chave correspondente à chave chave2'\ do domínio de Grade de Eventos1 no grupo de recursos \' \` \` \` MyResourceGroupName usando sua ID de recurso \` completa.</span><span class="sxs-lookup"><span data-stu-id="4bb48-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="4bb48-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4bb48-117">PARAMETERS</span></span>

### <span data-ttu-id="4bb48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb48-118">-DefaultProfile</span></span>
<span data-ttu-id="4bb48-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb48-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb48-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="4bb48-120">-DomainInputObject</span></span>
<span data-ttu-id="4bb48-121">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="4bb48-121">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb48-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="4bb48-122">-DomainName</span></span>
<span data-ttu-id="4bb48-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4bb48-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb48-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="4bb48-124">-DomainResourceId</span></span>
<span data-ttu-id="4bb48-125">Identificador de Recurso que representa o Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4bb48-125">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb48-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4bb48-126">-Name</span></span>
<span data-ttu-id="4bb48-127">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="4bb48-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb48-128">-ResourceGroupName</span></span>
<span data-ttu-id="4bb48-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bb48-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb48-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bb48-130">-Confirm</span></span>
<span data-ttu-id="4bb48-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb48-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb48-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb48-132">-WhatIf</span></span>
<span data-ttu-id="4bb48-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4bb48-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb48-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bb48-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb48-135">CommonParameters</span></span>
<span data-ttu-id="4bb48-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb48-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bb48-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb48-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb48-138">INPUTS</span></span>

### <span data-ttu-id="4bb48-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb48-139">System.String</span></span>

### <span data-ttu-id="4bb48-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="4bb48-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="4bb48-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4bb48-141">OUTPUTS</span></span>

### <span data-ttu-id="4bb48-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4bb48-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="4bb48-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="4bb48-143">NOTES</span></span>

## <span data-ttu-id="4bb48-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bb48-144">RELATED LINKS</span></span>

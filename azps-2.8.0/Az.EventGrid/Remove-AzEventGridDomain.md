---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: b46c9be4c8731fa6b9082a8076dd9ae175e62422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596516"
---
# <span data-ttu-id="8bf08-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8bf08-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="8bf08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bf08-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf08-103">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf08-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8bf08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bf08-104">SYNTAX</span></span>

### <span data-ttu-id="8bf08-105">DomainNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bf08-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bf08-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf08-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bf08-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf08-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf08-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bf08-108">DESCRIPTION</span></span>
<span data-ttu-id="8bf08-109">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf08-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8bf08-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bf08-110">EXAMPLES</span></span>

### <span data-ttu-id="8bf08-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bf08-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="8bf08-112">Remove o domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8bf08-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8bf08-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bf08-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="8bf08-114">Remove o domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8bf08-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8bf08-115">OS</span><span class="sxs-lookup"><span data-stu-id="8bf08-115">PARAMETERS</span></span>

### <span data-ttu-id="8bf08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf08-116">-DefaultProfile</span></span>
<span data-ttu-id="8bf08-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bf08-118">-InputObject</span></span>
<span data-ttu-id="8bf08-119">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8bf08-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8bf08-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bf08-120">-Name</span></span>
<span data-ttu-id="8bf08-121">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8bf08-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf08-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bf08-122">-PassThru</span></span>
<span data-ttu-id="8bf08-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="8bf08-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8bf08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf08-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bf08-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bf08-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bf08-126">-ResourceId</span></span>
<span data-ttu-id="8bf08-127">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="8bf08-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf08-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bf08-128">-Confirm</span></span>
<span data-ttu-id="8bf08-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf08-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf08-130">-WhatIf</span></span>
<span data-ttu-id="8bf08-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bf08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf08-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bf08-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf08-133">CommonParameters</span></span>
<span data-ttu-id="8bf08-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf08-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf08-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf08-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bf08-136">INPUTS</span></span>

### <span data-ttu-id="8bf08-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8bf08-137">System.String</span></span>

### <span data-ttu-id="8bf08-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8bf08-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="8bf08-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bf08-139">OUTPUTS</span></span>

### <span data-ttu-id="8bf08-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bf08-140">System.Boolean</span></span>

## <span data-ttu-id="8bf08-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bf08-141">NOTES</span></span>

## <span data-ttu-id="8bf08-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bf08-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124644"
---
# <span data-ttu-id="85dd5-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="85dd5-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="85dd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="85dd5-103">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="85dd5-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="85dd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85dd5-104">SYNTAX</span></span>

### <span data-ttu-id="85dd5-105">DomainNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85dd5-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85dd5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="85dd5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85dd5-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85dd5-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dd5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85dd5-108">DESCRIPTION</span></span>
<span data-ttu-id="85dd5-109">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="85dd5-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="85dd5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85dd5-110">EXAMPLES</span></span>

### <span data-ttu-id="85dd5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85dd5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="85dd5-112">Remove o domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="85dd5-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="85dd5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="85dd5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="85dd5-114">Remove o domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="85dd5-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="85dd5-115">OS</span><span class="sxs-lookup"><span data-stu-id="85dd5-115">PARAMETERS</span></span>

### <span data-ttu-id="85dd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dd5-116">-DefaultProfile</span></span>
<span data-ttu-id="85dd5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85dd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85dd5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85dd5-118">-InputObject</span></span>
<span data-ttu-id="85dd5-119">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="85dd5-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="85dd5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="85dd5-120">-Name</span></span>
<span data-ttu-id="85dd5-121">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="85dd5-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dd5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85dd5-122">-PassThru</span></span>
<span data-ttu-id="85dd5-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="85dd5-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="85dd5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dd5-124">-ResourceGroupName</span></span>
<span data-ttu-id="85dd5-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85dd5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="85dd5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85dd5-126">-ResourceId</span></span>
<span data-ttu-id="85dd5-127">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="85dd5-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="85dd5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85dd5-128">-Confirm</span></span>
<span data-ttu-id="85dd5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85dd5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85dd5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85dd5-130">-WhatIf</span></span>
<span data-ttu-id="85dd5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85dd5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85dd5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85dd5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85dd5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dd5-133">CommonParameters</span></span>
<span data-ttu-id="85dd5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dd5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dd5-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85dd5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dd5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85dd5-136">INPUTS</span></span>

### <span data-ttu-id="85dd5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="85dd5-137">System.String</span></span>

### <span data-ttu-id="85dd5-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="85dd5-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="85dd5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85dd5-139">OUTPUTS</span></span>

### <span data-ttu-id="85dd5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85dd5-140">System.Boolean</span></span>

## <span data-ttu-id="85dd5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85dd5-141">NOTES</span></span>

## <span data-ttu-id="85dd5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85dd5-142">RELATED LINKS</span></span>

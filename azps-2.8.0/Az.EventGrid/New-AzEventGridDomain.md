---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 2b69fed3c63edb503b2087cfb7b8ab142eb04473
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596527"
---
# <span data-ttu-id="8f567-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8f567-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="8f567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f567-102">SYNOPSIS</span></span>
<span data-ttu-id="8f567-103">Cria um novo domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f567-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8f567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f567-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f567-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f567-105">DESCRIPTION</span></span>
<span data-ttu-id="8f567-106">Cria um novo domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f567-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="8f567-107">Após a criação do domínio, um aplicativo pode publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="8f567-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="8f567-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f567-108">EXAMPLES</span></span>

### <span data-ttu-id="8f567-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f567-109">Example 1</span></span>

<span data-ttu-id="8f567-110">Cria um domínio de grade de \` domain1 \` no local geográfico especificado \` westus2 \` , no grupo de MyResourceGroupName grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8f567-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="8f567-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f567-111">Example 2</span></span>

<span data-ttu-id="8f567-112">Cria um domínio de grade de \` domain1 \` no local geográfico especificado \` westus2 \` , no grupo de recursos \` MyResourceGroupName, \` com as marcas especificadas "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="8f567-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="8f567-113">OS</span><span class="sxs-lookup"><span data-stu-id="8f567-113">PARAMETERS</span></span>

### <span data-ttu-id="8f567-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f567-114">-DefaultProfile</span></span>
<span data-ttu-id="8f567-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f567-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f567-116">-Local</span><span class="sxs-lookup"><span data-stu-id="8f567-116">-Location</span></span>
<span data-ttu-id="8f567-117">O local do domínio.</span><span class="sxs-lookup"><span data-stu-id="8f567-117">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f567-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f567-118">-Name</span></span>
<span data-ttu-id="8f567-119">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8f567-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f567-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f567-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f567-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f567-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f567-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="8f567-122">-Tag</span></span>
<span data-ttu-id="8f567-123">Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f567-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f567-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f567-124">-Confirm</span></span>
<span data-ttu-id="8f567-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f567-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f567-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f567-126">-WhatIf</span></span>
<span data-ttu-id="8f567-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f567-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f567-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f567-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f567-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f567-129">CommonParameters</span></span>
<span data-ttu-id="8f567-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f567-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f567-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f567-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f567-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f567-132">INPUTS</span></span>

### <span data-ttu-id="8f567-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8f567-133">System.String</span></span>

### <span data-ttu-id="8f567-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f567-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f567-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f567-135">OUTPUTS</span></span>

### <span data-ttu-id="8f567-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8f567-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="8f567-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f567-137">NOTES</span></span>

## <span data-ttu-id="8f567-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f567-138">RELATED LINKS</span></span>

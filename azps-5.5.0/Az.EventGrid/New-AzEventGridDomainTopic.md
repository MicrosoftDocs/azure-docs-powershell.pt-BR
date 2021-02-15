---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115315"
---
# <span data-ttu-id="e0fbd-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e0fbd-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="e0fbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fbd-103">Cria um novo Tópico de Domínio da Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e0fbd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0fbd-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0fbd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e0fbd-106">Cria um novo Tópico de Domínio da Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e0fbd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="e0fbd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0fbd-108">Example 1</span></span>

<span data-ttu-id="e0fbd-109">Cria um Tópico de Tópico de Domínio de Grade de \` Evento1 no Domínio1 no grupo \` de recursos \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="e0fbd-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="e0fbd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="e0fbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fbd-111">-DefaultProfile</span></span>
<span data-ttu-id="e0fbd-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0fbd-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e0fbd-113">-DomainName</span></span>
<span data-ttu-id="e0fbd-114">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fbd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0fbd-115">-Name</span></span>
<span data-ttu-id="e0fbd-116">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fbd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fbd-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0fbd-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0fbd-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0fbd-119">-Confirm</span></span>
<span data-ttu-id="e0fbd-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0fbd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0fbd-121">-WhatIf</span></span>
<span data-ttu-id="e0fbd-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0fbd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0fbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fbd-124">CommonParameters</span></span>
<span data-ttu-id="e0fbd-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0fbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fbd-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0fbd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fbd-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0fbd-127">INPUTS</span></span>

### <span data-ttu-id="e0fbd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e0fbd-128">System.String</span></span>

## <span data-ttu-id="e0fbd-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0fbd-129">OUTPUTS</span></span>

### <span data-ttu-id="e0fbd-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e0fbd-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="e0fbd-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e0fbd-131">NOTES</span></span>

## <span data-ttu-id="e0fbd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0fbd-132">RELATED LINKS</span></span>

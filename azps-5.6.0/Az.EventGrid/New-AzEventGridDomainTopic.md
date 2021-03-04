---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 18be852a8a44f55cbc159bdbc7b4dbf3f276582a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890419"
---
# <span data-ttu-id="cf300-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cf300-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="cf300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf300-102">SYNOPSIS</span></span>
<span data-ttu-id="cf300-103">Cria um novo tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf300-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="cf300-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf300-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf300-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf300-105">DESCRIPTION</span></span>
<span data-ttu-id="cf300-106">Cria um novo tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf300-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="cf300-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf300-107">EXAMPLES</span></span>

### <span data-ttu-id="cf300-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf300-108">Example 1</span></span>

<span data-ttu-id="cf300-109">Cria um Tópico de Domínio da Grade de Eventos1 no Domínio1 no grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cf300-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="cf300-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf300-110">PARAMETERS</span></span>

### <span data-ttu-id="cf300-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf300-111">-DefaultProfile</span></span>
<span data-ttu-id="cf300-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf300-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf300-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="cf300-113">-DomainName</span></span>
<span data-ttu-id="cf300-114">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="cf300-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="cf300-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cf300-115">-Name</span></span>
<span data-ttu-id="cf300-116">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="cf300-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="cf300-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf300-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf300-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf300-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf300-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf300-119">-Confirm</span></span>
<span data-ttu-id="cf300-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf300-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf300-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf300-121">-WhatIf</span></span>
<span data-ttu-id="cf300-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf300-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf300-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf300-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf300-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf300-124">CommonParameters</span></span>
<span data-ttu-id="cf300-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf300-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf300-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf300-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf300-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf300-127">INPUTS</span></span>

### <span data-ttu-id="cf300-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cf300-128">System.String</span></span>

## <span data-ttu-id="cf300-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf300-129">OUTPUTS</span></span>

### <span data-ttu-id="cf300-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cf300-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="cf300-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf300-131">NOTES</span></span>

## <span data-ttu-id="cf300-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf300-132">RELATED LINKS</span></span>

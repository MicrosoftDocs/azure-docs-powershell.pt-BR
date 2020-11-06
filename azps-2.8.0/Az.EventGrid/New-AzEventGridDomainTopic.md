---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 9946c065a572333062c512c3ce5fa866c5d3ce20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596524"
---
# <span data-ttu-id="dc466-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dc466-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="dc466-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc466-102">SYNOPSIS</span></span>
<span data-ttu-id="dc466-103">Cria um novo tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc466-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="dc466-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc466-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc466-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc466-105">DESCRIPTION</span></span>
<span data-ttu-id="dc466-106">Cria um novo tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc466-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="dc466-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc466-107">EXAMPLES</span></span>

### <span data-ttu-id="dc466-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc466-108">Example 1</span></span>

<span data-ttu-id="dc466-109">Cria um tópico de \` tópico1 do domínio \` da grade de eventos no domain1 de domínio \` \` em MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="dc466-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="dc466-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc466-110">PARAMETERS</span></span>

### <span data-ttu-id="dc466-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc466-111">-DefaultProfile</span></span>
<span data-ttu-id="dc466-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc466-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc466-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="dc466-113">-DomainName</span></span>
<span data-ttu-id="dc466-114">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dc466-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="dc466-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc466-115">-Name</span></span>
<span data-ttu-id="dc466-116">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dc466-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="dc466-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc466-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc466-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc466-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc466-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc466-119">-Confirm</span></span>
<span data-ttu-id="dc466-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc466-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc466-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc466-121">-WhatIf</span></span>
<span data-ttu-id="dc466-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc466-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc466-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc466-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc466-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc466-124">CommonParameters</span></span>
<span data-ttu-id="dc466-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc466-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc466-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc466-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc466-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc466-127">INPUTS</span></span>

### <span data-ttu-id="dc466-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dc466-128">System.String</span></span>

## <span data-ttu-id="dc466-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc466-129">OUTPUTS</span></span>

### <span data-ttu-id="dc466-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dc466-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="dc466-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc466-131">NOTES</span></span>

## <span data-ttu-id="dc466-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc466-132">RELATED LINKS</span></span>

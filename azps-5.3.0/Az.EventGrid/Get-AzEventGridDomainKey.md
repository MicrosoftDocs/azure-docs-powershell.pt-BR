---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271409"
---
# <span data-ttu-id="76844-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="76844-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="76844-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76844-102">SYNOPSIS</span></span>
<span data-ttu-id="76844-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="76844-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="76844-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76844-104">SYNTAX</span></span>

### <span data-ttu-id="76844-105">DomainNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="76844-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76844-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76844-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76844-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="76844-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76844-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76844-108">DESCRIPTION</span></span>
<span data-ttu-id="76844-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="76844-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="76844-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76844-110">EXAMPLES</span></span>

### <span data-ttu-id="76844-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76844-111">Example 1</span></span>

<span data-ttu-id="76844-112">Obtém as chaves de acesso compartilhado do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="76844-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="76844-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="76844-113">Example 2</span></span>

<span data-ttu-id="76844-114">Obtém as chaves de acesso compartilhado do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="76844-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="76844-115">OS</span><span class="sxs-lookup"><span data-stu-id="76844-115">PARAMETERS</span></span>

### <span data-ttu-id="76844-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76844-116">-DefaultProfile</span></span>
<span data-ttu-id="76844-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76844-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76844-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="76844-118">-DomainObject</span></span>
<span data-ttu-id="76844-119">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="76844-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="76844-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="76844-120">-DomainResourceId</span></span>
<span data-ttu-id="76844-121">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="76844-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="76844-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="76844-122">-Name</span></span>
<span data-ttu-id="76844-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="76844-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="76844-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76844-124">-ResourceGroupName</span></span>
<span data-ttu-id="76844-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76844-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="76844-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76844-126">CommonParameters</span></span>
<span data-ttu-id="76844-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76844-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76844-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76844-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76844-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76844-129">INPUTS</span></span>

### <span data-ttu-id="76844-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76844-130">System.String</span></span>

### <span data-ttu-id="76844-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="76844-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="76844-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76844-132">OUTPUTS</span></span>

### <span data-ttu-id="76844-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="76844-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="76844-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76844-134">NOTES</span></span>

## <span data-ttu-id="76844-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76844-135">RELATED LINKS</span></span>

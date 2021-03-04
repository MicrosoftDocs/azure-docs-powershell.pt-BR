---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: a211e3857cd81a5dd057795fb9e2956d60cbae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889475"
---
# <span data-ttu-id="8210e-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8210e-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="8210e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8210e-102">SYNOPSIS</span></span>
<span data-ttu-id="8210e-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8210e-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="8210e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8210e-104">SYNTAX</span></span>

### <span data-ttu-id="8210e-105">DomainNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8210e-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8210e-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8210e-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8210e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8210e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8210e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8210e-108">DESCRIPTION</span></span>
<span data-ttu-id="8210e-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8210e-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="8210e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8210e-110">EXAMPLES</span></span>

### <span data-ttu-id="8210e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8210e-111">Example 1</span></span>

<span data-ttu-id="8210e-112">Obtém as chaves de acesso compartilhado do domínio de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8210e-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="8210e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8210e-113">Example 2</span></span>

<span data-ttu-id="8210e-114">Obtém as chaves de acesso compartilhado do domínio de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8210e-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="8210e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8210e-115">PARAMETERS</span></span>

### <span data-ttu-id="8210e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8210e-116">-DefaultProfile</span></span>
<span data-ttu-id="8210e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8210e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8210e-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="8210e-118">-DomainObject</span></span>
<span data-ttu-id="8210e-119">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="8210e-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8210e-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="8210e-120">-DomainResourceId</span></span>
<span data-ttu-id="8210e-121">Identificador de Recurso que representa o Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8210e-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="8210e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8210e-122">-Name</span></span>
<span data-ttu-id="8210e-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8210e-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="8210e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8210e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8210e-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8210e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8210e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8210e-126">CommonParameters</span></span>
<span data-ttu-id="8210e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8210e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8210e-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8210e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8210e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8210e-129">INPUTS</span></span>

### <span data-ttu-id="8210e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8210e-130">System.String</span></span>

### <span data-ttu-id="8210e-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8210e-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="8210e-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8210e-132">OUTPUTS</span></span>

### <span data-ttu-id="8210e-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8210e-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="8210e-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="8210e-134">NOTES</span></span>

## <span data-ttu-id="8210e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8210e-135">RELATED LINKS</span></span>

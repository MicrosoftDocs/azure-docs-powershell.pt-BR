---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: 4d72be4f7ddbe6cd5884269c724c7505cc05fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596540"
---
# <span data-ttu-id="a1441-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a1441-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="a1441-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1441-102">SYNOPSIS</span></span>
<span data-ttu-id="a1441-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="a1441-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="a1441-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1441-104">SYNTAX</span></span>

### <span data-ttu-id="a1441-105">DomainNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1441-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1441-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1441-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1441-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1441-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1441-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1441-108">DESCRIPTION</span></span>
<span data-ttu-id="a1441-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="a1441-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="a1441-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1441-110">EXAMPLES</span></span>

### <span data-ttu-id="a1441-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1441-111">Example 1</span></span>

<span data-ttu-id="a1441-112">Obtém as chaves de acesso compartilhado do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a1441-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="a1441-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1441-113">Example 2</span></span>

<span data-ttu-id="a1441-114">Obtém as chaves de acesso compartilhado do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a1441-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="a1441-115">OS</span><span class="sxs-lookup"><span data-stu-id="a1441-115">PARAMETERS</span></span>

### <span data-ttu-id="a1441-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1441-116">-DefaultProfile</span></span>
<span data-ttu-id="a1441-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1441-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1441-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="a1441-118">-DomainObject</span></span>
<span data-ttu-id="a1441-119">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a1441-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a1441-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="a1441-120">-DomainResourceId</span></span>
<span data-ttu-id="a1441-121">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="a1441-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="a1441-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1441-122">-Name</span></span>
<span data-ttu-id="a1441-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a1441-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="a1441-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1441-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1441-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1441-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1441-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1441-126">CommonParameters</span></span>
<span data-ttu-id="a1441-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1441-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1441-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1441-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1441-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1441-129">INPUTS</span></span>

### <span data-ttu-id="a1441-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1441-130">System.String</span></span>

### <span data-ttu-id="a1441-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a1441-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="a1441-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1441-132">OUTPUTS</span></span>

### <span data-ttu-id="a1441-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a1441-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="a1441-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1441-134">NOTES</span></span>

## <span data-ttu-id="a1441-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1441-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126982"
---
# <span data-ttu-id="16a1a-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="16a1a-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="16a1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="16a1a-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de Grade de Evento.</span><span class="sxs-lookup"><span data-stu-id="16a1a-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="16a1a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16a1a-104">SYNTAX</span></span>

### <span data-ttu-id="16a1a-105">DomainNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16a1a-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a1a-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16a1a-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16a1a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="16a1a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16a1a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="16a1a-108">DESCRIPTION</span></span>
<span data-ttu-id="16a1a-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um domínio de Grade de Evento.</span><span class="sxs-lookup"><span data-stu-id="16a1a-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="16a1a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16a1a-110">EXAMPLES</span></span>

### <span data-ttu-id="16a1a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16a1a-111">Example 1</span></span>

<span data-ttu-id="16a1a-112">Obtém as chaves de acesso compartilhado do domínio domínio da Grade do \` Evento1 \` no grupo de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="16a1a-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="16a1a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="16a1a-113">Example 2</span></span>

<span data-ttu-id="16a1a-114">Obtém as chaves de acesso compartilhado do domínio domínio da Grade do \` Evento1 \` no grupo de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="16a1a-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="16a1a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16a1a-115">PARAMETERS</span></span>

### <span data-ttu-id="16a1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a1a-116">-DefaultProfile</span></span>
<span data-ttu-id="16a1a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16a1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a1a-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="16a1a-118">-DomainObject</span></span>
<span data-ttu-id="16a1a-119">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="16a1a-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="16a1a-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="16a1a-120">-DomainResourceId</span></span>
<span data-ttu-id="16a1a-121">Identificador de Recurso representando o Domínio da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="16a1a-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="16a1a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="16a1a-122">-Name</span></span>
<span data-ttu-id="16a1a-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="16a1a-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="16a1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="16a1a-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16a1a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="16a1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a1a-126">CommonParameters</span></span>
<span data-ttu-id="16a1a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a1a-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16a1a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a1a-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="16a1a-129">INPUTS</span></span>

### <span data-ttu-id="16a1a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="16a1a-130">System.String</span></span>

### <span data-ttu-id="16a1a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="16a1a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="16a1a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="16a1a-132">OUTPUTS</span></span>

### <span data-ttu-id="16a1a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="16a1a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="16a1a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="16a1a-134">NOTES</span></span>

## <span data-ttu-id="16a1a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16a1a-135">RELATED LINKS</span></span>

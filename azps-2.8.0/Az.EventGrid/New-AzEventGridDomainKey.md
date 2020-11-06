---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 2ed323b9d454ca97bceaf27c00aab4460a792941
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596525"
---
# <span data-ttu-id="8539b-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8539b-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="8539b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8539b-102">SYNOPSIS</span></span>
<span data-ttu-id="8539b-103">Regenera a chave de acesso compartilhada para um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8539b-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8539b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8539b-104">SYNTAX</span></span>

### <span data-ttu-id="8539b-105">DomainNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8539b-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8539b-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8539b-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8539b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8539b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8539b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8539b-108">DESCRIPTION</span></span>
<span data-ttu-id="8539b-109">Regenera a chave de acesso compartilhada para um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8539b-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8539b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8539b-110">EXAMPLES</span></span>

### <span data-ttu-id="8539b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8539b-111">Example 1</span></span>

<span data-ttu-id="8539b-112">Regenere a chave correspondente à chave \' key1 ' \ do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8539b-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="8539b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8539b-113">Example 2</span></span>

<span data-ttu-id="8539b-114">Regenere a chave correspondente à chave \' key1 ' \ do domínio da grade de eventos \` domain1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8539b-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="8539b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8539b-115">Example 3</span></span>

<span data-ttu-id="8539b-116">Regenere a chave correspondente à chave \' Key2 ' \ do domínio da grade de eventos \` domain1 \` no grupo de recursos \` MyResourceGroupName \` usando sua ID de recurso completo.</span><span class="sxs-lookup"><span data-stu-id="8539b-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="8539b-117">OS</span><span class="sxs-lookup"><span data-stu-id="8539b-117">PARAMETERS</span></span>

### <span data-ttu-id="8539b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8539b-118">-DefaultProfile</span></span>
<span data-ttu-id="8539b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8539b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8539b-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="8539b-120">-DomainInputObject</span></span>
<span data-ttu-id="8539b-121">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8539b-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8539b-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="8539b-122">-DomainName</span></span>
<span data-ttu-id="8539b-123">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8539b-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8539b-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="8539b-124">-DomainResourceId</span></span>
<span data-ttu-id="8539b-125">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="8539b-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="8539b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8539b-126">-Name</span></span>
<span data-ttu-id="8539b-127">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="8539b-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8539b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8539b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8539b-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8539b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="8539b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8539b-130">-Confirm</span></span>
<span data-ttu-id="8539b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8539b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8539b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8539b-132">-WhatIf</span></span>
<span data-ttu-id="8539b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8539b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8539b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8539b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8539b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8539b-135">CommonParameters</span></span>
<span data-ttu-id="8539b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8539b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8539b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8539b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8539b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8539b-138">INPUTS</span></span>

### <span data-ttu-id="8539b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8539b-139">System.String</span></span>

### <span data-ttu-id="8539b-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8539b-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="8539b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8539b-141">OUTPUTS</span></span>

### <span data-ttu-id="8539b-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8539b-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="8539b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8539b-143">NOTES</span></span>

## <span data-ttu-id="8539b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8539b-144">RELATED LINKS</span></span>

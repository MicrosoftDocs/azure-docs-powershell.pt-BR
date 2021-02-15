---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113839"
---
# <span data-ttu-id="b4465-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b4465-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="b4465-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4465-102">SYNOPSIS</span></span>
<span data-ttu-id="b4465-103">Remove um Tópico de Domínio da Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4465-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="b4465-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4465-104">SYNTAX</span></span>

### <span data-ttu-id="b4465-105">DomainTopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4465-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4465-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4465-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4465-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4465-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4465-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4465-108">DESCRIPTION</span></span>
<span data-ttu-id="b4465-109">Remove um Tópico de Domínio da Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4465-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="b4465-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4465-110">EXAMPLES</span></span>

### <span data-ttu-id="b4465-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4465-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="b4465-112">Remove o Tópico de Tópico do Domínio da Grade do Evento1 em Domínio1 no grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b4465-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b4465-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b4465-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="b4465-114">Remove o Tópico de Tópico do Domínio da Grade do Evento1 em Domínio1 no grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b4465-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b4465-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4465-115">PARAMETERS</span></span>

### <span data-ttu-id="b4465-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4465-116">-DefaultProfile</span></span>
<span data-ttu-id="b4465-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4465-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4465-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="b4465-118">-DomainName</span></span>
<span data-ttu-id="b4465-119">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b4465-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4465-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4465-120">-InputObject</span></span>
<span data-ttu-id="b4465-121">Objeto Tópico de Domínio do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b4465-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4465-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4465-122">-Name</span></span>
<span data-ttu-id="b4465-123">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b4465-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4465-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4465-124">-PassThru</span></span>
<span data-ttu-id="b4465-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b4465-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b4465-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4465-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4465-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4465-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4465-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4465-128">-ResourceId</span></span>
<span data-ttu-id="b4465-129">Identificador de Recursos que representa o Tópico de Domínio da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="b4465-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4465-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4465-130">-Confirm</span></span>
<span data-ttu-id="b4465-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4465-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4465-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4465-132">-WhatIf</span></span>
<span data-ttu-id="b4465-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4465-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4465-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4465-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4465-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4465-135">CommonParameters</span></span>
<span data-ttu-id="b4465-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4465-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4465-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4465-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4465-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4465-138">INPUTS</span></span>

### <span data-ttu-id="b4465-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b4465-139">System.String</span></span>

### <span data-ttu-id="b4465-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b4465-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="b4465-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4465-141">OUTPUTS</span></span>

### <span data-ttu-id="b4465-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4465-142">System.Boolean</span></span>

## <span data-ttu-id="b4465-143">Notas</span><span class="sxs-lookup"><span data-stu-id="b4465-143">NOTES</span></span>

## <span data-ttu-id="b4465-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4465-144">RELATED LINKS</span></span>

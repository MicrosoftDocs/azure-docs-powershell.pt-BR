---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885255"
---
# <span data-ttu-id="ce776-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="ce776-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="ce776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce776-102">SYNOPSIS</span></span>
<span data-ttu-id="ce776-103">Regenera as cadeias de caracteres de conexão primárias ou secundárias para o namespace de Barra de Serviço ou fila ou tópico.</span><span class="sxs-lookup"><span data-stu-id="ce776-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ce776-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce776-104">SYNTAX</span></span>

### <span data-ttu-id="ce776-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce776-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce776-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce776-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce776-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce776-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce776-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce776-108">DESCRIPTION</span></span>
<span data-ttu-id="ce776-109">O cmdlet **New-AzServiceBusKey** gera novas cadeias de conexão primárias ou secundárias para o namespace especificado ou fila ou tópico e regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="ce776-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="ce776-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce776-110">EXAMPLES</span></span>

### <span data-ttu-id="ce776-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce776-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ce776-112">Regenera as cadeias de caracteres de conexão primárias ou secundárias para o namespace.</span><span class="sxs-lookup"><span data-stu-id="ce776-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="ce776-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce776-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ce776-114">Regenera as cadeias de conexão primárias ou secundárias com o valor Key fornecido para o namespace.</span><span class="sxs-lookup"><span data-stu-id="ce776-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="ce776-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce776-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ce776-116">Regenera as cadeias de conexão primárias ou secundárias da fila.</span><span class="sxs-lookup"><span data-stu-id="ce776-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="ce776-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ce776-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ce776-118">Regenera as cadeias de conexão primárias ou secundárias com o valor key fornecido para a fila.</span><span class="sxs-lookup"><span data-stu-id="ce776-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="ce776-119">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="ce776-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ce776-120">Regenera as cadeias de caracteres de conexão primárias ou secundárias do tópico.</span><span class="sxs-lookup"><span data-stu-id="ce776-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="ce776-121">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="ce776-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ce776-122">Regenera as cadeias de conexão primárias ou secundárias com o valor Key fornecido para o tópico.</span><span class="sxs-lookup"><span data-stu-id="ce776-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="ce776-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce776-123">PARAMETERS</span></span>

### <span data-ttu-id="ce776-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce776-124">-DefaultProfile</span></span>
<span data-ttu-id="ce776-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce776-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce776-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="ce776-126">-KeyValue</span></span>
<span data-ttu-id="ce776-127">Uma chave de 256 bits codificada com base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="ce776-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ce776-128">-Name</span></span>
<span data-ttu-id="ce776-129">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce776-129">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce776-130">-Namespace</span></span>
<span data-ttu-id="ce776-131">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ce776-131">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="ce776-132">-Queue</span></span>
<span data-ttu-id="ce776-133">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="ce776-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ce776-134">-RegenerateKey</span></span>
<span data-ttu-id="ce776-135">Chaves regeneradas - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="ce776-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce776-136">-ResourceGroupName</span></span>
<span data-ttu-id="ce776-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ce776-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="ce776-138">-Topic</span></span>
<span data-ttu-id="ce776-139">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="ce776-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce776-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce776-140">-Confirm</span></span>
<span data-ttu-id="ce776-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce776-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce776-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce776-142">-WhatIf</span></span>
<span data-ttu-id="ce776-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce776-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce776-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce776-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce776-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce776-145">CommonParameters</span></span>
<span data-ttu-id="ce776-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce776-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce776-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce776-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce776-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce776-148">INPUTS</span></span>

### <span data-ttu-id="ce776-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ce776-149">System.String</span></span>

## <span data-ttu-id="ce776-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce776-150">OUTPUTS</span></span>

### <span data-ttu-id="ce776-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ce776-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="ce776-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce776-152">NOTES</span></span>

## <span data-ttu-id="ce776-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce776-153">RELATED LINKS</span></span>

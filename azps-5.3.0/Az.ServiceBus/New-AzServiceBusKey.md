---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433141"
---
# <span data-ttu-id="7267a-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="7267a-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="7267a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7267a-102">SYNOPSIS</span></span>
<span data-ttu-id="7267a-103">Regenera a cadeia de caracteres de conexão primária ou secundária para o namespace ou a fila ou tópico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="7267a-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="7267a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7267a-104">SYNTAX</span></span>

### <span data-ttu-id="7267a-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7267a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7267a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7267a-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7267a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7267a-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7267a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7267a-108">DESCRIPTION</span></span>
<span data-ttu-id="7267a-109">O cmdlet **New-AzServiceBusKey** gera novas cadeias de conexão primárias ou secundárias para o namespace ou fila ou regra de autorização ou tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="7267a-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="7267a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7267a-110">EXAMPLES</span></span>

### <span data-ttu-id="7267a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7267a-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7267a-112">Regenera as cadeias de conexão primária ou secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="7267a-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="7267a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7267a-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7267a-114">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o namespace.</span><span class="sxs-lookup"><span data-stu-id="7267a-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="7267a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7267a-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7267a-116">Regenera a cadeia de caracteres de conexão primária ou secundária para a fila.</span><span class="sxs-lookup"><span data-stu-id="7267a-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="7267a-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7267a-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7267a-118">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para a fila.</span><span class="sxs-lookup"><span data-stu-id="7267a-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="7267a-119">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="7267a-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7267a-120">Regenera as cadeias de conexão primária ou secundária para o tópico.</span><span class="sxs-lookup"><span data-stu-id="7267a-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="7267a-121">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="7267a-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7267a-122">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o tópico.</span><span class="sxs-lookup"><span data-stu-id="7267a-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="7267a-123">OS</span><span class="sxs-lookup"><span data-stu-id="7267a-123">PARAMETERS</span></span>

### <span data-ttu-id="7267a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7267a-124">-DefaultProfile</span></span>
<span data-ttu-id="7267a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7267a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7267a-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="7267a-126">-KeyValue</span></span>
<span data-ttu-id="7267a-127">Uma chave de 256 bits codificada em base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="7267a-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="7267a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7267a-128">-Name</span></span>
<span data-ttu-id="7267a-129">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7267a-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7267a-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7267a-130">-Namespace</span></span>
<span data-ttu-id="7267a-131">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7267a-131">Namespace Name</span></span>

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

### <span data-ttu-id="7267a-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="7267a-132">-Queue</span></span>
<span data-ttu-id="7267a-133">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="7267a-133">Queue Name</span></span>

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

### <span data-ttu-id="7267a-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7267a-134">-RegenerateKey</span></span>
<span data-ttu-id="7267a-135">Regenerar chaves-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="7267a-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="7267a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7267a-136">-ResourceGroupName</span></span>
<span data-ttu-id="7267a-137">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7267a-137">Resource Group Name</span></span>

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

### <span data-ttu-id="7267a-138">-Tópico</span><span class="sxs-lookup"><span data-stu-id="7267a-138">-Topic</span></span>
<span data-ttu-id="7267a-139">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="7267a-139">Topic Name</span></span>

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

### <span data-ttu-id="7267a-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7267a-140">-Confirm</span></span>
<span data-ttu-id="7267a-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7267a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7267a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7267a-142">-WhatIf</span></span>
<span data-ttu-id="7267a-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7267a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7267a-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7267a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7267a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7267a-145">CommonParameters</span></span>
<span data-ttu-id="7267a-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7267a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7267a-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7267a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7267a-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7267a-148">INPUTS</span></span>

### <span data-ttu-id="7267a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7267a-149">System.String</span></span>

## <span data-ttu-id="7267a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7267a-150">OUTPUTS</span></span>

### <span data-ttu-id="7267a-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7267a-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="7267a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7267a-152">NOTES</span></span>

## <span data-ttu-id="7267a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7267a-153">RELATED LINKS</span></span>

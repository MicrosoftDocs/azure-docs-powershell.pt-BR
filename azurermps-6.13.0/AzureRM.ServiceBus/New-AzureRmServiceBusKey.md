---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 6efd58497adc1e59f1bf6d2c2151386ee773f66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432731"
---
# <span data-ttu-id="66f90-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="66f90-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="66f90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66f90-102">SYNOPSIS</span></span>
<span data-ttu-id="66f90-103">Regenera a cadeia de caracteres de conexão primária ou secundária para o namespace ou a fila ou tópico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="66f90-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66f90-104">SYNTAX</span></span>

### <span data-ttu-id="66f90-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="66f90-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66f90-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66f90-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66f90-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66f90-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66f90-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66f90-108">DESCRIPTION</span></span>
<span data-ttu-id="66f90-109">O cmdlet **New-AzureRmServiceBusKey** gera novas cadeias de conexão primárias ou secundárias para o namespace ou fila ou regra de autorização ou tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="66f90-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="66f90-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66f90-110">EXAMPLES</span></span>

### <span data-ttu-id="66f90-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66f90-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="66f90-112">Regenera as cadeias de conexão primária ou secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="66f90-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="66f90-113">Exemplo 1,1</span><span class="sxs-lookup"><span data-stu-id="66f90-113">Example 1.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="66f90-114">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o namespace.</span><span class="sxs-lookup"><span data-stu-id="66f90-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="66f90-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="66f90-115">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="66f90-116">Regenera a cadeia de caracteres de conexão primária ou secundária para a fila.</span><span class="sxs-lookup"><span data-stu-id="66f90-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="66f90-117">Exemplo 2,2</span><span class="sxs-lookup"><span data-stu-id="66f90-117">Example 2.2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="66f90-118">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para a fila.</span><span class="sxs-lookup"><span data-stu-id="66f90-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="66f90-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="66f90-119">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="66f90-120">Regenera as cadeias de conexão primária ou secundária para o tópico.</span><span class="sxs-lookup"><span data-stu-id="66f90-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="66f90-121">Exemplo 3,1</span><span class="sxs-lookup"><span data-stu-id="66f90-121">Example 3.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="66f90-122">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o tópico.</span><span class="sxs-lookup"><span data-stu-id="66f90-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="66f90-123">OS</span><span class="sxs-lookup"><span data-stu-id="66f90-123">PARAMETERS</span></span>

### <span data-ttu-id="66f90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f90-124">-DefaultProfile</span></span>
<span data-ttu-id="66f90-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66f90-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f90-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="66f90-126">-KeyValue</span></span>
<span data-ttu-id="66f90-127">Uma chave de 256 bits codificada em base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="66f90-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="66f90-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="66f90-128">-Name</span></span>
<span data-ttu-id="66f90-129">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="66f90-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="66f90-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66f90-130">-Namespace</span></span>
<span data-ttu-id="66f90-131">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="66f90-131">Namespace Name</span></span>

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

### <span data-ttu-id="66f90-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="66f90-132">-Queue</span></span>
<span data-ttu-id="66f90-133">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="66f90-133">Queue Name</span></span>

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

### <span data-ttu-id="66f90-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="66f90-134">-RegenerateKey</span></span>
<span data-ttu-id="66f90-135">Regenerar chaves-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="66f90-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="66f90-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f90-136">-ResourceGroupName</span></span>
<span data-ttu-id="66f90-137">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="66f90-137">Resource Group Name</span></span>

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

### <span data-ttu-id="66f90-138">-Tópico</span><span class="sxs-lookup"><span data-stu-id="66f90-138">-Topic</span></span>
<span data-ttu-id="66f90-139">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="66f90-139">Topic Name</span></span>

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

### <span data-ttu-id="66f90-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66f90-140">-Confirm</span></span>
<span data-ttu-id="66f90-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66f90-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66f90-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f90-142">-WhatIf</span></span>
<span data-ttu-id="66f90-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66f90-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f90-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66f90-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66f90-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f90-145">CommonParameters</span></span>
<span data-ttu-id="66f90-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f90-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f90-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f90-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f90-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66f90-148">INPUTS</span></span>

### <span data-ttu-id="66f90-149">System. String</span><span class="sxs-lookup"><span data-stu-id="66f90-149">System.String</span></span>

## <span data-ttu-id="66f90-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66f90-150">OUTPUTS</span></span>

### <span data-ttu-id="66f90-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="66f90-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="66f90-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66f90-152">NOTES</span></span>

## <span data-ttu-id="66f90-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66f90-153">RELATED LINKS</span></span>

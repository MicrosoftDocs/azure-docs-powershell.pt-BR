---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113996"
---
# <span data-ttu-id="6a391-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="6a391-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="6a391-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a391-102">SYNOPSIS</span></span>
<span data-ttu-id="6a391-103">Regenera as cadeias de conexão primárias ou secundárias para o namespace ou fila ou tópico do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6a391-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="6a391-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a391-104">SYNTAX</span></span>

### <span data-ttu-id="6a391-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a391-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a391-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a391-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a391-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a391-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a391-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a391-108">DESCRIPTION</span></span>
<span data-ttu-id="6a391-109">O **cmdlet New-AzServiceBusKey** gera novas cadeias de conexão primárias ou secundárias para o namespace ou fila ou regra de autorização ou fila especificada.</span><span class="sxs-lookup"><span data-stu-id="6a391-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="6a391-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a391-110">EXAMPLES</span></span>

### <span data-ttu-id="6a391-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a391-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6a391-112">Regenera as cadeias de conexão primárias ou secundárias do namespace.</span><span class="sxs-lookup"><span data-stu-id="6a391-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="6a391-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6a391-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6a391-114">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o namespace.</span><span class="sxs-lookup"><span data-stu-id="6a391-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="6a391-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6a391-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6a391-116">Regenera as cadeias de conexão primárias ou secundárias da fila.</span><span class="sxs-lookup"><span data-stu-id="6a391-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="6a391-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="6a391-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6a391-118">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para a fila.</span><span class="sxs-lookup"><span data-stu-id="6a391-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="6a391-119">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="6a391-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6a391-120">Regenera as cadeias de conexão primárias ou secundárias do tópico.</span><span class="sxs-lookup"><span data-stu-id="6a391-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="6a391-121">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="6a391-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6a391-122">Regenera as cadeias de conexão primárias ou secundárias com o valor de chave fornecido para o tópico.</span><span class="sxs-lookup"><span data-stu-id="6a391-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="6a391-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a391-123">PARAMETERS</span></span>

### <span data-ttu-id="6a391-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a391-124">-DefaultProfile</span></span>
<span data-ttu-id="6a391-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a391-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a391-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="6a391-126">-KeyValue</span></span>
<span data-ttu-id="6a391-127">Uma chave de 256 bits codificada com base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="6a391-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="6a391-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a391-128">-Name</span></span>
<span data-ttu-id="6a391-129">Nome de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="6a391-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6a391-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a391-130">-Namespace</span></span>
<span data-ttu-id="6a391-131">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6a391-131">Namespace Name</span></span>

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

### <span data-ttu-id="6a391-132">-Fila</span><span class="sxs-lookup"><span data-stu-id="6a391-132">-Queue</span></span>
<span data-ttu-id="6a391-133">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="6a391-133">Queue Name</span></span>

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

### <span data-ttu-id="6a391-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6a391-134">-RegenerateKey</span></span>
<span data-ttu-id="6a391-135">Chaves de regeneração - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="6a391-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="6a391-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a391-136">-ResourceGroupName</span></span>
<span data-ttu-id="6a391-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6a391-137">Resource Group Name</span></span>

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

### <span data-ttu-id="6a391-138">-Tópico</span><span class="sxs-lookup"><span data-stu-id="6a391-138">-Topic</span></span>
<span data-ttu-id="6a391-139">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="6a391-139">Topic Name</span></span>

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

### <span data-ttu-id="6a391-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6a391-140">-Confirm</span></span>
<span data-ttu-id="6a391-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a391-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a391-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a391-142">-WhatIf</span></span>
<span data-ttu-id="6a391-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6a391-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a391-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a391-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a391-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a391-145">CommonParameters</span></span>
<span data-ttu-id="6a391-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a391-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a391-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a391-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a391-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a391-148">INPUTS</span></span>

### <span data-ttu-id="6a391-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6a391-149">System.String</span></span>

## <span data-ttu-id="6a391-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a391-150">OUTPUTS</span></span>

### <span data-ttu-id="6a391-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6a391-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="6a391-152">Notas</span><span class="sxs-lookup"><span data-stu-id="6a391-152">NOTES</span></span>

## <span data-ttu-id="6a391-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a391-153">RELATED LINKS</span></span>

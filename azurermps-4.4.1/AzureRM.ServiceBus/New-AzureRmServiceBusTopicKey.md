---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429109"
---
# <span data-ttu-id="52615-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="52615-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="52615-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52615-102">SYNOPSIS</span></span>
<span data-ttu-id="52615-103">Regenera as cadeias de conexão primária ou secundária para o tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="52615-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52615-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52615-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52615-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52615-105">DESCRIPTION</span></span>
<span data-ttu-id="52615-106">O cmdlet **New-AzureRmServiceBusTopicKey** gera uma nova cadeia de conexão primária ou secundária para o tópico de barramento de serviço especificado e a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="52615-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="52615-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52615-107">EXAMPLES</span></span>

### <span data-ttu-id="52615-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52615-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="52615-109">Regenera a cadeia de caracteres de conexão principal para o namespace.</span><span class="sxs-lookup"><span data-stu-id="52615-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="52615-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52615-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="52615-111">Regenera a cadeia de conexão secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="52615-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="52615-112">OS</span><span class="sxs-lookup"><span data-stu-id="52615-112">PARAMETERS</span></span>

### <span data-ttu-id="52615-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="52615-113">-RegenerateKeys</span></span>
<span data-ttu-id="52615-114">Especifica se deve regenerar as chaves primárias ou secundárias.</span><span class="sxs-lookup"><span data-stu-id="52615-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52615-115">-Resource</span><span class="sxs-lookup"><span data-stu-id="52615-115">-ResourceGroup</span></span>
<span data-ttu-id="52615-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52615-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="52615-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52615-117">-Confirm</span></span>
<span data-ttu-id="52615-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52615-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52615-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52615-119">-WhatIf</span></span>
<span data-ttu-id="52615-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52615-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52615-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52615-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52615-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52615-122">-DefaultProfile</span></span>
<span data-ttu-id="52615-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52615-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52615-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="52615-124">-Name</span></span>
<span data-ttu-id="52615-125">Nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="52615-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52615-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52615-126">-Namespace</span></span>
<span data-ttu-id="52615-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="52615-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52615-128">-Tópico</span><span class="sxs-lookup"><span data-stu-id="52615-128">-Topic</span></span>
<span data-ttu-id="52615-129">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="52615-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52615-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52615-130">CommonParameters</span></span>
<span data-ttu-id="52615-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52615-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52615-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52615-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52615-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52615-133">INPUTS</span></span>

### <span data-ttu-id="52615-134">-Resource</span><span class="sxs-lookup"><span data-stu-id="52615-134">-ResourceGroup</span></span>
 <span data-ttu-id="52615-135">System. String</span><span class="sxs-lookup"><span data-stu-id="52615-135">System.String</span></span>
 

### <span data-ttu-id="52615-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="52615-136">-NamespaceName</span></span>
 <span data-ttu-id="52615-137">System. String</span><span class="sxs-lookup"><span data-stu-id="52615-137">System.String</span></span>
 

### <span data-ttu-id="52615-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="52615-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="52615-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52615-139">System.String</span></span>
 

### <span data-ttu-id="52615-140">-Topicname</span><span class="sxs-lookup"><span data-stu-id="52615-140">-TopicName</span></span>
 <span data-ttu-id="52615-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52615-141">System.String</span></span>
 

### <span data-ttu-id="52615-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="52615-142">-RegenerateKeys</span></span>
 <span data-ttu-id="52615-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52615-143">System.String</span></span>

## <span data-ttu-id="52615-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52615-144">OUTPUTS</span></span>

### <span data-ttu-id="52615-145">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="52615-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="52615-146">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey Value} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="52615-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="52615-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52615-147">NOTES</span></span>

## <span data-ttu-id="52615-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52615-148">RELATED LINKS</span></span>


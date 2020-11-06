---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427779"
---
# <span data-ttu-id="a87a2-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a87a2-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="a87a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a87a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a87a2-103">Remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a87a2-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a87a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a87a2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a87a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a87a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a87a2-106">O cmdlet **Remove-AzureRmServiceBusTopic** remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a87a2-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a87a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a87a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a87a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a87a2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="a87a2-109">Remove o tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a87a2-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a87a2-110">OS</span><span class="sxs-lookup"><span data-stu-id="a87a2-110">PARAMETERS</span></span>

### <span data-ttu-id="a87a2-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a87a2-111">-Confirm</span></span>
<span data-ttu-id="a87a2-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87a2-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87a2-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87a2-113">-WhatIf</span></span>
<span data-ttu-id="a87a2-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a87a2-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a87a2-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a87a2-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87a2-116">-DefaultProfile</span></span>
<span data-ttu-id="a87a2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a87a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a87a2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a87a2-118">-Name</span></span>
<span data-ttu-id="a87a2-119">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="a87a2-119">Topic Name.</span></span>

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

### <span data-ttu-id="a87a2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a87a2-120">-Namespace</span></span>
<span data-ttu-id="a87a2-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="a87a2-121">Namespace Name.</span></span>

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

### <span data-ttu-id="a87a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="a87a2-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a87a2-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87a2-124">CommonParameters</span></span>
<span data-ttu-id="a87a2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87a2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87a2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a87a2-127">INPUTS</span></span>

### <span data-ttu-id="a87a2-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="a87a2-128">-ResourceGroup</span></span>
 <span data-ttu-id="a87a2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a87a2-129">System.String</span></span>

### <span data-ttu-id="a87a2-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a87a2-130">-NamespaceName</span></span>
 <span data-ttu-id="a87a2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a87a2-131">System.String</span></span>

### <span data-ttu-id="a87a2-132">-Topicname</span><span class="sxs-lookup"><span data-stu-id="a87a2-132">-TopicName</span></span>
 <span data-ttu-id="a87a2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a87a2-133">System.String</span></span>

## <span data-ttu-id="a87a2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a87a2-134">OUTPUTS</span></span>

### <span data-ttu-id="a87a2-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="a87a2-135">System.Object</span></span>

## <span data-ttu-id="a87a2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a87a2-136">NOTES</span></span>

## <span data-ttu-id="a87a2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a87a2-137">RELATED LINKS</span></span>


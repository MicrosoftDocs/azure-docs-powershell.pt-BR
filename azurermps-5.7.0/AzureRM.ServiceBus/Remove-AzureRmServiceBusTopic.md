---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: f2d295d31b0112a2adf73e2e4be064164df8fbb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433409"
---
# <span data-ttu-id="283b5-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="283b5-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="283b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="283b5-102">SYNOPSIS</span></span>
<span data-ttu-id="283b5-103">Remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="283b5-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="283b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="283b5-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="283b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="283b5-105">DESCRIPTION</span></span>
<span data-ttu-id="283b5-106">O cmdlet **Remove-AzureRmServiceBusTopic** remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="283b5-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="283b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="283b5-107">EXAMPLES</span></span>

### <span data-ttu-id="283b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="283b5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="283b5-109">Remove o tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="283b5-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="283b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="283b5-110">PARAMETERS</span></span>

### <span data-ttu-id="283b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283b5-111">-DefaultProfile</span></span>
<span data-ttu-id="283b5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="283b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="283b5-113">-Name</span></span>
<span data-ttu-id="283b5-114">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="283b5-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="283b5-115">-Namespace</span></span>
<span data-ttu-id="283b5-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="283b5-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="283b5-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="283b5-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="283b5-119">-Confirm</span></span>
<span data-ttu-id="283b5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="283b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="283b5-121">-WhatIf</span></span>
<span data-ttu-id="283b5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="283b5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="283b5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="283b5-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283b5-124">CommonParameters</span></span>
<span data-ttu-id="283b5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283b5-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="283b5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283b5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="283b5-127">INPUTS</span></span>

### <span data-ttu-id="283b5-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="283b5-128">-ResourceGroup</span></span>
 <span data-ttu-id="283b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="283b5-129">System.String</span></span>

### <span data-ttu-id="283b5-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="283b5-130">-NamespaceName</span></span>
 <span data-ttu-id="283b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="283b5-131">System.String</span></span>

### <span data-ttu-id="283b5-132">-Topicname</span><span class="sxs-lookup"><span data-stu-id="283b5-132">-TopicName</span></span>
 <span data-ttu-id="283b5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="283b5-133">System.String</span></span>

## <span data-ttu-id="283b5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="283b5-134">OUTPUTS</span></span>

### <span data-ttu-id="283b5-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="283b5-135">System.Object</span></span>

## <span data-ttu-id="283b5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="283b5-136">NOTES</span></span>

## <span data-ttu-id="283b5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="283b5-137">RELATED LINKS</span></span>


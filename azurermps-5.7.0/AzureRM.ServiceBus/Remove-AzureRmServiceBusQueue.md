---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431604"
---
# <span data-ttu-id="456ae-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="456ae-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="456ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="456ae-102">SYNOPSIS</span></span>
<span data-ttu-id="456ae-103">Remove a fila do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="456ae-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="456ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="456ae-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="456ae-105">DESCRIPTION</span></span>
<span data-ttu-id="456ae-106">O cmdlet **Remove-AzureRmServiceBusQueue** remove a fila do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="456ae-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="456ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="456ae-107">EXAMPLES</span></span>

### <span data-ttu-id="456ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="456ae-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="456ae-109">Remove a fila `SB-Queue_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="456ae-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="456ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="456ae-110">PARAMETERS</span></span>

### <span data-ttu-id="456ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456ae-111">-DefaultProfile</span></span>
<span data-ttu-id="456ae-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="456ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="456ae-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="456ae-113">-Name</span></span>
<span data-ttu-id="456ae-114">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="456ae-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456ae-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="456ae-115">-Namespace</span></span>
<span data-ttu-id="456ae-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="456ae-116">Namespace Name.</span></span>

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

### <span data-ttu-id="456ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="456ae-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="456ae-118">The name of the resource group</span></span>

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

### <span data-ttu-id="456ae-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="456ae-119">-Confirm</span></span>
<span data-ttu-id="456ae-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="456ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456ae-121">-WhatIf</span></span>
<span data-ttu-id="456ae-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="456ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456ae-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="456ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456ae-124">CommonParameters</span></span>
<span data-ttu-id="456ae-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456ae-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456ae-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="456ae-127">INPUTS</span></span>

### <span data-ttu-id="456ae-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="456ae-128">-ResourceGroup</span></span>
 <span data-ttu-id="456ae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="456ae-129">System.String</span></span>

### <span data-ttu-id="456ae-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="456ae-130">-NamespaceName</span></span>
 <span data-ttu-id="456ae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="456ae-131">System.String</span></span>

### <span data-ttu-id="456ae-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="456ae-132">-QueueName</span></span>
 <span data-ttu-id="456ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="456ae-133">System.String</span></span>

## <span data-ttu-id="456ae-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="456ae-134">OUTPUTS</span></span>

### <span data-ttu-id="456ae-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="456ae-135">System.Object</span></span>

## <span data-ttu-id="456ae-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="456ae-136">NOTES</span></span>

## <span data-ttu-id="456ae-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="456ae-137">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113783"
---
# <span data-ttu-id="fd527-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fd527-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="fd527-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd527-102">SYNOPSIS</span></span>
<span data-ttu-id="fd527-103">Cria um grupo de consumidores eventhub.</span><span class="sxs-lookup"><span data-stu-id="fd527-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="fd527-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd527-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd527-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd527-105">DESCRIPTION</span></span>
<span data-ttu-id="fd527-106">Cria um grupo de consumidores no Eventhub associado ao IotHub especificado.</span><span class="sxs-lookup"><span data-stu-id="fd527-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="fd527-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd527-107">EXAMPLES</span></span>

### <span data-ttu-id="fd527-108">Exemplo 1: Adicionar um grupo de consumidores ao eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="fd527-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="fd527-109">Adiciona um novo grupo de consumidores chamado "myconsumergroup" ao eventhub para eventos de telemetria no iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fd527-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="fd527-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd527-110">PARAMETERS</span></span>

### <span data-ttu-id="fd527-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd527-111">-DefaultProfile</span></span>
<span data-ttu-id="fd527-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fd527-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd527-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="fd527-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="fd527-114">Nome do EventHub ConsumerGroup que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="fd527-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd527-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd527-115">-Name</span></span>
<span data-ttu-id="fd527-116">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="fd527-116">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd527-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd527-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd527-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="fd527-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="fd527-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd527-119">-Confirm</span></span>
<span data-ttu-id="fd527-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd527-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd527-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd527-121">-WhatIf</span></span>
<span data-ttu-id="fd527-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd527-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd527-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd527-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd527-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd527-124">CommonParameters</span></span>
<span data-ttu-id="fd527-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd527-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd527-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd527-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd527-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd527-127">INPUTS</span></span>

### <span data-ttu-id="fd527-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fd527-128">System.String</span></span>

## <span data-ttu-id="fd527-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd527-129">OUTPUTS</span></span>

### <span data-ttu-id="fd527-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fd527-130">System.String</span></span>

## <span data-ttu-id="fd527-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fd527-131">NOTES</span></span>

## <span data-ttu-id="fd527-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd527-132">RELATED LINKS</span></span>

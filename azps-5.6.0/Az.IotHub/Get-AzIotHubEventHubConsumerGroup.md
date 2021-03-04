---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889951"
---
# <span data-ttu-id="1c6a0-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1c6a0-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="1c6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6a0-103">Obtém todos os grupos de consumidores eventhub.</span><span class="sxs-lookup"><span data-stu-id="1c6a0-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="1c6a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1c6a0-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c6a0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1c6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6a0-106">Obtém todos os grupos de consumidores eventhub para os diferentes EventHubs usados pelo IotHub.</span><span class="sxs-lookup"><span data-stu-id="1c6a0-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="1c6a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-107">EXAMPLES</span></span>

### <span data-ttu-id="1c6a0-108">Exemplo 1 Obtém todos os grupos de consumidores eventhub para o eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="1c6a0-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1c6a0-109">Obtém todos os grupos de consumidores eventhub para o eventhub de telemetria para o iothub chamado myiothub</span><span class="sxs-lookup"><span data-stu-id="1c6a0-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="1c6a0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-110">PARAMETERS</span></span>

### <span data-ttu-id="1c6a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6a0-111">-DefaultProfile</span></span>
<span data-ttu-id="1c6a0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1c6a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6a0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1c6a0-113">-Name</span></span>
<span data-ttu-id="1c6a0-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="1c6a0-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="1c6a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c6a0-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1c6a0-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1c6a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6a0-117">CommonParameters</span></span>
<span data-ttu-id="1c6a0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6a0-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6a0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6a0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-120">INPUTS</span></span>

### <span data-ttu-id="1c6a0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1c6a0-121">System.String</span></span>

## <span data-ttu-id="1c6a0-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-122">OUTPUTS</span></span>

### <span data-ttu-id="1c6a0-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="1c6a0-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="1c6a0-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="1c6a0-124">NOTES</span></span>

## <span data-ttu-id="1c6a0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c6a0-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9934ea8ba32fc1d63353e83303cfe8371629bca1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775843"
---
# <span data-ttu-id="a348b-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a348b-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="a348b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a348b-102">SYNOPSIS</span></span>
<span data-ttu-id="a348b-103">Obtém todas as consumergroups do eventhub.</span><span class="sxs-lookup"><span data-stu-id="a348b-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="a348b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a348b-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a348b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a348b-105">DESCRIPTION</span></span>
<span data-ttu-id="a348b-106">Obtém todos os consumergroups do eventhub para os diferentes EventHubs usados pelo IotHub.</span><span class="sxs-lookup"><span data-stu-id="a348b-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="a348b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a348b-107">EXAMPLES</span></span>

### <span data-ttu-id="a348b-108">O exemplo 1 Obtém todos os consumergroups do eventhub para o eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="a348b-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a348b-109">Obtém todos os consumergroups do eventhub para o eventhub do iothub chamado myiothub</span><span class="sxs-lookup"><span data-stu-id="a348b-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="a348b-110">OS</span><span class="sxs-lookup"><span data-stu-id="a348b-110">PARAMETERS</span></span>

### <span data-ttu-id="a348b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a348b-111">-DefaultProfile</span></span>
<span data-ttu-id="a348b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a348b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a348b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a348b-113">-Name</span></span>
<span data-ttu-id="a348b-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="a348b-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="a348b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a348b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a348b-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a348b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a348b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a348b-117">CommonParameters</span></span>
<span data-ttu-id="a348b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a348b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a348b-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a348b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a348b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a348b-120">INPUTS</span></span>

### <span data-ttu-id="a348b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a348b-121">System.String</span></span>

## <span data-ttu-id="a348b-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a348b-122">OUTPUTS</span></span>

### <span data-ttu-id="a348b-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="a348b-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="a348b-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a348b-124">NOTES</span></span>

## <span data-ttu-id="a348b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a348b-125">RELATED LINKS</span></span>

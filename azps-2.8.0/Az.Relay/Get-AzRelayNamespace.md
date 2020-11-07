---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: 3ef4934ce98b48051f052e2644dc7707fe89650f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773400"
---
# <span data-ttu-id="0e35e-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="0e35e-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="0e35e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e35e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e35e-103">Obtém uma descrição para o namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e35e-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="0e35e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e35e-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e35e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e35e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e35e-106">O cmdlet **Get-AzRelayNamespace** Obtém uma descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e35e-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="0e35e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e35e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e35e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e35e-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="0e35e-109">Retorna uma descrição do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="0e35e-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="0e35e-110">OS</span><span class="sxs-lookup"><span data-stu-id="0e35e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e35e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e35e-111">-DefaultProfile</span></span>
<span data-ttu-id="0e35e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e35e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e35e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e35e-113">-Name</span></span>
<span data-ttu-id="0e35e-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="0e35e-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e35e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e35e-115">-ResourceGroupName</span></span>
<span data-ttu-id="0e35e-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e35e-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e35e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e35e-117">CommonParameters</span></span>
<span data-ttu-id="0e35e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e35e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e35e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e35e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e35e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e35e-120">INPUTS</span></span>

### <span data-ttu-id="0e35e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0e35e-121">System.String</span></span>

## <span data-ttu-id="0e35e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e35e-122">OUTPUTS</span></span>

### <span data-ttu-id="0e35e-123">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0e35e-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="0e35e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e35e-124">NOTES</span></span>

## <span data-ttu-id="0e35e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e35e-125">RELATED LINKS</span></span>

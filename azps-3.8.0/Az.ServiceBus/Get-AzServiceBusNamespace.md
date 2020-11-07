---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943741"
---
# <span data-ttu-id="39e68-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="39e68-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="39e68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39e68-102">SYNOPSIS</span></span>
<span data-ttu-id="39e68-103">Obtém uma descrição para o namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39e68-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="39e68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39e68-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39e68-105">DESCRIPTION</span></span>
<span data-ttu-id="39e68-106">O cmdlet **Get-AzServiceBusNamespace** Obtém uma descrição do namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39e68-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="39e68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39e68-107">EXAMPLES</span></span>

### <span data-ttu-id="39e68-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39e68-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="39e68-109">OS</span><span class="sxs-lookup"><span data-stu-id="39e68-109">PARAMETERS</span></span>

### <span data-ttu-id="39e68-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e68-110">-DefaultProfile</span></span>
<span data-ttu-id="39e68-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39e68-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e68-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="39e68-112">-Name</span></span>
<span data-ttu-id="39e68-113">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="39e68-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e68-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e68-114">-ResourceGroupName</span></span>
<span data-ttu-id="39e68-115">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="39e68-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e68-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e68-116">CommonParameters</span></span>
<span data-ttu-id="39e68-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e68-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e68-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e68-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e68-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39e68-119">INPUTS</span></span>

### <span data-ttu-id="39e68-120">System. String</span><span class="sxs-lookup"><span data-stu-id="39e68-120">System.String</span></span>

## <span data-ttu-id="39e68-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39e68-121">OUTPUTS</span></span>

### <span data-ttu-id="39e68-122">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="39e68-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="39e68-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39e68-123">NOTES</span></span>

## <span data-ttu-id="39e68-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39e68-124">RELATED LINKS</span></span>

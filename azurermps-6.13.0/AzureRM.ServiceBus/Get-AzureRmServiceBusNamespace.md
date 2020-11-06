---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 37d142947c09c211c947f3bd80455a812f96844f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429340"
---
# <span data-ttu-id="bba20-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bba20-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="bba20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bba20-102">SYNOPSIS</span></span>
<span data-ttu-id="bba20-103">Obtém uma descrição para o namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bba20-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bba20-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bba20-105">DESCRIPTION</span></span>
<span data-ttu-id="bba20-106">O cmdlet **Get-AzureRmServiceBusNamespace** Obtém uma descrição do namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bba20-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="bba20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bba20-107">EXAMPLES</span></span>

### <span data-ttu-id="bba20-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bba20-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="bba20-109">OS</span><span class="sxs-lookup"><span data-stu-id="bba20-109">PARAMETERS</span></span>

### <span data-ttu-id="bba20-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba20-110">-DefaultProfile</span></span>
<span data-ttu-id="bba20-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bba20-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba20-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="bba20-112">-Name</span></span>
<span data-ttu-id="bba20-113">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="bba20-113">Namespace Name.</span></span>

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

### <span data-ttu-id="bba20-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba20-114">-ResourceGroupName</span></span>
<span data-ttu-id="bba20-115">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bba20-115">The name of the resource group</span></span>

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

### <span data-ttu-id="bba20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba20-116">CommonParameters</span></span>
<span data-ttu-id="bba20-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba20-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba20-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba20-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bba20-119">INPUTS</span></span>

### <span data-ttu-id="bba20-120">System. String</span><span class="sxs-lookup"><span data-stu-id="bba20-120">System.String</span></span>

## <span data-ttu-id="bba20-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bba20-121">OUTPUTS</span></span>

### <span data-ttu-id="bba20-122">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bba20-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bba20-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bba20-123">NOTES</span></span>

## <span data-ttu-id="bba20-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bba20-124">RELATED LINKS</span></span>

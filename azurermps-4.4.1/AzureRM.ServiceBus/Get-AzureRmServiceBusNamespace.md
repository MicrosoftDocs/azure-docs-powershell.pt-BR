---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602194"
---
# <span data-ttu-id="5b11e-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5b11e-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="5b11e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b11e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b11e-103">Obtém uma descrição para o namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b11e-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b11e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b11e-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b11e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b11e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b11e-106">O cmdlet **Get-AzureRmServiceBusNamespace** Obtém uma descrição do namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b11e-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="5b11e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b11e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b11e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b11e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="5b11e-109">Retorna uma descrição do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="5b11e-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5b11e-110">OS</span><span class="sxs-lookup"><span data-stu-id="5b11e-110">PARAMETERS</span></span>

### <span data-ttu-id="5b11e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b11e-111">-DefaultProfile</span></span>
<span data-ttu-id="5b11e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b11e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b11e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b11e-113">-Name</span></span>
<span data-ttu-id="5b11e-114">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="5b11e-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b11e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b11e-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5b11e-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b11e-117">CommonParameters</span></span>
<span data-ttu-id="5b11e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b11e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b11e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b11e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b11e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b11e-120">INPUTS</span></span>

### <span data-ttu-id="5b11e-121">-Resource</span><span class="sxs-lookup"><span data-stu-id="5b11e-121">-ResourceGroup</span></span>
<span data-ttu-id="5b11e-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5b11e-122">System.String</span></span>

### <span data-ttu-id="5b11e-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5b11e-123">-NamespaceName</span></span>
 <span data-ttu-id="5b11e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5b11e-124">System.String</span></span>

## <span data-ttu-id="5b11e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b11e-125">OUTPUTS</span></span>

### <span data-ttu-id="5b11e-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. Namespaceattributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5b11e-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5b11e-127">Nome: SB-Example1 ID: local do/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1: SKU EUA: nome: padrão, capacidade: 1, camada: ProvisioningState padrão: status com êxito: disponível para CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ Enabled: true</span><span class="sxs-lookup"><span data-stu-id="5b11e-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="5b11e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b11e-128">NOTES</span></span>
## <span data-ttu-id="5b11e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b11e-129">RELATED LINKS</span></span>

## <span data-ttu-id="5b11e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b11e-130">RELATED LINKS</span></span>


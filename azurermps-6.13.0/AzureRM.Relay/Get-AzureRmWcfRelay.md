---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 342c18add7438c75babd1225722c3830c4c5c696
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427190"
---
# <span data-ttu-id="98a03-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="98a03-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="98a03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98a03-102">SYNOPSIS</span></span>
<span data-ttu-id="98a03-103">Retorna uma descrição para o WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="98a03-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98a03-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a03-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98a03-105">DESCRIPTION</span></span>
<span data-ttu-id="98a03-106">O cmdlet **Get-AzureRmWcfRelay** retorna uma descrição do WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="98a03-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="98a03-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98a03-107">EXAMPLES</span></span>

### <span data-ttu-id="98a03-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98a03-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="98a03-109">Retorna a descrição do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="98a03-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="98a03-110">OS</span><span class="sxs-lookup"><span data-stu-id="98a03-110">PARAMETERS</span></span>

### <span data-ttu-id="98a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a03-111">-DefaultProfile</span></span>
<span data-ttu-id="98a03-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98a03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a03-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="98a03-113">-Name</span></span>
<span data-ttu-id="98a03-114">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="98a03-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a03-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98a03-115">-Namespace</span></span>
<span data-ttu-id="98a03-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="98a03-116">Namespace Name.</span></span>

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

### <span data-ttu-id="98a03-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a03-117">-ResourceGroupName</span></span>
<span data-ttu-id="98a03-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98a03-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="98a03-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a03-119">CommonParameters</span></span>
<span data-ttu-id="98a03-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a03-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98a03-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a03-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a03-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98a03-122">INPUTS</span></span>

### <span data-ttu-id="98a03-123">System. String</span><span class="sxs-lookup"><span data-stu-id="98a03-123">System.String</span></span>


## <span data-ttu-id="98a03-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98a03-124">OUTPUTS</span></span>

### <span data-ttu-id="98a03-125">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="98a03-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="98a03-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98a03-126">NOTES</span></span>

## <span data-ttu-id="98a03-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98a03-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439832"
---
# <span data-ttu-id="0e718-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="0e718-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="0e718-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e718-102">SYNOPSIS</span></span>
<span data-ttu-id="0e718-103">Retorna uma descrição para o WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="0e718-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e718-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e718-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e718-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e718-105">DESCRIPTION</span></span>
<span data-ttu-id="0e718-106">O cmdlet **Get-AzureRmWcfRelay** retorna uma descrição do WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="0e718-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="0e718-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e718-107">EXAMPLES</span></span>

### <span data-ttu-id="0e718-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e718-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="0e718-109">Retorna a descrição do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="0e718-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="0e718-110">OS</span><span class="sxs-lookup"><span data-stu-id="0e718-110">PARAMETERS</span></span>

### <span data-ttu-id="0e718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e718-111">-DefaultProfile</span></span>
<span data-ttu-id="0e718-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e718-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e718-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e718-113">-Name</span></span>
<span data-ttu-id="0e718-114">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="0e718-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e718-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e718-115">-Namespace</span></span>
<span data-ttu-id="0e718-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="0e718-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e718-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e718-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e718-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e718-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e718-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e718-119">CommonParameters</span></span>
<span data-ttu-id="0e718-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e718-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e718-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e718-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e718-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e718-122">INPUTS</span></span>

### <span data-ttu-id="0e718-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e718-123">-ResourceGroupName</span></span>
 <span data-ttu-id="0e718-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0e718-124">System.String</span></span>
 

### <span data-ttu-id="0e718-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e718-125">-Namespace</span></span>
 <span data-ttu-id="0e718-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0e718-126">System.String</span></span>
 

### <span data-ttu-id="0e718-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e718-127">-Name</span></span>
 <span data-ttu-id="0e718-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0e718-128">System.String</span></span> 

## <span data-ttu-id="0e718-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e718-129">OUTPUTS</span></span>

### <span data-ttu-id="0e718-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0e718-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0e718-131">Relaytype: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false usermetadata: ID de metadados do usuário:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name: TestWCFRelay1 tipo: Microsoft. retransmissor/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="0e718-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="0e718-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e718-132">NOTES</span></span>

## <span data-ttu-id="0e718-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e718-133">RELATED LINKS</span></span>


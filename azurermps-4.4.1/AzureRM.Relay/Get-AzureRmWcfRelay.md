---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 81463fc5202c9b5990e5d73d81c7bc2cbeadcca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430667"
---
# <span data-ttu-id="16c89-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="16c89-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="16c89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16c89-102">SYNOPSIS</span></span>
<span data-ttu-id="16c89-103">Retorna uma descrição para o WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="16c89-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16c89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16c89-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16c89-105">DESCRIPTION</span></span>
<span data-ttu-id="16c89-106">O cmdlet **Get-AzureRmWcfRelay** retorna uma descrição do WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="16c89-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="16c89-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16c89-107">EXAMPLES</span></span>

### <span data-ttu-id="16c89-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16c89-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="16c89-109">Retorna a descrição do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="16c89-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="16c89-110">OS</span><span class="sxs-lookup"><span data-stu-id="16c89-110">PARAMETERS</span></span>

### <span data-ttu-id="16c89-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16c89-111">-Namespace</span></span>
<span data-ttu-id="16c89-112">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="16c89-112">Namespace Name.</span></span>

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

### <span data-ttu-id="16c89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c89-113">-ResourceGroupName</span></span>
<span data-ttu-id="16c89-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16c89-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="16c89-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="16c89-115">-Name</span></span>
<span data-ttu-id="16c89-116">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="16c89-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="16c89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c89-117">-DefaultProfile</span></span>
<span data-ttu-id="16c89-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16c89-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c89-119">CommonParameters</span></span>
<span data-ttu-id="16c89-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c89-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c89-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c89-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16c89-122">INPUTS</span></span>

### <span data-ttu-id="16c89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c89-123">-ResourceGroupName</span></span>
 <span data-ttu-id="16c89-124">System. String</span><span class="sxs-lookup"><span data-stu-id="16c89-124">System.String</span></span>
 

### <span data-ttu-id="16c89-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16c89-125">-Namespace</span></span>
 <span data-ttu-id="16c89-126">System. String</span><span class="sxs-lookup"><span data-stu-id="16c89-126">System.String</span></span>
 

### <span data-ttu-id="16c89-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="16c89-127">-Name</span></span>
 <span data-ttu-id="16c89-128">System. String</span><span class="sxs-lookup"><span data-stu-id="16c89-128">System.String</span></span> 

## <span data-ttu-id="16c89-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16c89-129">OUTPUTS</span></span>

### <span data-ttu-id="16c89-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16c89-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="16c89-131">Relaytype: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false usermetadata: ID de metadados do usuário:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name: TestWCFRelay1 tipo: Microsoft. retransmissor/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="16c89-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="16c89-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16c89-132">NOTES</span></span>

## <span data-ttu-id="16c89-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16c89-133">RELATED LINKS</span></span>

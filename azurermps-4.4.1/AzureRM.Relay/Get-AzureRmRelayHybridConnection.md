---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429141"
---
# <span data-ttu-id="c96a1-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="c96a1-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="c96a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c96a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c96a1-103">Obtém uma descrição para o HybridConnection especificado no namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c96a1-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c96a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c96a1-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c96a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c96a1-106">O cmdlet **Get-AzureRmRelayHybridConnection** Obtém uma descrição do HybridConnection especificado no namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c96a1-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="c96a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c96a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c96a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c96a1-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="c96a1-109">Retorna a descrição do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="c96a1-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="c96a1-110">OS</span><span class="sxs-lookup"><span data-stu-id="c96a1-110">PARAMETERS</span></span>

### <span data-ttu-id="c96a1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c96a1-111">-Name</span></span>
<span data-ttu-id="c96a1-112">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="c96a1-112">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96a1-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c96a1-113">-Namespace</span></span>
<span data-ttu-id="c96a1-114">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c96a1-114">Namespace Name.</span></span>

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

### <span data-ttu-id="c96a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c96a1-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c96a1-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="c96a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96a1-117">-DefaultProfile</span></span>
<span data-ttu-id="c96a1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c96a1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c96a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96a1-119">CommonParameters</span></span>
<span data-ttu-id="c96a1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96a1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96a1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c96a1-122">INPUTS</span></span>

### <span data-ttu-id="c96a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96a1-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="c96a1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c96a1-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="c96a1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c96a1-125">-Name</span></span>
    System.String

## <span data-ttu-id="c96a1-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c96a1-126">OUTPUTS</span></span>

### <span data-ttu-id="c96a1-127">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c96a1-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c96a1-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 ListenerCount: 0 RequiresClientAuthorization: verdadeiro usermetadata: ID de meta dados do usuário:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection nome: TestHybridConnection tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="c96a1-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="c96a1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c96a1-129">NOTES</span></span>

## <span data-ttu-id="c96a1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c96a1-130">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427392"
---
# <span data-ttu-id="edf52-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="edf52-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="edf52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edf52-102">SYNOPSIS</span></span>
<span data-ttu-id="edf52-103">Obtém uma descrição para o HybridConnection especificado no namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="edf52-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="edf52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edf52-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edf52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edf52-105">DESCRIPTION</span></span>
<span data-ttu-id="edf52-106">O cmdlet **Get-AzRelayHybridConnection** Obtém uma descrição do HybridConnection especificado no namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="edf52-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="edf52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edf52-107">EXAMPLES</span></span>

### <span data-ttu-id="edf52-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="edf52-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="edf52-109">Retorna a descrição do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="edf52-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="edf52-110">OS</span><span class="sxs-lookup"><span data-stu-id="edf52-110">PARAMETERS</span></span>

### <span data-ttu-id="edf52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf52-111">-DefaultProfile</span></span>
<span data-ttu-id="edf52-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edf52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf52-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="edf52-113">-Name</span></span>
<span data-ttu-id="edf52-114">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="edf52-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="edf52-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="edf52-115">-Namespace</span></span>
<span data-ttu-id="edf52-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="edf52-116">Namespace Name.</span></span>

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

### <span data-ttu-id="edf52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf52-117">-ResourceGroupName</span></span>
<span data-ttu-id="edf52-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="edf52-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="edf52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf52-119">CommonParameters</span></span>
<span data-ttu-id="edf52-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf52-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf52-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf52-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edf52-122">INPUTS</span></span>

### <span data-ttu-id="edf52-123">System. String</span><span class="sxs-lookup"><span data-stu-id="edf52-123">System.String</span></span>

## <span data-ttu-id="edf52-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edf52-124">OUTPUTS</span></span>

### <span data-ttu-id="edf52-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="edf52-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="edf52-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edf52-126">NOTES</span></span>

## <span data-ttu-id="edf52-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edf52-127">RELATED LINKS</span></span>

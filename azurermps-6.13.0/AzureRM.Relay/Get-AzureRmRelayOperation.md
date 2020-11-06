---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: e7f45be6a39cdd2b7f2d11736d2a5f62831244c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429388"
---
# <span data-ttu-id="bc51c-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="bc51c-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="bc51c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc51c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc51c-103">Lista de operações de retransmissão aceitas</span><span class="sxs-lookup"><span data-stu-id="bc51c-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc51c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc51c-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc51c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc51c-105">DESCRIPTION</span></span>
<span data-ttu-id="bc51c-106">O cmdlet **Get-AzureRmRelayOperation** lista as operações com suporte para retransmissão.</span><span class="sxs-lookup"><span data-stu-id="bc51c-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="bc51c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc51c-107">EXAMPLES</span></span>

### <span data-ttu-id="bc51c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc51c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="bc51c-109">Lista as operações aceitas de retransmissão</span><span class="sxs-lookup"><span data-stu-id="bc51c-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="bc51c-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc51c-110">PARAMETERS</span></span>

### <span data-ttu-id="bc51c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc51c-111">-DefaultProfile</span></span>
<span data-ttu-id="bc51c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc51c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc51c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc51c-113">CommonParameters</span></span>
<span data-ttu-id="bc51c-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc51c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bc51c-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc51c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc51c-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc51c-116">INPUTS</span></span>

### <span data-ttu-id="bc51c-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bc51c-117">None</span></span>


## <span data-ttu-id="bc51c-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc51c-118">OUTPUTS</span></span>

### <span data-ttu-id="bc51c-119">Microsoft. Azure. Commands. Relay. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="bc51c-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>


## <span data-ttu-id="bc51c-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc51c-120">NOTES</span></span>

## <span data-ttu-id="bc51c-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc51c-121">RELATED LINKS</span></span>

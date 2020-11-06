---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 166dbf5520531ec5a77fbc1e7017738d7201f664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599511"
---
# <span data-ttu-id="1ccb5-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="1ccb5-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="1ccb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ccb5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccb5-103">Lista de operações de retransmissão aceitas</span><span class="sxs-lookup"><span data-stu-id="1ccb5-103">List supported Relay Operations</span></span>

## <span data-ttu-id="1ccb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ccb5-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ccb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ccb5-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccb5-106">O cmdlet **Get-AzRelayOperation** lista as operações com suporte para retransmissão.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="1ccb5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ccb5-107">EXAMPLES</span></span>

### <span data-ttu-id="1ccb5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ccb5-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

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

<span data-ttu-id="1ccb5-109">Lista as operações aceitas de retransmissão</span><span class="sxs-lookup"><span data-stu-id="1ccb5-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="1ccb5-110">OS</span><span class="sxs-lookup"><span data-stu-id="1ccb5-110">PARAMETERS</span></span>

### <span data-ttu-id="1ccb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccb5-111">-DefaultProfile</span></span>
<span data-ttu-id="1ccb5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ccb5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccb5-113">CommonParameters</span></span>
<span data-ttu-id="1ccb5-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccb5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccb5-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ccb5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccb5-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ccb5-116">INPUTS</span></span>

### <span data-ttu-id="1ccb5-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ccb5-117">None</span></span>

## <span data-ttu-id="1ccb5-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ccb5-118">OUTPUTS</span></span>

### <span data-ttu-id="1ccb5-119">Microsoft. Azure. Commands. Relay. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="1ccb5-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="1ccb5-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ccb5-120">NOTES</span></span>

## <span data-ttu-id="1ccb5-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ccb5-121">RELATED LINKS</span></span>

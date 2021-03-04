---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: e998bb09435abc787df78050ab25888d0e6651a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891725"
---
# <span data-ttu-id="0f4f7-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="0f4f7-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="0f4f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4f7-103">Retorna uma descrição para o WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="0f4f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f4f7-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4f7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="0f4f7-106">O cmdlet **Get-AzWcfRelay** retorna uma descrição do WcfRelay especificado.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="0f4f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="0f4f7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f4f7-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

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

<span data-ttu-id="0f4f7-109">Retorna a descrição do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="0f4f7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-110">PARAMETERS</span></span>

### <span data-ttu-id="0f4f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4f7-111">-DefaultProfile</span></span>
<span data-ttu-id="0f4f7-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f4f7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0f4f7-113">-Name</span></span>
<span data-ttu-id="0f4f7-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="0f4f7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f4f7-115">-Namespace</span></span>
<span data-ttu-id="0f4f7-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-116">Namespace Name.</span></span>

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

### <span data-ttu-id="0f4f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f4f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f4f7-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f4f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4f7-119">CommonParameters</span></span>
<span data-ttu-id="0f4f7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4f7-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4f7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4f7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-122">INPUTS</span></span>

### <span data-ttu-id="0f4f7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0f4f7-123">System.String</span></span>

## <span data-ttu-id="0f4f7-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-124">OUTPUTS</span></span>

### <span data-ttu-id="0f4f7-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="0f4f7-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="0f4f7-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f4f7-126">NOTES</span></span>

## <span data-ttu-id="0f4f7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f4f7-127">RELATED LINKS</span></span>

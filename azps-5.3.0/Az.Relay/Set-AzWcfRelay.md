---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428019"
---
# <span data-ttu-id="bb1d6-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="bb1d6-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="bb1d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1d6-103">Atualiza a descrição de um WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="bb1d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb1d6-104">SYNTAX</span></span>

### <span data-ttu-id="bb1d6-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb1d6-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb1d6-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="bb1d6-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb1d6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb1d6-107">DESCRIPTION</span></span>
<span data-ttu-id="bb1d6-108">O cmdlet Set-AzWcfRelay atualiza a descrição do WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="bb1d6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb1d6-109">EXAMPLES</span></span>

### <span data-ttu-id="bb1d6-110">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb1d6-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="bb1d6-111">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb1d6-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="bb1d6-112">Atualiza o WcfRelay especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="bb1d6-113">Este exemplo atualiza a propriedade usermetadata com novo valor.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="bb1d6-114">OS</span><span class="sxs-lookup"><span data-stu-id="bb1d6-114">PARAMETERS</span></span>

### <span data-ttu-id="bb1d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1d6-115">-DefaultProfile</span></span>
<span data-ttu-id="bb1d6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1d6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb1d6-117">-InputObject</span></span>
<span data-ttu-id="bb1d6-118">Objeto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1d6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb1d6-119">-Name</span></span>
<span data-ttu-id="bb1d6-120">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1d6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb1d6-121">-Namespace</span></span>
<span data-ttu-id="bb1d6-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-122">Namespace Name.</span></span>

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

### <span data-ttu-id="bb1d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb1d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb1d6-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="bb1d6-125">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="bb1d6-125">-UserMetadata</span></span>
<span data-ttu-id="bb1d6-126">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade WcfRelay. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1d6-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb1d6-127">-Confirm</span></span>
<span data-ttu-id="bb1d6-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1d6-129">-WhatIf</span></span>
<span data-ttu-id="bb1d6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1d6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1d6-132">CommonParameters</span></span>
<span data-ttu-id="bb1d6-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1d6-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1d6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1d6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb1d6-135">INPUTS</span></span>

### <span data-ttu-id="bb1d6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bb1d6-136">System.String</span></span>

### <span data-ttu-id="bb1d6-137">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="bb1d6-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="bb1d6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb1d6-138">OUTPUTS</span></span>

### <span data-ttu-id="bb1d6-139">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="bb1d6-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="bb1d6-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb1d6-140">NOTES</span></span>

## <span data-ttu-id="bb1d6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb1d6-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 837c6e69f2b01ec0ae8de8ed7a711a041096dd2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891711"
---
# <span data-ttu-id="10215-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="10215-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="10215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10215-102">SYNOPSIS</span></span>
<span data-ttu-id="10215-103">Cria um WcfRelay no namespace Relay especificado.</span><span class="sxs-lookup"><span data-stu-id="10215-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="10215-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10215-104">SYNTAX</span></span>

### <span data-ttu-id="10215-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10215-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10215-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="10215-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10215-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10215-107">DESCRIPTION</span></span>
<span data-ttu-id="10215-108">O New-AzWcfRelay cmdlet cria um WcfRelay no namespace Relay especificado.</span><span class="sxs-lookup"><span data-stu-id="10215-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="10215-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10215-109">EXAMPLES</span></span>

### <span data-ttu-id="10215-110">Exemplo 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="10215-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="10215-111">Cria um novo WcfRelay \` TestWCFRelay2 no \` namespace De retransmissão \` especificado TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="10215-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="10215-112">Exemplo 2 - Propriedades</span><span class="sxs-lookup"><span data-stu-id="10215-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="10215-113">Cria um novo WcfRelay TestWCFRelay no namespace De retransmissão \` \` especificado \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="10215-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="10215-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10215-114">PARAMETERS</span></span>

### <span data-ttu-id="10215-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10215-115">-DefaultProfile</span></span>
<span data-ttu-id="10215-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10215-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10215-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10215-117">-InputObject</span></span>
<span data-ttu-id="10215-118">Objeto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="10215-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="10215-119">-Name</span><span class="sxs-lookup"><span data-stu-id="10215-119">-Name</span></span>
<span data-ttu-id="10215-120">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="10215-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="10215-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="10215-121">-Namespace</span></span>
<span data-ttu-id="10215-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="10215-122">Namespace Name.</span></span>

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

### <span data-ttu-id="10215-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="10215-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="10215-124">true se a autorização do cliente for necessária para essa retransmissão; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="10215-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10215-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="10215-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="10215-126">true se a segurança de transporte for necessária para essa retransmissão; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="10215-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10215-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10215-127">-ResourceGroupName</span></span>
<span data-ttu-id="10215-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="10215-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="10215-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="10215-129">-UserMetadata</span></span>
<span data-ttu-id="10215-130">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection.por exemplo. ele pode ser usado para armazenar dados descritivos, como lista de equipes e suas informações de contato também podem ser armazenadas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="10215-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="10215-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="10215-131">-WcfRelayType</span></span>
<span data-ttu-id="10215-132">Tipo WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="10215-132">WcfRelay Type.</span></span>
<span data-ttu-id="10215-133">Os valores possíveis incluem: 'NetTcp' ou 'Http'</span><span class="sxs-lookup"><span data-stu-id="10215-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10215-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10215-134">-Confirm</span></span>
<span data-ttu-id="10215-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10215-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10215-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10215-136">-WhatIf</span></span>
<span data-ttu-id="10215-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10215-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10215-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10215-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10215-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10215-139">CommonParameters</span></span>
<span data-ttu-id="10215-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10215-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10215-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10215-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10215-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10215-142">INPUTS</span></span>

### <span data-ttu-id="10215-143">System.String</span><span class="sxs-lookup"><span data-stu-id="10215-143">System.String</span></span>

### <span data-ttu-id="10215-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="10215-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="10215-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10215-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="10215-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10215-146">OUTPUTS</span></span>

### <span data-ttu-id="10215-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="10215-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="10215-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="10215-148">NOTES</span></span>

## <span data-ttu-id="10215-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10215-149">RELATED LINKS</span></span>

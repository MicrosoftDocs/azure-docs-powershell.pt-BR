---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427177"
---
# <span data-ttu-id="fcb49-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="fcb49-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="fcb49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcb49-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb49-103">Cria um WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="fcb49-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcb49-104">SYNTAX</span></span>

### <span data-ttu-id="fcb49-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fcb49-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcb49-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fcb49-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcb49-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb49-108">O cmdlet New-AzureRmWcfRelay cria um WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="fcb49-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fcb49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcb49-109">EXAMPLES</span></span>

### <span data-ttu-id="fcb49-110">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb49-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

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

<span data-ttu-id="fcb49-111">Cria um novo WcfRelay \` TestWCFRelay2 \` no namespace de retransmissão especificado \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="fcb49-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="fcb49-112">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcb49-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

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

<span data-ttu-id="fcb49-113">Cria um novo WcfRelay \` TestWCFRelay \` no namespace de retransmissão especificado \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="fcb49-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="fcb49-114">OS</span><span class="sxs-lookup"><span data-stu-id="fcb49-114">PARAMETERS</span></span>

### <span data-ttu-id="fcb49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb49-115">-DefaultProfile</span></span>
<span data-ttu-id="fcb49-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb49-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb49-117">-InputObject</span></span>
<span data-ttu-id="fcb49-118">Objeto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fcb49-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="fcb49-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcb49-119">-Name</span></span>
<span data-ttu-id="fcb49-120">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fcb49-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="fcb49-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcb49-121">-Namespace</span></span>
<span data-ttu-id="fcb49-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="fcb49-122">Namespace Name.</span></span>

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

### <span data-ttu-id="fcb49-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="fcb49-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="fcb49-124">verdadeiro se for necessária a autorização do cliente para este retransmissor; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="fcb49-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="fcb49-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="fcb49-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="fcb49-126">verdadeiro se a segurança de transporte for necessária para esse retransmissor; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="fcb49-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="fcb49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb49-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcb49-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcb49-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcb49-129">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="fcb49-129">-UserMetadata</span></span>
<span data-ttu-id="fcb49-130">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fcb49-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="fcb49-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="fcb49-131">-WcfRelayType</span></span>
<span data-ttu-id="fcb49-132">Tipo de WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fcb49-132">WcfRelay Type.</span></span>
<span data-ttu-id="fcb49-133">Os valores possíveis incluem: ' NetTcp ' ou ' http '</span><span class="sxs-lookup"><span data-stu-id="fcb49-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="fcb49-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcb49-134">-Confirm</span></span>
<span data-ttu-id="fcb49-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb49-136">-WhatIf</span></span>
<span data-ttu-id="fcb49-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcb49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb49-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcb49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb49-139">CommonParameters</span></span>
<span data-ttu-id="fcb49-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fcb49-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb49-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb49-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcb49-142">INPUTS</span></span>

### <span data-ttu-id="fcb49-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb49-143">System.String</span></span>
<span data-ttu-id="fcb49-144">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fcb49-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="fcb49-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcb49-145">OUTPUTS</span></span>

### <span data-ttu-id="fcb49-146">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="fcb49-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="fcb49-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcb49-147">NOTES</span></span>

## <span data-ttu-id="fcb49-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcb49-148">RELATED LINKS</span></span>

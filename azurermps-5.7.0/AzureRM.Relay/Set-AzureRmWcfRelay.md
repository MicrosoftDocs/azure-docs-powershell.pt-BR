---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428805"
---
# <span data-ttu-id="2edd9-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="2edd9-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="2edd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2edd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2edd9-103">Atualiza a descrição de um WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="2edd9-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2edd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2edd9-104">SYNTAX</span></span>

### <span data-ttu-id="2edd9-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2edd9-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2edd9-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2edd9-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edd9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2edd9-107">DESCRIPTION</span></span>
<span data-ttu-id="2edd9-108">O cmdlet Set-AzureRmWcfRelay atualiza a descrição do WcfRelay no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="2edd9-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="2edd9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2edd9-109">EXAMPLES</span></span>

### <span data-ttu-id="2edd9-110">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edd9-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="2edd9-111">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="2edd9-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="2edd9-112">Atualiza o WcfRelay especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="2edd9-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="2edd9-113">Este exemplo atualiza a propriedade usermetadata com novo valor.</span><span class="sxs-lookup"><span data-stu-id="2edd9-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="2edd9-114">OS</span><span class="sxs-lookup"><span data-stu-id="2edd9-114">PARAMETERS</span></span>

### <span data-ttu-id="2edd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edd9-115">-DefaultProfile</span></span>
<span data-ttu-id="2edd9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2edd9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edd9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edd9-117">-InputObject</span></span>
<span data-ttu-id="2edd9-118">Objeto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="2edd9-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2edd9-119">-Name</span></span>
<span data-ttu-id="2edd9-120">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="2edd9-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2edd9-121">-Namespace</span></span>
<span data-ttu-id="2edd9-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="2edd9-122">Namespace Name.</span></span>

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

### <span data-ttu-id="2edd9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edd9-123">-ResourceGroupName</span></span>
<span data-ttu-id="2edd9-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2edd9-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2edd9-125">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="2edd9-125">-UserMetadata</span></span>
<span data-ttu-id="2edd9-126">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2edd9-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2edd9-127">-Confirm</span></span>
<span data-ttu-id="2edd9-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2edd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edd9-129">-WhatIf</span></span>
<span data-ttu-id="2edd9-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2edd9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edd9-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2edd9-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edd9-132">CommonParameters</span></span>
<span data-ttu-id="2edd9-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edd9-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edd9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edd9-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2edd9-135">INPUTS</span></span>

### <span data-ttu-id="2edd9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edd9-136">-ResourceGroupName</span></span>
<span data-ttu-id="2edd9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-137">System.String</span></span>

### <span data-ttu-id="2edd9-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2edd9-138">-NamespaceName</span></span>
<span data-ttu-id="2edd9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-139">System.String</span></span>

### <span data-ttu-id="2edd9-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="2edd9-140">-WcfRelayName</span></span>
<span data-ttu-id="2edd9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-141">System.String</span></span>

### <span data-ttu-id="2edd9-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edd9-142">-InputObject</span></span>
<span data-ttu-id="2edd9-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="2edd9-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="2edd9-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="2edd9-144">-WcfRelayType</span></span>
<span data-ttu-id="2edd9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-145">System.String</span></span>

### <span data-ttu-id="2edd9-146">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="2edd9-146">-UserMetadata</span></span>
<span data-ttu-id="2edd9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-147">System.String</span></span>

## <span data-ttu-id="2edd9-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2edd9-148">OUTPUTS</span></span>

### <span data-ttu-id="2edd9-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="2edd9-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="2edd9-150">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edd9-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="2edd9-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="2edd9-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="2edd9-152">Relaytype: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false usermetadata: usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade do HybridConnection. por exemplo, Ele pode ser usado para armazenar dados desc riptive, como lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2edd9-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="2edd9-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ()/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="2edd9-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="2edd9-154">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="2edd9-154">Example 2 - Properties</span></span>

### <span data-ttu-id="2edd9-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="2edd9-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="2edd9-156">Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false usermetadata: ID de metadados do usuário:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel de espaços/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay nome: TestWCFRelay tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="2edd9-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="2edd9-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2edd9-157">NOTES</span></span>

## <span data-ttu-id="2edd9-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2edd9-158">RELATED LINKS</span></span>


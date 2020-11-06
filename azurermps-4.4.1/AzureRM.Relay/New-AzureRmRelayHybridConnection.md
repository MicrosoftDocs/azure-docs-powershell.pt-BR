---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427804"
---
# <span data-ttu-id="d8e0e-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d8e0e-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="d8e0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e0e-103">Cria um HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8e0e-104">SYNTAX</span></span>

### <span data-ttu-id="d8e0e-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d8e0e-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e0e-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d8e0e-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e0e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8e0e-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e0e-108">O cmdlet New-AzureRmRelayHybridConnection cria um HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d8e0e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8e0e-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e0e-110">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e0e-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="d8e0e-111">Cria um novo HybirdConnection \` TestHybirdConnection2 \` no namespace de retransmissão especificado \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="d8e0e-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="d8e0e-112">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8e0e-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="d8e0e-113">Cria um novo HybirdConnection \` TestHybirdConnection1 \` no namespace de retransmissão especificado \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="d8e0e-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="d8e0e-114">OS</span><span class="sxs-lookup"><span data-stu-id="d8e0e-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e0e-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="d8e0e-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="d8e0e-116">verdadeiro se for necessária a autorização do cliente para este HybridConnections; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="d8e0e-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-117">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="d8e0e-117">-UserMetadata</span></span>
<span data-ttu-id="d8e0e-118">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8e0e-119">-Confirm</span></span>
<span data-ttu-id="d8e0e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e0e-121">-WhatIf</span></span>
<span data-ttu-id="d8e0e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e0e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e0e-124">-InputObject</span></span>
<span data-ttu-id="d8e0e-125">Objeto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8e0e-126">-Name</span></span>
<span data-ttu-id="d8e0e-127">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-127">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8e0e-128">-Namespace</span></span>
<span data-ttu-id="d8e0e-129">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-129">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e0e-130">-ResourceGroupName</span></span>
<span data-ttu-id="d8e0e-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e0e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e0e-132">-DefaultProfile</span></span>
<span data-ttu-id="d8e0e-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e0e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e0e-134">CommonParameters</span></span>
<span data-ttu-id="d8e0e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e0e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e0e-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e0e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e0e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8e0e-137">INPUTS</span></span>

### <span data-ttu-id="d8e0e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e0e-138">-ResourceGroupName</span></span>
<span data-ttu-id="d8e0e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e0e-139">System.String</span></span>

### <span data-ttu-id="d8e0e-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d8e0e-140">-NamespaceName</span></span>
<span data-ttu-id="d8e0e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e0e-141">System.String</span></span>

### <span data-ttu-id="d8e0e-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="d8e0e-142">-HybridConnectionsName</span></span>
<span data-ttu-id="d8e0e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e0e-143">System.String</span></span>

### <span data-ttu-id="d8e0e-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e0e-144">-InputObject</span></span>
<span data-ttu-id="d8e0e-145">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="d8e0e-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="d8e0e-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="d8e0e-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="d8e0e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8e0e-147">System.Boolean</span></span>

### <span data-ttu-id="d8e0e-148">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="d8e0e-148">-UserMetadata</span></span>
<span data-ttu-id="d8e0e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e0e-149">System.String</span></span>

## <span data-ttu-id="d8e0e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8e0e-150">OUTPUTS</span></span>

### <span data-ttu-id="d8e0e-151">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="d8e0e-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="d8e0e-152">Exemplos-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e0e-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="d8e0e-153">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true Metadata: ID de metadados do usuário:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2: TestHybirdConnection2 tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="d8e0e-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="d8e0e-154">Exemplos-2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8e0e-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="d8e0e-155">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true Metadata: ID de metadados do usuário:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1: TestHybirdConnection1 tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="d8e0e-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="d8e0e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8e0e-156">NOTES</span></span>

## <span data-ttu-id="d8e0e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8e0e-157">RELATED LINKS</span></span>


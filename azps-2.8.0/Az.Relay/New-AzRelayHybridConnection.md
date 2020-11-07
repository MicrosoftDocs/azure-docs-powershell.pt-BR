---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 204ab147ef166a07d2df737d4d85b6678ef8516f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773396"
---
# <span data-ttu-id="f23db-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="f23db-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="f23db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f23db-102">SYNOPSIS</span></span>
<span data-ttu-id="f23db-103">Cria um HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="f23db-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="f23db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f23db-104">SYNTAX</span></span>

### <span data-ttu-id="f23db-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f23db-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f23db-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f23db-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f23db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f23db-107">DESCRIPTION</span></span>
<span data-ttu-id="f23db-108">O cmdlet New-AzRelayHybridConnection cria um HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="f23db-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="f23db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f23db-109">EXAMPLES</span></span>

### <span data-ttu-id="f23db-110">Exemplo 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="f23db-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="f23db-111">Cria um novo HybirdConnection \` TestHybirdConnection2 \` no namespace de retransmissão especificado \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="f23db-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="f23db-112">Exemplo 2: Propriedades</span><span class="sxs-lookup"><span data-stu-id="f23db-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="f23db-113">Cria um novo HybirdConnection \` TestHybirdConnection1 \` no namespace de retransmissão especificado \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="f23db-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="f23db-114">OS</span><span class="sxs-lookup"><span data-stu-id="f23db-114">PARAMETERS</span></span>

### <span data-ttu-id="f23db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23db-115">-DefaultProfile</span></span>
<span data-ttu-id="f23db-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f23db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f23db-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f23db-117">-InputObject</span></span>
<span data-ttu-id="f23db-118">Objeto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="f23db-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23db-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f23db-119">-Name</span></span>
<span data-ttu-id="f23db-120">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="f23db-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23db-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f23db-121">-Namespace</span></span>
<span data-ttu-id="f23db-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f23db-122">Namespace Name.</span></span>

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

### <span data-ttu-id="f23db-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="f23db-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="f23db-124">verdadeiro se for necessária a autorização do cliente para este HybridConnections; caso contrário, false</span><span class="sxs-lookup"><span data-stu-id="f23db-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="f23db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23db-125">-ResourceGroupName</span></span>
<span data-ttu-id="f23db-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f23db-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f23db-127">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="f23db-127">-UserMetadata</span></span>
<span data-ttu-id="f23db-128">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f23db-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="f23db-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f23db-129">-Confirm</span></span>
<span data-ttu-id="f23db-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f23db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23db-131">-WhatIf</span></span>
<span data-ttu-id="f23db-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f23db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f23db-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f23db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23db-134">CommonParameters</span></span>
<span data-ttu-id="f23db-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23db-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23db-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f23db-137">INPUTS</span></span>

### <span data-ttu-id="f23db-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f23db-138">System.String</span></span>

### <span data-ttu-id="f23db-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="f23db-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="f23db-140">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f23db-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f23db-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f23db-141">OUTPUTS</span></span>

### <span data-ttu-id="f23db-142">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="f23db-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="f23db-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f23db-143">NOTES</span></span>

## <span data-ttu-id="f23db-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f23db-144">RELATED LINKS</span></span>
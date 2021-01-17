---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428021"
---
# <span data-ttu-id="8eb43-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="8eb43-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="8eb43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eb43-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb43-103">Atualiza a descrição de um HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="8eb43-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8eb43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eb43-104">SYNTAX</span></span>

### <span data-ttu-id="8eb43-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8eb43-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eb43-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8eb43-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eb43-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eb43-107">DESCRIPTION</span></span>
<span data-ttu-id="8eb43-108">O cmdlet Set-AzRelayHybridConnection atualiza a descrição do HybridConnection no namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="8eb43-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8eb43-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eb43-109">EXAMPLES</span></span>

### <span data-ttu-id="8eb43-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8eb43-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="8eb43-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8eb43-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="8eb43-112">Atualiza o HybridConnection especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="8eb43-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="8eb43-113">Este exemplo atualiza a propriedade usermetadata com novo valor.</span><span class="sxs-lookup"><span data-stu-id="8eb43-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="8eb43-114">OS</span><span class="sxs-lookup"><span data-stu-id="8eb43-114">PARAMETERS</span></span>

### <span data-ttu-id="8eb43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb43-115">-DefaultProfile</span></span>
<span data-ttu-id="8eb43-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb43-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb43-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eb43-117">-InputObject</span></span>
<span data-ttu-id="8eb43-118">Objeto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="8eb43-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb43-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eb43-119">-Name</span></span>
<span data-ttu-id="8eb43-120">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="8eb43-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="8eb43-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8eb43-121">-Namespace</span></span>
<span data-ttu-id="8eb43-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="8eb43-122">Namespace Name.</span></span>

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

### <span data-ttu-id="8eb43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb43-123">-ResourceGroupName</span></span>
<span data-ttu-id="8eb43-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8eb43-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="8eb43-125">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="8eb43-125">-UserMetadata</span></span>
<span data-ttu-id="8eb43-126">Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8eb43-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="8eb43-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8eb43-127">-Confirm</span></span>
<span data-ttu-id="8eb43-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eb43-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eb43-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb43-129">-WhatIf</span></span>
<span data-ttu-id="8eb43-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8eb43-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb43-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8eb43-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eb43-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb43-132">CommonParameters</span></span>
<span data-ttu-id="8eb43-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb43-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb43-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb43-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb43-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eb43-135">INPUTS</span></span>

### <span data-ttu-id="8eb43-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8eb43-136">System.String</span></span>

### <span data-ttu-id="8eb43-137">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="8eb43-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="8eb43-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eb43-138">OUTPUTS</span></span>

### <span data-ttu-id="8eb43-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="8eb43-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="8eb43-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eb43-140">NOTES</span></span>

## <span data-ttu-id="8eb43-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eb43-141">RELATED LINKS</span></span>

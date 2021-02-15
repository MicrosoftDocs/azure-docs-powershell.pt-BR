---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112600"
---
# <span data-ttu-id="848c0-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="848c0-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="848c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="848c0-102">SYNOPSIS</span></span>
<span data-ttu-id="848c0-103">Obtém as cadeias de conexão primária e secundária para determinado Namespace ou Fila ou Tópico ou Alias (Configurações geodr).</span><span class="sxs-lookup"><span data-stu-id="848c0-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="848c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="848c0-104">SYNTAX</span></span>

### <span data-ttu-id="848c0-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="848c0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="848c0-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="848c0-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="848c0-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="848c0-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="848c0-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="848c0-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="848c0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="848c0-109">DESCRIPTION</span></span>
<span data-ttu-id="848c0-110">O cmdlet **Get-AzServiceBusKey** retorna as cadeias de conexão primárias e secundárias para o namespace ou fila ou tópico ou alias (configurações geodr).</span><span class="sxs-lookup"><span data-stu-id="848c0-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="848c0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="848c0-111">EXAMPLES</span></span>

### <span data-ttu-id="848c0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="848c0-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="848c0-113">Cadeia de conexão primária e secundária para o espaço de nome especificado.</span><span class="sxs-lookup"><span data-stu-id="848c0-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="848c0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="848c0-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="848c0-115">Cadeia de conexão primária e secundária para a fila especificada.</span><span class="sxs-lookup"><span data-stu-id="848c0-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="848c0-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="848c0-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="848c0-117">Cadeia de conexão principal e secundária para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="848c0-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="848c0-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="848c0-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="848c0-119">Cadeia de conexão primária e secundária para o namespace e alias especificados.</span><span class="sxs-lookup"><span data-stu-id="848c0-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="848c0-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="848c0-120">PARAMETERS</span></span>

### <span data-ttu-id="848c0-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="848c0-121">-AliasName</span></span>
<span data-ttu-id="848c0-122">Nome do Alias</span><span class="sxs-lookup"><span data-stu-id="848c0-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848c0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848c0-123">-DefaultProfile</span></span>
<span data-ttu-id="848c0-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="848c0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="848c0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="848c0-125">-Name</span></span>
<span data-ttu-id="848c0-126">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="848c0-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848c0-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="848c0-127">-Namespace</span></span>
<span data-ttu-id="848c0-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="848c0-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848c0-129">-Fila</span><span class="sxs-lookup"><span data-stu-id="848c0-129">-Queue</span></span>
<span data-ttu-id="848c0-130">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="848c0-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848c0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848c0-131">-ResourceGroupName</span></span>
<span data-ttu-id="848c0-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="848c0-132">Resource Group Name</span></span>

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

### <span data-ttu-id="848c0-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="848c0-133">-Topic</span></span>
<span data-ttu-id="848c0-134">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="848c0-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848c0-135">CommonParameters</span></span>
<span data-ttu-id="848c0-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848c0-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848c0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848c0-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="848c0-138">INPUTS</span></span>

### <span data-ttu-id="848c0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="848c0-139">System.String</span></span>

## <span data-ttu-id="848c0-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="848c0-140">OUTPUTS</span></span>

### <span data-ttu-id="848c0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="848c0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="848c0-142">Notas</span><span class="sxs-lookup"><span data-stu-id="848c0-142">NOTES</span></span>

## <span data-ttu-id="848c0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="848c0-143">RELATED LINKS</span></span>

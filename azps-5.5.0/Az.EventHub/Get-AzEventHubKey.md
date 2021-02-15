---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111896"
---
# <span data-ttu-id="278e7-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="278e7-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="278e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="278e7-102">SYNOPSIS</span></span>
<span data-ttu-id="278e7-103">Obtém os detalhes da chave primária da regra de autorização de Hubs de Eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="278e7-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="278e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="278e7-104">SYNTAX</span></span>

### <span data-ttu-id="278e7-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="278e7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278e7-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="278e7-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278e7-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="278e7-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="278e7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="278e7-108">DESCRIPTION</span></span>
<span data-ttu-id="278e7-109">O cmdlet Get-AzEventHubKey retorna os vínculos de conexão primários e secundários e os detalhes das teclas da regra de autorização do NameSpace/Event Hubs/Alias especificada.</span><span class="sxs-lookup"><span data-stu-id="278e7-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="278e7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="278e7-110">EXAMPLES</span></span>

### <span data-ttu-id="278e7-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="278e7-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="278e7-112">Exemplo 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="278e7-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="278e7-113">Obtém detalhes de chaves e conexões primárias e secundárias para a regra de autorização \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="278e7-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="278e7-114">Exemplo 3: Alias (Configuração de GeoReovery)</span><span class="sxs-lookup"><span data-stu-id="278e7-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="278e7-115">Obtém detalhes de chaves e conexões Primário, Secundário, AliasPrimary e AliasSecondary para a regra de autorização \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="278e7-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="278e7-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="278e7-116">PARAMETERS</span></span>

### <span data-ttu-id="278e7-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="278e7-117">-AliasName</span></span>
<span data-ttu-id="278e7-118">Nome do Alias</span><span class="sxs-lookup"><span data-stu-id="278e7-118">Alias Name</span></span>

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

### <span data-ttu-id="278e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278e7-119">-DefaultProfile</span></span>
<span data-ttu-id="278e7-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="278e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278e7-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="278e7-121">-EventHub</span></span>
<span data-ttu-id="278e7-122">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="278e7-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278e7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="278e7-123">-Name</span></span>
<span data-ttu-id="278e7-124">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="278e7-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="278e7-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="278e7-125">-Namespace</span></span>
<span data-ttu-id="278e7-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="278e7-126">Namespace Name</span></span>

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

### <span data-ttu-id="278e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="278e7-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="278e7-128">Resource Group Name</span></span>

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

### <span data-ttu-id="278e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278e7-129">CommonParameters</span></span>
<span data-ttu-id="278e7-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278e7-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="278e7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278e7-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="278e7-132">INPUTS</span></span>

### <span data-ttu-id="278e7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="278e7-133">System.String</span></span>

## <span data-ttu-id="278e7-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="278e7-134">OUTPUTS</span></span>

### <span data-ttu-id="278e7-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="278e7-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="278e7-136">Notas</span><span class="sxs-lookup"><span data-stu-id="278e7-136">NOTES</span></span>

## <span data-ttu-id="278e7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="278e7-137">RELATED LINKS</span></span>

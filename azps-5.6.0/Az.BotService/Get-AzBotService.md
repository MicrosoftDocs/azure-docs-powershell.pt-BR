---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 305e65e95b876e3093f4a14590e8b2e111e44aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892816"
---
# <span data-ttu-id="36b58-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="36b58-101">Get-AzBotService</span></span>

## <span data-ttu-id="36b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b58-102">SYNOPSIS</span></span>
<span data-ttu-id="36b58-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="36b58-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="36b58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36b58-104">SYNTAX</span></span>

### <span data-ttu-id="36b58-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36b58-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36b58-106">Obter</span><span class="sxs-lookup"><span data-stu-id="36b58-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36b58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36b58-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36b58-108">Listar</span><span class="sxs-lookup"><span data-stu-id="36b58-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="36b58-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36b58-109">DESCRIPTION</span></span>
<span data-ttu-id="36b58-110">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="36b58-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="36b58-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36b58-111">EXAMPLES</span></span>

### <span data-ttu-id="36b58-112">Exemplo 1: Obter todos os BotServices</span><span class="sxs-lookup"><span data-stu-id="36b58-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="36b58-113">Obter todos os BotServices</span><span class="sxs-lookup"><span data-stu-id="36b58-113">Get all BotServices</span></span>

### <span data-ttu-id="36b58-114">Exemplo 2: Obter o BotService por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="36b58-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="36b58-115">Obter o BotService por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="36b58-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="36b58-116">Exemplo 3: Obter todos os BotServices por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b58-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="36b58-117">Obter todos os BotServices por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b58-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="36b58-118">Exemplo 4: Obter o BotService por inputObject</span><span class="sxs-lookup"><span data-stu-id="36b58-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="36b58-119">Obter o BotService por inputObject</span><span class="sxs-lookup"><span data-stu-id="36b58-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="36b58-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36b58-120">PARAMETERS</span></span>

### <span data-ttu-id="36b58-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b58-121">-DefaultProfile</span></span>
<span data-ttu-id="36b58-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36b58-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b58-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b58-123">-InputObject</span></span>
<span data-ttu-id="36b58-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="36b58-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b58-125">-Name</span><span class="sxs-lookup"><span data-stu-id="36b58-125">-Name</span></span>
<span data-ttu-id="36b58-126">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="36b58-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b58-127">-ResourceGroupName</span></span>
<span data-ttu-id="36b58-128">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="36b58-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b58-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36b58-129">-SubscriptionId</span></span>
<span data-ttu-id="36b58-130">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="36b58-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b58-131">CommonParameters</span></span>
<span data-ttu-id="36b58-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b58-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36b58-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b58-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36b58-134">INPUTS</span></span>

### <span data-ttu-id="36b58-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="36b58-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="36b58-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36b58-136">OUTPUTS</span></span>

### <span data-ttu-id="36b58-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="36b58-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="36b58-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="36b58-138">NOTES</span></span>

<span data-ttu-id="36b58-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36b58-139">ALIASES</span></span>

<span data-ttu-id="36b58-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="36b58-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36b58-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="36b58-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36b58-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36b58-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36b58-143">INPUTOBJECT <IBotServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="36b58-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36b58-144">`[ChannelName <ChannelName?>]`: O nome do recurso Channel.</span><span class="sxs-lookup"><span data-stu-id="36b58-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="36b58-145">`[ConnectionName <String>]`: O nome do recurso Configuração de Conexão de Serviço bot</span><span class="sxs-lookup"><span data-stu-id="36b58-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="36b58-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="36b58-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36b58-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="36b58-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="36b58-148">`[ResourceName <String>]`: O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="36b58-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="36b58-149">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="36b58-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="36b58-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36b58-150">RELATED LINKS</span></span>


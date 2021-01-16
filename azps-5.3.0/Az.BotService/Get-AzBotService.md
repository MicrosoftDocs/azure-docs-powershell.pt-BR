---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430353"
---
# <span data-ttu-id="34d4c-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="34d4c-101">Get-AzBotService</span></span>

## <span data-ttu-id="34d4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="34d4c-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="34d4c-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="34d4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34d4c-104">SYNTAX</span></span>

### <span data-ttu-id="34d4c-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="34d4c-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34d4c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="34d4c-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34d4c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34d4c-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34d4c-108">Programação</span><span class="sxs-lookup"><span data-stu-id="34d4c-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="34d4c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34d4c-109">DESCRIPTION</span></span>
<span data-ttu-id="34d4c-110">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="34d4c-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="34d4c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34d4c-111">EXAMPLES</span></span>

### <span data-ttu-id="34d4c-112">Exemplo 1: obter todos os BotServices</span><span class="sxs-lookup"><span data-stu-id="34d4c-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="34d4c-113">Obter todos os BotServices</span><span class="sxs-lookup"><span data-stu-id="34d4c-113">Get all BotServices</span></span>

### <span data-ttu-id="34d4c-114">Exemplo 2: obter o BotService por ResourceGroupName e nome</span><span class="sxs-lookup"><span data-stu-id="34d4c-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="34d4c-115">Obter o BotService por ResourceGroupName e nome</span><span class="sxs-lookup"><span data-stu-id="34d4c-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="34d4c-116">Exemplo 3: obter todos os BotServices por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d4c-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="34d4c-117">Obtenha todos os BotServices por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d4c-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="34d4c-118">Exemplo 4: obter o BotService por InputObject</span><span class="sxs-lookup"><span data-stu-id="34d4c-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="34d4c-119">Obter o BotService por InputObject</span><span class="sxs-lookup"><span data-stu-id="34d4c-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="34d4c-120">OS</span><span class="sxs-lookup"><span data-stu-id="34d4c-120">PARAMETERS</span></span>

### <span data-ttu-id="34d4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d4c-121">-DefaultProfile</span></span>
<span data-ttu-id="34d4c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34d4c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d4c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34d4c-123">-InputObject</span></span>
<span data-ttu-id="34d4c-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="34d4c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34d4c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="34d4c-125">-Name</span></span>
<span data-ttu-id="34d4c-126">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="34d4c-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="34d4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="34d4c-128">O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="34d4c-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="34d4c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34d4c-129">-SubscriptionId</span></span>
<span data-ttu-id="34d4c-130">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="34d4c-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="34d4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d4c-131">CommonParameters</span></span>
<span data-ttu-id="34d4c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d4c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34d4c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d4c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34d4c-134">INPUTS</span></span>

### <span data-ttu-id="34d4c-135">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="34d4c-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="34d4c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34d4c-136">OUTPUTS</span></span>

### <span data-ttu-id="34d4c-137">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="34d4c-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="34d4c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34d4c-138">NOTES</span></span>

<span data-ttu-id="34d4c-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="34d4c-139">ALIASES</span></span>

<span data-ttu-id="34d4c-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="34d4c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34d4c-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="34d4c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34d4c-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34d4c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34d4c-143">INPUTobject <IBotServiceIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="34d4c-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34d4c-144">`[ChannelName <ChannelName?>]`: O nome do recurso de canal.</span><span class="sxs-lookup"><span data-stu-id="34d4c-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="34d4c-145">`[ConnectionName <String>]`: O nome do recurso de configuração de conexão do serviço bot</span><span class="sxs-lookup"><span data-stu-id="34d4c-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="34d4c-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="34d4c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34d4c-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="34d4c-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="34d4c-148">`[ResourceName <String>]`: O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="34d4c-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="34d4c-149">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="34d4c-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="34d4c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34d4c-150">RELATED LINKS</span></span>


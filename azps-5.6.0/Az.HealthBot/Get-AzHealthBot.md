---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893306"
---
# <span data-ttu-id="880c7-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="880c7-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="880c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="880c7-102">SYNOPSIS</span></span>
<span data-ttu-id="880c7-103">Obter um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="880c7-103">Get a HealthBot.</span></span>

## <span data-ttu-id="880c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="880c7-104">SYNTAX</span></span>

### <span data-ttu-id="880c7-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="880c7-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="880c7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="880c7-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="880c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="880c7-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="880c7-108">Listar</span><span class="sxs-lookup"><span data-stu-id="880c7-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="880c7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="880c7-109">DESCRIPTION</span></span>
<span data-ttu-id="880c7-110">Obter um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="880c7-110">Get a HealthBot.</span></span>

## <span data-ttu-id="880c7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="880c7-111">EXAMPLES</span></span>

### <span data-ttu-id="880c7-112">Exemplo 1: Obter todo o HealthBot</span><span class="sxs-lookup"><span data-stu-id="880c7-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="880c7-113">Obter todo o HealthBot</span><span class="sxs-lookup"><span data-stu-id="880c7-113">Get all HealthBot</span></span>

### <span data-ttu-id="880c7-114">Exemplo 2: Obter todo o HealthBot por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c7-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="880c7-115">Obter todos os HealthBot por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c7-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="880c7-116">Exemplo 3: Obter HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="880c7-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="880c7-117">Obter HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="880c7-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="880c7-118">Exemplo 4: Obter HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="880c7-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="880c7-119">Obter HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="880c7-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="880c7-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="880c7-120">PARAMETERS</span></span>

### <span data-ttu-id="880c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880c7-121">-DefaultProfile</span></span>
<span data-ttu-id="880c7-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="880c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="880c7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="880c7-123">-InputObject</span></span>
<span data-ttu-id="880c7-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="880c7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="880c7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="880c7-125">-Name</span></span>
<span data-ttu-id="880c7-126">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="880c7-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="880c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="880c7-128">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="880c7-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="880c7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="880c7-129">-SubscriptionId</span></span>
<span data-ttu-id="880c7-130">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="880c7-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="880c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880c7-131">CommonParameters</span></span>
<span data-ttu-id="880c7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880c7-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="880c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880c7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="880c7-134">INPUTS</span></span>

### <span data-ttu-id="880c7-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="880c7-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="880c7-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="880c7-136">OUTPUTS</span></span>

### <span data-ttu-id="880c7-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="880c7-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="880c7-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="880c7-138">NOTES</span></span>

<span data-ttu-id="880c7-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="880c7-139">ALIASES</span></span>

<span data-ttu-id="880c7-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="880c7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="880c7-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="880c7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="880c7-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="880c7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="880c7-143">INPUTOBJECT <IHealthBotIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="880c7-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="880c7-144">`[BotName <String>]`: O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="880c7-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="880c7-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="880c7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="880c7-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="880c7-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="880c7-147">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="880c7-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="880c7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="880c7-148">RELATED LINKS</span></span>


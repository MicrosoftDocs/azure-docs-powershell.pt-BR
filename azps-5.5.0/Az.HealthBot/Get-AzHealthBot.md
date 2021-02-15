---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111862"
---
# <span data-ttu-id="f8895-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f8895-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="f8895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8895-102">SYNOPSIS</span></span>
<span data-ttu-id="f8895-103">Obter um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f8895-103">Get a HealthBot.</span></span>

## <span data-ttu-id="f8895-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8895-104">SYNTAX</span></span>

### <span data-ttu-id="f8895-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f8895-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8895-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f8895-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8895-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8895-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8895-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f8895-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8895-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8895-109">DESCRIPTION</span></span>
<span data-ttu-id="f8895-110">Obter um HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f8895-110">Get a HealthBot.</span></span>

## <span data-ttu-id="f8895-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8895-111">EXAMPLES</span></span>

### <span data-ttu-id="f8895-112">Exemplo 1: Obter todos os HealthBot</span><span class="sxs-lookup"><span data-stu-id="f8895-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f8895-113">Obter todo o HealthBot</span><span class="sxs-lookup"><span data-stu-id="f8895-113">Get all HealthBot</span></span>

### <span data-ttu-id="f8895-114">Exemplo 2: Obter todos os HealthBot por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8895-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f8895-115">Obter todos os HealthBot por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8895-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="f8895-116">Exemplo 3: Obter HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="f8895-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f8895-117">Obter o HealthBot por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="f8895-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="f8895-118">Exemplo 4: Obter HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="f8895-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f8895-119">Obter o HealthBot por InputObject</span><span class="sxs-lookup"><span data-stu-id="f8895-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="f8895-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8895-120">PARAMETERS</span></span>

### <span data-ttu-id="f8895-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8895-121">-DefaultProfile</span></span>
<span data-ttu-id="f8895-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8895-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8895-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8895-123">-InputObject</span></span>
<span data-ttu-id="f8895-124">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f8895-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8895-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8895-125">-Name</span></span>
<span data-ttu-id="f8895-126">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="f8895-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f8895-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8895-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8895-128">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="f8895-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f8895-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8895-129">-SubscriptionId</span></span>
<span data-ttu-id="f8895-130">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8895-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f8895-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8895-131">CommonParameters</span></span>
<span data-ttu-id="f8895-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8895-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8895-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8895-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8895-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="f8895-134">INPUTS</span></span>

### <span data-ttu-id="f8895-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="f8895-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f8895-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="f8895-136">OUTPUTS</span></span>

### <span data-ttu-id="f8895-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="f8895-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f8895-138">Notas</span><span class="sxs-lookup"><span data-stu-id="f8895-138">NOTES</span></span>

<span data-ttu-id="f8895-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="f8895-139">ALIASES</span></span>

<span data-ttu-id="f8895-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f8895-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8895-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f8895-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8895-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8895-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8895-143">INPUTOBJECT: <IHealthBotIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f8895-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8895-144">`[BotName <String>]`: o nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="f8895-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f8895-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f8895-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8895-146">`[ResourceGroupName <String>]`: o nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="f8895-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f8895-147">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8895-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f8895-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8895-148">RELATED LINKS</span></span>


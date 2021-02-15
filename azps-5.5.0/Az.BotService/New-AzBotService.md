---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112192"
---
# <span data-ttu-id="d271b-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="d271b-101">New-AzBotService</span></span>

## <span data-ttu-id="d271b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d271b-102">SYNOPSIS</span></span>
<span data-ttu-id="d271b-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d271b-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d271b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d271b-104">SYNTAX</span></span>

### <span data-ttu-id="d271b-105">Registro (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d271b-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d271b-106">Webapp</span><span class="sxs-lookup"><span data-stu-id="d271b-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d271b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d271b-107">DESCRIPTION</span></span>
<span data-ttu-id="d271b-108">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d271b-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d271b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d271b-109">EXAMPLES</span></span>

### <span data-ttu-id="d271b-110">Exemplo 1: Criar um novo bot</span><span class="sxs-lookup"><span data-stu-id="d271b-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="d271b-111">Criar um novo bot por ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d271b-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="d271b-112">Exemplo 2: Criar um novo Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d271b-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="d271b-113">Criar um novo Aplicativo Web por ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d271b-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="d271b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d271b-114">PARAMETERS</span></span>

### <span data-ttu-id="d271b-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d271b-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-116">-ApplicationSecsecsec</span><span class="sxs-lookup"><span data-stu-id="d271b-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="d271b-117">-BotTemplateType</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d271b-118">-DefaultProfile</span></span>
<span data-ttu-id="d271b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d271b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d271b-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d271b-120">-Description</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d271b-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-122">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="d271b-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="d271b-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-124">-Idioma</span><span class="sxs-lookup"><span data-stu-id="d271b-124">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-125">-Local</span><span class="sxs-lookup"><span data-stu-id="d271b-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d271b-126">-Name</span></span>
<span data-ttu-id="d271b-127">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="d271b-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-128">-Registro</span><span class="sxs-lookup"><span data-stu-id="d271b-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d271b-129">-ResourceGroupName</span></span>
<span data-ttu-id="d271b-130">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="d271b-130">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="d271b-131">-Sku</span></span>
<span data-ttu-id="d271b-132">O nome da sKU</span><span class="sxs-lookup"><span data-stu-id="d271b-132">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d271b-133">-SubscriptionId</span></span>
<span data-ttu-id="d271b-134">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d271b-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="d271b-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d271b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d271b-136">CommonParameters</span></span>
<span data-ttu-id="d271b-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d271b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d271b-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d271b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d271b-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d271b-139">INPUTS</span></span>

## <span data-ttu-id="d271b-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="d271b-140">OUTPUTS</span></span>

### <span data-ttu-id="d271b-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="d271b-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d271b-142">Notas</span><span class="sxs-lookup"><span data-stu-id="d271b-142">NOTES</span></span>

<span data-ttu-id="d271b-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="d271b-143">ALIASES</span></span>

## <span data-ttu-id="d271b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d271b-144">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890496"
---
# <span data-ttu-id="f7d37-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="f7d37-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="f7d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d37-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d37-103">Criar ou atualizar uma Autorização de Circuito Expresso em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f7d37-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f7d37-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7d37-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f7d37-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7d37-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d37-106">Criar ou atualizar uma Autorização de Circuito Expresso em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f7d37-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f7d37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7d37-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d37-108">Exemplo 1: Criar autorização</span><span class="sxs-lookup"><span data-stu-id="f7d37-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="f7d37-109">Este cmdlet cria autorização `azps-test-auth` em nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="f7d37-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="f7d37-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7d37-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d37-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7d37-111">-AsJob</span></span>
<span data-ttu-id="f7d37-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f7d37-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d37-113">-DefaultProfile</span></span>
<span data-ttu-id="f7d37-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d37-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d37-115">-Name</span></span>
<span data-ttu-id="f7d37-116">Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="f7d37-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d37-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f7d37-117">-NoWait</span></span>
<span data-ttu-id="f7d37-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f7d37-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d37-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f7d37-119">-PrivateCloudName</span></span>
<span data-ttu-id="f7d37-120">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="f7d37-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="f7d37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d37-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7d37-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7d37-122">The name of the resource group.</span></span>
<span data-ttu-id="f7d37-123">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f7d37-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f7d37-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7d37-124">-SubscriptionId</span></span>
<span data-ttu-id="f7d37-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f7d37-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d37-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d37-126">-Confirm</span></span>
<span data-ttu-id="f7d37-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d37-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d37-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d37-128">-WhatIf</span></span>
<span data-ttu-id="f7d37-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7d37-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d37-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7d37-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d37-131">CommonParameters</span></span>
<span data-ttu-id="f7d37-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d37-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d37-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d37-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d37-134">INPUTS</span></span>

## <span data-ttu-id="f7d37-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7d37-135">OUTPUTS</span></span>

### <span data-ttu-id="f7d37-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="f7d37-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="f7d37-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7d37-137">NOTES</span></span>

<span data-ttu-id="f7d37-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7d37-138">ALIASES</span></span>

## <span data-ttu-id="f7d37-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7d37-139">RELATED LINKS</span></span>


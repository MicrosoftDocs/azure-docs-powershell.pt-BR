---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 394975e341d52fb0067b420397189b0a8858cfcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114347"
---
# <span data-ttu-id="946d6-101">New-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="946d6-101">New-AzVMwareAuthorization</span></span>

## <span data-ttu-id="946d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="946d6-102">SYNOPSIS</span></span>
<span data-ttu-id="946d6-103">Criar ou atualizar uma Autorização de Circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="946d6-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="946d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="946d6-104">SYNTAX</span></span>

```
New-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="946d6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="946d6-105">DESCRIPTION</span></span>
<span data-ttu-id="946d6-106">Criar ou atualizar uma Autorização de Circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="946d6-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="946d6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="946d6-107">EXAMPLES</span></span>

### <span data-ttu-id="946d6-108">Exemplo 1: Criar autorização</span><span class="sxs-lookup"><span data-stu-id="946d6-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="946d6-109">Este cmdlet cria autorização `azps-test-auth` sob nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="946d6-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="946d6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="946d6-110">PARAMETERS</span></span>

### <span data-ttu-id="946d6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="946d6-111">-AsJob</span></span>
<span data-ttu-id="946d6-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="946d6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="946d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946d6-113">-DefaultProfile</span></span>
<span data-ttu-id="946d6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="946d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="946d6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="946d6-115">-Name</span></span>
<span data-ttu-id="946d6-116">Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="946d6-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="946d6-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="946d6-117">-NoWait</span></span>
<span data-ttu-id="946d6-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="946d6-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="946d6-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="946d6-119">-PrivateCloudName</span></span>
<span data-ttu-id="946d6-120">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="946d6-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="946d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="946d6-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="946d6-122">The name of the resource group.</span></span>
<span data-ttu-id="946d6-123">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="946d6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="946d6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="946d6-124">-SubscriptionId</span></span>
<span data-ttu-id="946d6-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="946d6-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="946d6-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="946d6-126">-Confirm</span></span>
<span data-ttu-id="946d6-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="946d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="946d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946d6-128">-WhatIf</span></span>
<span data-ttu-id="946d6-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="946d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="946d6-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="946d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="946d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946d6-131">CommonParameters</span></span>
<span data-ttu-id="946d6-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946d6-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="946d6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946d6-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="946d6-134">INPUTS</span></span>

## <span data-ttu-id="946d6-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="946d6-135">OUTPUTS</span></span>

### <span data-ttu-id="946d6-136">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="946d6-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="946d6-137">Notas</span><span class="sxs-lookup"><span data-stu-id="946d6-137">NOTES</span></span>

<span data-ttu-id="946d6-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="946d6-138">ALIASES</span></span>

## <span data-ttu-id="946d6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="946d6-139">RELATED LINKS</span></span>


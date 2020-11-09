---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283952"
---
# <span data-ttu-id="2f8c0-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f8c0-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="2f8c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8c0-103">Criar ou atualizar uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2f8c0-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="2f8c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f8c0-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2f8c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f8c0-105">DESCRIPTION</span></span>
<span data-ttu-id="2f8c0-106">Criar ou atualizar uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2f8c0-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="2f8c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f8c0-107">EXAMPLES</span></span>

### <span data-ttu-id="2f8c0-108">Exemplo 1: criar criação de autor</span><span class="sxs-lookup"><span data-stu-id="2f8c0-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="2f8c0-109">Este cmdlet cria autorização `azps-test-auth` na nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="2f8c0-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="2f8c0-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f8c0-110">PARAMETERS</span></span>

### <span data-ttu-id="2f8c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f8c0-111">-AsJob</span></span>
<span data-ttu-id="2f8c0-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2f8c0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2f8c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8c0-113">-DefaultProfile</span></span>
<span data-ttu-id="2f8c0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8c0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f8c0-115">-Name</span></span>
<span data-ttu-id="2f8c0-116">Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2f8c0-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="2f8c0-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2f8c0-117">-NoWait</span></span>
<span data-ttu-id="2f8c0-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2f8c0-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2f8c0-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2f8c0-119">-PrivateCloudName</span></span>
<span data-ttu-id="2f8c0-120">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="2f8c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f8c0-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-122">The name of the resource group.</span></span>
<span data-ttu-id="2f8c0-123">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2f8c0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f8c0-124">-SubscriptionId</span></span>
<span data-ttu-id="2f8c0-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2f8c0-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f8c0-126">-Confirm</span></span>
<span data-ttu-id="2f8c0-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f8c0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8c0-128">-WhatIf</span></span>
<span data-ttu-id="2f8c0-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f8c0-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f8c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8c0-131">CommonParameters</span></span>
<span data-ttu-id="2f8c0-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f8c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8c0-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f8c0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8c0-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f8c0-134">INPUTS</span></span>

## <span data-ttu-id="2f8c0-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f8c0-135">OUTPUTS</span></span>

### <span data-ttu-id="2f8c0-136">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f8c0-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="2f8c0-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f8c0-137">NOTES</span></span>

<span data-ttu-id="2f8c0-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2f8c0-138">ALIASES</span></span>

## <span data-ttu-id="2f8c0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f8c0-139">RELATED LINKS</span></span>


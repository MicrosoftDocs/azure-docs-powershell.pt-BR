---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113443"
---
# <span data-ttu-id="cad9c-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="cad9c-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="cad9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="cad9c-103">Criar ou atualizar uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="cad9c-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="cad9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cad9c-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cad9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cad9c-105">DESCRIPTION</span></span>
<span data-ttu-id="cad9c-106">Criar ou atualizar uma autorização de circuito do ExpressRoute em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="cad9c-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="cad9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cad9c-107">EXAMPLES</span></span>

### <span data-ttu-id="cad9c-108">Exemplo 1: criar criação de autor</span><span class="sxs-lookup"><span data-stu-id="cad9c-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="cad9c-109">Este cmdlet cria autorização `azps-test-auth` na nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="cad9c-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="cad9c-110">OS</span><span class="sxs-lookup"><span data-stu-id="cad9c-110">PARAMETERS</span></span>

### <span data-ttu-id="cad9c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cad9c-111">-AsJob</span></span>
<span data-ttu-id="cad9c-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cad9c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cad9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad9c-113">-DefaultProfile</span></span>
<span data-ttu-id="cad9c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cad9c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cad9c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cad9c-115">-Name</span></span>
<span data-ttu-id="cad9c-116">Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="cad9c-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="cad9c-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cad9c-117">-NoWait</span></span>
<span data-ttu-id="cad9c-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cad9c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cad9c-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="cad9c-119">-PrivateCloudName</span></span>
<span data-ttu-id="cad9c-120">O nome da nuvem privada.</span><span class="sxs-lookup"><span data-stu-id="cad9c-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="cad9c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad9c-121">-ResourceGroupName</span></span>
<span data-ttu-id="cad9c-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cad9c-122">The name of the resource group.</span></span>
<span data-ttu-id="cad9c-123">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cad9c-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cad9c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cad9c-124">-SubscriptionId</span></span>
<span data-ttu-id="cad9c-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cad9c-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cad9c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cad9c-126">-Confirm</span></span>
<span data-ttu-id="cad9c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad9c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad9c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad9c-128">-WhatIf</span></span>
<span data-ttu-id="cad9c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cad9c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cad9c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cad9c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad9c-131">CommonParameters</span></span>
<span data-ttu-id="cad9c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad9c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cad9c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad9c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cad9c-134">INPUTS</span></span>

## <span data-ttu-id="cad9c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cad9c-135">OUTPUTS</span></span>

### <span data-ttu-id="cad9c-136">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="cad9c-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="cad9c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cad9c-137">NOTES</span></span>

<span data-ttu-id="cad9c-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cad9c-138">ALIASES</span></span>

## <span data-ttu-id="cad9c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cad9c-139">RELATED LINKS</span></span>


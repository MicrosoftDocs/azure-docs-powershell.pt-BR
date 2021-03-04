---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885802"
---
# <span data-ttu-id="a93c0-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="a93c0-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="a93c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a93c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a93c0-103">Implante o jar criado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a93c0-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="a93c0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a93c0-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a93c0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a93c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a93c0-106">Implante o jar criado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a93c0-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="a93c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a93c0-107">EXAMPLES</span></span>

### <span data-ttu-id="a93c0-108">Exemplo 1: Implantar um jar compilado local para o serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="a93c0-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="a93c0-109">Implantar um jar compilado local para o serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="a93c0-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="a93c0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a93c0-110">PARAMETERS</span></span>

### <span data-ttu-id="a93c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a93c0-111">-AsJob</span></span>
<span data-ttu-id="a93c0-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a93c0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a93c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93c0-113">-DefaultProfile</span></span>
<span data-ttu-id="a93c0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a93c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93c0-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="a93c0-115">-JarPath</span></span>
<span data-ttu-id="a93c0-116">O caminho do jar precisa ser deplorável.</span><span class="sxs-lookup"><span data-stu-id="a93c0-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="a93c0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a93c0-117">-Name</span></span>
<span data-ttu-id="a93c0-118">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="a93c0-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93c0-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a93c0-119">-NoWait</span></span>
<span data-ttu-id="a93c0-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a93c0-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a93c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="a93c0-122">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a93c0-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a93c0-123">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a93c0-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a93c0-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a93c0-124">-ServiceName</span></span>
<span data-ttu-id="a93c0-125">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="a93c0-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a93c0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a93c0-126">-SubscriptionId</span></span>
<span data-ttu-id="a93c0-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a93c0-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a93c0-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a93c0-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a93c0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a93c0-129">-Confirm</span></span>
<span data-ttu-id="a93c0-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93c0-131">-WhatIf</span></span>
<span data-ttu-id="a93c0-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a93c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93c0-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a93c0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93c0-134">CommonParameters</span></span>
<span data-ttu-id="a93c0-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93c0-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a93c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93c0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a93c0-137">INPUTS</span></span>

## <span data-ttu-id="a93c0-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a93c0-138">OUTPUTS</span></span>

### <span data-ttu-id="a93c0-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="a93c0-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="a93c0-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="a93c0-140">NOTES</span></span>

<span data-ttu-id="a93c0-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a93c0-141">ALIASES</span></span>

## <span data-ttu-id="a93c0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a93c0-142">RELATED LINKS</span></span>


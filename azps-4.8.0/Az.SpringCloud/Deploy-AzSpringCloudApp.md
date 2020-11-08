---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111374"
---
# <span data-ttu-id="8c841-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="8c841-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="8c841-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c841-102">SYNOPSIS</span></span>
<span data-ttu-id="8c841-103">Implante o jar integrado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="8c841-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="8c841-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c841-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8c841-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c841-105">DESCRIPTION</span></span>
<span data-ttu-id="8c841-106">Implante o jar integrado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="8c841-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="8c841-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c841-107">EXAMPLES</span></span>

### <span data-ttu-id="8c841-108">Exemplo 1: implantar jar compilado local para serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="8c841-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="8c841-109">Implantar jar compilado local para o serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="8c841-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="8c841-110">OS</span><span class="sxs-lookup"><span data-stu-id="8c841-110">PARAMETERS</span></span>

### <span data-ttu-id="8c841-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c841-111">-AsJob</span></span>
<span data-ttu-id="8c841-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8c841-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8c841-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c841-113">-DefaultProfile</span></span>
<span data-ttu-id="8c841-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c841-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c841-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="8c841-115">-JarPath</span></span>
<span data-ttu-id="8c841-116">O caminho do jar precisa ser deploied.</span><span class="sxs-lookup"><span data-stu-id="8c841-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="8c841-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c841-117">-Name</span></span>
<span data-ttu-id="8c841-118">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c841-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="8c841-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8c841-119">-NoWait</span></span>
<span data-ttu-id="8c841-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8c841-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c841-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c841-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c841-122">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="8c841-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8c841-123">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="8c841-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8c841-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8c841-124">-ServiceName</span></span>
<span data-ttu-id="8c841-125">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="8c841-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8c841-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c841-126">-SubscriptionId</span></span>
<span data-ttu-id="8c841-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c841-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c841-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8c841-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8c841-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c841-129">-Confirm</span></span>
<span data-ttu-id="8c841-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c841-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c841-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c841-131">-WhatIf</span></span>
<span data-ttu-id="8c841-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c841-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c841-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c841-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c841-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c841-134">CommonParameters</span></span>
<span data-ttu-id="8c841-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c841-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c841-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c841-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c841-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c841-137">INPUTS</span></span>

## <span data-ttu-id="8c841-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c841-138">OUTPUTS</span></span>

### <span data-ttu-id="8c841-139">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="8c841-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="8c841-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c841-140">NOTES</span></span>

<span data-ttu-id="8c841-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8c841-141">ALIASES</span></span>

## <span data-ttu-id="8c841-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c841-142">RELATED LINKS</span></span>


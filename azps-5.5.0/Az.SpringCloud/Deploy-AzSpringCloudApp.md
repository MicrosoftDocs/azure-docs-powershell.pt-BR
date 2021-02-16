---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118630"
---
# <span data-ttu-id="5bf4d-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="5bf4d-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="5bf4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf4d-103">Implante o jarro criado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="5bf4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bf4d-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf4d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bf4d-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf4d-106">Implante o jarro criado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="5bf4d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bf4d-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf4d-108">Exemplo 1: Implantar o jar compilado local para o serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="5bf4d-109">Implante o jar compilado local para o serviço por nome.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="5bf4d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bf4d-110">PARAMETERS</span></span>

### <span data-ttu-id="5bf4d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bf4d-111">-AsJob</span></span>
<span data-ttu-id="5bf4d-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5bf4d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5bf4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf4d-113">-DefaultProfile</span></span>
<span data-ttu-id="5bf4d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf4d-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="5bf4d-115">-JarPath</span></span>
<span data-ttu-id="5bf4d-116">O caminho do jarro precisa ser deplorável.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="5bf4d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bf4d-117">-Name</span></span>
<span data-ttu-id="5bf4d-118">O nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="5bf4d-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5bf4d-119">-NoWait</span></span>
<span data-ttu-id="5bf4d-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="5bf4d-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5bf4d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf4d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bf4d-122">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5bf4d-123">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5bf4d-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5bf4d-124">-ServiceName</span></span>
<span data-ttu-id="5bf4d-125">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="5bf4d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5bf4d-126">-SubscriptionId</span></span>
<span data-ttu-id="5bf4d-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5bf4d-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5bf4d-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5bf4d-129">-Confirm</span></span>
<span data-ttu-id="5bf4d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf4d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf4d-131">-WhatIf</span></span>
<span data-ttu-id="5bf4d-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf4d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf4d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf4d-134">CommonParameters</span></span>
<span data-ttu-id="5bf4d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf4d-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bf4d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf4d-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="5bf4d-137">INPUTS</span></span>

## <span data-ttu-id="5bf4d-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="5bf4d-138">OUTPUTS</span></span>

### <span data-ttu-id="5bf4d-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="5bf4d-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="5bf4d-140">Notas</span><span class="sxs-lookup"><span data-stu-id="5bf4d-140">NOTES</span></span>

<span data-ttu-id="5bf4d-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="5bf4d-141">ALIASES</span></span>

## <span data-ttu-id="5bf4d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bf4d-142">RELATED LINKS</span></span>


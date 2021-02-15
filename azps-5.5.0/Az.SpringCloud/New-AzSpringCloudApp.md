---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112566"
---
# <span data-ttu-id="2c176-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2c176-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="2c176-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c176-102">SYNOPSIS</span></span>
<span data-ttu-id="2c176-103">Crie um novo aplicativo ou atualize um aplicativo que saia.</span><span class="sxs-lookup"><span data-stu-id="2c176-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="2c176-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c176-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c176-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c176-105">DESCRIPTION</span></span>
<span data-ttu-id="2c176-106">Crie um novo aplicativo ou atualize um aplicativo que saia.</span><span class="sxs-lookup"><span data-stu-id="2c176-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="2c176-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c176-107">EXAMPLES</span></span>

### <span data-ttu-id="2c176-108">Exemplo 1: Criar um aplicativo de nuvem de primavera.</span><span class="sxs-lookup"><span data-stu-id="2c176-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="2c176-109">Crie um aplicativo de nuvem de primavera.</span><span class="sxs-lookup"><span data-stu-id="2c176-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="2c176-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c176-110">PARAMETERS</span></span>

### <span data-ttu-id="2c176-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2c176-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="2c176-112">Nome da implantação ativa do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2c176-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="2c176-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c176-113">-AsJob</span></span>
<span data-ttu-id="2c176-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2c176-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2c176-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c176-115">-DefaultProfile</span></span>
<span data-ttu-id="2c176-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c176-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c176-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="2c176-117">-Fqdn</span></span>
<span data-ttu-id="2c176-118">Nome dns totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="2c176-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="2c176-119">-httpsOnly</span><span class="sxs-lookup"><span data-stu-id="2c176-119">-HttpsOnly</span></span>
<span data-ttu-id="2c176-120">Indique se apenas https é permitido.</span><span class="sxs-lookup"><span data-stu-id="2c176-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="2c176-121">-Local</span><span class="sxs-lookup"><span data-stu-id="2c176-121">-Location</span></span>
<span data-ttu-id="2c176-122">A localização GEO do aplicativo, sempre a mesma com seu recurso pai</span><span class="sxs-lookup"><span data-stu-id="2c176-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="2c176-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c176-123">-Name</span></span>
<span data-ttu-id="2c176-124">O nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c176-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="2c176-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c176-125">-NoWait</span></span>
<span data-ttu-id="2c176-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="2c176-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c176-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2c176-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="2c176-128">Caminho de montagem do disco persistente</span><span class="sxs-lookup"><span data-stu-id="2c176-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="2c176-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2c176-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="2c176-130">Tamanho do disco persistente em GB</span><span class="sxs-lookup"><span data-stu-id="2c176-130">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c176-131">-Público</span><span class="sxs-lookup"><span data-stu-id="2c176-131">-Public</span></span>
<span data-ttu-id="2c176-132">Indica se o aplicativo expõe o ponto de extremidade público</span><span class="sxs-lookup"><span data-stu-id="2c176-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="2c176-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c176-133">-ResourceGroupName</span></span>
<span data-ttu-id="2c176-134">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2c176-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2c176-135">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="2c176-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2c176-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c176-136">-ServiceName</span></span>
<span data-ttu-id="2c176-137">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="2c176-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2c176-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c176-138">-SubscriptionId</span></span>
<span data-ttu-id="2c176-139">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2c176-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c176-140">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c176-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2c176-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2c176-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="2c176-142">Caminho de montagem do disco temporário</span><span class="sxs-lookup"><span data-stu-id="2c176-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="2c176-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2c176-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="2c176-144">Tamanho do disco temporário em GB</span><span class="sxs-lookup"><span data-stu-id="2c176-144">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c176-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c176-145">-Confirm</span></span>
<span data-ttu-id="2c176-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c176-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c176-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c176-147">-WhatIf</span></span>
<span data-ttu-id="2c176-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c176-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c176-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c176-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c176-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c176-150">CommonParameters</span></span>
<span data-ttu-id="2c176-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c176-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c176-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c176-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c176-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c176-153">INPUTS</span></span>

## <span data-ttu-id="2c176-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c176-154">OUTPUTS</span></span>

### <span data-ttu-id="2c176-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="2c176-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="2c176-156">Notas</span><span class="sxs-lookup"><span data-stu-id="2c176-156">NOTES</span></span>

<span data-ttu-id="2c176-157">Aliases</span><span class="sxs-lookup"><span data-stu-id="2c176-157">ALIASES</span></span>

## <span data-ttu-id="2c176-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c176-158">RELATED LINKS</span></span>


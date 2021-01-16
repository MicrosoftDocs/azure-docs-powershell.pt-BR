---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259671"
---
# <span data-ttu-id="b0f1a-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="b0f1a-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="b0f1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f1a-103">Crie um novo aplicativo ou atualize um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="b0f1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0f1a-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0f1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f1a-106">Crie um novo aplicativo ou atualize um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="b0f1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f1a-108">Exemplo 1: criar um aplicativo de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="b0f1a-109">Crie um aplicativo em nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="b0f1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="b0f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="b0f1a-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b0f1a-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="b0f1a-112">Nome da implantação ativa do aplicativo</span><span class="sxs-lookup"><span data-stu-id="b0f1a-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="b0f1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0f1a-113">-AsJob</span></span>
<span data-ttu-id="b0f1a-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b0f1a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b0f1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f1a-115">-DefaultProfile</span></span>
<span data-ttu-id="b0f1a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f1a-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="b0f1a-117">-Fqdn</span></span>
<span data-ttu-id="b0f1a-118">Nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="b0f1a-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b0f1a-119">-HttpsOnly</span></span>
<span data-ttu-id="b0f1a-120">Indique se somente HTTPS é permitido.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="b0f1a-121">-Local</span><span class="sxs-lookup"><span data-stu-id="b0f1a-121">-Location</span></span>
<span data-ttu-id="b0f1a-122">A localização geográfica do aplicativo, sempre a mesma com seu recurso pai</span><span class="sxs-lookup"><span data-stu-id="b0f1a-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="b0f1a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0f1a-123">-Name</span></span>
<span data-ttu-id="b0f1a-124">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="b0f1a-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b0f1a-125">-NoWait</span></span>
<span data-ttu-id="b0f1a-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b0f1a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b0f1a-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="b0f1a-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="b0f1a-128">Caminho de montagem do disco persistente</span><span class="sxs-lookup"><span data-stu-id="b0f1a-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="b0f1a-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b0f1a-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="b0f1a-130">Tamanho do disco persistente em GB</span><span class="sxs-lookup"><span data-stu-id="b0f1a-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="b0f1a-131">-Público</span><span class="sxs-lookup"><span data-stu-id="b0f1a-131">-Public</span></span>
<span data-ttu-id="b0f1a-132">Indica se o aplicativo expõe um ponto de extremidade público</span><span class="sxs-lookup"><span data-stu-id="b0f1a-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="b0f1a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f1a-133">-ResourceGroupName</span></span>
<span data-ttu-id="b0f1a-134">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b0f1a-135">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b0f1a-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b0f1a-136">-ServiceName</span></span>
<span data-ttu-id="b0f1a-137">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b0f1a-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0f1a-138">-SubscriptionId</span></span>
<span data-ttu-id="b0f1a-139">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0f1a-140">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b0f1a-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="b0f1a-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="b0f1a-142">Caminho de montagem do disco temporário</span><span class="sxs-lookup"><span data-stu-id="b0f1a-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="b0f1a-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b0f1a-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="b0f1a-144">Tamanho do disco temporário em GB</span><span class="sxs-lookup"><span data-stu-id="b0f1a-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="b0f1a-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0f1a-145">-Confirm</span></span>
<span data-ttu-id="b0f1a-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f1a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f1a-147">-WhatIf</span></span>
<span data-ttu-id="b0f1a-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f1a-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f1a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f1a-150">CommonParameters</span></span>
<span data-ttu-id="b0f1a-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f1a-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0f1a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f1a-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0f1a-153">INPUTS</span></span>

## <span data-ttu-id="b0f1a-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0f1a-154">OUTPUTS</span></span>

### <span data-ttu-id="b0f1a-155">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="b0f1a-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="b0f1a-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0f1a-156">NOTES</span></span>

<span data-ttu-id="b0f1a-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b0f1a-157">ALIASES</span></span>

## <span data-ttu-id="b0f1a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0f1a-158">RELATED LINKS</span></span>


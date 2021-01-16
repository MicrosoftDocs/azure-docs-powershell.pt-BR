---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 859ea1febad82dbb09e88debe3f825feab18b1c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258131"
---
# <span data-ttu-id="beeb8-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="beeb8-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="beeb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="beeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="beeb8-103">Reinicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="beeb8-103">Restart the deployment.</span></span>

## <span data-ttu-id="beeb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="beeb8-104">SYNTAX</span></span>

### <span data-ttu-id="beeb8-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="beeb8-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="beeb8-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="beeb8-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="beeb8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="beeb8-107">DESCRIPTION</span></span>
<span data-ttu-id="beeb8-108">Reinicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="beeb8-108">Restart the deployment.</span></span>

## <span data-ttu-id="beeb8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="beeb8-109">EXAMPLES</span></span>

### <span data-ttu-id="beeb8-110">Exemplo 1: reinicie o serviço de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="beeb8-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="beeb8-111">Reinicie o serviço de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="beeb8-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="beeb8-112">Exemplo 2: reinicie o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="beeb8-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="beeb8-113">Reinicie o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="beeb8-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="beeb8-114">OS</span><span class="sxs-lookup"><span data-stu-id="beeb8-114">PARAMETERS</span></span>

### <span data-ttu-id="beeb8-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="beeb8-115">-AppName</span></span>
<span data-ttu-id="beeb8-116">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="beeb8-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beeb8-117">-AsJob</span></span>
<span data-ttu-id="beeb8-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="beeb8-118">Run the command as a job</span></span>

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

### <span data-ttu-id="beeb8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeb8-119">-DefaultProfile</span></span>
<span data-ttu-id="beeb8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="beeb8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beeb8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="beeb8-121">-InputObject</span></span>
<span data-ttu-id="beeb8-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="beeb8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="beeb8-123">-Name</span></span>
<span data-ttu-id="beeb8-124">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="beeb8-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="beeb8-125">-NoWait</span></span>
<span data-ttu-id="beeb8-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="beeb8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="beeb8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beeb8-127">-PassThru</span></span>
<span data-ttu-id="beeb8-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="beeb8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="beeb8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beeb8-129">-ResourceGroupName</span></span>
<span data-ttu-id="beeb8-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="beeb8-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="beeb8-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="beeb8-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="beeb8-132">-ServiceName</span></span>
<span data-ttu-id="beeb8-133">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="beeb8-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="beeb8-134">-SubscriptionId</span></span>
<span data-ttu-id="beeb8-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="beeb8-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="beeb8-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="beeb8-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeb8-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="beeb8-137">-Confirm</span></span>
<span data-ttu-id="beeb8-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beeb8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beeb8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beeb8-139">-WhatIf</span></span>
<span data-ttu-id="beeb8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="beeb8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beeb8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="beeb8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beeb8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeb8-142">CommonParameters</span></span>
<span data-ttu-id="beeb8-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeb8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeb8-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beeb8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeb8-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="beeb8-145">INPUTS</span></span>

### <span data-ttu-id="beeb8-146">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="beeb8-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="beeb8-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="beeb8-147">OUTPUTS</span></span>

### <span data-ttu-id="beeb8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="beeb8-148">System.Boolean</span></span>

## <span data-ttu-id="beeb8-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="beeb8-149">NOTES</span></span>

<span data-ttu-id="beeb8-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="beeb8-150">ALIASES</span></span>

<span data-ttu-id="beeb8-151">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="beeb8-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="beeb8-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="beeb8-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="beeb8-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="beeb8-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="beeb8-154">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="beeb8-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="beeb8-155">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="beeb8-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="beeb8-156">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="beeb8-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="beeb8-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="beeb8-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="beeb8-158">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="beeb8-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="beeb8-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="beeb8-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="beeb8-160">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="beeb8-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="beeb8-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="beeb8-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="beeb8-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="beeb8-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="beeb8-163">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="beeb8-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="beeb8-164">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="beeb8-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="beeb8-165">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="beeb8-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="beeb8-166">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="beeb8-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="beeb8-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="beeb8-167">RELATED LINKS</span></span>


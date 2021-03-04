---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0de600b2b21d634e85b4ed0266a3b72c95266f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886837"
---
# <span data-ttu-id="2d487-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="2d487-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="2d487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d487-102">SYNOPSIS</span></span>
<span data-ttu-id="2d487-103">Pare a implantação.</span><span class="sxs-lookup"><span data-stu-id="2d487-103">Stop the deployment.</span></span>

## <span data-ttu-id="2d487-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d487-104">SYNTAX</span></span>

### <span data-ttu-id="2d487-105">Parar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d487-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d487-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d487-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d487-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d487-107">DESCRIPTION</span></span>
<span data-ttu-id="2d487-108">Pare a implantação.</span><span class="sxs-lookup"><span data-stu-id="2d487-108">Stop the deployment.</span></span>

## <span data-ttu-id="2d487-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d487-109">EXAMPLES</span></span>

### <span data-ttu-id="2d487-110">Exemplo 1: Pare o Serviço de Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2d487-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="2d487-111">Pare o Serviço de Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2d487-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="2d487-112">Exemplo 2: pare o Serviço de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="2d487-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="2d487-113">Pare o Serviço de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="2d487-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="2d487-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d487-114">PARAMETERS</span></span>

### <span data-ttu-id="2d487-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="2d487-115">-AppName</span></span>
<span data-ttu-id="2d487-116">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="2d487-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d487-117">-AsJob</span></span>
<span data-ttu-id="2d487-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2d487-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2d487-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d487-119">-DefaultProfile</span></span>
<span data-ttu-id="2d487-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d487-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d487-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d487-121">-InputObject</span></span>
<span data-ttu-id="2d487-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2d487-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2d487-123">-Name</span></span>
<span data-ttu-id="2d487-124">O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="2d487-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2d487-125">-NoWait</span></span>
<span data-ttu-id="2d487-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2d487-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d487-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d487-127">-PassThru</span></span>
<span data-ttu-id="2d487-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2d487-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d487-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d487-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d487-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2d487-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2d487-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="2d487-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2d487-132">-ServiceName</span></span>
<span data-ttu-id="2d487-133">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="2d487-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d487-134">-SubscriptionId</span></span>
<span data-ttu-id="2d487-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d487-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d487-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2d487-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d487-137">-Confirm</span></span>
<span data-ttu-id="2d487-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d487-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d487-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d487-139">-WhatIf</span></span>
<span data-ttu-id="2d487-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d487-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d487-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d487-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d487-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d487-142">CommonParameters</span></span>
<span data-ttu-id="2d487-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d487-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d487-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d487-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d487-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d487-145">INPUTS</span></span>

### <span data-ttu-id="2d487-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2d487-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2d487-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d487-147">OUTPUTS</span></span>

### <span data-ttu-id="2d487-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d487-148">System.Boolean</span></span>

## <span data-ttu-id="2d487-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d487-149">NOTES</span></span>

<span data-ttu-id="2d487-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2d487-150">ALIASES</span></span>

<span data-ttu-id="2d487-151">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2d487-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d487-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2d487-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d487-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2d487-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d487-154">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2d487-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d487-155">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="2d487-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2d487-156">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="2d487-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2d487-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="2d487-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2d487-158">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="2d487-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2d487-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2d487-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2d487-160">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2d487-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d487-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="2d487-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2d487-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2d487-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2d487-163">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="2d487-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2d487-164">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="2d487-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2d487-165">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d487-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2d487-166">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2d487-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2d487-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d487-167">RELATED LINKS</span></span>


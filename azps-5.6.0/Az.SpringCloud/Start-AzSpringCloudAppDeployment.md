---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 2c16d60bc9a2b11e34c968eba552c6f8693f92f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885962"
---
# <span data-ttu-id="77dcb-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="77dcb-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="77dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="77dcb-103">Inicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="77dcb-103">Start the deployment.</span></span>

## <span data-ttu-id="77dcb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77dcb-104">SYNTAX</span></span>

### <span data-ttu-id="77dcb-105">Iniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="77dcb-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="77dcb-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="77dcb-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77dcb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77dcb-107">DESCRIPTION</span></span>
<span data-ttu-id="77dcb-108">Inicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="77dcb-108">Start the deployment.</span></span>

## <span data-ttu-id="77dcb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77dcb-109">EXAMPLES</span></span>

### <span data-ttu-id="77dcb-110">Exemplo 1: Iniciar o Serviço de Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="77dcb-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="77dcb-111">Inicie o Serviço de Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="77dcb-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="77dcb-112">Exemplo 2: Iniciar o Serviço de Nuvem de Mola a partir do pipe.</span><span class="sxs-lookup"><span data-stu-id="77dcb-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="77dcb-113">Inicie o Serviço de Nuvem de Mola a partir do pipe.</span><span class="sxs-lookup"><span data-stu-id="77dcb-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="77dcb-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77dcb-114">PARAMETERS</span></span>

### <span data-ttu-id="77dcb-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="77dcb-115">-AppName</span></span>
<span data-ttu-id="77dcb-116">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="77dcb-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77dcb-117">-AsJob</span></span>
<span data-ttu-id="77dcb-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="77dcb-118">Run the command as a job</span></span>

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

### <span data-ttu-id="77dcb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dcb-119">-DefaultProfile</span></span>
<span data-ttu-id="77dcb-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77dcb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77dcb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77dcb-121">-InputObject</span></span>
<span data-ttu-id="77dcb-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="77dcb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="77dcb-123">-Name</span></span>
<span data-ttu-id="77dcb-124">O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="77dcb-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="77dcb-125">-NoWait</span></span>
<span data-ttu-id="77dcb-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="77dcb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="77dcb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77dcb-127">-PassThru</span></span>
<span data-ttu-id="77dcb-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="77dcb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="77dcb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dcb-129">-ResourceGroupName</span></span>
<span data-ttu-id="77dcb-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="77dcb-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="77dcb-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="77dcb-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77dcb-132">-ServiceName</span></span>
<span data-ttu-id="77dcb-133">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="77dcb-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77dcb-134">-SubscriptionId</span></span>
<span data-ttu-id="77dcb-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77dcb-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="77dcb-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="77dcb-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dcb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77dcb-137">-Confirm</span></span>
<span data-ttu-id="77dcb-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77dcb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77dcb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dcb-139">-WhatIf</span></span>
<span data-ttu-id="77dcb-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77dcb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dcb-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77dcb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77dcb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dcb-142">CommonParameters</span></span>
<span data-ttu-id="77dcb-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dcb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dcb-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77dcb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dcb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77dcb-145">INPUTS</span></span>

### <span data-ttu-id="77dcb-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="77dcb-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="77dcb-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77dcb-147">OUTPUTS</span></span>

### <span data-ttu-id="77dcb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77dcb-148">System.Boolean</span></span>

## <span data-ttu-id="77dcb-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="77dcb-149">NOTES</span></span>

<span data-ttu-id="77dcb-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="77dcb-150">ALIASES</span></span>

<span data-ttu-id="77dcb-151">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="77dcb-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="77dcb-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="77dcb-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77dcb-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="77dcb-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="77dcb-154">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="77dcb-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="77dcb-155">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="77dcb-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="77dcb-156">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="77dcb-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="77dcb-157">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="77dcb-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="77dcb-158">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="77dcb-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="77dcb-159">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="77dcb-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="77dcb-160">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="77dcb-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="77dcb-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="77dcb-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="77dcb-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="77dcb-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="77dcb-163">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="77dcb-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="77dcb-164">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="77dcb-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="77dcb-165">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77dcb-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="77dcb-166">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="77dcb-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="77dcb-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77dcb-167">RELATED LINKS</span></span>


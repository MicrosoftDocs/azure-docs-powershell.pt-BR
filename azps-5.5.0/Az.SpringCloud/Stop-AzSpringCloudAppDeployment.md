---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113967"
---
# <span data-ttu-id="3d976-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="3d976-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="3d976-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d976-102">SYNOPSIS</span></span>
<span data-ttu-id="3d976-103">Interromper a implantação.</span><span class="sxs-lookup"><span data-stu-id="3d976-103">Stop the deployment.</span></span>

## <span data-ttu-id="3d976-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d976-104">SYNTAX</span></span>

### <span data-ttu-id="3d976-105">Parar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d976-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d976-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d976-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d976-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d976-107">DESCRIPTION</span></span>
<span data-ttu-id="3d976-108">Interromper a implantação.</span><span class="sxs-lookup"><span data-stu-id="3d976-108">Stop the deployment.</span></span>

## <span data-ttu-id="3d976-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d976-109">EXAMPLES</span></span>

### <span data-ttu-id="3d976-110">Exemplo 1: Interromper o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="3d976-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="3d976-111">Pare o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="3d976-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="3d976-112">Exemplo 2: Interromper o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="3d976-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="3d976-113">Interromper o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="3d976-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="3d976-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d976-114">PARAMETERS</span></span>

### <span data-ttu-id="3d976-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="3d976-115">-AppName</span></span>
<span data-ttu-id="3d976-116">O nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d976-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="3d976-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d976-117">-AsJob</span></span>
<span data-ttu-id="3d976-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3d976-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3d976-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d976-119">-DefaultProfile</span></span>
<span data-ttu-id="3d976-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d976-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d976-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d976-121">-InputObject</span></span>
<span data-ttu-id="3d976-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="3d976-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d976-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d976-123">-Name</span></span>
<span data-ttu-id="3d976-124">O nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="3d976-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="3d976-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d976-125">-NoWait</span></span>
<span data-ttu-id="3d976-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="3d976-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d976-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d976-127">-PassThru</span></span>
<span data-ttu-id="3d976-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3d976-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d976-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d976-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d976-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3d976-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d976-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3d976-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3d976-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3d976-132">-ServiceName</span></span>
<span data-ttu-id="3d976-133">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="3d976-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="3d976-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d976-134">-SubscriptionId</span></span>
<span data-ttu-id="3d976-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d976-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d976-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d976-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3d976-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3d976-137">-Confirm</span></span>
<span data-ttu-id="3d976-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d976-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d976-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d976-139">-WhatIf</span></span>
<span data-ttu-id="3d976-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3d976-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d976-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d976-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d976-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d976-142">CommonParameters</span></span>
<span data-ttu-id="3d976-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d976-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d976-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d976-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d976-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="3d976-145">INPUTS</span></span>

### <span data-ttu-id="3d976-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="3d976-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="3d976-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="3d976-147">OUTPUTS</span></span>

### <span data-ttu-id="3d976-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d976-148">System.Boolean</span></span>

## <span data-ttu-id="3d976-149">Notas</span><span class="sxs-lookup"><span data-stu-id="3d976-149">NOTES</span></span>

<span data-ttu-id="3d976-150">Aliases</span><span class="sxs-lookup"><span data-stu-id="3d976-150">ALIASES</span></span>

<span data-ttu-id="3d976-151">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="3d976-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d976-152">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3d976-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d976-153">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d976-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d976-154">INPUTOBJECT: <ISpringCloudIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="3d976-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d976-155">`[AppName <String>]`: o nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d976-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="3d976-156">`[BindingName <String>]`: o nome do recurso Encadernação.</span><span class="sxs-lookup"><span data-stu-id="3d976-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="3d976-157">`[CertificateName <String>]`: o nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="3d976-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="3d976-158">`[DeploymentName <String>]`: o nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="3d976-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="3d976-159">`[DomainName <String>]`: o nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="3d976-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="3d976-160">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3d976-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d976-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="3d976-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="3d976-162">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3d976-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3d976-163">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3d976-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3d976-164">`[ServiceName <String>]`: o nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="3d976-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="3d976-165">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d976-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3d976-166">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d976-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3d976-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d976-167">RELATED LINKS</span></span>


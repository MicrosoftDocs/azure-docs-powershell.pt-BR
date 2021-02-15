---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116161"
---
# <span data-ttu-id="fd46f-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="fd46f-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="fd46f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd46f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd46f-103">Inicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="fd46f-103">Start the deployment.</span></span>

## <span data-ttu-id="fd46f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd46f-104">SYNTAX</span></span>

### <span data-ttu-id="fd46f-105">Iniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd46f-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fd46f-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd46f-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd46f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd46f-107">DESCRIPTION</span></span>
<span data-ttu-id="fd46f-108">Inicie a implantação.</span><span class="sxs-lookup"><span data-stu-id="fd46f-108">Start the deployment.</span></span>

## <span data-ttu-id="fd46f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd46f-109">EXAMPLES</span></span>

### <span data-ttu-id="fd46f-110">Exemplo 1: Iniciar o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="fd46f-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="fd46f-111">Inicie o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="fd46f-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="fd46f-112">Exemplo 2: Iniciar o Serviço de Nuvem de Primavera a partir do cano.</span><span class="sxs-lookup"><span data-stu-id="fd46f-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="fd46f-113">Inicie o Serviço de Nuvem de Primavera a partir do cano.</span><span class="sxs-lookup"><span data-stu-id="fd46f-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="fd46f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd46f-114">PARAMETERS</span></span>

### <span data-ttu-id="fd46f-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="fd46f-115">-AppName</span></span>
<span data-ttu-id="fd46f-116">O nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd46f-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="fd46f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd46f-117">-AsJob</span></span>
<span data-ttu-id="fd46f-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fd46f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fd46f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd46f-119">-DefaultProfile</span></span>
<span data-ttu-id="fd46f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd46f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd46f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd46f-121">-InputObject</span></span>
<span data-ttu-id="fd46f-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fd46f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd46f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd46f-123">-Name</span></span>
<span data-ttu-id="fd46f-124">O nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="fd46f-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="fd46f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd46f-125">-NoWait</span></span>
<span data-ttu-id="fd46f-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="fd46f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd46f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd46f-127">-PassThru</span></span>
<span data-ttu-id="fd46f-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fd46f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fd46f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd46f-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd46f-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fd46f-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fd46f-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="fd46f-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fd46f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fd46f-132">-ServiceName</span></span>
<span data-ttu-id="fd46f-133">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="fd46f-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="fd46f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd46f-134">-SubscriptionId</span></span>
<span data-ttu-id="fd46f-135">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd46f-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd46f-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fd46f-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd46f-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd46f-137">-Confirm</span></span>
<span data-ttu-id="fd46f-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd46f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd46f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd46f-139">-WhatIf</span></span>
<span data-ttu-id="fd46f-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd46f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd46f-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd46f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd46f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd46f-142">CommonParameters</span></span>
<span data-ttu-id="fd46f-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd46f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd46f-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd46f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd46f-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd46f-145">INPUTS</span></span>

### <span data-ttu-id="fd46f-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="fd46f-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="fd46f-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd46f-147">OUTPUTS</span></span>

### <span data-ttu-id="fd46f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd46f-148">System.Boolean</span></span>

## <span data-ttu-id="fd46f-149">Notas</span><span class="sxs-lookup"><span data-stu-id="fd46f-149">NOTES</span></span>

<span data-ttu-id="fd46f-150">Aliases</span><span class="sxs-lookup"><span data-stu-id="fd46f-150">ALIASES</span></span>

<span data-ttu-id="fd46f-151">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="fd46f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd46f-152">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fd46f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd46f-153">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd46f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd46f-154">INPUTOBJECT: <ISpringCloudIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="fd46f-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd46f-155">`[AppName <String>]`: o nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd46f-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="fd46f-156">`[BindingName <String>]`: o nome do recurso Encadernação.</span><span class="sxs-lookup"><span data-stu-id="fd46f-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="fd46f-157">`[CertificateName <String>]`: o nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="fd46f-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="fd46f-158">`[DeploymentName <String>]`: o nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="fd46f-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="fd46f-159">`[DomainName <String>]`: o nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="fd46f-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="fd46f-160">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fd46f-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd46f-161">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="fd46f-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="fd46f-162">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="fd46f-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fd46f-163">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="fd46f-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fd46f-164">`[ServiceName <String>]`: o nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="fd46f-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="fd46f-165">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd46f-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fd46f-166">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fd46f-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fd46f-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd46f-167">RELATED LINKS</span></span>

